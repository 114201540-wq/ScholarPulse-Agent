# 產品客服 AI Agent (Product Customer Service Agent)

## 1. 專案簡介
本專案為中央大學 AI-Agent 課程作業，旨在 Coze 平台上建構一個完整的「電商產品客服 AI 助理」。專案涵蓋 Prompt 設計、知識庫 RAG、記憶機制、外掛 API 與 Guardrail 安全護欄。

## 2. 核心應用場景與功能規劃
- **[單元 1] LLM 選用與 Prompt 調整**：測試不同模型（如 GPT-4o, Claude）之性價比，並使用結構化 Prompt 定義客服角色。
- **[單元 2] 結構化輸出**：設定客服回覆邏輯與指定 JSON 格式輸出。
- **[單元 3] 記憶機制 (Memory)**：設定 Variable/Table，實現客戶「加入購物車」的狀態紀錄。
- **[單元 4] 產品知識庫 (Knowledge/RAG)**：上傳模擬產品手冊，讓 Agent 依據真實資料精準回答商品細節。
- **[單元 5] 外掛工具 (Plugin)**：串接寄信服務，於客戶告知「付款完成」時自動寄送確認信。
- **[單元 6~8] Chatflow & Guardrail**：建立自動化意圖識別流程，並加入安全護欄阻擋情色、不當言論或提示詞注入。

## 3. GitHub 專案紀錄
- 本檔案將隨每週課程進度持續更新實作成果。
## 單元 1：大腦核心 - LLM 選擇與參數設定 (LLM & Config)

### 1. 實作紀錄
- 已於 Coze 平台成功建立 Agent（產品客服助理）。
- 觀察並配置 Coze 模型參數：
  - **Temperature**：設定為 `0.2`，確保客服回答內容客觀嚴謹，避免 AI 產生幻覺。
  - **Max Tokens**：設定為 `2048`，控制單次輸出的文字量。
  - **Context Window**：調控上下文歷史對話輪數。

### 2. 課綱問題回答
* **Coze 最便宜的模型**：
  - 在 Coze 免費額度計費機制中，**GPT-3.5 Turbo** 與 **GPT-4o mini** 每次呼叫僅消耗 **0.1 Credit**（Gemini 1.5 Flash 為 0.25 Credit），為平台中最便宜且高 CP 值的模型。
* **Google Gemini 官網現有模型總覽**：
  - **Gemini 2.0 Flash / Flash-Lite**：次世代極速、低延遲與高性價比模型。
  - **Gemini 2.0 Thinking**：具備深度邏輯推論能力的思考型模型。
  - **Gemini 1.5 Pro**：具備 200 萬 (2M) Tokens 超長 Context Window 的高階模型。
  - **Gemini 1.5 Flash**：兼顧速度與 100 萬 (1M) Tokens 長文本處理的通用模型。

### 3. 知識點觀念整理
- **模型大小與精準度**：模型參數越大，承載的知識量越多，對於複雜問題的推論精準度越高，但相對的價格較貴且回應延遲較高。
- **蒸餾模型 (Distilled Model)**：透過大模型訓練小模型的技術，讓輕量模型（如 GPT-4o-mini 或 Flash 系列）以極低成本達到接近旗艦模型的精準度。
