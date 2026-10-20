# Server configuration

## Install

1. Put `territoria-1.0.0.jar` in the server's `mods/` folder.
2. Every player installs the **same jar**. A player without it is refused at login with a clear message.
3. Start the server once. Territoria creates `config/territoria-server.json` and `config/territoria/README.txt`.

The console prints a check line, for example:
`Territoria ready: economy=items, permissions=neoforge:default_handler, logo=none, countries=0`

## Editing the rules

The easiest way: join as an operator, open the menu (`N`), click the **hammer** at the bottom of the rail, change
values and click **Save**. The panel is split into *Economy*, *Costs*, *Countries*, *Power*, *Wars*, *Teleport*,
*Server*, *Moderation* and *Logs*, with an explanation under every setting (see [Admin tools](Admin-Tools.md)).

You can also edit `config/territoria-server.json` and run `/territoriaadmin reload`.

| Key | Default | What it does |
|---|---|---|
| `economy` | `auto` | `auto`, `items`, `vault` or `command` |
| `currency` | `minecraft:emerald` | Money item for the `items` economy |
| `currency_name` | `coins` | Money name for the `command` economy |
| `withdraw_command` / `deposit_command` | empty | Commands for the `command` economy |
| `chest_rows` | 6 | Rows of the country chest (1–6) |
| `max_claims` | 0 | Claim limit per country (0 = none) |
| `max_members` | 0 | Member limit per country (0 = none) |
| `claim_distance` | 12 | How far (chunks) a claim can reach |
| `max_markers` | 50 | Map markers per country |
| `creation_cost` | 0 | Price to found a country |
| `claim_cost` | 0 | Price per claimed chunk (country bank) |
| `claim_upkeep` | 0 | Daily cost per chunk (0 = off) |
| `claims_per_active` | 0 | Power: claims per active member (0 = off) |
| `active_days` | 14 | Days a member stays "active" after being seen |
| `war_hours` | 24 | Length of a war |
| `war_grief` | 1 | 1 = enemies can build/break in each other's land during a war |
| `capture_seconds` | 60 | Time to capture a chunk |
| `teleport_warmup` / `teleport_cooldown` | 5 / 60 | Seconds for the home teleport |
| `max_tax` | 100 | Highest daily tax |
| `plot_days` | 30 | Longest rent one payment can buy |
| `level_cost` | 100 | Price of research level 1 (doubles each level) |
| `level_claims` | 10 | Extra claims per research level |
| `discord_webhook` | empty | Discord webhook URL for news (hidden from players) |

**Suggested survival start:** `creation_cost` 32, `claim_cost` 4, `claims_per_active` 16, `claim_upkeep` 1,
`max_tax` 64.

## Server logo

Put a square PNG (max 256 KB) at `config/territoria/logo.png` and run `/territoriaadmin reload`. It appears at the top
of every player's menu rail. Without it, that corner stays empty.

## Discord

Create a webhook in your Discord channel (*Channel settings → Integrations → Webhooks → New webhook → Copy URL*)
and paste it in `discord_webhook`. Foundings, disbands and wars are posted there.

## Data & backups

Countries and claims are saved in the world (`<world>/data/`), so a normal world backup covers them. The
moderation history is in `<world>/territoria/moderation.log`.
