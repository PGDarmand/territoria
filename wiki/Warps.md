# Warps

A **warp** is a named teleport point inside your land: the town hall, the market, the mine, the arena…

## Warps tab

**Country menu → Warps** lists your country's warps and the **public** warps of every other country. Players
without a country see the public ones too.

- Filters: **All**, **My country**, **Public**.
- **Teleport** uses the same warm-up and cooldown as the home teleport (`teleport_warmup`, `teleport_cooldown`):
  don't move or take damage during the warm-up.
- The map button opens the world map centered on the warp.

## Creating warps

Needs the *Manage markers* rule.

1. Stand where the warp should be, **inside your land**.
2. Type a name, choose **Public** or **Private**, and click **Set warp here**.

Each warp row then has buttons to switch it between public and private, and to delete it (click twice to
confirm). The server limits how many warps each country has (`max_warps`, 5 by default).

| Warp | Who can use it |
|---|---|
| Private | Your members with the *Teleport home* rule |
| Public | Every player, except players banned from your land |

## Commands

| Command | Action |
|---|---|
| `/country warp <name>` | Teleport to one of your country's warps |
| `/country setwarp <name>` | Set a private warp where you stand |
| `/country delwarp <name>` | Delete a warp |
