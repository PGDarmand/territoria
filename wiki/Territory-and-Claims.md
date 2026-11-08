# Territory & claims

Land is claimed by **chunk** (16 × 16 blocks, full height).

## Claiming

Open **Territory** (or the world map, `M`):

- **left-click** a chunk to select it, or **drag** with the left button to select a rectangle (up to 256 chunks);
- **right-click** opens a menu: **Claim the selection**, **Release the selection** or clear it;
- **drag with the right button** to move the map, scroll to zoom;
- you need the *Claim & unclaim land* rule (without it, the left button just moves the map).

A selection is claimed chunk by chunk, starting near you, with the usual checks (limits, money, distance,
connected claims). If one fails, the message says how many chunks were claimed and why it stopped. The selection
is shared by both maps: select on the world map, claim from the Territory page, or the other way round.

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

### Auto-claim

Turn on **Auto-claim** in your personal settings (Country card), or use `/country autoclaim` (or `/autoclaim`):
every wild chunk you travel through is claimed for your country, with the usual checks. The whole path counts, so
flying fast or moving diagonally leaves no holes. It turns itself off and tells you why at the first claim that
fails (limit reached, not enough money…), and when you teleport, die or change dimension, so no land is claimed
far from home by accident. A whole trip writes one line in the country logs.

### Connected claims

When the server enables `connected_claims`, a new chunk must touch your land side by side (except your very
first chunk in a dimension). Countries then grow as one block instead of scattered dots.

## Protection

Inside your land, everything follows the **role rules**: building, containers, doors, redstone, animals,
villagers, buckets, fire, pearls, item pick-up… Outsiders get the *Visitor* role, trusted players and allies the
*Ally* role.

Protection also covers what has no player behind it: fire spread, explosions, fluids flowing in from outside and
hoppers pulling from your containers.

## Entering a country

Crossing a border shows a banner with the country's name and flag, and the minimap shows where you are.
