# 💬 Simple Chainlit Chatbot

> A fast, minimal chatbot built with Chainlit, uv, and OpenAI Agents SDK—ideal for learning and prototyping LLM-based apps.

---

## 📌 Project Description

**Simple Chainlit Chatbot** is a lightweight and modular conversational application built with Chainlit, an open-source framework designed for creating LLM-powered interfaces. This project serves as an excellent starting point for developers looking to explore how Large Language Models (LLMs) like OpenAI's GPT can be integrated into user-friendly applications with minimal setup.

The chatbot leverages **Chainlit** for both the frontend and backend, allowing developers to quickly build and iterate on conversational logic with a reactive UI. With just a few lines of code, you can deploy an interactive chatbot capable of handling real-time user input.

To streamline development and dependency management, the project uses **uv**, a next-generation Python package manager. uv acts as a faster alternative to pip and venv, handling environment creation and package installation with impressive speed and efficiency. This significantly reduces the time needed to go from setup to execution.

Additionally, the project includes the **OpenAI Agents SDK** (`openai-agents`), a toolkit that enables the creation of task-based AI agents capable of reasoning, planning, and executing based on natural language instructions. While the initial implementation is simple, this SDK provides the foundation for future upgrades where agents can autonomously perform multi-step tasks.

---

## 🧰 Tech Stack

- [Chainlit](https://www.chainlit.io/) – LLM-powered frontend + backend framework
- [uv](https://github.com/astral-sh/uv) – Fast Python package manager & environment tool
- [OpenAI Agents SDK](https://platform.openai.com/docs/assistants/overview) – Toolkit for task-based AI agents (future-ready)

---

## 🚀 Setup Instructions

### 1. Initialize a New Chainlit Project

```bash
uv init chatbot
```
## 2. Navigate to the Project Folder
```
cd chatbot
```
## 3. Open the Project in VS Code (optional)
```
code .
```
## 4. Add Required Dependencies
```
uv add chainlit openai-agents
```
## 5. Create a Simple App File
```
import chainlit as cl

@cl.on_message
async def main(message: cl.Message):
    await cl.Message(
        content=f"Received: {message.content}",
    ).send()
```
## 6. Run the Application
```
uv run chainlit run app.py -w
```
