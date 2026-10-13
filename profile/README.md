<!-- Hero -->
<p>
  <a href="https://tame.gg">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/profile/assets/hero-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="/profile/assets/hero-light.svg">
      <img src="/profile/assets/hero-dark.svg" width="100%" alt="tame.gg: Minecraft server software, Hypixel stats and everyday tools. Lines run from one tame.gg hub to five projects that light up in turn: tame.gg/stats for Hypixel stats, Flavor for Tailscale and Headscale networks, Lychee for downloads, Silk for Minecraft servers and Conduit, a Velocity-CTD proxy. Dotted lines lead to more projects.">
    </picture>
  </a>
</p>

**[tame.gg](https://tame.gg)** is a small, independent team building Minecraft server software, a Hypixel stats portal, and desktop tools we use ourselves. **[tame.gg/stats](https://tame.gg/stats)** tracks Hypixel players with nightly snapshots, leaderboards, trust tags and a Discord bot. **[Silk](https://tame.gg/projects/silk)** and **[Conduit](https://tame.gg/projects/conduit)** run the server and proxy side of a network. **[Flavor](https://tame.gg/projects/flavor)** and **[Lychee](https://tame.gg/projects/lychee)** are desktop apps for Linux, macOS and Windows. The site itself is closed source; every GitHub repository linked below is public.

<!-- Calls to action. Every button has light and dark variants. -->
<p>
  <a href="https://tame.gg"><picture><source media="(prefers-color-scheme: dark)" srcset="/profile/assets/buttons/website-dark.svg"><img src="/profile/assets/buttons/website-light.svg" height="44" alt="Visit tame.gg"></picture></a>
  <a href="https://tame.gg/stats"><picture><source media="(prefers-color-scheme: dark)" srcset="/profile/assets/buttons/stats-dark.svg"><img src="/profile/assets/buttons/stats-light.svg" height="44" alt="Open tame.gg/stats, the Hypixel stats portal"></picture></a>
  <a href="https://tame.gg/projects"><picture><source media="(prefers-color-scheme: dark)" srcset="/profile/assets/buttons/projects-dark.svg"><img src="/profile/assets/buttons/projects-light.svg" height="44" alt="All projects on tame.gg"></picture></a>
  <a href="#contribute"><picture><source media="(prefers-color-scheme: dark)" srcset="/profile/assets/buttons/contribute-dark.svg"><img src="/profile/assets/buttons/contribute-light.svg" height="44" alt="Jump to the Contribute section"></picture></a>
</p>

## Projects

<!-- tame.gg/stats -->
<p>
  <a href="https://tame.gg/stats">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/profile/assets/projects/stats-dark.svg">
      <img src="/profile/assets/projects/stats-light.svg" width="100%" alt="tame.gg/stats, a Hypixel stats portal: Hypixel data is snapshotted, turned into deltas, leaderboards and trust tags, shown on player pages, and served to the Discord bot and the partner API.">
    </picture>
  </a>
</p>

[![Site: tame.gg/stats](https://img.shields.io/badge/site-tame.gg%2Fstats-E8B84A?style=flat-square&labelColor=15110A)](https://tame.gg/stats)
[![Discord bot stars](https://img.shields.io/github/stars/tame-gg/tame-stats-bot?style=flat-square&label=bot%20stars&labelColor=15110A&color=D9A63C)](https://github.com/tame-gg/tame-stats-bot)
[![Discord bot top language](https://img.shields.io/github/languages/top/tame-gg/tame-stats-bot?style=flat-square&labelColor=15110A&color=C99530)](https://github.com/tame-gg/tame-stats-bot)

**Every Hypixel stat, with its history.** tame.gg/stats snapshots Hypixel every night and keeps the history, so a player page shows how someone is trending, not only where they stand today.

- **Player pages** with daily snapshots and deltas across Bed Wars, SkyWars, Duels, Pit, UHC, Murder Mystery, Build Battle, Arcade and more.
- **Leaderboards and head-to-head comparisons** for every mode.
- **Ranks and trust tags** alongside each player.
- **A Discord bot** with slash commands that DMs you when players you watch come online. Its source is public.
- **A partner API** for integrations.

The Discord bot runs on Bun and discord.js and needs a token issued by tame.gg:

```sh
bun install
bun run register   # push slash command definitions to Discord
bun run dev
```

tame.gg is not affiliated with Mojang or Hypixel Inc.

**[Site](https://tame.gg/stats)** · **[Discord bot repository](https://github.com/tame-gg/tame-stats-bot)** · **[Service status](https://status.tame.gg)**

<br>

<!-- Flavor -->
<p>
  <a href="https://github.com/tame-gg/Flavor">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/profile/assets/projects/flavor-dark.svg">
      <img src="/profile/assets/projects/flavor-light.svg" width="100%" alt="Flavor: the desktop app and flavorctl talk to the flavord daemon, which keeps one embedded node per network on Tailscale and Headscale at the same time, merges them into one device list, and explains where a connection goes in the Connection Inspector.">
    </picture>
  </a>
</p>

[![Latest Flavor release](https://img.shields.io/github/v/release/tame-gg/Flavor?include_prereleases&style=flat-square&label=release&labelColor=15110A&color=E8B84A)](https://github.com/tame-gg/Flavor/releases)
[![Flavor stars](https://img.shields.io/github/stars/tame-gg/Flavor?style=flat-square&labelColor=15110A&color=D9A63C)](https://github.com/tame-gg/Flavor/stargazers)
[![Flavor license](https://img.shields.io/github/license/tame-gg/Flavor?style=flat-square&labelColor=15110A&color=C99530)](https://github.com/tame-gg/Flavor/blob/main/LICENSE)

**Several tailnets, connected side by side.** Flavor is a desktop app, CLI and per-user daemon for Linux, macOS and Windows that keeps Tailscale and Headscale networks connected at the same time, and tells you where a connection goes when two of them use the same address.

- **One node per network.** Each network runs as its own embedded Tailscale node (`tsnet`) with its own identity. You do not need `tailscaled`.
- **One device list.** Every device on every network in one searchable table, each shown with the network it belongs to.
- **Decisions you can read.** The Connection Inspector and `flavorctl explain` show which networks a destination exists on and why one answer wins; the Conflict Center lists every overlapping address, name and route.
- **Reach services without root.** `flavorctl forward` and `flavorctl socks` connect through the network you choose without changing system routing.
- **No telemetry, verifiable releases.** Checksums are signed with Sigstore and GPG, and rebuilding a release commit with the same toolchains produces identical files.

```bash
# macOS, from the tame-gg Homebrew tap
brew install tame-gg/tap/flavor
brew services start flavor
brew install --cask tame-gg/tap/flavor-desktop

# Arch Linux, from the AUR
yay -S flavor-bin
systemctl --user enable --now flavord

# Windows 11, with Scoop
scoop bucket add tame-gg https://github.com/tame-gg/scoop-bucket
scoop install tame-gg/flavor
```

Flavor is in beta. Release tarballs for other Linux distributions, and how to verify them, are covered in the [install guide](https://github.com/tame-gg/Flavor/wiki/Install).

**[Repository](https://github.com/tame-gg/Flavor)** · **[Project page](https://tame.gg/projects/flavor)** · **[Releases](https://github.com/tame-gg/Flavor/releases)** · **[Documentation](https://github.com/tame-gg/Flavor/wiki)**

<br>

<!-- Lychee -->
<p>
  <a href="https://github.com/tame-gg/lychee">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/profile/assets/projects/lychee-dark.svg">
      <img src="/profile/assets/projects/lychee-light.svg" width="100%" alt="Lychee: a link is checked for range support, split into blocks fetched over Wi-Fi, Ethernet and a USB tether at the same time, and assembled into one file.">
    </picture>
  </a>
</p>

[![Lychee release: coming soon](https://img.shields.io/badge/release-coming%20soon-E8B84A?style=flat-square&labelColor=15110A)](https://tame.gg/projects/lychee)
[![Lychee stars](https://img.shields.io/github/stars/tame-gg/lychee?style=flat-square&labelColor=15110A&color=D9A63C)](https://github.com/tame-gg/lychee/stargazers)
[![Lychee license](https://img.shields.io/github/license/tame-gg/lychee?style=flat-square&labelColor=15110A&color=C99530)](https://github.com/tame-gg/lychee/blob/main/LICENSE)

**One download, every connection you have.** Lychee is a download accelerator for Windows, macOS and Linux. It fetches one file over several connections at once, and over several networks: with Wi-Fi and a phone tethered over USB, both work on the same download. Lychee is based on [Plexo](https://github.com/anmolkapil/plexo) (MIT).

- **Blocks, not halves.** Files are cut into blocks of up to 8 MB that every stream pulls from one queue, so a faster network simply takes more of them.
- **No slow finish.** Near the end, a free stream races a slow block, and the first to finish wins.
- **Safe pause and resume.** Before resuming, Lychee checks that the file on the server has not changed, and refuses rather than mixing two versions.
- **Torrents too.** Magnet links and `.torrent` files, with peers spread across your networks.
- **Limits and a browser handoff.** Per-network speed and data limits, a download schedule, and a Download with Lychee extension for Chrome, Edge, Brave, Arc and Firefox that only talks to the app on `127.0.0.1`.

```bash
git clone https://github.com/tame-gg/lychee.git
cd lychee
npm install
npm run dev
```

It needs no VPN, virtual adapter, kernel extension or administrator rights.

**[Repository](https://github.com/tame-gg/lychee)** · **[Project page](https://tame.gg/projects/lychee)** · **[Releases](https://github.com/tame-gg/lychee/releases)**

<br>

<!-- Silk -->
<p>
  <a href="https://github.com/tame-gg/Silk">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/profile/assets/projects/silk-dark.svg">
      <img src="/profile/assets/projects/silk-light.svg" width="100%" alt="Silk: each plugin goes through a compatibility check, where silk-supported and folia-supported plugins are accepted and unmarked plugins can run with warnings, then the world is ticked in regions on Folia's regional threading.">
    </picture>
  </a>
</p>

[![Latest Silk release](https://img.shields.io/github/v/release/tame-gg/Silk?style=flat-square&label=release&labelColor=15110A&color=E8B84A)](https://github.com/tame-gg/Silk/releases)
[![Silk stars](https://img.shields.io/github/stars/tame-gg/Silk?style=flat-square&labelColor=15110A&color=D9A63C)](https://github.com/tame-gg/Silk/stargazers)
[![Silk license](https://img.shields.io/github/license/tame-gg/Silk?style=flat-square&labelColor=15110A&color=C99530)](https://github.com/tame-gg/Silk/blob/main/LICENSE)

**Multithreaded, and still runs your plugins.** Silk is a Minecraft server platform built on Folia's regional multithreading, with plugin compatibility as the default rather than an afterthought.

- **Regional multithreading.** Keeps Folia's architecture, where separate regions of the world tick in parallel.
- **Compatibility first.** Plugins marked `silk-supported` or `folia-supported` load as compatibility-aware; unmarked plugins can be allowed with warnings instead of being blocked outright.
- **Fails safe.** Unsafe assumptions still fail safely where the server cannot preserve correctness.
- **Built-in reports.** `/silk status`, `/silk plugins` and `/silk report <plugin>` show region load and each plugin's compatibility report; `/tpsbar` and `/rambar` add live boss bars.

```bash
java -Xms4G -Xmx4G -jar silk-paperclip-v0.2.8-alpha.jar nogui
```

Silk is alpha, targets Minecraft 26.3 and builds with JDK 25. Each release also ships the patches it was built from.

**[Repository](https://github.com/tame-gg/Silk)** · **[Project page](https://tame.gg/projects/silk)** · **[Releases](https://github.com/tame-gg/Silk/releases)**

<br>

<!-- Conduit -->
<p>
  <a href="https://github.com/tame-gg/conduit">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/profile/assets/projects/conduit-dark.svg">
      <img src="/profile/assets/projects/conduit-light.svg" width="100%" alt="Conduit: a player connection passes the per-source throttle, the bot filter and the version gate, then reaches Paper, Spigot, Fabric, Forge or NeoForge backends.">
    </picture>
  </a>
</p>

[![Latest Conduit release](https://img.shields.io/github/v/release/tame-gg/conduit?style=flat-square&label=release&labelColor=15110A&color=E8B84A)](https://github.com/tame-gg/conduit/releases/latest)
[![Conduit stars](https://img.shields.io/github/stars/tame-gg/conduit?style=flat-square&labelColor=15110A&color=D9A63C)](https://github.com/tame-gg/conduit/stargazers)
[![Conduit license](https://img.shields.io/github/license/tame-gg/conduit?style=flat-square&labelColor=15110A&color=C99530)](https://github.com/tame-gg/conduit/blob/main/LICENSE)

**Velocity, with the plugins built in.** Conduit is a fork of [Velocity-CTD](https://github.com/GemstoneGG/Velocity-CTD) for people who run networks, modded or not. It folds the usual proxy-side plugin stack into the proxy and configures all of it from one `conduit.toml`.

- **Modded clients.** A configurable known-packs limit, a modded handshake cache, and NeoForge and Forge handling.
- **Floods and bots.** A per-source connection throttle, a bot filter, a channel guard for cheat channels, and an attack mode you can switch on live.
- **Operations.** Maintenance mode, a version gate, backend health checks, draining and fallback routing, all under `/conduit`.
- **Batteries included.** LuckPerms and spark are bundled and installed on first run, and step aside if you manage your own.
- **Drop-in.** Existing Velocity plugins and your existing `velocity.toml` keep working.

```bash
git clone https://github.com/tame-gg/conduit.git
cd conduit
./scripts/setup.sh   # clones upstream Velocity-CTD and applies Conduit patches
./gradlew build
```

Building needs Java 25 or newer. On first run, Conduit writes an annotated `conduit.toml` next to `velocity.toml`.

**[Repository](https://github.com/tame-gg/conduit)** · **[Project page](https://tame.gg/projects/conduit)** · **[Releases](https://github.com/tame-gg/conduit/releases)**

<br>

<!-- More projects and install channels -->
### More from tame.gg

<p>
  <a href="https://github.com/tame-gg/homebrew-tap">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="/profile/assets/channels-dark.svg">
      <img src="/profile/assets/channels-light.svg" width="100%" alt="Install channels: the tame-gg Homebrew tap carries Flavor, the Flavor desktop app, FreshLock and Powerflow, and the tame-gg Scoop bucket carries Flavor for Windows.">
    </picture>
  </a>
</p>

Our macOS apps and Flavor install from the [Homebrew tap](https://github.com/tame-gg/homebrew-tap); Flavor for Windows installs from the [Scoop bucket](https://github.com/tame-gg/scoop-bucket).

```bash
brew tap tame-gg/tap
brew trust tame-gg/tap   # Homebrew 6+
```

| Project | What it is |
| --- | --- |
| [Palladium](https://github.com/tame-gg/palladium) | The tame.gg fork of Leaf for performance-heavy Paper networks, with `/palladium perf` operator views. [Project page](https://tame.gg/projects/palladium) · [Releases](https://github.com/tame-gg/palladium/releases) |
| [FreshLock](https://github.com/tame-gg/freshlock) | macOS app locker: protect any app with Touch ID, Apple Watch or your Mac password. `brew install --cask tame-gg/tap/freshlock` · [Project page](https://tame.gg/projects/freshlock) |
| [Kestrel](https://tame.gg/projects/kestrel) | Pre-release desktop system monitor: one row per app, 30 days of history, listening ports mapped to their apps. |
| [Pulse](https://github.com/tame-gg/pulse) | Apple Silicon menu bar system monitor and thermal control. |
| [Powerflow](https://github.com/tame-gg/powerflow) | Mac power and charging monitor; a fork of [lzt1008/powerflow](https://github.com/lzt1008/powerflow) with macOS 27 fixes. `brew install --cask tame-gg/tap/powerflow` |
| [NotchAgent](https://github.com/tame-gg/NotchAgent) | Real-time status of local AI coding agents in the MacBook notch. |
| [Swords Launcher](https://github.com/tame-gg/swordslauncher) | Minecraft launcher for managing several installations; a fork of Prism Launcher, itself a fork of MultiMC. |
| [Universe](https://github.com/tame-gg/Universe) | Single-JAR cluster orchestrator for deploying application instances across nodes. |
| [conduit-native](https://github.com/tame-gg/conduit-native) | An independent Minecraft proxy with its own protocol stack and ViaVersion bundled; not a Velocity fork. |
| [koels.net](https://koels.net) | Kyle's personal site. |

<!-- How we build -->
## How we build

<table>
  <tbody>
    <tr>
      <td width="50%" valign="top">
        <b>Upstream gets the credit</b><br>
        Lychee is based on Plexo (MIT). Conduit is built on Velocity-CTD, Silk on Folia and Paper, and Palladium on Leaf, Purpur and Paper. Each README names what it inherits.
      </td>
      <td width="50%" valign="top">
        <b>Nothing phones home</b><br>
        Flavor has no telemetry and turns off Tailscale's log upload. Lychee's browser extension only talks to the app on <code>127.0.0.1</code>. FreshLock is local-only by default, with no network calls.
      </td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td width="50%" valign="top">
        <b>Tools for the people running it</b><br>
        Conduit has <code>/conduit</code> diagnostics and a Prometheus endpoint, Silk has <code>/silk status</code> and per-plugin reports, and Palladium has <code>/palladium perf</code>.
      </td>
      <td width="50%" valign="top">
        <b>Releases you can check</b><br>
        Flavor signs its checksums with Sigstore and GPG and builds reproducibly. Palladium and FreshLock ship a SHA-256 checksum file next to their release downloads.
      </td>
    </tr>
  </tbody>
</table>

<!-- Tech stack -->
| | tame.gg/stats | Flavor | Lychee | Silk | Conduit |
| --- | --- | --- | --- | --- | --- |
| **Built with** | Discord bot: TypeScript, Bun, discord.js | Go daemon, Tauri 2 shell in Rust, React interface | Electron, React 19, TypeScript, Tailwind CSS | Java, Gradle with Paperweight patches | Java, Gradle, overlays applied to upstream |
| **Built on** | Hypixel data, snapshotted nightly | Tailscale `tsnet`, Connect, gVisor | Plexo, WebTorrent | Folia and Paper | Velocity-CTD |
| **Runs on** | The web and Discord | Linux, macOS, Windows 11 (x86_64 and arm64) | Windows, macOS, Linux | Minecraft 26.3 on JDK 25 | Proxy for Paper, Spigot, Fabric, Forge and NeoForge |
| **Tests** | — | Go, Rust and frontend tests, Headscale acceptance tests | Playwright end-to-end tests | Gradle build and test suite | — |
| **Stage** | Live | Beta | Beta (release candidates) | Alpha | 1.x releases |
| **License** | — | MIT | MIT | GPL-3.0 | GPL-3.0 |

<!-- Contribute -->
## Contribute

Flavor, Lychee, Silk and Conduit all take pull requests. Each project's guide covers setup and the checks to run; read it before starting on a larger change, and keep pull requests focused. Flavor's [code of conduct](https://github.com/tame-gg/Flavor/blob/main/CODE_OF_CONDUCT.md) applies to everyone taking part in that project.

| | Flavor | Lychee | Silk | Conduit |
| --- | --- | --- | --- | --- |
| **Bugs and ideas** | [Open an issue](https://github.com/tame-gg/Flavor/issues/new/choose) | Issues are off; start with the [contributing guide](https://github.com/tame-gg/lychee/blob/main/CONTRIBUTING.md) | [Open an issue](https://github.com/tame-gg/Silk/issues/new/choose) | [Open an issue](https://github.com/tame-gg/conduit/issues/new) |
| **Local setup** | [CONTRIBUTING.md](https://github.com/tame-gg/Flavor/blob/main/CONTRIBUTING.md) | [CONTRIBUTING.md](https://github.com/tame-gg/lychee/blob/main/CONTRIBUTING.md) | [CONTRIBUTING.md](https://github.com/tame-gg/Silk/blob/main/CONTRIBUTING.md) | [Maintaining the fork](https://github.com/tame-gg/conduit#maintaining-the-fork) |
| **Before review** | `go vet`, `go test`, `npm test`, `cargo test` | `npm run lint`, `typecheck`, `test:e2e:smoke` | `./gradlew applyAllPatches` and `build`, with test evidence | Re-run setup and `./gradlew build` |

<!-- Security -->
## Security

> [!WARNING]
> Report vulnerabilities privately. Do not open a public issue, pull request or discussion for a security problem.

Flavor takes reports through [GitHub private vulnerability reporting](https://github.com/tame-gg/Flavor/security/advisories/new), as its [SECURITY.md](https://github.com/tame-gg/Flavor/blob/main/SECURITY.md) describes. FreshLock takes reports by email at security@tame.gg, per its [SECURITY.md](https://github.com/tame-gg/freshlock/blob/main/SECURITY.md). For every other project, contact the maintainers privately, for example at hey@tame.gg, the contact address on [tame.gg](https://tame.gg), and leave time for a fix before disclosure.

<!-- Footer -->
<br>

<a href="https://tame.gg"><img src="/profile/assets/divider.svg" width="100%" alt="tame.gg divider: a gold line runs out from a gold diamond at the center"></a>

<p align="center">
  <a href="https://tame.gg">tame.gg</a> &nbsp;·&nbsp; <a href="https://tame.gg/stats">stats</a> &nbsp;·&nbsp; <a href="https://tame.gg/projects">projects</a> &nbsp;·&nbsp; <a href="https://status.tame.gg">status</a> &nbsp;·&nbsp; <a href="https://github.com/tame-gg/homebrew-tap">homebrew tap</a>
</p>
