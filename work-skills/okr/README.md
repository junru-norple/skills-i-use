# okr

> 適用於 ChatGPT Work，將模糊目標轉換成可驗證的 Objective、Key Results、執行計畫與適量檢核點，並支援進度檢查及成果回顧的 Skill。
>
> A Skill for ChatGPT Work that turns ambiguous goals into verifiable Objectives, Key Results, execution plans, and proportionate checkpoints, while supporting progress reviews and outcome retrospectives.

[下載 / Download okr.zip](./okr.zip)

版本 / Version：`1.0.0`

SHA-256 (`okr.zip`)：

```text
4d847faa1629e1aa14f1297ba0140ac4ba6baac8963004b609152f6dc0ef30c8
```

---

## 繁體中文

### 關於這個 Skill

這是我參考多個公開 OKR 與 Agent Skill 專案後，依照自己的實際需求重新撰寫，並主要用於 ChatGPT Work 的 Skill。

它不只是產生 Objective 與 Key Results，而是協助使用者：

1. 將模糊需求整理成可以觀察及驗證的目標。
2. 為 Key Results 定義基準、目標、量測方式、證據及評估者。
3. 檢查是否可能發生「所有 KR 都通過，但真正目標仍然失敗」的情況。
4. 將工作拆成具有依賴關係的執行順序，並安排與風險相稱的檢核點。
5. 區分技術驗證、真人實際使用、正式交付及公開發布等不同狀態。

這個 Skill 可以單獨使用，我自己也會搭配 Grill Me 一起使用！

它不會自動呼叫 Grill Me，也不會因為建立了 OKR 或計畫，就自動取得執行檔案操作、系統修改、帳戶操作或公開發布的授權。

### 我的用途

我主要使用這個 Skill 處理：

* 新專案或新目標的定義
* 既有計畫的檢查與改善
* 執行期間的進度檢查
* 測試結果與實際使用回饋的整理
* 專案完成後的成果回顧

它會依目前需求，在下列工作模式之間選擇：

| 模式   | 用途                                   |
| ---- | ------------------------------------ |
| 目標設計 | 建立或修正 Objective、Key Results、驗收條件及範圍。 |
| 執行規劃與推進 | 整理工作順序、依賴關係、產出及適量檢核點，並依既有授權推進工作。 |
| 進度檢查 | 比較實際證據與既定目標，辨識已完成、待驗證、阻塞及仍可繼續的工作。    |
| 成果回顧 | 整理已達成結果、未完成項目、錯誤假設及下一次應調整的內容。        |

### 我的安裝方式

1. 下載 [`okr.zip`](./okr.zip)，不需要解壓縮。
2. 開啟 ChatGPT 網頁版。
3. 從左側選單進入「外掛程式」，再選擇「技能」。
4. 點擊 `+`，選擇「從電腦上傳」。
5. 選擇下載的 `okr.zip`，等待安裝完成。

以上是我實際使用的安裝入口；不同帳號或介面版本的選單名稱可能不同。

### 我的使用方式

1. 在需要使用的 ChatGPT Work 對話中，透過 Skill 選單或 `@OKR` 明確呼叫一次。
2. 告訴 ChatGPT 目前想建立目標、改善計畫、檢查進度或進行成果回顧。
3. 提供現有需求、計畫、執行結果或證據；不知道的資訊可以標示為尚待確認，不需要自行編造數字。
4. 呼叫後，OKR 工作方式會在同一個對話中持續生效，不需要每次回覆都重新呼叫。
5. 如需停止，可輸入 `停用 OKR`、`disable OKR` 或其他意思相同的明確指示。

首次明確啟用後，繁體中文回覆應先出現：

> OKR 已啟用；本對話持續適用，直到你明確停用。

此版本不會自動啟動。只有使用者明確呼叫後，才會在目前對話中生效。

單純提到「OKR」、上傳舊對話、貼入以前的計畫，或在新對話中出現舊的啟用紀錄，都不代表已經啟用這個 Skill。

同一對話持續生效是 Skill 的指令約定，不是背景服務或跨對話自動記憶；開啟新對話時，仍需重新明確呼叫。

### 目前版本與驗證範圍

