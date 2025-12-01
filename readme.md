# be-privacy-filters

Custom filters for Belgian users:

- `pihole-hosts-be.txt`  
  Extra DNS blocklist for Pi-hole (hosts format).

- `ubo-be-tracking.txt`  
  Network filters for uBlock Origin to block Belgian tracking domains.

- `ubo-be-cosmetic.txt`  
  Cosmetic filters for uBlock Origin to hide Belgian ad placeholders and banners.

Usage:

1. Pi-hole: add the *raw* URL of `pihole-hosts-be.txt` as a new adlist.
2. uBlock Origin: add the *raw* URLs of `ubo-be-tracking.txt` and `ubo-be-cosmetic.txt` as custom filter lists.
