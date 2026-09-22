# surfPRM

<div align="center">

[![Models](https://img.shields.io/badge/🤗_Hugging_Face-Models-blue)](https://huggingface.co/polowitty/surfPRM-qwen3.5-9b)
[![Dataset](https://img.shields.io/badge/🤗_Hugging_Face-Dataset-yellow)](https://huggingface.co/datasets/polowitty/surfPRM-data)
[![License](https://img.shields.io/badge/License-Apache_2.0-green)](#-license)

</div>

**surfPRM** is a process reward model (PRM) for web agents. Given the task intent,
the current page's accessibility tree (AXTree), and the previous action trajectory,
it evaluates candidate next actions and selects the better one with structured
`<State>/<Criteria>/<Analysis>/<Answer>` reasoning.

## 📦 Released Artifacts

| Artifact | Type | Link |
| :--- | :--- | :--- |
| surfPRM-qwen3.5-4b | Model (LoRA SFT, merged) | [polowitty/surfPRM-qwen3.5-4b](https://huggingface.co/polowitty/surfPRM-qwen3.5-4b) |
| surfPRM-qwen3.5-9b | Model (LoRA SFT, merged) | [polowitty/surfPRM-qwen3.5-9b](https://huggingface.co/polowitty/surfPRM-qwen3.5-9b) |
| surfPRM-data | Training data (9,821 pairwise step-preference samples) | [polowitty/surfPRM-data](https://huggingface.co/datasets/polowitty/surfPRM-data) |

## 🚀 Quick Start

Both models are standard Qwen3.5 checkpoints (merged LoRA, bfloat16) and can be loaded
with `transformers >= 5.6` via `AutoProcessor` / `AutoModelForImageTextToText`. Format
inputs with the prompt template documented in the model cards, then parse the preferred
action from the `<Answer>` tag of the output.

## 📜 License

This project is released under the Apache 2.0 license. Please also comply with the
[Qwen](https://huggingface.co/Qwen) base model license terms.
