# PMiP Conference Website
### 20th Anniversary — Project Management in Practice
**Boston University Metropolitan College · Department of Administrative Sciences**

---

## Overview

This is the official website for the annual **Project Management in Practice (PMiP) Conference** at Boston University's Metropolitan College. The site serves as the central digital hub for conference information, attendee engagement, speaker profiles, registration, and stakeholder communication.

This project was developed as part of a BU IT Project & Product Management course (Milestone 2).

- **Conference Date:** November 6, 2026
- **Theme:** AI-Powered Project Management
- **Venue:** TBD — Center for Computing & Data Sciences or 1010 Commonwealth Ave, Boston, MA
- **Contact:** yolandat@bu.edu

---

## File Structure

```
/pmip-conference-website
  index.html              → About page (homepage)
  vanguard-forum.html     → 20th Anniversary Vanguard Forum
  announcements.html      → Announcements & Updates
  registration.html       → Registration & Call for Papers
  agenda.html             → Conference Agenda
  speakers.html           → Speakers & Profiles
  industry-board.html     → Industry Board
  contact.html            → Contact
  README.md               → This file
  /templates
    template.html         → Master page template for building new pages
```

---

## How to Update for a New Conference Year

Each page contains a **Conference Configuration block** at the top of the `<head>` section. This is the **only place** you need to update year, date, theme, and venue information.

```javascript
const CONFERENCE = {
  year:        "2026",         // ← Update to new year
  theme:       "AI-Powered Project Management", // ← Update theme
  date:        "November 6, 2026",  // ← Update date
  venue:       "Boston University...", // ← Update if venue changes
  format:      "In-person · Open to Registrants",
  hostedBy:    "Dept. of Administrative Sciences, BU MET",
  registerURL: "registration.html"
};
```

Update this block in each page file and the Event Details sidebar will reflect the changes automatically.

### Using AI to Update for a New Year

You can also feed any page to an AI tool (e.g. Claude Code, ChatGPT, Gemini, etc...) with the following prompt:

> *"Update this HTML file for the [YEAR] PMiP Conference. The new date is [DATE], theme is [THEME], and venue is [VENUE]. Update the CONFERENCE config block and any hardcoded references throughout the page."*

---

## How to Add a New Page

1. Copy `/templates/template.html` and rename it (e.g. `newpage.html`)
2. Update the `<title>` tag
3. Set `class="active"` on the matching nav link
4. Customize the hero banner (eyebrow, headline, subtext, pills)
5. Build your content in the `main-col` div
6. Save and test in a browser before committing

---

## How to Run Locally

No server required. Just open any `.html` file in a browser:

- Double click the file in Finder or File Explorer
- Or in VS Code: right click → **"Open in Default Browser"**

All pages must be in the same root folder for navigation links to work correctly.

---

## Git Workflow

- **Never push directly to `main`**
- Use feature branches for new changes
- Test locally before committing changes
- Open a Pull Request and merge into `main` after testing

---

## Team

| Name | Role | Contributions |
|------|------|---------------|
| Sherif Errefae | Project Manager | Agenda, Contact, Industry Board, Vanguard Forum, Speakers |
| Pedro Almeyda | QA / Engineer Lead | Template, Prompts, Homepage, Registration, Announcements, README, GitHub Repository |
| Andre Bet-Warda | Team Member | Burnup Chart |
| Stephanie Pollich | Team Member | Conclusions, Resource Management |
| Prof. Vijay Kanabar | Professor & Project Sponsor |

---

## Tools Used

- **Claude AI** — AI-assisted development and prompt engineering
- **ChatGPT** - brainstorming, proofreading, and content refinement
- **VS Code** — Code editor / IDE
- **GitHub** — Version control and repository hosting
- **Eventbrite** — Conference registration (link TBD)
- **Slack / Google Drive / Zoom** — Team collaboration and communication

---

## Notes

- Eventbrite registration link will be added to `registration.html` once available
- Venue to be confirmed between CCDS ("Jenga building") and 1010 Commonwealth Ave

---

*Prototype — BU MET IT Project & Product Management Course · June 2026*
