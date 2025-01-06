Title: Thoughts on AI
Date: 2025-01-06 11:22
Category: AI, Thoughts and Ramblings
Tags: Thoughts
Summary My thoughts on AI in the software industry as of January 2025
Authors: Justin Walters
Lang: en
Status: draft

I've been messing around with various AI and ML tools for the past year or so. I'm sure anyone who works as a software engineer can attest that pretty much every company in existence wants to stick some sort of AI powered feature into their product these days. It seems to be a bit of a bubble if I'm honest. A new shiny toy has been revealed and if your comapny isn't playing with it, investors don't want anything to do with you.

Is this a good thing? Is it a bad thing? I'm not sure either way. If I can say anything, I can say I expected this as soon as I started seeing the hyp around Chat-GPT for the first time.

One thing I can say is that I see a lot of companies that try to insert AI into their product I believe it actually makes their product worse. An example would be, replacing a wiki or documentation page with a poorly implemented AI chatbot; likely just some javascript pasted in from a third party service. Another glaring example would be AI generated content. Almost any google search these days will net you at least a full page of LLM generated slop articles that exist simply to satisfy search algorithms and drive traffic. At this juncture it appears to me that AI is making the user experience of the web much worse. Information is getting more difficult to find, and when you do find it, it's more difficult than ever to be sure of how accurate it is.

At the end of the day, LLMs are really just prediuctive text machines; they don't really have any sort of reasoning or logic capabilities unless you set them up to use things like RAG and chain of thought processing. Even then, your mileage may vary. The quality of an LLM's output is only as good as the quality of its training set and the quality of its reasoning chain.

Last year I built out a prototype RAG and chain of thought process for providing users with suggestions on how to improve native ad performance. Since this was a PoC I just hooked it up to use GPT-4o via the OpenAI API. I was able to create a vector DB with embeddings generated from various internal best practice documents, campaign retrospectives, and content dumps. I fed this through a coupe of "agents". Each agent was responsible for one step of the process. the first agent was responsible for using an internal API to retrieve performance data for the ad in question. the next agent was responsible for categorizing the ad and getting performance data for the ad's category and verticl. The next agent used the ad content and categorization data to query the vector db for relevant documents. All of this data was then fed into anoter agent which provided suggestions for improving ad performance based on all of the previous f=gathered data. The last step was an agent that would essentially act as an "editor" to condense and simplify the suggestions and data for presentation to a user.

This little R&D project was actually pretty promising and will likely get productized at some point. The reason I bring this project up is so I can talk about the pitfalls of LLM usage and possibly how to avoid them. 

One thing that I noticed right off the bat is the need for supervision and explicit instructions on every step. Now, this one seems obvious, but it's a little more nuanced than one might think.
