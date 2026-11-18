# Hybrid LoRA for Artistic Image Generation

> **MSc AI & Data Science research | Generative AI | Parameter-efficient fine-tuning | Responsible AI**

This project investigates parameter-efficient fine-tuning methods for adapting text-to-image diffusion models to artistic styles. It explores whether a hybrid low-rank adaptation approach can reduce training resource requirements while retaining visual fidelity and diversity.

## Research problem

Full fine-tuning of large generative models can be computationally expensive and difficult to access for independent researchers and artists. Low-Rank Adaptation (LoRA) offers a more efficient alternative by learning a small number of trainable parameters. However, different adapter designs make different trade-offs between parameter efficiency, adaptation capacity and output quality.

This research evaluates those trade-offs in the context of artwork generation.

## Research objectives

- Investigate parameter-efficient adaptation of pretrained diffusion models for artistic image generation.
- Compare standard LoRA with adaptive and alternative low-rank adapter methods.
- Develop and evaluate a hybrid approach combining adaptive rank allocation with a Hadamard-product adapter.
- Measure computational cost alongside generated-image quality.
- Consider the implications of style imitation and generative AI for artists, attribution and creative ownership.

## Methods and experimental scope

The experimental work centres on Stable Diffusion 1.5 and compares the following approaches:

| Method | Description |
|---|---|
| LoRA | Low-rank weight updates using a pair of trainable matrices |
| AdaLoRA | Adaptive allocation and pruning of rank components |
| LoHA | Low-rank adaptation using a Hadamard-product decomposition |
| AdaLoHA (hybrid) | Hybrid approach combining adaptive rank allocation with the LoHA parameterisation |

The hybrid method is the central research contribution explored in this project. Its performance should be interpreted in relation to the same dataset, training configuration and evaluation protocol used for the baselines.

## Evaluation

The evaluation plan considers both resource use and image quality:

- **Computational efficiency:** peak GPU memory and training time.
- **Image-text alignment:** CLIP-based similarity.
- **Distributional similarity:** Fréchet Inception Distance (FID).
- **Perceptual diversity / similarity:** LPIPS.

Results should be compared under consistent prompts, sampling settings, dataset splits and hardware conditions. Any reported benchmark should include its configuration so that it can be interpreted and reproduced.

## Tools and technologies

- Python
- PyTorch
- Hugging Face Diffusers
- Stable Diffusion 1.5
- Parameter-efficient fine-tuning methods
- Google Colab / NVIDIA T4 (target experimental environment)

## Responsible AI considerations

The project also examines the relationship between style-conditioned image generation and the interests of artists. Relevant questions include consent, attribution, ownership, the use of copyrighted training data, transparency about AI-generated work, and the effect of accessible generative tools on creative communities.

The intention is to consider technical efficiency and artistic responsibility together, rather than treating model performance as the only measure of success.

## Repository contents

This repository is the public research home for the dissertation project. The following materials should be added as they are prepared for release:

- [ ] Clean, independently runnable notebooks for each adapter method
- [ ] Dataset description, provenance and preprocessing instructions
- [ ] Experiment configurations and reproducibility notes
- [ ] Evaluation scripts and benchmark tables
- [ ] Representative generated samples, with prompts and settings
- [ ] Dissertation or research summary and presentation

No dataset or model weights are included by default. Check the relevant licences and usage terms before redistributing any third-party material.

## Current status and limitations

This README describes the research scope and intended evaluation. Quantitative findings should be added only alongside the corresponding experimental configuration and supporting outputs. The project should not be treated as independently reproducible until the notebooks, data instructions and evaluation materials have been published and tested.

## Research questions

1. How do LoRA, AdaLoRA and LoHA compare for artistic adaptation of a pretrained diffusion model?
2. Can the proposed hybrid method improve the trade-off between memory use and generated-image quality?
3. What evaluation protocol captures both fidelity and diversity in artwork generation?
4. How should efficient style adaptation account for artists' rights, attribution and creative agency?

---

**Author:** Anu Oloja  
**Research area:** Applied AI, generative models, efficient fine-tuning and responsible AI
