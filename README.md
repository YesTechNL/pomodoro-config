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
  "tyt": "2027-06-19 10:15:00",
  "ayt": "2027-06-20 10:15:00",
  "ydt": "2027-06-20 10:15:00",
  "announced": 0
}
```

`announced`: `1` if these are the official ÖSYM dates, `0` if they're
still provisional - `0` shows a "not yet officially announced" banner
at the top of the exam page instead of presenting the dates as final.

Each date must be exactly `yyyy-MM-dd HH:mm:ss` and a real calendar
date/time - anything else (wrong format, out-of-range month/day, missing
key) makes the app show "!" for that exam instead of a wrong date.
