# Hebrew Video Transcription and Evaluation

This project evaluates different Automatic Speech Recognition (ASR) models for Hebrew speech transcription.

The goal is to compare transcription quality and speed using WER, CER, and RTF.

The project was tested on three different datasets to compare model performance across different Hebrew speech sources.

---

## Project Overview

The project includes:

- Loading Hebrew audio datasets
- Running ASR models
- Generating Hebrew transcriptions
- Comparing model outputs with reference transcripts
- Calculating evaluation metrics
- Comparing models based on accuracy and speed

---

## Datasets

This project worked on three Hebrew speech/transcription datasets.

### Dataset 1

Main Hebrew speech dataset used for model evaluation.

- Total clips: 9,360
- Total duration: 451.4 minutes
- Total duration in hours: 7.52 hours
- Evaluation subset: 610 clips
- Evaluation duration: 30 minutes

### Dataset 2

Hebrew YouTube video dataset used to test transcription on real video/audio.

### Dataset 3

Additional Hebrew audio/text dataset used for extra testing and comparison.

---

## Models Evaluated

The following ASR models were evaluated:

- `openai/whisper-large-v3`
- `ivrit-ai/whisper-large-v3-turbo`
- `OzLabs/Caspi-1.7B`

`Qwen/Qwen3-ASR-1.7B` was tested but removed from the final comparison because Hebrew is not officially supported.

---

## Evaluation Metrics

The models were evaluated using:

- WER
- CER
- RTF

---

## Results

| Model | WER | CER | RTF |
|---|---:|---:|---:|
| `ivrit-ai/whisper-large-v3-turbo` | 22.93% | 14.15% | 0.185x |
| `OzLabs/Caspi-1.7B` | 25.02% | 12.21% | 0.419x |
| `openai/whisper-large-v3` | 25.11% | 14.45% | 0.562x |

---

## Discussion

`ivrit-ai/whisper-large-v3-turbo` achieved the best WER and the fastest inference speed.

`OzLabs/Caspi-1.7B` achieved the best CER.

`openai/whisper-large-v3` gave good results, but it was slower than the other models.

---

## Conclusion

The best overall model is:

```text
ivrit-ai/whisper-large-v3-turbo
