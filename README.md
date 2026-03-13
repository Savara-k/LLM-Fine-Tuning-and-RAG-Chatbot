# LLM-Fine-Tuning-and-RAG-Chatbot

## Project Overview
This project demonstrates how to build and fine-tune a Large Language Model (LLM). The notebook walks through the core concepts behind modern NLP systems including prompt engineering, transformer models, parameter-efficient fine-tuning (LoRA), model evaluation using ROUGE metrics, and Retrieval Augmented Generation (RAG).
The goal of the project is to create a knowledge-grounded chatbot capable of summarizing conversations and answering questions using retrieved information from a product knowledge base.
This project was built as a hands-on exercise to better understand how LLM pipelines work in real-world AI applications.

## Key Concepts Covered
* Large Language Models
* Understanding how modern LLMs work including:
* Transformers
* Attention mechanisms
* Tokenization
* Text embeddings
* Prompt Engineering
* Exploring different prompting strategies:
* Zero-shot prompting
* One-shot prompting
* Few-shot prompting
* Dialogue Summarization
* Using the DialogSum dataset to train a model that summarizes conversations.
* Fine-Tuning with LoRA (PEFT)
* Instead of training an entire LLM, this project uses Low-Rank Adaptation (LoRA) to efficiently fine-tune only a small portion of the model parameters.

## Benefits include:
* Lower GPU usage
* Faster training
* Smaller models
* Model Evaluation
* Performance is evaluated using ROUGE metrics, which measure the similarity between generated summaries and reference summaries.
* Retrieval Augmented Generation (RAG)
* A simple RAG pipeline is implemented to allow the chatbot to retrieve product information from a vector database before generating answers.
This helps reduce hallucinations and ensures responses are grounded in real data.

---

## Project Pipeline
The system follows this pipeline:
User Query
    ↓
Prompt Engineering
    ↓
Fine-Tuned LLM (FLAN-T5 + LoRA)
    ↓
Retrieval System (Sentence Transformers + ChromaDB)
    ↓
Context Injection
    ↓
Generated Response

---

## Technologies Used
* Language
* Python 3
* Libraries
* transformers
* datasets
* torch
* evaluate
* rouge_score
* peft
* sentence-transformers
* chromadb
* Model
* FLAN-T5 Base
* Dataset
* DialogSum (Dialogue Summarization Dataset)


---

## Model Performance
After fine-tuning the model for two epochs using LoRA:
* Metric
* Score
* ROUGE-1
* 0.4219
* ROUGE-2
* 0.1789
* ROUGE-L
* 0.3888

These results show improved summarization capability compared to the base model.

---

## Example Output
Dialogue
* Person1: Hey are we still meeting at 3?
* Person2: Can we move it to 3:30?
* Person1: Sure that works.

## Generated Summary
Two people reschedule their meeting from 3:00 to 3:30.


---

## Future Improvements
Possible improvements for future versions of the project:
* Add a Streamlit web interface
* Train on a larger dialogue dataset
* Use larger instruction-tuned models
* Implement RLHF (Reinforcement Learning from Human Feedback)
* Deploy the chatbot using AWS or HuggingFace Spaces
