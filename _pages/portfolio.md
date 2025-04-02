---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: true
---

I'm deeply passionate about creating consumer-facing AI products. Here are a range of research and personal projects I have worked on over the past few years!

---

## 🧪 Research Projects

### Simulus – XR + LLM based Social Simulations for Self-Care

<img src="{{ '/files/demos/Simulus_Demo.gif' | relative_url }}" alt="Simulus Demo" width="560" height="315">

Simulus was a project built as part of my time doing research with Professor Haiyi Zhu, Anna Fang, and Alekhya Maram at Carnegie Mellon University. Haiyi, Anna, and Alekhya were so lovely to work with and made this summer the undoubtedly best summer of my 21 years. We built Simulus as a way for users to practice stress relief in AR/VR using the Meta Quest 3, allowing them to navigate stressful situations by conversing with ChatGPT-based virtual avatars. This also marked my first time developing in XR.

**Key Features**
* **LLM-Based Avatars**: We enabled GPT-4o-based avatars in our system, creating personas with different identities and conversational styles.
* **Contextual Memory**: Our system builds on previous conversations to enhance realism and immersion over time.
* **Speech-to-Text Integration**: To allow users to directly interact with avatars using just their voice, we integrated OpenAI's Whisper API.

**Tech Stack**: Unity OpenXR, GPT-4o, OpenAI Whisper
---

### SoundWatch - Deep Learning based Sound Awareness System for iPhone and Apple Watch

<iframe width="560" height="315" src="https://www.youtube.com/embed/aanpbJIDB4g?si=8h4zeGKxkCLtDl5v" frameborder="0" allowfullscreen></iframe>

SoundWatch is a deep learning-based sound awareness system for Deaf and Hard of Hearing users, designed to run on iPhone and Apple Watch. It alerts users to important environmental sounds like alarms, sirens, or doorbells through haptic and visual cues.

**Key Features**
* **Real-Time Sound Detection**: Uses CoreML and a custom sound classification model to detect sound events locally on-device.
* **Seamless Watch Integration**: Logs and notifies users via the Apple Watch with a companion iOS app.
* **Event Logging System**: Built a full-stack backend + dashboard to view logs and analyze usage patterns across time.

**Tech Stack**: Swift, CoreML, FastAPI, React, PostgreSQL

---

## 🚀 Personal Projects

### EverArc – A Simple Habit Tracker for iOS (Personal Project)

<iframe width="560" height="315" src="https://www.youtube.com/embed/6vDa7zFkcOc" frameborder="0" allowfullscreen></iframe>

Over the years, I have tried many different Habit Tracker apps, but I was never able to consistently log habits over a long period of time. I wanted to use a simple, yet effective app that reduced setup friction while also delivering visually crafty ways of showing me my progress. This led to the development of EverArc! Try out the beta version for free on TestFlight!

**Key Features**
* **Quick, One-Tap Habit Tracking**: Complete your daily habits with a single tap, with automatic streak calculation to keep your motivation high.
* **Visual Progress System**: Color-coded progress rings and calendar heatmaps make it easy to see your consistency at a glance, with celebratory animations when you complete all habits.
* **Minimalist, Focused UI**: No unnecessary settings or overwhelming options—just the essential features you need to build better habits consistently.

**Tech Stack**: SwiftUI, SwiftData, SwiftCharts

---

### Words of Wisdom – An AR-Based Cognitive Defusion App

<iframe width="560" height="315" src="https://www.youtube.com/embed/Lc0h_Mie0o0" frameborder="0" allowfullscreen></iframe>

Negative thoughts can impact our mood and behavior. *Words of Wisdom* is an Augmented Reality experience inspired by Cognitive Defusion, helping users visualize thoughts as separate from themselves and let them go—both physically and emotionally—through mindful breathing.

**Key Features**
* **Thoughts in AR**: Visualize your thought as a floating 3D object, paired with a drifting cloud to symbolize letting go.
* **Breath-Powered Interaction**: Move the cloud by exhaling into the mic, with sound classification ensuring only real breathing triggers motion.
* **Guided Reflection & Logs**: Reframe thoughts with affirmations, categorize them, and track progress using a self-reflection log.

**Tech Stack**: SwiftUI, CoreML, ARKit, SwiftData, SoundAnalysis

---

### OpenTitan RAG – An AI-Powered Document Assistant

<iframe width="560" height="315" src="https://www.youtube.com/embed/MeZdiM05C2s" frameborder="0" allowfullscreen></iframe>

Navigating complex technical documentation can be challenging. *OpenTitan RAG* is a specialized Retrieval-Augmented Generation system that helps users efficiently find and understand information about the OpenTitan project by combining powerful document retrieval with AI-driven natural language responses.

**Key Features**
* **Intelligent RAG System**: Utilizes FAISS indices for efficient semantic search across document embeddings, enabling users to ask natural language questions and receive precise information without manual keyword searching.
* **Conversation Memory & Context**: Maintains chat history to handle follow-up questions and provide consistent responses throughout extended interactions, creating a coherent experience across complex technical topics.
* **User-Friendly Interface**: Clean, responsive design with dark/light mode, chat management features, and markdown rendering for easy consumption of technical content with source attribution.

**Tech Stack**: Claude 3 Opus, FAISS Vector Indices, Sentence Transformers, Flask, React, Hugging Face Embeddings, Langchain, PyTorch
