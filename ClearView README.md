# ClearView

**A weekly status hub for programs run in Azure DevOps (ADO).** Team members update their tasks in plain language. Project leads get a live program view, a timeline, a RAID log and a ready-to-present status deck, all rolled up from those updates.

> **Demo with fictional data.** Every company, person, project and work-item ID here is made up (*Harborline* is a fictional company). Nothing connects to a real ADO organization.

![Program view](screenshots/program-view.png)

## What it does

| Tab | For | What it shows |
|---|---|---|
| **My work** | Team members | The tasks you need to update this sprint, with guided steps and a speak-to-type option |
| **Program view** | Project leads | Workstreams with on track / at risk / off track status worked out from task data, plus a "heads up" list of what needs attention |
| **Timeline** | Everyone | Sprint or waterfall view of Epics → Features → Stories → Tasks, with progress fill and a today line |
| **RAID log** | Project leads | Risks, assumptions, issues and decisions, each tied to a task |
| **Status deck** | Leadership | A slide-by-slide status report (timeline, program summary, one slide per workstream), with a copy-to-email summary |
| **Settings** | Admins | Roles (Admin, Project Lead, Team Member, Viewer), sharing and reminders |

## How status is worked out

Each workstream's status comes from its tasks rather than being typed in:

- **Off track:** overdue tasks, or a large share of unassigned or not-started work in the current sprint
- **At risk:** sprint tasks not yet started, or work that is starting to slip
- **On track:** nothing blocked, overdue or unassigned

## Screenshots

| My work | Timeline | Status deck |
|---|---|---|
| ![My work](screenshots/my-work.png) | ![Timeline](screenshots/timeline.png) | ![Status deck](screenshots/status-deck.png) |

## Running it

No build step and no dependencies. It's one self-contained HTML file.

```sh
# open directly
open index.html

# or serve it
python3 -m http.server 8000   # then visit http://localhost:8000
```

Use **Signed in as** in the header to switch between people and see each role's view.

## Built with

Plain HTML, CSS and JavaScript in a single file. No framework. Browser storage keeps per-viewer settings.
