# AI101 · 01 — Introduction: what AI actually is

- **Video:** https://youtu.be/d9tA7JGl3sk (10:31, subtitles in 9 languages)
- **Task:** introduce yourself in BUILD → https://t.me/ainarchyx
- **Nothing to install** in this lesson.

[Transcript](transcript.md) · [Subtitles](subtitles/) · [Glossary](../GLOSSARY.md)

---

## In one minute

You already use AI every day: face unlock, spam filters, maps, your keyboard's next-word guess. A few years ago a new kind arrived, the kind you can talk to, and almost all of it runs on someone else's computer. This course explains that kind of AI from zero and ends with one running on your own machine, offline.

## The words

People use these words loosely. They are circles, one inside the other:

```
+-- Artificial intelligence ----------------------------+
|   the whole field                                     |
|   +-- Machine learning -----------------------------+ |
|   |   learning from examples,                       | |
|   |   not hand-written rules                        | |
|   |   +-- Deep learning --------------------------+ | |
|   |   |   machine learning with many-layered      | | |
|   |   |   neural networks                         | | |
|   |   |   +-- Language models ------------------+ | | |
|   |   |   |   trained on text to predict        | | | |
|   |   |   |   what comes next                   | | | |
|   |   |   +-------------------------------------+ | | |
|   |   +-------------------------------------------+ | |
|   +-------------------------------------------------+ |
+-------------------------------------------------------+
```

- **Artificial intelligence (AI)** is the whole field: getting machines to do things that would need intelligence if a person did them.
- **Machine learning**: instead of writing the rules (`if the email says "free money", it's spam`), you show the computer thousands of examples and it finds the patterns itself, including ones nobody would have thought to write down.
- **Deep learning**: machine learning done with **neural networks**, long chains of simple maths stacked in many **layers**. During **training**, millions or billions of numbers are nudged a tiny bit at a time until the answers get better. "Deep" just means many layers.
- **Language models**: neural networks trained on enormous amounts of text to do one thing, predict what comes next. The chatbots you've heard of are language models wrapped in an app. Lesson 02 shows why such a simple job turns out to be so powerful.
- **Generative AI** means models that create something new: text, images, sound, video. Language models are one kind; image generators are another.

## Seventy years in three minutes

| Year | What happened |
|---|---|
| 1950 | Alan Turing asks "Can machines think?" and proposes a test instead of an answer: if you can't tell a machine from a person in conversation, does the difference matter? |
| 1956 | A summer workshop at Dartmouth College (USA). Its 1955 proposal is where the name "artificial intelligence" comes from. |
| 1958 | Frank Rosenblatt's perceptron learns simple patterns from examples: a grandparent of today's neural networks. |
| 1966 | Joseph Weizenbaum's ELIZA imitates a therapist by turning your sentences into questions. It understands nothing, yet people confide in it. That's the **ELIZA effect**: we read a mind into anything that talks back fluently. |
| 1970s, late 1980s | **AI winters.** The promises were too big and the computers too small; funding dried up. |
| 1997 | IBM's Deep Blue beats Garry Kasparov at chess, by searching about 200 million positions a second with hand-written rules. It didn't learn chess. |
| 2012 | AlexNet wins an image-recognition contest by a huge margin, trained on two graphics cards (GPUs). Deep learning takes over the field. |
| 2017 | Google researchers publish "Attention Is All You Need", introducing the **transformer**. The "T" in GPT stands for transformer. |
| 2022 | A transformer-based chatbot goes public and is everywhere within weeks. |
| 2023 | Meta shares LLaMA with researchers; within about a week the weights leak online and people run it on their own laptops. A steady stream of **open-weight models** follows, from labs in the USA, France and China. That stream is why this course can exist. |

The pattern: big promises, disappointment, a quiet breakthrough, big promises again. What's different this time is three things arriving together: oceans of text from the internet, cheap parallel computing from graphics chips, and the transformer to make use of both.

## Good at, bad at

