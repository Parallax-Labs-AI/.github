<div align="center">

# Parallax Labs

**AI since 2026.**

Small models. Big reasoning.

[![HuggingFace](https://img.shields.io/badge/HuggingFace-parallaxlabs-white?style=flat-square&logo=huggingface&logoColor=black&labelColor=white)](https://huggingface.co/parallaxlabs)
[![Website](https://img.shields.io/badge/Website-labs.parallaxstudios.xyz-white?style=flat-square&labelColor=white)](https://labs.parallaxstudios.xyz)
[![Parent](https://img.shields.io/badge/Parallax%20Studios-parallaxstudios.xyz-white?style=flat-square&labelColor=white)](https://parallaxstudios.xyz)

</div>

---

## What we do

Parallax Labs is the AI research division of **Parallax Studios**. We build small language models that reason like ones hundreds of times their size.

Our work is guided by one rule: **every model we ship must run on hardware people actually own.** That means a hard ceiling of 15 billion parameters for local models, quantizations that fit on consumer GPUs, and a design philosophy that prioritizes accessibility over benchmark scores.

We don't chase benchmark numbers, we chase capability.

---

## Our models

### Parallax 2 Preview
The first public look at the Parallax-2 line. A 4 billion parameter model based on the proven Qwen 3.5 architecture, but trained specifically for reasoning skills comparable to models like Anthropic's Opus 4.7, and coding skillsets trained using GLM 5.2 datasets from Hugging Face.

| | |
| :--- | :--- |
| **Parameters** | 4B |
| **Base** | Qwen 3.5-4B |
| **Context** | 2K trained, 262K supported |
| **Quantizations** | FP16, Q4_K_M, Q2_K_L |
| **Minimum RAM** | 4 GB (Q4_K_M) |
| **Repo** | [`parallaxlabs/parallax-2-preview`](https://huggingface.co/parallaxlabs/parallax-2-preview) |

**[Try it in your browser →](https://labs.parallaxstudios.xyz/chat)** · **[Download on HuggingFace →](https://huggingface.co/parallaxlabs/parallax-2-preview)**

### Coming soon

- **Parallax 2 Mini** - A 2 billion parameter model, designed to run in a browser tab via WebLLM. Allowing users to run a surprisingly skilled AI, all in the web.
- **Parallax 2** - Our 14 billion parameter flagship model, designed for powerful coding skills, combined with immense powerful reasoning skills, and more to create the best local AI experience yet.
- **Parallax 2 Cloud** - a model that runs in the cloud (or on a local AI cluster for you tech nerds) with power exceeding even our best flagship local models.

---

## Our Values

**Local-first.**
We design our models to run effortlessly on local hardware with no issues. Absolutely no cloud service is required, no matter if you have an enthusiast GPU, a laptop with a half-decent CPU, or a cheap GPU with at least 8GB of VRAM, you can run Parallax models.

**Small by design.**
Our models are designed by choice to be small, to ensure that no matter your level of hardware, whether it be low-end, consumer, or enthusiast, you can run our models.

**Next Level Reasoning**
Our preview model, Parallax 2 Preview, a 4 billion parameter model, can out-reason significantly bigger models with its Opus 4.7-level reasoning skills.

---

## The 15B rule

Every model we ship for local use is capped at 15 billion parameters, by choice, not by limitation.

| Model size | Q4 file size | Runs on |
| :--- | :--- | :--- |
| 2B | ~1.4 GB | Phones, Chromebooks, browsers |
| 4B | ~2.8 GB | Laptops, 6GB GPUs |
| 14B | ~9 GB | 12GB GPUs, M-series Macs |
| 15B | ~10 GB | The ceiling |

We did this because once you start passing 15 billion parameters, the models start requiring much better hardware to run.

---

## Get started

### Run locally with Ollama

```bash
# Download the GGUF
curl -L https://huggingface.co/parallaxlabs/parallax-2-preview/resolve/main/parallax-labs.parallax-2-preview.Q4_K_M.gguf -o parallax.gguf

# Import into Ollama
echo "FROM $(pwd)/parallax.gguf" > Modelfile
ollama create parallax-2-preview -f Modelfile

# Chat
ollama run parallax-2-preview
