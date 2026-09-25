# secure-push-workflow

把「打包 → 安检 → 推送」这条链固化为一个显式的策略编排层。它自己不做任何底层脏活，只做**调度 + 决策 + 门控**：按顺序调用三个底层 skill，并在安检不通过时硬性停住。

## 环境依赖

- 操作系统：Windows
- 运行时：无（纯指令型 skill，由 agent 直接执行）
- 第三方软件：无（仅依赖系统自带的 PowerShell / 标准库）

## 目录结构

    secure-push-workflow/
    ├── SKILL.md    技能入口与工作流
    ├── evals.yaml

## 安装

    # GitHub
    git clone https://github.com/hpsks416/secure-push-workflow.git "$env:USERPROFILE\.dsh\skills\secure-push-workflow"
    # 或 Gitee（国内直连）
    git clone https://gitee.com/hpsks416/secure-push-workflow.git "$env:USERPROFILE\.dsh\skills\secure-push-workflow"

克隆后 DSH 自动重新发现，无需构建。

## License

MIT License. See [LICENSE](LICENSE).
