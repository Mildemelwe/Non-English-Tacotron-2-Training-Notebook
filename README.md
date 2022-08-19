# Non-English-Tacotron-2-Training-Notebook
Tacotron 2 training notebook supporting Japanese, French, and Mandarin
# Overview
This notebook is meant to provide easier access to training Tacotron 2 models in languages other than English. Currently, Japanese (TALQu and neuTalk phonetics), French, and Mandarin pretrained models are included, but the plan is to include more in the future, such as German.
# Supported audio
Audio for training should be 16-bit 22050hz mono WAV files. Do not include spaces in filenames. Files should only include alphanumerics (half-width), dashes, and underscores. This means no Japanese or Chinese filenames, or diacritics. Audio clips should be 10 seconds or less to facilitate learning. Based on my tests, I recommend having at least 15 minutes of audio.
# Transcriptions
The transcription file should be a text document with each line having the following format: `wavs/{name_of_file}.wav|{text}`. Use one of the included G2Ps to convert the transcription to the appropriate phonetic input.
# Training
The steps in the notebook should be rather self-explanitory, I hope. Upload your audio into the wavs/ folder before starting training. Here are some notes to keep in mind:
- Batch size should ideally be a factor of the amount of wavs you have. For example, when training a model with 15 wavs I set the batch size to 5.
- If you have the T4 GPU on Colab, do not set the batch size higher than 14.
- Output directory for training should be in Google Drive in case you get disconnected.
- As you train, checkpoints will build up. Delete old ones and empty trash to keep your drive storage available.
- Stop training when you get to an appropriate validation loss. For example, what I do is: less than 30 files = under 0.07; 30-100 files = under 0.09; 150+ files = under 0.1; more than 30 minutes of data = under 0.14
# Attributions
- TALQu phonetic system by Haruqa (https://booth.pm/ja/items/2755336)
- neuTalk Japanese phonetic system by neutrogic (https://github.com/neutrogic/neuTalk)
- TALQu pretrained model by Haruqa (https://github.com/Haruqa/tacotron2/releases)
- neuTalk Japanese and Mandarin pretrained models by neutrogic (https://github.com/neutrogic/neuTalk)
- French pretrained model created by Mildemelwe and trained by neutrogic (https://github.com/neutrogic)
- Some code formatting from the Uberduck Tacotron 2 training notebook (https://colab.research.google.com/drive/1WTilMdm9Vf7KE79gzkeeTBigAN6iv3Bg?usp=sharing)
- Tacotron 2 implementation by NVIDIA (https://github.com/NVIDIA/tacotron2)
