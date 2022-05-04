# Events

[ [Back to README](README.md) ]

Description of events supported by MMS:

## ProductEvent

Implemented in [go-mms](https://github.com/metno/go-mms/blob/79a925c16b28d944c2a1ade24a3532de034e6b89/pkg/mms/events.go#L37)

| Attribute  | Description  |
| --- | --- |
| Product  | File (object) name without timestamp. E.g. `meps_det_2_5km.ncml` or `met_forecast_1_0km_nordic.zarr`  |
| JobName | For larger production units, a more detailed identification of where the product comes from (e.g. ecFlow job) |
| MMD | MMD metadata string |
| ProductLocation | Full path to the file or object. E.g. `/lustre/storeB/project/metproduction/products/meps/meps_det_2_5km_20210828T09Z.ncml` or `https://s3.rgw-test.met.no/yr-maps-test/meps/2021-08-28T10:00:00Z` |
| ProductionHub | Some identification of the production unit of this product (e.g. ecflow-nwp@prod-serverb) |
| Counter | `Counter` out of `TotalCount` for products that are part of a collection of products |
| TotalCount | `TotalCount` of products in a collection of products |
| RefTime | For forecasting models. The forecast reference time in NWP is the "data time", the time of the analysis from which the forecast was made. |
| CreatedAt |  Timestamp of event creation. Assigned by mmsd. |
| NextEventAt | The time when next event is expected to arrive (for purposes of monitoring and alerting) |

## Other Events

Currenlty only ProductEvent is implemented. Though the idea of MMS is that other event types can be added when needed. An example would be an ecFlow trigger event or a code update event from GitHub/Gitlab with the purpose of triggering a build.
