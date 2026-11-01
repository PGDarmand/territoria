# Server configuration

## Install

1. Put the jar for your loader (`territoria-neoforge-…jar`, or `territoria-fabric-…jar` plus Fabric API) in the server's `mods/` folder.
2. Every player installs the **same jar**. A player without it is refused at login with a clear message.
3. Start the server once. Territoria creates `config/territoria-server.json` and `config/territoria/README.txt`.

The console prints a check line, for example:
`Territoria ready (NeoForge): economy=items, permissions=neoforge:default_handler, logo=none, countries=0`

## Editing the rules

The easiest way: join as an operator, open the menu (`N`), click the **hammer** at the bottom of the rail, change
values and click **Save**. The panel is split into *Economy*, *Costs*, *Countries*, *Power*, *Research*, *Role rules*,
*Wars*, *Teleport*, *Server*, *Moderation* and *Logs*, with an explanation under every setting (see [Admin tools](Admin-Tools.md)).

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
| `war_grief` | 1 | 1 = raiding: enemies at war get the `war_rules` in each other's land |
| `war_rules` | all land rules | Land rules raiders get, comma-separated (e.g. `containers,doors`) |
| `war_explosions` | 0 | 1 = TNT lit by an enemy at war breaks blocks even where explosions are off |
| `locked_rules` | empty | Rules countries can't change, comma-separated (e.g. `ender_pearls,fire`) |
| `capture_seconds` | 60 | Time to capture a chunk |
| `teleport_warmup` / `teleport_cooldown` | 5 / 60 | Seconds for the home teleport |
| `max_tax` | 100 | Highest tax per day (hourly taxes get a 24th, weekly ones 7 times) |
| `plot_days` | 30 | Longest rent one payment can buy, in days |
| `max_level` | 5 | Number of research levels (1–50) |
| `level_cost` | 100 | Price of research level 1 |
| `level_growth` | 100 | % added to the price each level (100 = doubles) |
| `level_members` | 1 | Members needed per level (level N: leader + N × this) |
| `level_chunks` | 5 | Chunks needed per level (level N: N × this) |
| `level_claims` | 10 | Extra claims per research level |
| `level_warps` | 0 | Extra warps per research level |
| `level_member_slots` | 0 | Extra member slots per research level (when `max_members` is set) |
| `discord_webhook` | empty | Discord webhook URL for news (hidden from players) |
| `max_warps` | 5 | Warps per country |
| `connected_claims` | 0 | 1 = new chunks must touch the country's land |
| `web_map` | 1 | 1 = show the countries on BlueMap (when the BlueMap mod is installed) |
| `chat_tags` | 1 | 0 = no "[Country]" before names in chat (name tags and TAB keep it); players can also hide it |
| `treasury` | 0 | 1 = bank money lives in a Treasury block, public on the map and lootable in wars (items economy) |

**Suggested survival start:** `creation_cost` 32, `claim_cost` 4, `claims_per_active` 16, `claim_upkeep` 1,
`max_tax` 64.

## Server logo

Put a square PNG (max 256 KB) at `config/territoria/logo.png` and run `/territoriaadmin reload`. It appears at the top
of every player's menu rail. Without it, that corner stays empty.

## Discord

Create a webhook in your Discord channel (*Channel settings → Integrations → Webhooks → New webhook → Copy URL*)
and paste it in `discord_webhook`. Foundings, disbands and wars are posted there.

## Web map (BlueMap)

Install the [BlueMap](https://modrinth.com/plugin/bluemap) mod on the server: with `web_map` on, every country
appears on BlueMap's web page in its color, with its capital, refreshed every two minutes. A **Countries**
layer can be toggled on the web page. Without BlueMap, this setting does nothing.

## Data & backups

Countries and claims are saved in the world (`<world>/data/`), so a normal world backup covers them. The
moderation history is in `<world>/territoria/moderation.log`.
