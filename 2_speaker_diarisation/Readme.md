# Speaker Diarization

A speaker diarization pipeline developed as part of the IIT Madras Speech Processing course (EE6130). The project combines speech segmentation, pretrained speaker embeddings, and agglomerative clustering to identify speaker turns in multi-speaker audio.

## Objective

Given a multi-speaker audio recording, determine:

> Who spoke when?

The project also investigates how the duration of speech segments affects speaker clustering.

## Approach

The diarization pipeline consists of:

```text
Audio
  ↓
Whisper-based Speech Segmentation
  ↓
ECAPA Speaker Embeddings
  ↓
Agglomerative Clustering
  ↓
Speaker Labels
```
