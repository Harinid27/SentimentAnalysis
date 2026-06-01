# Voice-Based Sentiment Analysis using Whisper and DistilBERT

## Overview

This project is a simple end-to-end AI pipeline that performs sentiment analysis on voice input.

The user provides an audio file containing speech. The system converts the speech into text using OpenAI Whisper, analyzes the sentiment of the transcribed text using a pretrained DistilBERT sentiment model from Hugging Face, and finally converts the prediction result back into speech using gTTS.

The complete workflow combines Speech Recognition, Natural Language Processing, and Text-to-Speech synthesis into a single pipeline.

---

## Features

* Converts speech audio into text using Whisper
* Performs sentiment analysis using a transformer model
* Predicts whether the sentiment is Positive or Negative
* Converts the final prediction into voice output
* Supports `.mp3` and `.wav` audio files
* Easy to run in Google Colab

---

## Technologies Used

* Python
* OpenAI Whisper
* Hugging Face Transformers
* DistilBERT
* gTTS (Google Text-to-Speech)
* PyTorch
* Google Colab

---

## Project Workflow

```text
Audio Input
     ↓
Whisper Speech Recognition
     ↓
Text Transcription
     ↓
DistilBERT Sentiment Analysis
     ↓
Positive / Negative Prediction
     ↓
gTTS Text-to-Speech
     ↓
Final Audio Output
```

---

## Models Used

### 1. Whisper

Used for Speech-to-Text conversion.

Model:

```python
whisper.load_model("base")
```

Whisper is capable of understanding speech from audio files and converting it into readable text.

---

### 2. DistilBERT Sentiment Model

Used for sentiment classification.

Model:

```python
distilbert/distilbert-base-uncased-finetuned-sst-2-english
```

This model predicts whether the transcribed sentence has a positive or negative sentiment.

---

### 3. gTTS

Used for converting the final sentiment result into audio.

---

## Installation

Install the required libraries:

```python
!pip install openai-whisper
!pip install transformers
!pip install torch
!pip install gTTS
```

---

## How to Run

### Step 1

Open the notebook in Google Colab.

### Step 2

Install all required libraries.

### Step 3

Upload an audio file (`.mp3` or `.wav`).

### Step 4

Run all cells in sequence.

### Step 5

The system will:

* transcribe the audio
* predict the sentiment
* generate spoken output

---

## Example

### Input Audio

```text
"I really love this product"
```

### Transcribed Text

```text
I really love this product
```

### Predicted Sentiment

```text
POSITIVE
```

### Final Audio Output

```text
"The predicted sentiment is POSITIVE"
```

---

## Folder Structure

```text
project/
│
├── sentiment_analysis.ipynb
├── sample_audio.mp3
├── sentiment_output.mp3
└── README.md
```

---

## Learning Outcomes

This project helped in understanding:

* Speech Recognition
* Transformer-based NLP
* Pretrained Models
* Sentiment Analysis
* Audio Processing
* End-to-End AI Pipelines
* Hugging Face model usage
* Text-to-Speech synthesis

---

## Future Improvements

Some possible future enhancements:

* Add real-time microphone input
* Support multilingual sentiment analysis
* Detect emotions instead of only positive/negative
* Build a web application interface
* Deploy using Flask or FastAPI
* Add conversation memory and chatbot integration

---

## Conclusion

This project demonstrates how multiple AI models can be combined to create a complete voice-based sentiment analysis system. It integrates speech recognition, NLP, and speech synthesis into one workflow and provides a practical understanding of how modern AI pipelines work in real-world applications.

---
