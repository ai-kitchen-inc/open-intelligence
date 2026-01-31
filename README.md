# The Architecture of Intelligence
**Subtitle:** A Conceptual Guide to the Primitives of Large Language Models

## Purpose
This repository is a clear, citation-friendly guide to the **Primitives of Intelligence**—the minimal building blocks that make modern AI work. It is written for readers who want to understand *how* AI works without heavy jargon.

We aim to create a **legacy repository**: a clear historical map of how AI techniques evolved, why they worked, and how they connect.

## Design Principles
1. **Plain English First**: Every concept is explained like a human would teach another human.
2. **Layered Learning**: Each chapter moves from intuition to engineering to references.
3. **Concepts > APIs**: We focus on enduring ideas, not fleeting frameworks.
4. **Minimalism**: One chapter, one primitive. No clutter.
5. **Traceable Lineage**: Each chapter links to the foundational papers that changed the field.

---

# Repo Structure
```
/README.md                → The front door (this file)
/chapters/                → The book, one chapter per file
/chapters/01_attention.md
/chapters/02_compression.md
/chapters/03_alignment.md
/chapters/04_verification.md
/chapters/05_routing.md
/chapters/06_tools.md
/chapters/07_latent_space.md
/appendix/                → Extra notes, glossary, references
/timeline/                → Historical timeline of key AI milestones
```

---

# Read the Chapters
Start anywhere, but Chapter 1 is a good entry point. Each abstract summarizes the chapter’s focus and key ideas.

1. **[The Attention Primitive (Context)](chapters/01_attention.md)**  
   *Attention replaces the sequential bottleneck with parallel relevance weighting across tokens. It is a Q/K/V look-up mechanism that lets the model link distant ideas and scale context efficiently (e.g., FlashAttention).*

2. **[The Compression Principle (Capacity)](chapters/02_compression.md)**  
   *Prediction drives understanding: models act as lossy compressors of relationships rather than memorizing text. Scaling laws and data/parameter ratios (e.g., Chinchilla) explain how capacity and data shape performance.*

3. **[The Alignment Interface (Control)](chapters/03_alignment.md)**  
   *Alignment turns base completion models into helpful systems by injecting preference signals. It spans supervised instruction, RLHF reward modeling, and direct preference optimization to steer behavior.*

4. **[The Verification Loop (Reasoning)](chapters/04_verification.md)**  
   *Reasoning emerges from deliberate, iterative verification rather than one-shot answers. Inference-time compute, self-correction, and synthetic reasoning data improve correctness and reliability.*

5. **[The Routing Architecture (Efficiency)](chapters/05_routing.md)**  
   *Mixture-of-Experts addresses dense compute waste by routing tokens to specialized experts. Conditional computation yields large capacity with lower inference cost.*

6. **[The Tool-Use Framework (Agency)](chapters/06_tools.md)**  
   *Tool use expands models beyond parametric memory via retrieval and actions. RAG supplies external context while ReAct-style loops teach when to call APIs and interpret observations.*

7. **[The Latent Representation (Universality)](chapters/07_latent_space.md)**  
   *Latent space organizes concepts as directions in high-dimensional space. Monosemanticity and the Platonic hypothesis suggest convergent internal maps across large models.*

---

# Chapter Abstracts & Key Ideas
These chapter abstracts capture the distilled engineering ideas without internal authoring prompts.

## Chapter 1: The Attention Primitive
**Abstract:** Attention replaces sequential processing with parallel relevance weighting, letting models connect distant concepts and scale context efficiently.

**Key Ideas:**
- **Sequential Bottleneck:** RNNs processed data linearly, losing long-range context.
- **Parallelization as Key:** Transformers process full sequences at once, enabling GPU efficiency.
- **Relevance Weighting:** Attention scores relationships between every pair of tokens.
- **Look-Up Mechanism (Q/K/V):** Query-Key-Value acts like a database lookup.
- **Context Window:** The model’s working memory; FlashAttention improves memory IO.

---

## Chapter 2: The Compression Principle
**Abstract:** Intelligence emerges from compressing vast data into predictive rules; scaling laws and data/parameter balance reveal how capacity drives performance.

**Key Ideas:**
- **Prediction is Understanding:** Prediction requires modeling underlying structure.
- **Lossy Compression:** Models store relationships, not verbatim text.
- **Scaling Laws:** Performance scales with data/compute in a power-law.
- **Token-to-Parameter Ratio:** Chinchilla highlights optimal data-to-model size.

---

## Chapter 3: The Alignment Interface
**Abstract:** Alignment turns raw completion engines into helpful systems by injecting human preference signals through instruction and preference optimization.

**Key Ideas:**
- **Base vs. Instruct:** Base models complete; instruct models follow tasks.
- **Preference Signal:** Helpfulness requires human preference data.
- **RLHF:** Reward models score outputs.
- **DPO:** Directly optimizes toward preferred answers.

---

## Chapter 4: The Verification Loop
**Abstract:** Reasoning improves when models are encouraged to verify and refine answers, using additional inference-time compute and self-correction.

