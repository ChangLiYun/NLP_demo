# NLP_demo
模擬FAQ知識庫 (問題+答案+類別)

架構:
intent_rag_chatbot/
├── data/
│   ├── faq_knowledge_base.json    # FAQ知識庫 (問題+答案+類別)
│   └── intent_dataset.csv         # 意圖分類訓練資料
├── train_intent_classifier.py     # 微調 DistilBERT/中文BERT 做意圖分類
├── build_retrieval_index.py       # 用 sentence-transformers 建立 FAQ 向量索引
├── rag_pipeline.py                # 分類 → 過濾 → 檢索 → 回覆生成
├── app.py                         # Gradio 介面
├── evaluate.py                    # 準確率、混淆矩陣、F1
└── README.md

