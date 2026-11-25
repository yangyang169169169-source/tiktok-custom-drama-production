# 三套 Skill 安装更新

GitHub 发布标签为 `v2026.11.25.1`。短剧和改编 Skill 版本为 `2026.11.25.1`，动画 Skill 版本为 `0.8.2-character-board-20261125`。

- 短剧 Skill：[发布页](https://github.com/yangyang169169169-source/tiktok-custom-drama-production/releases/tag/v2026.11.25.1)
- 改编 Skill：[发布页](https://github.com/yangyang169169169-source/short-drama-adaptation-pipeline/releases/tag/v2026.11.25.1)
- 动画 Skill：[发布页](https://github.com/yangyang169169169-source/animation-skill/releases/tag/v2026.11.25.1)

## 可复制给其他 Codex

```text
从上述三个 GitHub Release 下载 v2026.11.25.1 对应的 ZIP 和 .zip.sha256，只进行 Skill 安装更新。
确认每个同名 Skill 的实际加载入口与符号链接。备份当前运行目录及本机参考库配置。核对下载 ZIP 的 SHA-256 后解压，在解压后含 FILES.sha256 的目录执行 shasum -a 256 -c FILES.sha256，或使用系统等效命令。短剧与改编使用该目录作为 Skill 根目录，动画使用其中带 SKILL.md 的 animation-skill/ 子目录。保留原有参考库路径和无冲突定制。如果本机定制仍要求单近景或全身面部清晰，核对它的适用范围并仅处理与新项目构图冲突的部分。报告实际入口、版本、核验与备份位置。
新项目完整定妆图为横版 16:9 白底三栏四视图。左栏正面全身，中栏 45° 三分之四全身，两张仅局部虚化面部。右栏上方为清晰正脸，下方为清晰 45° 三分之四侧转近景。发型轮廓、身形、衣装及配饰应清楚。同角色同造型的四视图交付为一张常规定妆图，身份锁定和视频参考直接使用整板。动画非人角色按实际面部、表情或身份结构取景，无可辨面部的完整形态保持清楚。
历史项目沿用确认规格。此次只更新 Skill，自动同步仍停用，安装不启动剧本改写、资产生成、画布、视频、超分、剪辑或导出。
```

短剧 Skill 用于客户成稿校对与资产，改编 Skill 保留原剧集数、分集边界、自然时长和步骤1—4。改编步骤1的剧本检索单独依赖 script-library-reviewer。已有母本可从步骤2开始。需要本机参考库时，保留已有的 `references/共享主演参考库配置.json`，或将其中路径指向接收端实际参考库。
