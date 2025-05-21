# VibeCheck – Team Sentiment AI via Slack

VibeCheck is a lightweight, privacy-conscious Slack bot that uses AI to help teams stay emotionally aligned. It asks a weekly check-in question, analyzes responses with NLP models from Hugging Face, and summarizes the team’s mood for managers—no clunky dashboards or invasive surveys required.

Demo
Coming soon: [Demo video link or animated GIF showing check-in → response → summary]

Problem Statement: Remote and hybrid teams often miss emotional cues that affect productivity, culture, and burnout. Existing solutions are too heavy or intrusive.

Solution

A Slack-native assistant that:
- Prompts each team member once a week for a quick written check-in
- Analyzes sentiment and emotions using Hugging Face models
- Generates a weekly team-level summary for managers
- Stores anonymized results for long-term trends

Tech Stack

| Layer        | Tool / Service |
|--------------|----------------|
| Bot Platform | Slack API + Bolt for Python |
| NLP          | Hugging Face Transformers (`sentiment-analysis`, `emotion classification`) |
| Backend      | Python + FastAPI |
| Storage      | Supabase (PostgreSQL + Auth) |
| Optional UI  | Streamlit dashboard or Chart.js for Phase 2 |
| Deployment   | Render.com or Railway.app |

Core Features

- `/checkin` command or weekly auto-DM
- NLP analysis of user responses
- Team sentiment/emotion rollup
- Privacy-first: No storing full names or messages without consent
- Weekly Slack post with visual summary

Sample Output

> _“This week, 67% of team members expressed neutral or positive emotions. Most frequent emotions were ‘motivated’ and ‘overwhelmed’. Compared to last week, positivity is up by 12%.”_

Future Roadmap

- [ ] Admin dashboard with trends
- [ ] Opt-in journaling mode
- [ ] Burnout risk alerts
- [ ] Integration with Google Calendar (energy-aware scheduling)

Running Locally

```bash
git clone https://github.com/yourname/vibecheck.git
cd vibecheck
pip install -r requirements.txt
ngrok http 3000  # for local Slack testing
