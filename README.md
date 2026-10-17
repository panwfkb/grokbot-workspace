# grokbot-workspace

本地 Agent 与「云端调度」之间的任务交接仓。

## 用法

1. 本地 Agent 把任务写到 `tasks/inbox.md`（或 `tasks/` 下任意 `.md`）并 push 到 `main`。
2. GitHub Action 会 POST 叫醒云端调度。
3. 云端调度读取最新任务文档并执行。

## Secrets（仓库 Settings → Secrets and variables → Actions）

- `GROKBOT_WEBHOOK_URL`：云端调度例行任务里的 Webhook 地址
- `GROKBOT_WEBHOOK_TOKEN`：发送密钥（Bearer 后面那串，不含 `Bearer `）
