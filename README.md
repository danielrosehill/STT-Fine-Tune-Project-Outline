# STT Fine-Tuning Project

*August 28, 2025*

## Objectives

1. **STT fine-tuning** (personal use)
2. **Training data for voice note entity recognition model** (Voice Router)
3. **Smaller public/open source dataset** with annotations for various audio recording conditions for use in STT evaluations (personal, open source)

## Background

- Since about last year I've become a voice note taking fanatic! I'm hoping to use this dataset for a variety of purposes (above).
- I've extracted a dataset of about 700 voice notes from a voice note app. These contain:
  - 1x MP3 file
  - 1x TXT file (uncorrected AI transcript; likely Whisper)
  - In total, about 13 hours of audio

## Annotations Planned

| Annotation | Objective | Description |
|------------|-----------|-------------|
| **Corrected transcript** | STT fine-tune | Correct each transcript rectifying transcription errors |
| **Audio challenge tagging** | Evaluation set | Tag each transcript containing a specified subset of audio challenges to evaluate various STT models' ability to transcribe under 'real world' conditions - including crying babies and loud traffic |
| **Non-speaker audio** | Evaluation set | Voice notes containing audio that an intelligent STT model may be able to infer was not intended to be part of the transcript - such as interjections |
| **Background conversations** | Evaluation set | Tagging conversations picked up in background audio in foreign languages with language tagging |
| **Multilingual audio** | Evaluation set and reference | Transcriptions in which multiple languages were used |
| **Microphone used** | Evaluation set | Tagging for: Phone mic, Bluetooth mic, Desktop mic. Assesses various STTs' ability to transcribe on suboptimal hardware |
| **Note entity type** | App project | Entity classification based upon a defined set of common entities present in my voice note dataset |

## Computed Parameters

Added parameters that can be automatically populated:

- **Runtime**
- **Computed WPM and speech rate** (classification: 1 to 5)
- **Average dB level**

## Hugging Face Datasets

### Voice Note Audio (Public Dataset)
[https://huggingface.co/datasets/danielrosehill/Voice-Note-Audio](https://huggingface.co/datasets/danielrosehill/Voice-Note-Audio)

### Basic STT Evaluation for Synthetic Voice Notes
[https://huggingface.co/datasets/danielrosehill/STT-Voice-Notes-Evals](https://huggingface.co/datasets/danielrosehill/STT-Voice-Notes-Evals)

