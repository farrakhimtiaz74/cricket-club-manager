# Cricket Club Manager — Native Android App

A full native Android cricket club management simulation game. Manage your club through T20 league seasons, a 50-over cup and playoffs: pick your XI, play ball-by-ball matches, set tactics, run transfers and auctions, hire staff, sign sponsors — and try not to get sacked by the board.

**100% native Java — no WebView, no website inside. Works completely offline, zero permissions.**

## Download

- **APK (latest release):** see the [Releases](../../releases) section — `cricket-club-manager.apk`
- Package: `io.github.farrakhimtiaz74.cricketmanager`
- Version: 12.0 (versionCode 12) · minSdk 21 (Android 5.0+) · targetSdk 34
- Size: ~221 KB

## What's in v12 — the 100-update mega-batch

Versions 3.0–12.0 added all 100 approved updates in ten batches:

- **Match engine:** Super Overs, rain + simplified DLS, pitch types (Flat/Green/Dry/Turning), dew, live win predictor, Manhattan chart, partnerships & fall of wickets, Player of the Match, Highlights mode, match speeds
- **Tactics:** powerplay plans, 20-over bowling rotation planner, next-batter picker, assistant-coach suggestions, batter-vs-bowler match-ups, 6 field presets with a field map, segment pep talks, danger-man plans, per-batter bowling plans
- **Squad & players:** season + career stats, form graphs, ages & potential with development, injuries & physio, morale, captaincy, auto-pick Best XI, player comparison, milestone alerts, specialist tags
- **Transfers & contracts:** off-season retain/release, contract renewals, turn-based auction vs AI clubs, mid-season window, weekly wages, loans in/out, free agents, scouting, poaching offers, rumours
- **League & season:** real PSL-style playoffs (Qualifier, Eliminators, Final) + trophy ceremony, tournament leaderboards, live "As It Stands" table, Road to Playoffs, head-to-head records, season awards, all-time Records Book, Hall of Fame, multi-season history
- **Teams & world:** all 8 clubs playable, custom team creator, full 18-man AI squads, a real 50-over Cup, home advantage + gate income, derbies, named grounds, moving World T20I rankings, international call-ups, player renaming
- **HQ, staff & money:** 5 hireable staff roles, facilities to Level 10, ticket pricing, sponsor deals with objectives, merchandise income, pre-season training camp, board confidence — with the sack if it crashes — manager XP & levels, fan mood, HQ Finances view
- **News & immersion:** post-match press conferences, newspaper headlines, fan social feed, Coach's Corner tips, pre-match analysis, season review, shareable match report cards, trophy cabinet, season calendar, rival manager quotes
- **Modes & challenges:** 3 difficulty levels, daily challenge, 4 scenario matches, weekly quests, 15 achievements, prediction game, 3 career save slots, quick season, season result code, hardcore mode
- **App & QoL:** career backup export/import, sync-code transfer, What's New screen, Roman Urdu commentary, sound effects, big text + reduce animations, full Settings screen, global search, CSV stats export

## Core game

- **6 tabs:** Hub, Team, League, World, Profile, HQ — dark slate (#0f172a / #1e293b) + gold (#f59e0b) UI
- Ball-by-ball engine with toss, live commentary (English or Roman Urdu), tactics that genuinely change outcomes, mid-match save/resume
- Every Club Cash (CF) movement is recorded in an in-game ledger; career saves migrate forward across versions

## Build

Pure framework Java, built with the manual Android pipeline (no Gradle):

```bash
cd native
./build.sh
```

Requires an Android SDK (build-tools 36.1.0, platform android-34) and a JDK — see `native/build.sh` for the exact aapt2 + javac + d8 + zipalign + apksigner steps. Source is also provided as `cricket-club-manager-source.zip`.

## Notes

- DLS uses a simplified resource formula; other teams' tournament stats are standout-based
- Season history and records accumulate from v7.0 onward
- Fully offline by design — career transfer between phones uses the in-app sync code, not a server
