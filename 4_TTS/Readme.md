
---

## 4. Dutch Text-to-Speech

```markdown
# Dutch Text-to-Speech with SpeechT5

A text-to-speech project developed as part of the IIT Madras Speech Processing course (EE6130). The project fine-tunes Microsoft's SpeechT5 model for Dutch speech synthesis using VoxPopuli and speaker embeddings.

## Objective

Fine-tune a pretrained SpeechT5 model to synthesize Dutch speech from text while conditioning the generated speech on speaker characteristics.

## Dataset

The Dutch (`nl`) subset of the:

`facebook/voxpopuli`

dataset was used.

A subset of the available training data was selected for experimentation.

## Approach

The TTS pipeline consists of:

```text
Input Text
    ↓
SpeechT5 Text Encoder
    ↓
SpeechT5 Decoder
    ↓
Mel Spectrogram
    ↓
HiFi-GAN Vocoder
    ↓
Synthesized Speech `````
````
Speaker characteristics are incorporated using speaker embeddings extracted with a pretrained SpeechBrain speaker encoder.

The preprocessing pipeline includes:
Text normalization and tokenization.
Audio resampling and preprocessing.
Mel-spectrogram target generation.
Speaker embedding extraction.
Custom batching and padding for variable-length sequences.

The speaker embeddings were extracted using: speechbrain/spkrec-xvect-voxceleb
The pretrained SpeechT5 model was fine-tuned using:
Gradient accumulation
Gradient checkpointing
Mixed-precision training
Learning-rate scheduling
Sequence-to-sequence training

The model predicts mel spectrograms, which are subsequently converted into waveform audio using a HiFi-GAN vocoder.
After fine-tuning, the model was used to generate Dutch speech from text while conditioning the synthesis on speaker embeddings.

Technologies
```
Python
PyTorch
Hugging Face Transformers
Hugging Face Datasets
SpeechT5
SpeechBrain
X-vector speaker embeddings
HiFi-GAN
VoxPopuli
Repository Contents
tts-german.ipynb — implementation and experiments
Report.pdf — detailed report
````

Note: The notebook uses the Dutch (nl) VoxPopuli subset despite the original filename tts-german.ipynb.
