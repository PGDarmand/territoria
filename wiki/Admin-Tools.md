# Admin tools

Players with `territoria.admin` see a **hammer** at the bottom of the menu rail, above Settings.

## Panel sections

| Section | What's inside |
|---|---|
| Economy | Pick the money source in plain words (items, Vault, command bridge) and its options |
| Costs | Creation cost, claim cost, upkeep, research cost, max tax |
| Countries | Member and claim limits, claim distance, markers, chest size, plot rent length |
| Power | Claims per active member, active days, claims per research level |
| Wars | War length, grief, capture time |
| Teleport | Home warm-up and cooldown |
| Server | Discord webhook |
| Moderation | Your tools (bypass, unclaim your chunk, reload) and every country: set bank or level, teleport, give your chunk, end wars, delete |
| Logs | The moderation history, newest first |

Every setting is checked on the server. **Save** writes `config/territoria-server.json`.

## Moderation log

Foundings, disbands, claims, wars, bank withdrawals and admin commands are logged, in the **Logs** section,
`/territoriaadmin logs` and `<world>/territoria/moderation.log`.

## Bypass

**Bypass: ON** (or `/territoriaadmin bypass`) lets you build and open everything in every claim until you turn it
off or log out.
