# Generative-Ai-with-Large-Language-Models
Generative AI for Dialogue Summarization

Overview

This project focuses on summarizing conversational dialogues using a Generative AI model. The primary objective is to process and distill key information from dialogues efficiently while maintaining context and coherence. The project utilizes the FLAN-T5 model from Hugging Face, a state-of-the-art transformer model fine-tuned for natural language generation tasks.

Features

Summarizes multi-turn conversational dialogues into concise summaries.

Leverages pre-trained FLAN-T5 to ensure high-quality summaries.

Customizable parameters for adjusting summary length and style.

Deployable on cloud infrastructure for scalability.

Technologies Used

Programming Language: Python

Model: FLAN-T5 from Hugging Face

Libraries/Frameworks:

Hugging Face Transformers

PyTorch

Pandas and NumPy (for data preprocessing)

Tools: Jupyter Notebook, Google Colab

Deployment Platform: AWS (Optional)

Project Structure

project-directory
|— data/
|   — sample_dialogues.json   # Example input data
|— notebooks/
|   — Generative_AI_Dialogue_Summarization.ipynb  # Main notebook
|— src/
|   — preprocessing.py         # Preprocessing scripts
|   — summarize.py           # Summarization logic
|— models/
|   — flan_t5/              # Model files (optional)
|— README.md

Setup Instructions

Clone the Repository

git clone <repository_url>
cd project-directory

Install Dependencies
Ensure you have Python 3.8+ installed, then run:

pip install -r requirements.txt

Download the Model
Load the FLAN-T5 model using Hugging Face’s API:

from transformers import T5ForConditionalGeneration, T5Tokenizer

tokenizer = T5Tokenizer.from_pretrained("google/flan-t5-base")
model = T5ForConditionalGeneration.from_pretrained("google/flan-t5-base")

Run the Notebook
Open the Generative_AI_Dialogue_Summarization.ipynb notebook in Jupyter or Colab, and follow the step-by-step instructions.

Usage

Input Format
Provide conversational dialogues in JSON format:

{
  "dialogues": [
    "Speaker 1: Hello, how are you?",
    "Speaker 2: I’m good, thank you! How about you?",
    "Speaker 1: Doing well, thanks for asking!"
  ]
}

Generate Summaries
Use the summarization script or notebook to process the input:

from src.summarize import generate_summary

summary = generate_summary(dialogues)
print(summary)

Output Example



Summary: The speakers exchange greetings and check on each other's well-being.
