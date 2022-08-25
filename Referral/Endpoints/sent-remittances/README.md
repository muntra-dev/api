Extends [remittance model](../remittances/).

## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /sent-remittances | deleted, include, order, page, patient_id, per_page, query, sender_clinic_ids, sort_by, status, user_ids |

## Properties
Properties are found in [the remittance model](../remittances/).

## Relations
Relations are found in [the remittance model](../remittances/).


## Statuses (in order of evaluation)
| Code | Color | Condition |
| ---- | ----- | --------- |
| `declined` | Gray | `declined_at` is truthy |
| `completed` | Green | <ul><li>`closed_at` is truthy</li><li>`receiver_user_signed_at` and `remittance_response` are truthy</li></ul> |
| `sent-confirmed` | White | `confirmed_receipt_at` is truthy |
| `sent-unconfirmed` | Red | `signed_at` is truthy |
| `draft` | Yellow |  |

## Samples
### GET Request
#### URL
```
/api/sent-remittances?deleted=false&include=patient%2Creceiver_clinic%2Creceiver_user%2Cremittance_emails%2Csender_clinic%2Csender_user%2Csnail_mails&order=desc&page=1&patient_id=&per_page=10&query=&sender_clinic_ids=765&sort_by=id&status=sent-unconfirmed&user_ids=
```
#### Response Payload
```
{
  "data": [
    {
      "type": "remittance",
      "id": "539",
      "attributes": {
        "patient_address_1": "Frans väg 16",
        "patient_address_2": "wewew",
        "patient_city": "Bromma",
        "patient_date_of_birth": "1981-08-14T00:00:00+02:00",
        "patient_e_mail_address": "gmail@gmail.com",
        "patient_first_name": "Niclas",
        "patient_gender": "male",
        "patient_last_name": "Andersson",
        "patient_municipality": "qwerdsdwewe",
        "patient_phone_number_cell": "+46700000000",
        "patient_phone_number_home": "+46700000000",
        "patient_phone_number_work": "+46700000000",
        "patient_postal_code": "16733",
        "patient_social_security_number": "198108111496",
        "sender_clinic_address_1": "Mäster Samuelsgatan 36",
        "sender_clinic_address_2": "C/O Epicenter",
        "sender_clinic_city": "Stockholm",
        "sender_clinic_email_address": "gmail@gmail.com",
        "sender_clinic_name": "Muntra, test",
        "sender_clinic_phone_number": "+46700000000",
        "sender_clinic_postal_code": "11157",
        "receiver_clinic_address_1": "Mäster Samuelsgatan 36",
        "receiver_clinic_address_2": "C/O Epicenter",
        "receiver_clinic_city": "Stockholm",
        "receiver_clinic_email_address": "gmail@gmail.com",
        "receiver_clinic_name": "Muntra, test",
        "receiver_clinic_phone_number": "+46700000000",
        "receiver_clinic_postal_code": "11157",
        "receiver_user_email_address": "",
        "receiver_user_first_name": "",
        "receiver_user_last_name": "",
        "receiver_user_phone_number": null,
        "receiver_user_social_security_number": null,
        "receiver_user_signed_at": null,
        "remittance_background": "test",
        "remittance_comment": "",
        "remittance_question": "test",
        "desired_treatment": null,
        "remittance_response": null,
        "urgent": false,
        "consultation": false,
        "booked": false,
        "priority": null,
        "due_date": "2021-07-12T18:33:38+02:00",
        "signed_at": "2021-06-28T18:33:55+02:00",
        "sender_user_email_address": "gmail@gmail.com",
        "sender_user_first_name": "Niclas",
        "sender_user_last_name": "Rask",
        "sender_user_phone_number": "+46700000000",
        "sender_user_social_security_number": "198108100000",
        "receiver_first_view_at": null,
        "confirmed_receipt_at": "2021-07-05T09:50:16+02:00",
        "declined_at": "2021-07-06T13:44:19+02:00",
        "closed_at": null,
        "printed_at": null,
        "approved_at": null,
        "created_at": "2021-06-28T18:33:39+02:00",
        "updated_at": "2021-07-06T13:44:19+02:00"
      },
      "relationships": {
        "sender_clinic": {
          "data": {
            "type": "clinic",
            "id": "2"
          }
        },
        "patient": {
          "data": {
            "type": "patient",
            "id": "337"
          }
        },
        "sender_user": {
          "data": {
            "type": "user",
            "id": "4"
          }
        },
        "receiver_clinic": {
          "data": {
            "type": "clinic",
            "id": "2"
          }
        },
        "receiver_user": {
          "data": {
            "type": "user",
            "id": "4"
          }
        },
        "remittance_emails": {
          "data": [
            {
              "type": "remittance_email",
              "id": "2079"
            }
          ]
        },
        "snail_mails": {
          "data": [
            {
              "type": "snail_mail",
              "id": "1466"
            }
          ]
        }
      }
    }
  ],
  "included": [
    {
      "type": "role",
      "id": "3",
      "attributes": {
        "name": "Tandläkare",
        "slug": "dentist",
        "occupational_code": "TAN",
        "is_caregiver_role": true
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
        "clinic_phone_number": "+46700000000",
        "clinic_postal_code": "11645",
        "organization_name": "Muntra AB",
        "allow_remittance_without_individual_recipient": true,
        "accepts_digital_remittance": true
      }
    },
    {
      "type": "patient",
      "id": "337",
      "attributes": {
        "social_security_number": "198108111496",
        "first_name": "Niclas",
        "last_name": "Andersson",
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
        "phone_number_home": "+46700000000",
        "phone_number_work": "+46700000000",
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
      "type": "user",
      "id": "4",
      "attributes": {
        "first_name": "Niclas",
        "last_name": "Rask",
        "title": "Specialisttandläkare Ortodonti, Odont. Dr.",
        "e_mail_address": "gmail@gmail.com",
        "phone_number_cell": "+46700000000",
        "overall_rating": 4.38,
        "number_of_reviews": 21
      },
      "relationships": {
        "role": {
          "data": {
            "type": "role",
            "id": "3"
          }
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "remittance_email",
      "id": "2079",
      "attributes": {
        "to": "gmail@gmail.com",
        "to_name": null,
        "subject": "Muntra, test har fått en remiss från Muntra, test",
        "body": null,
        "sent_at": "2021-06-28T18:38:00+02:00",
        "scheduled": true,
        "message_status": "sent",
        "error_code": null,
        "deleted": false,
        "created_at": "2021-06-28T18:33:40+02:00"
      }
    },
    {
      "type": "snail_mail",
      "id": "1466",
      "attributes": {
        "first_name": "",
        "last_name": "Muntra, test",
        "address_1": "Mäster Samuelsgatan 36",
        "address_2": "C/O Epicenter",
        "city": "Stockholm",
        "postal_code": "11157",
        "output_date": "2021-06-28T19:33:40+02:00",
        "color": false,
        "body": null,
        "wait_number_of_hours_after_send": null,
        "sent_at": "2021-06-28T18:38:40+02:00",
        "only_send_if_booking_unconfirmed": false,
        "only_send_if_invoice_unread": false,
        "only_send_if_remittance_unread": true,
        "scheduled": false,
        "message_status": null,
        "error_code": null,
        "deleted": true,
        "created_at": "2021-06-28T18:33:40+02:00"
      }
    }
  ],
  "meta": {
    "pagination": {
      "total": 1,
      "count": 1,
      "per_page": 100,
      "current_page": 1,
      "total_pages": 1
    }
  },
  "links": {
    "self": "http://journalapitest.prodentor.se/api/sent-remittances?page=1",
    "first": "http://journalapitest.prodentor.se/api/sent-remittances?page=1",
    "last": "http://journalapitest.prodentor.se/api/sent-remittances?page=1"
  }
}
```
