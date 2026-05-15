# Prompt Pattern Library

A personal collection of prompting techniques I've studied and tested across different large language models. Each pattern includes an explanation of what it is, when to use it, the actual prompt, and the real output I got.

The goal of this repo is simple — to document what works, what doesn't, and why. Prompting is more of a craft than people think, and the only way to get better at it is to be systematic about it.

---

## Patterns covered

| Pattern | What it is |
|---|---|
| [Zero-shot prompting](./zero-shot/README.md) | Asking the model with no examples |
| [Few-shot prompting](./few-shot/README.md) | Giving examples before the actual task |
| [Chain-of-thought prompting](./chain-of-thought/README.md) | Getting the model to reason step by step |
| [Role-play prompting](./role-play/README.md) | Assigning a persona to shape the response |
| [System prompt design](./system-prompt/README.md) | Setting context and behavior at the system level |

---

## How this repo is structured

Each folder covers one pattern. Inside you'll find:
- A plain-English explanation of the technique
- When to use it and when not to
- A real prompt example
- The actual output from the model
- Key observations and takeaways

---

## Models used

- ChatGPT (GPT-4)
- Claude (Sonnet)
- Gemini (1.5 Pro)

---

*This is a living document — I update it as I learn and experiment more.*
