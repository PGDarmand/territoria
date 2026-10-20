# Bank, taxes & research

## Bank

Every country has a bank. In the **Bank** tab:

- **Deposit**: any member can put money in;
- **Withdraw**: only roles with *Withdraw from the bank*;
- the history lists the latest transactions (deposits, withdrawals, taxes, rent, fees, chest items);
- the ranking of contributors shows who gave the most.

Money comes from the server's economy: emeralds by default, or Vault, an economy mod or a command bridge
(see [Permissions & compatibility](Permissions-and-Compatibility.md)).

The bank pays the claim fees, the research levels and the daily upkeep.

## Country chest

A shared chest (up to 6 rows, `chest_rows`) opened from the **Bank** tab, for roles with *Use the country chest*.
Every item added or taken is logged in the history.

## Taxes

Members with *Set taxes* choose a **daily tax**: one default amount, and optionally a different amount per role.
Once per real day, every online member (except the leader) pays their role's tax into the bank. A member who
can't pay is told and tried again the next day. The server caps the tax with `max_tax`.

## Research

Research levels make your country bigger. Each level:

- costs money from the bank (`level_cost`, doubling every level);
- needs enough members and claims;
- adds `level_claims` extra claims.

| Level | Members needed | Claims needed | Cost (default `level_cost` 100) |
|---|---|---|---|
| 0 → 1 | 2 | 5 | 100 |
| 1 → 2 | 3 | 10 | 200 |
| 2 → 3 | 4 | 15 | 400 |
| 3 → 4 | 5 | 20 | 800 |
| 4 → 5 | 6 | 25 | 1600 |

Level 5 is the maximum. Buy levels from the **Research** tab (*Buy research levels* rule).
