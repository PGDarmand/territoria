# Territory & claims

Land is claimed by **chunk** (16 × 16 blocks, full height).

## Claiming

Open **Territory**:

- **left-click** a chunk to claim it, **right-click** to release it;
- drag to move the map, scroll to zoom;
- you need the *Claim & unclaim land* rule.

Or stand in a chunk and use `/country claim` / `/country unclaim`.

Limits the server can set:

| Setting | Effect |
|---|---|
| `claim_distance` | How far from you a chunk can be claimed |
| `claim_cost` | Price per chunk, paid by the country bank |
| `max_claims` | Hard limit per country |
| `claims_per_active` | **Power**: each active member allows this many claims |
| `level_claims` | Extra claims per research level |
| `claim_upkeep` | Daily cost per chunk |

### Power

When `claims_per_active` is set, a country can hold `active members × claims_per_active` chunks (+ research
bonus). A member is active if seen within `active_days`. Inactive countries slowly lose the right to expand.

### Upkeep

When `claim_upkeep` is set, the bank pays every chunk once a day. If it can't, members are warned. The next day the
chunks the bank can't afford are released, farthest from the capital first.

## Protection

Inside your land, everything follows the **role rules**: building, containers, doors, redstone, animals,
villagers, buckets, fire, pearls, item pick-up… Outsiders get the *Visitor* role, trusted players and allies the
*Ally* role.

Protection also covers what has no player behind it: fire spread, explosions, fluids flowing in from outside and
hoppers pulling from your containers.

## Entering a country

Crossing a border shows a banner with the country's name and flag, and the minimap shows where you are.
