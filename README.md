# Online-Gambling-Sites-on-Philippines-for-Network-Denylist-or-Pi-Hole

List of Online Gambling domains common in the Philippines for network denylists / Pi-hole.

Credit to u/Elegant-Fox-3652 on Reddit

Reddit Post: https://www.reddit.com/r/InternetPH/comments/1p7q42d/list_of_online_gambling_sites_for_network_denylist/

Extra PH domains added from PAGCOR registered domain lists and community reports.

## Files

| File | Use for |
| --- | --- |
| `Sugal-Domain.txt` | Plain domains (router/firewall denylist, Pi-hole gravity-style adlist) |
| `Sugal-Domain-PiHole-Regex.txt` | Pi-hole regex blacklist (blocks domain + all subdomains) |

## Pi-hole regex import

1. Open Pi-hole Admin → **Domains** (or **Regex filters**)
2. Add each line as a **Regular expression** / Deny  
   Or copy lines into `/etc/pihole/regex.list` and run `pihole restartdns`
3. Patterns look like `(\.|^)example\.com$` — that blocks `example.com` and `*.example.com`

Brand-family patterns at the top of the regex file also catch rotating mirrors (e.g. `paldoplus*`, `phlago*`, `jilibet*`, `bk8ph*`).

Please spread this — fork/improve welcome. Credit the original poster and this repo.
