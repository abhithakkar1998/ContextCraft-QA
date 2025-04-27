# ContextCraft-QA: A Simple Question Answering System

This repository contains a basic question answering (QA) system that utilizes Sentence Transformers for embedding generation, FAISS for similarity search, and GPT-2 for answer generation. We implement RAG by embedding text chunks and queries, retrieving the most similar chunks, and then prompting GPT-2 to answer based on that retrieved context.

**⚠️ Important: This is a demonstration project with very simple data samples. The system's accuracy and coherence are limited by the small and basic dataset provided. Expect some repetition and potentially imperfect answers. ⚠️**

## Features

* **Document Chunking:** Splits input text files into smaller chunks.
* **Embedding Generation:** Uses Sentence Transformers to create vector embeddings of text chunks.
* **Similarity Search:** Employs FAISS to efficiently retrieve relevant context chunks based on a query.
* **Answer Generation:** Leverages GPT-2 to generate answers from the retrieved context.

## Limitations

* **Small Dataset:** The system is trained on a very limited set of text files, resulting in a narrow scope of knowledge.
* **Simple Implementation:** This is a basic implementation intended for educational purposes. It lacks many of the robustness and optimization features of a production-ready QA system.
* **Repetitive Output:** Due to the simplicity of the model and dataset, the system may sometimes produce repetitive or redundant answers.
* **Potential Inaccuracies:** The generated answers may not always be accurate or complete.

## Files

* **`get_wiki_data.ipynb`:** This Jupyter Notebook is responsible for fetching and preprocessing data from Wikipedia. It can be used to generate the text files used as the knowledge source for the QA system. You can modify the topics you need in this file.
* **`contextcraft_qa.ipynb`:** This Jupyter Notebook contains the core logic of the question answering system. It handles document chunking, embedding generation, similarity search, and answer generation.

## Getting Started

1.  Clone the repository.
2.  Install the required libraries (see `requirements.txt` - create this file).
3.  Generate the necessary data text files by running the cells in `get_wiki_data.ipynb`. These files will be saved to the dataset/ directory.
4.  Execute the cells in `contextcraft_qa.ipynb` to observe the RAG and LLM components.

## Improvements and Future Work

* **Larger and More Diverse Dataset:** Significantly expanding the dataset will improve the system's ability to handle a wider range of queries and reduce repetition.
* **Advanced Chunking Strategies:** Implementing more sophisticated chunking methods (e.g., semantic chunking) can help preserve context and improve retrieval.
* **Fine-tuning the Language Model:** Fine-tuning GPT-2 (or a more powerful language model) on a QA dataset can greatly enhance answer quality.
* **Prompt Engineering:** Experimenting with different prompt formats can influence the generated answers.
* **Repetition Penalty:** Adding a repetition penalty during answer generation can help reduce redundant output.
* **Evaluation Metrics:** Implementing metrics to evaluate the system's performance (e.g., BLEU, ROUGE) would allow for quantitative comparisons of different approaches.

## Disclaimer

This project is for educational and demonstrative purposes only. It is not intended for production use.