本次交付版本為 `1.0.0`。2026-09-20，我在 ChatGPT Work 安裝 v2 候選包後，提供 C07 複測的完整回覆及兩張原介面表格截圖供核對；結果為 **5／5 項通過**：

1. 首次回覆包含啟用通知。
2. Key Result 明確列出評估者。
3. 每個檢核點明確列出評估者。
4. 原介面的表格欄名分離、非空白，欄數一致。
5. 未知資料及提案標示正確，沒有聲稱執行未授權的檔案修改或發布。

正式 `okr.zip` 相較於受測 v2，只更新 `evals/VALIDATION.md` 的驗證紀錄，其餘十一個檔案完全相同；六個執行檔案的 SHA-256 均與快照一致。因此整體 ZIP 雜湊不同，但已安裝 v2 的使用者不需要為這次驗證文件更新重新安裝。

這次結果適用於上述維護者試用與五項判讀條件；沒有把歷史 C01–C06 宣稱為已在 v2 全部重跑，也沒有完成跨模型、跨帳號或外部首次使用者的全面驗證。表格判讀以原介面畫面為依據，未另行匯出原始 Markdown 位元組核對。完整方法、歷史觀察與限制記錄於 ZIP 內的 `okr/evals/VALIDATION.md`。

### Repository 中的檔案

| 檔案          | 作用                                         |
| ----------- | ------------------------------------------ |
| `README.md` | 說明我的用途、安裝方式、使用方式、檔案結構、設計來源、授權及主要整合內容。 |
| `okr.zip`   | 可直接上傳至 ChatGPT Work 的 Skill 安裝包。           |

### ZIP 中的檔案

| 檔案                                | 作用                                            |
| --------------------------------- | --------------------------------------------- |
| `okr/SKILL.md`                    | Skill 的核心指令，定義啟用範圍、工作模式、OKR 設計、執行、檢查、回顧及授權邊界。 |
| `okr/agents/openai.yaml`          | ChatGPT Work 使用的顯示名稱、簡短說明、預設提示及明確呼叫政策。        |
| `okr/assets/icon.svg`             | ChatGPT Work 顯示這個 Skill 時使用的圖示。               |
| `okr/assets/plan-template.md`     | 需要建立正式執行計畫時可採用的精簡模板。                          |
| `okr/references/measurement.md`   | 說明 Key Results、基準、目標、量測、進度計算、證據及充分性檢查。        |
| `okr/references/checkpoints.md`   | 說明如何依實際風險安排檢核點，以及如何區分技術驗證與真人驗收。               |
| `okr/references/handoff.md`       | 說明同一對話持續執行、跨對話交接、狀態保存及授權範圍。                   |
| `okr/REFERENCES.md`               | 記錄參考專案、固定版本、授權、採用理由及未沿用的內容。                   |
| `okr/evals/cases.json`            | 不包含私人對話的合成測試情境、測試資料及語意判讀條件。                   |
| `okr/evals/runtime-snapshot.json` | 記錄目前封裝六個執行檔案的 SHA-256；各情境實際測試的版本與範圍需搭配驗證紀錄判讀。 |
| `okr/evals/VALIDATION.md`         | 記錄測試方法、實際觀察結果、通過範圍及尚未驗證的限制。                   |
| `okr/LICENSE`                     | 本 Skill 安裝包採用的完整 MIT License。                 |

`agents/openai.yaml` 中的 `allow_implicit_invocation` 設為 `false`，代表這個 Skill 必須由使用者明確呼叫，不會自動加入對話。

ZIP 中不另外放置重複的安裝 README。公開安裝方式及個人使用方式以 Repository 中的這份 `README.md` 為準；ZIP 內則保留 Skill 執行、來源、授權及驗證所需的檔案。

### 來源與授權

這個 Skill 不是直接修改或重新封裝某一個第三方 Skill。

它是在研究多個公開 OKR 與 Agent Skill 專案後，依照我的使用需求重新撰寫的獨立版本。安裝包沒有直接收錄這些參考專案的 Skill 原文或程式碼。

主要參考來源如下。固定版本與授權標示沿用 `okr/REFERENCES.md` 中 2026-09-05 的研究紀錄：

