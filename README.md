# Audiocraft Infinity WebUI

Adds generation of songs with a length of over 30 seconds.

Adds the ability to continue songs.

Adds a seed option.

Disables (hopefully) the gradio analytics.

## Installation (Windows)
1. Install Python 3.9 (Add to PATH and All Users, also install recomended in C:\Python39)
```
https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe
```
2. Rename python.exe to python39.exe
3. Download `https://visualstudio.microsoft.com/visual-cpp-build-tools/`
4. Install VS Build Tools using this
```
vs_buildtools.exe --norestart --passive --downloadThenInstall --includeRecommended --add Microsoft.VisualStudio.Workload.NativeDesktop --add Microsoft.VisualStudio.Workload.VCTools --add Microsoft.VisualStudio.Workload.MSBuildTools
```
5. Clone the repo:
`git clone --recursive https://github.com/dports/musicgen-web`
6. Create virtual env: `python39 -m venv venv`
7. Activate virtual env: `venv\Scripts\activate`
8. Install the requirements:
`python39 -m pip install -r requirements.txt`
9. Clone the Meta audiocraft repo:
`git clone https://github.com/facebookresearch/audiocraft`
10. Copy the webui.py to the directory of the Meta audiocraft repo
`copy /b .\webui.py .\audiocraft\`
11. Go to the audiocraft directory
`cd .\audiocraft\`
## Usage
1. ```venv\Scripts\activate```
2. ```python39 webui.py```
## Models

Meta provides 4 pre-trained models. The pre trained models are:
- `small`: 300M model, text to music only - [🤗 Hub](https://huggingface.co/facebook/musicgen-small)
- `medium`: 1.5B model, text to music only - [🤗 Hub](https://huggingface.co/facebook/musicgen-medium)
- `melody`: 1.5B model, text to music and text+melody to music - [🤗 Hub](https://huggingface.co/facebook/musicgen-melody)
- `large`: 3.3B model, text to music only - [🤗 Hub](https://huggingface.co/facebook/musicgen-large)

**Needs a GPU!**

I recommend 12GB of VRAM for the large model.

## Colab

For google colab you need to replace `demo.launch()` with `demo.queue().launch(share=True)` in webui.py

## License
* The code in this repository is released under the AGPLv3 license as found in the [LICENSE file](LICENSE).
