# Screenshot Guide

How to add screenshots to the SquadsSpace docs.

## Team workflow

1. Take the screenshot (see tables below for exactly what to capture)
2. Name it **exactly** as listed in the Filename column
3. Upload to S3 at `squad-space/public-assets/public-docs/[folder]/[filename]`
4. Done — docs pick it up automatically. No code changes needed.

## S3 bucket structure

```
s3://squad-space/public-assets/public-docs/
├── getting-started/
├── players/
└── organizer/
    ├── dashboard/
    ├── tournaments/
    ├── matches/
    ├── groups/
    ├── live-scoring/
    ├── overlays/
    ├── scrims/
    └── clubs/
```

Base URL: `https://squad-space.s3.ap-south-1.amazonaws.com/public-assets/public-docs`

---

## Getting Started

**Upload to:** `public-assets/public-docs/getting-started/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `become-organizer-landing.png` | The "Become Organizer" landing page | `/organizer/register` |
| `organizer-dashboard-first-view.png` | Organizer Dashboard right after activation | `/organizer/[slug]` |

## Players

**Upload to:** `public-assets/public-docs/players/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `player-dashboard.png` | Player Dashboard — tournaments, clubs, quick actions | `/dashboard` |
| `all-tournaments-page.png` | All Tournaments with cards, filters, status badges | `/tournaments/p/all-tournaments` |
| `tournament-register-button.png` | Tournament page with Register/Join button in hero | Any tournament page |
| `registration-status-page.png` | Registration Status with requirements progress tracker | `/tournaments/p/[slug]/status` |
| `match-hub.png` | Match Hub — schedule, room credentials, match selector | Match Hub for any active tournament |
| `squad-page.png` | Squad page with members, invite code | `/squads` |
| `clubs-directory.png` | Clubs directory with club cards | `/clubs` |
| `profile-page.png` | Profile page — hero banner, tournaments, clubs | `/profile/[username]` |
| `notifications-page.png` | Notifications with tabs (All, Unread, Saved) | `/notifications` |

## Organizer Dashboard

**Upload to:** `public-assets/public-docs/organizer/dashboard/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `organizer-dashboard.png` | Organizer Dashboard — club details, quick actions, tournaments | `/organizer/[slug]` |
| `tournament-dashboard.png` | Tournament Dashboard with tabs (Overview, Roadmap, Registrations...) | `/organizer/[slug]/tournaments/[tSlug]` |

## Tournament Creation & Editing

**Upload to:** `public-assets/public-docs/organizer/tournaments/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `create-wizard-overview.png` | Creation wizard with Step 1 visible | `/organizer/[slug]/tournaments/create` |
| `create-step1-details.png` | Step 1: Tournament Details — name, format, schedule, requirements | Same page, Step 1 |
| `create-step2-game-config.png` | Step 2: Game Configuration — scoring, platforms | Same page, Step 2 |
| `create-step3-review.png` | Step 3: Review & Create summary | Same page, Step 3 |
| `edit-accordion-sections.png` | Edit page with expandable accordion sections | `/organizer/.../edit` |
| `edit-locked-field-badge.png` | A locked field showing red/amber badge (hover for tooltip) | Same page, hover on locked field |

## Roadmap Builder

**Upload to:** `public-assets/public-docs/organizer/tournaments/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `roadmap-empty-configure.png` | Roadmap tab before configuration — "Configure" button | Tournament Dashboard → Roadmap tab |
| `roadmap-stages-configured.png` | Complete roadmap with 2-3 stages | Roadmap Builder with stages filled |
| `roadmap-stage-editor.png` | One stage being edited — entrants, group size, qualifiers | Stage editor in builder |
| `roadmap-published.png` | Published roadmap with "Manage" buttons | Roadmap tab after publishing |
| `roadmap-poster-templates.png` | Poster template gallery (Neon, Nebula, Inferno, Phantom) | Poster image creation page |
| `roadmap-poster-preview.png` | Poster preview before download | Same page, preview mode |

## Registrations

**Upload to:** `public-assets/public-docs/organizer/tournaments/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `registrations-page.png` | Registrations tab with filters and cards | Tournament Dashboard → Registrations |
| `registration-detail-panel.png` | Detail panel — team info, members, requirements | Click any registration |
| `registrations-bulk-actions.png` | Multiple selected with bulk action buttons | Select 3+ registrations |
| `registration-modes-selector.png` | Registration mode selection in creation wizard | Tournament creation Step 1 |

## Status Control & Export

