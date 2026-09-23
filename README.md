# secure-push-workflow

Orchestrate the full "package → security scan → push" pipeline for a local project, calling github-ready-packager, secret-scan, and acp-studio in order with a hard gate that stops on any security finding. Use when the user asks to publish, ship, or push a local project to GitHub/Gitee end-to-end and wants safety enforced automatically. Not for editing code, single commits, or sync-only requests.

## License

MIT License. See [LICENSE](LICENSE).

