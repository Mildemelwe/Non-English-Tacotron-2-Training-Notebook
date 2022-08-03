# Non-English-Tacotron-2-Training-Notebook
Tacotron 2 training notebook supporting Japanese, French, and Mandarin
# Overview
This notebook is meant to provide easier access to training Tacotron 2 models in languages other than English. Currently, Japanese (TALQu and neuTalk phonetics), French, and Mandarin pretrained models are included, but the plan is to include more in the future, such as German.
# Supported audio
Audio for training should be 16-bit 22050hz mono WAV files. Do not include spaces in filenames. Files should only include alphanumerics (half-width), dashes, and underscores. This means no Japanese or Chinese filenames, or diacritics. Audio clips should be 10 seconds or less to facilitate learning. Based on my tests, I recommend having at least 15 minutes of audio.
# Transcriptions
The transcription file should be a text document with each line having the following format: `wavs/{name_of_file}.wav|{text}`.
