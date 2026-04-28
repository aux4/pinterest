#### Description

The `analytics` command retrieves account-level analytics for the authenticated user over a date range.

#### Usage

```bash
aux4 pinterest user analytics --startDate <YYYY-MM-DD> --endDate <YYYY-MM-DD> [--metricTypes <types>] [--tokenFile <path>]
```

--startDate     Start date in YYYY-MM-DD format
--endDate       End date in YYYY-MM-DD format
--metricTypes   Comma-separated metric types (default: IMPRESSION,PIN_CLICK,SAVE)
--tokenFile     Custom token file path

#### Example

```bash
aux4 pinterest user analytics --startDate 2026-01-01 --endDate 2026-01-31
```

```text
{"all":{"daily_metrics":[{"date":"2026-01-01","data_status":"READY","metrics":{"IMPRESSION":500,"PIN_CLICK":45,"SAVE":20}}]}}
```
