# 发版说明

本文件的内容会成为 GitHub Release 的正文，并进入 `latest.json` 的 `notes` 字段 ——
桌面端的更新对话框和安卓端的更新对话框都直接展示它，所以请当成**给用户看的**文案写，
不要写成 commit log。

**它同时是发布的触发器**：`.gitea/workflows/push_to_release_repo.yml` 在打 `v*` tag 时
把本文件推到发布仓，发布仓的 `release.yml` 监听的正是本文件的变更。内容没变就不会发布。

发版前记得同步改 `src-tauri/tauri.conf.json` 的 `version` —— **构建出的版本号取自那里，
不是 tag**，两者不一致时 tag 只是个标记，装到用户机器上的是 conf 里的那个号。

---

## v0.1.0

首个版本。
