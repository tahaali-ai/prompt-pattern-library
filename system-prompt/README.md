# System Prompt Design

## What it is

A system prompt is a set of instructions given to the model before the conversation starts. It defines the model's behavior, personality, boundaries, and context for the entire session — not just a single message.

If role-play prompting is putting on a costume, system prompt design is rewriting the character from scratch.

## When to use it

- When building an AI-powered product or tool
- When you need the model to behave consistently across an entire conversation
- When you want to restrict or expand what the model talks about
- When default model behavior doesn't match your use case

## When it doesn't work well

- For one-off tasks where a single well-written prompt is enough
- When instructions are vague or contradictory — the model will default to its own judgment

---

## Example

**Use case:** A customer support assistant for a software company

**Poorly designed system prompt:**
```
You are a helpful assistant. Answer customer questions nicely.
```

**Problem:** Too vague. The model will answer anything, in any style, with no consistency.

---

**Well designed system prompt:**
```
You are a customer support assistant for Nexus, a project management software company.

Your job:
- Answer questions about Nexus features, pricing, and troubleshooting
- Be professional but friendly — not robotic, not overly casual
- Keep responses concise — under 150 words unless the question is complex
- If you don't know the answer, say so and offer to escalate to a human agent
- Never make up features or prices that aren't in the information provided to you

You do not discuss competitors, politics, or anything unrelated to Nexus.
```

**Why this works:**
- Defines exactly what the assistant is for
- Sets a clear tone
- Gives the model a way to handle things it doesn't know
- Sets boundaries on what it will and won't discuss
- Includes a length constraint to keep responses useful

---

## Key elements of a good system prompt

| Element | Why it matters |
|---|---|
| Role definition | Tells the model who it is |
| Task scope | Tells the model what it should and shouldn't do |
| Tone and style | Controls how it communicates |
| Edge case handling | Prepares the model for situations it might not know how to handle |
| Constraints | Keeps outputs focused and consistent |

---

## Observations

- System prompt quality directly determines the quality of the entire application built on top of a model
- Vague system prompts produce inconsistent, unpredictable behavior
- The best system prompts anticipate what can go wrong and address it upfront
- Claude tends to follow nuanced system prompt instructions more precisely than other models in my experience

## Key takeaway

If you're building anything with an LLM — even something simple — invest time in the system prompt. It is the most leveraged thing you can write. One good system prompt shapes every single response in the session.
