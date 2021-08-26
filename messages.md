# Events

[ [Back to README](README.md) ]

Description of events supported by MMS:

## ProductEvent

Implemented in [go-mms](https://github.com/metno/go-mms/blob/79a925c16b28d944c2a1ade24a3532de034e6b89/pkg/mms/events.go#L37)

| Attribute  | Description  |
| --- | --- |
| Product  | shortname, i.e., file(object) name without timestamp  |
| JobName | For larger production units, a more detailed identification of where the product comes from (e.g. ecFlow job) |
| ProductLocation | Storage system + protocol + filename or object name |
| ProductionHub | Some identification of the production unit of this product (e.g. ecflow-nwp@prod-serverb) |
| Counter | `Counter` out of `TotalCount` for products that are part of a collection of products |
| TotalCount | `TotalCount` of products in a collection of products |
| RefTime | For forecasting models. The forecast reference time in NWP is the "data time", the time of the analysis from which the forecast was made. |
| CreatedAt |  timestamp of the produced file (object) |
| NextEventAt | timestamp of the next event |

## Other Events

Currenlty only ProductEvent is implemented. Though the idea of MMS is that other event types can be added when needed. An example would be an ecFlow trigger event or a code update event from GitHub/Gitlab with the purpose of triggering a build.