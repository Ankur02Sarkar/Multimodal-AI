# Multimodal AI Video Insights Platform

A full-stack, cloud-deployed SaaS solution for real-time video sentiment and emotion analysis, trained on human dialogs. Built using PyTorch, AWS SageMaker, Next.js, React, and Tailwind. Inspired by [Train and Deploy a Multimodal AI Model](https://www.youtube.com/watch?v=Myo5kizoSk0).

## Overview
This platform enables users to upload video files and receive comprehensive sentiment and emotion insights for each spoken sentence in the video. Features include multimodal deep learning, cloud training and inference, and a modern SaaS UI with authentication and usage quota management.

- **End-to-end AI SaaS:** From dataset, model training to deployment and SaaS product.
- **Target Users:** Developers, startups, researchers, enterprises seeking advanced video understanding.
- **Demo video:** [YouTube: Train and Deploy a Multimodal AI Model](https://www.youtube.com/watch?v=Myo5kizoSk0)

## Features
- **Multimodal Sentiment & Emotion Analysis:**
  - Audio, Video, and Transcript fusion for accuracy
  - Detects sentiment (positive/negative/neutral)
  - Classifies emotion (joy, sadness, anger, surprise, fear, disgust, neutral)
- **ML Pipeline:**
  - Data preprocessing and feature engineering
  - Model training (PyTorch, MELD dataset)
  - Cloud deployment (AWS SageMaker)
- **SaaS and API:**
  - Next.js/React frontend, Tailwind for UI
  - RESTful inference API
  - Auth.js-based authentication
  - Usage quota dashboard
- **Scalable & Cost-optimized:**
  - AWS S3 storage, GPU compute on SageMaker
  - IAM-based secure endpoints
- **Modern Dev Experience:**
  - Code in VS Code, Python >=3.12
  - Docker/gcloud support


## Tech Stack
| Layer       | Technology                        |
|-------------|------------------------------------|
| ML/AI       | PyTorch, BERT                     |
| Data        | MELD Dataset (Friends Dialogs)    |
| Cloud/Infra | AWS SageMaker, S3, EC2, IAM       |
| Frontend    | Next.js 15, React, Tailwind CSS   |
| API/Auth    | REST, Auth.js, Prisma ORM         |


## Setup Guide
1. **Clone the repo & install dependencies**
2. **Download the MELD dataset (~10GB)**
3. **Configure AWS credentials & create SageMaker resources**
4. **Train model via AWS GPU instances or existing pretrained weights**
5. **Deploy the trained model to SageMaker endpoint**
6. **Start the Next.js webapp for the user dashboard**


## Usage Example
1. Sign up/log in via the SaaS dashboard
2. Upload a video file (.mp4 supported)
3. View real-time sentiment and emotion map per utterance
4. Manage API keys and monthly quota for programmatic inference


## Key Results
- **Highly interpretable output:** Per-sentence predictions visualized in a clear dashboard
- **Cloud scalability:** Leverages AWS for both compute and storage
- **Modern developer experience:** Easily extend the app or plug into other systems


## Model Architecture
- Video frames → CNN → Feature vectors
- Audio signal → Feature extractor
- Transcript (ASR/BERT) → Text embeddings
- **Multimodal fusion** layer merges video, audio, and text
- Classification heads output emotion and sentiment
- Training includes loss weighting for class imbalance


## Use Case Scenarios
- Automated customer feedback analysis from video forms
- Video UGC emotion/sentiment tagging
- Content moderation for emotion-triggering videos
- Research on human emotion recognition in multimedia


## Notable Implementation Details
- PyTorch implementation with BERT for text
- Model tracing, parameter logging (TensorBoard)
- SageMaker deployment script with IAM roles
- Prisma ORM with Next.js/React
- API keys and user authentication (Auth.js)
- Usage quota logic on backend and dashboard
- Supports both training from scratch and loading pretrained weights


## Costs
- Training: ~$15/job on AWS GPU
- Endpoint: ~$1.50/hr uptime
- Data storage: Minimal (S3)
- Free/low-cost options: Run locally or use pretrained weights for demo


## References & Resources
- [Video walkthrough](https://www.youtube.com/watch?v=Myo5kizoSk0)
- [ai-video-sentiment-model (GitHub)](https://github.com/Andreaswt/ai-video-sentiment-model)
- [ai-video-sentiment-saas (GitHub)](https://github.com/Andreaswt/ai-video-sentiment-saas)
- [MELD Dataset](https://affective-meld.github.io/)
- [Excalidraw diagrams, model files, sample data (Google Drive)](https://drive.google.com/drive/folders/1f5tOlIixDUeYtzzIdctQRb_-qllzAMQd)
