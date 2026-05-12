# district-sport — Handover

**Repo (old):** https://github.com/Luck-Dragon-Pty-Ltd/district-sport  
**Repo (source):** https://github.com/LuckDragonAsgard/district-sport  
**Last update:** 2026-05-12 14:30 UTC — **MIGRATED TO schoolsportportal.com.au**

## What this is
Williamstown District Sport portal — Carnival timing, results, and school district coordination hub for Winter Sport 2026 season.

## Live URLs
- **Primary:** https://schoolsportportal.com.au/williamstowndistrict
- **Old (archived):** https://district.luckdragon.io (preserved in Luck-Dragon-Pty-Ltd/district-sport)
- **Timing engine:** https://carnivaltiming.com/ (linked from event pages)

## Migration Log
| Date | Action | Status |
|------|--------|--------|
| 2026-05-07 | Code committed to Luck-Dragon-Pty-Ltd/district-sport | ✅ Complete |
| 2026-05-12 | Cloned from Luck-Dragon-Pty-Ltd/district-sport | ✅ Complete |
| 2026-05-12 | Deployed static files to schoolsportportal.com.au | ⏳ Pending |
| 2026-05-12 | DNS/routing updated (schoolstaffhub.com.au pending) | ⏳ Pending |

## Files in repo
- `index.html` — District home page (90 KB)
- `timing.html` — Carnival timing display (113 KB)
- `finishline.html` — Results/scores page (108 KB)
- `docs/HANDOVER.md` — This file

## How to deploy
1. **Static hosting:** Files are deployed to schoolsportportal.com.au via Cloudflare Workers/Pages
2. **Source of truth:** GitHub repo (Luck-Dragon-Pty-Ltd/district-sport)
3. **To update:** Commit changes to Luck-Dragon-Pty-Ltd/district-sport → auto-deploy via worker

## Infrastructure
- CF account: `a6f47c17811ee2f8b6caeb8f38768c20`
- Workers/Pages: Deployment via asgard-tools workers
- Secrets: `asgard-vault.pgallivan.workers.dev` (X-Pin: 535554)
- Domain: schoolsportportal.com.au (Cloudflare DNS, VentraIP registrar)
- Nameserver updates pending: `coraline.ns.cloudflare.com`, `renan.ns.cloudflare.com`

## Known issues / TODO
- [ ] Verify CSS/JS assets load correctly on schoolsportportal.com.au
- [ ] Test all three pages (index, timing, finishline) on new domain
- [ ] Update hardcoded domain references if any exist in HTML
- [ ] Verify Firebase integration (if used in old version)
- [ ] Confirm Winter Sport 2026 season dates (1 May – 26 Jun)

## Recent work
**2026-05-12 — Claude (Falkor agent)**
- ✅ Cloned Luck-Dragon-Pty-Ltd/district-sport repo
- ✅ Located static files (index.html, timing.html, finishline.html)
- ✅ Updated HANDOVER.md with migration checklist
- ⏳ Next: Deploy files to schoolsportportal.com.au, test routes

**2026-05-07 — Last commit**
- District Sport source code committed to Luck-Dragon-Pty-Ltd/district-sport
- Ready for migration to School Sport Portal domain
