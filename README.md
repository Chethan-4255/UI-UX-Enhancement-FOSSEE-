# FOSSEE Workshop Booking — UI/UX Enhancement (Chethan Vasthaw Tippani)

Hi! I picked up the basic workshop booking site and gave it a modern, clean look with a dark theme that actually reads well on phones. I kept the structure and views intact; most edits are templates and CSS.

LinkedIn: https://www.linkedin.com/in/CHETHAN-VASTHAW  
Phone: +91 7013121524


## How to run (quick start)
1) Create venv and install deps
```
python -m venv .venv
.\.venv\Scripts\pip install -r requirements.txt
```
2) Run migrations
```
.\.venv\Scripts\python manage.py makemigrations cms
.\.venv\Scripts\python manage.py migrate
```
3) Start server
```
.\.venv\Scripts\python manage.py runserver
```
4) Optional — create admin user
```
.\.venv\Scripts\python manage.py createsuperuser
```


## What I changed (high level)
- New `workshop_app/static/workshop_app/css/theme.css` with a glassy dark theme, high-contrast text, and soft shadows.
- Updated `workshop_app/templates/workshop_app/base.html` with cleaner navbar and hero; theme is included here.
- Login and Register pages: centered cards, better spacing, mobile-first.
- Public Statistics page: filters card, tables, and dark-friendly charts.
- Activation page: removed bright jumbotron; now a dark glass card.
- Subtle micro-animations on cards and buttons.

### Admin theming
- Added `workshop_portal/templates/admin/base_site.html` to inject a custom stylesheet.
- Added `workshop_app/static/workshop_app/css/admin_theme.css` to theme Django admin with the same dark palette.

## Design principles
- Readability first: good contrast, calmer colors, and generous spacing.
- Reduce friction: obvious actions, bigger tap targets, fewer borders/lines.
- Familiar components: Bootstrap semantics kept, so it’s easy to follow.
- Progressive enhancement: if custom CSS fails, the site still works.


## Responsiveness
- Navbar toggler visible on dark, layout stacks nicely on mobile.
- Tables get clearer headers and hover to help scanning on small screens.
- Chart dialog and axes recolored for dark backgrounds.


## Trade‑offs
- Picked dark theme for comfort; screenshots on dark backgrounds need care.
- Kept Bootstrap instead of heavier JS frameworks to keep the app fast.
- Light animations only; no heavy libraries, so performance stays snappy.


## Most challenging part
Making every state (dropdowns, dialogs, table headers, form errors) readable in dark without missing tiny details. I audited components and added overrides where needed. Iterated until no “washed out” text remained.


## Screenshots (before ➜ after)
- Login: docs/before_login.png ➜ docs/after_login.png
- Stats: docs/before_stats.png ➜ docs/after_stats.png
- Activation: docs/before_activation.png ➜ docs/after_activation.png
