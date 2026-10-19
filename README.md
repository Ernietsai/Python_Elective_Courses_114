[![nbviewer](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.org/github/Ernietsai/Python_Elective_Courses_114)
[![NotebookLM](https://img.shields.io/badge/AI-NotebookLM-blue.svg)](https://notebooklm.google.com/notebook/0b39ce89-808d-4d81-b7a9-1708c49e2faf)

# MNIST Handwritten Digit Recognition & Deployment
「Python 入門多元選修」課程中製作的專案。本專案從基礎數據處理出發，結合深度學習模型開發，並最終實現網頁端即時辨識部署。

## 專案亮點
* **APCS 實作思維應用**：運用 APCS 四級所累積的邏輯能力，自主解決複雜資料結構 (Dictionary) 的解析問題。
* **人機協作除錯**：在 Gradio 部署過程中，發現並修正 AI 工具 (Google Gemini) 擷取錯誤 Key 值 (`background` vs `layers`) 的邏輯偏誤。
* **自動化機器學習 (AutoML)**：導入 AutoKeras 進行超參數搜尋，將準確率優化至 99%。

## 使用技術
* **語言**：Python
* **資料處理**：NumPy, Pandas (Vectorization 向量化運算)
* **機器學習**：TensorFlow / Keras, AutoKeras
* **應用部署**：Gradio (Web App Interface)
* **開發環境**：Google Colab

## 檔案說明
* `01AutoKeras_MNIST_辨識.ipynb`: 包含自動化搜尋模型與 Gradio 介面實作。
* `Colab實作：使用_CNN_建立MNIST...`: 詳載手動調教卷積神經網路 (CNN) 的實驗紀錄。
* `Numpy及資料視覺化.ipynb`: 實作 3D 動態圖表與效能優化對比。

## 關鍵除錯紀錄 (Debug Log)
在 Gradio `Sketchpad` 模式下，回傳資料格式為 `dict`。
原本 AI 建議程式：`data['background']` (僅含背景資訊)
修正後程式：`data['layers']` (包含實際手寫筆跡數據)
*此修正使網頁 App 辨識率由錯誤回傳變為 99% 的辨識正確率。*

## NotebookLM 專案導覽
> 我利用 Google NotebookLM 整合了本專案的部分技術文件、開發筆記與參考資料。您可以透過下方的連結進入互動式介面，快速檢索本專案的技術細節，或由 AI 為您摘要複雜的模型架構。
> 🔗 [NotebookLM 專案導覽](https://notebooklm.google.com/notebook/0b39ce89-808d-4d81-b7a9-1708c49e2faf)
