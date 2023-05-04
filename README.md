# text-generation-webui-barktts
A simple extension for the [text-generation-webui by oobabooga](https://github.com/oobabooga/text-generation-webui) that uses [Bark](https://github.com/suno-ai/bark) for audio output.

## How to install
Assuming you already have the webui set up:

1. Activate the conda environment with the `cmd_xxx.bat` or using `conda activate textgen`
2. Enter the  `text-generation-webui/extensions/` directory and clone this repository
```
cd text-generation-webui/extensions/
git clone https://github.com/minemo/text-generation-webui-barktts bark_tts/
```
3. install the requirements
```
pip install -r extensions/bark_tts/requirements.txt
```
4. Add `--extensions bark_tts` to your startup script <br/> <b>or</b> <br/> enable it through the `Interface Mode` tab in the webui

## Tips
The full version of Bark requires around 12Gb of memory to hold everything on GPU at the same time. However, even smaller cards down to ~2Gb work with some additional settings. For this extension, you could open `extensions/bark_tts/.env`, then set `USE_SMALL_MODELS` and `USE_CPU` to `true`:

```
# Whether to use small models
USE_SMALL_MODELS=true

# Whether to use CPU
USE_CPU=true
```
