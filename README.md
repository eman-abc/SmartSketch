# SmartSketch
Turn descriptions into faces: a conversational AI for forensic sketches, missing person reconstructions, and creative edits.

Conversational AI for Facial Image Generation and Editing (FYP – In Progress)
This project is our Final Year Project (FYP) at NUST SEECS. It focuses on developing a conversational system that can generate, modify, or sketch human faces based on natural language descriptions.

The system integrates LangChain for conversational memory and decision routing, diffusion-based models (Stable Diffusion, InstructPix2Pix, ControlNet) for image generation and editing, and a web-based chat-style interface.
The solution is designed for three primary use cases:

> Criminal sketch generation
> Missing person reconstruction
> General public image enhancement

Problem Statement
> The process of creating facial representations from verbal descriptions is often slow, subjective, and resource-intensive, particularly in forensic contexts.
> Although generative AI models can produce realistic faces, existing tools are often too technical, lack conversational interfaces, and are not specialized for law enforcement applications.

This project addresses these challenges by providing:

> Natural language interaction suitable for non-technical users
> Conversational memory for iterative refinements
> Multi-modal capabilities (text-to-image, image-to-image, and sketch generation)

System Pipeline: Step-by-Step Flow

User Interaction (Frontend)
  Web application built with Streamlit or React/Django
  Option to upload an image and enter a prompt
  Real-time image updates displayed in a chat-like interface

LangChain Core (Backend Processing)
  Memory: Tracks previous user instructions (e.g., "make him older" → "add sunglasses")
  PromptTemplate: Converts user input into structured prompts for models
  Tool Agent: Selects whether to generate a new face, edit an image, or produce a sketch

Image Models
  Text-to-Image:	Stable Diffusion 1.5 (HF)	Generate new faces from scratch
  Image Editing:	InstructPix2Pix / ControlNet	Add or modify facial features
  Sketch Generation:	FLUX.1 / Sketchley	Produce grayscale sketches

FastAPI Backend
  Receives tool selection from LangChain
  Routes requests to the appropriate model
  Returns base64-encoded images to the frontend

Result Delivery
  Displays generated, edited, or sketched image in the chat interface
  Allows users to refine or download the results

Features
  Three operational modes: Criminal sketch, missing person reconstruction, and image editing
  Conversational memory for step-by-step modifications
  Integration of multiple generative and editing models
  Deployment options on local GPU or cloud platforms (Colab, HuggingFace Spaces, Replicate)

Technology Stack
  Frontend: Streamlit, React, or Django
  Backend: FastAPI, LangChain
  Models: Stable Diffusion, InstructPix2Pix, ControlNet, FLUX.1
  Deployment: HuggingFace Spaces, Colab, Local GPU
  Languages and Libraries: Python, NumPy, Pillow, Transformers

Project Timeline
> Phase	Milestone	Status
  1	Literature review and dataset preparation	Ongoing
  2	LangChain agent setup and model integration	Planned
  3	Frontend UI and API connection	Planned
  4	Optimization, testing, and deployment	Planned

Planned Repository Structure
(To be finalized as development progresses)
