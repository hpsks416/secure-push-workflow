# secure-push-workflow

把「打包 → 安检 → 推送」这条链固化为一个显式的策略编排层。它自己不做任何底层脏活，只做**调度 + 决策 + 门控**：按顺序调用三个底层 skill，并在安检不通过时硬性停住。

## 适用对象

- DeepSeek Harness（DSH）用户：一个可由 AI agent 按需自动加载的 skill，克隆即用、无需构建。
- 需要「打包→安检→推送」端到端发布的人

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
