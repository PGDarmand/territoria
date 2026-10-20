# Plots, rentals & embassies

A **plot** is a box inside your land (any size, like a WorldEdit selection) that you rent out: an apartment, a
shop, a market stall, a farm. The renter can build only inside the box. The rent goes to the country bank.

## Creating a plot

Needs the *Rent out plots* rule.

1. **Territory → Get wand** gives you the **Plot Wand**.
2. Left-click a block for corner 1, right-click another for corner 2. The selection is drawn in the world.
3. **Territory → New plot**: give it a name, a description, a price and a rent length in days
   (up to `plot_days`, 30 by default).

The whole box must be inside your land and can't overlap another plot. Plots can be edited (✎) or deleted (✖)
from the list. If a chunk is lost, the plots reaching into it go with it.

## Renting

**Country menu → Rentals** lists every plot on the server, from every country. Players without a country can use
it too.

- Filters: **All**, **Free**, **My rentals**, plus a search by plot or country name.
- Each card shows the country, name, description, size, coordinates, price and status.
- Pick how many **rent periods** to pay at once with **− ×N +**. The total is shown before you pay.
- **Rent** a free plot or **Extend** yours, from anywhere: no need to walk there.
- **Leave** gives the plot back (no refund).
- The map button opens the world map centered on the plot.

You can pay up to **12 periods** at once, and at most **365 days ahead** in total. When the rent runs out, the
plot is free again.

Walking into a plot also shows its card in the chat, with **[Rent]**, **[Extend]** and **[Leave]** buttons
(one period).

## Embassies

An **embassy** is a plot lent **for free** to an **allied** country. Every member of that country gets the
renter's rights inside the box: a place to build their embassy in your capital.

- In the plot editor, click the **Embassy** field to pick one of your allies (or *None* for an ordinary plot).
- An embassy can't be rented and doesn't appear in Rentals.
- A plot that is currently rented can't become an embassy until the rent ends.
- If the alliance ends, the embassy closes by itself and becomes an ordinary free plot again.
- In Territory, embassies show in blue as *Embassy · Country*.
