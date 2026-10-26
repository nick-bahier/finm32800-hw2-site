# Dataframe: `hw2:fed_funds_futures` - 30-Day Fed Funds Futures (ZQ)

One row per contract per trading day, pulled from the Databento GLBX.MDP3 (CME Globex) dataset with the ohlcv-1d schema and the parent symbol ZQ.FUT, which returns every listed ZQ contract. Columns: date (tz-naive trading date), symbol, open, high, low, close, volume. A ZQ contract settles at 100 minus the calendar-day average of the effective federal funds rate over its delivery month, so 100 minus the close is the market's expected average rate for that month. The pull includes calendar-spread symbols such as ZQU6-ZQZ6; use fedwatch.filter_outright_contracts to keep only the outright monthly contracts (ZQU6). Far-dated months trade thinly and may have no bar on a given day; fedwatch.latest_prices_by_contract carries each contract's last available close forward.


## DataFrame Glimpse

```
Rows: 11755
Columns: 7
$ date   <datetime[ns]> 2026-10-19 00:00:00
$ symbol          <str> 'ZQN7'
$ open            <f64> 95.45
$ high            <f64> 95.45
$ low             <f64> 95.375
$ close           <f64> 95.38
$ volume          <u64> 1479


```

## Dataframe Manifest

| Dataframe Name                 | 30-Day Fed Funds Futures (ZQ)                                                          |
|--------------------------------|--------------------------------------------------------------------------------------|
| Dataframe ID                   | [fed_funds_futures](../dataframes/hw2/fed_funds_futures.md)                                       |
| Sources                        | CME Group                                          |
| Providers                      | Databento                                        |
| Provider Links                 | https://databento.com/                                   |
| Tags                           | Monetary Policy, Futures, Fedwatch, Interest Rates                                             |
| Access Types                   |                                       |
| How is data pulled?            | Databento Historical API via Python                                                   |
| Data available up to (min)     | 2026-10-19 00:00:00                                                             |
| Data available up to (max)     | 2026-10-19 00:00:00                                                             |
| Dataframe Path                 | /Users/nicolasbahier/Desktop/DPforQF/hw2-nick-bahier/_data/fed_funds_futures.parquet                                             |


**Linked Charts:**


- [hw2:fedwatch_latest_forecast](../../charts/hw2.fedwatch_latest_forecast.md)



## Pipeline Manifest

| Pipeline Name                   | HW 2: The Yield Curve and the Policy Path                       |
|---------------------------------|--------------------------------------------------------|
| Pipeline ID                     | [hw2](../../../index.md)              |
| Maintainer                      | Jeremiah Bejarano               |
| Contributors                    | Jeremiah Bejarano |
| Repository                     | https://github.com/hw-finm-32800/hw2                  |
| Pipeline Web Page               | <a href="file:///Users/nicolasbahier/Desktop/DPforQF/hw2-nick-bahier/docs/index.html">Pipeline Web Page      |
| Date of Last Code Update        | 2026-10-20 16:40:40           |
| OS Compatibility                | Windows, Linux, macOS |
| Linked Dataframes               |  [hw2:crsp_treasury_consolidated](../../dataframes/hw2/crsp_treasury_consolidated.md)<br>  [hw2:fed_yield_curve](../../dataframes/hw2/fed_yield_curve.md)<br>  [hw2:fed_funds_futures](../../dataframes/hw2/fed_funds_futures.md)<br>  |


**Build Commands:**
```
doit

```

