# 短剧与改编 Skill 更新

短剧和改编 Skill 同步到 **v2026.11.27.1**。短剧用于客户成稿校对和资产制作，改编用于母版改编及后续资产制作。

- [短剧 Skill v2026.11.27.1](https://github.com/yangyang169169169-source/tiktok-custom-drama-production/releases/tag/v2026.11.27.1)
- [改编 Skill v2026.11.27.1](https://github.com/yangyang169169169-source/short-drama-adaptation-pipeline/releases/tag/v2026.11.27.1)

人物定妆增加正脸颊颌验收。平视正脸比较嘴角高度及略低处的左右轮廓，发现无依据的单侧凸起时定位到具体一段做局部修正。首套验收通过后用作锁脸母版，后续换装继续核对该处。保留角色原有五官、骨相与有依据的自然差异。

## 可直接发给 Codex

```text
请把短剧与改编 Skill 更新到 2026.11.27.1。
短剧下载页 https://github.com/yangyang169169169-source/tiktok-custom-drama-production/releases/tag/v2026.11.27.1
改编下载页 https://github.com/yangyang169169169-source/short-drama-adaptation-pipeline/releases/tag/v2026.11.27.1

从各 Release 的 Assets 下载版本 ZIP 及同名 .zip.sha256。先确认本机实际加载的 Skill 目录、符号链接和本机定制，备份现用版及参考库配置。在下载目录用 shasum -a 256 -c <ZIP 文件名>.sha256 校验 ZIP，再解压进入含 SKILL.md 的目录，用 shasum -a 256 -c FILES.sha256 校验包内文件。Windows 可用系统等效 SHA-256 命令。按现有入口更新，保留本机人脸和服装库路径及适用的定制。回报实际入口、SKILL.md 版本、校验结果及备份位置。

新版在人像正脸检查左右下颊在同一高度的宽度和弧线。单侧凸起按局部轮廓修正，保留角色身份，首套通过后再用于锁脸。新项目继续使用 16:9 白底三栏四视图，历史项目沿用已确认规格。这次只更新 Skill。资产生成、历史返修和视频制作按使用者当次授权执行。
```

改编步骤1的剧本检索仍使用已有的 `script-library-reviewer`，已知底本可按原流程从步骤2开始。参考库路径配置位于 `references/共享主演参考库配置.json`。
