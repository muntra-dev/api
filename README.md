# API Docs for Muntra Patient Management System (MPMS)

All endpoints currently use the namespace `/api`, as in eg.:
```
GET /api/patient-invoices
```

MPMS is built on top of the JSON API specification:
https://jsonapi.org/

## Property Types
Data models' properties can be of the following types.
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


## Other Stuff
Some endpoints require authentication or a token, others are completely public.

Examples of public endpoints are `muntra-clinics`, `muntra-roles`. Non-public endpoints are eg. `patients`, `bookings` or `journal-entries`.

The `Authorization` request header is not needed for public endpoints.
