# grill-me

> 適用於 ChatGPT Work，透過決策樹與分輪提問，在執行前壓力測試計畫、設計或想法的 Skill。
>
> A Skill for ChatGPT Work that stress-tests a plan, design, or idea through decision-tree interview rounds before action is taken.

[下載 grill-me.zip](./grill-me.zip)

SHA-256：`b341cefbc97dcaf76bb71b9204e40df12f66ce03e5964a0c91592713dc50bd9e`

---

## 繁體中文

### 關於這個 Skill

這是我目前在 ChatGPT Work 中實際使用的第三方改良 Skill。

它會在執行計畫、設計或想法以前，先將尚未確定的問題整理成具有依賴關係的決策樹，並分輪詢問目前已具備回答條件的問題。

需要查找的客觀事實由 ChatGPT 負責調查；需求、優先順序、取捨及驗收標準等主觀決策則保留給使用者決定。

這是決策釐清與計畫壓力測試工具，不代表計畫一定正確、完整、無問題，但也不會在尚未確認共同理解以前直接開始執行。

### 我的用途

我主要在規劃專案、確認需求、設計系統、選擇工作流程及進行重要決策時使用這個 Skill。

它會要求 ChatGPT：

1. 將計畫、設計或想法整理成具有依賴關係的決策樹。
2. 每輪只詢問目前可以獨立回答的問題，並提供選項、取捨及建議答案。
3. 主動查找可以從對話、檔案、連接來源、檔案系統、網路或工具取得的事實。
4. 根據每輪回答更新決策樹，再詢問下一批已解除依賴的問題。
5. 在所有重要分支完成後，取得使用者的明確確認才可進入後續行動。

### 我的安裝方式

1. 下載 [`grill-me.zip`](./grill-me.zip)，不需要解壓縮。
2. 開啟 ChatGPT 網頁版。
3. 從左側選單進入「外掛程式」，再選擇「技能」。
4. 點擊 `+`，選擇「從電腦上傳」。
5. 選擇下載的 `grill-me.zip`，等待安裝完成。

### 我的使用方式

1. 在需要使用的 ChatGPT Work 對話中，透過 Skill 選單或 `@Grill Me` 明確呼叫。
2. 提供想要檢查的計畫、設計、需求或想法。
3. 依照對話中列出的編號或字母，以文字輸入選項或自己的答案；同一輪可一次回答多題，不使用可點擊式選項。
4. ChatGPT 會根據回答重新整理決策樹，並繼續詢問下一輪問題。
5. 決策樹完成後，確認或修正 ChatGPT 整理出的共同理解，再另外指示是否整理結論、撰寫計畫或開始執行。

此版本不會自動啟動。只有使用者明確呼叫後，才會開始 Grill Me 訪談流程。

### Repository 中的檔案

| 檔案 | 作用 |
| --- | --- |
| `README.md` | 說明我的用途、安裝方式、使用方式、檔案結構、來源、授權及主要修改。 |
| `grill-me.zip` | 可直接上傳至 ChatGPT Work 的 Skill 安裝包。 |

### ZIP 中的檔案

| 檔案 | 作用 |
| --- | --- |
| `grill-me/SKILL.md` | Skill 的核心指令，定義決策樹、問題前緣、分輪訪談、事實查找及完成確認規則。 |
| `grill-me/agents/openai.yaml` | ChatGPT Work 使用的顯示名稱、簡短說明、預設提示及呼叫政策。 |
| `grill-me/LICENSE` | 原始專案的完整 MIT 授權條款及原作者著作權聲明。 |

`agents/openai.yaml` 中的 `allow_implicit_invocation` 設為 `false`，代表這個 Skill 必須由使用者明確呼叫，不會自動加入對話。

### 來源與授權

