# GenAIResources

- [GenAIResources](#genairesources)
  - [Prompt Engineering](#prompt-engineering)
    - [OpenAI - Video Course about Prompt Engineering basics from OpenAI](#openai---video-course-about-prompt-engineering-basics-from-openai)
    - [Learn Prompting - text based learning resources](#learn-prompting---text-based-learning-resources)
    - [Sample Prompts](#sample-prompts)
      - [Starter templates](#starter-templates)
      - [Text to Image](#text-to-image)
      - [Misc](#misc)
  - [Ethics and Safety](#ethics-and-safety)
    - [](#)
  - [Chat](#chat)
    - [Auto-GPT](#auto-gpt)
  - [Text To Image Tools](#text-to-image-tools)
    - [Midjourney](#midjourney)
    - [Stable Diffusion](#stable-diffusion)
    - [Firefly](#firefly)
  - [Resources](#resources)
    - [Steps to Install Open AI Tools using Jupyter Labs](#steps-to-install-open-ai-tools-using-jupyter-labs)
      - [Steps to first API call](#steps-to-first-api-call)
    - [Make Use Of](#make-use-of)

This is a collection of resources for working with Generative AI technologies.

## Prompt Engineering

### OpenAI - Video Course about Prompt Engineering basics from OpenAI

[https://learn.deeplearning.ai/](https://learn.deeplearning.ai/)

```text
In this course, we'll share with you some of the possibilities for what you can do, as well as best practices for how you can do them. 
There's a lot of material to cover. First, you'll learn some prompting best practices for software development, then we'll cover some common use cases, summarizing, inferring, transforming, expanding, and then you'll build a chatbot using an LLM. We hope that this will spark your imagination about new applications that you can build. 
```

### Learn Prompting - text based learning resources

[https://learnprompting.org/](https://learnprompting.org/)

```text
Your Guide to Communicating with Artificial Intelligence
Learn how to use ChatGPT and other AI tools to accomplish your goals using our free and open source curriculum, designed for all skill levels!
```

### Sample Prompts

#### Starter templates

- Generate a script for a 30-second commercial promoting <subject>
- Create a list of potential blog post ideas about <subject>
- Generate a list of ideas for businesses about <subject>
- Create a [JavaScript] program to create a responsive web page layout using CSS and HTML that displays <composition>
- Write a [Python] function to generate a random password requiring only numbers and letters
- Write a poem about suffering and pain, using metaphors and imagery to evoke strong emotion
- I want you to act as a travel guide. I will write you my destination and you will suggest a location to visit near my  destination. In also give you the type of locations I want you to suggest. You will also suggest me places of similar type that are close to my first destination. My first request is “I am in Kyoto and I want to visit only museums.”
- I want you to act as a personal cook and create a healthy meal plan for the week

#### Text to Image

#### Misc

## Ethics and Safety

### 

[https://owasp.org/www-project-top-10-for-large-language-model-applications/](https://owasp.org/www-project-top-10-for-large-language-model-applications/)

```text
The OWASP Top 10 for Large Language Model Applications project aims to educate developers, designers, architects, managers, and organizations about the potential security risks when deploying and managing Large Language Models (LLMs). The project provides a list of the top 10 most critical vulnerabilities often seen in LLM applications, highlighting their potential impact, ease of exploitation, and prevalence in real-world applications. Examples of vulnerabilities include prompt injections, data leakage, inadequate sandboxing, and unauthorized code execution, among others. The goal is to raise awareness of these vulnerabilities, suggest remediation strategies, and ultimately improve the security posture of LLM applications.
```

## Chat 

### Auto-GPT

[https://news.agpt.co/](https://news.agpt.co/)

```text
The official website for Auto-GPT. Explore the new frontier of autonomous AI and try the fastest growing open source project in the history of GitHub for yourself.
```

## Text To Image Tools

### Midjourney 

[https://www.midjourney.com/app/](https://www.midjourney.com/app/)

```text
Midjourney is an independent research lab exploring new mediums of thought and expanding the imaginative powers of the human species.
```

Requires monthy subscription and dischord account.

### Stable Diffusion

[https://stablediffusionweb.com/](https://stablediffusionweb.com/)

```text
Stable Diffusion is a latent text-to-image diffusion model capable of generating photo-realistic images given any text input, cultivates autonomous freedom to produce incredible imagery, empowers billions of people to create stunning art within seconds.
```

Free to try a prompt right on the webpage.

### Firefly

[https://firefly.adobe.com/](https://firefly.adobe.com/)

```text
Firefly is Adobe’s new generative AI service. As part of Creative Cloud, Firefly offers new ways to bring your ideas to life while improving creative workflows.
```

Requires Adobe Creative Cloud subscription, and signup for beta access.

## Resources

### Steps to Install Open AI Tools using Jupyter Labs

1. Install Python3 (and PIP)
1. Use PIP to install following pakages
   1. `pip install openai`
   1. `pip install jupyterlab`
   1. `pip install python-dotenv`
   1. `pip install panel`
   1. `pip install notebook==6.5.4`
2. Get API Key and setup an Environment variables
   1. export OPENAI_API_KEY="sk-dq...X"
3. Run `jupyter-lab`

#### Steps to first API call

These 3 steps are the basic steps to make an API call:

```python
import openai
import os

from dotenv import load_dotenv, find_dotenv
_ = load_dotenv(find_dotenv())

openai.api_key  = os.getenv('OPENAI_API_KEY')
```

```python
def get_completion(prompt, model="gpt-3.5-turbo"):
    messages = [{"role": "user", "content": prompt}]
    response = openai.ChatCompletion.create(
        model=model,
        messages=messages,
        temperature=0, # this is the degree of randomness of the model's output
    )
    return response.choices[0].message["content"]
```

```python
text = f"""
You should express what you want a model to do by \ 
providing instructions that are as clear and \ 
specific as you can possibly make them. \ 
This will guide the model towards the desired output, \ 
and reduce the chances of receiving irrelevant \ 
or incorrect responses. Don't confuse writing a \ 
clear prompt with writing a short prompt. \ 
In many cases, longer prompts provide more clarity \ 
and context for the model, which can lead to \ 
more detailed and relevant outputs.
"""
prompt = f"""
Summarize the text delimited by triple backticks \ 
into a single sentence.
```{text}```
"""
response = get_completion(prompt)
print(response)
```

### Make Use Of

[https://www.makeuseof.com/tag/chatgpt/](https://www.makeuseof.com/tag/chatgpt/)

```text
Learn the latest about ChatGPT and what you can do with this powerful AI chatbot.
```
