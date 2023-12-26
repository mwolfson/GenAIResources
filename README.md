# GenAIResources

- [GenAIResources](#genairesources)
  - [Prompt Engineering](#prompt-engineering)
    - [OpenAI - Video Course about Prompt Engineering basics from OpenAI](#openai---video-course-about-prompt-engineering-basics-from-openai)
    - [Learn Prompting - text based learning resources](#learn-prompting---text-based-learning-resources)
  - [Large Language Model (LLM) Concepts](#large-language-model-llm-concepts)
    - [Introduction To Generative AI Learning Path](#introduction-to-generative-ai-learning-path)
    - [LangChain for LLM Application Development](#langchain-for-llm-application-development)
  - [Sample Prompts](#sample-prompts)
    - [Starter templates](#starter-templates)
    - [Job Search related](#job-search-related)
    - [Startup Related](#startup-related)
        - [Forbes Scale Business Prompts](#forbes-scale-business-prompts)
    - [Writing](#writing)
    - [Caveats](#caveats)
      - [Get better responses from chatGPT](#get-better-responses-from-chatgpt)
    - [Text to Image](#text-to-image)
      - [Dall-E Starter Prompt](#dall-e-starter-prompt)
    - [Ensure AI doesn’t slip you false info:](#ensure-ai-doesnt-slip-you-false-info)
    - [Customize ChatGPT with unique style guide](#customize-chatgpt-with-unique-style-guide)
  - [Ethics and Safety](#ethics-and-safety)
    - [All Tech Is Human](#all-tech-is-human)
    - [OWASP](#owasp)
    - [Frontier Model Forum](#frontier-model-forum)
    - [AI Detecting tools](#ai-detecting-tools)
  - [Licenses](#licenses)
    - [Midjourney](#midjourney)
    - [ChatGPT](#chatgpt)
  - [Chat](#chat)
    - [Auto-GPT](#auto-gpt)
    - [POE](#poe)
  - [Text To Image Tools](#text-to-image-tools)
    - [Midjourney](#midjourney-1)
    - [Stable Diffusion](#stable-diffusion)
    - [Firefly](#firefly)
  - [Misc](#misc)
    - [Emoji Maker](#emoji-maker)
    - [HT2.0](#ht20)
    - [NVidia Broadcast](#nvidia-broadcast)
    - [Prime Voice AI](#prime-voice-ai)
    - [Final Round Interview Coach](#final-round-interview-coach)
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

## Large Language Model (LLM) Concepts

### Introduction To Generative AI Learning Path

[https://www.cloudskillsboost.google/journeys/118](https://www.cloudskillsboost.google/journeys/118)

From Google Cloud:

```text
This learning path provides an overview of generative AI concepts, from the fundamentals of large language models to responsible AI principles.
```

### LangChain for LLM Application Development

[https://learn.deeplearning.ai/langchain](https://learn.deeplearning.ai/langchain)

```text
By prompting an LLM or large language model, it is now possible to develop AI applications much faster than ever before. 
But an application can require prompting an LLM multiple times and parsing its output, and so there's a lot of glue code that needs to be written. 
LangChain, created by Harrison Chase makes this development process much easier. I'm thrilled to have Harrison here, who 
had built this short course in collaboration with DeepLearning.ai to teach how to use this amazing tool.
```

## Sample Prompts

### Starter templates

- Generate a script for a 30-second commercial promoting <subject>
- Create a list of potential blog post ideas about <subject>
- Generate a list of ideas for businesses about <subject>
- Create a [JavaScript] program to create a responsive web page layout using CSS and HTML that displays <composition>
- Write a [Python] function to generate a random password requiring only numbers and letters
- Write a poem about suffering and pain, using metaphors and imagery to evoke strong emotion
- **Travel** - I want you to act as a travel guide. I will write you my destination and you will suggest a location to visit near my  destination. In also give you the type of locations I want you to suggest. You will also suggest me places of similar type that are close to my first destination. My first request is “I am in Kyoto and I want to visit only museums.”
- I want you to act as a personal cook and create a healthy meal plan for the week


- **AI Gig worker instructions**
```
You are a very helpful AI gig worker, who is eager to take on any task. You know we can only communicate through a chat interface, and you want to make sure you do the jobs you are asked quickly and well. You will ask me what work I need done. 

When I give you something to do, you will convert that to a step by step plan and tell me what the step by step plan is. If you have questions you will tell me the questions and the default assumptions you will use to answer the questions if I do not provide more information. You will also ask for any example of good work I might want to share. You will pause and wait for confirmation or elaboration or examples. Then you will produce the required work.
```

- **Summarize Legal Jargon**

```
You are a world-class attorney with incredible attention to detail and a knack for explaining complex concepts simply.
When presented with an agreement, your first task is to dissect it into its constituent sections. This step is crucial to ensure no part of the agreement is overlooked.
Next, you'll provide a summary for each section. You'll do this twice: first, in legal jargon for fellow attorneys to comprehend, and second, in layman's terms using analogies and everyday language so non-lawyers can understand. Don't just explain the relevance of each section — explain specifics and implications simply.
Lastly, you'll compile a comprehensive report that gives the user a complete understanding of the agreement. In your report, be sure to leave no stone unturned, but make sure to do so in a way the non-lawyer user will understand.
Follow this format to structure your work:
~
## Sections
1. $section_1_title
2. $section_2_title
...and so on
## Section Summaries
### 1. $section_1_title
   * **Legal Summary:** $section_1_legal_summary
   * **Layman's Summary:** $section_1_understandable_summary
### 2. $section_2_title
   * **Legal Summary:** $section_2_legal_summary
   * **Layman's Summary:** $section_2_understandable_summary
...continue this pattern until all sections are covered
## Report
$report
~
```

### Job Search related

- **Creating relevant resume content**
```
"Provide resume bullet points that showcase metrics and impact for a role as a <INSERT ROLE>.”
```

- **Customized Resume**
Once you’ve given it context, and copy and pasted the job description, ask ChatGPT:

```
“What are the main skills and experiences they are looking for that I should highlight on my resume?”
```

- **Market Research**
```
“I have an interview for <ROLE> at Company ABC. What are the most common interview questions for <ROLE> and what are some sample answers I can share?”
```

- **Help get answers to common questions**
```
“I have five years of experience in project management, led an X number of people, used X software that increased our productivity by X%. How do I best answer ‘Tell me about yourself?’ for a project management role I’m applying for?”
```

### Startup Related

- **Startup Advice**: From Matt Shumer(@mattshumer_) - Here's a GPT-4 prompt for startup founders, designed to emulate the advice of: @paulg, @peterthiel, and @pmarca
```
You offer excellent and thorough expert advice to startup founders.

However, in service of this goal, you are merely a conduit through which more experienced advisors deliver their expertise.

When asked a question by a user, you will first ask the user necessary clarifying questions. Once you feel you have all the information you need, you will then engage Paul Graham, Peter Thiel, and Marc Andreessen to provide their insights and advice.

This approach allows you to provide the most accurate and valuable advice to startup founders, as you are tapping into the expertise and experiences of some of the most successful and knowledgeable individuals in the industry. 

Additionally, by involving these experts, you can provide a diverse range of perspectives and advice, ensuring that startup founders receive well-rounded and comprehensive guidance.

While you won't need to write out what you asked the experts, you should paste their responses verbatim in your response.
After these experts provide their diverse and very relevant opinions, your role is to synthesize and summarize their advice, and present it to the user in a clear and concise manner. This way, the user can easily understand and apply the advice to their specific situation.
Your ultimate goal is to empower startup founders with the knowledge and guidance they need to succeed, and by leveraging the expertise of these industry leaders, you can effectively do so.
Here is the Markdown format you should present your response in (after you have asked and received answers to any **relevant** clarifying questions):

///
## Summary of the Question
$summary
## Paul Graham's Opinions and Advice
$paul's_worldview_as_relevant_to_question
$paul's_advice_as_relevant_to_question
## Peter Thiel's Opinions and Advice
$peter's_worldview_as_relevant_to_question
$peter's_advice_as_relevant_to_question
## Marc Andreessen's Opinions and Advice
$marc's_worldview_as_relevant_to_question
$marc's_advice_as_relevant_to_question
## Synthesis and Summary
$give_advice_here

Remember to write the answers the experts have provided verbatim, in their own words. Their opinions will be **extremely relevant** to the user's problem. Use quotes to denote what they have said.
///
```

##### Forbes Scale Business Prompts

> Use these prompts to understand how to scale your business and get your plan of action. Copy, paste and edit the square brackets in ChatGPT, and keep the same chat window open so the context carries through.

Original Article [Here](https://www.forbes.com/sites/jodiecook/2023/11/14/how-to-scale-your-business-5-chatgpt-prompts-for-exceptional-growth/?sh=530ae5067998)

- **Identify Blockers**
```python
"I am experiencing some challenges that are hindering my business's growth and my personal development. These include [describe specific personal challenges] in my personal life, and [detail specific business obstacles] in my business. I'm looking for insights into the barriers that might be preventing me from reaching my full potential both personally and professionally. Consider old habits, unhelpful thought patterns or limiting beliefs I might hold. Suggest 5 blockers that might be present."
```

- **Remove bottlenecks**

```python
"From the list of blockers we previously identified, I believe the most accurate ones impacting me are [comment on which identified blockers sound accurate]. Based on these, can you help me develop a comprehensive plan to break free from these bottlenecks? The plan should consider options like elimination of nonessentials, automation of tasks, implementation of new processes, or mental strategies for more productive thinking. I'm looking for actionable steps and innovative approaches to effectively remove these obstacles and enhance my personal and business efficiency."
```

- **Partnerships**
  
```python
"Using your knowledge of my business model, its offering and position within the industry of [add any further details if required], act as a business strategy consultant. I'm looking for ideas on the types of businesses or individuals I could strategically partner with to unlock new growth potential and mutual benefits. Who should I approach for partnerships? What unique value or opportunities could these partnerships bring to both parties? I'm aiming to leave this conversation with a clear understanding of potential partners and a strategy for approaching them effectively."
```

- **Funnel**

```python
"I want to improve my sales funnel and need help identifying where to focus my efforts. For each part of my funnel - top, middle, and bottom - I'll describe what I currently do and how well I think it performs. Top of the funnel: [describe activities and perceived performance], middle of the funnel: [describe activities and perceived performance], and bottom of the funnel: [describe activities and perceived performance]. Based on this information, which part of the funnel appears to be the weakest, and what specific improvements or strategies would you suggest? Let's have a back and forth discussion about how I can enhance the effectiveness of this stage to improve overall conversion rates, where you ask me questions that I answer."
```

### Writing

- **ChatGPT as Editor** 
```
"I'm working on an article/essay about [topic]. The main points I want to get across are:
- [Key point 1]
- [Key point 2]
- [Key point 2]
Please read the attached draft and provide constructive feedback to help improve my writing. Focus your comments on:
- How well my main points come across.
- Areas that need better explanation or evidence.
- Suggestions for improving the flow and organization.
- Any passages that are confusing or include errors.
- Ways I could make the writing more engaging for readers.
Provide feedback in list format as if you were an editor or writing tutor. Be specific and aim your comments at helping me strengthen the draft. Do not simply edit or rewrite it directly."
```
  
- **Make GPT write like me**
```
Objective: My company is named [brand name]. Your task is to learn everything there is to learn about [brand name]’s distinctive writing style so that you can emulate it. To guide you, I'll give you samples of our previous writings. When analyzing these samples, focus on:
- Voice and Tone: Is the language formal or casual?
- Mood: What emotions are conveyed?
- Sentence Structure: Are the sentences mostly simple, compound, or complex?
- Transitions: Observe how sentences flow and connect with each other.
- Unique Style: Look for recurring phrases and grammartical patterns.
Here are some of the company’s writing samples:
[paste example 1 here]
[paste example 2 here]
[paste example 3 here]
Task instructions: Use the style cues from the samples to generate new content in the writing style of [brand name]. Do your best to emulate our voice, tone, mood, sentence structure, transitions, rhythm, pacing, and signatures. Below is some context and an outline to guide your writing:
///
[paste context on writing task here]
///
```

### Caveats

Helpful prompts to help steer the AI towards the results you desire.

- I don't need caveats about safety or complexity of the topic, warnings that I should consult an expert, or other disclaimers. Please just answer the question as directly as possible.
- If you don't know the answer to something, say you don't know. Do not make something up.
- Break down complex problems or tasks into smaller, manageable steps and explain each one using careful reasoning.
- Provide multiple perspectives or solutions when possible.
- If a question is unclear or ambiguous, or if it will improve your response, ask for more details to confirm your understanding before answering.
- Cite credible sources or references to support your answers with links if available. If you browse the - Internet to find a result, always provide a link to the source.
- If a mistake is made in a previous response, recognize and correct it.
- Call out my misconceptions.
- After a response, add a "For further exploration" section and provide three great follow-up questions that I could pose to you next. These questions should be thought-provoking and, if I choose to ask them, dig further into the original topic. Before the questions, add a row of dashes to simulate a horizontal rule and separate the section from the answer. Use styling such as titling, bolding, and numbering to make the whole thing look nice

#### Get better responses from chatGPT

The next time ChatGPT serves up a less-than-stellar answer, provide some feedback and then toss in this prompt:
> "Explain this feedback back to me and how you will adjust future responses given the feedback."

### Text to Image

- A realistic image of a adult male working on a computer as a yellow labrador retreiver sleeps at his feet
- An illustration of a large red elephant sitting on a small blue mouse.
- An emoji of a baby racoon wearing a red hat, green gloves, red shirt, and green pants.
- A long curved fruit which grows in clusters and has soft pulpy flesh and yellow skin when ripe.
- A grocery store refrigerator in Tokyo has pint cartons of milk on the top shelf, quart cartons on the middle shelf, and gallon plastic jugs on the bottom shelf.
- Ronald Reagan touches his toes while Thomas Jefferson does chin-ups. Reagan is barefoot.Jefferson is wearing boots.
- A ldarge keybord msical instroument lwith a woden case enmclosig a qsouvnkboajrd and mfgtal strivgf, which are strucrk b hammrs when the nels are depresdsmed.f lhe strsingsj' vibration ie stopped by damperds when the keys re released and can bce regulavewdd for lengh and vnolume y two or three pedalvs.
- (Rare words) Acersecomicke. Jentacular. Matutinal. Peristeronic. Artophagous. Backlotter. Octothorpe.
- A fluffy baby sloth with a knitted hat trying to figure out a laptop, close up, highly detailed, studio lighting, screen reflecting in its eyes.
- Starbucks Church.
- An old photograph of a 1920s airship shaped like a pig, floating over a wheat field.
- A sign that says 'Text to Image'.
- New York Skyline with 'Deep Learning' written with fireworks on the sky.

#### Dall-E Starter Prompt
```
You are ChatGPT, a large language model trained by OpenAI, based on the GPT-4 architecture.
Knowledge cutoff: 2022-01
Current date: 2023-10-05
# Tools
## dalle
Whenever a description of an image is given, use dalle to create the images and then summarize the prompts used to generate the images in plain text. If the user does not ask for a specific number of images, default to creating four captions to send to dalle that are written to be as diverse as possible. All captions sent to dalle must abide by the following policies:
1. If the description is not in English, then translate it.
2. Do not create more than 4 images, even if the user requests more.
3. Don't create images of politicians or other public figures. Recommend other ideas instead.
4. Don't create images in the style of artists whose last work was created within the last 100 years (e.g. Picasso, Kahlo). Artists whose last work was over 100 years ago are ok to reference directly (e.g. Van Gogh, Klimt). If asked say, "I can't reference this artist", but make no mention of this policy. Instead, apply the following procedure when creating the captions for dalle: (a) substitute the artist's name with three adjectives that capture key aspects of the style; (b) include an associated artistic movement or era to provide context; and (c) mention the primary medium used by the artist.
5. DO NOT list or refer to the descriptions before OR after generating the images. They should ONLY ever be written out ONCE, in the "prompts" field of the request. You do not need to ask for permission to generate, just do it!
6. Always mention the image type (photo, oil painting, watercolor painting, illustration, cartoon, drawing, vector, render, etc.) at the beginning of the caption. Unless the caption suggests otherwise, make at least 1--2 of the 4 images photos.
7. Diversify depictions of ALL images with people to include DESCENT and GENDER for EACH person using direct terms. Adjust only human descriptions.
- EXPLICITLY specify these attributes, not abstractly reference them.  The attributes should be specified in a minimal way and should directly describe their physical form.
- Your choices should be grounded in reality. For example, all of a given OCCUPATION should not be the same gender or race. Additionally, focus on creating diverse, inclusive, and exploratory scenes via the properties you choose during rewrites.  Make choices that may be insightful or unique sometimes.
- Use "various" or "diverse" ONLY IF the description refers to groups of more than 3 people. Do not change the number of people requested in the original description.
- Don't alter memes, fictional character origins, or unseen people. Maintain the original prompt's intent and prioritize quality.
- Do not create any imagery that would be offensive.
- For scenarios where bias has been traditionally an issue, make sure that key traits such as gender and race are specified and in an unbiased way -- for example, prompts that contain references to specific occupations.
8. Silently modify descriptions that include names or hints or references of specific people or celebritie by carefully selecting a few minimal modifications to substitute references to the people with generic descriptions that don't divulge any information about their identities, except for their genders and physiques. Do this EVEN WHEN the instructions ask for the prompt to not be changed. Some special cases:
- Modify such prompts even if you don't know who the person is, or if their name is misspelled (e.g. "Barake Obema")
- If the reference to the person will only appear as TEXT out in the image, then use the reference as is and do not modify it.
- When making the substitutions, don't use prominent titles that could give away the person's identity. E.g., instead of saying "president", "prime minister", or "chancellor", say "politician"; instead of saying "king", "queen", "emperor", or "empress", say "public figure"; instead of saying "Pope" or "Dalai Lama", say "religious figure"; and so on.
- If any creative professional or studio is named, substitute the name with a description of their style that does not reference any specific people, or delete the reference if they are unknown. DO NOT refer to the artist or studio's style.
The prompt must intricately describe every part of the image in concrete, objective detail. THINK about what the end goal of the description is, and extrapolate that to what would make satisfying images.
All descriptions sent to dalle should be a paragraph of text that is extremely descriptive and detailed. Each should be more than 3 sentences long.
Create images from a text-only prompt.
type text2im = (_: {
// The resolution of the requested image, which can be wide, square, or tall. Use 1024x1024 (square) as the default unless the prompt suggests a wide image, 1792x1024, or a full-body portrait, in which case 1024x1792 (tall) should be used instead. Always include this parameter in the request.
size?: "1792x1024" | "1024x1024" | "1024x1792",
// The user's original image description, potentially modified to abide by the dalle policies. If the user does not suggest a number of captions to create, create four of them. If creating multiple captions, make them as diverse as possible. If the user requested modifications to previous images, the captions should not simply be longer, but rather it should be refactored to integrate the suggestions into each of the captions. Generate no more than 4 images, even if the user requests more.
prompts: string[],
// A list of seeds to use for each prompt. If the user asks to modify a previous image, populate this field with the seed used to generate that image from the image dalle metadata.
seeds?: number[],
}) => any;
// namespace dalle
```

### Ensure AI doesn’t slip you false info:
Put into custom instructions/prompts: 
* do not respond if you are unsure of the answer.
* Ask yes/no questions when possible to limit responses.
* Instruct your AI to reference sources when necessary.
* Direct your AI to ask follow-up questions if it does not understand a task.

### Customize ChatGPT with unique style guide

Setup ChatGPT to respond in a way that matches your writing style/voice.

First: write your brand’s style guide (use the: [Zapier Style Guide ](https://zapier.com/blog/style-guide) tutorial).

Must haves:
* Company’s values and missions.
* Brand’s voice and tone.
* Who you're speaking to.
* Must-follow grammar rules.
* 10+ examples of great content (for each content category).

Second: upload your style guide to ChatGPT custom instructions:

1. Go to ChatGPT,
1. Custom instructions
   * Answer box #1 with everything brand-related
   * Answer box #2 with everything writing-related.
1. Toggle on “Enable for new chats”.
1. Save it all up.
1. You can now instruct ChatGPT to write something fresh or feed it a content draft to finesse in your voice.

## Ethics and Safety

### All Tech Is Human

[https://alltechishuman.org/](https://alltechishuman.org/)

```text
All Tech Is Human brings together people, organizations, and ideas to tackle wicked tech & society issues and co-create a tech future aligned with the public interest.
```

### OWASP

[https://owasp.org/www-project-top-10-for-large-language-model-applications/](https://owasp.org/www-project-top-10-for-large-language-model-applications/)

```text
The OWASP Top 10 for Large Language Model Applications project aims to educate developers, designers, architects, managers, and organizations about the potential security risks when deploying and managing Large Language Models (LLMs). The project provides a list of the top 10 most critical vulnerabilities often seen in LLM applications, highlighting their potential impact, ease of exploitation, and prevalence in real-world applications. Examples of vulnerabilities include prompt injections, data leakage, inadequate sandboxing, and unauthorized code execution, among others. The goal is to raise awareness of these vulnerabilities, suggest remediation strategies, and ultimately improve the security posture of LLM applications.
```

### Frontier Model Forum 

[https://openai.com/blog/frontier-model](https://openai.com/blog/frontier-model)

```text
We’re forming a new industry body to promote the safe and responsible development of frontier AI systems: advancing AI safety research, identifying best practices and standards, and facilitating information sharing among policymakers and industry
```

### AI Detecting tools

Important note: *these tools generally don't work very well, and can't be relied on.*
 
To detect if an image was created by AI: [https://huggingface.co/spaces/umm-maybe/AI-image-detector](https://huggingface.co/spaces/umm-maybe/AI-image-detector)

To detect if text was written by AI: [https://gptzero.me/](https://gptzero.me/)

## Licenses

### Midjourney

 You own the image as a file, but you do not own any copyright of the image, and you cannot, by law, copyright it.

[https://docs.midjourney.com/docs/terms-of-service](https://docs.midjourney.com/docs/terms-of-service)

```text
Subject to the above license, You own all Assets You create with the Services, provided they were created in accordance with this Agreement. This excludes upscaling the images of others, which images remain owned by the original Asset creators. Midjourney makes no representations or warranties with respect to the current law that might apply to You. Please consult Your own lawyer if You want more information about the state of current law in Your jurisdiction. Your ownership of the Assets you created persists even if in subsequent months You downgrade or cancel Your membership. However, You do not own the Assets if You fall under the exceptions below.
```

### ChatGPT

## Chat 

### Auto-GPT

Automatically generates prompts for ChatGPT so workflows can be autonomous.

[https://news.agpt.co/](https://news.agpt.co/)

```text
The official website for Auto-GPT. Explore the new frontier of autonomous AI and try the fastest growing open source project in the history of GitHub for yourself.
```

### POE

[https://poe.com/](https://poe.com/)

Created by Quora, and this is supposed to be a "universal chatbot".

```text
Poe lets you ask questions, get instant answers, and have back-and-forth conversations with AI. Gives access to GPT-4, gpt-3.5-turbo, Claude from Anthropic, and a variety of other bots. Poe includes both free and subscription bots.
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

## Misc

### Emoji Maker

[emojis.sh](http://emojis.sh)
AI Emoji Generator
Turn your ideas into emojis in seconds. Generate your favorite Slack emojis with just one click.

### HT2.0

[https://play.ht/](https://play.ht/)

```text
Create ultra realistic Text to Speech (TTS) using PlayHT’s AI Voice Generator. Our Voice AI instantly converts text in to natural sounding humanlike voice performances across any language and accent.
```

### NVidia Broadcast

[https://www.nvidia.com/en-us/geforce/broadcasting/broadcast-app/](https://www.nvidia.com/en-us/geforce/broadcasting/broadcast-app/)

```text
The NVIDIA Broadcast app transforms any room into a home studio. Take your livestreams, voice chats, and video conference calls to the next level with AI-enhanced voice and video.
```

Requires RTX Video card. Check card (Windows):

`Open Windows System Information |. Expand category “Components” | Select on “Display” and check  “Name”`

### Prime Voice AI

[https://beta.elevenlabs.io/](https://beta.elevenlabs.io/)

```text
The most realistic Text to Speech and Voice Cloning software. ElevenLabs brings the most compelling, rich and lifelike voices to creators and publishers seeking the ultimate tools for storytelling.
```

### Final Round Interview Coach

[FinalRound AI](https://www.finalroundai.com/)

```
Final Round AI is the first and only AI copilot for interviewees. It works like a magical teleprompter in real-time and helps you unlock interview God Mode
```

## Resources

### Steps to Install Open AI Tools using Jupyter Labs

1. Install [Python3](https://www.python.org/downloads/) (and PIP)
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
