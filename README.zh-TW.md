# CoCo Colab Notebooks

[English](README.md) | **繁體中文**

繁體中文的 Google Colab notebook，用來跑開源的 AI 影片與音樂生成模型。介面、說明和錯誤訊息都是繁體中文。

## Notebook 一覽

| Notebook | 用途 | 在 Colab 開啟 |
|---|---|---|
| `MiniMax_H3_zhTW.ipynb` | MiniMax H3 影片生成（ComfyUI 後端）。可用 Colab 表單、Gradio 圖形介面或 JSON 批次操作。 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Chocochocococo/CoCo-Colab-Notebooks/blob/main/MiniMax_H3_zhTW.ipynb) |
| `YuE2_AutoLRC_zhTW.ipynb` | YuE2 歌曲生成，附批量生成、Seed 管理、自動 LRC 歌詞時間軸與 MP3 輸出。可用 Colab 表單或 Gradio 圖形介面操作，圖形介面可以先產生樂譜、修改後再生成，並顯示樂譜的預估長度。 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Chocochocococo/CoCo-Colab-Notebooks/blob/main/YuE2_AutoLRC_zhTW.ipynb) |
| `ACE-Step_1.5_XL_AutoLRC_zhTW.ipynb` | ACE-Step 1.5 歌曲生成，使用最高品質的 XL（4B DiT）+ 4B LM 組合，附批量生成、Seed 管理、LRC 歌詞時間軸（ACE-Step 內建對齊或 Whisper）與 MP3 輸出。可用 Colab 表單或 Gradio 圖形介面操作，圖形介面可以先讓 LM 規劃 BPM、調性、拍號和長度，修改後再生成。 | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Chocochocococo/CoCo-Colab-Notebooks/blob/main/ACE-Step_1.5_XL_AutoLRC_zhTW.ipynb) |

## 使用前請先知道

- **需要付費的 Colab GPU**：這些模型都需要 L4 或 A100 等級的 GPU（ACE-Step XL 建議用 A100），免費的 T4 幾乎跑不動。
- **需要 Google 雲端硬碟空間**：模型會快取在你的雲端硬碟，避免每次重新下載。各 notebook 開頭有寫大約需要多少空間。
- **免費版 Colab 與圖形介面**：Colab 規定免費執行階段不能主要透過網頁介面操作，使用 Gradio 圖形介面可能被中斷。付費方案且運算單元有餘額時不受此限。
- **用完記得關**：執行階段開著就會持續扣運算單元。用完請到「執行階段 → 中斷連線並刪除執行階段」。

## 怎麼用

1. 點上表的「Open In Colab」。
2. 在 Colab 選「檔案 → 在雲端硬碟中儲存複本」，之後都從自己的副本開啟。
3. 依照 notebook 開頭的說明，由上往下執行。

## 來源與致謝

- `MiniMax_H3_zhTW.ipynb` 修改自 [Skquark/AEI-Colab-Notebooks](https://github.com/Skquark/AEI-Colab-Notebooks) 的 `MiniMax-H3_ComfyUI_Colab.ipynb`（MIT License，Copyright (c) 2026 Skquark）。原作的授權條文保留在該 notebook 的說明裡。
- `YuE2_AutoLRC_zhTW.ipynb` 的 LRC 歌詞時間軸使用 [ijuinryukichi/lyric-align](https://github.com/ijuinryukichi/lyric-align)（MIT License），執行時以 `pip` 安裝，本 repo 不包含它的程式碼。
- `ACE-Step_1.5_XL_AutoLRC_zhTW.ipynb` 執行時從官方 repo 安裝 [ACE-Step 1.5](https://github.com/ace-step/ACE-Step-1.5)，選擇 Whisper LRC 時也會使用 lyric-align；本 repo 不包含它們的程式碼。

## 授權

本 repo 的 notebook 程式碼以 [MIT License](LICENSE) 釋出。

MIT 只涵蓋 notebook 程式碼。模型權重（MiniMax H3、YuE2、ACE-Step、Whisper 等）不包含在本 repo 內，各有自己的授權條款，使用前請自行確認，尤其是商業用途。

## 免責聲明

這些 notebook 依「現況」提供。Colab 的環境、模型和相依套件都會更新，無法保證永遠能正常執行。
