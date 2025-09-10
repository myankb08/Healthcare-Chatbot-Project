# Healthcare-Chatbot-Project

This project is a domain-specific conversational AI. The chatbot serves as a "Healthcare Information Assistant".

## Features

* **Conversational AI**: Powered by the `phi-3-mini-4k-instruct` language model to understand and generate helpful, natural language responses.
* **Domain-Specific Knowledge**: Includes a custom knowledge base with specific details about the IITGN Health Centre, such as timings, location, services, and emergency contacts. A semantic search mechanism ensures reliable information retrieval.
* **Advanced Memory**: Implements a hybrid memory system using LangGraph to maintain context:
    * **Conversational Memory**: Persists chat history across sessions.
    * **Entity Memory**: Uses the `GLiNER` model to extract and remember key medical and personal entities.
    * **Vector Memory**: Leverages `FAISS` for semantic retrieval of relevant past conversation topics.
* **Optimized Performance**: The model is loaded using **Unsloth** and **4-bit quantization** for efficient, high-speed inference with a low memory footprint
* **Web UI**: Deployed with a clean, user-friendly interface created using **Gradio**.

## How to Run

1.  Clone this repository to your local machine or a cloud environment like Google Colab.
2.  Install the required dependencies using the `requirements.txt` file:
    ```bash
    pip install -r requirements.txt
    ```
3.  Open the `.ipynb` file in a Jupyter environment (Google Colab with a T4 GPU is recommended).
4.  Run all the cells in the notebook. The Gradio user interface will launch in the final cell's output.

## Key Technologies Used

* LangChain & LangGraph
* Gradio
* Hugging Face Transformers
* Unsloth
* FAISS (for vector storage)
* GLiNER (for entity recognition)
