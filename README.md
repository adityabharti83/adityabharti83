<div align="center">

```sql
SELECT name, role, location
FROM   engineers
WHERE  obsession = 'clean_data'
  AND  bullshit  = FALSE;
```

```
 name          | role                | location
----------------+---------------------+------------------
 Aditya Bharti  | Data Analyst        | Pune, India
(1 row)
```

![Profile Views](https://komarev.com/ghpvc/?username=adityabharti83&label=QUERY%20COUNT&color=blue&style=flat-square)

</div>

<br>

## `-- about_me.sql`

```sql
/*
  I don't trust a dashboard until I've seen the raw table it came from.
  Most of my work is the unglamorous 80%: fixing types, killing
  duplicates, deciding what "null" actually means in THIS dataset —
  before a single chart gets drawn.

  Background: B.E. Computer Software Engineering, CGPA 8.68.
  Currently: shipping ETL pipelines and BI dashboards, one intern
  rotation at a time, one open-source pipeline in my own repo.
*/
```

<br>

## `-- schema: skills`

```
┌─────────────────────┬──────────────────────────────────────────────┐
│ column               │ values                                       │
├─────────────────────┼──────────────────────────────────────────────┤
│ languages            │ Python, SQL                                   │
│ analysis             │ Pandas, NumPy, EDA, Statistics, Data Cleaning │
│ bi_tools              │ Power BI, DAX, Tableau, Looker, Excel         │
│ data_engineering      │ ETL, Data Pipelines, Data Modeling, Validation│
│ cloud                 │ BigQuery, GCP, Snowflake                      │
│ dev_workflow          │ Git, GitHub, CI/CD, REST APIs                 │
│ ai_assisted_analytics │ Generative AI tooling in the analysis loop    │
└─────────────────────┴──────────────────────────────────────────────┘
```

<br>

## `-- version_history.changelog`

```diff
v3.1  (current)  Shipping pipelines that go past the notebook — pushing toward
                 GCP + Cloud Functions, not just local scripts.
v3.0  Nov 2025   Data Engineer Apprentice @ thinkbridge — learned that the
                 pipeline breaking at 2am matters more than the pipeline
                 looking clever at 2pm.
v2.0  Jan 2025   Data Analytics Intern @ Clustor Computing — first time
                 a dashboard I built changed an actual decision, not
                 just a grade.
v1.0  Jul 2025   B.E. Computer Software Engineering, CGPA 8.68 — graduated
                 realizing the hard part was never the syntax.
+ known_issue: still double-checking every JOIN before I trust the row count.
+ status: no fix planned, it's a feature.
```

<br>

## `-- query_log.txt` (professional experience)

```log
[Nov 2025 – Dec 2025] thinkbridge · Data Engineer Apprentice
  > built ETL pipelines (Python + SQL) for ingestion, transformation,
    validation of analytics-ready datasets
  > optimized slow queries; wired Git + CI/CD into the workflow
  > integrated external APIs & cloud sources, added cleaning/validation
    at the boundary

[Jan 2025 – Oct 2025] Clustor Computing · Data Analytics Intern
  > mined structured data for trends, anomalies, quality issues
  > cleaned/validated/EDA'd datasets before they ever touched a report
  > shipped interactive Power BI dashboards + KPI reporting
```

<br>

## `-- EXPLAIN ANALYZE: pune_transit_monitor`

**The project I'd actually want a hiring manager to open.**
Real PMPML GTFS schedule data — not a Kaggle CSV — turned into a validated, query-able dataset and a Power BI layer on top.

```
Seq Scan on raw_gtfs_feed              (routes=627, stops=6696)
  -> Filter: valid_schema = true
  -> HashJoin on trip_id                (trips=15,138)
       -> Nested Validation              (stop_times=627,412+)
            -> Output: cleaned, tested, analysis-ready tables
Planning: Python + SQLite  |  Execution: BigQuery  |  Display: Power BI
Status: pipeline live · Power BI dashboard in progress · GCP wiring in progress
```

`Stack:` Python · SQL · SQLite · Pandas · Power BI · Pytest · GTFS
`Repo:` [github.com/adityabharti83/pune-transit-monitor](https://github.com/adityabharti83/pune-transit-monitor)

<br>

## `-- EXPLAIN ANALYZE: airbnb_market_analytics`

```
Seq Scan on listings                    (rows=1,000,000+)
  -> Feature Engineering                (price, availability, host, geo)
  -> Aggregate + KPI Rollup
       -> Output: Power BI dashboard, trend + pricing insights
Status: complete
```

`Repo:` github.com/adityabharti83/airbnb-market-analytics

<br>

## `-- SELECT * FROM github_activity;`

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=adityabharti83&show_icons=true&theme=tokyonight&hide_border=true" height="165"/>
<img src="https://streak-stats.demolab.com?user=adityabharti83&theme=tokyonight&hide_border=true" height="165"/>

<img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg" width="100%" alt="contribution snake"/>

</div>

<br>

## `-- known_issues.md`

```md
- [ ] Occasionally refactors a working script at 1am for "readability"
- [ ] Cannot leave a `SELECT *` in production code, physically incapable
- [x] Will absolutely argue that a bar chart was the wrong choice
- [ ] Has strong opinions about tabs vs commas in CSVs (it's commas)
```

<br>

## `-- connection_string`

```ini
[contact]
email    = adityabharti6088@gmail.com
github   = github.com/adityabharti83
linkedin = linkedin.com/in/aditya-bharti
status   = OPEN — looking for Data Analyst roles
```

<div align="center">

<sub>certified: AccioJobs Data Analytics · 5★ SQL on HackerRank</sub>

</div>
