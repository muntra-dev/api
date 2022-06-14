## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /muntra-patient-reviews | caregiver_id, order, page, per_page, sort_by |


## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| created_date |  | isodate |
| overall_rating |  | number |
| patient_name |  | string |
| review_comment |  | string |


## Samples
### GET Request
#### URL
```
/api/muntra-patient-reviews?sort_by=has_review_comment%2Ccreated_date&order=desc&page=2&per_page=10&caregiver_id=4
```
#### Response Payload
```
{
  "data": [
    {
      "type": "muntra_patient_review",
      "id": "75",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "FH",
        "review_comment": "",
        "created_date": "2021-10-12T10:41:07+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "48",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "Testso Testison",
        "review_comment": "",
        "created_date": "2021-09-30T12:10:29+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "46",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "TE",
        "review_comment": "",
        "created_date": "2020-06-26T17:40:04+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "43",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "NR",
        "review_comment": "",
        "created_date": "2020-06-26T16:51:37+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "42",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "HV",
        "review_comment": "",
        "created_date": "2020-06-26T16:48:47+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "41",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "HV",
        "review_comment": "",
        "created_date": "2020-06-26T16:45:19+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "40",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "HV",
        "review_comment": "",
        "created_date": "2020-06-26T16:43:52+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "39",
      "attributes": {
        "overall_rating": 3,
        "patient_name": "NR",
        "review_comment": "",
        "created_date": "2020-06-26T16:41:20+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "36",
      "attributes": {
        "overall_rating": 3,
        "patient_name": "NR",
        "review_comment": "",
        "created_date": "2020-06-25T00:12:50+00:00"
      }
    },
    {
      "type": "muntra_patient_review",
      "id": "35",
      "attributes": {
        "overall_rating": 5,
        "patient_name": "NR",
        "review_comment": "",
        "created_date": "2020-06-25T00:09:02+00:00"
      }
    }
  ],
  "meta": {
    "pagination": {
      "total": 21,
      "count": 10,
      "per_page": 10,
      "current_page": 2,
      "total_pages": 3
    }
  },
  "links": {
    "self": "http://journalapitest.prodentor.se/api/muntra-patient-reviews?page=2",
    "first": "http://journalapitest.prodentor.se/api/muntra-patient-reviews?page=1",
    "prev": "http://journalapitest.prodentor.se/api/muntra-patient-reviews?page=1",
    "next": "http://journalapitest.prodentor.se/api/muntra-patient-reviews?page=3",
    "last": "http://journalapitest.prodentor.se/api/muntra-patient-reviews?page=3"
  }
}
```
