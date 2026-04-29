# Multimodal Idiom Understanding

Multimodal NLP system for selecting the image that best represents the **figurative** meaning of idiomatic phrases, using joint text-image encoding. Built as an Advanced AI coursework at Newcastle University.

## Overview

Idiomatic expressions (e.g. "secret santa", "ivory tower", "dirty money") carry figurative meanings that differ from their literal interpretations. This project builds a multimodal pipeline that, given an idiomatic phrase in context, selects the most appropriate image representing its figurative — not literal — meaning.

## Approach

### Text Processing
- Transformer-based encoder to represent idiomatic phrase context
- LLM-based data augmentation using **Groq API** (LLaMA) to expand low-resource idiom categories

### Image Encoding
- Vision encoder to produce image embeddings for candidate images

### Joint Ranking
- Cross-modal similarity scoring to rank candidate images
- Selects the image whose embedding best aligns with the figurative phrase embedding

### Data Augmentation
- **Google Gemini API** used for additional text augmentation
- **Groq (LLaMA)** used for sentence-level augmentation of idiomatic phrases

## Dataset

Idiomatic phrases drawn from the SemEval Multimodal Idiom Understanding task, including compound idioms such as:
- *dirty money*, *secret santa*, *ivory tower*, *low-hanging fruit*

Each phrase is paired with 3 candidate images; the model must identify the image matching the figurative sense.

## Files

| File | Description |
|------|-------------|
| `multimodal_idiom_understanding.ipynb` | Full pipeline: preprocessing, encoding, augmentation, evaluation |
| `Report_Advanced_Ai.pdf` | Detailed project report |

## Tech Stack

- Python 3
- HuggingFace Transformers
- Google Gemini API
- Groq API (LLaMA)
- PyTorch
- Google Colab
