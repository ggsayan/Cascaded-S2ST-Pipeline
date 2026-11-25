# Cascaded Bengali-to-English Speech Translation Pipeline

Code, results and report for a cascaded pipeline that translates Bengali speech into English speech in the original speaker's voice. The pipeline transcribes the clip, romanizes the words, aligns them to the audio and marks the speaker's pauses, translates the pause-marked text, and synthesizes the translation with zero-shot voice cloning.

## Models

| Stage            | Model                                                                                                                       |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------- |
| Transcription    | [bodhan-ai/indic-transcribe-core](https://huggingface.co/bodhan-ai/indic-transcribe-core)                                   |
| Romanization     | [uroman](https://github.com/isi-nlp/uroman) (rule-based)                                                                    |
| Alignment        | `torchaudio.pipelines.MMS_FA`                                                                                               |
| Translation      | [bodhan-ai/indic-translate](https://huggingface.co/bodhan-ai/indic-translate)                                               |
| Speech synthesis | [multimodalart/higgs-audio-v3-tts-4b-transformers](https://huggingface.co/multimodalart/higgs-audio-v3-tts-4b-transformers) |

The models are downloaded from Hugging Face at run time and are not included here.
