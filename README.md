# Katia's Fundraising CRM

A personal, zero-install CRM for tracking fundraising leads as a visual pipeline.
Everything lives in one file: **`index.html`** — no server, no accounts, no dependencies.

## How to use it

1. Open `index.html` in any browser (double-click it, or serve it from GitHub Pages).
2. The board comes pre-loaded with all current leads across six stages:
   - 🤝 **Intros Made** — both sides accepted, waiting to connect
   - 📤 **Pending Outreach** — contacted, awaiting reply
   - 🎯 **Direct Outreach** — not in network, reach out yourself
   - 💰 **Negotiation** — active deal conversations
   - ✅ **Closed Won** — committed
   - ❌ **Closed Lost** — passed, or the intro window expired

## Features

- **Drag & drop** cards between stages (and reorder within a stage).
- **Click any card** to edit: name, fund, email, LinkedIn URL, tags, notes, next-action date.
- **LinkedIn on every card** — if you've saved a profile URL it opens directly; if not,
  the "Find on LI" button runs a LinkedIn people search for that name + fund so you can
  grab the real URL and paste it in.
- **Email button** — appears once you add an email; click to compose (mailto).
- **Pitch tracking** — each lead has "Pitch for" checkboxes (Frontier Residency /
  BerlinHouse) that show as colored chips on the card and are searchable
  (type "frontier" or "berlinhouse" in the search box to filter).
- **Next-action dates** show on cards and turn red when overdue.
- **Tags** — free-form; `hot`, `warm`, and `booked` get automatic colors.
- **Search** across names, funds, notes, and tags.
- **Rename stages** inline, delete them, or add new ones with "+ Add stage".
- **Auto-saved** to your browser's localStorage on every change.
- **Export / Import** — download all data as JSON (do this occasionally as a backup,
  or to move the board to another browser/computer).

## Working as a team (shared live board)

Out of the box the board is single-player (saved per browser). To collaborate:

1. Click **Share** in the header.
2. Follow the three steps in the dialog: create a free [Supabase](https://supabase.com)
   project, run the provided setup SQL in its SQL Editor, and paste the project URL +
   anon public key into the dialog.
3. Click **Create shared board**, then **Copy** the invite link and email it to your team.

Anyone who opens the invite link joins the same live board — edits sync both ways
within a few seconds (the header shows "Shared · synced"). If two people edit at the
exact same moment, the last save wins for that change.

Note: anyone with the invite link can view and edit the board, so only share it with
people you trust.

## Notes

- Data is stored per-browser. If you open the file on a different machine or clear
  browsing data, use **Export** on the old one and **Import** on the new one.
- The seed data only loads the first time; after that, your saved board always wins.
