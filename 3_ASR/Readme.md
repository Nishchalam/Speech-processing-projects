
---

## 3. Assamese ASR

```markdown
# Assamese Automatic Speech Recognition

An automatic speech recognition project developed as part of the IIT Madras Speech Processing course (EE6130). The project fine-tunes OpenAI's Whisper-Tiny model for Assamese speech recognition using Mozilla Common Voice.

## Objective

Adapt a pretrained Whisper model to recognize Assamese speech and investigate how training hyperparameters affect ASR performance.

## Dataset

The Assamese subset of:

`mozilla-foundation/common_voice_11_0`

was used for fine-tuning.

Audio was resampled to 16 kHz to match Whisper's expected input format.

## Approach

The ASR pipeline consists of:

```text
Assamese Speech
      ↓
Audio Preprocessing
      ↓
Whisper Feature Extractor
      ↓
Whisper-Tiny
      ↓
Text Transcription `````
````

The WhisperProcessor was used for both audio feature extraction and text tokenization.

A custom data collator was implemented to handle variable-length audio features and transcription labels.

The pretrained: openai/whisper-tiny

checkpoint was fine-tuned using Hugging Face's Seq2SeqTrainer.

The experiments investigated the effect of:

Learning rate
Number of training epochs
Gradient accumulation
Mixed-precision training
Gradient checkpointing

Several configurations were compared, including learning rates of 1e-5 and 5e-6, different training durations, and gradient accumulation settings.

The primary evaluation metric was:WER was used to monitor validation performance and select the best-performing model.

Technologies
```
Python
PyTorch
Hugging Face Transformers
Hugging Face Datasets
Whisper-Tiny
Mozilla Common Voice
TensorBoard
CUDA / mixed-precision training
Repository Contents
asr-assamese-ipynb.ipynb — fine-tuning and evaluation notebook
ASR_EE24S004_Report.pdf — detailed report
````
