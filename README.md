# Ai-Requirements-to-code-generato
Based on the uploaded project, this is an **AI Requirements-to-Code Generator** built with **Streamlit + Groq**. It takes natural language software requirements and automatically generates software architecture, UML diagrams, ERDs, and starter code using an LLM. The UI also supports iterative refinement and PlantUML visualization. 

---

# Req2Code – AI Requirements to Code Generator

This is an **AI-powered software engineering assistant** that transforms natural language software requirements into structured software architecture, UML diagrams, ER diagrams, and production-ready code skeletons.

It is designed for **students, software engineers, educators, system analysts, and developers** who want to rapidly convert software requirements into an initial design and implementation blueprint.

---

## Live Demo

**Deployed App:** Req2Code – AI Requirements to Code Generator

---

# What Problem Does It Solve?

Software development usually begins with requirement analysis and system design.

Developers often spend significant time:

* understanding requirements,
* identifying entities and relationships,
* creating UML diagrams,
* designing databases,
* preparing architecture,
* and writing initial boilerplate code.

This AI-powered application automates these early software engineering tasks by:

* accepting software requirements in natural language,
* extracting system entities and relationships,
* generating UML diagrams,
* producing ER diagrams when needed,
* generating a code skeleton in the selected programming language,
* allowing iterative refinement through conversational feedback.

This significantly accelerates the software design phase before implementation begins.

---

# Features

* Natural language software requirement analysis
* AI-powered software architecture generation
* Automatic entity extraction
* Relationship identification
* Constraint extraction
* Interactive UML generation including:

  * Class Diagram
  * Sequence Diagram
  * State Machine Diagram
* Automatic ER Diagram generation when persistent storage is required
* PlantUML source generation
* Live PlantUML rendering
* Multi-language code skeleton generation
* Supported languages:

  * Python
  * Java
  * C++
  * JavaScript
  * TypeScript
  * Go
  * Rust
* Interactive architecture refinement using conversational feedback
* Luxury dark-themed Streamlit interface
* Session state management
* Raw JSON inspection mode
* Error handling and JSON recovery for unreliable AI outputs

---

# AI Feature

The application uses a Large Language Model through the **Groq API** to perform software architecture generation.

The AI performs the following workflow:

* analyzes the software requirements,
* identifies entities,
* extracts relationships,
* determines software constraints,
* generates PlantUML diagrams,
* creates ER diagrams,
* generates an initial code skeleton,
* returns everything as structured JSON.

The application also supports iterative refinement by allowing users to provide feedback, after which the AI regenerates the architecture while preserving the existing design. 

---

# How the AI Works

The user enters software requirements.

The application sends the requirements to the Groq LLM together with a strict system prompt.

The model is instructed to:

* return valid JSON only,
* identify entities,
* generate UML diagrams,
* generate ER diagrams,
* create a code skeleton,
* avoid markdown,
* avoid explanations,
* produce syntactically valid PlantUML.

The application then:

* validates the returned JSON,
* repairs malformed JSON when possible,
* renders PlantUML diagrams,
* displays the generated architecture,
* enables iterative refinement through user feedback. 

---

# Full System Prompt

The AI is instructed to:

* Parse software requirements.
* Return valid JSON only.
* Extract:

  * entities
  * relationships
  * constraints
  * class diagram
  * sequence diagram
  * state machine
  * ER diagram
  * code skeleton
* Produce valid PlantUML.
* Generate code in the selected programming language.
* Make reasonable assumptions for incomplete requirements.
* Never output markdown or additional explanations. 

---

# Tools, Services, and Models Used

## Development

* Python
* Streamlit

## AI

* Groq API
* Llama 3.3 70B Versatile

## Diagram Rendering

* PlantUML

## Libraries

* Pillow
* httpx

---

# Environment Variables

Configure the following secret:

```env
GROQ_API_KEY=your_api_key
```

---

# AI Model

Primary Model:

* llama-3.3-70b-versatile

---

# Deployment

* Hugging Face Spaces

---

# How It Works

1. User enters software requirements.
2. The AI analyzes the requirements.
3. Entities and relationships are extracted.
4. UML diagrams are generated.
5. ER diagram is generated if required.
6. Code skeleton is generated in the selected language.
7. PlantUML diagrams are rendered.
8. User can provide additional feedback.
9. The AI regenerates the architecture accordingly. 

---

# Screenshots

Screenshots of Project, for example:

### 1. Main Interface

Main Screen

### 2. Generated Software Architecture

Overview

### 3. UML Diagrams

Class Diagram

Sequence Diagram

State Machine Diagram

### 4. ER Diagram

Database Design

### 5. Generated Code Skeleton

Starter Code

### 6. AI Refinement Chat

Architecture Refinement

---

# How to Run the Project

## Prerequisites

* Python 3.10
* Groq API Key

---

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/Req2Code.git
cd Req2Code
```

---

### 2. Create a virtual environment

```bash
python -m venv venv
```

Linux/macOS

```bash
source venv/bin/activate
```

Windows

```bash
venv\Scripts\activate
```

---

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Configure API key

Create a `.env` file or configure Hugging Face Secrets:

```env
GROQ_API_KEY=your_groq_api_key
```

---

### 5. Run the application

```bash
streamlit run app.py
```

The application will open automatically at:

```
http://localhost:8501
```

This README is grounded in the uploaded source code and dependency files.
