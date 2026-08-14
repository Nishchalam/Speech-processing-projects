
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
Text Transcription 
