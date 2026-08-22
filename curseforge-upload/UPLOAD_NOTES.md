# CurseForge upload — VanillaSkills Casino 1.0.0

This is a **brand-new mod** — there is no existing CurseForge project for it yet. You'll need to
create one before you can upload anything. This is the one file in this whole batch that isn't a
"click Upload File" job.

## Step 1 — create the project

CurseForge → your dashboard → **Create Project** → **Mod**.

Suggested project fields (yours to change, these are just sensible defaults):
- **Name:** VanillaSkills Casino
- **Slug:** something like `vanillaskills-casino` (check availability)
- **Summary:** "Slots, blackjack and video poker on the VanillaSkills skill screen, played with Quest Shards."
- **Category:** Server Utility (or Adventure/Fabric — whichever your other mods use)
- **License:** match whatever you picked for the other mods (currently All Rights Reserved per your
  standing convention)

## Step 2 — set the required dependency

On the file-upload screen, add **Vanilla-Skills** (projectID `1570558`) as a **Required Dependency**.
CF will refuse to let players download this without it installed, which is correct — the casino
does nothing without VanillaSkills.

## Step 3 — upload the files

### Fabric jar (26.2)
**File:** `vscasino-1.0.0+mc26.2.jar` (in this folder)
- Game version **26.2**, loader **Fabric**
- Required dependency: **Vanilla-Skills** (`1570558`), version **1.7.6 or newer**
- Required dependency: **Fabric API** (`306612`)

### Fabric jar (26.1.2)
**File:** `vscasino-1.0.0+mc26.1.2.jar`
(in `../../../26.1.2/vscasino/curseforge-upload/`)
- Game version **26.1.2**, loader **Fabric**
- Same dependencies as above

### Texture pack — your call
`VSCasino-TexturePack.zip` is auto-pushed to joining players by the mod itself, so nothing *requires*
it to exist on CurseForge — it already works purely off the GitHub release
(https://github.com/Andrewwwwwwwwwwwwwww/vscasino/releases/tag/v1.0.0), same as VanillaSkills' own
pack is hosted. Two options:
- **Skip it** (my default recommendation) — one less CF project to keep in sync every time art
  changes; GitHub hosting already works.
- **Mirror the VS-Textures pattern** — create a separate resource-pack project (e.g. "VSC-Textures")
  like VanillaSkills has, if you'd rather have it independently browsable/downloadable on CF, or
  want a CF-hosted URL instead of GitHub for the auto-push. If you want this, say so and I'll switch
  the baked-in `DEFAULT_RP_URL` over to whatever CF gives you and rebuild both jars.

## Description text (starter draft)

> Adds a casino to the VanillaSkills skill screen — click the button above your stats to open a
> lobby with **Slots**, **Blackjack**, and **Video Poker**, all played with your Quest Shards.
>
> - Fully server-side: vanilla clients can play with nothing installed, and the server pushes card
>   and chip artwork to them automatically on join.
> - Blackjack supports doubling and splitting; you're never forced to stand early.
> - Every game has an in-game "How to play" book with a clickable table of contents.
> - Deeply configurable: bet limits, payout rates, the whole video poker paytable, sound effects,
>   and more — see `casino.json` per world.
> - Your VanillaSkills luck attribute gives a small bonus to winnings.
>
> Requires **VanillaSkills 1.7.6 or newer**.

## Changelog to paste
```
### Added
- Initial release: Slots, Blackjack (with double down and split), and Video Poker.
- Fully server-side, with custom card and chip artwork pushed to vanilla clients automatically.
- Deeply configurable economy, sounds, and per-game settings.
```

## After creating the project
Send me the new projectID and fileIDs once CF approves them — the ModHub page currently links only
to GitHub, and I can add the CurseForge link once it exists.
