# be-privacy-filters

A collection of custom blocklists and filter rules focused on Belgian websites, media platforms, tracking infrastructure, and regional advertising networks.
These lists are intended to complement existing global filter sets (OISD, EasyPrivacy, AdGuard, StevenBlack, etc.) by covering domains and tracking endpoints that are commonly used in Belgium but are often missing from international lists.
All filters are generated and maintained based on real network traffic analysis, Pi-hole query logs, and uBlock Origin logger data.

## Repository structure
```
be-privacy-filters/
├── pihole/
│   └── pihole-be-blocklist.txt
├── ubo/
│   ├── ubo-be-tracking.txt
│   └── ubo-be-cosmetic.txt
└── README.md
```

## Pi-hole blocklist (DNS level)

File: pihole/pihole-be-blocklist.txt  
Format: hosts (0.0.0.0 domain)

This list blocks Belgian-focused tracking and advertising domains, including:

- DPG Media (HLN, Nieuwsblad, HBvL, GVA, VTM)
- Mediahuis tracking
- VRT and VRT MAX analytics
- Streamz, RTL Play, VTM GO measurement domains
- Banking telemetry (Belfius, Argenta)
- Contentsquare, Kaching, Pexi, Smartocto, Refinery89
- Various third-party trackers heavily used in Belgium

To use in Pi-hole:

1. Open Pi-hole admin panel  
2. Group Management → Adlists  
3. Add this URL:  
   https://raw.githubusercontent.com/Koen88/be-privacy-filters/main/pihole/pihole-be-blocklist.txt  
4. Save → Update Gravity

---

## uBlock Origin network filters

File: ubo/ubo-be-tracking.txt  
Type: network filtering rules (Adblock/uBO syntax)

Blocks:

- Belgian tracking endpoints
- analytics APIs
- measurement beacons
- consent and telemetry scripts
- ad-delivery CDNs
- profiling and engagement frameworks

To use in uBlock Origin:

1. Open Dashboard  
2. Go to Filter lists  
3. Under “Custom”, add:  
   https://raw.githubusercontent.com/Koen88/be-privacy-filters/main/ubo/ubo-be-tracking.txt  
4. Apply changes

---

## uBlock Origin cosmetic filters

File: ubo/ubo-be-cosmetic.txt  
Type: cosmetic (element hiding) rules

Hides visible ad placeholders and UI elements on Belgian media sites:

- HLN  
- Nieuwsblad / HBvL / GVA  
- De Standaard  
- VRT / VRT MAX  
- Streamz  
- RTL / RTLplay  
- Voetbalkrant  

To use in uBlock Origin:

Add this URL:  
https://raw.githubusercontent.com/Koen88/be-privacy-filters/main/ubo/ubo-be-cosmetic.txt  
Then apply changes.

---

## Project aims

- Provide improved coverage for Belgian tracking where global lists fall short  
- Reduce analytics, tracking, profiling and UX-measurement scripts  
- Maintain site functionality (no aggressive breakage)  
- Keep filters simple, stable, and easy to maintain  
- Designed to work alongside major lists (OISD, EasyPrivacy, AdGuard, etc.)

---

## Contributing

Contributions are welcome.

You can help by submitting:

- uBlock Origin log samples  
- Pi-hole query logs  
- new Belgian tracking domains  
- cosmetic filter improvements  
- false positive reports  

Please open an issue or submit a pull request.

---

## Status

Actively maintained.  
Stable for daily use.  
Compatible with Pi-hole, AdGuard Home and uBlock Origin.
