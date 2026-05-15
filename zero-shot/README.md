# Zero-Shot Prompting

## What it is

Zero-shot prompting means asking a model to do something without giving it any examples. You just describe the task and let the model figure it out on its own using what it already knows from training.

It's the most common way people use AI — they just don't realize it has a name.

## When to use it

- When the task is straightforward and well-defined
- When you want a quick answer without setting up a full prompt
- When the model is likely to have seen similar tasks during training

## When it doesn't work well

- Complex tasks that need a specific format or style
- Situations where the model keeps misunderstanding what you want
- Tasks requiring very specific domain knowledge

---

## Example

**Task:** Classify the sentiment of a customer review

**Prompt:**
```
Classify the sentiment of this review as Positive, Negative, or Neutral.

Review: "The delivery was late and the packaging was damaged, but the product itself works fine."
```

**Output (ChatGPT):**
```
Neutral
```

**Output (Claude):**
```
Neutral — the review contains both negative aspects (late delivery, damaged packaging) 
and a positive one (product works fine), which balance out to an overall neutral sentiment.
```

**Output (Gemini):**
```
Neutral
```

---

## Observations

- All three models got the correct classification
- Claude gave the most detailed reasoning without being asked — useful when you need explainability
- ChatGPT and Gemini were more concise — better when you just need the label
- Zero-shot works well here because sentiment classification is a very common NLP task these models have seen many times

## Key takeaway

Zero-shot is your starting point. If the model gets it right, you're done. If it keeps missing the mark, move to few-shot and give it examples.
