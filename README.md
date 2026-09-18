# pomodoro-config

Public config for the Pomodoro app. Currently just `exam_dates.json`,
fetched by the app at startup so exam dates can be updated without a
new app release.

Edit `exam_dates.json` directly on GitHub (or clone, edit, push) whenever
dates need to change - the app picks up the new values on next launch,
typically within a few minutes due to GitHub's CDN cache.

Format:
```json
{
  "tyt": "2026-06-21 10:14:59",
  "ayt": "2026-06-22 10:14:59",
  "ydt": "2026-06-22 15:44:59",
  "msu": "2026-02-23 10:14:59",
  "lgs": "2026-06-15 09:29:59"
}
```
