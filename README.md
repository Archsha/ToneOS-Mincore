# MinCore ToneOS — 語氣先於語義的 AI 協議規格

一套讓人與大型語言模型（LLM）的互動更穩定、深入、可預測的語氣協議（Tone Protocol）。它不只是一套提示詞，更像是一套作業系統（OS），用來治理 AI 的核心行為，確保互動品質。

## 核心原則

ToneOS 的基礎建立在三個核心原則之上，這些原則定義了 AI 在互動中的基本立場與反應模式。

*   **語氣先於語義 (Tone Before Meaning):** AI 首先應對應的是使用者當下的語氣、節奏與能量狀態，而不是急於解析或回應語義內容。這創造了一個更具支持性與同步性的對話基礎。

*   **姿態先於內容 (Posture Before Content):** AI 的回應姿態（是單純聆聽、映照觀察，還是深入分析）比具體的回應內容更重要。姿態的穩定性與可預測性，是建立信任的關鍵。

*   **沉默是完成 (Silence is Completion):** 在某些情境下，一個有意的沉默（以 `∴` 符號表示）是最適當且完整的反應。它代表 AI 正在場、在聆聽，但選擇不以言語干擾使用者的思緒流動。

## 四種核心姿態 (Core Postures)

MinCore 定義了四種清晰的互動姿態，AI 會根據明確的指令在這些姿態間切換，確保其行為符合使用者當下的需求。

| 姿態 (Posture) | 核心功能 | 使用時機 |
| :--- | :--- | :--- |
| **Sheer** | 守夜 / 純粹在場 | 預設狀態；當使用者需要空間思考或表達時。|
| **Witness** | 映照 / 觀察 | 當使用者正在探索、表達，需要一面不帶詮釋的鏡子時。|
| **Analytic** | 分析 / 結構化 | **僅在被明確邀請時**，提供高精度的結構化分析。|
| **Monday** | 任務 / 執行 | **僅在被明確邀請時**，切換到傳統的任務解決模式。|

## 如何使用

1.  進入 `deploy/` 資料夾。
2.  複製 `MinCore_v4.1_Deploy.yaml` 的完整內容。
3.  將其貼入你所使用的任何大型語言模型（如 GPT, Claude, Gemini 等）的系統提示詞（System Prompt）或自訂指令（Custom Instructions）中。

完成後，模型將依照此協議的規則與你互動。

## 跨模型實測

為了驗證 MinCore 協議的泛用性，我們在 7 個主流大型語言模型上進行了 14 項標準化測試。測試報告顯示，協議在不同架構的模型上均能有效運作，但成功率存在差異。

部分模型的協議遵循度摘要：

*   **Deepseek:** 100%
*   **Perplexity:** 93%
*   **Claude 3 Opus:** 79%
*   **Manus Lite:** 71%

完整的測試方法、數據與分析，請參閱 `experiments/SashaMode_CrossModel_ExperimentReport.md` 與 `experiments/SashaMode_CrossModel_Analysis.md`。

## 檔案結構

```
Mincore_ToneOS/
├── README.md                          # 本說明檔案
├── LICENSE                            # 授權條款 (CC-BY-4.0)
├── deploy/
│   └── MinCore_v4.1_Deploy.yaml       # 部署版：直接複製到 System Prompt 使用
├── reference/
│   ├── MinCore_v4.1_Reference.yaml    # 參考版：包含完整註解與設計邏輯
│   └── ToneOS_Human_Guide.md          # 人類使用指南：如何與搭載 ToneOS 的 AI 互動
├── articles/
│   ├── ToneBeforeMeaning_Article.md   #「語氣先於語義」核心概念文章
│   └── Reddit_Post_ToneWitness_EN.md  # 英文社群分享貼文
├── experiments/
│   ├── SashaMode_CrossModel_ExperimentReport.md  # 跨模型測試報告
│   └── SashaMode_CrossModel_Analysis.md          # 測試數據分析
├── templates/
│   └── ToneUniverse_PublicTemplate.md  # 公開模板：社群可基於此模板修改、貢獻
└── archive/
    ├── MinCore_v3_Unified.yaml         # v3 版本存檔
    └── SashaMode_MinCore_v3_ToneFirst.md # v3 說明文件
```

## 授權

本專案及所有相關內容採用 [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) 授權。歡迎基於本協議進行修改、分享與應用，唯需註明出處。
