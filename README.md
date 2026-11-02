<p align="center">
  <img src="https://github.com/vhostyhq/.profile/blob/main/vhosty-wordmark.svg" alt="vhosty" width="320">
</p>

<h3 align="center">Herd for your tailnet.</h3>

<p align="center">
  Every folder becomes a private HTTPS site on your own domain,<br>
  reachable from your phone, laptop, or any device on your <a href="https://tailscale.com">Tailscale</a> network.
</p>

```
~/Sites/escrow   →  https://escrow.yourdomain.dev
~/Sites/kudos    →  https://kudos.yourdomain.dev
localhost:5173   →  https://5173.yourdomain.dev
```

- **Real HTTPS.** A trusted Let's Encrypt wildcard certificate. No browser warnings, no local CA.
- **Private.** Only your tailnet can reach your sites. Nothing is exposed to the internet and no router ports are opened.
- **No per-site setup.** Drop a folder in and it's live.
- **PHP your way.** Several versions side by side, pinned per site, with per-site settings and extension checks.
- **Built for an always-on dev box.** Run your projects and coding agents on one machine, and check on them from anywhere.

Runs on **Linux** (systemd) and **macOS** (launchd), and works alongside [Laravel Herd](https://herd.laravel.com).

## Projects

| | |
|---|---|
| **[vhosty](https://github.com/vhostyhq/vhosty)** | The server setup and CLI: Caddy, PHP-FPM, Tailscale Serve, DNS, Docker services, and `vhosty doctor` to keep it all healthy. |
| **[vite-plugin](https://github.com/vhostyhq/vite-plugin)** | [`@vhosty/vite-plugin`](https://www.npmjs.com/package/@vhosty/vite-plugin): HTTPS and hot reload for Vite at `https://<port>.<your-domain>`, with no config. |

## Get started

```bash
curl -fsSL https://raw.githubusercontent.com/vhostyhq/vhosty/main/install.sh | bash
vhosty setup
```

You'll need Tailscale, a domain whose DNS is on Cloudflare (or another [supported provider](https://github.com/vhostyhq/vhosty#dns-providers)), and an API token for it. Setup handles the rest.

Then add the Vite plugin to your projects:

```bash
npm i -D @vhosty/vite-plugin
```

## Learn more

- [How it works](https://github.com/vhostyhq/vhosty#how-it-works)
- [Using vhosty with Laravel Herd](https://github.com/vhostyhq/vhosty#with-laravel-herd-macos)
- [Laravel + Vite guide](https://github.com/vhostyhq/vhosty/blob/main/docs/laravel-vite.md)
- [Running vhosty on a cloud VM](https://github.com/vhostyhq/vhosty/blob/main/docs/instabox.md)
- [Contributing](https://github.com/vhostyhq/vhosty/blob/main/CONTRIBUTING.md)

<sub>MIT licensed. Found a bug or have an idea? <a href="https://github.com/vhostyhq/vhosty/issues">Open an issue</a>.</sub>
