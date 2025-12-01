# be-privacy-filters

Opinionated Belgian privacy filter collection for Pi-hole and uBlock Origin.

## Lists

**Pi-hole (DNS level)**  
- `pihole-be-hosts.txt`  
  Extra DNS blocklist for Belgian-oriented tracking and analytics endpoints, in hosts-file format.

**uBlock Origin (browser level)**  
- `ubo-be-tracking.txt`  
  Network filters (Adblock syntax) for Belgian sites.  
- `ubo-be-cosmetic.txt`  
  Cosmetic filters for hiding leftover ad placeholders and consent trash on Belgian sites.

All lists are designed to complement, **not replace**, big community lists like OISD, EasyList and EasyPrivacy.

---

## Raw URLs

- Pi-hole:  
  `https://raw.githubusercontent.com/Koen88/be-privacy-filters/main/pihole-be-hosts.txt`

- uBlock Origin – tracking:  
  `https://raw.githubusercontent.com/Koen88/be-privacy-filters/main/ubo-be-tracking.txt`

- uBlock Origin – cosmetic:  
  `https://raw.githubusercontent.com/Koen88/be-privacy-filters/main/ubo-be-cosmetic.txt`

---

## How to use

### Pi-hole

1. Go to **Group Management → Adlists**.  
2. Add the Pi-hole URL above as a new adlist.  
3. Assign it to the groups you want.  
4. Run **Tools → Update Gravity** or `pihole -g` on the CLI.

### uBlock Origin

1. Open uBO dashboard → **Filter lists**.  
2. Scroll to **Import…** at the bottom.  
3. Paste the two uBO URLs (tracking + cosmetic), one per line.  
4. Click **Apply changes**.

---

## Automatic releases

This repository can auto-create tags and GitHub releases when you push changes to `main`.

- Workflow file: `.github/workflows/release.yml`  
- Tag format: `vYYYY.MM.DD-HHMM` (for example `v2025.12.01-2359`).

You do **not** need to do anything manually: just commit and push; the workflow will:
- create (or move) a tag for the current date-time, and
- create a GitHub Release that bundles the current versions of the three lists.
