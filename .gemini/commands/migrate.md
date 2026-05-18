---
description: Safely create and apply Django migrations after model changes
---

Help me create and apply Django migrations for the Jayti project.

Steps:
1. Show me the current migration state: `python manage.py showmigrations`
2. Detect any model changes: `python manage.py makemigrations --check --dry-run`
3. If there are changes, generate the migration: `python manage.py makemigrations`
4. Show me the generated migration file so I can review it
5. Apply the migration: `python manage.py migrate`
6. Confirm success by running `python manage.py showmigrations` again

Important rules:
- Never squash or delete existing migration files
- If a migration touches the `core` app, double-check it doesn't break UserProfile
- If adding a field, always provide a default or `null=True, blank=True`
