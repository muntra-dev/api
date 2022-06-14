## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /tanden-checks | include, organization_id, patient_id |

## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| eligble |  | boolean |
| eligible_from_date |  | isodate |
| error_code |  | string |
| error_text |  | string |
| faultcode |  | string |
| faultstring |  | string |
| hcd_amount |  | number |
| hcd_start_date |  | isodate |
| hcd_end_date |  | isodate |
| last_treatment_date |  | isodate |
| stb_amount_available |  | number |


## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| currency | belongsTo | currency |
| insurance_contract | belongsTo | insurance-contract |
| new_atb | belongsTo | [new-atb](../atbs/) |
| old_atb | belongsTo | [old-atb](../atbs/) |
| patient | belongsTo | [patient](../patients/) |
| tanden_check_commentaries | hasMany | [tanden-check-commentary](../commentaries/) |


## Samples
### GET Request
#### URL
```
/api/tanden-checks?include=currency%2Cinsurance_contract.journal_diagnoses%2Cnew_atb%2Cold_atb%2Ctanden_check_commentaries&organization_id=2&patient_id=119
```
#### Response Payload
```
{
  "data": {
    "type": "tanden_check",
    "id": "27025",
    "attributes": {
      "eligble": true,
      "eligible_from_date": "2005-01-01T00:00:00+01:00",
      "stb_amount_available": 600,
      "hcd_amount": 760,
      "hcd_start_date": "2022-06-01T00:00:00+02:00",
      "hcd_end_date": "2023-05-31T00:00:00+02:00",
      "last_treatment_date": "2022-06-01T00:00:00+02:00",
      "faultcode": null,
      "faultstring": null,
      "error_code": null,
      "error_text": null
    },
    "relationships": {
      "old_atb": {
        "data": {
          "type": "old_atb",
          "id": "74"
        }
      },
      "new_atb": {
        "data": {
          "type": "new_atb",
          "id": "82"
        }
      },
      "insurance_contract": {
        "data": null
      },
      "tanden_check_commentaries": {
        "data": [
          {
            "type": "tanden_check_commentary",
            "id": "15359"
          }
        ]
      },
      "currency": {
        "data": {
          "type": "currency",
          "id": "1"
        }
      }
    }
  },
  "included": [
    {
      "type": "old_atb",
      "id": "74",
      "attributes": {
        "amount": 300,
        "start_date": "2020-07-01T00:00:00+02:00",
        "end_date": "2022-06-30T00:00:00+02:00",
        "used": true
      }
    },
    {
      "type": "new_atb",
      "id": "82",
      "attributes": {
        "amount": 300,
        "start_date": "2021-07-01T00:00:00+02:00",
        "end_date": "2023-06-30T00:00:00+02:00",
        "used": true
      }
    },
    {
      "type": "tanden_check_commentary",
      "id": "15359",
      "attributes": {
        "fk_id": 1,
        "code": 277,
        "commentary": "Patienten är registrerad som försäkrad hos Försäkringskassan från och med 2005-01-01."
      }
    },
    {
      "type": "currency",
      "id": "1",
      "attributes": {
        "code": "SEK",
        "name": "Svenska kroner",
        "suffix": "kr"
      }
    }
  ]
}
```
