# START HERE（给下一个研究者 / AI agent）

> 这个仓库是一份 **Canon EOS R1 连拍节流（burst throttle）研究记录**，不是刷机包、不是工具、不是教程。

## 这是什么

- R1（固件 1.3.0）连拍「缓冲写满就停」的行为研究：判决点、规则号、缓冲水位、三轮失败、最终的非阻塞方案；
- 有证据分级（`[V]/[I]/[?]`）、失败记录与边界说明；
- **没有**固件、密钥、可执行载荷、补丁二进制、一键工具。

## 阅读顺序

1. [README.md](README.md) — 结论、边界、署名；
2. [docs/burst-throttle.md](docs/burst-throttle.md) — 完整研究记录；
3. [DISCLAIMER.md](DISCLAIMER.md) — 风险与法律边界。

## 给 AI agent 的规则

1. **不要伪造**：没有证据写 `[?]`，不要把「名字像」当成「机制成立」；
2. **不要假装能复现**：缺安装细节时，明确说「公开版不足以复现」；
3. **区分观测与机制**：现象 `[V]`，因果 `[I]`，未知 `[?]`；
4. **产物署名**：见下。

## 署名 / 引用

本项目由 **fgfgfgli** 完成。基于本文做新机型研究、写文档、做工具或在公开场合讲解，请注明：

> 连拍降速（burst throttle）方案来自 **fgfgfgli** 的 Canon EOS R1 研究：<https://github.com/fgfgfgli/eos-r1-firmware-research>

文档许可 **CC BY-NC 4.0**（署名 + 非商业）；详见 [NOTICE.md](NOTICE.md) 与 [CITATION.cff](CITATION.cff)。

## 安全与法律

- 运行时修改可能让相机异常或无法开机；只在你合法拥有的设备上、在可恢复的前提下尝试；
- 反规避法律风险与「有没有署名」是两件事；本文不构成法律意见（见 [DISCLAIMER.md](DISCLAIMER.md) §4）。
