# Multimodal Music Recommendation System using LLMs

A research project that combines **listening history, audio, lyrics, song metadata, and engagement signals** to recommend music. It extends the **E4SRec framework** so recommendations incorporate song content alongside user interaction patterns.

## How It Works

1. **Prepare listening histories:** Process LastFM-1K interactions into sessions and chronological training, validation, and test splits.
2. **Encode listening patterns:** Use SASRec, BERT4Rec, or GRU4Rec to generate item embeddings from listening sequences.
3. **Add song content:** Incorporate pretrained audio and lyric embeddings, plus LLM-generated metadata describing composition, vocals, and instruments.
4. **Combine features:** Experiment with concatenation, weighted sums, cross-attention, and feature-wise modulation (FiLM).
5. **Generate recommendations:** Project song representations into the LLM's embedding space and use listening histories to score candidate tracks. Metadata and estimated listening completion ratios can provide additional context.
6. **Evaluate:** Compare zero-shot and fine-tuned models using Recall, NDCG, MRR, and Precision.

## Experiments

- Compare LLaMA and Qwen model backbones.
- Evaluate different audio and lyric encoders.
- Test the contribution of individual modalities and fusion strategies.
- Use LoRA for parameter-efficient fine-tuning.

## Key Findings

Content features improve recommendation quality in several configurations, but gains depend on the model and fusion strategy. Lyric embeddings provide strong semantic signals, while simply combining every available feature does not consistently produce the best results.

## Technologies

Python · PyTorch · Hugging Face Transformers · PEFT/LoRA · Azure OpenAI · Pandas · NumPy

## Paper, Dataset, and Code

- [Research Paper](https://arxiv.org/abs/2606.00125)
- [Published Dataset](https://zenodo.org/records/20431748)
- [Original Implementation — E4SRec, LastFM Branch](https://github.com/sreehitha177/E4SRec/tree/LastFM)

This repository contains the project overview and paper. Training, preprocessing, metadata annotation, and evaluation code are available in the original implementation.
