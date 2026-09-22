# Ponytail

## 繁體中文

讓 Codex 在寫程式、修正問題與重構時，優先重用現有程式，減少不必要的程式碼與依賴。

適用於 **Windows 11 的本機 Codex Desktop／CLI**。這份 README 是使用說明，`INSTALL_PROMPT.txt` 是交給 Codex 的安裝指令。

### 安裝

1. 開啟 [INSTALL_PROMPT.txt](./INSTALL_PROMPT.txt) 的原始文字（Raw），或下載後開啟。
2. 全選並複製內容，貼到本機 Codex 對話送出。
3. 查看 Codex 的安裝結果；安裝完成後若找不到 Skill，重新啟動 Codex。

已安裝者不必重裝。Prompt 要求 Codex 先檢查，找到既有安裝就停止。

### 使用

在 Skill 選單選取 `ponytail`，再描述需求。

CLI 範例：

```text
$ponytail full
簡化目前專案中重複的程式碼，保留既有功能並驗證修改結果。
```

`lite` 提出簡化建議；`full` 主動簡化；`ultra` 先檢視需求與方案的必要性。

依上游設計，啟用後會在目前對話持續套用；輸入 `stop ponytail` 或 `normal mode` 可要求停止。

### 來源與調整

作者：Dietrich Gebert · [上游來源與選用版本（v4.10.0）](https://github.com/DietrichGebert/ponytail/tree/e3ba2aa6f1e6f0bc4d69eb09c9f0d0a93af56156/skills/ponytail) · [上游授權：MIT](https://github.com/DietrichGebert/ponytail/blob/e3ba2aa6f1e6f0bc4d69eb09c9f0d0a93af56156/LICENSE)

安裝使用固定版本，保留上游指令及授權，並設定為手動呼叫才啟動。

註：安裝 Prompt 僅在維護者的電腦上測試過，尚未在全新 Windows 環境或其他電腦上測試。

---

## English

Helps Codex reuse existing code and reduce unnecessary code and dependencies when developing, fixing bugs, or refactoring.

For **local Codex Desktop / CLI on Windows 11**. This README is the usage guide; `INSTALL_PROMPT.txt` contains the instructions to give Codex.

### Install

1. Open [INSTALL_PROMPT.txt](./INSTALL_PROMPT.txt) in Raw view, or download and open it.
2. Copy the entire contents and send them in a local Codex conversation.
3. Read the installation result. If installation succeeds but the Skill is missing, restart Codex.

The prompt instructs Codex to check first and stop if an installation exists, without reinstalling it.

### Use

Select `ponytail` from the Skill picker, then describe the task.

CLI example:

```text
$ponytail full
Simplify duplicated code in this project, preserve existing behavior,
and verify the changes.
```

`lite` suggests simplifications; `full` actively simplifies; `ultra` first examines whether the requirements and approach are necessary.

The upstream instructions keep Ponytail active in the current conversation after invocation. Use `stop ponytail` or `normal mode` to request deactivation.

### Source and adaptations

Author: Dietrich Gebert · [Upstream source and selected version (v4.10.0)](https://github.com/DietrichGebert/ponytail/tree/e3ba2aa6f1e6f0bc4d69eb09c9f0d0a93af56156/skills/ponytail) · [Upstream license: MIT](https://github.com/DietrichGebert/ponytail/blob/e3ba2aa6f1e6f0bc4d69eb09c9f0d0a93af56156/LICENSE)

Installation uses a pinned revision, preserves upstream instructions and licensing, and configures explicit invocation.

Note: The installation prompt has only been tested on the maintainer's computer. It has not been tested in a clean Windows environment or on other computers.
