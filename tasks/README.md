# tasks

`tasks/` 是本地 Agent 与云端调度之间的任务交接目录。

本地 Agent 把待办写到 `tasks/inbox.md` 并推到 `main` 后，GitHub Action 会叫醒云端调度，由云端读取任务并执行。
