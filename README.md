Speech Mastery Application

Overview

The Speech Mastery App is designed to help students improve their public speaking skills. This Flask-based web application is designed to help users enhance their speech clarity and delivery. It processes audio input to provide feedback on filler words, grammar, pauses, and emotions. The application utilizes OpenAI's Whisper model for speech-to-text conversion, an emotion detection model for analyzing tone, and other NLP techniques for speech refinement.

Features

Speech-to-Text Conversion: Uses Whisper model for high-accuracy transcription.

Filler Word Detection & Removal: Identifies and removes common filler words from speech.

Grammar Correction: Provides corrections for grammatical errors using language_tool_python.

Long Pause Detection: Analyzes pauses in speech and provides insights.

Emotion Analysis: Detects emotions in speech and visualizes their distribution.

Visual Feedback: Generates plots for pause durations and emotion probabilities.

Installation

Prerequisites

Please make sure that you have Python 3.8 or later installed.

Clone the Repository

git clone https://github.com/Rachana311/speech-mastery.git
cd speech-mastery

Install Dependencies

Use pip to install the required dependencies:

pip install -r requirements.txt

Required Libraries

The application requires the following libraries:

Flask
pydub
matplotlib
numpy
transformers
whisper
language_tool_python
librosa
torch
base64
re

Usage

Running the Application

python app.py

The application will start and be accessible at http://127.0.0.1:5000/.

How to Use

Upload an audio file (supported formats: WAV, MP3, M4A).

The application transcribes the speech, removes filler words, and corrects grammar.

It analyzes long pauses and emotion distribution.

Feedback and visual insights are displayed on the results page.

API Endpoints

POST /upload - Accepts audio files for processing.

GET /results - Returns processed results including transcript, grammar corrections, filler word analysis, and emotional insights.

Models Used

Whisper (Large): Converts speech to text.

Hugging Face Emotion Model (firdhokk/speech-emotion-recognition-with-openai-whisper-large-v3): Predicts emotions in speech.

File Structure

/ speech-mastery
    |-- app.py                # Main Flask application
    |-- templates/            # HTML templates for the web interface
    |-- static/               # CSS, JS, and image files
    |-- requirements.txt      # List of dependencies
    |-- README.md             # Documentation
