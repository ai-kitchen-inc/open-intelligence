# Chapter 6: The Tool-Use Framework (Agency)

## The Brain in a Jar

By 2023, we had built a genius. But it was a tragic genius.

Imagine the smartest person in the world, locked in a windowless room with no internet, no books, and no calculator. If you asked them: *"What is the weather in Tokyo right now?"* they would fail. They might guess (hallucinate), but they couldn't *know*.

Even worse, if you asked them: *"Calculate the square root of 4,829,102,"* they might try to do it in their head and get it wrong.

This was the limitation of **Parametric Memory**. The model's knowledge was frozen in its "weights" (its brain cells) on the day it finished training. It knew everything about the past, but nothing about the present. It was a brain in a jar.

## The Library Card: RAG (Retrieval-Augmented Generation)

The first step to freeing the brain was to give it a library card. This is **Retrieval-Augmented Generation (RAG)**.

Instead of forcing the model to memorize every fact (which leads to hallucinations), we allowed it to "cheat."
When you ask a question, the system first runs a Google Search (or database lookup), finds the relevant documents, and pastes them into the prompt *before* the model answers.

* **User:** "Who won the game last night?"
* **System (Hidden):** [Searches ESPN... Finds article... Pastes text: "The Warriors beat the Lakers 110-100."]
* **Model:** "The Warriors won 110-100."

The model didn't "know" who won. It just read the text we gave it. We turned a "Closed Book Exam" into an "Open Book Exam." This solved the two biggest problems in AI: **Freshness** (knowing new things) and **Hallucination** (making things up).

## The Hands: ReAct (Reason + Act)

But reading isn't enough. We wanted the model to *do* things. We wanted it to book flights, run Python code, and send emails.

The breakthrough here was the **ReAct** paper (Yao et al., 2022). It proposed a simple loop that turned a passive chatbot into an active **Agent**.

Instead of just talking to the user, the model talks to a "console."

1. **Thought:** "The user wants to calculate a mortgage. I am bad at math. I should use a calculator tool."
2. **Action:** `CALCULATOR.execute(500000 * 0.07)`
3. **Observation:** (The computer replies) `35000`
4. **Thought:** "Okay, the interest is 35k. Now I can answer the user."
5. **Response:** "The yearly interest is $35,000."

This is the birth of **Tool Use**. We taught the model that it has "API hands." If it outputs a specific text command (like `[SEARCH]`), the software freezes the model, runs the command in the real world, and feeds the result back into the model's ear.

## Toolformer: The Self-Teaching Craftsman

At first, we had to manually teach models how to use these tools. "Here is a calculator. Please use it."

Then came **Toolformer** (Schick et al., 2023). It proved that models could *teach themselves* when to use tools. By letting the model try to answer questions, and giving it a reward when it successfully used a tool to get the right answer, it learned its own limitations.

It learned: *"Every time I try to multiply big numbers, I fail. Every time I use the calculator tool, I win. Therefore, I will always use the calculator for math."*

It developed **epistemic humility**—the knowledge of what it *doesn't* know.

---

## Summary of the Primitive

The **Tool-Use Framework** marked the transition from **AI as a database** to **AI as an engine**. We stopped trying to cram the whole world into the model's weights. Instead, we taught the model to interface with the world. We gave the brain in the jar a set of hands and an internet connection.

**Next:** We have built the complete machine. It learns, it aligns, it reasons, it routes, and it acts. But *why* does it work? When we peer into the mathematical soup of neurons, what do we actually see? We conclude with **Chapter 7: The Latent Representation.**
