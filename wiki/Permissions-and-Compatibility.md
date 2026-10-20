# Permissions & compatibility

## Economy

| `economy` | Money comes from |
|---|---|
| `auto` (default) | The first available: a registered mod economy → Vault → command bridge → items |
| `items` | The `currency` item in the inventory (emeralds by default) |
| `vault` | Vault / VaultUnlocked on hybrid servers (Arclight, Mohist, Youer…): EssentialsX, CMI, any Vault economy |
| `command` | Any economy with commands, through `withdraw_command` and `deposit_command` |

Command bridge example:

```json
"economy": "command",
"currency_name": "coins",
"withdraw_command": "eco take {player} {amount}",
"deposit_command": "eco give {player} {amount}"
```

`{player}`, `{uuid}` and `{amount}` are filled in. The take command must **fail** when the player can't afford it.

Mod developers can plug in directly: implement `com.territoria.economy.Economy` and call `Economies.register(...)`.

## Permission nodes

The nodes go through NeoForge's permission API, so **LuckPerms** (NeoForge) manages them. On hybrid servers,
LuckPerms as a Bukkit plugin works too.

| Node | Default | Allows |
|---|---|---|
| `territoria.use` | everyone | `/country` and the country menu |
| `territoria.create` | everyone | Founding a country |
| `territoria.claim` | everyone | Claiming chunks (still needs the role rule) |
| `territoria.home` | everyone | Home teleport |
| `territoria.chat` | everyone | Country chat |
| `territoria.war` | everyone | Declaring wars |
| `territoria.admin` | operators | `/territoriaadmin` and the admin panel |
| `territoria.bypass.protection` | nobody | Build and interact in any claim |
| `territoria.bypass.cooldown` | nobody | No home warm-up / cooldown |

Example, only VIPs can found countries:

```
/lp group default permission set territoria.create false
/lp group vip permission set territoria.create true
```

## Name tags & placeholders

Country names before player names use `nt_` scoreboard teams. A player already in another plugin's team gets it
in the TAB name instead.

Other mods can read `com.territoria.country.TerritoriaPlaceholders.resolve(player, key)` with the keys `country`, `role`,
`balance`, `currency`, `claims`, `members`, `online`, `level`, `power`, `tax`.

## Resource packs

Menu icons are plain PNGs at `assets/territoria/textures/gui/icons/<name>.png` (white on transparent, tinted by the
mod), so a resource pack can restyle them.
