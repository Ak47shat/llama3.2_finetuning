# 🦙 Llama 3.2 Fine-Tuning: All-in-One Guide

This repository offers a **complete, end-to-one workflow** for fine-tuning Llama 3.2, contained entirely within the `llama3_2_finetuning.ipynb` Jupyter Notebook.

## ⚙️ Prerequisites & Setup

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/Ak47shat/llama3.2_finetuning.git
    cd llama3.2_finetuning    
    ```
2.  **Install Dependencies:**
    ```bash
    pip install transformers accelerate datasets sentencepiece bitsandbytes
    pip install torch --index-url [https://download.pytorch.org/whl/cu118](https://download.pytorch.org/whl/cu118) # For CUDA 11.8
    ```
3.  **Data:** Add your training dataset files to the `./data/` directory.

## ▶️ Execution Steps

1.  **Launch Notebook:**
    ```bash
    jupyter notebook llama3_2_finetuning.ipynb
    ```
2.  **Run:** Execute all cells in the notebook sequentially.
3.  **Output:** The fine-tuned model will be saved in the `./outputs/` directory.

## 🧪 Key Features in the Notebook

The notebook handles the entire lifecycle:

| Category | Features Included |
| :--- | :--- |
| **Model Setup** | Loads Llama 3.2 and tokenizer. |
| **Data Processing** | Preprocesses and tokenizes datasets. |
| **Training** | Uses `transformers` + `accelerate`. |
| **Optimization** | Optional **4-bit training** with `bitsandbytes` (for lower VRAM). |
| **Evaluation** | Calculates **perplexity** and provides **sample generations**. |
| **Export** | Instructions for local inference, quantized inference, and Hugging Face Hub upload. |

## ⚠️ Important Notes

* Reduce batch size if GPU VRAM is low.
* Avoid unnecessarily high learning rates to prevent instability.
* Model performance highly depends on the quality of your dataset.

This project is released under the **MIT License**.
