# Map, minimap & HUD

## World map (`M`)

A live map of the terrain you have explored, with every country's land in its color. It is saved on your computer
for each world separately: a new world (even with the same name, or a server that was reset) starts with a blank
map. Your personal markers are kept per world the same way.

- drag to move, scroll to zoom, `Space` recenters on you;
- players who can claim select chunks with the left button and move the map with the **right** button; their
  right-click menu also claims or releases the selection (see [Territory & claims](Territory-and-Claims.md));
- `E` closes the map (and every Territoria menu), like it closes a chest;
- hover a chunk to see who owns it;
- capitals are marked with a star.

### Markers

Countries can put **markers** on the map (*Manage markers* rule): home, flag, star, sword, skull, pickaxe,
diamond, anchor… with a name. One of them can be the **Capital**. Markers show on every member's map, minimap and
compass. The server limits how many each country has (`max_markers`).

## Minimap

A corner minimap with the land around you and the country you stand in. In your personal settings you choose:

- on / off, size, which corner;
- coordinates shown or hidden;
- zoom with **`Z`**.

## Borders in the world

Country borders can be drawn in the world as light walls along the chunk edges, so you see where land starts.

## Compass

Off by default: turn it on in your personal settings (**HUD** card). A compass strip at the top of the screen shows the cardinal points, your heading in degrees, and the direction of
capitals and markers, so you can walk to them. It can be turned off in the settings.

## Personal settings (gear icon)

Everything about your own screen, and only yours:

- **World**: country borders drawn in the world, also in caves or not;
- **HUD**: minimap (size, corner, coordinates), compass, the banner when entering a country;
- **Country**: country tags in chat, country chat mode, the country sidebar, auto-claim.

Long pages scroll with the mouse wheel when the window is small (big GUI scale).
