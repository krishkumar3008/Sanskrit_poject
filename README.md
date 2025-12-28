# Sanskrit RAG System (CPU-Based)

This repository contains an end-to-end **Retrieval-Augmented Generation (RAG)** system designed to answer queries based on Sanskrit documents. The entire pipeline, from ingestion to inference, is optimized to run on **CPU** hardware without requiring a GPU.

## 📌 Project Overview
The goal of this project is to demonstrate a functional RAG pipeline for low-resource languages (Sanskrit) in a resource-constrained environment (CPU only).

* **Domain:** Sanskrit Literature (Stories like *Murkhabhrtyasya*, *Kalidasa*, etc.).
* **Input:** `.docx` documents containing Sanskrit text.
* **Hardware:** CPU (No GPU required).

## 🚀 Features
* **Document Ingestion:** Automated loading and cleaning of `.docx` files using `python-docx`.
* **Smart Chunking:** Text segmentation (500 chars) with overlap to preserve semantic context.
* **Vector Search:** Uses `FAISS` and `paraphrase-multilingual-mpnet-base-v2` for high-accuracy retrieval.
* **CPU Inference:** Utilizes `TinyLlama-1.1B`, a lightweight LLM optimized for standard processors.

## 🛠️ Architecture
1.  **Loader:** Extracts text from `Rag-docs.docx`.
2.  **Embedder:** Converts text chunks into 768-dimensional vectors.
3.  **Vector Store:** Indexes vectors using L2 distance (Euclidean).
4.  **Generator:** A 1.1B parameter Chat model generates answers based on retrieved context.

## 📦 Installation

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/sanskrit-rag-cpu.git](https://github.com/your-username/sanskrit-rag-cpu.git)
   cd sanskrit-rag-cpu
