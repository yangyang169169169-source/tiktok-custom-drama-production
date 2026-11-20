# 两套 Skill 同步交接

发布版本：`v2026.11.21.1`（2026-11-21）。这是一次手动发布，自动 GitHub 同步保持停止。

## 固定下载入口

- 短剧 Skill：[发布页](https://github.com/yangyang169169169-source/tiktok-custom-drama-production/releases/tag/v2026.11.21.1) · [安装 ZIP](https://github.com/yangyang169169169-source/tiktok-custom-drama-production/releases/download/v2026.11.21.1/tiktok-custom-drama-production-v2026.11.21.1.zip) · [ZIP SHA-256](https://github.com/yangyang169169169-source/tiktok-custom-drama-production/releases/download/v2026.11.21.1/tiktok-custom-drama-production-v2026.11.21.1.zip.sha256)
- 改编 Skill：[发布页](https://github.com/yangyang169169169-source/short-drama-adaptation-pipeline/releases/tag/v2026.11.21.1) · [安装 ZIP](https://github.com/yangyang169169169-source/short-drama-adaptation-pipeline/releases/download/v2026.11.21.1/short-drama-adaptation-pipeline-v2026.11.21.1.zip) · [ZIP SHA-256](https://github.com/yangyang169169169-source/short-drama-adaptation-pipeline/releases/download/v2026.11.21.1/short-drama-adaptation-pipeline-v2026.11.21.1.zip.sha256)

使用本次固定版本的 Release ZIP，而不是浮动的 main。两个 ZIP 各自包含一个同名 Skill 根目录。

## 给接收者 Agent 的同步指令

```text
请从以上两套 GitHub Release 下载并同步 v2026.11.21.1 的 tiktok-custom-drama-production 和 short-drama-adaptation-pipeline，只做安装更新与核验。

1. 先查找当前工作区和个人目录的同名 Skill，核对实际加载入口及是否存在符号链接。备份将更新的同名目录及本机参考库配置；沿用已有的唯一维护源，不另造会被旧入口遮蔽的副本。没有既有安装时，默认安装到目标项目的 .agents/skills/ 下，两套分别保持同名目录。
2. 下载两个 ZIP 和对应 .sha256，核对 ZIP 的 SHA-256 后解压。逐文件校验各包 SOURCE_SHA256.json 的 files 字段及 FILES.sha256，保留完整目录结构。
3. 对照旧版定制；保留接收者自己的参考库路径、已有角色身份和项目规则。两套仅替换自身运行文件；不覆盖其他 Skill、AGENTS.md、账号、API 密钥、浏览器配置或项目文件。发现与本次新标准冲突的定制，说明具体冲突并按当次指令处理。
4. 短剧 Skill 为客户成稿最小校对与人物、场景、道具资产流程。改编 Skill 为项目维护版 2026.11.21.1，保留原剧集数、分集边界、自然时长及步骤1—4，不装回旧版固定50集／2分钟的流程。
5. 核对两套均包含人物肤质脸型与服装验收规则：默认白皙细嫩无瑕，前10集出镜角色覆盖；主要女性小巧柔V脸；成年主要女性按剧情提高合适露肤度并显曲线；男女均不露点、乳晕或透点；男主及主要男配参考顶级男模或男演员的协调脸型骨相，避免太长太方太大；每套仅常规定妆三联板，无独立UpperBody派生图。要求须进入完整提示词及实际看图验收。
6. 公开包只含规则，没有私人参考图片或参考库。优先保留已有 references/共享主演参考库配置.json；新安装时把其中 library_root 和 clothing_library_root 指向接收者实际的人脸与服装库。默认相对路径适用于项目 .agents/skills/ 布局，相对 SKILL.md 根目录解析。未取得素材时如实标记，不创建空库冒充已有参考；不得读取不存在的原作者电脑路径。
7. 使用接收者自己的已授权工具。改编步骤1的剧本库检索需另有 script-library-reviewer；已有母本可从步骤2开始。此次安装不制作剧本、生成资产、操作画布、收费、发布项目、恢复冻结视频阶段或启用自动同步。
8. 完成后列出两套实际路径、版本、SHA-256核验结果、备份位置、参考库与依赖状态。需要重新加载时新开聊天再核对实际读取路径，不能仅凭文件复制完成声称已加载。
9. 核对新增 references/女性服装穿搭备选参考.md 及主入口和服装调研中的链接。7组影视、女星及博主仅作非必选候选，角色、年代、年龄和场合适配时再网上或小红书查具体造型，可全部不采用，不要求逐项搜索；实际采用时记录来源、借鉴部位与本剧调整，不把文字名单冒充已看图。
```

## 本机核验

在 ZIP 所在目录使用 `shasum -a 256 -c 对应文件.zip.sha256`（macOS）或 `sha256sum -c 对应文件.zip.sha256`（Linux）；Windows PowerShell 可用 `Get-FileHash 对应文件.zip -Algorithm SHA256` 对照 `.sha256` 内容。

`SOURCE_SHA256.json` 的 `files` 是发布后运行文件的哈希；`source_sha256` 用于追溯维护源，不能拿它校验经过路径适配的发布文件。解压后也可在各 Skill 根目录用 `shasum -a 256 -c FILES.sha256` 核对整包文件。

核验文件、规则与依赖完整不等于已验证生成图片效果。参考库、客户原稿、项目、登录与密钥不在公开仓库中。
