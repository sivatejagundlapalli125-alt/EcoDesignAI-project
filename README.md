# EcoDesignAI

AI-powered eco-design: compare sustainable materials and visualize greener product concepts.

## What it does

- Recommends product materials using the sustainability engine and its materials dataset.
- Provides a Flask web app with account registration, login, and a design studio.
- Generates product concept images with OpenAI's image API using `gpt-image-1.5`.

## Project structure

- `chatbot/` — Flask app, templates, browser assets, and Python dependencies.
- `image/` — image prompts and OpenAI image generation.
- `sustainability_engine/` — material filtering and sustainability decisions.

## Run locally on Windows

Use Python 3.10 or newer. From the project root in PowerShell:

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
py -m pip install -r chatbot\requirements.txt
$env:OPENAI_API_KEY = "your-api-key"
$env:FLASK_SECRET_KEY = "use-a-long-random-secret"
py chatbot\app.py
```

Then open [http://127.0.0.1:5000](http://127.0.0.1:5000) and create an account.

## API key and local data

Image generation requires an OpenAI API key with access to the image model and sufficient API credits. API usage may incur charges; GitHub does not provide API credits.

Keep your key in a local environment variable or a local `.env` file in the project root. Never commit the key. The repository's `.gitignore` excludes `.env`, the local SQLite database, and virtual environments.