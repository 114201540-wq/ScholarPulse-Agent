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
