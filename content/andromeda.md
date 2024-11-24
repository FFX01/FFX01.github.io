Title: Andromeda
Summary: Experimental LLM-driven Web Scraper and Content Analyzer/Generator
Date: 2024-11-23 18:22
Authors: Justin Walters
Category: Projects
Tags: Nativo, Python, FastAPI, AI, LLM, Web Scraping, Web, R&D, NLP

Andromeda was a project that came about during a transitional period I went through at Nativo where I was being moved from one team to another. This was during the initial boom in popularity of LLMs brought upon us by OpenAI's GPT-4. As such, I was tasked with spending some time to research the capabilities of some of the more popular AI tools and find out how we might utilize them.

I wanted to see if there was a way I could build out a tool like [NIQ]({filename}nativo_iq.md) but more tailored to internal use and enhanced with NLP and LLM capabilities. This ended up working out fairly well. I implemented the tool using FastAPI(mostly so internal teams could use the auto-generated swagger docs) and built out a simple web spidering and scraping module. Users could then post a url or a set of urls to an endpoint and the application would spider those urls(with limits of course) and ingest the content. 

After content was ingested it went through several cleaning and categorization steps. Firslty, the content text would be stripped of all html markup and javascript, then it would be categorized into IAB categories and internal verticals. Following that, the content would go through a process of entity extraction(identify places/things/events/etc mentioned) so we could built out an entity graph. Finally, it would be turned into an embedding and stored in a vector database to be used for [RAG](https://en.wikipedia.org/wiki/Retrieval-augmented_generation).

The data produced from the above process could then be used as context in LLM prompts to generate new content, ad healdines, etc. It could also be used as a knowledge base to allow internal users and content writers to determine a brand's writing style or "voice".

Unfortunately, although this project was deployed for testing, it never gained steam and was never fully productized.


