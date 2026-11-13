# Swedish Learning App (Clock Game)

A gamified language-learning app for mastering Swedish time expressions (klockan), built as a full-stack desktop application.

## What it does

- **Gamified learning** — clock-based quiz with lives, scoring, and progressive levels.
- **Adaptive difficulty** — levels advance based on the player's score, so questions scale with mastery.
- **Full-stack persistence** — user accounts, session login, game progress, leaderboard (top 5), and words-learned stats, persisted via a MySQL backend.

## Architecture

| Layer | Module | Role |
|---|---|---|
| UI | `ui.py` | Tkinter interface |
| Game logic | `game_logic_connector.py` | lives, score, level progression, answer validation |
| Backend connector | `backend_connector.py` | interface to backend API |
| Backend | `backend/backend_API.py`, `storage.py`, `user_management.py` | MySQL persistence, user/session/leaderboard |
| Content | `backend/PopulateDBWords.py`, `source/fetchQA/` | question bank |

## Tech stack

Python 3.10 · Tkinter · Pillow · MySQL · unittest

## Run & test

```bash
pip install -r requirements.txt
python -m source.main   # run
python -m unittest      # test
