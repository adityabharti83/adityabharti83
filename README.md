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
