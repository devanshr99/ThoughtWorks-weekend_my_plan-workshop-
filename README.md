# ThoughtWorks - Plan My Weekend Workshop

An AI-powered weekend planner built using **Google Agent Development Kit (ADK)**, **Gemini Flash**, and vector embeddings.

## Project Structure

```
thoughtsworks/
├── plan_my_weekend/
│   ├── data/
│   │   └── weekend_data.json       # Curated activities and weekend spots
│   ├── scripts/
│   │   └── ingest.py               # Vector embedding generation & MongoDB ingestion
│   ├── .env.example                # Example environment variables
│   ├── .gitignore                  # Folder-level git ignore
│   ├── __init__.py
│   └── agent.py                    # Google ADK agent definition
├── .gitignore
├── requirements.txt
└── README.md
```

## Setup & Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/devanshr99/ThoughtWorks-weekend_my_plan-workshop-.git
   cd ThoughtWorks-weekend_my_plan-workshop-
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python -m venv .venv
   # Windows:
   .venv\Scripts\activate
   # macOS/Linux:
   source .venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables:**
   Copy `plan_my_weekend/.env.example` to `plan_my_weekend/.env`:
   ```bash
   cp plan_my_weekend/.env.example plan_my_weekend/.env
   ```
   Fill in your API credentials:
   - `GOOGLE_API_KEY`: Your Gemini API key.
   - `MONGODB_URI`: Connection string for MongoDB (if using vector storage).

## Running the Project

- **Ingest weekend data & embeddings:**
  ```bash
  python plan_my_weekend/scripts/ingest.py
  ```

- **Run the Agent with Google ADK:**
  ```bash
  adk run plan_my_weekend
  # or launch web UI
  adk web plan_my_weekend
  ```