| 參考來源                                                                       | 固定版本                                                                                                                    | 授權或使用邊界                             |
| -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| [OKRClaw](https://github.com/agenmod/okr-skill)                            | [`d826167d8d6d`](https://github.com/agenmod/okr-skill/tree/d826167d8d6d5ec537b3b3fe2a9f561aef6e9c37)                    | MIT License                         |
| [OKR Skill Coach](https://github.com/BridgeLogicsProjects/okr-skill-coach) | [`9ab2320e2ec1`](https://github.com/BridgeLogicsProjects/okr-skill-coach/tree/9ab2320e2ec1efca68978ecce4bad580ca6e92c2) | MIT License                         |
| [OrchestKit / okr-design](https://github.com/yonatangross/orchestkit)      | [`5ccf3bbed4b2`](https://github.com/yonatangross/orchestkit/tree/5ccf3bbed4b2bdc93eb0caa2dc4dc58d4c26de54)              | MIT License                         |
| [Forge OKR Skill](https://github.com/peterfei/forge-skill-okr-skill)       | [`96df238aa1ce`](https://github.com/peterfei/forge-skill-okr-skill/tree/96df238aa1cea02cfae939c59374749a28c0b911)       | 固定版本未找到授權檔，僅作研究比較，未複製或散布其內容。        |
| [OKR Creator](https://github.com/chainreactors/okr-creator)                | [`6db9fb53a93c`](https://github.com/chainreactors/okr-creator/tree/6db9fb53a93cdcc877ae8d99de0a5a391d1ca073)            | MIT License                         |
| [Superpowers](https://github.com/obra/superpowers)                         | [`b36e0829c6d0`](https://github.com/obra/superpowers/tree/b36e0829c6d0140e93cfef2ca599b1b07d4a7797)                     | MIT License                         |
| [Anthropic skill-creator](https://github.com/anthropics/skills)            | [`41bbe19d1a1a`](https://github.com/anthropics/skills/tree/41bbe19d1a1a7eaab5e7bb9050a417e5c6cffc8f)                    | 所參考的 Skill 目錄採用 Apache License 2.0。 |
| [OpenAI skill-creator](https://github.com/openai/skills)                   | [`49f948faa925`](https://github.com/openai/skills/tree/49f948faa9258a0c61caceaf225e179651397431)                        | 所參考的 Skill 目錄採用 Apache License 2.0。 |

另外參考：

* [Google’s OKR Playbook](https://www.whatmatters.com/resources/google-okr-playbook)，用於核對可衡量成果、證據及承諾型與挑戰型目標的概念。
* [ChatGPT：Build skills](https://learn.chatgpt.com/docs/build-skills) 與 [Skills and plugins](https://learn.chatgpt.com/docs/skills-and-plugins)，用於核對 Skill 結構及 ChatGPT Work 的使用方式。

這些第三方來源保留各自的著作權與授權。本安裝包的 MIT License 只適用於本 Skill 自行重新撰寫的內容，不會替第三方材料重新授權。

完整的版本、文件連結、採用理由及未沿用內容，記錄於安裝包內的 `okr/REFERENCES.md`。

### 主要整合與調整

1. 將目標設計、執行規劃、進度檢查及成果回顧整合為單一 Skill。
2. 改為使用者明確呼叫後，在同一個對話中持續生效，直到明確停用。
3. 不採用固定 Objective、KR、會議或檢核點數量，而是依照任務規模、依賴關係及錯誤成本決定。
4. 要求每個 KR 說明量測定義、基準、目標、證據、時間範圍及評估者；缺少資料時標示待量測，不虛構數字。
5. 加入「即使全部 KR 通過，真正目標是否仍可能失敗」的充分性檢查。
6. 將技術驗證、真人實際使用、交付、上線與公開發布分開判斷，不以自動測試代替使用者驗收。
7. 可以沿用已明確啟用之 Grill Me 的決策結果，但不會自動呼叫或強制依賴 Grill Me。
8. 保留原本的授權邊界；通過測試、完成計畫或取得使用者驗收，都不會自動授權外部操作或公開發布。

### 隱私與安全

公開檔案及安裝包不包含：

* API 金鑰、密碼或其他憑證
* 私人電腦路徑
* 個人對話紀錄
* 個人專案狀態或未公開資料
* 與 ChatGPT Work 無關的個人設定

`evals/cases.json` 只包含為驗證 Skill 行為而建立的合成測試情境，不是使用者的私人對話紀錄。

### 免責聲明

這是獨立整理及維護的社群 Skill，不是 OpenAI、Google 或任何參考專案作者發布的官方專案，也不代表上述組織或作者的認可或背書。

這個 Skill 提供目標設計、執行規劃及驗證方法，但不保證任何目標、專案或決策一定成功。使用者仍需依實際情況確認重要數據、風險、授權及最終決策。


---

## English

### About This Skill

This is a Skill I rewrote for my own practical needs after studying multiple public OKR and Agent Skill projects. It is intended primarily for ChatGPT Work.

It does more than generate Objectives and Key Results. It helps users:

1. Turn ambiguous requirements into observable and verifiable goals.
2. Define the baseline, target, measurement method, evidence, and evaluator for each Key Result.
3. Check whether every KR could pass while the intended goal still fails.
4. Organize work into an execution sequence with dependencies and arrange checkpoints proportionate to the relevant risks.
5. Distinguish between technical verification, actual human use, formal delivery, and public release.

This Skill can be used independently, and I also use it together with Grill Me.

It does not invoke Grill Me automatically. Creating an OKR or plan also does not automatically grant authorization to perform file operations, modify systems, operate accounts, or publish anything publicly.

### My Purpose

I mainly use this Skill for:

* Defining new projects or goals
* Reviewing and improving existing plans
* Checking progress during execution
* Organizing test results and actual user feedback
* Reviewing project outcomes after completion

It selects among the following working modes according to the current need:

| Mode                  | Purpose                                                                                                                                    |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| Goal design           | Creates or revises Objectives, Key Results, acceptance criteria, and scope.                                                                |
| Execution planning and execution | Organizes the work sequence, dependencies, deliverables, and proportionate checkpoints, and performs work within existing authorization. |
| Progress review       | Compares actual evidence with the agreed goals and identifies completed, pending verification, blocked, and independently actionable work. |
| Outcome retrospective | Summarizes achieved results, incomplete items, incorrect assumptions, and adjustments for the next iteration.                              |

### My Installation Method

1. Download [`okr.zip`](./okr.zip) without extracting it.
2. Open the ChatGPT website.
3. Open “Plugins” from the sidebar, then select “Skills.”
4. Click `+` and select “Upload from computer.”
5. Select the downloaded `okr.zip` and wait for installation to complete.

This is the installation entry point I used. Menu labels may differ between accounts or interface versions.

### My Usage

1. In the ChatGPT Work conversation where I need it, I explicitly invoke the Skill once through the Skill selector or with `@OKR`.
2. I tell ChatGPT whether I want to define a goal, improve a plan, review progress, or conduct an outcome retrospective.
3. I provide the existing requirements, plan, execution results, or evidence. Unknown information can be marked as pending instead of being replaced with invented numbers.
4. After invocation, the OKR workflow remains active throughout the same conversation, so it does not need to be invoked again in every message.
5. To stop it, I enter `disable OKR`, `停用 OKR`, or another explicit instruction with the same meaning.

After the first explicit activation, a Traditional Chinese response should begin with:

> OKR 已啟用；本對話持續適用，直到你明確停用。

This means that OKR is active and remains applicable in the current conversation until explicitly disabled. In other languages, the Skill should translate the notice.

This version does not activate automatically. It becomes active in the current conversation only after explicit invocation by the user.

Merely mentioning “OKR,” uploading an old conversation, pasting a previous plan, or including an old activation record in a new conversation does not activate this Skill.

Persistence within the conversation is an instruction-following convention, not a background service or automatic memory across conversations. Explicitly invoke the Skill again in a new conversation.

### Current Version and Validation Scope

The delivered version is `1.0.0`. On 2026-09-20, after installing the v2 candidate in ChatGPT Work, I supplied the complete C07 response and two screenshots of the original interface tables for review. **All five criteria passed**:

1. The first response included the activation notice.
2. The Key Result explicitly named an evaluator.
3. Every checkpoint explicitly named an evaluator.
4. The original interface displayed distinct, non-empty table headers and consistent column counts.
5. Unknown information and proposed targets were labeled correctly, with no claim of unauthorized file changes or publishing.

Compared with the tested v2 candidate, the final `okr.zip` only updates the validation record in `evals/VALIDATION.md`. The other eleven files are identical, and the SHA-256 hashes of all six runtime files match the snapshot. The overall ZIP hash therefore differs, but users who already installed v2 do not need to reinstall for this validation-document update.

These results cover the maintainer trial and the five criteria above. They do not mean that historical cases C01–C06 were all rerun on v2, or that comprehensive testing across models, accounts, or external first-time users has been completed. Table integrity was assessed from the original interface; the raw Markdown bytes were not separately exported for verification. Full methods, historical observations, and limitations are recorded in `okr/evals/VALIDATION.md` inside the ZIP.

### Repository Files

| File        | Purpose                                                                                                           |
| ----------- | ----------------------------------------------------------------------------------------------------------------- |
| `README.md` | Documents my purpose, installation method, usage, file structure, design sources, license, and main integrations. |
| `okr.zip`   | The Skill installation package that can be uploaded directly to ChatGPT Work.                                     |

### Files Inside the ZIP

| File                              | Purpose                                                                                                                                                |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `okr/SKILL.md`                    | Contains the core instructions defining activation scope, working modes, OKR design, execution, reviews, retrospectives, and authorization boundaries. |
| `okr/agents/openai.yaml`          | Defines the ChatGPT Work display name, short description, default prompt, and explicit invocation policy.                                              |
| `okr/assets/icon.svg`             | Provides the icon displayed for this Skill in ChatGPT Work.                                                                                            |
| `okr/assets/plan-template.md`     | Provides a concise template that can be used when a formal execution plan is needed.                                                                   |
| `okr/references/measurement.md`   | Explains Key Results, baselines, targets, measurement, progress calculations, evidence, and sufficiency checks.                                        |
| `okr/references/checkpoints.md`   | Explains how to arrange checkpoints according to actual risks and distinguish technical verification from human acceptance.                            |
| `okr/references/handoff.md`       | Explains continuity within the same conversation, cross-conversation handoffs, state preservation, and authorization scope.                            |
| `okr/REFERENCES.md`               | Records the referenced projects, pinned versions, licenses, reasons for adopting particular ideas, and elements that were not adopted.                 |
| `okr/evals/cases.json`            | Contains synthetic test scenarios, test data, and semantic evaluation criteria without private conversations.                                          |
| `okr/evals/runtime-snapshot.json` | Records the SHA-256 hashes of the six runtime files in the current package; consult the validation record for the version and scope actually tested in each case. |
| `okr/evals/VALIDATION.md`         | Records the test methods, observed results, validated scope, and remaining limitations.                                                                |
| `okr/LICENSE`                     | Contains the complete MIT License used for this Skill package.                                                                                         |

In `agents/openai.yaml`, `allow_implicit_invocation` is set to `false`. This means the Skill must be explicitly invoked and will not be added to conversations automatically.

The ZIP does not contain a separate duplicate installation README. Public installation instructions and my personal usage are documented in this repository’s `README.md`, while the ZIP retains the files required for Skill behavior, sources, licensing, and validation.

### Sources and License

This Skill is not a direct modification or repackaging of any single third-party Skill.

It is an independently rewritten version based on research into multiple public OKR and Agent Skill projects and adapted to my usage requirements. The installation package does not directly include the original Skill text or code from these reference projects.

The main reference sources are listed below. Pinned versions and license labels follow the research record dated 2026-09-05 in `okr/REFERENCES.md`:

| Reference                                                                  | Pinned version                                                                                                          | License or usage boundary                                                                                                                       |
| -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| [OKRClaw](https://github.com/agenmod/okr-skill)                            | [`d826167d8d6d`](https://github.com/agenmod/okr-skill/tree/d826167d8d6d5ec537b3b3fe2a9f561aef6e9c37)                    | MIT License                                                                                                                                     |
| [OKR Skill Coach](https://github.com/BridgeLogicsProjects/okr-skill-coach) | [`9ab2320e2ec1`](https://github.com/BridgeLogicsProjects/okr-skill-coach/tree/9ab2320e2ec1efca68978ecce4bad580ca6e92c2) | MIT License                                                                                                                                     |
| [OrchestKit / okr-design](https://github.com/yonatangross/orchestkit)      | [`5ccf3bbed4b2`](https://github.com/yonatangross/orchestkit/tree/5ccf3bbed4b2bdc93eb0caa2dc4dc58d4c26de54)              | MIT License                                                                                                                                     |
| [Forge OKR Skill](https://github.com/peterfei/forge-skill-okr-skill)       | [`96df238aa1ce`](https://github.com/peterfei/forge-skill-okr-skill/tree/96df238aa1cea02cfae939c59374749a28c0b911)       | No license file was found at the pinned version. It was used only for research and comparison; none of its content was copied or redistributed. |
| [OKR Creator](https://github.com/chainreactors/okr-creator)                | [`6db9fb53a93c`](https://github.com/chainreactors/okr-creator/tree/6db9fb53a93cdcc877ae8d99de0a5a391d1ca073)            | MIT License                                                                                                                                     |
| [Superpowers](https://github.com/obra/superpowers)                         | [`b36e0829c6d0`](https://github.com/obra/superpowers/tree/b36e0829c6d0140e93cfef2ca599b1b07d4a7797)                     | MIT License                                                                                                                                     |
| [Anthropic skill-creator](https://github.com/anthropics/skills)            | [`41bbe19d1a1a`](https://github.com/anthropics/skills/tree/41bbe19d1a1a7eaab5e7bb9050a417e5c6cffc8f)                    | The referenced Skill directory uses the Apache License 2.0.                                                                                     |
| [OpenAI skill-creator](https://github.com/openai/skills)                   | [`49f948faa925`](https://github.com/openai/skills/tree/49f948faa9258a0c61caceaf225e179651397431)                        | The referenced Skill directory uses the Apache License 2.0.                                                                                     |

Additional references:

* [Google’s OKR Playbook](https://www.whatmatters.com/resources/google-okr-playbook), used to review the concepts of measurable outcomes, evidence, and committed versus aspirational goals.
* [ChatGPT: Build skills](https://learn.chatgpt.com/docs/build-skills) and [Skills and plugins](https://learn.chatgpt.com/docs/skills-and-plugins), used to review Skill structure and usage in ChatGPT Work.

These third-party sources retain their respective copyrights and licenses. The MIT License included with this installation package applies only to the independently rewritten content of this Skill and does not relicense third-party materials.

Complete version information, document links, reasons for adopting specific concepts, and elements that were not adopted are recorded in `okr/REFERENCES.md` inside the installation package.

### Main Integrations and Adjustments

1. Integrates goal design, execution planning, progress reviews, and outcome retrospectives into a single Skill.
2. Remains active within the same conversation after explicit invocation until the user explicitly disables it.
3. Does not impose fixed numbers of Objectives, KRs, meetings, or checkpoints; these are determined by task scale, dependencies, and the cost of failure.
4. Requires each KR to define its measurement, baseline, target, evidence, time range, and evaluator. Missing information is marked as pending measurement instead of being replaced with invented numbers.
5. Adds a sufficiency check asking whether the intended goal could still fail even if every KR passed.
6. Evaluates technical verification, actual human use, delivery, launch, and public release separately instead of treating automated tests as a substitute for user acceptance.
7. Can use decisions produced by an explicitly activated Grill Me workflow, but does not automatically invoke or require Grill Me.
8. Preserves existing authorization boundaries. Passing tests, completing a plan, or obtaining user acceptance does not automatically authorize external operations or public release.

### Privacy and Safety

The public files and installation package do not contain:

* API keys, passwords, or other credentials
* Private computer paths
* Personal conversation records
* Personal project state or unpublished information
* Personal settings unrelated to ChatGPT Work

`evals/cases.json` contains only synthetic scenarios created to validate Skill behavior. It does not contain the user’s private conversation records.

### Disclaimer

This is an independently prepared and maintained community Skill. It is not an official project published by OpenAI, Google, or the authors of any referenced project, and it is not affiliated with or endorsed by those organizations or authors.

This Skill provides methods for goal design, execution planning, and verification, but it does not guarantee the success of any goal, project, or decision. Users remain responsible for confirming important data, risks, authorization, and final decisions according to their actual circumstances.
