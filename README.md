# Study Planner

> Turn exam dates and weak topics into a realistic day-by-day plan.

Hack Day Haldia x GRID community - 6-hour build challenge

**Repo:** `team-alpha` | **Stack:** Python / Flask | **Difficulty:** Medium-Hard | **Time:** 6 hours

## Brief
Students juggle many subjects at once. Build a planner that takes subjects, exam dates, difficulty and free hours per day, and produces a schedule that actually fits.

## Core tasks (must-do)
- [ ] Subjects with exam date, difficulty (1-5) and a topic list
- [ ] Daily available hours, including days off
- [ ] Scheduling logic: weight subjects by difficulty and days left, never exceed a day's capacity
- [ ] Week and day views of the plan
- [ ] Mark sessions done and show progress % per subject
- [ ] Automatic re-plan when sessions are missed
- [ ] Persist everything in SQLite (helper already in app.py)

## Bonus tasks (only after the core works)
- [ ] .ics calendar export
- [ ] Pomodoro timer inside each session
- [ ] Streaks and a weekly report chart
- [ ] Break a pasted syllabus into topics with an AI model

## What is already here
- `index.html` - base page that pings `/api/health`
- `app.py` - Flask app with a SQLite helper (`db()`, `init_db()`), `/api/health` and TODO endpoint stubs (they return 501 until you implement them)
- `requirements.txt` - `flask`, `gunicorn`

## Run locally
```bash
pip install -r requirements.txt
python app.py   # then open http://127.0.0.1:5000
```

## Deploy
Any Python host works (for example Render or PythonAnywhere). Start command: `gunicorn app:app`. Free hosts may reset the filesystem on restart, so the SQLite file can reset - fine for a demo.

## Suggested pacing
- Hour 1: read this README, agree on a plan and split the work
- Hours 2-4: build the core tasks
- Hour 5: integrate, polish, then bonus tasks if time allows
- Hour 6: deploy, open the Pull Request, submit on the MLH platform (OrganizerHQ)

## Submission checklist
- [ ] All core tasks work end to end
- [ ] Project is deployed and the live link opens
- [ ] Pull Request created on the Voyage GitHub repository assigned to your team
- [ ] Project submitted on the MLH platform (OrganizerHQ) - instructions are shared at the start of the event

## Rules
- Build new features on top of this starter project and integrate them.
- Teams of 3-4; every member must be present.
- AI tools and open-source / open-weight models are fully allowed.
