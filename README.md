**RAG-based Information Retrieval System**
Welcome to the RAG-based (Retrieval-Augmented Generation) Information Retrieval System! This project demonstrates a simple yet effective pipeline for leveraging state-of-the-art language models and embedding techniques to build an intelligent information retrieval system.

**Overview**
In this project, I developed a system that can answer questions based on a diverse set of textual data sources, including website notes and research papers. The pipeline involves data preparation, chunking, vector embedding creation, and utilizing a language model for retrieval and generation.
**
Key Steps**

**1. Data Preparation**
Web Scraping: Collected data from specified websites containing notes.
Research Papers: Extracted text from two seminal papers:
"Attention is All You Need": Converted HTML to text.
"GPT": Extracted LaTeX content and converted it to text.

**2. Data Chunking**
Utilized the Natural Language Toolkit (NLTK) for chunking the prepared unstructured data.
Chose simple chunking over semantic chunking due to better performance with the extracted text from research papers.

**3. Vector Embeddings of Chunks**
Employed the 'all-MiniLM-L6-V2' mini language model to create vector embeddings for the chunks.
Stored these embeddings locally in a numpy ndarray for efficient retrieval.

**4. Model Selection**
Used the 'Gemini-1.5-flash' model for generation, balancing precision and creativity with a temperature setting of 0.5.
Increased the token limit to 10,000 to enable more comprehensive answers.

**5. Generation with RAG**
Implemented a system prompt to guide the model’s responses.
Created embeddings of the input prompt and retrieved similar chunks using cosine similarity.
Passed the relevant chunks to the model to generate informative answers.

**How to Use**
Run the Colab Notebook:
Open the Colab File.
Execute all cells (Ctrl + F9) to initialize the pipeline and generate answers based on your queries.

**Important Notes**
This project is a prototype and can be integrated into a more structured codebase for further development.
The choice of tools and models was driven by availability and resource constraints.

**Future Work**
Improve Data Chunking: Experiment with advanced semantic chunking methods for better performance.
**Vector Database**: Implement a more robust vector database for efficient storage and retrieval.
**Enhanced Models**: Explore more powerful language models as resources allow.
