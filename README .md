# WPBL · Where the World Plays

An interactive world map showcasing the hometowns of every player in the Women's Pro Baseball League.

## Features

- 🌍 **Interactive world map** - click any pin to see which players are from that area
- 🎨 **Color-coded by team** - Boston (red), Los Angeles (blue), New York (navy), San Francisco (orange)
- 🔢 **Multi-player pins** - pins show a number when multiple players share a region
- 🖼️ **Player cards** - photos, team, and position
- 🔗 **Direct links** - click a player card to open their official WPBL profile
- 🏷️ **Team filter** - filter the map to show only one team at a time
- 📊 **Live stats** - player count, countries, and hometown count update with the filter

## Teams

| Team | Color |
|------|-------|
| Boston | Red `#268040` |
| Los Angeles | Blue `#475da9` |
| New York | Navy `#299598` |
| San Francisco | Orange `#8152a0` |

## Hosting on GitHub Pages

### First-time setup

1. Create a new GitHub repository (e.g., `wpbl-player-map`)
2. Push this folder's contents to the `main` branch
3. Go to **Settings → Pages**
4. Under **Source**, select **GitHub Actions**
5. Push any commit - the workflow will deploy automatically

Your site will be live at:
```
https://<your-username>.github.io/<your-repo-name>/
```

### Updating player data

All player data lives in the `PLAYERS` array inside `index.html`. Each entry looks like:

```js
{ name:"Player Name", team:"Boston", pos:"RHP",
  photo:"https://...",
  coords:[lat, lng], location:"City, Country" },
```

Just edit `index.html`, commit, and push - the GitHub Action redeploys automatically.

## Tech Stack

- Pure HTML/CSS/JavaScript (no build step needed)
- [Leaflet.js](https://leafletjs.com/) for the map
- OpenStreetMap tiles
- Google Fonts (Bebas Neue + DM Sans)
- GitHub Actions for CI/CD
