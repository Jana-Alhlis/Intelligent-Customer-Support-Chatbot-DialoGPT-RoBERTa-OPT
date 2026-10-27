# AI-Based Customer Support Chatbot

## Project Overview

This project focuses on exploring transformer-based Natural Language Processing (NLP) techniques to develop an AI-driven customer support chatbot. The system is designed to process customer messages, identify their intent and sentiment, and produce relevant conversational responses.

Three language models—DialoGPT, RoBERTa, and OPT-125M—were examined to understand their different capabilities in dialogue generation, text classification, and sentiment analysis within customer service scenarios.

## Project Goals

- Develop an approach for automating routine customer support interactions.
- Generate responses based on customer messages and conversational context.
- Identify the intent behind customer inquiries.
- Detect sentiment to better understand customer feedback.
- Compare language models based on response quality and computational requirements.

## Dataset Description

The experiments used a customer support dataset containing question-and-answer pairs and conversational text.

| Attribute | Description |
|---|---|
| Initial dataset | 27,000 records |
| Experimental sample | 5,000 records |
| Training portion | 80% |
| Testing portion | 20% |
| Application domain | E-commerce and customer service |

The data covers customer inquiries and support responses, along with additional fields related to query categories, sentiment, response times, and resolution status.

## Implementation Approach

### 1. Text Preparation

The data preparation stage involved several operations to make the text suitable for model training:

- Handling missing or incomplete entries.
- Standardizing text formatting and punctuation.
- Removing unnecessary spaces and unwanted characters.
- Converting text into model-compatible tokens.
- Applying padding where required.
- Dividing the data into training and testing sets.

### 2. Models Investigated

**DialoGPT — Dialogue Generation**

DialoGPT was explored for generating natural-language replies to customer inquiries. The experiments reported an improvement in accuracy when the input sequence length increased from 100 to 150 tokens.

**RoBERTa — Text Understanding**

RoBERTa was considered for extracting meaning from customer messages, particularly for intent classification and sentiment detection. Its architecture is better suited to text understanding tasks than unrestricted conversational generation.

**OPT-125M — Text Generation**

OPT-125M was evaluated as an alternative language-generation model, with attention to response speed and computational cost. The reported observations highlighted trade-offs involving fluency, context retention, and response consistency.

### 3. Experimental Setup

The documented environment included the following configuration:

- **Language:** Python 3.9
- **Deep Learning Framework:** PyTorch
- **Transformer Tools:** Hugging Face Transformers
- **Text Processing:** NLTK and spaCy
- **Batch Size:** 8
- **Learning Rate:** 2e-5
- **Training Epochs:** 3
- **Optimizer:** AdamW
- **Platform:** Google Colab

## Evaluation

The models were assessed using reported classification metrics, text-generation metrics, and qualitative review of their outputs.

| Model | Reported Metrics | Observations |
|---|---|---|
| DialoGPT | 62% accuracy, 100% precision, 62% recall, 77% F1-score, 0.39 ROUGE-L | Showed promising results for conversational response generation. |
| OPT-125M | 77% F1-score, 0.39 ROUGE-L | Offered an alternative for text generation, with some limitations in coherence. |
| RoBERTa | 32.7% reported response accuracy, 25% F1-score | More appropriate for classification and sentiment-related tasks. |

*Note: These values reflect the reported experiments and should not be interpreted as directly comparable without consistent evaluation procedures for each task.*

## Main Observations

- DialoGPT showed potential for producing contextually relevant customer support replies.
- Input sequence length affected the reported generation results.
- OPT-125M presented a trade-off between computational efficiency and response quality.
- RoBERTa offered a different approach focused on understanding and classifying customer text.
- A pipeline combining intent detection with a dedicated response-generation model could be investigated in future experiments.

## Tools and Technologies

- Python
- Natural Language Processing (NLP)
- DialoGPT
- RoBERTa
- OPT-125M
- PyTorch
- Hugging Face Transformers
- NLTK
- spaCy
- Google Colab

## Limitations and Future Directions

The experiments relied on a subset of the available data, which may limit the diversity of customer scenarios represented during training and evaluation.

Potential future improvements include:

- Increasing the diversity of training examples.
- Fine-tuning models on customer-service-specific conversations.
- Integrating intent classification and response generation into one workflow.
- Improving response relevance and conversational consistency.
- Testing the system on unseen customer inquiries.
- Establishing task-specific evaluation metrics for classification and text generation.

## Project Scope

This project explores the application of transformer architectures to customer support automation, emphasizing conversational response generation, customer-message classification, sentiment analysis, and the trade-offs between language-model capabilities.
