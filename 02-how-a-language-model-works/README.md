# AI101 · 02 — How a language model works

- **Video:** https://youtu.be/7wPjNNU4W5g (7:58, subtitles in 9 languages)
- **Task:** find a confident, wrong answer and post it in BUILD → https://t.me/ainarchyx
- **Nothing to install** in this lesson.

[Transcript](transcript.md) · [Subtitles](subtitles/) · [Glossary](../GLOSSARY.md) · [Lesson 01](../01-introduction/)

---

## In one minute

Your phone keyboard suggests the next word. A language model does the same thing, scaled up enormously: text is cut into **tokens**, the model predicts which token comes next, one is picked and added, and the loop repeats until the answer is done. Training sets the model's numbers once, at enormous cost. Running it uses those numbers without changing them. And because it produces what is *likely*, not what is *true*, it can be fluent and wrong.

## 1. Tokens: text becomes numbers

A model can't read letters or words. Text is first cut into **tokens**: whole words, pieces of words, or single characters such as punctuation. Every token has a number (its **token ID**), and the model only ever sees those numbers.

```
Language | models | don | 't | read | words | .
  14126     4211   1541  956  1373   4339    13      ← an illustration; real splits and IDs depend on the model
```

- Common words are usually one token; long or rare words are split ("unbelievable" might become *un · believ · able*).
- Each model has its own **tokenizer**, so the same text splits differently from model to model.
- The full list of tokens a model knows is its **vocabulary**. Meta's Llama 3 models have about 128,000.
- Rule of thumb for English: **100 tokens ≈ 75 words**.
- Other languages often need more tokens for the same meaning, up to 15 times more in one 2023 study. More tokens means slower answers, higher prices on paid services, and less text fitting in at once.
- This is also why chatbots long struggled to count the r's in "strawberry": the model sees something like *straw* + *berry*, not ten letters.

### Optional: see the tokens yourself

No account or install needed. Paste a sentence into a tokenizer page and watch it split:

- OpenAI's tokenizer: https://platform.openai.com/tokenizer
- The Tokenizer Playground on Hugging Face (several open models side by side): https://huggingface.co/spaces/Xenova/the-tokenizer-playground

Try the same sentence in English and in your own language, and compare the counts. Don't paste anything private: these are websites.

## 2. Predict, pick, repeat

You give the model a row of tokens. It gives back one thing: for **every** token in its vocabulary, how likely that token is to come next.

```
The capital of France is  ?
  Paris    ████████████████████████████████████  92 %
  the      █                                       2 %
  a        ▌                                       1 %
  …and the rest of the vocabulary: almost zero      ← an illustration, not real numbers
```

The program **picks** one token, adds it to the end, and feeds the whole row back in. **Predict, pick, repeat**, one token at a time, until the answer is finished. When a chatbot's reply appears piece by piece, that is the loop running.

- The pick is usually drawn from the top few candidates, not always the single most likely one. That's why the same question can get different answers. (Lesson 10 shows the setting behind it, *temperature*.)
- When a chatbot "thinks" before answering, that thinking is more tokens, produced the same way.

## 3. Why predicting is enough

To predict text well, a model has to pick up whatever helps prediction:

| Fill in the blank | What it takes |
|---|---|
| She ___ to the shop yesterday. | grammar |
| The Eiffel Tower is in ___. | facts |
| 12 + 7 = ___ | arithmetic |
| "Bonjour" in English is ___. | translation |
| …and the murderer is ___. | following a whole story |

Nobody programmed grammar or facts in. They are side effects of getting better at one simple game. But what the model learned is **what text tends to say**, which is usually, not always, what's true.

## 4. Training and running

| | Training | Running (inference) |
|---|---|---|
| What happens | Shown text with the next token hidden, the model guesses, and its numbers are nudged towards the right answer. Repeated trillions of times. | Your message goes in, tokens come out. |
| The numbers | change, a tiny bit at a time | **frozen**: they don't change while you chat |
| Scale | Llama 3: more than 15 trillion tokens, thousands of graphics chips, weeks to months | one machine, seconds |

- Training first produces a **base model**, which only continues text. A second stage, **fine-tuning** on examples of helpful conversations and on people's ratings of answers, turns it into an assistant.
- The model does **not** learn from your chat. Whether a company keeps your chats to train its next model is a separate question; lesson 04 covers it.
- A chatbot doesn't remember earlier messages: the app sends the **whole conversation** back in every turn. The amount a model can take in at once is its **context window**; in a very long chat the oldest parts may no longer fit. "Memory" features save notes and add them to the text that's sent in.

## 5. Why it makes things up

A language model produces **likely** next tokens, and there's no built-in step that checks whether they're **true**. When an answer appeared in its training text many times, likely and true usually line up. When it didn't, it still produces the most likely-sounding text: a name that sounds like a name, a date that looks like a date, a source that looks like a source.

- **A real case:** in 2023, two lawyers in New York filed a brief citing six court cases that ChatGPT had supplied. None of them existed. The judge fined the lawyers and their firm $5,000 (*Mata v. Avianca*).
- **Another reason:** a 2025 OpenAI paper argues that the way models are trained and tested often rewards guessing, like a multiple-choice exam where a blank scores zero but a guess sometimes scores.

**So check first:** specific, rare or recent facts, and above all names, numbers, dates, quotes and links. **What helps:** give the model the text you're asking about instead of relying on its memory, and open any source it gives you.

## Your task: find a confident, wrong answer

1. Use any chatbot you like.
2. Ask it something you can check: a precise date, a small town's population, a quote, or **a source** ("Give me a scientific paper about …, with the title and authors").
3. Check the answer: search the exact title in quotes, open the official site, or look the fact up somewhere reliable.
4. Post in **BUILD** (https://t.me/ainarchyx): the question, the answer, and how you found out it was wrong.

Leave out anything personal: no real names of private people, no health or account details. If every answer you get is right, post that too, with what you asked; that's useful to know.

## Words from this lesson

token · token ID · tokenizer · vocabulary · next-token prediction · base model · fine-tuning · inference · context window. All are in the [glossary](../GLOSSARY.md).

## What's next

**AI101 · 03 — What a model actually is:** a file full of numbers, and why making one costs millions while running one on your own computer costs little more than electricity.

## Sources

- OpenAI Help Center, "What are tokens and how to count them?" (1 token ≈ ¾ of an English word; 100 tokens ≈ 75 words).
- Meta AI, "Introducing Meta Llama 3: The most capable openly available LLM to date", 18 April 2024 (a vocabulary of 128K tokens; pretrained on over 15T tokens; two custom-built 24K-GPU clusters).
- A. Petrov, E. La Malfa, P. Torr, A. Bibi, "Language Model Tokenizers Introduce Unfairness Between Languages", NeurIPS 2023.
- TechCrunch, "Why AI can't spell 'strawberry'", 27 August 2024.
- L. Ouyang et al., "Training language models to follow instructions with human feedback", NeurIPS 2022.
- *Mata v. Avianca, Inc.*, No. 22-cv-1461 (PKC), S.D.N.Y., opinion and order on sanctions, 22 June 2023.
- A. T. Kalai, O. Nachum, S. Vempala, E. Zhang, "Why Language Models Hallucinate", arXiv:2509.04664, OpenAI, September 2025.

The token splits and IDs, probability numbers, the colour example and the made-up name, date and source in the video are illustrations, not real model output.

## Changes to this page

- 2026-11-22 — first version.
