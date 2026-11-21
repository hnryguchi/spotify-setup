# My Spotify with Spicetify

[Português](README.md) · **English**

The Spotify I use on my computer: translucent theme, live lyrics and a background that changes with the album cover.
Everything is installed through **Spicetify**, no coding required. It takes about 5 minutes.

**Follow me:** [open.spotify.com/user/31ilerrhi3kodpoigqprs65xdrz4](https://open.spotify.com/user/31ilerrhi3kodpoigqprs65xdrz4)

## What's in my setup

| Type | Name | What it does |
|---|---|---|
| Theme | [Hazy](https://github.com/Astromations/Hazy) | translucent look, with the blurred album cover in the background |
| Extension | [Beautiful Lyrics](https://github.com/surfbryce/beautiful-lyrics) | word-by-word synced lyrics with a dynamic background |
| Extension | [Spicy Lyrics](https://github.com/Spikerko/spicy-lyrics) | another full-screen live lyrics view |
| Extension | [SpicyThemes](https://github.com/7xeh/SpicyThemes) | themes for the Spicy Lyrics screen |

## Step by step (Windows)

**1. Install Spotify from the official website**, not from the Microsoft Store: [spotify.com/download](https://www.spotify.com/download/).
The Store version does not work with Spicetify. Open Spotify once, log in and close it.

**2. Install Spicetify.** Open **PowerShell** (Start menu → type "PowerShell") and paste:

```powershell
iwr -useb https://raw.githubusercontent.com/spicetify/cli/main/install.ps1 | iex
```

When it asks *"Do you also want to install Spicetify Marketplace?"*, press **Enter** (yes).

**3. Open Spotify.** A new **Marketplace** tab will appear in the Spotify menu.

**4. Install the theme and extensions from the Marketplace:**
- **Themes** tab → search for **Hazy** → **Install**;
- **Extensions** tab → search for and install **Beautiful Lyrics**, **Spicy Lyrics** and **SpicyThemes**.

Done. Play a song and open the lyrics (microphone icon) to see the live lyrics.

<details>
<summary><b>macOS / Linux</b></summary>

In the Terminal:

```bash
curl -fsSL https://raw.githubusercontent.com/spicetify/cli/main/install.sh | sh
```

Then continue from step 3. On Linux, Spotify installed via Snap does not work; use the `.deb`/`.rpm` package or Flatpak (see the [documentation](https://spicetify.app/docs/advanced-usage/installation)).
</details>

## If Spotify updates and the look disappears

Spotify updates undo Spicetify. In PowerShell:

```powershell
spicetify update
spicetify backup apply
```

If that fails, `spicetify restore backup apply` usually fixes it.

## To go back to regular Spotify

```powershell
spicetify restore
```

## Good to know

- Spicetify is **not an official** Spotify product. It only modifies the app on your computer; your account and playlists are not affected.
- The themes and extensions are made by other people (links in the table above). Credit goes to them.
- Official documentation: [spicetify.app](https://spicetify.app).

---

> © Henry Noguchi. **All rights reserved.** Public for viewing only; copying, reuse or presenting it as your own requires permission. See [LICENSE](LICENSE).
