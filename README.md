# redirect

This repository contains the Vercel redirect configuration for Play Origin (formerly Prodigy Origin) extension links. The `prodigyorigin.com` domain is kept verbatim — see `../ProdigyOrigin/meta/REBRAND.md`.

## What it does

- Routes `firefox.prodigyorigin.com` to the Firefox Add-ons listing
- Routes `edge.prodigyorigin.com` to the Microsoft Edge Add-ons listing
- Routes `chrome.prodigyorigin.com` → **temporary** → `prodigyorigin.com/get` (Chrome Web Store unavailable)
- Routes `extension.prodigyorigin.com` → **temporary** → `prodigyorigin.com/get` (Chrome Web Store unavailable)

> **Temporary:** `chrome.prodigyorigin.com` and `extension.prodigyorigin.com` previously linked directly to
> store listings. They now redirect to the website's /get page while Play Origin is unavailable on the
> Chrome Web Store. Restore the original rules once the Chrome listing is reinstated.

## Files

- `vercel.json`: redirect rules and status codes
- `public/index.html`: minimal static fallback page

## playorig.in subdomains

| Subdomain | Destination | Status |
|---|---|---|
| `extension.playorig.in`, `ext.playorig.in` | `playorig.in/get` (temp, until store listings live) | 302 |
| `chrome.playorig.in` | `playorig.in/get` (temp, until Chrome Web Store listing) | 302 |
| `edge.playorig.in` | Microsoft Edge Add-ons listing | 301 |
| `firefox.playorig.in` | Firefox AMO listing | 301 |
| `discord.playorig.in`, `dsc.playorig.in` | `dsc.gg/ProdigyPXP` | 301 |
| `youtube.playorig.in`, `yt.playorig.in` | `youtube.com/@ProdigyPXP` | 301 |
| `github.playorig.in`, `gh.playorig.in` | `github.com/ProdigyPXP` | 301 |

DNS: `playorig.in` has a wildcard Vercel ALIAS — no per-subdomain DNS records needed.
All subdomains are served by the `origin-redirect` Vercel project.
