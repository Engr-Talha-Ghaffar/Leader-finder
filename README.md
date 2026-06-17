# Lead Finder CRM v3 Professional

Lead Finder CRM v3 is a local Flask dashboard for finding Google Maps leads, validating contact data, scoring lead quality, managing campaigns, tracking follow-ups, auditing websites, and exporting outreach-ready reports.

## Main Features

- Google Maps lead collection by business type + city
- Phone validation and Pakistan-friendly normalization
- Email detection from audited websites
- Website quality checker: SSL, speed, mobile viewport, contact form, WhatsApp button, availability
- Social media detection: Facebook, Instagram, LinkedIn, TikTok, YouTube
- Lead scoring: High / Medium / Low
- Suggested offer: Website Setup, Website Redesign, GBP Optimization, Social Media Setup, Website + SEO
- Campaign management
- Follow-up dashboard
- Activity timeline for each lead
- Personalized WhatsApp outreach message
- Proposal generator per lead
- Excel, CSV, and printable HTML reports
- Search history stored in SQLite
- Automatic database migrations for older v2 databases

## Installation on Windows

```bash
cd lead-finder-dashboard
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python -m playwright install chromium
python app.py
```

Open this URL in your browser:

```text
http://127.0.0.1:5000
```

## Important Notes

1. This project is designed for local/internal lead research and CRM workflow.
2. It does not bypass CAPTCHA or login walls. If Google shows a verification screen, solve it manually in the browser window.
3. Website audit needs internet access from your local computer.
4. Bulk spam is not recommended. The WhatsApp feature opens manual one-click outreach only.
5. For production/commercial scale, consider using an official Places API or compliant data provider.

## Pages

- Dashboard: search leads and view live stats
- All Leads: filters, lead details, website audit, proposal, CRM updates
- Hot Leads: high-scoring leads
- Follow Ups: due/overdue follow-up leads
- Campaigns: group leads into campaigns
- Reports: export Excel/CSV/HTML report

## Data Storage

Default database path:

```text
data/leads.db
```

Exports are saved in:

```text
exports/
```

## Clean Project Notes

The ZIP does not include `.venv`, `__pycache__`, browser binaries, or heavy cache folders. Create the virtual environment after unzipping.

## Login

The dashboard is protected with a fixed local login.

Default credentials:

- Username: `admin`
- Password: `admin123`

You can change them in `.env`:

```env
LOGIN_USERNAME=your_username
LOGIN_PASSWORD=your_password
```

After logout, all dashboard pages, API routes, and export links require login again.
