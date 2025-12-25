# Copilot / AI Agent Instructions for Awesome_Traditional_Chinese_Datasets

簡短說明：本專案是一個以繁體中文為主的靜態資料集清單（單一 `README.md` 為主要內容）。本檔提供對 AI 編碼或維護代理（Copilot 類）立刻有用的背景、可執行任務與格式範例。

---

## 一眼看懂（Big picture） 🔍
- 專案定位：收集、整理「繁體中文資料集」的索引與說明。內容為 Markdown 文檔，無程式碼、無建置或測試流程。
- 主要檔案：`README.md`（所有資料集條目都集中在此）。
- 外部整合點：大多為外部資源（Hugging Face、GitHub 專案、官方網站等），內容以外部連結為主。

## 立即可做的任務（useful, specific tasks for AI agents） ✅
- 新增資料集：在 `README.md` 對應段落加入條列項，格式參考既有項目。
  - 範例：`- Fineweb-zhtw 繁體中文網路文本資料(107GB):(https://huggingface.co/datasets/voidful/fineweb-zhtw)`
  - 必要欄位：名稱、簡短說明、來源 URL、若可得則標註授權（license）或注意事項
- 標準化連結與格式：檢查全 repo 所有 Markdown 連結，統一使用完整 URL，移除多餘的重複條目。
- 分類與目錄：可考慮新增或更新章節標題（例如「來源自 HuggingFace」、「台語」、「推理資料集」），並維護一個簡單「目錄」(TOC) 以利瀏覽。
- 檢查可存取性：驗證每個外部連結是否 200 OK，並在無法存取時加上註解（如 "連結失效"）或移除。

## 風格與慣例（Project-specific conventions） 🧭
- 語言：內容以繁體中文撰寫（包含條目標題與說明）。
- 格式：每個資料集條目為 Markdown 列表項，呈現方式通常為
  - `- <名稱> <簡述>:(<網址>)`
- 目錄層級：使用標題（`###`、`####`）分節（例如：`### 繁體中文資料集`、`#### 推理資料集`）。

## 不存在但需知的事項（explicit negatives） ⚠️
- 沒有 CI / build / test 指令或自動化腳本。
- 沒有明確的 PR 模版或貢獻指南；因此 Agent 應以保守方式建立 PR（提供詳細說明與來源），並把變更限制在 `README.md`。

## 提交 PR 的建議步驟（practical checklist for agents creating PRs） 🛠️
1. 在 `README.md` 新增條目，遵循現有語言與格式。
2. 確認連結可存取（HTTP 200），若非，可在註解中說明檢查結果。
3. 若新增的是大型資料（如 >10GB）或需額外授權，於條目加上一行說明（例如：`授權: MIT` 或 `注意: 需申請授權`）。
4. PR 描述包含：新增內容摘要、來源鏈接、檢查清單（連結檢查、授權標記）。

## 顯著樣式範例（from repo）
- 來源範例：
  - `- Fineweb-zhtw 繁體中文網路文本資料(107GB):(https://huggingface.co/datasets/voidful/fineweb-zhtw)`
- 章節範例： `### 繁體中文資料集`、`#### 推理資料集`

## 可自動化但需注意的操作（automation tips） 🤖
- 自動化任務：連結健康檢查、重複條目偵測、README 的 TOC 生成。
- 注意：不要自動改寫中文敘述語句的語氣或內容（以免改變原意）；自動化應以標準化連結格式、標點與分節為主。

## 問題與溝通（if uncertain） 💬
- 若來源授權不清楚或資料有疑慮，為安全起見在條目前註明並在 PR 說明中請維護者確認。

---

如果你要我直接開一個 PR（例如：新增連結檢查或加入 TOC）我可以著手實作；或者先把這份說明微調成更短或更詳細的版本，請告訴我你偏好的範圍。