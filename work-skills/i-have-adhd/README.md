# i-have-adhd

> 適用於 ChatGPT Work ，讓 ChatGPT Work 知道你有 ADHD 的 Skill，讓chatGPT的回覆更容易閱讀、開始執行及持續完成。
>
> A Skill for ChatGPT Work that lets ChatGPT know you have ADHD, so its responses are easier to read, act on, and follow through to completion.

[下載 i-have-adhd.zip](./i-have-adhd.zip)

SHA-256：`a8cd3d8047b3f49bfbf05d6c069d022cafd301457abe9e4a267ad6681391253b`

---

## 繁體中文

### 關於這個 Skill

這是我目前在 ChatGPT Work 中實際使用的第三方改良 Skill。

它會調整 ChatGPT 的回覆呈現方式，讓回答更容易閱讀與執行。它的目的不只是縮短內容，而是降低開始任務、記住目前進度及完成多步驟工作的困難。

這是回覆格式與工作流程輔助工具，不是醫療診斷或治療工具。

### 我的用途

我主要在進行專案規劃、故障排除、學習新內容及多步驟操作時使用這個 Skill。

它會要求 ChatGPT：

1. 先給出現在可以執行的下一個動作。
2. 將多步驟工作整理成清楚的編號步驟。
3. 在後續回覆中重新說明目前進度、時間估計及已完成成果。
4. 減少無關延伸，並直接說明錯誤原因與處理方法。
5. 以一個具體的下一步結束，避免不必要的開場與客套結尾。

### 我的安裝方式

1. 下載 [`i-have-adhd.zip`](./i-have-adhd.zip)，不需要解壓縮。
2. 開啟 ChatGPT 網頁版。
3. 從左側選單進入「外掛程式」，再選擇「技能」。
4. 點擊 `+`，選擇「從電腦上傳」。
5. 選擇下載的 `i-have-adhd.zip`，等待安裝完成。

### 我的使用方式

1. 在需要使用的 ChatGPT Work 對話中，透過 Skill 選單或 `@I Have ADHD` 明確呼叫一次。
2. 呼叫後，直接告訴 ChatGPT 目前需要處理的任務。
3. Skill 會要求後續回覆在同一個對話中持續採用 ADHD 友善格式。
4. 如需停止，可輸入 `stop adhd mode` 或 `normal mode`。

此版本不會自動啟動。只有明確呼叫後，才會加入目前對話。

### Repository 中的檔案

| 檔案                | 作用                                |
| ----------------- | --------------------------------- |
| `README.md`       | 說明我的用途、安裝方式、使用方式、檔案結構、來源、授權及主要修改。 |
| `i-have-adhd.zip` | 可直接上傳至 ChatGPT Work 的 Skill 安裝包。  |

### ZIP 中的檔案

| 檔案                               | 作用                                     |
| -------------------------------- | -------------------------------------- |
| `i-have-adhd/SKILL.md`           | Skill 的核心指令，定義持續生效方式、ADHD 友善回覆原則及輸出規則。 |
| `i-have-adhd/agents/openai.yaml` | ChatGPT Work 使用的顯示名稱、簡短說明、預設提示及呼叫政策。   |
| `i-have-adhd/LICENSE`            | 原專案的完整 MIT 授權條款及原作者著作權聲明。              |

`agents/openai.yaml` 中的 `allow_implicit_invocation` 設為 `false`，代表這個 Skill 必須由使用者明確呼叫，不會自動加入對話。

### 來源與授權

