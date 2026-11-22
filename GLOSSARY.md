# Glossary

Every word the course uses, in plain English, with the lesson that explains it. It grows with each lesson.

| Word | Meaning | Lesson |
|---|---|---|
| **AI winter** | A period when funding and interest in AI research dried up because the promises had not been met. There were two: in the 1970s and in the late 1980s. | [01](01-introduction/) |
| **Artificial intelligence (AI)** | The whole field: getting machines to do things that would need intelligence if a person did them. | [01](01-introduction/) |
| **Base model** | A model straight out of training. It only continues text; ask it a question and it may reply with more questions. | [02](02-how-a-language-model-works/) |
| **Chatbot** | An app you talk to in text. The chatbots most people know are language models wrapped in an app. | [01](01-introduction/) |
| **Context window** | The amount of text a model can take in at once, counted in tokens. In a very long chat the oldest parts may no longer fit. | [02](02-how-a-language-model-works/) |
| **Deep learning** | Machine learning done with neural networks that have many layers. "Deep" just means many layers. | [01](01-introduction/) |
| **ELIZA effect** | Our habit of reading a mind into anything that talks back fluently. Named after ELIZA, a 1966 program that understood nothing. | [01](01-introduction/) |
| **Fine-tuning** | Training a model further on a smaller, chosen set of examples, such as helpful conversations and people's ratings of answers. It turns a base model into an assistant. | [02](02-how-a-language-model-works/) |
| **Generative AI** | Models that create something new: text, images, sound or video. | [01](01-introduction/) |
| **Graphics card (GPU)** | A chip first built for video games. It turned out to be very good at the maths neural networks need. Lesson 05 explains why it matters for running models. | [01](01-introduction/) |
| **Hallucination** | When a model invents facts, sources or quotes and presents them as real. | [01](01-introduction/) · [02](02-how-a-language-model-works/) |
| **Inference** | Running a trained model: text goes in, tokens come out. Its numbers don't change while it runs. | [02](02-how-a-language-model-works/) |
| **Language model** | A neural network trained on enormous amounts of text to do one thing: predict what comes next. | [01](01-introduction/) |
| **Layer** | One stage of a neural network. Each layer takes numbers in and passes new numbers on to the next. | [01](01-introduction/) |
| **Machine learning** | Learning patterns from examples instead of following rules written by hand. | [01](01-introduction/) |
| **Neural network** | Long chains of simple maths, stacked in layers. Training adjusts the numbers inside it until its answers get better. | [01](01-introduction/) |
| **Next-token prediction** | The one job of a language model: given a row of tokens, say how likely each possible next token is. Answers are written by predicting, picking and repeating. | [02](02-how-a-language-model-works/) |
| **Open-weight model** | A model whose weights anyone can download and run on their own computer. Lesson 04 explains how this differs from "open source". | [01](01-introduction/) |
| **Terminal** | A window where you type commands instead of clicking. Lesson 08 shows that it is not scary. | [01](01-introduction/) |
| **Token** | A piece of text a model works with: a whole word, part of a word, or a single character. Text is cut into tokens before the model sees it. | [02](02-how-a-language-model-works/) |
| **Token ID** | The number that stands for a token. The model only ever sees these numbers. | [02](02-how-a-language-model-works/) |
| **Tokenizer** | A model's own way of cutting text into tokens. Different models split the same text differently. | [02](02-how-a-language-model-works/) |
| **Training** | Showing a model huge numbers of examples and nudging its numbers, a tiny bit at a time, until its answers get better. | [01](01-introduction/) |
| **Training cut-off** | The date after which a model knows nothing, unless it is connected to a search tool. | [01](01-introduction/) |
| **Transformer** | A design for neural networks, published in 2017, that handles language far better and can be trained at enormous scale. The "T" in GPT. | [01](01-introduction/) |
| **Vocabulary** | The full list of tokens a model knows. Meta's Llama 3 models have about 128,000. | [02](02-how-a-language-model-works/) |
| **Weights** | The numbers inside a neural network that training adjusts. A model is mostly a large file of weights. Lesson 03 explains them. | [01](01-introduction/) |
