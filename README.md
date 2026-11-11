# CoCo Colab Notebooks

**English** | [繁體中文](README.zh-TW.md)

Google Colab notebooks for running open-source AI video and music generation models, with a Traditional Chinese interface.

> **Language note:** the notebooks themselves are written for Traditional Chinese speakers. Form labels, instructions, the Gradio panels and error messages are all in Traditional Chinese. Prompts for the models are still written in English.

## Notebooks

| Notebook | What it does | Open in Colab |
|---|---|---|
| `MiniMax_H3_zhTW.ipynb` | MiniMax H3 video generation on a ComfyUI backend. Can be driven from Colab forms, a Gradio panel, or a JSON batch file. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Chocochocococo/CoCo-Colab-Notebooks/blob/main/MiniMax_H3_zhTW.ipynb) |
| `YuE2_AutoLRC_zhTW.ipynb` | YuE2 song generation with batch generation, seed management, automatic LRC lyric timestamps and MP3 export. Can be driven from Colab forms or a Gradio panel. The panel can plan the score first, let you edit it, then generate, and it shows an estimated length for the score. | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Chocochocococo/CoCo-Colab-Notebooks/blob/main/YuE2_AutoLRC_zhTW.ipynb) |

## Before you start

- **A paid Colab GPU is required.** Both models need an L4 or A100 class GPU. The free T4 is not practical.
- **Google Drive space is required.** Models are cached in your Drive so they are not downloaded again every session. Each notebook states roughly how much space it needs at the top.
- **Free Colab and the Gradio panels.** Colab does not allow free runtimes to be used mainly through a web UI, so a session using a Gradio panel may be disconnected. Paid plans with a positive compute unit balance are not affected.
- **Disconnect when you are done.** A running runtime keeps consuming compute units. Use "Runtime → Disconnect and delete runtime" when you finish.

## How to use

1. Click "Open In Colab" in the table above.
2. In Colab, choose "File → Save a copy in Drive", and open your own copy from then on.
3. Follow the instructions at the top of the notebook and run the cells from top to bottom.

## Credits

- `MiniMax_H3_zhTW.ipynb` is modified from `MiniMax-H3_ComfyUI_Colab.ipynb` in [Skquark/AEI-Colab-Notebooks](https://github.com/Skquark/AEI-Colab-Notebooks) (MIT License, Copyright (c) 2026 Skquark). The original license text is kept inside that notebook.
- `YuE2_AutoLRC_zhTW.ipynb` uses [ijuinryukichi/lyric-align](https://github.com/ijuinryukichi/lyric-align) (MIT License) for LRC lyric timestamps. It is installed with `pip` at runtime; this repository does not contain its code.

## License

The notebook code in this repository is released under the [MIT License](LICENSE).

MIT covers the notebook code only. Model weights (MiniMax H3, YuE2, Whisper and others) are not included in this repository and each has its own license terms. Check them before use, especially for commercial use.

## Disclaimer

These notebooks are provided "as is". Colab's environment, the models and their dependencies all change over time, so there is no guarantee they will keep working.
