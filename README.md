# 🤖 AI Code Review Bot — by Samiul Islam

A GitHub Actions bot that automatically reviews pull requests using Google Gemini
and posts the review as a PR comment.

---

## 🚀 How it works

1. A pull request is opened (or updated) against `main`.
2. The workflow in `.github/workflows` triggers.
3. `review.py` (stdlib-only, no dependencies) sends the diff to Gemini.
4. The AI review is posted on the PR as a comment.

Smart retries: backs off on rate limits / server errors and falls back to a
secondary model; fails fast on auth errors.

---

## ⚙️ Setup

1. Fork or use this repo.
2. Add your Gemini API key as a repository secret named `GEMINI_API_KEY`
   (Settings → Secrets and variables → Actions).
3. Open a pull request — the bot reviews it automatically.

## 🧪 Test

```bash
python test_review.py
```

---

*Made by [Samiul Islam](https://github.com/samiul14)*
