# AI101 · 01 — Introduction: transcript

What the narrator says, chapter by chapter. Lines that only describe the picture are left out.

## 0:00 · Cold open

You've already used AI today. Probably before breakfast. Your phone recognised your face and unlocked. Your email quietly moved a scam into the spam folder. Your map guessed the traffic and changed your route. Your keyboard finished a word before you did. None of it said "artificial intelligence" on the box. It just worked, somewhere you couldn't see.

Then, a few years ago, a new kind arrived. The kind you can talk to. It writes, explains, translates and argues back. And almost all of it runs on someone else's computer.

This course is about understanding that kind of AI, from zero. And by the last lesson, you'll have one running on your own computer. No account. No subscription. No internet needed.

## 0:51 · What this course is

Welcome to AI101. It's for people who have never trained a model, never opened a terminal, and maybe aren't sure what a model even is. That's exactly the right place to start.

Here's the deal. It's free. There are no sponsors, no affiliate links, and nothing to buy. When we use a tool, we'll tell you why, and we'll show you at least one alternative. We'll be honest about what this technology can't do, not just what it can. And we'll go slowly. Every word gets explained the first time it appears.

What do you need? A computer. If it's from the last few years and has at least eight gigabytes of memory, it can very likely run a small model. Lesson five will tell you exactly what fits yours. You don't need to code. You don't need an expensive graphics card. You don't need to pay anyone.

One more thing. Tools in this field change every month. So the videos explain the ideas, and the exact steps live in a written guide that we keep up to date. The link is in the description.

## 1:57 · The words

Let's start with the words, because people use them loosely, and that causes a lot of confusion.

Artificial intelligence is the biggest circle. It's the whole field: getting machines to do things that would need intelligence if a person did them. Recognising a face. Planning a route. Playing chess. Understanding a sentence.

For decades, the main way to do that was to write the rules by hand. Imagine building a spam filter that way. If the email says "free money", it's spam. If it says "you won", it's spam. It works, until the scammers write "fr3e m0ney". Then you need another rule. And another.

Machine learning is the next circle in. Instead of writing the rules, you show the computer examples. Thousands of emails marked spam, thousands marked fine. The program finds the patterns itself, including ones no person would have thought to write down.

Deep learning is a circle inside that. It's machine learning done with neural networks: long chains of simple maths, stacked in many layers. Each layer passes numbers to the next. During training, millions or billions of those numbers are nudged, a tiny bit at a time, until the answers get better. "Deep" just means many layers. It's not deep in any mystical sense. It needs a lot of data and a lot of computing power, which is why it only really took off in the last fifteen years.

And inside deep learning is the circle this course is mostly about: language models. A language model is a neural network trained on enormous amounts of text to do one thing: predict what comes next. That sounds too simple to be useful. Lesson two shows why it isn't. The chatbots you've heard of are language models, wrapped in an app.

You'll also hear "generative AI". That means models that create something new: text, images, sound, video. Language models are one kind. Image generators are another.

So. AI is the field. Machine learning is learning from examples. Deep learning is doing that with many-layered neural networks. And language models are deep learning trained on text.

## 4:13 · Seventy years in three minutes

None of this started in 2022.

1950. The mathematician Alan Turing publishes a paper that opens with a simple question: can machines think? Instead of answering it, he proposes a test. If you can't tell a machine from a person in conversation, does the difference matter?

1956. A small group of researchers spends a summer at Dartmouth College in the United States. The proposal for that workshop is where the name "artificial intelligence" comes from. They expected real progress in a single summer.

1958. Frank Rosenblatt introduces the perceptron, an early machine that learns to recognise simple patterns from examples. It's a grandparent of every neural network today.

1966. Joseph Weizenbaum at MIT writes ELIZA, a program that imitates a therapist by turning your sentences back into questions. It understands nothing. And still, people confided in it. Weizenbaum later wrote that his own secretary, who had watched him build it, asked him to leave the room so she could talk to it in private. We still call this the ELIZA effect: we read a mind into anything that talks back fluently. Keep that in mind. It's still true.

Then the money ran out. The promises had been too big, and the computers too small. In the 1970s, and again in the late 1980s, funding dried up. These stretches are called AI winters.

1997. IBM's Deep Blue beats the world chess champion, Garry Kasparov. But Deep Blue didn't learn chess. It searched around two hundred million positions a second, using rules and evaluations its builders wrote by hand.

2012. Everything changes, quietly. A neural network called AlexNet enters a competition to recognise objects in photos, and wins by a huge margin. It was trained on two graphics cards, the same kind of chips built for video games. Graphics cards turned out to be very good at the maths neural networks need. Since then, deep learning has taken over almost the whole field.

2017. Eight researchers at Google publish a paper called "Attention Is All You Need". It introduces the transformer, a new design for neural networks that handles language far better and can be trained at enormous scale. The "T" in GPT stands for transformer.

2022. A chatbot built on a transformer goes public, and within weeks, it's everywhere.

2023. Meta shares its language model, LLaMA, with researchers. Within about a week, the weights leak to the whole internet. People start running it on their own laptops. Since then, a steady stream of open-weight models has followed, from labs in the United States, France and China. That stream is the reason this course can exist.

Notice the pattern. Big promises. Disappointment. A quiet breakthrough. Big promises again. What's different this time is three things arriving together. Oceans of text from the internet. Cheap parallel computing from graphics chips. And the transformer, to make use of both.

## 7:39 · Good at, bad at

So what can today's language models actually do well? Honestly, quite a lot. They're good at drafting and rewriting text. Summarising something long. Translating. Explaining an idea at your level, and then again more simply if you ask. Brainstorming. Helping with code. Turning messy notes into something organised.

And what are they bad at? They can be wrong with complete confidence. A language model produces what sounds likely, and "sounds likely" is not the same as "is true". When it invents facts, sources or quotes, that's called a hallucination. It only knows what was in its training data, up to a cut-off date, unless it's connected to a search tool. It doesn't know your life, your files or your situation unless you tell it.

And remember ELIZA. Fluent isn't the same as understanding.

Is it actually thinking? Serious researchers disagree, and we won't pretend to settle it in lesson one. For this course, one practical rule is enough. Treat it like a very fast, very well-read assistant who is sometimes confidently wrong. Use it. Learn from it. Check what matters.

## 8:53 · Where we're going

Here's the map. Part one: understand. How a language model works, what a model actually is, open versus closed, and whether your computer can run one. No installing anything yet. Part two: run it. How to download safely, your first local model without touching a terminal, then the terminal itself, choosing a model, and using it well. Part three: make it yours. Chatting with your own documents privately, voice and images, keeping it all healthy, and passing it on.

By the end, you'll have an AI that lives on your machine. It answers with the cable unplugged. No one else sees your conversations. No one can raise the price or switch it off.

This course is one part of something bigger. We're ainarchy, an open group of people who think everyone should be able to build with this technology, freely and for free. Every lesson ends with a small task in our Telegram group, in a room called BUILD. That's where the real learning happens: people helping people, at every level.

Your first task is easy. Go to BUILD and introduce yourself. Tell us what computer you have, if you know, and one thing you'd like to do with an AI that runs on your own machine. No personal details needed. That's it.

Next time: how a language model actually works, and why it sometimes makes things up. See you in lesson two.
