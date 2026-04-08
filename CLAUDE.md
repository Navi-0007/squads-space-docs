# CLAUDE.md — squads-space-docs (Public Docs)

User-facing documentation for SquadsSpace, served via Mintlify.

**Stack:** Mintlify (docs.json config), MDX content, deployed to docs.squads-space.com.

---

## 1. Terminology — Use What Users See

All status names, button labels, and UI references MUST match what users see in the app.
The canonical source is `esports_frontend/utils/constants/ssot/labels/status-labels.ts`.

**Never use internal enum names in docs.** Use the display labels:

| Internal enum value | What to write in docs |
|--------------------|-----------------------|
| `DRAFT` | Draft |
| `PUBLISHED` | Published |
| `REGISTRATION` | Registration Open |
| `REGISTRATION_CLOSED` | Registration Closed |
| `IN_PROGRESS` | **Live** (not "In Progress") |
| `COMPLETED` | Completed |
| `CANCELLED` | Cancelled |
| `PAUSED` | Paused |

| Registration enum | What to write in docs |
|-------------------|-----------------------|
| `PENDING` | **Needs Approval** (not "Pending") |
| `CONFIRMED` | Confirmed |
| `PENDING_MEMBERS` | **Applied** (not "Pending Members") |
| `REJECTED` | Rejected |
| `CANCELLED` | Cancelled |
| `CLUB_CHECK_FAILED` | Club Check Failed |

| Match enum | What to write in docs |
|------------|-----------------------|
| `NOT_SCHEDULED` | Not Scheduled |
| `SCHEDULED` | Scheduled |
| `IN_PROGRESS` | **Live** (not "In Progress") |
| `COMPLETED` | Completed |
| `CANCELLED` | Cancelled |

---

## 2. Content Structure

```
getting-started/    # Onboarding for players and organizers
players/            # Player-facing guides
organizer/          # Organizer-facing guides
  ├── tournaments/
  ├── scrims/
  ├── running-matches/
  ├── live-streaming/
  ├── managing-players/
  └── founding-clubs/
```

Navigation is defined in `docs.json`. Only pages listed there are served.

---

## 3. Rules

1. **Simple English only.** No technical jargon, no enum values, no code references, no architecture terms.
   - Never say: OCR, SSE, WebSocket, API, endpoint, enum, SSOT, JWT, polling, real-time sync, server-sent events, presign, S3
   - Instead say: "notifications arrive instantly", "updates automatically", "live updates"
   - The screenshot-to-scores feature is called **"Smart Results"** — never "OCR"
   - See root `CLAUDE.md` Section 2 for the full feature naming table
2. **Match the app UI.** Button names, screen titles, and flow descriptions must match what users actually see.
3. **No internal terminology.** Use what the user sees on screen, not what developers call it internally.
4. **MDX format.** Use Mintlify components (Callout, Steps, Tabs) where helpful.
5. **One topic per page.** Keep pages focused and under 100 lines where possible.
5. **Link related pages.** Every page should have a "Related" section at the bottom.
6. **Test flows against the app.** Before publishing, verify that described steps match the actual UI.
