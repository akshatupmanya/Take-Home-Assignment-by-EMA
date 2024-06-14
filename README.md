**Collab File - https://colab.research.google.com/drive/1VS0E1wXq1FWLMCOpd6RaHNLpw6pDAkNm?authuser=1#scrollTo=3VKI6jVJtueg**
I made a RAG based project, where I tried to solve your assignment, I took these steps:

**DATA PREPARATION**
I scraped all the data from Notes(Given websites), data from two research papers(In first, I took HTML file and converted that into text and in second, I took Latex content from file and then converted into text… I hope you understand why I did that and not did directly scraping from pdfs ) ‘Attention is all you need’ and ‘GPT’.
**CHUNKING OF DATA:**
I simply made chunks of prepared unstructured data. I used NLTK(Natural Language Tool Kit) for chunking the data. I used simple chunking, although I tried first semantic chunking, but it was not that effective on Text extracted by Papers. 
**Vector Embeddings of Chunks(Local Vector DB)**
I used ‘all-MiniLM-L6-V2’ mini language model for embedding, although I tried another mini Language model first, but it was not giving that good results.
I made vector embeddings of all chunks and stored that into a ‘numpy-nd-array’, (I don’t had time to make a vector db, so I made a local one)
**Model:**
I used ‘Gemini-1.5-flash’ as it was only large language family I can afford…
temperature is 0.5 as I want balanced outputs, neither too precise, nor too creative. I increased token limit to 10000 as I wanted more explained output and model can use all parameters to give an amazing explained answer. 
**Generation(With RAG):**
I simply passed a system prompt that gives instruction to model, like what to response and how to response, and then I made embedding of given prompt, retrieved similar chunks from DB through cosine similarity and passed it through model and It gave me answers.
**Important note.**
I just created a simple pipeline and Working Collab code, which can be integrated in a structured code.