| Today's language models are good at | and bad at |
|---|---|
| drafting and rewriting text | being wrong with complete confidence |
| summarising something long | telling "sounds likely" apart from "is true" |
| translating | facts, sources and quotes: they sometimes invent them (**hallucination**) |
| explaining an idea at your level, then again more simply | anything after their **training cut-off**, unless connected to a search tool |
| brainstorming | your life, your files, your situation, unless you tell them |
| helping with code | |
| turning messy notes into something organised | |

And remember ELIZA: fluent isn't the same as understanding. Whether these models "think" is something serious researchers disagree about. For this course, one practical rule is enough:

> **Treat it like a very fast, very well-read assistant who is sometimes confidently wrong. Use it. Learn from it. Check what matters.**

## Your task: introduce yourself in BUILD

Go to the BUILD room in our Telegram group (**https://t.me/ainarchyx**) and tell us:

1. **What computer you have**, if you know: Windows, Mac or Linux, roughly how old, and how much memory (RAM). The steps below show where to look.
2. **One thing you'd like to do** with an AI that runs on your own machine.

No personal details needed. An answer can be as short as this:

> Windows 11 laptop from 2021, 16 GB RAM. I'd like to summarise my lecture notes without uploading them anywhere.

### Where to find your computer's details

You only need two things for now: the **processor** and the **memory (RAM)**. Don't post serial numbers or product keys; we never need them.

**Windows 11 or 10**
1. Open **Start → Settings → System → About**.
2. Under *Device specifications*, read **Processor** and **Installed RAM**.
3. Optional, if you're curious: press **Ctrl + Shift + Esc** to open Task Manager, go to **Performance** and click **GPU** to see your graphics chip and its memory. Lesson 05 explains why it matters.

**macOS**
1. Click the **Apple menu** (top left) → **About This Mac**.
2. Read **Chip** (or **Processor**) and **Memory**.

**Linux**
1. Open your desktop's **Settings → About** (on some systems: *System Details* or *System Info*).
2. Read **Processor** and **Memory**.

**Only a phone or tablet?** You can follow all of Part 1. The hands-on lessons need a computer; say so in BUILD and we'll think it through with you.

## What's next

**AI101 · 02 — How a language model works**, and why it sometimes makes things up.

The full course map is on the [front page](../README.md#lessons).

## Sources

- Alan Turing, "Computing Machinery and Intelligence", *Mind* 59 (236), 1950.
- J. McCarthy, M. Minsky, N. Rochester, C. Shannon, "A Proposal for the Dartmouth Summer Research Project on Artificial Intelligence", 31 August 1955. The workshop ran in summer 1956.
- Frank Rosenblatt, "The Perceptron: A Probabilistic Model for Information Storage and Organization in the Brain", *Psychological Review* 65 (6), 1958.
- Joseph Weizenbaum, "ELIZA — A Computer Program for the Study of Natural Language Communication between Man and Machine", *Communications of the ACM* 9 (1), 1966. The secretary story is from his book *Computer Power and Human Reason*, 1976.
- James Lighthill, "Artificial Intelligence: A General Survey", 1973.
- IBM, Deep Blue vs Garry Kasparov, May 1997 (about 200 million positions per second).
- A. Krizhevsky, I. Sutskever, G. Hinton, "ImageNet Classification with Deep Convolutional Neural Networks", NeurIPS 2012 (two NVIDIA GTX 580 GPUs; top-5 error 15.3% against 26.2% for the runner-up).
- A. Vaswani et al., "Attention Is All You Need", NeurIPS 2017.
- OpenAI, "Introducing ChatGPT", 30 November 2022.
- Meta AI, "Introducing LLaMA", 24 February 2023. The weights leaked online in early March 2023 (The Verge, 8 March 2023); llama.cpp ran it on laptops the same month.

The ELIZA conversation in the video is our own example, written in ELIZA's style. The word percentages in chapter 2 of the video are an illustration, not real numbers. The narration is a synthetic voice (Kokoro, an open-weight model) run on our own machine.

## Changes to this page

- 2026-11-22 — first version.
- 2026-11-22 — video link added.
