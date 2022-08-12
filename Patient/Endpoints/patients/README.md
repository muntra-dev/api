## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /patients | history_id, include, include_first_future_booking, include_latest_unbooked_rebooking, organization_id, patient_id |
| GET | /patients | birth_year_parity, check_exceeds_page, clinic_ids, exclude_examined_in_current_year, from_patient_birth_date, has_email, include, include_first_future_booking, include_latest_unbooked_rebooking, order, page, patient_tag_ids, per_page, rebooking_from_date, rebooking_to_date, sort_by, status, to_patient_birth_date, user_ids |

## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| address_1 |  | string |
| address_2 |  | string |
| auto_include_email_invitation |  | boolean |
| auto_include_sms_invitation |  | boolean |
| auto_include_sms_reminder |  | boolean |
| auto_include_snail_mail_invitation |  | boolean |
| booking_status |  | string |
| city |  | string |
| county_council_certificate_end_date |  | string |
| county_council_certificate_number |  | string |
| created_at |  | isodate |
| date_of_birth |  | isodate |
| deleted |  | boolean |
| e_mail_address |  | string |
| end_date_free_card |  | isodate |
| euro_certificate_number |  | string |
| external_dentist |  | string |
| external_hygienist |  | string |
| fax_number |  | string |
| first_name |  | string |
| free_card_number |  | string |
| gender |  | string |
| initials |  | string |
| invoice_reference |  | string |
| last_name |  | string |
| maiden_name |  | string |
| municipality |  | string |
| notes |  | string |
| passport_number |  | string |
| patient_number |  | string |
| phone_number_cell |  | string |
| phone_number_home |  | string |
| phone_number_work |  | string |
| postal_code |  | string |
| prefers_not_to_be_contacted_by_clinic |  | boolean |
| protected_identity |  | boolean |
| recurring |  | boolean |
| referral_source |  | string |
| signed_at |  | isodate |
| social_security_number |  | string |
| start_date_free_card |  | isodate |
| status |  | string |
| teeth_count |  | number |
| updated_at |  | isodate |
| untreated_teeth_count |  | number |
| wants_anestesia |  | boolean |
| warning |  | boolean |
| warning_text |  | string |
| xray_id |  | string |


## Relations
| Name | Cardinality | Data Model |
| ------------- | ------------- | ------------- |
| booking_attendees | hasMany | booking-attendee |
| booking_preferences | hasMany | booking-preference |
| claims | hasMany | validate-claim |
| clinic | belongsTo | clinic |
| county_council | belongsTo | county-council |
| county_council_patient_category | belongsTo | county-council-patient-category |
| declaration | belongsTo | declaration |
| default_reimbursement_type | belongsTo | reimbursement-type |
| dental_lab_orders | hasMany | dental-lab-order |
| elements | hasMany | element |
| emails | hasMany | email |
| files | hasMany | file |
| invoices | hasMany | patient-invoice |
| journal_entries | hasMany | journal-entry |
| last_credit_check | belongsTo | credit-check |
| last_risk_evaluation | belongsTo | risk-evaluation |
| last_tanden_check | belongsTo | [tanden-check](../tanden-checks/) |
| location | belongsTo | location |
| mounts | hasMany | mount |
| parodont_journal_entries | hasMany | parodont-journal-entry |
| patient_tags | hasMany | patient-tag |
| payments | hasMany | invoice-payment |
| prescriptions | hasMany | human-prescription |
| rebooking_defaults | hasMany | rebooking-default |
| rebookings | hasMany | rebooking |
| remittances | hasMany | remittance |
| reviews | hasMany | patient-review |
| signer | belongsTo | user |
| sms | hasMany | sms |
| state_registration | belongsTo | state-registration |
| stb_disease | belongsTo | [stb-disease](../stb-diseases/) |
| teeth | hasMany | tooth |
| user | belongsTo | user |

