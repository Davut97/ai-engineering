# LLM basics

## Concepts

Write each one in 1 to 3 sentences, in your own words, while watching Karpathy's
"Intro to Large Language Models". If you can't explain it simply, rewatch that part.

- **Token:**
is smallest unit of data which the AI models reads it can be a work or a chunk of a word.
- **Context window:**
The max number of tokens the model can see at once (input + output). Its working memory for one request, measured in tokens 
- **Parameters (weights):**
Numbers learned in training (like w and b in the rent example) that turn input tokens into a prediction of the next token. 70B = 70 billion of them
- **Pre-training vs fine-tuning:**
pre training is where the nural network is trained on a large set of data on clustres of gpus this proccess usally takes around 12 days. fine tuning is the proccess of tunning the ai model to answer is a sepcifc way on a smaller set of examples
- **Inference:**
the live phase where a trained AI model applies its learned knowledge to new, unseen data to generate an output, prediction, or decision.
- **Temperature:**
It controls how random, predictable, or creative the AI’s responses will be when it generates text
- **System prompt:**
the developers instruction for the whole conversation what to say what to not say, the tone the format, the user can not see the system prompt the model weighs it above user messages
- **Hallucination, and why it happens:**
hallucination is where ai models presents something fake while presenting it in a very confidence way, it happens because the ai models are statistical prediction engines.

## Experiments

### 2026-10-13: Ollama, llama3.2, "Explain what a token is in one sentence."

| Run | Messages sent | Input tokens | Output tokens | Generation time | Answer |
|---|---|---|---|---|---|
| 1 | user message only | 35 | 38 | 0.30 s | Wrong meaning: described an auth/crypto token |
| 2 | + system: "You are a tutor teaching how large language models work." | 46 | 52 | 0.41 s | Right topic, still vague: said "word or character" instead of sub-word pieces |

What I learned (my words):

- each message has two keys role and content for the roles we have 3 options
1. system: which is the system prompt for the whole app (e.g don't answer legal questions)
2. user: what the user typed
3. assistant: the model's earlier replies which we needs to resend because the api has no memory.



## Try next

- Same question with `"options": {"temperature": 0}` three times, then `"temperature": 1` three times. Do the answers change?
- Same question to a frontier model (Claude, GPT or Gemini). Compare quality, speed and token counts.

## Questions I still have

-
