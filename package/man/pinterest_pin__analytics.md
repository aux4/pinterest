#### Description

The `analytics` command retrieves analytics for a specific pin over a date range. Available metrics include IMPRESSION, PIN_CLICK, SAVE, and more.

#### Usage

```bash
aux4 pinterest pin analytics <pinId> --startDate <YYYY-MM-DD> --endDate <YYYY-MM-DD> [--metricTypes <types>]
```

--startDate     Start date in YYYY-MM-DD format
--endDate       End date in YYYY-MM-DD format
--metricTypes   Comma-separated metric types (default: IMPRESSION,PIN_CLICK,SAVE)

#### Example

```bash
aux4 pinterest pin analytics 123456789 --startDate 2026-01-01 --endDate 2026-01-31
```

```text
{"all":{"daily_metrics":[{"date":"2026-01-01","data_status":"READY","metrics":{"IMPRESSION":150,"PIN_CLICK":12,"SAVE":5}}]}}
```