## Samples
### GET Request
#### URL
```
/api/patients?history_id=draft&include=booking_attendees.booking%2Cbooking_preferences.weekdays%2Cclinic%2Ccountry%2Ccounty_council.used_county_council_price_list%2Ccounty_council_patient_category%2Cdefault_reimbursement_type%2Clast_credit_check.currency%2Clast_tanden_check.currency%2Clast_tanden_check.insurance_contract.journal_diagnoses%2Clast_tanden_check.new_atb%2Clast_tanden_check.old_atb%2Clocation.third_party%2Cpatient_tags%2Crebooking_defaults.booking_type%2Crebooking_defaults.clinic%2Crebooking_defaults.user%2Crebookings.booking%2Csigner.role%2Cstate_registration.country%2Cstate_registration.sender.role%2Cstb_disease%2Cuser&include_first_future_booking=true&include_latest_unbooked_rebooking=true&organization_id=2&patient_id=327
```
#### Response Payload
```
{
  "data": {
    "type": "patient",
    "id": "327",
    "attributes": {
      "social_security_number": "199302182212",
      "first_name": "Test",
      "last_name": "Patient",
      "maiden_name": null,
      "initials": null,
      "gender": "male",
      "address_1": "Testvägen 13",
      "address_2": null,
      "city": "Uppsala",
      "postal_code": "12345",
      "municipality": null,
      "date_of_birth": "1981-08-11T00:00:00+02:00",
      "passport_number": null,
      "phone_number_cell": "+46734100450",
      "phone_number_home": null,
      "phone_number_work": null,
      "fax_number": null,
      "e_mail_address": "rask.niels@gmail.com",
      "deleted": false,
      "created_at": "2019-12-13T16:23:02+01:00",
      "updated_at": "2022-06-14T15:50:08+02:00",
      "patient_number": "238",
      "invoice_reference": "test",
      "status": "active",
      "wants_anestesia": false,
      "start_date_free_card": "2020-10-27T00:00:00+01:00",
      "end_date_free_card": "2020-11-08T00:00:00+01:00",
      "free_card_number": "12341234",
      "county_council_certificate_number": "1234",
      "county_council_certificate_end_date": "2021-09-21T00:00:00+02:00",
      "euro_certificate_number": null,
      "protected_identity": true,
      "warning": true,
      "warning_text": null,
      "xray_id": "198112111144",
      "notes": null,
      "external_dentist": null,
      "external_hygienist": null,
      "auto_include_email_invitation": false,
      "auto_include_sms_invitation": null,
      "auto_include_sms_reminder": null,
      "auto_include_snail_mail_invitation": null,
      "prefers_not_to_be_contacted_by_clinic": true,
      "recurring": true,
      "referral_source": "journal",
      "teeth_count": 24,
      "untreated_teeth_count": 24,
      "signed_at": null,
      "booking_status": "patient_not_to_be_contacted"
    },
    "relationships": {
      "country": {
        "data": null
      },
      "clinic": {
        "data": {
          "type": "clinic",
          "id": "2"
        }
      },
      "user": {
        "data": {
          "type": "user",
          "id": "4"
        }
      },
      "location": {
        "data": {
          "type": "location",
          "id": "753"
        }
      },
      "stb_disease": {
        "data": {
          "type": "stb_disease",
          "id": "1"
        }
      },
      "default_reimbursement_type": {
        "data": {
          "type": "reimbursement_type",
          "id": "3"
        }
      },
      "county_council": {
        "data": {
          "type": "county_council",
          "id": "1"
        }
      },
      "county_council_patient_category": {
        "data": {
          "type": "county_council_patient_category",
          "id": "43"
        }
      },
      "booking_attendees": {
        "data": [
          {
            "type": "booking_attendee",
            "id": "8166"
          }
        ]
      },
      "rebookings": {
        "data": [
          {
            "type": "rebooking",
            "id": "279"
          },
          {
            "type": "rebooking",
            "id": "280"
          },
          {
            "type": "rebooking",
            "id": "281"
          },
          {
            "type": "rebooking",
            "id": "282"
          },
          {
            "type": "rebooking",
            "id": "283"
          },
          {
            "type": "rebooking",
            "id": "284"
          },
          {
            "type": "rebooking",
            "id": "285"
          },
          {
            "type": "rebooking",
            "id": "286"
          },
          {
            "type": "rebooking",
            "id": "287"
          },
          {
            "type": "rebooking",
            "id": "288"
          },
          {
            "type": "rebooking",
            "id": "289"
          },
          {
            "type": "rebooking",
            "id": "290"
          },
          {
            "type": "rebooking",
            "id": "291"
          },
          {
            "type": "rebooking",
            "id": "307"
          }
        ]
      },
      "rebooking_defaults": {
        "data": [
          {
            "type": "rebooking_default",
            "id": "52"
          },
          {
            "type": "rebooking_default",
            "id": "54"
          }
        ]
      },
      "booking_preferences": {
        "data": [
          {
            "type": "booking_preference",
            "id": "9"
          }
        ]
      },
      "last_tanden_check": {
        "data": {
          "type": "tanden_check",
          "id": "22850"
        }
      },
      "signer": {
        "data": null
      },
      "last_credit_check": {
        "data": {
          "type": "credit_check",
          "id": "8"
        }
      },
      "patient_tags": {
        "data": []
      },
      "state_registration": {
        "data": null
      }
    }
  },
  "included": [
    {
      "type": "third_party",
      "id": "754",
      "attributes": {
        "organization_number": "1234123412",
        "organization_name": "Test Delete",
        "invoice_address_1": "rtrest",
        "invoice_address_2": "tewt",
        "invoice_postal_code": "12345",
        "invoice_city": "sadgasd",
        "invoice_email_address": "",
        "invoice_phone_number": "",
        "invoice_phone_number_2": "",
        "invoice_phone_mobile": "",
        "invoice_fax": "",
        "created_at": "2022-06-07T15:39:52+02:00",
        "updated_at": "2022-06-07T15:43:26+02:00"
      }
    },
    {
      "type": "payer_type",
      "id": "2",
      "attributes": {
        "name": "Landsting",
        "object_model": "county-council",
        "object_property": "id"
      }
    },
    {
      "type": "county_council_price_list",
      "id": "3",
      "attributes": {
        "name": "Folktandvården Uppsala, 2017-01-01 - 2018-01-XX",
        "deleted": false,
        "created_at": "2017-09-30T19:03:49+02:00",
        "updated_at": "2018-10-13T17:19:05+02:00"
      }
    },
    {
      "type": "booking",
      "id": "3494",
      "attributes": {
        "class": "PUBLIC",
        "summary": "Parod",
        "text": "Parod",
        "dtstamp": "2022-03-08T00:56:00+01:00",
        "dtstart": "2022-11-08T07:00:00+01:00",
        "dtend": "2022-11-08T08:00:00+01:00",
        "reschedulable": true,
        "duration_in_minutes": null,
        "description": "Parod",
        "location": "Muntra, test, Mäster Samuelsgatan 36 Stockholm Sverige",
        "transparent": false,
        "status": "CONFIRMED",
        "price": null,
        "new_patient": false,
        "patient_wants_earlier_slot": false,
        "patient_made_late_cancellation": false,
        "patient_failed_to_appear": false,
        "patient_failed_to_appear_handled": false,
        "patient_declaration_allowed": false,
        "done": false
      }
    },
    {
      "type": "clinic",
      "id": "2",
      "attributes": {
        "clinic_name": "Muntra, test",
        "clinic_address_1": "Katarinavägen 15 ",
        "clinic_address_2": "C/O Epicenter",
        "clinic_postal_code": "11157",
        "clinic_city": "Stockholm",
        "clinic_reference": null,
        "clinic_email_address": "a.haseeb19@gmail.com",
        "clinic_phone_number": "+4632240541",
        "clinic_phone_number_2": "+46734100450",
        "clinic_phone_mobile": "+46734100450",
        "clinic_fax": "",
        "clinic_professional_statement": "Specialistklinik fokuserad på estetiska behandlingar. Tandläkare med specialistexamen.  Ny rad.",
        "workplace_code": "4000000000000",
        "website_address": "https://www.muntra.se",
        "booking_requires_two_factor_authentication": false,
        "active": true,
        "timezone": "Europe/Stockholm",
        "latitude": 59.3192383,
        "longitude": 18.0753312,
        "google_places_description": "Muntra AB, Katarinavägen, Stockholm, Sverige",
        "journal_entry_autosign_limit_in_days": 1,
        "journal_entry_unsign_limit_in_days": 30,
        "default_sms_invitation_text": "Hej [patient_first_name]! Välkommen [booking_daydatetime] till [clinic_address_1]. Bekräfta tiden via [booking_confirmation_link]",
        "default_sms_reminder_text": "PÅMINNELSE: Hej [patient_first_name]! Nu är det dags att besöka oss. Välkommen till [clinic_name] på [clinic_address_1] kl. [booking_time] den [booking_date]. Mvh, [caregiver_first_name] [caregiver_last_name], [caregiver_title]",
        "default_snail_mail_invitation_text": "Hej [patient_first_name]!\r\n\r\n\r\n\r\nNu är det dags att besöka oss.\r\n\r\nVälkommen till [clinic_name] på [clinic_address_1] kl. [booking_time] den [booking_date].\r\n\r\nBekräfta gärna tiden genom att gå till följande länk: [booking_confirmation_link]\r\n\r\nMed vänlig hälsning,\r\n[caregiver_first_name] [caregiver_last_name], [caregiver_title]",
        "default_hours_until_sms_invitation_sent": 72,
        "default_hours_before_sms_reminder_sent": 48,
        "default_hours_until_snail_mail_invitation_sent": 168,
        "allow_remittance_without_individual_recipient": true,
        "accepts_digital_remittance": true,
        "has_cbct": true,
        "created_at": "2017-09-11T15:30:22+02:00",
        "updated_at": "2022-04-29T07:07:08+02:00"
      }
    },
    {
      "type": "user",
      "id": "4",
      "attributes": {
        "social_security_number": "198108111496",
        "first_name": "Niels",
        "last_name": "Rask",
        "maiden_name": "",
        "initials": "NR",
        "gender": "male",
        "address_1": "Hejgatan 4",
        "address_2": "",
        "city": "Bromma",
        "postal_code": "16733",
        "municipality": "Bromma kommun",
        "date_of_birth": "1981-08-18T00:00:00+02:00",
        "passport_number": "",
        "phone_number_cell": "+46734100450",
        "phone_number_home": "+46840906890",
        "phone_number_work": "+46840906890",
        "fax_number": "",
        "e_mail_address": "niels@muntra.se",
        "deleted": null,
        "created_at": "2017-09-11T15:28:20+02:00",
        "updated_at": "2022-06-12T17:23:49+02:00",
        "active": true,
        "prescriber_code": "9001",
        "professional_statement": "Tandläkare med specialistexamen. Tandläkare med specialistexamen. Tandläkare med specialistexamen. Tandläkare med specialistexamen. Tandläkare med specialistexamen. Tandläkare med specialistexamen. Tandläkare med specialistexamen. Tandläkare med specialistexamen. \r\nNy rad.",
        "title": "Specialisttandläkare Ortodonti, Odont. Dr.",
        "hide_reviews": false,
        "hide_reviews_discreetly": false,
        "number_of_reviews": 21,
        "overall_rating": 4.38
      }
    },
    {
      "type": "booking_type",
      "id": "10",
      "attributes": {
        "name": "Akut",
        "text": "Akut",
        "color": "rgba(208, 94, 99, 1.0)",
        "text_color": "rgba(255, 255, 255, 1.0)",
        "color_order": 9,
        "duration_in_minutes": 30,
        "reschedulable": false,
        "patient_declaration_allowed": true,
        "default": true
      }
    },
    {
      "type": "weekday",
      "id": "1",
      "attributes": {
        "day": 1
      }
    },
    {
      "type": "weekday",
      "id": "2",
      "attributes": {
        "day": 2
      }
    },
    {
      "type": "old_atb",
      "id": "70",
      "attributes": {
        "amount": 300,
        "start_date": "2020-07-01T00:00:00+02:00",
        "end_date": "2022-06-30T00:00:00+02:00",
        "used": true
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
    },
    {
      "type": "location",
      "id": "753",
      "attributes": {
        "address_1": "test",
        "address_2": "test",
        "city": "test",
        "postal_code": "12345"
      },
      "relationships": {
        "third_party": {
          "data": {
            "type": "third_party",
            "id": "754"
          }
        }
      }
    },
    {
      "type": "stb_disease",
      "id": "1",
      "attributes": {
        "code": "1100",
        "description": "Muntorrhet pga. läkemedelsbehandling"
      }
    },
    {
      "type": "reimbursement_type",
      "id": "3",
      "attributes": {
        "name": "Landsting",
        "active": true
      },
      "relationships": {
        "payer_types": {
          "data": [
            {
              "type": "payer_type",
              "id": "2"
            }
          ]
        },
        "reimbursement_rules": {
          "data": []
        }
      }
    },
    {
      "type": "county_council",
      "id": "1",
      "attributes": {
        "invoice_address_1": "Folktandvården FE72",
        "invoice_address_2": "Refnr: TV3150001 Box 6363 ",
        "invoice_city": "Uppsala",
        "invoice_postal_code": "75135",
        "organization_name": "Folktandvården Uppsala"
      },
      "relationships": {
        "used_county_council_price_list": {
          "data": {
            "type": "county_council_price_list",
            "id": "3"
          }
        }
      }
    },
    {
      "type": "county_council_patient_category",
      "id": "43",
      "attributes": {
        "code": "S15",
        "label": "Behandling av frätskador på tänderna som orsakats av anorexia nervosa, bulimia nervosa eller gastroesofageal refluxsjukdom på patienter som är medicinskt rehabiliterade"
      }
    },
    {
      "type": "booking_attendee",
      "id": "8166",
      "attributes": {
        "dtstart": null,
        "dtend": null,
        "partstat": "NEEDS-ACTION",
        "rsvp": true,
        "first_sendout_on": "2022-09-09T07:00:00+02:00",
        "arrived_at": null
      },
      "relationships": {
        "booking": {
          "data": {
            "type": "booking",
            "id": "3494"
          }
        }
      }
    },
    {
      "type": "rebooking",
      "id": "279",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:09+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "280",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:10+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "281",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:11+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "282",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:12+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "283",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:12+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "284",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:13+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "285",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:14+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "286",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:15+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "287",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:16+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "288",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:17+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "289",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:17+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "290",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:18+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "291",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:55:19+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking",
      "id": "307",
      "attributes": {
        "date": "2023-09-16T00:00:00+02:00",
        "description": "Parod",
        "duration_in_minutes": 60,
        "rebooked": false,
        "last_treatment_date": null,
        "next_treatment_date": null,
        "created_at": "2022-03-16T16:56:25+01:00"
      },
      "relationships": {
        "booking": {
          "data": null
        }
      }
    },
    {
      "type": "rebooking_default",
      "id": "52",
      "attributes": {
        "description": "Akut",
        "status": null,
        "booking_duration": 25,
        "months_to_booking": 18,
        "auto_rebook": false
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "clinic",
            "id": "2"
          }
        },
        "user": {
          "data": {
            "type": "user",
            "id": "4"
          }
        },
        "booking_type": {
          "data": {
            "type": "booking_type",
            "id": "10"
          }
        }
      }
    },
    {
      "type": "rebooking_default",
      "id": "54",
      "attributes": {
        "description": "Akut",
        "status": null,
        "booking_duration": 50,
        "months_to_booking": 18,
        "auto_rebook": true
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "clinic",
            "id": "2"
          }
        },
        "user": {
          "data": {
            "type": "user",
            "id": "4"
          }
        },
        "booking_type": {
          "data": {
            "type": "booking_type",
            "id": "10"
          }
        }
      }
    },
    {
      "type": "booking_preference",
      "id": "9",
      "attributes": {
        "dtstart_in_minutes": 900,
        "dtend_in_minutes": 1020,
        "fit": true
      },
      "relationships": {
        "weekdays": {
          "data": [
            {
              "type": "weekday",
              "id": "1"
            },
            {
              "type": "weekday",
              "id": "2"
            }
          ]
        }
      }
    },
    {
      "type": "tanden_check",
      "id": "22850",
      "attributes": {
        "eligble": true,
        "eligible_from_date": "2005-01-01T00:00:00+01:00",
        "stb_amount_available": 600,
        "hcd_amount": 10490,
        "hcd_start_date": "2020-12-14T00:00:00+01:00",
        "hcd_end_date": "2021-12-13T00:00:00+01:00",
        "last_treatment_date": "2021-05-07T00:00:00+02:00",
        "faultcode": null,
        "faultstring": null,
        "error_code": null,
        "error_text": null
      },
      "relationships": {
        "old_atb": {
          "data": {
            "type": "old_atb",
            "id": "70"
          }
        },
        "new_atb": {
          "data": null
        },
        "insurance_contract": {
          "data": null
        },
        "currency": {
          "data": {
            "type": "currency",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "credit_check",
      "id": "8",
      "attributes": {
        "amount": 3000,
        "approved": true,
        "created_at": "2021-10-20T15:52:40+02:00",
        "valid_until": "2022-01-18T00:00:00+01:00"
      },
      "relationships": {
        "currency": {
          "data": {
            "type": "currency",
            "id": "1"
          }
        }
      }
    }
  ]
}
```
