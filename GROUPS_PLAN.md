# Group VIP - plan (waiting for approval, not built)

Goal (like a club website group system, but driven by this repo): a paying group lists its staff once; any instance
started by one of its senior staff loads that team, so the group runs its own events here.

## Data (roster.json, refreshed by the world every hour)
```json
"groups": [
  {
    "id": "pawpatrol",
    "name": "Paw Patrol",
    "tier": "group",                 // group | groupposter
    "logo": "groups/pawpatrol.png",   // shown on the VIP Groups wall + in their instances
    "owners":   ["Display Name"],     // can START a group instance (their list loads)
    "hosts":    ["Name", "Name"],     // auto Host when they join that instance
    "security": ["Name"],             // auto Security
    "djs":      ["Name"],             // auto DJ
    "colors": { "accent": "#C7B3FF", "floor": "walnut" }   // later: instance look
  }
]
```

## How an instance becomes a group instance
1. The instance starter (or, in a Group instance, the first player) is in some group's `owners`.
2. The world marks the instance as that group's (synced once by the owner, like the founder today).
3. Everyone who joins is checked against that group's `hosts` / `security` / `djs` -> roles given automatically.
4. The list is re-downloaded every hour (VRChat string loading); changes apply without anyone rejoining.

## VIP-host powers (the paid part)
- Lock / unlock the front gate, timeout (Cage), jail: only in a **VIP instance** = a group instance of a paying group,
  or an instance with the world owner / roster staff in it. Elsewhere Hosts keep go-to / bring / roles, not moderation.
  (Changes current behaviour - switch on only after testing; NOT before an event.)

## In-world
- **VIP Groups wall** (new room or the gallery): one card per paying group - logo, name, "hosting now" badge when a
  group instance is live... (badge only for the current instance).
- Group instance touches (later): logo on the Den screen / neon slot, accent colour for coves + neon, floor finish pick.

## Open questions for foxi
- Who counts as "senior staff" that can start a group instance: owners only, or owners + hosts?
- Should Group VIP hosts get timeout / jail, or only the gate lock?
- One group per instance, or can a VIP host pick between groups they belong to?