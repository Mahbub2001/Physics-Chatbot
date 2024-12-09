# Physics Book Chatbot

## **Physics Book Chatbot**

A physics-focused chatbot application built using **Streamlit** and **LangChain**, designed to answer questions strictly based on a provided physics textbook PDF. The chatbot also includes an evaluation pipeline to measure the quality of its answers using **ROUGE** and **BLEU** metrics. It uses the **Llama 3.1** model for generating accurate, context-based responses.

---

## **Features**
1. **Physics Chatbot:**
   - Answers questions based solely on the content of the physics textbook.
   - Retrieves relevant information using embeddings and a retriever.
   - Ensures no hallucinated or external information is included in responses.

2. **Llama 3.1 Model:**
   - Utilizes **Llama 3.1**, a state-of-the-art lightweight LLM optimized for high-quality, context-aware responses.

3. **Evaluation Metrics:**
   - Supports **ROUGE** (ROUGE-1, ROUGE-2, ROUGE-L) for overlap-based evaluation.
   - Implements **BLEU** for assessing response accuracy against reference answers.
   - Automatically processes a set of questions and reference answers for evaluation.

4. **Streamlit Interface:**
   - Simple and interactive chat interface.
   - Displays dynamic chatbot responses with a typing effect.
   - Presents evaluation results in an organized table format.

---

## **Evaluation Metrics**

### **ROUGE**
Measures the overlap between chatbot responses and reference answers:
- **ROUGE-1 F1**: Unigram overlap.
- **ROUGE-2 F1**: Bigram overlap.
- **ROUGE-L F1**: Longest common subsequence.

### **BLEU**
Evaluates the n-gram precision of chatbot responses against reference answers:
- Scores range from **0** (poor match) to **1** (perfect match).

---

## **Dependencies**
All dependencies are listed in `requirements.txt`. Key libraries include:
- **`streamlit`**: For the interactive web interface.
- **`langchain`**: For building the chatbot's retrieval-augmented generation (RAG) pipeline.
- **`chroma-db`**: For vector storage and retrieval.
- **`nltk`** and **`rouge-score`**: For evaluation metrics.
- **`Llama 3.1`**: For generating context-aware responses.

---

## **Acknowledgments**
- **LangChain**: For the framework enabling RAG-based conversational AI.
- **Ollama**: For the lightweight and efficient LLM used for generating responses.
- **Streamlit**: For providing an easy-to-use interface for interactive applications.

---

## **Setup and Installation**

### Prerequisites
- Python 3.8 or higher
- A physics textbook PDF (`phybook10.pdf`) 
- [Ollama LLM](https://ollama.ai/) running locally
- **Llama 3.1** installed and ready to serve responses

### Installation Steps
# Install additional packages using pip
pip install -r requirements.txt

# Run
streamlit run emne.py

# Test
streamlit run test_emne.py
