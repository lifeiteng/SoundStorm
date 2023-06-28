# SoundStorm

# Progress
- [x] Implement modules
- [x] Training
- [x] End-To-End Synthesizer
- [x] Inference Sampling
- [x] Subjective Evaluation
- [x] Objective Evaluation
- [x] [Demo Page](https://lifeiteng.github.io/SoundStorm/index.html)

# Objective Evaluation
* `LibriTTS test clean`
* ASR WER `whisper large-v2`
* Speaker Embedding [https://huggingface.co/docs/transformers/model_doc/wavlm#transformers.WavLMForXVector](https://huggingface.co/docs/transformers/model_doc/wavlm#transformers.WavLMForXVector)

| Prompt | WER | Speaker cosine Similarity  | UtteranceLevel Pitch Mean MAE |  UtteranceLevel Pitch Std MAE |  UtteranceLevel Duration Diff | 
| ---- | ---- | ---- | ---- | ---- | ---- | 
| Ground Truth | 0.86 | - | - | - | - |
| 2 Seconds | 2.32 | 0.8670 | 20.1407 | 17.4387 | - |
| 4 Seconds | 2.10 | 0.8817 | 21.1379 | 19.3733 | - |
| 6 Seconds | 1.95 | 0.8905 | 17.2253 | 15.3792 | - |
| 8 Seconds | 2.33 | 0.8895 | 18.5837 | 15.9667 | - |
| 4 Seconds(PrefixPrompt) | 1.83 | 0.9351 | 12.0929 | 14.3814 | `1.5564 / 12.7153` (avg utter duration）|