| 項目 | 資訊 |
| --- | --- |
| 原作者 | Matt Pocock |
| 原始專案 | [mattpocock/skills](https://github.com/mattpocock/skills) |
| 採用的上游版本 | [v1.2.0](https://github.com/mattpocock/skills/tree/v1.2.0) |
| 固定來源 Commit | [`2ffb184ffbb752faa664c0b204f3c9241b1428e9`](https://github.com/mattpocock/skills/commit/2ffb184ffbb752faa664c0b204f3c9241b1428e9) |
| 上游入口 Skill | [`grill-me/SKILL.md`](https://github.com/mattpocock/skills/blob/v1.2.0/skills/productivity/grill-me/SKILL.md) |
| 上游核心 Skill | [`grilling/SKILL.md`](https://github.com/mattpocock/skills/blob/v1.2.0/skills/productivity/grilling/SKILL.md) |
| 授權 | [MIT License](https://github.com/mattpocock/skills/blob/v1.2.0/LICENSE) |

MIT License 允許使用、複製、修改、發布及重新散布。本安裝包保留完整的原作者著作權聲明與 MIT 授權條款。

這是依照我的 ChatGPT Work 使用需求整理的修改版本，不是原作者發布的官方安裝包，也不會自動同步上游後續變更。

### 主要修改

1. 將上游分開的 `grill-me` 入口與 `grilling` 核心流程整理成單一、可獨立使用的 ChatGPT Work Skill。
2. 將 `allow_implicit_invocation` 設為 `false`，並移除 ChatGPT Work 不使用的 `disable-model-invocation` 欄位。
3. 將決策樹、問題前緣、分輪訪談及完成條件重整成較明確的結構，並移除固定的表情符號輸出格式。
4. 將事實查找規則改為可使用目前對話、附件、連接來源、檔案系統、網路及其他可用工具。
5. 加入來源 metadata、預設提示及完整的原始 MIT `LICENSE`。
6. 將所有訪談選項限制為對話文字，讓使用者自行輸入選項或答案，不使用可點擊式選項、按鈕、表單、投票或其他互動輸入元件。

### 隱私與安全

公開檔案及安裝包皆不包含：

* API 金鑰、密碼或其他憑證
* 私人電腦路徑
* 個人對話紀錄
* 與 ChatGPT Work 無關的設定

### 免責聲明

這是獨立整理及維護的第三方修改版本，不是 OpenAI 或 Matt Pocock 的官方專案，也不代表 OpenAI 或原作者的認可或背書。

---

## English

### About This Skill

This is a third-party Skill that I adapted and actively use in ChatGPT Work.

Before a plan, design, or idea is acted upon, it organizes unresolved questions into a decision tree with dependencies and asks, in rounds, only the questions whose prerequisites have already been settled.

ChatGPT is responsible for investigating objective facts. Subjective decisions such as requirements, priorities, trade-offs, and acceptance criteria remain under the user’s control.

This is a decision-clarification and plan stress-testing tool. It does not mean that a plan is necessarily correct, complete, or free of issues, nor will it begin taking action before shared understanding has been confirmed.

### My Purpose

I mainly use this Skill for project planning, requirement clarification, system design, workflow selection, and important decisions.

It instructs ChatGPT to:

1. Organize the plan, design, or idea into a decision tree with dependencies.
2. Ask only the currently independent questions in each round, including useful choices, trade-offs, and a recommended answer.
3. Investigate facts available from the conversation, files, connected sources, filesystem, web, or other tools.
4. Update the decision tree after each round and ask the next set of newly unblocked questions.
5. Obtain the user’s explicit confirmation after every material branch has been resolved and before taking further action.

### My Installation Method

1. Download [`grill-me.zip`](./grill-me.zip) without extracting it.
2. Open the ChatGPT website.
3. Open “Plugins” from the sidebar, then select “Skills.”
4. Click `+` and select “Upload from computer.”
5. Select the downloaded `grill-me.zip` and wait for installation to finish.

### My Usage

1. In the ChatGPT Work conversation where I need it, I explicitly invoke the Skill through the Skill selector or with `@Grill Me`.
2. I provide the plan, design, requirement, or idea that I want to examine.
3. I type my selections or answers using the numbers or letters listed in the conversation; multiple questions from the same round may be answered together, without using clickable options.
4. ChatGPT updates the decision tree from my answers and continues with the next round.
5. When the decision tree is complete, I confirm or correct ChatGPT’s summary of our shared understanding, then separately instruct it to summarize, write a plan, or begin implementation.

This version does not activate automatically. The Grill Me interview begins only after explicit invocation.

### Repository Files

| File | Purpose |
| --- | --- |
| `README.md` | Documents my purpose, installation method, usage, file structure, source, license, and main changes. |
| `grill-me.zip` | The Skill installation package that can be uploaded directly to ChatGPT Work. |

### Files Inside the ZIP

| File | Purpose |
| --- | --- |
| `grill-me/SKILL.md` | Contains the core instructions for the decision tree, question frontier, interview rounds, fact investigation, and completion confirmation. |
| `grill-me/agents/openai.yaml` | Defines the ChatGPT Work display name, short description, default prompt, and invocation policy. |
| `grill-me/LICENSE` | Contains the complete upstream MIT License and original copyright notice. |

In `agents/openai.yaml`, `allow_implicit_invocation` is set to `false`. This means the Skill must be explicitly invoked and will not be added to conversations automatically.

### Source and License

| Item | Information |
| --- | --- |
| Original author | Matt Pocock |
| Upstream project | [mattpocock/skills](https://github.com/mattpocock/skills) |
| Upstream version used | [v1.2.0](https://github.com/mattpocock/skills/tree/v1.2.0) |
| Pinned upstream commit | [`2ffb184ffbb752faa664c0b204f3c9241b1428e9`](https://github.com/mattpocock/skills/commit/2ffb184ffbb752faa664c0b204f3c9241b1428e9) |
| Upstream entry Skill | [`grill-me/SKILL.md`](https://github.com/mattpocock/skills/blob/v1.2.0/skills/productivity/grill-me/SKILL.md) |
| Upstream core Skill | [`grilling/SKILL.md`](https://github.com/mattpocock/skills/blob/v1.2.0/skills/productivity/grilling/SKILL.md) |
| License | [MIT License](https://github.com/mattpocock/skills/blob/v1.2.0/LICENSE) |

The MIT License permits use, copying, modification, publication, and redistribution. This installation package retains the complete original copyright notice and MIT License terms.

This is a modified package prepared for my ChatGPT Work usage. It is not an official package published by the original author and does not automatically track later upstream changes.

### Main Changes

1. Combines the upstream `grill-me` entry point and `grilling` core workflow into one standalone ChatGPT Work Skill.
2. Sets `allow_implicit_invocation` to `false` and removes the `disable-model-invocation` field that ChatGPT Work does not use.
3. Reorganizes the decision-tree, question-frontier, interview-round, and completion rules into a clearer structure while removing the fixed emoji-based output format.
4. Makes fact investigation environment-neutral by allowing the conversation, attachments, connected sources, filesystem, web, and other available tools.
5. Adds source metadata, a default prompt, and the complete upstream MIT `LICENSE`.
6. Requires all interview choices to be presented as plain chat text so the user types a selection or answer, without clickable options, buttons, forms, polls, or other interactive input controls.


### Privacy and Safety

The public files and installation package do not contain:

* API keys, passwords, or other credentials
* Private computer paths
* Personal conversation records
* Settings unrelated to ChatGPT Work

### Disclaimer

This is an independently prepared and maintained third-party modification. It is not an official OpenAI or Matt Pocock project and is not affiliated with or endorsed by OpenAI or the original author.