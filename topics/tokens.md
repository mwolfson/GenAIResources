- [Tokens](#tokens)
  - [Token](#token)
  - [Tokenization](#tokenization)
    - [Details about Tokenizer Algorithms](#details-about-tokenizer-algorithms)
    - [Tokenization Example](#tokenization-example)
    - [How to Count Tokens](#how-to-count-tokens)
      - [Estimate](#estimate)
      - [Tokenizer Tool (website)](#tokenizer-tool-website)
      - [tiktoken library for Python](#tiktoken-library-for-python)
      - [gpt-3 encoder library for Javascript](#gpt-3-encoder-library-for-javascript)
  - [Why is Tokenization needed?](#why-is-tokenization-needed)
    - [Maximum Token limit](#maximum-token-limit)
      - [Token Limits of Popular LLMs](#token-limits-of-popular-llms)
      - [API Charges Per Token](#api-charges-per-token)

# Tokens

LLMs don't comprehend raw text as language. Instead words are encoded into numerical representations (tokens). These tokens are fed into the model for processing. 

LLMs work by breaking a query into smaller components and then using statistical models to predict the most likely response based on the patterns that it learned during training.

Think of LLMs as a [**calculator for words**](https://simonwillison.net/2023/Apr/2/calculator-for-words/) (the flaw in this thinking, is that calculators are repeatable, and LLMs will give you a different response every time).

## Token

A token is a single word, character or subword unit, which are common sequences found in text. 

## Tokenization

This is the process of reducing the complexity of text, by converting it into individual words, subwords, or punctuation that the model can use for processing.  

Tokenization is performed using algorithms like **[Byte Pair Encoding (BPE)](https://en.wikipedia.org/wiki/Byte_pair_encoding)**, **[SentencePiece](https://towardsdatascience.com/sentencepiece-tokenizer-demystified-d0a3aac19b15)**, **[Unigram LM](https://medium.com/mti-technology/n-gram-language-model-b7c2fc322799)**, or **[WordPiece](https://huggingface.co/learn/nlp-course/chapter6/6?fw=pt)**. These algorithms split text into small units, and understands frequent and rare words, which helps limit the model’s vocabulary size but still enables the ability to represent any text sequence.

Once the words have been broken down into tokens, the tokens are converted into specific IDs that match the vocabulary model of the LLM.

### Details about Tokenizer Algorithms

Hugging Face has a great [overview](https://huggingface.co/docs/transformers/tokenizer_summary) explaining the difference between the various algorithms, and how they work.

### Tokenization Example

Example of using the HuggingFace Transformers library and the GPT-3.5 model:

```python
from transformers import AutoTokenizer

# Load the tokenizer for the GPT-3.5 model
tokenizer = AutoTokenizer.from_pretrained("gpt-3.5-turbo")

# Define the prompt
prompt = "Translate the following English text to French: 'Hello, how are you?'"

# Tokenize the prompt
tokenized_prompt = tokenizer(prompt, return_tensors="pt")

# Print the tokenized input
print(tokenized_prompt)
```

This will break this sentence down into the following tokens.

![tokenizer1](../assets/tokenizer1.png)

Then the text snippets can be converted to TokenIDs that correspond to an ID in the model's vocabulary.

**input_ids** - represents the tokenized version of the prompt, where each number corresponds to a token ID in the model's vocabulary.

**attention_mask** indicates which tokens should be attended to (1) and which should be ignored (0). (none are ignored in this example)

Output:
```python
{
 'input_ids': tensor([[8291, 17660, 262, 1708, 3594, 2420, 284, 4141, 25, 705, 15496, 11, 703, 389, 345, 30]]),
 'attention_mask': tensor([[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]])
}
```

These tokens are then converted to the following Vocabulary tokens corresponding to ChatGPT3.5.

![tokenizer2](../assets/tokenizer2.png)

### How to Count Tokens

#### Estimate

You can approximate how many tokens are in your prompt, but using this formula to give you an estimation:


> A helpful rule of thumb is that one token generally corresponds to ~4 characters of text for common English text. This translates to roughly ¾ of a word (so 100 tokens ~= 75 words).

#### Tokenizer Tool (website)

OpenAI Tokenizer - useful [token visualizer](https://platform.openai.com/tokenizer) tool to help understand how sentences are broken down into tokens.

#### tiktoken library for Python

[OpenAI tiktoken Library](https://github.com/openai/tiktoken/blob/main/README.md) - tool that uses the BPE tokenizer to give you a token count

Install:
```python
pip install tiktoken
```

Run encoding:
```python
import tiktoken

encoding = tiktoken.get_encoding("cl100k_base") // specifies with encoding to use
// -or- 
// encoding = tiktoken.encoding_for_model("gpt-3.5-turbo") // choose encoding for a specific model
encoding.encode("A string that will be encoded")  // encode the string will return a list of tokens
```
[32, 4731, 326, 481, 307, 30240]

Define method to count tokens:
```python
def tokens_from_string(string_to_count: str, encoding_name: str) -> int:
  """Returns the number of tokens in a string, for a specific encoding"""
  encoding = tiktoken.get_encoding(encoding_name)
  num_tokens = len(encoding.encode(string_to_count))
  return num_tokens
```

Use Method to count tokens
```python
tokens_from_string("tiktoken is great!", "cl100k_base")
```
6

#### gpt-3 encoder library for Javascript

If you are not using Python, there is different library that can be used for Javascript named [GPT-3-Encoder](https://www.npmjs.com/package/gpt-3-encoder).

Install:
```javascript
npm install gpt-3-encoder
```

Run:
```javascript
const {encode, decode} = require('gpt-3-encoder')

const str = 'This is an example sentence to try encoding out on!'
const encoded = encode(str)
console.log('Encoded this string looks like: ', encoded)

console.log('We can look at each token and what it represents')
for(let token of encoded){
  console.log({token, string: decode([token])})
}

const decoded = decode(encoded)
console.log('We can decode it back into:\n', decoded)
```

## Why is Tokenization needed?

Breaking text into tokens makes it more computationally efficient to handle and analyze, especially when dealing with large amounts of data.

### Maximum Token limit

LLMs have a limit to the amount of tokens allowed in each prompt. This is to restrict the number of tokens processed in a single interaction, which ensures efficient performance. 

Tokens might have different sizes depending on the vocabulary of the model. Certain characters of symbols might be treated as seperated tokens, and adding tokens representing beginning or ending of text can impact the count. Whitespace is not ignored, and will increase the count.

This is important when dealing with limited token budgets (when using LLMs that calculate usage based on token usage. When text needs to be truncated or shortened, important context might be lost.

#### Token Limits of Popular LLMs

| Language Model          | Token Limit |
| ----------------------- | ----------- |
| Bard                    | 8196        |
| ChatGPT (GPT-3.5-Turbo) | 4096        |
| ChatGPT (GPT-4)         | 8192        |
| ChatGPT (GPT-4-32k)     | 32,768      |
| Llama                   | 2048/4096   |
| StableLM-Alpha          | 4096        |
| T5                      | 512         |
| OpenLLaMA               | 2048        |
| MPT-7B                  | 84k         |
| Claude                  | 100k        |

#### API Charges Per Token 

Many LLM Products (including OpenAI) charge per token, for API Access. There is a cost for both input and output values. This can result in very expensive usage charges if token size is not limited.

| Language Model                        | Input Cost              | Output Cost |
| ------------------------------------- | -------------------- | ------------------ |
| Bard (PaLM2 Text )                    | $0.0010 / 1K tokens  | $0.0010 / 1K tokens|
| Bard (PaLM2 Chat )                    | $0.0005 / 1K tokens  | $0.0005 / 1K tokens|
| Claud2                                | $0.0005 / 1K tokens  | $0.0046 / 1K tokens|
| ChatGPT (GPT-3.5-Turbo) - 4k Context  | $0.0015 / 1K tokens  | $0.002 / 1K tokens |
| ChatGPT (GPT-3.5-Turbo) - 16k Context | $0.003 / 1K tokens   | $0.004 / 1K tokens |
| ChatGPT (GPT-4) - 8k Context          | $0.03 / 1K tokens    | $0.06 / 1K tokens  |
| ChatGPT (GPT-4) - 32k Context         | $0.06 / 1K tokens    | $0.012 / 1K tokens |

More details: [OpenAI Pricing](https://openai.com/pricing), [Bard & VertexAI Pricing](https://cloud.google.com/vertex-ai/pricing#generative_ai_models)