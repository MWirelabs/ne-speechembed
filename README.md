<div align="center">

# NE-SpeechEmbed

**First speech-text retrieval model for Northeast Indian languages.**

[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97-MWirelabs%2Fne--speechembed-yellow)](https://huggingface.co/MWirelabs/ne-speechembed)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

</div>

---

## Architecture

- **Speech encoder:** Whisper-medium (fine-tuned on NE-ASR, checkpoint-8000)
- **Text encoder:** xlm-roberta-base
- **Projection:** Linear(1024→768) speech, Linear(768→768) text
- **Loss:** InfoNCE with learned temperature
- **Embed dim:** 768 (L2 normalized)

## Languages

Khasi, Garo, Mizo, Nagamese, Kokborok, Assamese, Wancho, Chakma

## Retrieval Results (100-sample pool)

| Language | R@1 | R@5 | R@10 |
|---|---|---|---|
| Khasi | 5.0% | 19.0% | 27.0% |
| Garo | 7.0% | 21.0% | 33.0% |
| Mizo | 5.0% | 17.0% | 30.0% |
| Nagamese | 5.0% | 19.0% | 30.0% |
| Kokborok | 8.0% | 24.0% | 35.0% |
| Random | 1.0% | 5.0% | 10.0% |

## Training Data

73,476 speech-text pairs from proprietary MWire corpora and Vaani.

## Citation

NE-MultiSpeech: Multilingual ASR and Speech-Text Embeddings for Northeast Indian Languages (EMNLP ARR May 2026)

## License

CC-BY-4.0 -- MWire Labs
