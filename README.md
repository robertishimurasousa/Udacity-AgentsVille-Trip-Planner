# Prompting for Effective LLM Reasoning and Planning

This repository tracks coursework for **Prompting for Effective LLM Reasoning and Planning (CD14526)**, the first course in Udacity's **Agentic AI Nanodegree (ND900)**. The exercises build from role-based prompts to tool use, structured prompt chains, and feedback loops. The course concludes with the AgentsVille Trip Planner. [Course outline](https://www.udacity.com/course/prompting-for-effective-llm-reasoning-and-planning--cd14526) · [Nanodegree overview](https://www.udacity.com/course/agentic-ai--nd900)

## Lessons and exercises

Open each guide to find its starter and solution notebooks. Try the starter first, then compare your approach with the reference solution.

| Topic | What to practice |
| --- | --- |
| [Introduction](introduction-to-prompting-for-llm-reasoning-and-planning/README.md) | Explore the prompting environment and compare model choices. |
| [Role-based prompting](Lessons/lesson-1-role-based-prompting/exercises/README.md) | Use a defined role to steer the model's voice and behavior. |
| [Chain-of-Thought and ReAct prompting](Lessons/lesson-2-chain-of-thought-and-react-prompting/exercises/README.md) | Compare guided reasoning with tool use across two exercises. |
| [Prompt instruction refinement](Lessons/lesson-3-prompt-instruction-refinement/exercises/README.md) | Refine roles, instructions, examples, and output formats. |
| [Chaining prompts for agentic reasoning](Lessons/lesson-4-chaining-prompts-for-agentic-reasoning/exercises/README.md) | Pass structured results between workflow steps. |
| [LLM feedback loops](Lessons/lesson-5-implementing-llm-feedback-loops/exercises/README.md) | Use evaluation feedback to improve successive model outputs. |

## Run the notebooks locally

From the repository root, create a Python 3.11 environment and install the [project dependencies](requirements.txt).

```sh
python3.11 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip install notebook==7.6.5
python -m notebook
```

In PyCharm, select the project's `.venv` interpreter and open the desired notebook. Check its setup cell for any exercise-specific dependencies or provider settings. Use the ignored `.env` or the kernel's environment for credentials, using [`.env.example`](.env.example) as a template. [Vocareum classroom configuration](https://help.vocareum.com/en/articles/9341351-genai-in-vocareum-labs)

## Assessed project

**AgentsVille Trip Planner** turns traveler preferences, dates, and a budget into a structured `TravelPlan`. It uses simulated forecasts and activities, then uses a ReAct loop to revise the itinerary. The notebook evaluates the original plan and the revised candidate before the final tool returns the approved result.

Place the AgentsVille classroom files `project_starter.ipynb` and `project_lib.py` in the local `Project/` directory. The repository keeps these classroom files local. Run the notebook with `Project/` as its working directory so it can import the helper. Supply credentials in `Project/.env` or through the kernel environment.

For submission, follow the classroom rubric and upload a ZIP containing the completed notebook and helper at the archive root. Keep credentials and the virtual environment outside the ZIP. [Udacity submission checklist](https://support.udacity.com/hc/en-us/articles/47406875454477-How-to-Submit-your-Project-Successfully-Checklist)

## Contributions and attribution

Use English for documentation, code comments, commits, pull requests, and reviews. Exercise materials come from Udacity. [Upstream materials](https://github.com/udacity/cd14526-Effective-Prompting-AgenticAIC1-exercises) · [License](LICENSE.md) · [Security policy](SECURITY.md)
