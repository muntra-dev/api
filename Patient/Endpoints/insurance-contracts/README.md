## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| contract_id |  | string |
| end_date |  | isodate |
| organization_id |  | string |
| price_excluding_vat |  | number |
| start_date |  | isodate |


## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| journal_diagnoses | hasMany | journal-diagnosis |
| tanden_checks | hasMany | [tanden-check](../tanden-checks/) |
