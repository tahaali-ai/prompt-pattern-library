# Role-Play Prompting

## What it is

Role-play prompting means assigning the model a specific persona, role, or character before giving it a task. The role shapes how the model responds — its tone, vocabulary, level of detail, and even what it chooses to include or leave out.

It's one of the most flexible techniques in prompt engineering because the same task can produce very different results depending on the role you assign.

## When to use it

- When you need a very specific tone (expert, teacher, critic, etc.)
- When the audience matters — a doctor explaining something to a patient vs. a colleague
- When you want the model to stay consistent across a long conversation
- When default model responses feel too generic

## When it doesn't work well

- When the role conflicts with what the model is willing to do
- When you assign a vague role like "be helpful" — that changes nothing
- When the task is so simple that tone doesn't matter

---

## Example

**Task:** Explain what a neural network is

**Prompt without role:**
```
Explain what a neural network is.
```

**Output:** A standard textbook explanation with technical terms.

---

**Prompt with role — for a beginner:**
```
You are a patient teacher explaining AI concepts to a complete beginner 
who has no technical background. Use simple language and a real-world 
analogy. Explain what a neural network is.
```

**Output (Claude):**
```
Think of a neural network like your brain learning to recognize your 
friend's face. The first time you met them, you noticed things — the 
shape of their nose, the color of their eyes. Over time, the more you 
saw them, the faster you recognized them.

A neural network works the same way. It's made up of layers of simple 
units (like neurons in your brain) that each notice something small. 
Together, they learn patterns — and the more examples they see, 
the better they get.
```

---

**Prompt with role — for a technical audience:**
```
You are a senior ML engineer reviewing documentation for other engineers. 
Explain what a neural network is in precise technical terms.
```

**Output (Claude):**
```
A neural network is a computational graph composed of layers of 
parameterized linear transformations followed by non-linear activation 
functions. During forward propagation, input data flows through these 
layers producing an output. During training, backpropagation computes 
gradients of the loss with respect to each parameter, and an optimizer 
updates the weights to minimize that loss.
```

---

## Observations

- The same question, two completely different responses — just by changing the role
- The role affects vocabulary, analogies, assumed knowledge, and length
- Claude was particularly good at adapting tone based on audience
- The more specific the role, the more consistent the output across a long conversation

## Key takeaway

Before writing any prompt, ask yourself: who should be answering this? Defining that role upfront saves you multiple rounds of revision and gets you to the right output faster.
