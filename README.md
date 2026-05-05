# Reasoning in Vision-Language Models

Implementation of a mini Vision-Language Model (ViT + GPT-2) with Chain-of-Thought reasoning and prompt-based accuracy comparison on A-OKVQA.

## Overview

This project explores reasoning in Vision-Language Models (VLMs), especially for Visual Question Answering (VQA). Instead of directly predicting an answer, the model is trained to generate intermediate reasoning steps before producing the final answer.

The goal of this project is to better understand how multimodal reasoning can be implemented through:

- visual feature extraction
- vision-language alignment
- autoregressive language generation
- Chain-of-Thought style supervision
- prompt-based comparison between answer-only and reasoning-based generation

## Motivation

Most basic VQA models directly map an image-question pair to an answer. However, many visual reasoning tasks require commonsense reasoning, object understanding, and multi-step inference.

This project investigates whether a lightweight VLM architecture can learn to generate reasoning traces and improve interpretability on A-OKVQA-style questions.

## Model Architecture

The model consists of three main components:

```text
Image
  ↓
Vision Encoder (ViT)
  ↓
Vision Projector
  ↓
Language Model (GPT-2)
  ↓
Generated Reasoning + Answer
```
## 📊 Results

### Prompt Accuracy Comparison

| Prompt Type | Accuracy |
|------------|--------|
| Plain Prompt | 0.710 |
| CoT Prompt | **0.870** |

> CoT prompting improves accuracy from **71.0% → 87.0%** on A-OKVQA.

---