**Upload to:** `public-assets/public-docs/organizer/tournaments/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `status-control-transitions.png` | Status Control page — transition cards | Tournament Dashboard → Status |
| `status-control-risk-level.png` | Transition card showing risk level badge | Same page, any transition card |
| `export-modal.png` | Export modal — categories and format selection | Tournaments → Export |
| `point-table-config.png` | Point table — kill points + placement grid | Tournament creation Step 2 |

## Groups & Invited Slots

**Upload to:** `public-assets/public-docs/organizer/groups/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `auto-groups-config.png` | Auto-groups configuration — naming, seeding, fill | `/rounds/[round]/auto-groups` |
| `auto-groups-preview.png` | Group preview after "Preview Groups" | Same page, after preview |
| `groups-locked.png` | Groups page with lock indicators (green dots) | `/rounds/[round]/groups` |
| `groups-multi-swap.png` | Multi Swap view with teams selected | Same page, multi-select mode |
| `invited-slots-page.png` | Invited Slots — invite link, capacity, joined teams | `/rounds/[round]/invited-slots` |
| `invited-slots-link-actions.png` | Invite link with Copy, Rotate, Revoke buttons | Same page, link card |

## Match Management & Mass Operations

**Upload to:** `public-assets/public-docs/organizer/matches/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `group-match-page.png` | Group page — match selector, schedule, results | Any group page |
| `match-status-card.png` | Match status with action buttons (Start Match, etc.) | Group page, match selected |
| `results-entry-table.png` | Results entry — placement and kills columns | Group page → Results |
| `room-credentials-card.png` | Room ID & Password card (with lock icon if not started) | Group page → ID/Password |
| `mass-create-scheduling.png` | Mass Create — scheduling options (Parallel, Global, Same Time) | Mass Ops → Create, Step 3 |
| `mass-create-maps.png` | Mass Create — map selection | Mass Ops → Create, Step 4 |
| `mass-manager.png` | Mass Manager — bulk edit schedules | Mass Ops → Mass Manager |
| `mass-resultor.png` | Mass Resultor — score entry across groups | Mass Ops → Mass Resultor |

## Smart Results

**Upload to:** `public-assets/public-docs/organizer/matches/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `smart-results-upload.png` | Upload screen — file picker | Group page → Smart Results button |
| `smart-results-review.png` | Review screen — extracted scores | After upload, review step |
| `smart-results-confirm.png` | Confirm screen before saving | After review, confirm step |

## Stage Management

**Upload to:** `public-assets/public-docs/organizer/matches/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `complete-stage-status.png` | Complete Stage — group statuses | Stage → Complete Stage |
| `complete-stage-qualifiers.png` | Qualifier preview — teams above/below line | Review Qualifiers step |
| `complete-stage-winners.png` | Winners view for final stage | Review Winners step |
| `announcement-create.png` | New Announcement form | Group → Announcements → New |
| `announcement-player-view.png` | Announcements in player Match Hub | Player Match Hub |
| `stage-settings.png` | Stage Settings — name, auto-assign, redistribute | Stage → Settings |
| `stage-summary.png` | Stage Summary — overview with tabs | Stage → Summary |

## Live Scoring

**Upload to:** `public-assets/public-docs/organizer/live-scoring/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `live-scoring-setup.png` | Setup page — teams, broadcast config, Start button | Group → Live Scoring |
| `live-scoring-active.png` | Active session — match tabs, score table, sidebar | During active session |
| `live-scoring-push-scores.png` | Bottom bar with "Push Scores" and "End Session" | During session, bottom |
| `live-scoring-end-session.png` | End Session confirmation modal | After clicking End Session |
| `standalone-create.png` | Standalone session creation wizard | Sidebar → Live Scoring → Create |

## Stream Overlays

**Upload to:** `public-assets/public-docs/organizer/overlays/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `overlay-urls-modal.png` | OBS Overlay URLs modal with copy buttons | After starting live session |
| `overlay-side-in-obs.png` | Side overlay running in OBS (overlay + game feed) | OBS with browser source |
| `overlay-wide-in-obs.png` | Wide 16:9 overlay running in OBS | OBS with browser source |
| `overlay-template-gallery.png` | Template gallery showing designs | Broadcast config → template picker |
| `overlay-broadcast-config.png` | Broadcast config fields (tournament, stage, handles) | Live Scoring setup |

## Scrims

**Upload to:** `public-assets/public-docs/organizer/scrims/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `scrim-management.png` | Scrim page — schedule, results, announcements | Any scrim page |

## Clubs

**Upload to:** `public-assets/public-docs/organizer/clubs/`

| Filename | What to capture | Where in the app |
|----------|----------------|-----------------|
| `club-settings.png` | Club Settings — name, region, social links, banner | Organizer sidebar → Club Settings |
| `club-members.png` | Club Members page | Organizer sidebar → Members |
| `club-public-page.png` | Public club page as a player sees it | `/clubs/[slug]` |

---

## Tips for good screenshots

1. **Use a populated account** — show real-looking data (team names, scores, etc.)
2. **Full width** — capture the full page, not a cropped section
3. **Default theme** — use the default dark theme for consistency
4. **Hide personal info** — blur or use test accounts without real emails
5. **PNG format** — use PNG for crisp text
6. **1200px+ wide** — minimum width for readability in docs
7. **Name exactly as listed** — filenames must match or the docs won't find them
