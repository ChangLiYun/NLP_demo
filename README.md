# 銀行客服 RAG Chatbot

## 專案簡介
本專案是一個 **檢索增強生成 (RAG)** 聊天機器人，專門處理銀行與金控網站的常見客服問題。  
系統結合 **意圖分類 (Intent Classification)** 與 **FAQ 檢索 (Semantic Retrieval)**，能根據使用者輸入的問題：
1. 判斷意圖類別 (如：帳單查詢、繳費服務、信用卡服務)
2. 從 FAQ 知識庫檢索最相關的答案
3. 生成自然語言回覆，模擬智能客服的應用場景

---

## 🎯 專案目標
- 建立一個能處理銀行客服常見問題的 NLP 系統
- 展示完整的 RAG 架構：分類 → 檢索 → 回覆生成
- 提供互動式介面，讓使用者能即時體驗系統功能

---

## 🛠 技術棧
- **[Transformers](ca://s?q=HuggingFace_Transformers)** — 微調 DistilBERT/中文 BERT 做意圖分類
- **[Sentence-Transformers](ca://s?q=Sentence_Transformers)** — 建立 FAQ 語意檢索索引
- **[FAISS](ca://s?q=FAISS_檢索庫)** — 高效向量檢索
- **[Gradio](ca://s?q=Gradio_UI)** — 建立互動式介面
- **[Python](ca://s?q=Python)** — 資料處理與系統整合

---

## 📂 專案結構
<img width="809" height="341" alt="image" src="https://github.com/user-attachments/assets/823ced1c-af2a-42b2-8b34-f671514df4d7" />


---

## 📑 FAQ 知識庫範例
```json
{
  "id": "bill_001",
  "intent": "帳單查詢",
  "question": "信用卡帳單什麼時候出來？",
  "answer": "信用卡帳單通常於每月固定結帳日後3-5個工作日內產生，您可透過中信銀APP或網路銀行即時查詢。"
}