| 項目      | 資訊                                                                     |
| ------- | ---------------------------------------------------------------------- |
| 原作者     | Ayoub Ghriss                                                           |
| 原始專案    | [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd)            |
| 採用的上游版本 | [0.2.0](https://github.com/ayghri/i-have-adhd/blob/main/package.json)  |
| 授權      | [MIT License](https://github.com/ayghri/i-have-adhd/blob/main/LICENSE) |

MIT License 允許使用、複製、修改、發布及重新散布。本安裝包保留完整的原作者著作權聲明與 MIT 授權條款。

這是依照我的 ChatGPT Work 使用需求整理的修改版本，不是原作者發布的官方安裝包。

### 主要修改

1. 將說明與封裝內容調整為主要適用於 ChatGPT Work。
2. 移除 ChatGPT Work 不需要的 `agents/gemini.toml`。
3. 將完整的原始 MIT `LICENSE` 加入安裝包。
4. 將 `allow_implicit_invocation` 設為 `false`，改成手動呼叫。
5. 移除目前驗證器不支援的 `disable-model-invocation` 欄位，並整理 metadata 格式；原本的核心回覆規則保持不變。

### 隱私與安全

公開檔案及安裝包皆不包含：

* API 金鑰、密碼或其他憑證
* 私人電腦路徑
* 個人對話紀錄
* 與 ChatGPT Work 無關的設定

### 免責聲明

這是獨立整理及維護的第三方修改版本，不是 OpenAI 官方專案，也不代表 OpenAI 或原作者的認可或背書。

---

## English

### About This Skill

This is a third-party Skill that I adapted and actively use in ChatGPT Work.

It changes how ChatGPT presents responses so they are easier to read and act on. Its purpose is not merely to shorten responses, but to reduce the difficulty of starting tasks, remembering the current state, and completing multi-step work.

This is a response-formatting and workflow aid. It is not a medical diagnosis or treatment tool.

### My Purpose

I mainly use this Skill for project planning, troubleshooting, learning new material, and completing multi-step tasks.

It instructs ChatGPT to:

1. Lead with the next action that can be performed immediately.
2. Organize multi-step work into clearly numbered steps.
3. Restate the current state, time estimate, and completed progress in later responses.
4. Suppress unrelated tangents and explain errors and fixes directly.
5. End with one concrete next step while avoiding unnecessary introductions and closing pleasantries.

### My Installation Method

1. Download [`i-have-adhd.zip`](./i-have-adhd.zip) without extracting it.
2. Open the ChatGPT website.
3. Open “Plugins” from the sidebar, then select “Skills.”
4. Click `+` and select “Upload from computer.”
5. Select the downloaded `i-have-adhd.zip` and wait for installation to finish.

### My Usage

1. In the ChatGPT Work conversation where I need it, I explicitly invoke the Skill through the Skill selector or with `@I Have ADHD`.
2. After invoking it, I give ChatGPT the task I want to complete.
3. The Skill instructs ChatGPT to continue using the ADHD-friendly format for the remainder of the same conversation.
4. To stop it, I enter `stop adhd mode` or `normal mode`.

This version does not activate automatically. It is added to a conversation only after explicit invocation.

### Repository Files

| File              | Purpose                                                                                              |
| ----------------- | ---------------------------------------------------------------------------------------------------- |
| `README.md`       | Documents my purpose, installation method, usage, file structure, source, license, and main changes. |
| `i-have-adhd.zip` | The Skill installation package that can be uploaded directly to ChatGPT Work.                        |

### Files Inside the ZIP

| File                             | Purpose                                                                                                    |
| -------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `i-have-adhd/SKILL.md`           | Contains the core instructions, persistence behavior, ADHD-friendly response principles, and output rules. |
| `i-have-adhd/agents/openai.yaml` | Defines the ChatGPT Work display name, short description, default prompt, and invocation policy.           |
| `i-have-adhd/LICENSE`            | Contains the complete upstream MIT License and original copyright notice.                                  |

In `agents/openai.yaml`, `allow_implicit_invocation` is set to `false`. This means the Skill must be explicitly invoked and will not be added to conversations automatically.

### Source and License

| Item                  | Information                                                            |
| --------------------- | ---------------------------------------------------------------------- |
| Original author       | Ayoub Ghriss                                                           |
| Upstream project      | [ayghri/i-have-adhd](https://github.com/ayghri/i-have-adhd)            |
| Upstream version used | [0.2.0](https://github.com/ayghri/i-have-adhd/blob/main/package.json)  |
| License               | [MIT License](https://github.com/ayghri/i-have-adhd/blob/main/LICENSE) |

The MIT License permits use, copying, modification, publication, and redistribution. This installation package retains the complete original copyright notice and MIT License terms.

This is a modified package prepared for my ChatGPT Work usage. It is not an official installation package published by the original author.

### Main Changes

1. Adjusts its description and package contents primarily for ChatGPT Work.
2. Removes `agents/gemini.toml`, which is not needed by ChatGPT Work.
3. Includes the complete upstream MIT `LICENSE` in the installation package.
4. Sets `allow_implicit_invocation` to `false` for explicit-only invocation.
5. Removes the unsupported `disable-model-invocation` field and normalizes the metadata format while preserving the original core response rules.

### Privacy and Safety

The public files and installation package do not contain:

* API keys, passwords, or other credentials
* Private computer paths
* Personal conversation records
* Settings unrelated to ChatGPT Work

### Disclaimer

This is an independently prepared and maintained third-party modification. It is not an official OpenAI project and is not affiliated with or endorsed by OpenAI or the original author.
