<p align="center">
  <a href="https://github.com/afficho">
    <img src="https://raw.githubusercontent.com/afficho/afficho-brand/main/assets/icon.svg" width="96" height="96" alt="Afficho icon">
  </a>
</p>

<h1 align="center">afficho</h1>
<p align="center"><strong>Open source digital signage for everyone.</strong></p>

<p align="center">
Turn any screen into a smart display. Push content to one device or a thousand&nbsp;&mdash;&nbsp;from a Raspberry Pi on the wall to a fleet across the globe.
</p>

---

### Why Afficho?

Most digital signage platforms lock you in: proprietary software, mandatory cloud subscriptions, opaque pricing. Afficho takes a different approach.

- **Free and open source.** Self-host the client, manage content locally, no account needed.
- **Cloud when you want it.** [Afficho Cloud](https://github.com/afficho/afficho-cloud) adds fleet management, remote content push, and monitoring &mdash; for teams that need it.
- **Runs on anything.** Raspberry Pi, mini PCs, Android sticks, repurposed laptops. If it has a screen and runs Linux, it runs Afficho.
- **Dead simple.** Upload media, arrange a playlist, assign it to a screen. That's it.

### Repositories

| Repo | Description |
|------|-------------|
| [**afficho-client**](https://github.com/afficho/afficho-client) | The on-device daemon &mdash; manages content, drives the display, serves the local admin UI. Written in Go. |
| [**afficho-cloud**](https://github.com/afficho/afficho-cloud) | Multi-tenant SaaS backend for fleet management, content distribution, and remote control. |
| [**afficho-types**](https://github.com/afficho/afficho-types) | Shared wire-format types for the client&ndash;cloud protocol. |
| [**afficho-brand**](https://github.com/afficho/afficho-brand) | Brand assets, design tokens, and style guide. |

### How it works

```
 ┌──────────────────┐         ┌──────────────────┐
 │   Afficho Cloud  │  WSS    │  afficho-client   │
 │   (optional)     │────────▶│  on your device   │
 │   Fleet mgmt     │         │                   │
 └──────────────────┘         │  ┌──────────────┐ │
                              │  │   Chromium    │ │
 ┌──────────────────┐  HTTP   │  │   (kiosk)     │ │
 │   Local Admin UI │────────▶│  │   ┌────────┐  │ │
 │   (browser)      │         │  │   │ Screen │  │ │
 └──────────────────┘         │  │   └────────┘  │ │
                              │  └──────────────┘ │
                              └──────────────────┘
```

1. **Install** the client on a device connected to a display
2. **Upload** images, videos, or web pages through the local admin UI (or push from the cloud)
3. **Schedule** playlists &mdash; the screen plays your content in a loop
4. **Scale** with Afficho Cloud when you need centralized management

---

<p align="center">
  <sub>From the French <em>afficher</em> &mdash; to display, to put up a notice.</sub>
</p>
