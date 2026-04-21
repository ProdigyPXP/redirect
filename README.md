# redirect

This repository contains the Vercel redirect configuration for Prodigy Origin extension links.

## What it does

- Routes `firefox.prodigyorigin.com` to the Firefox Add-ons listing
- Routes `edge.prodigyorigin.com` to the Microsoft Edge Add-ons listing
- Routes `chrome.prodigyorigin.com` to the Chrome Web Store listing
- Routes `extension.prodigyorigin.com` based on user agent:
  - Edge user agents → Edge listing
  - Firefox user agents → Firefox listing
  - All other user agents → Chrome listing

## Files

- `vercel.json`: redirect rules and status codes
- `public/index.html`: minimal static fallback page
