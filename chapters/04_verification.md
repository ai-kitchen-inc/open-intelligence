# Chapter 4: The Verification Loop (Reasoning)

### The "System 1" Trap

Imagine you are on a game show. The host asks: *"What is 2 + 2?"*
You shout: *"Four!"* instantly.

Then the host asks: *"What is 34 multiplied by 82?"*
If you shout an answer instantly, you will be wrong. Your brain cannot hold that calculation in a single flash of intuition. You need to pause, grab a pen and paper, and work it out digit by digit.

In psychology, Daniel Kahneman calls this **System 1** (Fast Intuition) vs. **System 2** (Slow Reasoning).

For years, LLMs were stuck in **System 1**. When you asked GPT-3 a hard logic puzzle, it tried to "guess" the answer in one go. It didn't have a scratchpad. It didn't have a backspace key. It had to commit to the first word, then the second, endlessly falling forward. It was like trying to solve a Sudoku puzzle in pen without ever looking back at what you just wrote.

### The Magic Spell: "Let's Think Step by Step"

In 2022, researchers (Wei et al.) discovered a "magic spell."

They found that if you simply added the phrase *"Let's think step by step"* to the prompt, the model's intelligence skyrocketed.

Why?

Because you gave the model permission to **generate "thought tokens"** before generating the "answer token."

* **Prompt:** "What is 34 * 82?"
* **Standard Response:** "2700" (A guess. Wrong.)
* **Chain-of-Thought Response:** "First, 30 times 80 is 2400. Then 30 times 2 is 60... [Reasoning...] ... Therefore the answer is 2788."

Those intermediate words are the **Scratchpad**. By generating them, the model is putting its "working memory" onto the page. It can "read" what it just wrote to inform what it writes next. **Thinking is just the act of talking to yourself before you talk to the audience.**

### The DeepSeek-R1 Breakthrough: Self-Taught Reasoning

For a while, we thought we had to *teach* models how to reason by showing them thousands of examples of humans solving math problems.

Then came **DeepSeek-R1** (Guo et al., 2025). They tried something radical. They didn't show the model *how* to solve the problem. They just gave it a hard problem and a binary reward:

* **Correct Answer:** +1 Cookie.
* **Wrong Answer:** -1 Cookie.

At first, the model guessed randomly. But over thousands of tries, it stumbled on a strategy. It realized that if it generated a lot of gibberish text *before* the answer—exploring, backtracking, checking itself—it got the cookie more often.

It **invented** Chain-of-Thought.

It started saying things like: *"Wait, that doesn't look right. Let me check the calculation again. Ah, I missed a carry."*

Nobody told it to do that. It learned that **verification loops** (generating text to critique previous text) increased accuracy. It evolved an internal monologue purely for survival.

### Inference-Time Compute

This leads us to a new law of physics in AI: **Inference-Time Compute.**

Previously, we thought a model's intelligence was fixed after training.
Now we know: **You can buy intelligence with time.**

If you let the model "think" (generate hidden reasoning tokens) for 10 seconds, it is smarter than if you force it to answer in 1 second. We are trading "compute time" for "IQ points." We are moving from models that are just "Encyclopedias" to models that are "Thinkers."

---

### Summary of the Primitive

**Reasoning** is not a different algorithm; it is a **process**. It is the loop of generating a thought, reading it, critiquing it, and refining it. By allowing the model to "show its work" in the latent space (or the scratchpad), we allow it to solve problems that are far too complex for a single intuition.

**Next:** We have a model that can think deep thoughts. But it is expensive. Every time we ask it a simple question, we are firing up a trillion-parameter brain. That’s like using a supercomputer to calculate a tip. How do we make it efficient? We proceed to **Chapter 5: The Routing Architecture.**
