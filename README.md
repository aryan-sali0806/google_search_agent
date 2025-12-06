📘 Google Search Agent — Powered by Google ADK + Gemini 2.5

This project is a simple AI Agent built using the Google Agent Developer Kit (ADK).
The agent uses Gemini 2.5 Pro along with the Google Search Tool to fetch real-time information from the web and respond intelligently to user queries.

It supports:

🔍 Real-time Google Search

🤖 Intelligent responses using Gemini

🧠 Session-based conversations

⚡ Auto-generated UI via adk web

🐍 Fully async Python backend

🔧 Easy to extend with more tools

🚀 Features

Search-enabled AI assistant
The agent automatically decides when to call Google Search and blends the results into its response.

Auto UI with ADK
No frontend coding required — adk web launches a clean UI to interact with the agent.

Session-controlled conversations
The agent remembers context within a session using ADK’s InMemorySessionService.

Async execution
Fast and scalable thanks to asyncio + ADK runner.

🏗️ Tech Stack

Python 3.10+

Google ADK

Gemini 2.5 Pro

Google Search Tool

Async Runner

UV package manager (optional)

📂 Project Structure
.
├── main.py
├── pyproject.toml
├── uv.lock
├── .gitignore
└── .venv/             # Not committed to Git

🔧 Setup Instructions
1️⃣ Install Dependencies (using UV)
uv sync


or using pip:

pip install -r requirements.txt

🔑 API Key Setup

The ADK uses your Google AI Studio API key.

PowerShell (Windows)
$env:GOOGLE_API_KEY="YOUR_KEY_HERE"

macOS/Linux
export GOOGLE_API_KEY="YOUR_KEY_HERE"


⚠️ Never commit your API key to GitHub.

▶️ Running the Agent (Backend)

To run the agent directly:

uv run python main.py


Or with plain Python:

python main.py


This will run a sample prompt:

what's the latest ai news?

💬 Launching the Auto-Generated UI

The ADK provides a built-in UI for interacting with your agent:

adk web --port 8000


Then open:

http://localhost:8000


This UI connects to your backend and allows you to chat with your agent in real time.

🧠 How It Works (Summary)

You type a query in the ADK UI.

The UI sends the query → your local ADK backend.

ADK Runner sends the message to the Gemini model.

If needed, Gemini triggers the Google Search Tool.

Search results are returned → sent back into the model.

Gemini generates the final answer.

UI displays the response.

🧰 Want to Extend the Agent?

You can add more tools:

tools=[google_search, my_custom_tool]


Or change the model:

model="gemini-2.5-flash"


ADK makes it super easy to add multi-step workflows, toolchains, and advanced logic.

📜 License

This project follows the Apache 2.0 License, as provided in the source templates from Google ADK.

🙌 Credits

Built using:

Google Agent Developer Kit

Gemini AI models

Google Search Tool

Open-source examples from Google ADK templates
