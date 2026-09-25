# secure-push-workflow

Orchestrate the full "package → security scan → push" pipeline for a local project, calling github-ready-packager, secret-scan, and acp-studio in order with a hard gate that stops on any security finding. Use when the user asks to publish, ship, or push a local project to GitHub/Gitee end-to-end and wants safety enforced automatically. Not for editing code, single commits, or sync-only requests.

## 这是什么

DSH（DeepSeek Harness）skill —— 一个可由 AI agent 按需自动加载的能力单元。克隆到 skill 目录后，DSH 会依据上方描述自动发现并触发它，无需构建。

## 安装

最简单：用 [dsh-config](https://github.com/hpsks416/dsh-config) 的一键脚本 `install.ps1` 批量安装全部 skill。单个安装：

    # GitHub
    git clone https://github.com/hpsks416/secure-push-workflow.git "$env:USERPROFILE\.dsh\skills\secure-push-workflow"
    # 或 Gitee（国内直连更快）
    git clone https://gitee.com/hpsks416/secure-push-workflow.git "$env:USERPROFILE\.dsh\skills\secure-push-workflow"

克隆后 DSH 会自动重新发现，无需重启。更新用：

    git -C "$env:USERPROFILE\.dsh\skills\secure-push-workflow" pull

## 目录结构

    secure-push-workflow/
    ├── SKILL.md    技能入口与工作流
    ├── evals.yaml

## 依赖

无运行时依赖，纯指令型 skill（由 agent 直接执行 Markdown 工作流）。

## License

MIT License. See [LICENSE](LICENSE).
