# FACETGATE: Mitigating Multitask Interference in Vision-Language Models for Fine-Grained Offensive Meme Analysis

FACETGATE is a multimodal framework designed for fine-grained offensive meme analysis across Bangla, English, and code-mixed content. It is developed to improve task-specific Target prediction while preserving the performance of the remaining offensive-content classification tasks.

The framework introduces a specialized Target prediction pathway alongside a shared multimodal backbone. FACETGATE combines a **Gated Core-5** route with a **Selective HiReCon Target Expert (SHTE)**, allowing Target-related representations to be modeled separately while keeping the generalist prediction route intact.

This repository contains the source code, training and evaluation scripts, model configurations, and reproducibility resources used in the FACETGATE study.

## Dataset

Experiments are conducted on **M³Offend**, a multilingual and multimodal offensive meme dataset containing Bangla, English, and code-mixed memes.

The dataset includes:

- Meme images
- Human-corrected OCR text
- Predefined train, validation, and test splits
- Fine-grained annotation labels
- Language annotations
- Target-category annotations

The prediction tasks include:

- Offensive
- Vulgar
- Abuse
- Sarcastic
- Language
- Target

The M³Offend dataset is available on Hugging Face:

**Hugging Face:**  
https://huggingface.co/datasets/Shahadat364/M3Offend/

## FACETGATE Architecture

FACETGATE consists of two parallel components:

1. **Gated Core-5 Route**  
   Handles the general offensive-content prediction tasks while preserving the shared representation learned by the vision-language model.

2. **Selective HiReCon Target Expert (SHTE)**  
   Provides a specialized prediction pathway for the Target task, allowing Target-specific information to be modeled without substantially interfering with the Core-5 tasks.

The outputs of the two pathways are combined to produce the complete set of predictions.

## Repository Contents

This repository provides resources for reproducing the experiments reported in the FACETGATE study, including:

- FACETGATE implementation
- Model training scripts
- Evaluation scripts
- Model and experiment configurations
- Fine-tuning utilities
- Multitask prediction pipeline
- Reproducibility resources

## Research Use

This repository is intended for academic and research purposes in areas including:

- Multimodal offensive-content detection
- Multilingual meme understanding
- Vision-language models
- Multitask learning
- Fine-grained content moderation
- Target-aware offensive language analysis

## Citation

If you use FACETGATE or M³Offend in your research, please cite the corresponding paper.

Citation information will be updated after publication.

## Code and Dataset

- **Code:** This GitHub repository
- **Dataset:** https://huggingface.co/datasets/Shahadat364/M3Offend/

## Disclaimer

The dataset may contain offensive, abusive, vulgar, sarcastic, stereotypical, or otherwise sensitive content. These materials are included strictly for research purposes and do not represent the views of the dataset creators or authors.

Please use the dataset and code responsibly and in accordance with applicable licenses and ethical research practices.
