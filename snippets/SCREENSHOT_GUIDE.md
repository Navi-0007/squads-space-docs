# Screenshot Guide

How to add screenshots to the SquadsSpace docs.

## Quick steps

1. Take the screenshot (see the table below for exactly what to capture)
2. Upload it to S3 (or any public URL)
3. Open `snippets/screenshots.mdx` and paste the URL next to the matching variable
4. Commit and push — every page using that variable automatically shows the new image

## Where to find `screenshots.mdx`

`snippets/screenshots.mdx` in this repo. Each variable is an empty string `""` until you add a URL.

**Before:**
```
export const ss_player_dashboard = ""
```

**After:**
```
export const ss_player_dashboard = "https://your-s3-bucket.s3.amazonaws.com/docs/player-dashboard.png"
```

## What pages show while screenshots are missing

Pages show a blue info box: **"Screenshot coming soon — [description]"**. Once you add the URL, the actual image replaces it automatically.

---

## Screenshot list

### Getting Started

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_getting_started_become_organizer_landing` | The "Become Organizer" landing page before applying | `/organizer/register` |
| `ss_getting_started_become_organizer_dashboard` | Organizer Dashboard right after activation | `/organizer/[slug]` |

### Player Pages

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_player_dashboard` | Player Dashboard with tournaments, clubs, quick actions visible | `/dashboard` |
| `ss_player_browsing_tournaments` | All Tournaments page with cards, filters, status badges | `/tournaments/p/all-tournaments` |
| `ss_player_register_button` | Tournament page showing the Register/Join button in hero | Any tournament page |
| `ss_player_registration_status` | Registration Status page with requirements progress tracker | `/tournaments/p/[slug]/status` |
| `ss_player_match_hub` | Match Hub with schedule, room credentials, match selector | Match Hub for any active tournament |
| `ss_player_squad_page` | Squad page showing members, invite code, name | `/squads` |
| `ss_player_clubs_directory` | Clubs directory with club cards | `/clubs` |
| `ss_player_profile` | Profile page with hero banner, tournaments, clubs | `/profile/[username]` |
| `ss_player_notifications` | Notifications page with tabs (All, Unread, Saved) | `/notifications` |

### Organizer Dashboard

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_organizer_dashboard` | Organizer Dashboard — club details, quick actions, tournaments list | `/organizer/[slug]` |
| `ss_organizer_tournament_dashboard` | Tournament Dashboard with tabs (Overview, Roadmap, Registrations...) | `/organizer/[slug]/tournaments/[tSlug]` |

### Tournament Creation

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_create_tournament_wizard` | Full creation wizard — Step 1 visible | `/organizer/[slug]/tournaments/create` |
| `ss_create_tournament_step1_details` | Step 1: Tournament Details with fields visible | Same page, Step 1 |
| `ss_create_tournament_step2_game_config` | Step 2: Game Configuration — scoring, platforms | Same page, Step 2 |
| `ss_create_tournament_step3_review` | Step 3: Review & Create summary | Same page, Step 3 |

### Tournament Editing

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_edit_tournament_accordion` | Edit page with accordion sections expanded | `/organizer/.../edit` |
| `ss_edit_tournament_locked_field` | A locked field showing red/amber badge with tooltip | Same page, hover on locked field |

### Roadmap Builder

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_roadmap_builder_empty` | Roadmap tab before configuration — "Configure" button visible | Tournament Dashboard → Roadmap tab |
| `ss_roadmap_builder_stages` | Complete roadmap with 2-3 stages configured | Roadmap Builder with stages |
| `ss_roadmap_builder_stage_config` | One stage being configured — entrants, group size, qualifiers fields | Stage editor in builder |
| `ss_roadmap_builder_published` | Published roadmap with "Manage" buttons on each stage | Roadmap tab after publishing |
| `ss_roadmap_poster_templates` | Poster template gallery showing Neon, Nebula, Inferno, Phantom | Poster image creation page |
| `ss_roadmap_poster_download` | Poster preview before download | Same page, preview mode |

### Registration & Requirements

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_registrations_page` | Registrations tab with filters (All, Pending, Confirmed...) and cards | Tournament Dashboard → Registrations |
| `ss_registrations_detail_panel` | Detail panel open for one registration — team info, members, requirements | Click any registration |
| `ss_registrations_bulk_actions` | Multiple registrations selected with bulk action buttons visible | Select 3+ registrations |
| `ss_registration_modes_comparison` | Registration mode selection in creation wizard (Open, Approval Required...) | Tournament creation Step 1 |

### Group Creation

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_auto_groups_config` | Auto-groups configuration page — naming, seeding, fill options | `/rounds/[round]/auto-groups` |
| `ss_auto_groups_preview` | Group preview after clicking "Preview Groups" | Same page, after preview |
| `ss_groups_page_locked` | Groups page with lock indicators (green dots) | `/rounds/[round]/groups` |
| `ss_groups_multi_swap` | Multi Swap view with teams selected for moving | Same page, multi-select mode |

