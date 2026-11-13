# Cricket Club Manager — Native Android App

A full native Android cricket club management simulation game. Manage **Lahore Qalandars** through a T20 season: pick your XI, play ball-by-ball matches, set tactics, top the league, and upgrade your club HQ.

**100% native Java — no WebView, no website inside. Works completely offline, zero permissions.**

## Download

- **APK (latest release):** see the [Releases](../../releases) section — `cricket-club-manager.apk`
- Package: `io.github.farrakhimtiaz74.cricketmanager`
- Version: 1.0 (versionCode 1) · minSdk 21 (Android 5.0+) · targetSdk 34
- Size: ~50 KB

## Features

- **6 tabs:** Hub, Team, League, World, Profile, HQ — dark slate (#0f172a / #1e293b) + gold (#f59e0b) UI
- **Hub:** Season/day calendar, Club Cash (CF), next-match card, Advance Day, Recovery, Team Talk, club news
- **Team:** 18-man Lahore Qalandars squad with Batting / Bowling / Stamina / Set % / Rating, role filters (Bat / Bowl / AR / WK), tap-to-pick Starting XI with keeper & bowling warnings
- **Match engine:** Coin-call toss, bat/bowl first, Bowl Ball / Sim Over / Sim Innings / Sim Match, live commentary, scorecard, run rate, projected score, DLS par while chasing, Tactics (Defend / Build / Attack / Slog + running style) that genuinely change outcomes. Mid-match progress is saved — close the app and resume
- **League:** Group A & Group B tables (P / W / L / NRR / PTS) + all 24 fixtures
- **World:** Player & nation rankings for T20I / ODI / Test (Batting, Bowling, All-rounder)
- **Profile:** Career record, win %, streaks, titles, match history
- **HQ:** 5 upgradeable facilities (Stadium, Medical Centre, Training Complex, Youth Academy, Commercial Centre) paid in Club Cash, with real in-game effects

## Build

Pure framework Java, built with the manual Android pipeline (no Gradle):

```bash
cd native
./build.sh
```

Requires an Android SDK (build-tools 36.1.0, platform android-34) and a JDK — see `native/build.sh` for the exact aapt2 + javac + d8 + zipalign + apksigner steps. Source is also provided as `cricket-club-manager-source.zip`.

## Notes

- Season champion is the overall points leader across both groups
- DLS par uses a simplified resource formula
- World rankings are a static snapshot
