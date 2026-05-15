# Chain-of-Thought Prompting

## What it is

Chain-of-thought prompting is a technique where you ask the model to think through a problem step by step before giving the final answer. Instead of jumping straight to a conclusion, the model shows its reasoning — which usually makes the answer more accurate and easier to verify.

The simplest way to trigger it: just add "think step by step" to your prompt.

## When to use it

- Math problems and logical reasoning tasks
- Any multi-step problem where the order of steps matters
- When you want to check the model's reasoning, not just its answer
- Complex decisions that involve weighing multiple factors

## When it doesn't work well

- Simple factual questions — asking for step-by-step reasoning on "what is the capital of France" just adds noise
- When you need a very short output and reasoning would bloat the response

---

## Example

**Task:** Solve a word problem

**Prompt without chain-of-thought:**
```
A store sells apples for $1.50 each and oranges for $2.00 each. 
Sara bought 4 apples and 3 oranges. She paid with a $20 bill. 
How much change did she get?
```

**Output:** `$8.00` *(incorrect)*

---

**Prompt with chain-of-thought:**
```
A store sells apples for $1.50 each and oranges for $2.00 each. 
Sara bought 4 apples and 3 oranges. She paid with a $20 bill. 
How much change did she get? Think through this step by step.
```

**Output (ChatGPT):**
```
Step 1: Cost of apples → 4 × $1.50 = $6.00
Step 2: Cost of oranges → 3 × $2.00 = $6.00
Step 3: Total cost → $6.00 + $6.00 = $12.00
Step 4: Change → $20.00 - $12.00 = $8.00

Sara gets $8.00 in change.
```

**Output (Claude):**
```
Let me work through this:
- 4 apples at $1.50 each = $6.00
- 3 oranges at $2.00 each = $6.00
- Total = $12.00
- Change from $20 = $8.00

Sara received $8.00 in change.
```

---

## Observations

- In this case both approaches gave the same answer — but for harder problems, chain-of-thought makes a significant difference in accuracy
- Showing the reasoning also makes it easy to spot exactly where a model goes wrong, which is useful for debugging prompts
- "Think step by step" is not magic — for very complex tasks you may need to structure the steps yourself in the prompt

## Key takeaway

Whenever accuracy matters and the task has multiple steps, always ask the model to reason before it answers. It takes one extra sentence in your prompt and noticeably improves reliability.
