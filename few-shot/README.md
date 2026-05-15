# Few-Shot Prompting

## What it is

Few-shot prompting means giving the model a few examples of the task before asking it to do the real thing. The examples teach the model the format, style, and logic you expect — without you having to explain it in words.

Think of it like showing someone how to do something rather than describing it.

## When to use it

- When zero-shot keeps giving you the wrong format
- When you need outputs in a very specific style
- When the task has a pattern the model can pick up from examples
- When consistency across multiple outputs matters

## When it doesn't work well

- When your examples are low quality — bad examples teach bad habits
- When you only have one example (that's one-shot, and sometimes not enough)
- When the task is so unique that no example really captures it

---

## Example

**Task:** Generate a product description in a specific style

**Prompt:**
```
Here are two examples of product descriptions in our brand voice:

Example 1:
Product: Wireless Earbuds
Description: Forget the wires. Just your music, your pace, your world. 
Up to 30 hours of battery. Built for people who keep moving.

Example 2:
Product: Laptop Stand
Description: Your desk, elevated. Literally. Adjustable height, 
solid aluminum, and a posture your back will actually thank you for.

Now write one for:
Product: Mechanical Keyboard
```

**Output (ChatGPT):**
```
Every keystroke, intentional. Satisfying tactile feedback, 
customizable RGB lighting, and a build that means business. 
This is how you type when you mean it.
```

**Output (Claude):**
```
Type like you mean it. Tactile switches that click with purpose, 
a solid frame that doesn't flex, and enough customization to make it 
truly yours. Work that sounds as good as it feels.
```

---

## Observations

- Both models picked up the brand voice from just two examples — short, punchy, second-person
- Neither model needed to be told "write in a punchy style" — the examples did that work
- The quality of few-shot outputs is directly tied to the quality of your examples
- Claude leaned slightly more creative; ChatGPT stayed closer to the example structure

## Key takeaway

Few-shot prompting is one of the most powerful tools in prompt engineering. When you can't get consistent results with instructions alone, show the model what you want instead of telling it.
