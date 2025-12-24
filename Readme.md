# Starting Point - LinkedIn's Filter sucks.

While searching for an internship position, I came across lots of unrelated positions. After realizing how bad LinkedIn job search filtering is,   
I decided to do my own filtering. In the following section of the README page, you can find insights, my steps, and improvements of the script during the project.

# Steps I followed.

During this project, I wanted to deal with a little bit of Object-Oriented Programming and decided to give my best using defs. After building a base structure, I'll deepen my knowledge and usage of OOP elements.

First of all, I tried to scrape job listings on LinkedIn, in which I learned valuable lessons about changing IDs, etc. In this manner, I used AI to detect which elements to look for.

After that, I implemented a locally run LLM using Ollama.

Once everything was running without an error, I tried to fine-tune the prompt, because I wasn't amazed by the labeling that the LLM was doing. Its rules were mostly too tolerant and working faster than I expected.

During fine-tuning, I realized some "mistakes" that affected the quality of the LLM's output. I was asking AI to rate the company based on size, the location of the position based on the "beauty" of the location, and the relevance to Data Science. Which wasn't that optimal for an LLM, especially for a small model.

After realizing that the LLM wasn't understanding what I meant by "beautifulness" and failing at rating things since it had no extensive comparison, I decided to only check whether the position fits my requirements or not with a simple return "recejted" or "accepted".

# Current State

Currently, I am trying to improve the labeling by changing the prompt. I was aiming a high Recall, however I'am not happy with the results, therefore I'll focuse more on precision. Besides, I should send the links in a better format, which should make it able to click easier. 

## Recent Updates: 
-> I scheduled a task on an old computer, which triggers the script once a day. -> Since some job listings may appear multiple times, the script checks whether the job was already seen by storing a text file with the links of scraped job listings. The LLM is only used if the job (i.e., the link) is not in that file.
-> Since some job listings may appear mutlible times, the script checks, wahter the job is already seen by storing a text file with the links of scraped job listings. LLM is only used, if the job (aka. the link) is not in that file. 

