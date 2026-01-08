---
title: "RAG-Powered Document Assistant"
date: 2025-01-08
permalink: /posts/2012/08/blog-post-1/
tags:
  - cool projects
  - AI
  - RAG
---

## 🚀 The Mission
Large Language Models are excellent at general conversation but fail when asked about specific, private datasets. My goal was to build a retrieval system that grounds AI responses in verifiable facts, effectively turning an LLM into a reliable research assistant that doesn't "hallucinate."

## 🛠 Engineering & Architecture
I architected a modular RAG (Retrieval-Augmented Generation) pipeline that handles the transition from raw data to structured AI insight.

* **Orchestration:** Used **LangChain** to manage the flow between the document loader, the retriever, and the generator.
* **Vector Storage:** Integrated **ChromaDB** for high-performance similarity searches.
* **Embedding Model:** Leveraged `sentence-transformers` to map text into high-dimensional vector space.

## 🔍 The Gritty Details
Success in RAG is determined by the quality of the data passed to the model. I focused on three technical optimizations:

1.  **Semantic Chunking:** I implemented **Recursive Character Text Splitting** with a 200-character overlap. This prevents "context clipping" where a vital piece of information is split between two chunks, losing its meaning.
2.  **Vector Persistence:** Instead of an in-memory store, I configured a persistent local database in ChromaDB, allowing the system to scale to thousands of pages without re-indexing on every launch.
3.  **Source-Grounded Prompting:** I engineered a strict system prompt that forces the model to cite its sources from the retrieved metadata. If the answer isn't in the provided context, the model is instructed to admit it doesn't know, rather than guessing.

---

### Key Takeaways
* **Language:** Python
* **Libraries:** LangChain, PyPDF2, ChromaDB
* **Status:** Complete / Prototype
