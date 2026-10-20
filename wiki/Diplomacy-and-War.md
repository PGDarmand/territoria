# Diplomacy & war

Needs the *Diplomacy & wars* rule.

## Relations

In the **Diplomacy** tab, every other country is **Neutral**, **Ally** or **Enemy**.

- **Ally**: you send a request, and they must accept. Allies' members get the *Ally* role in your land, and you can
  give them an [embassy](Plots-Rentals-and-Embassies.md#embassies).
- **Enemy**: one side can declare it alone. Only enemies can go to war.
- **Neutral**: back to normal (this also ends an alliance and its embassies).

## War

1. Declare war on an enemy country (Diplomacy tab, or `/country war <name>`).
2. The war lasts `war_hours` (24 h by default). With `war_grief` on, both sides can build and break in each
   other's land.
3. **Capturing land**: stand in an enemy chunk and start a capture (*Capture enemy land* rule, or
   `/country capture`). It takes `capture_seconds`. The capture pauses while a defender is in the chunk and
   cancels if you leave or die. Then the chunk becomes yours, and flags standing in it switch to your flag.
4. The war ends when the time is up, when both sides propose **peace**, or when one side **surrenders**.

When a side surrenders, its members get a **DEFEAT** screen and the winners a **VICTORY** screen.

Wars, foundings and disbands can be posted to Discord by the server (`discord_webhook`).
