[العربي](./03-nlp_ar.md)

# <a name="-3-natural-language-processing"></a>🤖 Chapter 3: Natural Language Processing (NLP)

## 1. What is it?
NLP deals with the interaction between computers and human language — building systems that can understand, generate, and reason about text and speech.

## 2. What does the specialist do?
An NLP specialist preprocesses text, chooses tokenization and embedding strategies, fine-tunes or trains language models, builds retrieval and QA systems, and evaluates model outputs with appropriate metrics.

## 3. Sub-domains
- Text classification and sentiment analysis  
- Sequence labeling (NER, POS tagging)  
- Machine translation and summarization  
- Question answering and retrieval-augmented generation (RAG)  
- Conversational AI and dialog systems

## 4. Expanded Key Concepts
- Tokenization (BPE, WordPiece), static vs contextual embeddings  
- Masked vs causal language modeling, attention and Transformers  
- Evaluation metrics: BLEU, ROUGE, F1, perplexity  
- Prompting and instruction tuning for LLMs

## 5. Expanded Tools & Technologies
- Hugging Face Transformers & Datasets, Tokenizers  
- spaCy, NLTK, SentenceTransformers, Faiss for vector search  
- Serving: ONNX Runtime, Triton, Hugging Face Inference

## 6. In-Depth Workflow (example: document QA system)
1. Chunk documents and compute embeddings.  
2. Build a vector index (FAISS) for retrieval.  
3. Fine-tune a reader model (extractive/abstractive) on QA pairs.  
4. Orchestrate retriever → reader and monitor hallucinations.

## 7. Common Job Roles
- NLP Engineer  
- Conversational AI Engineer  
- Information Retrieval Engineer

## 8. A-Z Glossary

<details>
<summary>Click to expand/collapse the glossary</summary>

| Term | Explanation |
|---|---|
| **`Attention`** | A mechanism that allows a model to focus on relevant parts of the input sequence. |
| **`BLEU`** | A metric for evaluating the quality of machine-translated text. |
| **`Contextual Embedding`** | A word embedding that depends on the context in which the word appears. |
| **`Decoder`** | The part of a sequence-to-sequence model that generates the output sequence. |
| **`Embedding`** | A vector representation of a word or token. |
| **`F1`** | A measure of a test's accuracy. It is the harmonic mean of precision and recall. |
| **`GPT`** | Generative Pre-trained Transformer. |
| **`Masked LM`** | Masked Language Model. |
| **`NER`** | Named Entity Recognition. |
| **`Prompt`** | The input text given to a language model. |
| **`QA`** | Question Answering. |
| **`RAG`** | Retrieval-Augmented Generation. |
| **`Tokenizer`** | A tool that splits text into smaller units called tokens. |

</details>

[⬆️ Back to Table of Contents](./README_AI_en.md)
