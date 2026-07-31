# Multimodal Music Recommendation System using LLMs

This project explores how Large Language Models (LLMs) can improve music recommendation by incorporating multimodal information beyond traditional item IDs. The proposed framework enriches the LastFM-1K dataset with LLM-generated semantic metadata, audio embeddings, lyric embeddings, and user engagement signals, enabling recommendation models to reason about a song’s content rather than relying solely on listening history. 

A large-scale multimodal benchmark was constructed by combining listening sessions with musicological annotations, acoustic features, neural audio embeddings, and lyric representations. Multiple recommendation backbones and fusion strategies were evaluated under both zero-shot and fine-tuned settings to understand how different modalities contribute to recommendation quality.

Experimental results show that multimodal enrichment consistently improves recommendation performance over traditional ID-based approaches, with lyric-based semantic representations providing the strongest gains. The study also highlights that naïve multimodal fusion is often insufficient, emphasizing the importance of effective cross-modal alignment for future recommendation systems. 

Dataset published: https://zenodo.org/records/20431748

Paper: https://arxiv.org/abs/2606.00125
