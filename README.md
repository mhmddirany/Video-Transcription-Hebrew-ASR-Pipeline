# Hebrew Video Transcription and Evaluation

This project evaluates different ASR models for Hebrew speech transcription.  
The goal is to compare transcription quality and speed using WER, CER, and RTF.

## Dataset

The evaluation was done on Hebrew audio clips.

- Total dataset: 9,360 clips
- Total duration: 451.4 minutes
- Evaluation subset: 610 clips
- Evaluation duration: 30 minutes

## Models Evaluated

The following models were tested:

- openai/whisper-large-v3
- ivrit-ai/whisper-large-v3-turbo
- OzLabs/Caspi-1.7B

Qwen/Qwen3-ASR-1.7B was not included in the final comparison because Hebrew is not officially supported.

## Evaluation Metrics

The models were evaluated using:

- WER: Word Error Rate
- CER: Character Error Rate
- RTF: Real-Time Factor

Lower WER, CER, and RTF values are better.

## Results

| Model | WER | CER | RTF |
|---|---:|---:|---:|
| ivrit-ai/whisper-large-v3-turbo | 22.93% | 14.15% | 0.185x |
| OzLabs/Caspi-1.7B | 25.02% | 12.21% | 0.419x |
| openai/whisper-large-v3 | 25.11% | 14.45% | 0.562x |

## Discussion

The ivrit-ai Whisper Turbo model achieved the best WER and was also the fastest model.  
Caspi achieved the best CER, meaning it produced fewer character-level mistakes.  
OpenAI Whisper Large v3 performed well but was slower than the other models.

## Conclusion

The best overall model is `ivrit-ai/whisper-large-v3-turbo` because it has the lowest WER and fastest inference time.  
Caspi is also useful when character-level accuracy is more important.
