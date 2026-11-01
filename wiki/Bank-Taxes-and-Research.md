# Bank, taxes & research

## Bank

Every country has a bank. In the **Bank** tab:

- **Deposit**: any member can put money in;
- **Withdraw**: only roles with *Withdraw from the bank*;
- **Shift-click** Deposit to put in all the money you carry, or Withdraw to take the whole bank;
- the history lists the latest transactions (deposits, withdrawals, taxes, rent, fees, chest items);
- the ranking of contributors shows who gave the most.

Money comes from the server's economy: emeralds by default, or Vault, an economy mod or a command bridge
(see [Permissions & compatibility](Permissions-and-Compatibility.md)).

The bank pays the claim fees, the research levels and the daily upkeep.

### Treasury (server option)

When the server turns on `treasury` (items economy only), the money lives in a **Treasury** block in the world:

- get it from **Bank → Get the treasury block** and place it in your land (one per country);
- the Bank page then shows where it is, and deposits / withdrawals happen **at the block**: put currency in to
  deposit, take it out to withdraw (taking needs *Withdraw from the bank*);
- every treasury is shown on the map to **everyone**;
- enemies at war who may open containers during raids can **loot** it. Your members are warned;
- if it is broken or blown up, the money is safe: get a new block from the Bank page.

## Country chest

A shared chest (up to 6 rows, `chest_rows`) opened from the **Bank** tab, for roles with *Use the country chest*.
Every item added or taken is logged in the history. The **↩** button in the chest goes back to the country menu.

When a country is disbanded, its chest goes back to the leader: into the inventory, the rest at their feet (an
offline leader gets it at the next login).

## Taxes

Members with *Set taxes* choose a **tax**: one default amount, and optionally a different amount per role, and
how often it is paid with the **per hour / per day / per week** button. Once per period, every online member
(except the leader) pays their role's tax into the bank. A member who can't pay is told and tried again the next
period. The server caps the tax with `max_tax`, which is per day: a 24th of it per hour, 7 times it per week.

## Research

Research levels make your country bigger. Each level:

- costs money from the bank (`level_cost`, raised by `level_growth` % each level: 100 = it doubles);
- needs enough members and claims (`level_members` and `level_chunks` per level);
- adds `level_claims` extra claims, and if the server wants, `level_warps` warps and `level_member_slots` member
  slots.

The server picks how many levels there are (`max_level`, 5 by default, up to 50). The table below uses the defaults.

| Level | Members needed | Claims needed | Cost (default `level_cost` 100) |
|---|---|---|---|
| 0 → 1 | 2 | 5 | 100 |
| 1 → 2 | 3 | 10 | 200 |
| 2 → 3 | 4 | 15 | 400 |
| 3 → 4 | 5 | 20 | 800 |
| 4 → 5 | 6 | 25 | 1600 |

Level 5 is the maximum. Buy levels from the **Research** tab (*Buy research levels* rule).
