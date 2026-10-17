# MEOW world lists

The MEOW VRChat world downloads `roster.json` from this repo every time someone joins
(VRChat String Loading, `raw.githubusercontent.com`).

## VIPs (Patreon supporters)
Add the person's **exact VRChat display name** to `"vips"`. On their next join they get:
- the VIP role (VIP perks / VIP area once it exists)
- music control: the DJ tab in the menu (house music, queue, level)

VIPs can give plain VIP to friends in-world (Players tab > Give VIP). Those friends do NOT get music control
unless a Host makes them DJ.

## Staff
`"staff"`: `{"name": "Display Name", "rank": "staff"}` or `"rank": "admin"`. The world owner is set in Unity and can
never come from this file.

## Editing
Edit `roster.json` on github.com (pencil icon), keep it valid JSON (commas between names, quotes around each name),
commit. GitHub can take up to ~5 minutes to serve the new file; people already in the world keep the old list until
they rejoin.

## Supporter board
"supporters": the names on the board in the Den, by tier: "groupposter" (Group + Poster VIP, top), "poster" (Poster VIP), "group" (Group VIP), "vip" (VIP), "kitten". The "name" is just the label shown on the board (any text); perks still come from "vips".
