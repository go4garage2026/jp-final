---
description: Diagnose a Django error, traceback, or unexpected behaviour in Jayti
---

I have an error in the Jayti app. Help me debug it.

Please:
1. Ask me to paste the full traceback or describe the symptom
2. Identify which Django app and view is involved
3. Read the relevant source files to understand the code
4. Explain the root cause clearly
5. Provide a specific fix with the exact code change needed
6. Check if the fix might break any related functionality
7. Suggest a test to confirm the fix works

Context to keep in mind:
- Single-user app; auth issues are rare but check `@login_required` decorators
- Database is PostgreSQL in prod, SQLite in dev — some queries behave differently
- AI features gracefully degrade if API keys are missing
- The astro module (pyswisseph) can fail silently if ephemeris data is unavailable
