---
description: Deploy Jayti to Firebase Hosting + Google Cloud Run
---

Walk me through deploying the Jayti app to production.

## Pre-deploy checks
1. Run `ruff check .` — must be clean
2. Run `pytest tests -q --ignore=tests/e2e` — must pass
3. Run `python manage.py check --deploy --fail-level WARNING` with prod-like env — must show 0 issues
4. Show current git status — remind me to commit everything first

## Deploy steps
5. `git push origin main` — triggers Cloud Build automatically (show me the Cloud Build URL)
6. Monitor: `gcloud run services describe jayti --region=asia-south1 --format='value(status.url)'`
7. Health check: `curl https://jaytibirthday.in/health`

## Post-deploy verification
8. Check Cloud Run logs for errors: `gcloud run services logs read jayti --region=asia-south1 --limit=20`
9. Confirm static files are served: test a static URL
10. Summarise: deployed ✅ or issues found ❌

Firebase project: `jayti-c7605`
Cloud Run region: `asia-south1`
Service name: `jayti`
