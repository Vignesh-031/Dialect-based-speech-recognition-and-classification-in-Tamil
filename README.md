CODERS@DravidianLangTech 2026
Dialect-Based Speech Recognition and Classification in Tamil

This repository contains the implementation of our system submitted to the Shared Task on Dialect-Based Speech Recognition and Classification in Tamil at DravidianLangTech 2026 (ACL Workshop).

👥 Team CODERS

Nilu R Salim

A Dileep Ram

S Madhu Vishahan

TT Pranesh

kk Tamizh Mathi

S Vigneshwaran

Department of Computer Science and Engineering
Sri Sivasubramania Nadar College of Engineering

📌 Task Description

The shared task focuses on processing dialectal Tamil speech and consists of two subtasks:

Subtask 1 — Dialect Classification

Predict the dialect category from a given speech recording.

Dialect labels include:

Northern

Southern

Western

Eastern

Subtask 2 — Automatic Speech Recognition (ASR)

Generate accurate Tamil text transcriptions from dialectal speech recordings.

The task evaluates the ability of models to handle dialectal pronunciation variations and low-resource speech data.

🧠 System Overview

Our system uses a hybrid pipeline combining speech recognition and transformer-based language modeling.

1️⃣ Dialect Classification Pipeline

Steps:

Speech audio input

Transcription using Whisper ASR

Text preprocessing

Dialect prediction using Tamil-BERT Transformer

Model details:

Pretrained Model: l3cube-pune/tamil-bert

Batch size: 16

Learning rate: 2e-5

Epochs: 11

Optimizer: AdamW

Output:

Dialect label prediction:

Central

Northern

Southern

Western

2️⃣ Automatic Speech Recognition (ASR)

For the ASR task, we fine-tuned a pretrained Whisper model to improve transcription accuracy on dialectal Tamil speech.

Steps:

Speech audio input

Feature extraction (log-Mel spectrogram)

Whisper fine-tuning

Adapted ASR model

Tamil text transcription

Model details:

Model: Whisper-tiny

Learning rate: 1e-5

Training steps: 200

Batch size: 1

Sampling rate: 16 kHz

📊 Results Summary
Subtask 1 — Dialect Classification
Model	Metric	Score	Rank
Whisper + Tamil-BERT	Macro F1-score	0.18	Rank 10
Subtask 2 — Automatic Speech Recognition
Model	Metric	Score	Rank
Fine-tuned Whisper-tiny	Word Error Rate (WER)	0.95	Rank 9
