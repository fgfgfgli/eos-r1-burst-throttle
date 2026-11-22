# Canon EOS R1 连拍节流研究（burst throttle）

> **一句话**：对 Canon EOS R1（固件 1.3.0）连拍「缓冲写满就停」行为的研究记录——定位判决点、测缓冲水位、试了三轮错误方案，最后用「改写结论」的方式把长时间 busy 变成短停顿。
> **研究记录，不是产品、工具或教程。**

**作者 / Author**：**fgfgfgli**
**仓库 / Repository**：<https://github.com/fgfgfgli/eos-r1-burst-throttle>
**许可 / License**：**CC BY-NC 4.0**（署名 + 非商业）

> **引用 / Citation**：基于本文做新机型研究、写文档或在公开场合讲解，请注明 **fgfgfgli** 与仓库链接，并说明是否修改。详见 [NOTICE.md](NOTICE.md) 与 [CITATION.cff](CITATION.cff)。

## 结论

- 连拍的「停」是**前端缓冲写满**造成的（挂起瞬间空位 3/40），不是帧数配额；
- 把「继续拍」（规则 0）改写成「挂起」（规则 1），复用相机自己的挂起路径 ⇒ **非阻塞**的「拍一阵 → 停一下 → 再拍一阵」；
- 实测等效约 **15–20 fps**，是顿挫，不是平滑降速；
- 自旋方案在「AF-ON 快速切档 + 连拍」下会偶发 Err70，**已放弃**。

## 文档

- [docs/burst-throttle.md](docs/burst-throttle.md) — 准入链、规则号、四个闸门、缓冲水位、三轮失败、最终方案、边界与复盘。

## 边界

- 只到机制与证据等级；**跳板/桩布局、落点地址、写入常量不在公开版**；
- 不提供安装步骤、不提供可执行材料、不承诺任何机型可用；
- RAM-only 改动，断电即恢复；使用风险自负（见 [DISCLAIMER.md](DISCLAIMER.md)）。

## 署名

连拍降速（burst throttle）方案来自 **fgfgfgli** 的 Canon EOS R1 研究。
转载、演绎或在公开场合讲解，请署名并附仓库链接（CC BY-NC 4.0）。
