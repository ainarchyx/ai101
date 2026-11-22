# AI101 · 02 — How a language model works: transcript

What the narrator says, chapter by chapter. Lines that only describe the picture are left out.

## 0:00 · Cold open

Open the keyboard on your phone and start a message. Above the keys, it suggests the next word. Tap the middle suggestion, again and again. You get a sentence that sounds a bit like you, and means almost nothing.

Now take the same idea and scale it up enormously. Train it on a huge share of everything written online. It stops producing nonsense. It writes essays, answers questions and fixes code. That's a language model. This lesson is about how it works, and why it sometimes makes things up.

## 0:36 · Tokens

A computer can't read words. It can only work with numbers. So the first step is to cut text into small pieces, called tokens. A token can be a whole word, part of a word, or a single character such as a full stop. Each token has a number, its ID, and the model only ever sees those numbers.

Common words are usually a single token. Longer or rarer words get split into pieces. "Unbelievable" might become three tokens. The exact pieces depend on the model; each one has its own way of splitting text, called a tokenizer.

The full list of tokens a model knows is its vocabulary. Meta's Llama 3 models, for example, have about a hundred and twenty-eight thousand. A rough rule for English: a hundred tokens is about seventy-five words.

Other languages often need more tokens to say the same thing. A 2023 study found that the same text can take up to fifteen times as many tokens in one language as in another. More tokens means slower answers, higher prices on paid services, and less text fitting in at once.

Tokens also explain a famous mistake. Ask how many times the letter R appears in "strawberry", and for a long time many chatbots said two. The model doesn't see letters; it sees a couple of tokens, something like "straw" and "berry". It's being asked about letters it never directly sees.

## 2:07 · Predict, pick, repeat

Now the heart of it. You give the model a row of tokens. It gives back one thing: for every token in its vocabulary, how likely that token is to come next. After "The capital of France is", the token "Paris" gets almost all of the probability. Most tokens get almost none.

Then the program picks one token, adds it to the end, and feeds the whole row back in. Predict, pick, repeat. One token at a time, until the answer is finished. When you watch a chatbot's reply appear piece by piece, that is literally what you're seeing.

The pick isn't always the single most likely token. Usually it's drawn from the top few, which is why the same question can get a different answer each time. Lesson ten shows the setting that controls this. And when a chatbot "thinks" before it answers, that thinking is more tokens, produced the same way.

## 3:03 · Why it works

"Just predicting the next word" sounds like a party trick. Here's why it isn't. To predict text well, you need whatever helps you predict it. "She blank to the shop yesterday." That takes grammar. "The Eiffel Tower is in blank." That takes facts. "Twelve plus seven equals blank." That takes arithmetic. "Bonjour, in English, is blank." That takes translation.

Now imagine the last page of a detective novel. "And the murderer is blank." To guess that name, you'd have to follow the whole plot.

Nobody programmed grammar or facts into these models. They picked them up as a side effect of getting better at one simple game. But notice what they learned: what text tends to say. That's usually, but not always, what's true.

## 3:51 · Training and running

A model's life has two very different phases. The first is training. The model starts as random numbers. It's shown a stretch of text with the next token hidden, makes a guess, and is told the right answer. Every number that pushed it towards the wrong guess is nudged a tiny bit. Then the next stretch of text, and the next, trillions of times. Meta says its Llama 3 models were trained on more than fifteen trillion tokens. That takes weeks or months, on thousands of graphics chips running day and night.

What comes out is called a base model. It continues text, nothing more. Ask it a question and it might answer with more questions, like a page from a quiz book. So there's a second stage. The model is trained further on examples of helpful conversations, and on people's ratings of its answers. That's what turns a text-continuer into an assistant.

The second phase is running the model, also called inference. Training is over, and the numbers are frozen. Your message goes in, tokens come out. The model does not learn from your conversation; its numbers don't change while you chat. Whether a company keeps your chats to train its next model is a separate question, and lesson four covers it.

So how does a chatbot remember what you said three messages ago? It doesn't. The app sends the whole conversation back in, every single time. The amount of text a model can take in at once is called its context window. In a very long chat, the oldest parts may no longer fit. And when an app says it remembers you, it's saving notes and adding them to the text it sends in.

## 5:32 · Why it makes things up

Now lesson one's warning makes sense. A language model produces likely next tokens. There's no built-in step that checks whether they're true. When an answer appeared in its training text many times, likely and true usually line up. When it didn't, the model still produces the most likely-sounding text. A name that sounds like a name. A date that looks like a date. A source that looks like a source.

In 2023, two lawyers in New York filed a brief that cited six court cases. ChatGPT had supplied them. None of the six existed. The judge fined the lawyers and their firm five thousand dollars. The fake cases looked real: names, quotes, citations.

A 2025 paper from OpenAI adds another reason. The way models are trained and tested often rewards guessing. Think of a multiple-choice exam where a blank answer scores zero. Guessing sometimes scores, so a model that bluffs looks better than one that says "I don't know".

So the rule from lesson one gets sharper. The more specific, rare or recent a fact is, the more you should check it. Names, numbers, dates, quotes and links most of all. It helps to give the model the text you're asking about, instead of relying on its memory. And if it gives you a source, open it.

## 6:54 · Your task

Let's put it together. Text becomes tokens, and tokens become numbers. The model predicts the next token, one at a time. Training sets its numbers, once, at enormous cost. Running uses those numbers, and they don't change while you chat. And because it predicts what's likely, not what's true, it can be fluent and wrong.

Your task for this lesson. Find a question that a chatbot answered confidently and wrongly. Post it in BUILD: the question, the answer, and how you found out it was wrong. Any chatbot is fine, and leave out anything personal. If you're stuck, ask for a source on something specific, and check whether it exists.

Next time: what a model actually is. A file full of numbers, and why making one costs millions, while running one on your own computer costs little more than electricity. See you in lesson three.