**Key Ideas:**
- **System 1 vs. System 2:** Fast answers vs. deliberate reasoning.
- **Inference-Time Compute:** More thinking time improves outcomes.
- **Self-Correction:** Models can verify when incentivized.
- **Synthetic Data:** Models can generate high-quality reasoning data.

---

## Chapter 5: The Routing Architecture
**Abstract:** Mixture-of-Experts increases capacity efficiently by routing tokens to specialized sub-models instead of activating all parameters.

**Key Ideas:**
- **Dense Compute Waste:** Standard models activate all parameters every time.
- **Conditional Computation:** Only some experts activate per token.
- **Router:** A controller selects experts.
- **Economic Efficiency:** Large capacity with cheaper inference.

---

## Chapter 6: The Tool-Use Framework
**Abstract:** Tool use extends model capability with retrieval and actions, enabling open-book reasoning and interaction with external systems.

**Key Ideas:**
- **Parametric vs. Non-Parametric Memory:** Weights vs. retrieval.
- **ReAct Loop:** Thought → Action → Observation → Thought.
- **API Calls:** Models learn when to use tools.

---

## Chapter 7: The Latent Representation
**Abstract:** Concepts live as directions in a high-dimensional latent space; evidence suggests convergence toward shared internal maps.

**Key Ideas:**
- **Black Box Problem:** We build models without full interpretability.
- **Linear Representation:** Concepts can be linear directions.
- **Monosemanticity:** Some neurons map to single concepts.
- **Platonic Hypothesis:** Large models converge on similar internal maps.

---

# How to Contribute
This project values clarity over hype. If you want to contribute:
- Teach one idea **well**.
- Use analogies sparingly and precisely.
- Cite foundational papers.
- Keep the writing timeless.

---

# References (Harvard Style)
1. Vaswani, A. et al. (2017) ‘Attention is all you need’, *Advances in Neural Information Processing Systems (NeurIPS)*.
2. Alammar, J. (2018) ‘The illustrated transformer’, *Blog post*.
3. Devlin, J. et al. (2018) ‘BERT: Pre-training of deep bidirectional transformers for language understanding’, *arXiv preprint* arXiv:1810.04805.
4. Brown, T.B. et al. (2020) ‘Language models are few-shot learners’, *Advances in Neural Information Processing Systems (NeurIPS)*.
5. Kaplan, J. et al. (2020) ‘Scaling laws for neural language models’, *arXiv preprint* arXiv:2001.08361.
6. Hoffmann, J. et al. (2022) ‘Training compute-optimal large language models’, *arXiv preprint* arXiv:2203.15556.
7. Touvron, H. et al. (2023) ‘LLaMA: Open and efficient foundation language models’, *arXiv preprint* arXiv:2302.13971.
8. Su, J. et al. (2021) ‘RoFormer: Enhanced transformer with rotary position embedding’, *arXiv preprint* arXiv:2104.09864.
9. Dao, T. et al. (2022) ‘FlashAttention: Fast and memory-efficient exact attention with IO-awareness’, *Advances in Neural Information Processing Systems (NeurIPS)*.
10. Lewis, P. et al. (2020) ‘Retrieval-augmented generation for knowledge-intensive NLP tasks’, *Advances in Neural Information Processing Systems (NeurIPS)*.
11. Ouyang, L. et al. (2022) ‘Training language models to follow instructions with human feedback’, *Advances in Neural Information Processing Systems (NeurIPS)*.
12. Rafailov, R. et al. (2023) ‘Direct preference optimization: Your language model is secretly a reward model’, *Advances in Neural Information Processing Systems (NeurIPS)*.
13. Wei, J. et al. (2022) ‘Chain-of-thought prompting elicits reasoning in large language models’, *Advances in Neural Information Processing Systems (NeurIPS)*.
14. Yao, S. et al. (2023) ‘ReAct: Synergizing reasoning and acting in language models’, *International Conference on Learning Representations (ICLR)*.
15. Guo, D. et al. (2025) ‘DeepSeek-R1: Incentivizing reasoning capability in LLMs via reinforcement learning’, *Technical report*.
16. Yang, A. et al. (2025) ‘Qwen3 technical report’, *Technical report*.
17. Shazeer, N. et al. (2017) ‘Outrageously large neural networks: The sparsely-gated mixture-of-experts layer’, *International Conference on Learning Representations (ICLR)*.
18. Fedus, W. et al. (2021) ‘Switch transformers: Scaling to trillion parameter models with simple and efficient sparsity’, *Journal of Machine Learning Research*.
19. Mistral AI (2024) ‘Mixtral of experts’, *Technical report*.
20. Komatsuzaki, A. et al. (2022) ‘Sparse upcycling: Training mixture-of-experts from dense checkpoints’, *International Conference on Learning Representations (ICLR)*.
21. Huh, M. et al. (2024) ‘The platonic representation hypothesis’, *arXiv preprint* arXiv:2405.07987.
