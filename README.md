# Abhyas · अभ्यास

Personal UPSC answer-writing log. Every attempt. Every evaluation. One source of truth.

## What it is

A practice journal for your handwritten Mains answers — no matter where the question came from. PYQ, test series, teacher's question, mock, or random self-practice — they all live here with photos, scores, and feedback.

## What changed from Adarsh

Adarsh was meant to host topper copies. **Abhyas is for YOUR attempts only.** Topper copies live on upscpath (subscribed) or in your shared Drive. This app focuses on what only you can produce — your own writing practice + evaluations.

## Core flow

1. Write your answer on paper (set Bholwa Pomodoro 8 min).
2. Open Abhyas → tap **+** → fill source (PYQ / Test / Teacher / Mock / Random), paper, topic, question text.
3. **📷 Take photo** of each page → save.
4. Later, after teacher/self review → open that attempt → tap **+ Evaluation** → add score, comments, strengths tags, weaknesses tags, optional photos of marked copy.
5. Browse **Insights** tab to see your strengths and weaknesses patterns across all attempts.

## Source types

- 📘 **PYQ** — Previous Year Question
- 📝 **Test Series** — paid coaching test
- 👨‍🏫 **Teacher** — question given by a teacher
- 🎯 **Mock** — full-length mock test
- 🎲 **Random** — self-practice / from book / Telegram

Filter at home screen by source.

## v1 features

- Photo upload (camera or gallery), auto-compressed
- Question + answer + evaluation per attempt
- Strengths / weaknesses as comma-separated tags
- Insights view: aggregate tag frequency
- Saved / Recent / Source filter
- Search across all text (question, notes, evaluation)
- Light Anthropic-inspired theme

## v2 (when needed)

- Cloud sync via Supabase (same Gmail)
- Image storage in Supabase Storage (currently base64 in localStorage)
- Export as PDF (full practice log for revision)
- Charts: improvement over time per topic
- Cross-link to upsc-mains-pyq (when attempt is a PYQ)

## Deploy

Repo can be renamed from `adarsh` to `abhyas` on GitHub:
1. https://github.com/sauravanandb2w/adarsh/settings
2. Repository name field → change to `abhyas` → Rename
3. Update local remote:
   ```bash
   cd ~/Desktop/Health/adarsh
   git remote set-url personal https://github.com/sauravanandb2w/abhyas.git
   ```
4. GitHub Pages URL auto-updates to `sauravanandb2w.github.io/abhyas/`
5. Locally, optional: rename folder `adarsh` → `abhyas`

## Data migrates automatically

Existing Adarsh data in localStorage migrates on first load — only `type: "mine"` entries kept, with sensible defaults for source/date fields.
