Language Identification: Developed a multilingual speech-language classifier using pretrained Wav2Vec2/HuBERT representations and CNN-based classification.
Speaker Diarization: Built a diarization pipeline combining Whisper-based speech segmentation, ECAPA-TDNN speaker embeddings, and agglomerative clustering, with experiments on segment duration.
ASR: Fine-tuned Whisper-Tiny for Assamese speech recognition using Mozilla Common Voice and evaluated performance using Word Error Rate (WER).
TTS: Fine-tuned SpeechT5 for German speech synthesis using speaker embeddings and a HiFi-GAN vocoder.
