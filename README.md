# API Docs for Muntra Patient Management System (MPMS)

All endpoints currently use the namespace `/api`, as in e.g.
```
GET /api/patient-invoices
```
MPMS is built on top of the JSON API specification:
https://jsonapi.org/
## Property Types
Data models' properties can be any of the following types.
| Type |  |  |
| ------------- | ------------- | ------------- |
| boolean |  |  |
| isodate |  |  |
| number |  |  |
| string |  |  |

## Request Headers
```
  Accept: application/x.journal.v1+json
  Content-Type: application/json
  Authorization: Bearer {access-token}
```

`Authorization` is not needed for public endpoints such as `muntra-clinics`.
