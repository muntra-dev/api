Extends [remittance model](../remittances/).

## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /received-remittances | deleted, include, order, page, patient_id, per_page, query, receiver_clinic_ids, sort_by, status, user_group_ids, user_id |

## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| booked |  | boolean |
| priority |  | number |

Additional properties are found in [the remittance model](../remittances/).

## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| receiver_journal_entry | belongsTo | journal-entry |
| user_group | belongsTo | user-group |

Additional relations are found in [the remittance model](../remittances/).


## Statuses (in order of parsing)
| Code | Color | Condition |
| ---- | ----- | --------- |
| `declined` | Gray | `declined_at` is truthy |
| `completed` | Green | <ul><li>`closed_at` is truthy</li><li>`receiver_user_signed_at` and `remittance_response` is truthy</li></ul> |
| `booked` | Purple | `booked` is truthy |
| `approved` | White | `approved_at` is truthy |
| `received-confirmed` | Blue | `confirmed_receipt_at` is truthy |
| `received-unconfirmed` | Red | `signed_at` is truthy |
| `draft` | Yellow |  |

## Samples
### GET Request
#### URL
```
/api/received-remittances?deleted=false&include=patient%2Creceiver_clinic%2Creceiver_user%2Cremittance_responses.signer%2Csender_clinic%2Csender_user%2Cuser_group&order=asc&page=1&patient_id=426&per_page=10&query=&receiver_clinic_ids=2&sort_by=priority&status=approved%2Cbooked%2Cdraft%2Creceived-confirmed%2Creceived-unconfirmed&user_group_ids=1&user_ids=
```
#### Response Payload
```
{
  "data": [
    {
      "type": "received_remittance",
      "id": "520",
      "attributes": {
        "patient_address_1": "Frans väg 16",
        "patient_address_2": "wewew",
        "patient_city": "Bromma",
        "patient_date_of_birth": "1981-08-14T00:00:00+02:00",
        "patient_e_mail_address": "gmail@gmail.com",
        "patient_first_name": "Niels",
        "patient_gender": "male",
        "patient_last_name": "Rask-Andersen",
        "patient_municipality": "qwerdsdwewe",
        "patient_phone_number_cell": "+46700000000",
        "patient_phone_number_home": "+46700000000",
        "patient_phone_number_work": "+46700000000",
        "patient_postal_code": "16733",
        "patient_social_security_number": "198108111496",
        "sender_clinic_address_1": "Gatuadress #1",
        "sender_clinic_address_2": "Gatuadress #1",
        "sender_clinic_city": "Ort #1",
        "sender_clinic_email_address": "gmail@gmail.com",
        "sender_clinic_name": "Företagsnamn #1",
        "sender_clinic_phone_number": null,
        "sender_clinic_postal_code": "12345",
        "receiver_clinic_address_1": "Mäster Samuelsgatan 36",
        "receiver_clinic_address_2": "C/O Epicenter",
        "receiver_clinic_city": "Stockholm",
        "receiver_clinic_email_address": "gmail@gmail.com",
        "receiver_clinic_name": "Muntra, test",
        "receiver_clinic_phone_number": "+46840906890",
        "receiver_clinic_postal_code": "11157",
        "receiver_user_email_address": null,
        "receiver_user_first_name": null,
        "receiver_user_last_name": null,
        "receiver_user_phone_number": null,
        "receiver_user_social_security_number": null,
        "receiver_user_signed_at": null,
        "remittance_background": null,
        "remittance_comment": null,
        "remittance_question": null,
        "desired_treatment": null,
        "remittance_response": null,
        "urgent": false,
        "consultation": false,
        "booked": false,
        "priority": null,
        "due_date": null,
        "signed_at": null,
        "sender_user_email_address": null,
        "sender_user_first_name": null,
        "sender_user_last_name": null,
        "sender_user_phone_number": null,
        "sender_user_social_security_number": null,
        "receiver_first_view_at": null,
        "confirmed_receipt_at": "2021-06-07T15:00:51+02:00",
        "declined_at": null,
        "closed_at": null,
        "printed_at": null,
        "approved_at": "2022-08-16T11:34:42+02:00",
        "created_at": "2021-06-07T15:00:51+02:00",
        "updated_at": "2022-08-16T11:34:59+02:00"
      },
      "relationships": {
        "sender_clinic": {
          "data": {
            "type": "clinic",
            "id": "1"
          }
        },
        "patient": {
          "data": {
            "type": "patient",
            "id": "337"
          }
        },
        "sender_user": {
          "data": null
        },
        "receiver_clinic": {
          "data": {
            "type": "clinic",
            "id": "2"
          }
        },
        "receiver_user": {
          "data": null
        },
        "user_group": {
          "data": null
        },
        "remittance_responses": {
          "data": []
        }
      }
    }
  ],
  "included": [
    {
      "type": "clinic",
      "id": "1",
      "attributes": {
        "clinic_address_1": "Gatuadress #1",
        "clinic_address_2": "",
        "clinic_city": "Ort #1",
        "clinic_email_address": "gmail@gmail.com",
        "clinic_name": "Företagsnamn #1 - nr1",
        "clinic_phone_number": "",
        "clinic_postal_code": "12345",
        "organization_name": "Företagsnamn #1",
        "allow_remittance_without_individual_recipient": true,
        "accepts_digital_remittance": true
      }
    },
    {
      "type": "patient",
      "id": "337",
      "attributes": {
        "social_security_number": "198108111496",
        "first_name": "Niels",
        "last_name": "Rask-Andersen",
        "maiden_name": null,
        "initials": null,
        "gender": "male",
        "address_1": "Frans väg 16",
        "address_2": "wewew",
        "city": "Bromma",
        "postal_code": "16733",
        "municipality": "qwerdsdwewe",
        "date_of_birth": "1981-08-14T00:00:00+02:00",
        "passport_number": null,
        "phone_number_cell": "+46700000000",
        "phone_number_home": "+4623",
        "phone_number_work": "+46232121",
        "fax_number": null,
        "e_mail_address": "gmail@gmail.com",
        "deleted": true,
        "created_at": "2020-03-19T17:05:58+01:00",
        "updated_at": "2021-08-12T08:48:37+02:00",
        "patient_number": "248",
        "invoice_reference": "123",
        "status": "active",
        "wants_anestesia": false,
        "start_date_free_card": "2021-05-04T00:00:00+02:00",
        "end_date_free_card": "2021-05-20T00:00:00+02:00",
        "free_card_number": null,
        "county_council_certificate_number": null,
        "county_council_certificate_end_date": "2021-05-06T00:00:00+02:00",
        "euro_certificate_number": null,
        "protected_identity": false,
        "warning": false,
        "warning_text": null,
        "xray_id": null,
        "notes": null,
        "external_dentist": null,
        "external_hygienist": null,
        "auto_include_email_invitation": null,
        "auto_include_sms_invitation": null,
        "auto_include_sms_reminder": null,
        "auto_include_snail_mail_invitation": null,
        "prefers_not_to_be_contacted_by_clinic": false,
        "recurring": true,
        "referral_source": null,
        "teeth_count": null,
        "untreated_teeth_count": null,
        "signed_at": null
      }
    },
    {
      "type": "clinic",
      "id": "2",
      "attributes": {
        "clinic_address_1": "Katarinavägen 15 ",
        "clinic_address_2": "C/O Epicenter",
        "clinic_city": "Stockholm",
        "clinic_email_address": "gmail@gmail.com",
        "clinic_name": "Muntra, test",
        "clinic_phone_number": "+4632240541",
        "clinic_postal_code": "11645",
        "organization_name": "Muntra AB",
        "allow_remittance_without_individual_recipient": true,
        "accepts_digital_remittance": true
      }
    }
  ],
  "meta": {
    "pagination": {
      "total": 1,
      "count": 1,
      "per_page": 10,
      "current_page": 1,
      "total_pages": 1
    }
  },
  "links": {
    "self": "http://journalapitest.prodentor.se/api/received-remittances?page=1",
    "first": "http://journalapitest.prodentor.se/api/received-remittances?page=1",
    "last": "http://journalapitest.prodentor.se/api/received-remittances?page=1"
  }
}
```
