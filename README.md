# Agricultural Extension RAG: Smart Retrieval for Farmers

This repository contains all project scripts and code required to reproduce the final submission for the **Agricultural Extension RAG: Smart Retrieval for Farmers** competition on Kaggle. The codebase provided matches the final submitted solution exactly.

## Methodology Summary
The core approach centers on a dense retrieval architecture using pre-trained **Sentence Transformers** to match farmer queries with relevant agricultural extension documents[cite: 1]. 
* **Model Selection:** The pipeline employs a 1.34 GB embedding model loaded via `safetensors` for efficient memory mapping and accelerated PyTorch inference[cite: 1].
* **Inference Pipeline:** The retrieval system tokenizes inputs using the `sentence-transformers` configuration and processes them in batched sequences (handling up to 393 batches per run) to compute semantic similarity scores efficiently[cite: 1]. It is designed to work seamlessly with vector search libraries like FAISS.
* **Execution:** All data loading, embedding generation, and final submission formatting are consolidated within the primary Jupyter environment[cite: 1].

## Repository Structure
* **`Agric_code (1).ipynb`**: The primary Jupyter Notebook containing the full end-to-end pipeline, strictly matching the final competition submission[cite: 1].

## Reproduction Steps
1. Clone this repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Download the official competition data and place it inside the `data/` folder.
4. Run all cells sequentially in **`Agric_code (1).ipynb`** to generate the final `submission.csv`
