# Pesport Multi-Modal Agent

This repository contains the code and configurations for the **Pesport Multi-Modal Agent**—an AI-powered interactive assistant designed to enhance the user experience for Pesport, a digital gaming company. The agent supports various input modes, including text, image, and voice, delivering an engaging and versatile interaction model for users. 

The agent was built using Azure AI Studio, utilizing OpenAI's models (GPT-4, DALL·E, and Whisper) to handle different types of user inputs and offer real-time responses within the gaming app. This README provides an overview of the project, its features, technical architecture, and setup instructions for deploying and integrating the agent.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Architecture](#architecture)
4. [Technologies and Models Used](#technologies-and-models-used)
5. [Approach and Workflow](#approach-and-workflow)
6. [Deployment and Integration](#deployment-and-integration)
7. [Setup and Installation](#setup-and-installation)
8. [Future Improvements](#future-improvements)
9. [License](#license)

---

## Project Overview

The **Pesport Multi-Modal Agent** is an AI-based system designed to engage users in real-time within the Pesport gaming app. By supporting text, image, and voice inputs, the agent offers a rich, multi-faceted experience. Each model is strategically selected and integrated to meet specific needs:
- **Text-based interactions** are handled by OpenAI’s **GPT-4**, providing conversation and information-based responses.
- **Image generation** is managed by **DALL·E**, creating custom visuals based on text prompts from users.
- **Voice inputs** are processed by **Whisper**, converting spoken language into text for further processing.

Together, these models enable a dynamic user experience, where users can interact via chat, voice, or image, making the gaming experience more immersive.

---

## Features

- **Chat Completion (Text)**: Uses GPT-4 to provide intelligent, natural responses to user inquiries within the game.
- **Text-to-Image Generation**: DALL·E converts user text prompts into images, offering a creative visual element for user engagement.
- **Voice-to-Text Conversion**: Whisper transcribes spoken user inputs into text, making hands-free interaction possible.
- **Ambiguous Input Handling**: For inputs containing both text and image, GPT-4 focuses only on text processing to prioritize clarity.

Each feature has been designed with the gaming user experience in mind, providing users with new ways to interact, explore, and personalize their experience.

---

## Architecture

The architecture of the **Pesport Multi-Modal Agent** follows a modular design. Each model endpoint was deployed on Azure AI Studio and accessed via dedicated APIs. The agent system can manage multiple models simultaneously, allowing for smooth switching between input types.

### Key Components:
1. **Input Processor**: Determines the type of input (text, voice, or image) and routes it to the corresponding model.
2. **API Endpoints**: Separate endpoints for GPT-4, DALL·E, and Whisper ensure that each model operates independently and efficiently.
3. **Backend Integration**: APIs were supplied to backend engineers to facilitate integration with the gaming app’s interface.
4. **Ambiguity Handler**: Manages cases where input contains multiple formats, ensuring clear processing priorities.

---

## Technologies and Models Used

- **Azure AI Studio**: Deployment and management of all model endpoints.
- **GPT-4 (OpenAI)**: Handles text-based chat interactions.
- **DALL·E (OpenAI)**: Manages text-to-image generation.
- **Whisper (OpenAI)**: Converts voice inputs to text for seamless interaction.
- **Flask**: Used as the backend framework to host and manage API endpoints.

---

## Approach and Workflow

1. **Model Selection**: Chose OpenAI models for their advanced capabilities in handling text, image, and voice processing.
2. **Development and Testing**: Each model was trained and tested separately to ensure compatibility and accuracy in predictions and responses.
3. **Endpoint Deployment**: Deployed model endpoints on Azure AI Studio, making each accessible through APIs.
4. **Backend Integration**: Collaborated with backend engineers to integrate API endpoints within the gaming app’s user interface.
5. **Ambiguity Resolution**: Implemented logic to handle cases where inputs contain multiple formats, with a preference for text when both text and image are present.

### Workflow Diagram
1. **User Input** → 2. **Input Detection** → 3. **Model Routing** → 4. **Model Processing (GPT-4/DALL·E/Whisper)** → 5. **Output Delivery in App**

---

## Deployment and Integration

All model endpoints are hosted on **Azure AI Studio** and made accessible to the Pesport backend through secured APIs. 

### Steps:
1. **Deploy Models**: Each model (GPT-4, DALL·E, Whisper) was deployed as a separate endpoint.
2. **API Integration**: API endpoints were shared with backend developers for direct integration within the app’s frontend.
3. **Testing and Debugging**: Extensive testing was conducted to ensure model accuracy and app compatibility, with adjustments made based on user input scenarios.

---

## Setup and Installation

1. **Clone Repository**:
   ```bash
   git clone https://github.com/Cemaster016/pesport-multimodal-agent.git
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Environment Variables**: Set up API keys and endpoint URLs for Azure AI Studio in a `.env` file.
4. **Run Application**:
   ```bash
   python app.py
   ```

---

## Future Improvements

- **User Feedback Loop**: Incorporate a feedback mechanism to allow users to rate interactions, enhancing model training.
- **Enhanced Ambiguity Handling**: Expand logic to manage additional types of ambiguous inputs.
- **Extended Multilingual Support**: Implement additional language support within the Whisper model for a broader user base.