### Invited Slots

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_invited_slots_page` | Invited Slots page — invite link, capacity, joined teams | `/rounds/[round]/invited-slots` |
| `ss_invited_slots_link_actions` | Invite link section with Copy, Rotate, Revoke buttons | Same page, link card |

### Match Management

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_match_management_group` | Group page with match selector, schedule, results sections | Any group page |
| `ss_match_status_card` | Match status card showing status + action buttons (Start Match, etc.) | Group page, match selected |
| `ss_match_results_entry` | Results entry table with placement and kills columns | Group page → Results |
| `ss_match_room_credentials` | Room ID & Password card (with lock icon if not started) | Group page → ID/Password |

### Mass Operations

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_mass_create_scheduling` | Mass Create — scheduling options (Parallel, Global, Same Time) | Mass Operations → Create Matches, Step 3 |
| `ss_mass_create_maps` | Mass Create — map selection (Same for all, Custom per group) | Mass Operations → Create Matches, Step 4 |
| `ss_mass_manager` | Mass Manager page with match details across groups | Mass Operations → Mass Manager |
| `ss_mass_resultor` | Mass Resultor page with score entry | Mass Operations → Mass Resultor |

### Smart Results

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_smart_results_upload` | Smart Results upload screen — file picker visible | Group page → Smart Results button |
| `ss_smart_results_review` | Review screen showing extracted scores from screenshot | After upload, review step |
| `ss_smart_results_confirm` | Confirm screen before saving results | After review, confirm step |

### Live Scoring

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_live_scoring_setup` | Live Scoring setup page — teams, broadcast config, Start button | Group page → Live Scoring |
| `ss_live_scoring_active` | Active scoring interface — match tabs, score table, standings sidebar | During active session |
| `ss_live_scoring_push_scores` | Bottom bar showing "Push Scores" and "End Session" buttons | During active session, bottom |
| `ss_live_scoring_end_session` | End Session confirmation modal | After clicking End Session |
| `ss_live_scoring_standalone_create` | Standalone session creation — basic info, teams, points config | Sidebar → Live Scoring → Create |

### Stream Overlays

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_overlay_urls_modal` | OBS Overlay URLs modal with copy buttons | After starting live session |
| `ss_overlay_side_in_obs` | Side overlay rendered in OBS (overlay + game feed) | OBS with browser source added |
| `ss_overlay_wide_in_obs` | Wide 16:9 overlay rendered in OBS | OBS with browser source added |
| `ss_overlay_template_gallery` | Template gallery showing available designs | Broadcast config → template picker |
| `ss_overlay_broadcast_config` | Broadcast configuration fields (tournament, stage, handles) | Live Scoring setup page |

### Stage Completion

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_complete_stage_status` | Complete Stage page — group statuses (ready, incomplete, etc.) | Stage → Complete Stage |
| `ss_complete_stage_qualifiers` | Qualifier preview — teams highlighted above/below qualifier line | Review Qualifiers step |
| `ss_complete_stage_winners` | Winners view for final stage | Review Winners step (final stage) |

### Status Control

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_status_control_transitions` | Status Control page — transition cards with descriptions | Tournament Dashboard → Status |
| `ss_status_control_risk_levels` | Transition card showing risk level badge (low/medium/high) | Same page, any transition card |

### Scrim, Club, Other

| Variable | What to capture | Where in the app |
|----------|----------------|-----------------|
| `ss_scrim_management_page` | Scrim page with schedule, results, announcements sections | Any scrim page |
| `ss_club_settings` | Club Settings page — name, region, social links, banner | Organizer sidebar → Club Settings |
| `ss_club_members` | Club Members page — member list | Organizer sidebar → Members |
| `ss_club_public_page` | Public club page as a player sees it | `/clubs/[slug]` |
| `ss_announcements_create` | New Announcement form — title, description, type selector | Group → Announcements → New |
| `ss_announcements_player_view` | Announcements card in player Match Hub | Player Match Hub → Announcements |
| `ss_export_modal` | Export modal — category selection and format | Tournaments → Export |
| `ss_stage_settings` | Stage Settings page — name, auto-assign, redistribute | Stage → Settings |
| `ss_stage_summary` | Stage Summary — overview with tabs | Stage → Summary |
| `ss_point_table_config` | Point table configuration — kill points + placement grid | Tournament creation Step 2 |

---

## Tips for good screenshots

1. **Use a populated account** — screenshots should show real-looking data (team names, scores, etc.)
2. **Full width** — capture the full page width, not a cropped section
3. **Light theme** — use the default theme for consistency
4. **Hide personal info** — blur or use test accounts without real emails
5. **PNG format** — upload as PNG for crisp text rendering
6. **Recommended size** — 1200px wide minimum for readability on docs
