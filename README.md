# redirect

This repository contains the Vercel redirect configuration for Prodigy Origin extension links.

## What it does

- Routes `firefox.prodigyorigin.com` to the Firefox Add-ons listing
- Routes `edge.prodigyorigin.com` to the Microsoft Edge Add-ons listing
- Routes `chrome.prodigyorigin.com` → **temporary** → `prodigyorigin.com/get` (Chrome Web Store unavailable)
- Routes `extension.prodigyorigin.com` → **temporary** → `prodigyorigin.com/get` (Chrome Web Store unavailable)

> **Temporary:** `chrome.prodigyorigin.com` and `extension.prodigyorigin.com` previously linked directly to
> store listings. They now redirect to the website's /get page while Prodigy Origin is unavailable on the
> Chrome Web Store. Restore the original rules once the Chrome listing is reinstated.

## Files

- `vercel.json`: redirect rules and status codes
- `public/index.html`: minimal static fallback page
