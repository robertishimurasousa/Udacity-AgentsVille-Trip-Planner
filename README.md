# AgentsVille Trip Planner

AgentsVille Trip Planner is the first assessed project in Udacity's **Agentic AI Nanodegree (ND900)**. The assignment calls for a Jupyter Notebook that plans a trip to a fictional city, evaluates the itinerary, and revises it using simulated weather and activity data. [Udacity program](https://www.udacity.com/course/agentic-ai--nd900)

This repository documents the local development setup. The classroom notebook supplies the application scaffold and the assignment TODOs.

## How the planner is designed

1. Validate traveler preferences, dates, and budget with `VacationInfo`. Use the trip dates to request weather and activity data.
2. Generate a daily itinerary as JSON and validate it against the notebook's `TravelPlan` model.
3. Evaluate constraints such as budget, dates, interests, and weather. Use a ReAct assistant to revise the plan. The assistant runs evaluations before finalizing the plan through `final_answer_tool`.

## Local setup

The local setup was verified with Python 3.11.18 and Jupyter Notebook 7.6.5. Download `project_starter.ipynb` and `project_lib.py` from the AgentsVille project workspace in the Udacity Classroom and place both files next to this README. Set the repository root as the notebook working directory.

```sh
python3.11 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip install notebook==7.6.5
python -m notebook project_starter.ipynb
```

In PyCharm, select the interpreter from `.venv`. The notebook contains an installation cell with the same six dependency pins.

## Model configuration

If needed, copy `.env.example` to `.env` and set `OPENAI_API_KEY` locally. Set `OPENAI_BASE_URL` to the classroom's Vocareum endpoint when using a classroom-issued key. Leave the variable unset for a direct OpenAI key. [Vocareum configuration](https://help.vocareum.com/en/articles/9341351-genai-in-vocareum-labs)

Replace the placeholder client setup in your local notebook with the cell below. It reads the key and endpoint together from the ignored `.env` in the notebook's working directory. The starter selects `gpt-4.1-mini` in the following cell.

```python
from dotenv import dotenv_values
from openai import OpenAI

settings = dotenv_values(".env", interpolate=False)
api_key = settings.get("OPENAI_API_KEY")
if not api_key:
    raise RuntimeError("Set OPENAI_API_KEY in the local .env file.")

client = OpenAI(
    api_key=api_key,
    base_url=settings.get("OPENAI_BASE_URL") or "https://api.openai.com/v1",
)
```

## Assignment and submission

Complete the notebook TODOs and use the classroom rubric to verify the itinerary prompt, weather evaluation, activity tool description, ReAct tool calls, and Pydantic validation. Run the final notebook in a fresh kernel and review the resulting itinerary and evaluations.

The classroom instructions specify uploading a ZIP with the code files. Include the completed notebook and required library files. Keep the local environment, credentials, and generated caches out of the archive. [Udacity submission checklist](https://support.udacity.com/hc/en-us/articles/47406875454477-How-to-Submit-your-Project-Successfully-Checklist)

## Contributions and course materials

Use English for repository documentation, code comments, commit messages, pull requests, reviews, and merge messages. Keep the source and rights notices for educational materials with the files they cover. [License and attribution](LICENSE.md) · [Security policy](SECURITY.md)
