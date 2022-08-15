## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| POST | /remittance-responses | TBD |

## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| created_at |  | isodate |
| external | If `true`, the remittance-response is copied to the referral sender / receiver. | boolean |
| signed_at |  | isodate |
| text |  | string |
| updated_at |  | isodate |


## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| files | hasMany | file |
| remittance | belongsTo | remittance |
| signer | belongsTo | user |
| signer_clinic | belongsTo | clinic |

## Samples
### GET Request
#### URL
```
```
#### Response Payload
```
```
