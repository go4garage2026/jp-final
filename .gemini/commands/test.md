---
description: Run the full Jayti test suite (lint + unit tests + Django deploy check)
---

Run the complete test pipeline for the Jayti project in this order:

1. **Lint** — `ruff check .`
2. **Unit + smoke tests** — `DEBUG=True SECRET_KEY=dev LOG_TO_FILE=0 pytest tests -q --ignore=tests/e2e`
3. **Django deploy check** — `DEBUG=False SECRET_KEY=ci-key-long-enough-for-production ALLOWED_HOSTS=example.com LOG_TO_FILE=0 python manage.py check --deploy --fail-level WARNING`

Run all three commands, show the output of each, and summarise:
- ✅ passed / ❌ failed for each step
- Any errors with a brief explanation
- A recommended fix if something failed
