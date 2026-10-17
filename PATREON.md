# MEOW - Kitty Lounge: Patreon / VIP plan

USD per month. Ranks, top first: **Group + Poster VIP > Poster VIP > Group VIP > VIP > Kitten**.
Poster and Group can be bought separately or together. DJ / music control is a small perk of Group VIP and up.

| Rank | Price | Perks |
|---|---|---|
| **Group + Poster VIP** | $60 | Everything in Group VIP + Poster VIP (your group's staff in your instances AND a poster to promote your group) |
| **Poster VIP** | $50 | One big lit courtyard poster for the month (personal or group promo, 1 free swap) + VIP perks + DJ tab |
| **Group VIP** | $25 | Your VRChat group's staff list in the world (PLANNED, see GROUPS_PLAN.md): instances started by your group staff auto-give Host / Security to your team; VIP-host powers (gate lock, timeout, jail) in those instances; DJ tab; your group on the VIP Groups wall |
| **VIP** | $12 | Overhead VIP paw flair (hide any time in Settings), VIP area (when it opens), can give plain VIP to friends |
| **Kitten** | $5 | Name on the supporter board in the Den, Discord supporter role |

Add-ons: extra poster slot +$35 - mid-month poster swap $10. Yearly: pay 10 months, get 12.

## Running it today
- VIP / Poster / Group-and-up: add the exact VRChat display name to `roster.json` -> `"vips"` (VIP flair + DJ tab today).
- Board: add `{ "name": "label", "tier": "groupposter|poster|group|vip|kitten" }` to `"supporters"`.
- Posters: `posters/poster_NN.png` (see posters/README.md).
- Group staff lists: not live yet (plan below needs your OK).

## Rules
- Perks follow the world rules; staff can remove any perk for rule breaks (no refund for the current month).
- Posters: VRChat ToS + Community Guidelines (no nudity, gore, hate, illegal content, scams).
- Check VRChat's current Terms / creator guidelines on paid perks before launch; keep perks cosmetic / convenience.