# Group VIP - plan v2 (decisions from foxi 2026-10-17; ready to build after approval)

## Ranks inside a group (all saved per group in roster.json)
| Group rank | Can open a group instance | Auto role on join (in THEIR group's instance) |
|---|---|---|
| owners | yes | Host (+ Security, DJ, video) |
| seniorHosts | yes | Host (+ Security, DJ, video) |
| hosts | no | Host |
| security | no | Security |
| djs | no | DJ |
| video | no | Video control |
| access | no | Gate access |

```json
"groups": [
  { "id": "pawpatrol", "name": "Paw Patrol", "tier": "group", "logo": "groups/pawpatrol.png",
    "owners": ["A"], "seniorHosts": ["B"], "hosts": ["C"], "security": ["D"], "djs": ["E"], "video": [], "access": [] }
]
```

## Which group an instance belongs to (never wrong perms)
1. The **instance group is decided first**, once, from the person who opened it (the instance starter, or the first
   player of a Group / Public instance = the founder the world already tracks).
2. Instance group = the group where that person is an **owner or seniorHost**. Synced and frozen for the instance.
3. Only then are joiners checked - and **only against that one group's lists**. Being staff in another group gives
   nothing here. So someone in two groups can never get the wrong group's perms.
4. **Instance Setup panel** (opener only): opens by itself when the instance creator first loads in (and from the
   menu any time after). Only the instance creator sees it.
   - **Group dropdown**: `Default (no group)`, then every paying group where the creator is owner / seniorHost.
     - in no group -> only `Default`.
     - in exactly one group -> that group is **pre-selected**, `Default` still there to switch it off.
     - in two or more -> starts on `Default` until they pick one.
   - Changing the pick re-applies the group roles for everyone in the instance (old group's auto roles removed).
   - Same panel: lock / unlock the gate, and later the instance looks (group logo, accent colour, floor).
   - VRChat does not tell worlds which VRChat Group an instance was made under, so the creator's pick is the source of truth.5. Lists re-download every hour; roles update live.

## Moderation powers (paid)
- **Timeout (Cage):** Group VIP hosts in their own group instance (+ foxi, roster staff).
- **Jail:** only foxi for now (jail is not finished).
- **Gate lock:** VIP hosts in VIP instances (+ foxi, roster staff).
- Non-VIP instances: Hosts keep go-to / bring / giving DJ, video, access - no timeout / jail / gate lock.
- Rollout: build with a world switch, test, then turn on - **never before an event**.

## Still planned
- VIP Groups wall (a card per paying group, logo + name, "live here now" in a group instance).
- Group instance looks: logo on the Den screen / a neon slot, accent colour (coves, neon), floor finish.