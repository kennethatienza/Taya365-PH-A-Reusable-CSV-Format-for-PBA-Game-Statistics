# Taya365 PH: A Reusable CSV Format for PBA Game Statistics
> A **PBA score file** works best when each row shows **one team's stats from one match**. Fans can track scores over time, but **mixed team names can make a clean set look wrong**. A **CSV file** stores plain text in rows and makes the stats easy to sort.

<img width="1536" height="1024" alt="The Court That Unrolls" src="https://github.com/user-attachments/assets/6d4b052c-9321-459a-b993-8e8874775ee6" />
<br>
<br>

The **[Taya365 PH](https://taya365ph.com/)** site covers sports, yet **its pages are not league box scores**. This guide lays out **one plain file for team stats**, fit for sheets and GitHub. Use **real PBA game records** for live data, not scores made up to fill gaps.

## Give Each Team One Row for Every Game

Give each team **one row per game**, so a full match has two linked rows. Both rows share **one game ID**, yet each has its own team name and game stats. This layout lets fans check a match fast, without rows for each player on court.

A **game ID** must stay the same, even when a site moves its match page. The ID ties the two sides together without the need to match names or dates. **Do not use one ID for two games**, even if the same teams meet once more.

Each row shows **one side's game totals**, while the other row holds its rival's stats. For a final match, the **two team scores** must match the score shown by the league. When one row is lost, **mark the pair as incomplete** and leave unknown stats blank.

## Store the Key Fields Behind Each Final Score

Start with **season, conference, game ID, date, team, rival, and points** in each row. Add **rebounds, assists, and turnovers** only when trusted box scores show those team totals. Keep **game status and overtime flags**, since an unfinished game cannot count as a final result.

A **source link** shows where the score came from, so readers can check it again. Write **dates as year-month-day** to keep day and month order the same in each sheet. Store **stats as whole numbers**, but use an empty cell when no good source shows them.

## Copy This Sample CSV Into Your GitHub Repo

This **sample CSV has made-up teams and scores**, so none of its rows show real games. Both rows have **the same sample ID and date**, but each side has its own stats. Paste the text into **pba_team_games.csv**, then swap the sample rows for checked league data.

```csv
season,conference,game_id,date_ph,team,opponent,points,rebounds,assists,turnovers,overtime,status,source_url
SAMPLE,EXAMPLE,SAMPLE001,2000-01-01,Example A,Example B,100,39,23,10,no,final,
SAMPLE,EXAMPLE,SAMPLE001,2000-01-01,Example B,Example A,92,35,17,12,no,final,
```

**Commas split the fields**, so put quote marks around a team name that has a comma. The **blank source cells** mean these fake rows have no real match page to cite. **Remove both sample rows before you post real scores**, or they may skew the file.

Save the file as **UTF-8 CSV**, so team names stay clear when sent to other devices. Some sheet apps change dates on save, so **check the dates and IDs after export**. Keep **the same header names** each time, since tools may look for those exact words.

## Check Box Scores Against Trusted PBA Game Records

Use **official PBA match pages** for dates and teams, then check whether each has full statistics. For **points and team totals**, use a league box score or a trusted game report. **Do not list a live score as final** until a good source backs the result.

A score can change after the game, so **keep each source link with its own row**. When the source omits a stat, **leave that cell blank rather than type in zero**. A **zero says none took place**, but a blank says the count is not yet known.

## Find Repeat Rows Before They Skew Team Averages

A match needs **two team rows**, and each should share the same ID and game date. Check for **the same ID with the same team twice**, which may point to repeat data. Use **one team name style** across the file, not a mix of nicknames and short forms.

Compare **both scores to the final league result** before you mark the game as checked. **Scores and team stats must be whole numbers at least zero**, not text or rough guesses. When two sources clash, **flag the row for review** and do not just choose one.

**Overtime points belong in final scores**, since the game does not end at the last normal buzzer. Set **overtime to yes only when the source confirms extra time beyond four normal quarters**. **Do not swap final scores for scores after four quarters**, or your sums may be wrong.

## Let GitHub Show the File and Each Change

GitHub can show **a saved CSV as a table**, so fans can scan rows on screen. Store **the actual .csv file in the repo**, not just a code block in its README. Use that **README to list field meanings**, source rules, and what a blank cell tells readers.

When a score gets fixed, **save a new commit** and say what row was changed. This helps fans see **which value changed and why**, rather than trust an unseen edit. Keep the **file history focused on verified game updates**, so future readers can retrace each change.

## Separate Past PBA Facts From Sports Betting Claims

A **box score shows past play**, while odds show a market view of what might come next. **One good game cannot prove the next result**, no matter how neat the sheet looks. The rows also **cannot prove what bets any site lists**, or that its price is fair.

Use **points, boards, and assists as past facts**, not as sure signs of what comes next. Fans may find trends over time, yet **a small set of games can mislead them**. **Label gaps and fixes in the data**, so each claim can be traced to its source.

The **[Taya365 PH basketball sportsbook guide](https://taya365ph.com/sportsbook/)** lists sports markets, **not a trusted feed of PBA game stats**. For each match, **use league data for facts** and keep market claims in their own place. **A CSV file helps only when its scores are real, its links work, and its rows agree.**
