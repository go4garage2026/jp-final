---
description: Scaffold a new Django feature module for Jayti (model + views + urls + template)
---

I want to add a new feature to the Jayti app. Scaffold it completely.

Please ask me for:
1. **Feature name** (e.g. "habits", "reading", "budget")
2. **What it does** in one sentence
3. **Key data fields** for the model

Then generate:

### 1. Django app skeleton
- `{name}/__init__.py`
- `{name}/models.py` — with `user = models.ForeignKey(User)` and sensible fields
- `{name}/apps.py`
- `{name}/admin.py`
- `{name}/views.py` — CRUD views with `@login_required`
- `{name}/urls.py`
- `{name}/migrations/0001_initial.py`
- `{name}/migrations/__init__.py`
- `{name}/tests.py`

### 2. Template
- `templates/{name}/{name}_list.html` — extending `base.html`, matching pink theme

### 3. Integration
- Add to `jaytipargal/settings.py` INSTALLED_APPS
- Add `path('{name}/', include('{name}.urls'))` to `jaytipargal/urls.py`
- Add nav link in `templates/base.html` sidebar
- Add dashboard card in `templates/core/dashboard.html`

### 4. Migration
- Run `python manage.py makemigrations {name}` and `python manage.py migrate`

Keep the design warm, personal, and consistent with the existing pink theme.
