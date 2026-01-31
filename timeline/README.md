# AI Timeline

A concise timeline of milestones that shaped modern large language models, grouped by era. This is a living document and will expand as chapters mature.

## Phase I: The Theoretical Bedrock (1950–2010)
*Before we had the data or the hardware, we had the math.*

| Year | Milestone | Why it matters (The Primitive) |
| --- | --- | --- |
| **1950** | **The Turing Test** (Alan Turing) | **Defined the Goal.** Shifted the question from "Can machines think?" to "Can machines imitate?" This set the target for modern generative AI. |
| **1957** | **The Perceptron** (Frank Rosenblatt) | **The First Neuron.** Introduced the idea that a machine could learn by adjusting weights based on error, though it could not solve XOR yet. |
| **1986** | **Backpropagation** (Hinton et al.) | **The Learning Signal.** Solved how to train multi-layer networks by flowing error backward to update the network. |
| **1997** | **LSTM** (Hochreiter & Schmidhuber) | **Memory.** Solved the vanishing gradient problem, letting networks hold longer context. |

## Phase II: The Deep Learning Ignition (2012–2016)
*We found the hardware (GPUs) and the representation (embeddings).*

| Year | Milestone | Why it matters (The Primitive) |
| --- | --- | --- |
| **2012** | **AlexNet wins ImageNet** | **The GPU Moment.** Proved that large neural networks trained on GPUs could outpace hand-engineered features. |
| **2013** | **Word2Vec** (Mikolov/Google) | **Latent Space (Chapter 7).** Showed meaning can be represented as geometry in vector space (e.g., King - Man + Woman = Queen). |
| **2014** | **Seq2Seq** (Sutskever et al.) | **Encoder-Decoder.** Established the translation blueprint: encode a sentence to a vector, then decode it. |
| **2015** | **ResNet** (He et al.) | **Depth.** Skip connections let information flow through hundreds of layers without vanishing. |

## Phase III: The Transformer Revolution (2017–2020)
*The architecture that allowed us to eat the internet.*

| Year | Milestone | Why it matters (The Primitive) |
| --- | --- | --- |
| **2017** | **Attention Is All You Need** (Vaswani et al.) | **The Attention Primitive (Chapter 1).** Replaced sequential processing with parallel attention across tokens. |
| **2018** | **BERT** (Devlin/Google) | **Bidirectionality.** Taught models to read both left and right context for stronger understanding. |
| **2019** | **GPT-2** (OpenAI) | **Zero-Shot Learning.** Demonstrated task generalization from broad pretraining. |
| **2020** | **GPT-3 & Scaling Laws** (Kaplan/OpenAI) | **The Compression Principle (Chapter 2).** Established power-law scaling with data and compute. |

## Phase IV: Optimization & Alignment (2021–2023)
*Making them efficient, obedient, and helpful.*

| Year | Milestone | Why it matters (The Primitive) |
| --- | --- | --- |
| **2021** | **Switch Transformers** (Google) | **The Routing Architecture (Chapter 5).** Mixture of Experts scales capacity without linear compute cost. |
| **2022** | **Chinchilla** (DeepMind) | **Data Efficiency.** Corrected scaling laws by showing models were under-trained relative to data. |
| **2022** | **InstructGPT / ChatGPT** (OpenAI) | **The Alignment Interface (Chapter 3).** RLHF turned base models into helpful assistants. |
| **2022** | **FlashAttention** (Dao et al.) | **Context Window.** IO-aware attention enabled long-context scaling. |
| **2023** | **LLaMA** (Meta) | **Open Weights.** Proved smaller, well-trained open models could rival closed labs. |

## Phase V: The Agentic Frontier (2024–Present)
*Thinking, reasoning, and acting.*

| Year | Milestone | Why it matters (The Primitive) |
| --- | --- | --- |
| **2023** | **Toolformer & RAG** | **The Tool-Use Framework (Chapter 6).** Shifted models from memorization to tool-enabled utilization. |
| **2024** | **DPO** (Rafailov et al.) | **Alignment Stability.** Simplified alignment by optimizing preferences directly. |
| **2024** | **Golden Gate Claude** (Anthropic) | **Interpretability (Chapter 7).** Mapped neurons to concepts, advancing monosemanticity. |
| **2025** | **DeepSeek-R1** (DeepSeek) | **The Verification Loop (Chapter 4).** Reinforcement learning alone induced stronger reasoning. |

## How to read this timeline
Each milestone connects to a chapter primitive. The goal is to track the lineage of ideas, not to be exhaustive.
