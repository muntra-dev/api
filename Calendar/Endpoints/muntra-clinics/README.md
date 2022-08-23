## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /muntra-clinics | dtend, dtstart, include, include_administrative_roles, include_caregiver_locations_without_procedure_id_matches, new_patient, procedure_ids |


## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| clinic_name |  | string |
| clinic_address_1 |  | string |
| clinic_address_2 |  | string |
| clinic_postal_code |  | string |
| clinic_city |  | string |
| clinic_email_address |  | string |
| clinic_phone_number |  | string |
| clinic_phone_number_2 |  | string |
| clinic_phone_mobile |  | string |
| clinic_fax |  | string |
| clinic_professional_statement |  | string |
| default_sms_reminder_text |  | string |
| website_address |  | string |
| booking_requires_two_factor_authentication |  | boolean |
| active |  | boolean |
| latitude |  | number |
| longitude |  | number |
| google_places_description |  | string |
| accepts_children |  | boolean |
| accessible_via_elevator |  | boolean |
| accessible_via_stairs |  | boolean |
| capable_of_handling_fear_of_medical_procedures |  | boolean |
| handicap_accessible |  | boolean |
| has_drinks |  | boolean |
| has_free_parking_directly_outside_of_clinic |  | boolean |
| has_free_parking_near_the_clinic |  | boolean |
| has_magazines |  | boolean |
| has_music |  | booleanboolean |
| has_paid_parking_directly_outside_of_clinic |  | false |
| has_paid_parking_near_the_clinic |  | boolean |
| has_restroom |  | boolean |
| has_toys |  | boolean |
| has_tv |  | boolean |
| has_waiting_room |  | boolean |
| has_wifi |  | boolean |
| number_of_reviews |  | number |
| overall_rating |  | number |
| info_rating_advice_and_tips |  | number |
| info_rating_follow_up |  | number |
| info_rating_how_to_find_place |  | number |
| info_rating_patient_health |  | number |
| info_rating_patient_treatment |  | number |
| info_rating_pre_meeting |  | number |
| info_rating_pricing |  | number |
| rating_quality |  | number |
| rating_bedside_manner |  | number |
| rating_hygiene |  | number |
| rating_reception_on_arrival |  | number |
| rating_thoroughness |  | number |
| rating_wait_time |  | number |


## Relations
| Name | Cardinality | Data Model |
| ------------- | ------------- | ------------- |
|  | hasMany |  |
|  | belongsTo |  |

## Samples
### GET Request
#### URL
```
/api/muntra-clinics/177?dtend=2022-08-25T23%3A59%3A59%2B02%3A00&dtstart=2022-08-23T10%3A48%3A53%2B02%3A00&include=caregiver_locations.default_procedure.procedure%2Ccaregiver_locations.free_bookable_slots%2Ccaregiver_locations.caregivers.role%2Ccaregiver_locations.caregivers.default_user_image%2Ccaregiver_locations.procedures.procedure%2Cgoogle_place_detail.parent_place%2Clogotype%2Ccaregiver_locations.next_free_bookable_slot&include_administrative_roles=false&include_caregiver_locations_without_procedure_id_matches=true&new_patient=true&procedure_ids=1
```
#### Response Payload
```
{
  "data": {
    "type": "muntra_clinic",
    "id": "177",
    "attributes": {
      "clinic_name": "MyDentist Västerås",
      "clinic_address_1": "Vasagatan 20",
      "clinic_address_2": "",
      "clinic_postal_code": "72215",
      "clinic_city": "Västerås",
      "clinic_email_address": "vasteras@mydentist.se",
      "clinic_phone_number": "021-3720250",
      "clinic_phone_number_2": "",
      "clinic_phone_mobile": "+46213720250",
      "clinic_fax": "",
      "clinic_professional_statement": "",
      "default_sms_reminder_text": "Hej [patient_first_name]! Här är en påminnelse om din tid på [clinic_name] på [clinic_address_1] kl. [booking_time] den [booking_date]. \r\n\r\nVänligen ring 0213720250 eller maila vasteras@mydentist.se för att avboka eller boka om din tid senast 24h innan bokat besök.\r\n\r\nMvh, [caregiver_first_name], [caregiver_title].",
      "website_address": "https://www.mydentist.se/",
      "booking_requires_two_factor_authentication": false,
      "active": true,
      "latitude": 59.6109456,
      "longitude": 16.5456755,
      "google_places_description": "Vasagatan 20, Västerås, Sweden",
      "accepts_children": null,
      "accessible_via_elevator": false,
      "accessible_via_stairs": false,
      "capable_of_handling_fear_of_medical_procedures": true,
      "handicap_accessible": true,
      "has_drinks": null,
      "has_free_parking_directly_outside_of_clinic": false,
      "has_free_parking_near_the_clinic": false,
      "has_magazines": null,
      "has_music": null,
      "has_paid_parking_directly_outside_of_clinic": false,
      "has_paid_parking_near_the_clinic": true,
      "has_restroom": null,
      "has_toys": false,
      "has_tv": null,
      "has_waiting_room": true,
      "has_wifi": null,
      "number_of_reviews": 310,
      "overall_rating": 4.8,
      "info_rating_advice_and_tips": 4.7,
      "info_rating_follow_up": 4.67,
      "info_rating_how_to_find_place": 4.92,
      "info_rating_patient_health": 4.7,
      "info_rating_patient_treatment": 4.77,
      "info_rating_pre_meeting": 4.6899999999999995,
      "info_rating_pricing": 4.39,
      "rating_quality": 4.83,
      "rating_bedside_manner": 4.85,
      "rating_hygiene": 4.92,
      "rating_reception_on_arrival": 4.85,
      "rating_thoroughness": 4.85,
      "rating_wait_time": 4.59
    },
    "relationships": {
      "caregiver_locations": {
        "data": [
          {
            "type": "muntra_caregiver_at_location",
            "id": "15363"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15675"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15365"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15399"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15673"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15333"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15489"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15597"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15588"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15643"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "21390"
          },
          {
            "type": "muntra_caregiver_at_location",
            "id": "15361"
          }
        ]
      },
      "google_place_detail": {
        "data": {
          "type": "muntra_google_place_detail",
          "id": "EiFWYXNhZ2F0YW4gMjAsIFbDpHN0ZXLDpXMsIFN2ZXJpZ2UiUBJOCjQKMgmd-x7WPmFeRhHAwBUIQkU9QBoeCxDuwe6hARoUChIJY9LQ6U5hXkYR0hNhGPP-ABMMEBQqFAoSCVnAvVJJYV5GEd0qEXVCiTOn"
        }
      },
      "logotype": {
        "data": {
          "type": "muntra_clinic_image",
          "id": "4814"
        }
      }
    }
  },
  "included": [
    {
      "type": "muntra_role",
      "id": "3",
      "attributes": {
        "name": "Tandläkare",
        "slug": "dentist",
        "occupational_code": "TAN",
        "is_caregiver_role": true
      }
    },
    {
      "type": "muntra_procedure",
      "id": "1",
      "attributes": {
        "name": "Basundersökning av tandläkare"
      }
    },
    {
      "type": "muntra_procedure",
      "id": "4",
      "attributes": {
        "name": "Akut tandläkarundersökning"
      }
    },
    {
      "type": "muntra_education",
      "id": "247",
      "attributes": {
        "degree": "Doctor of Dental Surgery",
        "field_of_study": null,
        "school": "Umeå Universitet"
      }
    },
    {
      "type": "muntra_language",
      "id": "116",
      "attributes": {
        "iso_code": "sv",
        "name": "Svenska"
      }
    },
    {
      "type": "muntra_language",
      "id": "26",
      "attributes": {
        "iso_code": "en",
        "name": "Engelska"
      }
    },
    {
      "type": "muntra_user_image",
      "id": "4830",
      "attributes": {
        "original": "https://fileapi.muntra.se/images/eyJpdiI6ImlOTEwraFBRc0ZSc0x6cFdHbmxmR2c9PSIsInZhbHVlIjoiS1VySDliYTA0S0NYZjQ5NE5sT3ZWXC9DUjdMdWp5XC91SkhNTFZXb1wvWEw1NmtOTjNWbmxEMlg5cDIwUWtUOGsxellpbmM2N2RLK0NOTVd0ZGh4V3ZJQlVJZVdZa0tpTWxiRnB4VEkyckorcWM9IiwibWFjIjoiMGNhNTQyNThiYzI4MjJjYTFkN2NiNDExMzZkMDA5Zjc4YTkxN2UyMTc4MzY1YjczZjlmYjY5YzU0NTcxOTFlMCJ9",
        "small_thumbnail": "https://fileapi.muntra.se/images/eyJpdiI6ImlOTEwraFBRc0ZSc0x6cFdHbmxmR2c9PSIsInZhbHVlIjoiS1VySDliYTA0S0NYZjQ5NE5sT3ZWXC9DUjdMdWp5XC91SkhNTFZXb1wvWEw1NmtOTjNWbmxEMlg5cDIwUWtUOGsxellpbmM2N2RLK0NOTVd0ZGh4V3ZJQlVJZVdZa0tpTWxiRnB4VEkyckorcWM9IiwibWFjIjoiMGNhNTQyNThiYzI4MjJjYTFkN2NiNDExMzZkMDA5Zjc4YTkxN2UyMTc4MzY1YjczZjlmYjY5YzU0NTcxOTFlMCJ9?h=140&w=140&fit=crop",
        "large_thumbnail": "https://fileapi.muntra.se/images/eyJpdiI6ImlOTEwraFBRc0ZSc0x6cFdHbmxmR2c9PSIsInZhbHVlIjoiS1VySDliYTA0S0NYZjQ5NE5sT3ZWXC9DUjdMdWp5XC91SkhNTFZXb1wvWEw1NmtOTjNWbmxEMlg5cDIwUWtUOGsxellpbmM2N2RLK0NOTVd0ZGh4V3ZJQlVJZVdZa0tpTWxiRnB4VEkyckorcWM9IiwibWFjIjoiMGNhNTQyNThiYzI4MjJjYTFkN2NiNDExMzZkMDA5Zjc4YTkxN2UyMTc4MzY1YjczZjlmYjY5YzU0NTcxOTFlMCJ9?h=216&w=216&fit=crop"
      }
    },
    {
      "type": "muntra_role",
      "id": "4",
      "attributes": {
        "name": "Tandhygienist",
        "slug": "dental-hygienist",
        "occupational_code": "TAH",
        "is_caregiver_role": true
      }
    },
    {
      "type": "muntra_user_image",
      "id": "4835",
      "attributes": {
        "original": "https://fileapi.muntra.se/images/eyJpdiI6IkRxK2RlMlNhRk9SRm40akMzOGR3TVE9PSIsInZhbHVlIjoiZVJUUVh5SjBaS0tcL2w4N2lLSDFWTVZVRml3UTA4aXJCT0E4czFiQVFYNzNxNGdWYzNjZ25VVjc1dVozZElcLzEyOGJBaU5JZHBYaWl3R1RCc3plTldYVFJ4b0RLTEFuajRNMVduWjVEN1c1dz0iLCJtYWMiOiIyZGRjN2NmMGYxNGFhYzdlZWRmYmMwYjAxMGYyYTU4YTc1MWYyMTcxMWQ2Njc5Mjc5NGFhYzhjZDliZDhmZjJmIn0=",
        "small_thumbnail": "https://fileapi.muntra.se/images/eyJpdiI6IkRxK2RlMlNhRk9SRm40akMzOGR3TVE9PSIsInZhbHVlIjoiZVJUUVh5SjBaS0tcL2w4N2lLSDFWTVZVRml3UTA4aXJCT0E4czFiQVFYNzNxNGdWYzNjZ25VVjc1dVozZElcLzEyOGJBaU5JZHBYaWl3R1RCc3plTldYVFJ4b0RLTEFuajRNMVduWjVEN1c1dz0iLCJtYWMiOiIyZGRjN2NmMGYxNGFhYzdlZWRmYmMwYjAxMGYyYTU4YTc1MWYyMTcxMWQ2Njc5Mjc5NGFhYzhjZDliZDhmZjJmIn0=?h=140&w=140&fit=crop",
        "large_thumbnail": "https://fileapi.muntra.se/images/eyJpdiI6IkRxK2RlMlNhRk9SRm40akMzOGR3TVE9PSIsInZhbHVlIjoiZVJUUVh5SjBaS0tcL2w4N2lLSDFWTVZVRml3UTA4aXJCT0E4czFiQVFYNzNxNGdWYzNjZ25VVjc1dVozZElcLzEyOGJBaU5JZHBYaWl3R1RCc3plTldYVFJ4b0RLTEFuajRNMVduWjVEN1c1dz0iLCJtYWMiOiIyZGRjN2NmMGYxNGFhYzdlZWRmYmMwYjAxMGYyYTU4YTc1MWYyMTcxMWQ2Njc5Mjc5NGFhYzhjZDliZDhmZjJmIn0=?h=216&w=216&fit=crop"
      }
    },
    {
      "type": "muntra_procedure",
      "id": "135",
      "attributes": {
        "name": "Brush up"
      }
    },
    {
      "type": "muntra_procedure",
      "id": "9",
      "attributes": {
        "name": "Tandblekning"
      }
    },
    {
      "type": "muntra_procedure",
      "id": "148",
      "attributes": {
        "name": "Professionell tandrengöring"
      }
    },
    {
      "type": "muntra_procedure",
      "id": "2",
      "attributes": {
        "name": "Basundersökning av tandhygienist"
      }
    },
    {
      "type": "muntra_procedure",
      "id": "176",
      "attributes": {
        "name": "Månadens erbjudande augusti Brush up x3"
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "4755",
      "attributes": {
        "first_name": "Anders",
        "last_name": "Lundell",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 15,
        "overall_rating": 5,
        "info_rating_advice_and_tips": 4.45,
        "info_rating_follow_up": 4.67,
        "info_rating_how_to_find_place": 5,
        "info_rating_patient_health": 4.5,
        "info_rating_patient_treatment": 4.67,
        "info_rating_pre_meeting": 4.75,
        "info_rating_pricing": 4.67,
        "rating_quality": 5,
        "rating_bedside_manner": 5,
        "rating_hygiene": 5,
        "rating_reception_on_arrival": 5,
        "rating_thoroughness": 5,
        "rating_wait_time": 4.92
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5370",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6705",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "90935d22962e76862749a51de21fe202",
      "attributes": {
        "dtstart": "2022-09-01T08:00:00+02:00",
        "dtend": "2022-09-01T08:30:00+02:00"
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "5020",
      "attributes": {
        "first_name": "Shero",
        "last_name": "Hussein",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 48,
        "overall_rating": 4.98,
        "info_rating_advice_and_tips": 4.71,
        "info_rating_follow_up": 4.74,
        "info_rating_how_to_find_place": 4.9,
        "info_rating_patient_health": 4.6899999999999995,
        "info_rating_patient_treatment": 4.88,
        "info_rating_pre_meeting": 4.64,
        "info_rating_pricing": 4.1,
        "rating_quality": 4.93,
        "rating_bedside_manner": 4.84,
        "rating_hygiene": 4.98,
        "rating_reception_on_arrival": 4.84,
        "rating_thoroughness": 4.91,
        "rating_wait_time": 4.29
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": [
            {
              "type": "muntra_education",
              "id": "247"
            }
          ]
        },
        "languages": {
          "data": [
            {
              "type": "muntra_language",
              "id": "116"
            },
            {
              "type": "muntra_language",
              "id": "26"
            }
          ]
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5419",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6709",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "5a0548e566e112b20624896fa7a4a66d",
      "attributes": {
        "dtstart": "2022-09-08T11:00:00+02:00",
        "dtend": "2022-09-08T11:30:00+02:00"
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "4756",
      "attributes": {
        "first_name": "Marie",
        "last_name": "Berglöf",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "female",
        "active": true,
        "number_of_reviews": 24,
        "overall_rating": 4.96,
        "info_rating_advice_and_tips": 4.73,
        "info_rating_follow_up": 4.57,
        "info_rating_how_to_find_place": 5,
        "info_rating_patient_health": 5,
        "info_rating_patient_treatment": 5,
        "info_rating_pre_meeting": 4.91,
        "info_rating_pricing": 3.9,
        "rating_quality": 4.91,
        "rating_bedside_manner": 4.96,
        "rating_hygiene": 5,
        "rating_reception_on_arrival": 5,
        "rating_thoroughness": 4.96,
        "rating_wait_time": 4.96
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "c17c1481255b46fab0298e352f5185ed",
      "attributes": {
        "dtstart": "2022-08-24T12:00:00+02:00",
        "dtend": "2022-08-24T12:30:00+02:00"
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5371",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6708",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "4801",
      "attributes": {
        "first_name": "Samy",
        "last_name": "Mebdi",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 36,
        "overall_rating": 4.92,
        "info_rating_advice_and_tips": 4.9399999999999995,
        "info_rating_follow_up": 4.9399999999999995,
        "info_rating_how_to_find_place": 4.97,
        "info_rating_patient_health": 4.82,
        "info_rating_patient_treatment": 4.91,
        "info_rating_pre_meeting": 4.82,
        "info_rating_pricing": 4.79,
        "rating_quality": 4.97,
        "rating_bedside_manner": 4.9399999999999995,
        "rating_hygiene": 4.97,
        "rating_reception_on_arrival": 4.9399999999999995,
        "rating_thoroughness": 4.91,
        "rating_wait_time": 4.74
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": {
            "type": "muntra_user_image",
            "id": "4830"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5374",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6702",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "a8d5651f316f3d511a86b317f9a8feab",
      "attributes": {
        "dtstart": "2022-08-26T16:00:00+02:00",
        "dtend": "2022-08-26T16:30:00+02:00"
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "5018",
      "attributes": {
        "first_name": "Razieh",
        "last_name": "Ghobadi",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "female",
        "active": true,
        "number_of_reviews": 23,
        "overall_rating": 4.87,
        "info_rating_advice_and_tips": 4.75,
        "info_rating_follow_up": 4.65,
        "info_rating_how_to_find_place": 4.9,
        "info_rating_patient_health": 4.63,
        "info_rating_patient_treatment": 4.68,
        "info_rating_pre_meeting": 4.74,
        "info_rating_pricing": 4.35,
        "rating_quality": 4.86,
        "rating_bedside_manner": 4.86,
        "rating_hygiene": 4.86,
        "rating_reception_on_arrival": 4.91,
        "rating_thoroughness": 4.82,
        "rating_wait_time": 4.57
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "4"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": {
            "type": "muntra_user_image",
            "id": "4835"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5418",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "135"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6602",
      "attributes": {
        "frequency_in_minutes": 90,
        "duration_in_minutes_existing_patient": 90,
        "duration_in_minutes_new_patient": 90,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "9"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7454",
      "attributes": {
        "frequency_in_minutes": 40,
        "duration_in_minutes_existing_patient": 40,
        "duration_in_minutes_new_patient": 40,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "148"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7455",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "2"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7631",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "176"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "4744",
      "attributes": {
        "first_name": "Homi",
        "last_name": "Es",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 29,
        "overall_rating": 4.79,
        "info_rating_advice_and_tips": 4.75,
        "info_rating_follow_up": 4.64,
        "info_rating_how_to_find_place": 4.76,
        "info_rating_patient_health": 4.78,
        "info_rating_patient_treatment": 4.82,
        "info_rating_pre_meeting": 4.7,
        "info_rating_pricing": 4.48,
        "rating_quality": 4.76,
        "rating_bedside_manner": 4.83,
        "rating_hygiene": 4.9,
        "rating_reception_on_arrival": 4.79,
        "rating_thoroughness": 4.79,
        "rating_wait_time": 4.41
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "d11573ee87870b988d85078fc2521e14",
      "attributes": {
        "dtstart": "2022-08-24T08:00:00+02:00",
        "dtend": "2022-08-24T08:30:00+02:00"
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5366",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6707",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "3954",
      "attributes": {
        "first_name": "Karl Oscar Vilhelm",
        "last_name": "Hedlund",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 36,
        "overall_rating": 4.75,
        "info_rating_advice_and_tips": 4.63,
        "info_rating_follow_up": 4.6,
        "info_rating_how_to_find_place": 4.97,
        "info_rating_patient_health": 4.67,
        "info_rating_patient_treatment": 4.77,
        "info_rating_pre_meeting": 4.77,
        "info_rating_pricing": 4.29,
        "rating_quality": 4.76,
        "rating_bedside_manner": 4.82,
        "rating_hygiene": 4.82,
        "rating_reception_on_arrival": 4.82,
        "rating_thoroughness": 4.76,
        "rating_wait_time": 4.21
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "706fe33ae4c13900f8ca134854c73a84",
      "attributes": {
        "dtstart": "2022-08-23T11:10:00+02:00",
        "dtend": "2022-08-23T11:40:00+02:00"
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "5ee1bb5af86af07b20fddbcddfaaab16",
      "attributes": {
        "dtstart": "2022-08-23T16:30:00+02:00",
        "dtend": "2022-08-23T17:00:00+02:00"
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "3220",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6706",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "2699",
      "attributes": {
        "first_name": "Imad",
        "last_name": "Haddad",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 40,
        "overall_rating": 4.7,
        "info_rating_advice_and_tips": 4.74,
        "info_rating_follow_up": 4.74,
        "info_rating_how_to_find_place": 4.84,
        "info_rating_patient_health": 4.58,
        "info_rating_patient_treatment": 4.71,
        "info_rating_pre_meeting": 4.58,
        "info_rating_pricing": 4.53,
        "rating_quality": 4.89,
        "rating_bedside_manner": 4.88,
        "rating_hygiene": 4.9399999999999995,
        "rating_reception_on_arrival": 4.74,
        "rating_thoroughness": 4.86,
        "rating_wait_time": 4.8
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5406",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6703",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_free_bookable_slot",
      "id": "1f7afb2ca73c52a58ce38f7c9430463a",
      "attributes": {
        "dtstart": "2022-09-10T08:00:00+02:00",
        "dtend": "2022-09-10T08:30:00+02:00"
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "4960",
      "attributes": {
        "first_name": "Michael",
        "last_name": "Nilsson Ström",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 24,
        "overall_rating": 4.62,
        "info_rating_advice_and_tips": 4.84,
        "info_rating_follow_up": 4.85,
        "info_rating_how_to_find_place": 4.9,
        "info_rating_patient_health": 4.83,
        "info_rating_patient_treatment": 4.95,
        "info_rating_pre_meeting": 4.89,
        "info_rating_pricing": 4.8,
        "rating_quality": 4.85,
        "rating_bedside_manner": 4.95,
        "rating_hygiene": 5,
        "rating_reception_on_arrival": 5,
        "rating_thoroughness": 4.95,
        "rating_wait_time": 4.95
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5403",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6704",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "4"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "4995",
      "attributes": {
        "first_name": "Sara-Fatima",
        "last_name": "Karimi",
        "professional_statement": "Tandhygienist uppgifter",
        "title": "",
        "hide_reviews": false,
        "gender": "female",
        "active": true,
        "number_of_reviews": 31,
        "overall_rating": 4.45,
        "info_rating_advice_and_tips": 4.26,
        "info_rating_follow_up": 4.23,
        "info_rating_how_to_find_place": 4.93,
        "info_rating_patient_health": 4.52,
        "info_rating_patient_treatment": 4.22,
        "info_rating_pre_meeting": 4.33,
        "info_rating_pricing": 4.22,
        "rating_quality": 4.41,
        "rating_bedside_manner": 4.5600000000000005,
        "rating_hygiene": 4.7,
        "rating_reception_on_arrival": 4.59,
        "rating_thoroughness": 4.59,
        "rating_wait_time": 4.48
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "4"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5413",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "135"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6604",
      "attributes": {
        "frequency_in_minutes": 90,
        "duration_in_minutes_existing_patient": 90,
        "duration_in_minutes_new_patient": 90,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "9"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7456",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "2"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7457",
      "attributes": {
        "frequency_in_minutes": 40,
        "duration_in_minutes_existing_patient": 40,
        "duration_in_minutes_new_patient": 40,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "148"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7632",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "176"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "2698",
      "attributes": {
        "first_name": "Mohammed",
        "last_name": "Abdallatif",
        "professional_statement": null,
        "title": null,
        "hide_reviews": false,
        "gender": "male",
        "active": true,
        "number_of_reviews": 0,
        "overall_rating": 0,
        "info_rating_advice_and_tips": 0,
        "info_rating_follow_up": 0,
        "info_rating_how_to_find_place": 0,
        "info_rating_patient_health": 0,
        "info_rating_patient_treatment": 0,
        "info_rating_pre_meeting": 0,
        "info_rating_pricing": 0,
        "rating_quality": 0,
        "rating_bedside_manner": 0,
        "rating_hygiene": 0,
        "rating_reception_on_arrival": 0,
        "rating_thoroughness": 0,
        "rating_wait_time": 0
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "3"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7184",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 0
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "1"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver",
      "id": "4754",
      "attributes": {
        "first_name": "Suzan",
        "last_name": "Ali",
        "professional_statement": "",
        "title": "",
        "hide_reviews": false,
        "gender": "female",
        "active": true,
        "number_of_reviews": 0,
        "overall_rating": 0,
        "info_rating_advice_and_tips": 0,
        "info_rating_follow_up": 0,
        "info_rating_how_to_find_place": 0,
        "info_rating_patient_health": 0,
        "info_rating_patient_treatment": 0,
        "info_rating_pre_meeting": 0,
        "info_rating_pricing": 0,
        "rating_quality": 0,
        "rating_bedside_manner": 0,
        "rating_hygiene": 0,
        "rating_reception_on_arrival": 0,
        "rating_thoroughness": 0,
        "rating_wait_time": 0
      },
      "relationships": {
        "role": {
          "data": {
            "type": "muntra_role",
            "id": "4"
          }
        },
        "specialities": {
          "data": []
        },
        "educations": {
          "data": []
        },
        "languages": {
          "data": []
        },
        "default_user_image": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "5369",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "135"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "6606",
      "attributes": {
        "frequency_in_minutes": 90,
        "duration_in_minutes_existing_patient": 90,
        "duration_in_minutes_new_patient": 90,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "9"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_procedure_at_location",
      "id": "7633",
      "attributes": {
        "frequency_in_minutes": 30,
        "duration_in_minutes_existing_patient": 30,
        "duration_in_minutes_new_patient": 30,
        "minimum_age": 24
      },
      "relationships": {
        "procedure": {
          "data": {
            "type": "muntra_procedure",
            "id": "176"
          }
        }
      }
    },
    {
      "type": "muntra_google_place_detail",
      "id": "ChIJ8fA1bTmyXEYRYm-tjaLruCI",
      "attributes": {
        "include_in_sitemap": true,
        "name": "Sverige",
        "location_lat": "60.12816100000001",
        "location_lng": "18.643501",
        "viewport_northeast_lat": "69.0599709",
        "viewport_northeast_lng": "24.1773101",
        "viewport_southwest_lat": "55.0059799",
        "viewport_southwest_lng": "10.5798",
        "reference": "CmRbAAAAQvQYfFyVzflpkzUhPlMzb9NHe7WsYoKL-9oLMg74n8iBAY8-AKUSRblgi33PAWpR1T_XR4n0MLrkguBKmNuiyWfbxMJGOpVmR041pudhNufgd0d1oYbvH_xicKbcc38nEhC17qVIXfmdKYC4fIbL50r8GhTpXb-2386c21m8KnNJiM2iUoQxFw",
        "place_id": "ChIJ8fA1bTmyXEYRYm-tjaLruCI",
        "formatted_address": ""
      },
      "relationships": {
        "parent_place": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_google_place_detail",
      "id": "ChIJzRXH8jBhXkYRl-My_cp5cHk",
      "attributes": {
        "include_in_sitemap": true,
        "name": "Västmanlands län",
        "location_lat": "59.6713879",
        "location_lng": "16.2158953",
        "viewport_northeast_lat": "60.1906571",
        "viewport_northeast_lng": "16.9458588",
        "viewport_southwest_lat": "59.21625899999999",
        "viewport_southwest_lng": "15.4174699",
        "reference": "ChIJzRXH8jBhXkYRl-My_cp5cHk",
        "place_id": "ChIJzRXH8jBhXkYRl-My_cp5cHk",
        "formatted_address": ""
      },
      "relationships": {
        "parent_place": {
          "data": {
            "type": "muntra_google_place_detail",
            "id": "ChIJ8fA1bTmyXEYRYm-tjaLruCI"
          }
        }
      }
    },
    {
      "type": "muntra_google_place_detail",
      "id": "ChIJp6lbRYFCXkYRIEBl4rZdQbw",
      "attributes": {
        "include_in_sitemap": true,
        "name": "Västerås",
        "location_lat": "59.60990049999999",
        "location_lng": "16.5448092",
        "viewport_northeast_lat": "59.676659",
        "viewport_northeast_lng": "16.6539362",
        "viewport_southwest_lat": "59.57252499999999",
        "viewport_southwest_lng": "16.4362451",
        "reference": "ChIJp6lbRYFCXkYRIEBl4rZdQbw",
        "place_id": "ChIJp6lbRYFCXkYRIEBl4rZdQbw",
        "formatted_address": ""
      },
      "relationships": {
        "parent_place": {
          "data": {
            "type": "muntra_google_place_detail",
            "id": "ChIJzRXH8jBhXkYRl-My_cp5cHk"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15363",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "Ett bra bemötande och en bra behandling ingen stress."
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "4755"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5370"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6705"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "5370"
          }
        },
        "next_free_bookable_slot": {
          "data": {
            "type": "muntra_free_bookable_slot",
            "id": "90935d22962e76862749a51de21fe202"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15675",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "Snabb, professionell och mycket trevlig."
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "5020"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5419"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6709"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "6709"
          }
        },
        "next_free_bookable_slot": {
          "data": {
            "type": "muntra_free_bookable_slot",
            "id": "5a0548e566e112b20624896fa7a4a66d"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15365",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "Mycket bra 😀😀"
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "4756"
          }
        },
        "free_bookable_slots": {
          "data": [
            {
              "type": "muntra_free_bookable_slot",
              "id": "c17c1481255b46fab0298e352f5185ed"
            }
          ]
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5371"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6708"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "5371"
          }
        },
        "next_free_bookable_slot": {
          "data": {
            "type": "muntra_free_bookable_slot",
            "id": "c17c1481255b46fab0298e352f5185ed"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15399",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "Very clear and precis understanding of your situation and what is needed to be done "
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "4801"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5374"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6702"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "5374"
          }
        },
        "next_free_bookable_slot": {
          "data": {
            "type": "muntra_free_bookable_slot",
            "id": "a8d5651f316f3d511a86b317f9a8feab"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15673",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "Jättebra!"
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "5018"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5418"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6602"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7454"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7455"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7631"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "5418"
          }
        },
        "next_free_bookable_slot": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15333",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "An expert and a kind dentist."
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "4744"
          }
        },
        "free_bookable_slots": {
          "data": [
            {
              "type": "muntra_free_bookable_slot",
              "id": "d11573ee87870b988d85078fc2521e14"
            }
          ]
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5366"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6707"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "6707"
          }
        },
        "next_free_bookable_slot": {
          "data": {
            "type": "muntra_free_bookable_slot",
            "id": "d11573ee87870b988d85078fc2521e14"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15489",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "En superbra!! tandläkare."
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "3954"
          }
        },
        "free_bookable_slots": {
          "data": [
            {
              "type": "muntra_free_bookable_slot",
              "id": "706fe33ae4c13900f8ca134854c73a84"
            },
            {
              "type": "muntra_free_bookable_slot",
              "id": "5ee1bb5af86af07b20fddbcddfaaab16"
            }
          ]
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "3220"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6706"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "3220"
          }
        },
        "next_free_bookable_slot": {
          "data": {
            "type": "muntra_free_bookable_slot",
            "id": "706fe33ae4c13900f8ca134854c73a84"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15597",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "Imad gör dig lugn och trygg. Han är vänlig och det känns inte alls så läskigt att gå till tandläkaren när det är Imad som gör behandlingen. "
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "2699"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5406"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6703"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "6703"
          }
        },
        "next_free_bookable_slot": {
          "data": {
            "type": "muntra_free_bookable_slot",
            "id": "1f7afb2ca73c52a58ce38f7c9430463a"
          }
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15588",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "De kan förvänta sig en kompetent, lyhörd och inkännande tandläkare och hygienist. Som båda har förmågan att kommunicera väl under hela besöket och få sin patient att känna sig väl omhändertagen. Jag litar på deras tips och råd och fick mycket bra information med mig därifrån. De fick mig att känna att jag betalade för en hälso-behandling snarare än att jag bokat det \"obligatoriska\" tandläkarbesöket :) Jag är mycket nöjd.  "
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "4960"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5403"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6704"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "5403"
          }
        },
        "next_free_bookable_slot": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15643",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": true,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": "Proffsigt och situationsanpassat"
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "4995"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5413"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6604"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7456"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7457"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7632"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "5413"
          }
        },
        "next_free_bookable_slot": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "21390",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": false,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": null
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "2698"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7184"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "7184"
          }
        },
        "next_free_bookable_slot": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_caregiver_at_location",
      "id": "15361",
      "attributes": {
        "latitude": 59.6109456,
        "longitude": 16.5456755,
        "auto_approve_patient_booking": true,
        "require_patient_email": true,
        "require_patient_cellphone": true,
        "calendar_activated": false,
        "booking_requests_activated": false,
        "distance": null,
        "latest_review_comment": null
      },
      "relationships": {
        "clinic": {
          "data": {
            "type": "muntra_clinic",
            "id": "177"
          }
        },
        "caregiver": {
          "data": {
            "type": "muntra_caregiver",
            "id": "4754"
          }
        },
        "free_bookable_slots": {
          "data": []
        },
        "procedures": {
          "data": [
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "5369"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "6606"
            },
            {
              "type": "muntra_caregiver_procedure_at_location",
              "id": "7633"
            }
          ]
        },
        "default_procedure": {
          "data": {
            "type": "muntra_caregiver_procedure_at_location",
            "id": "5369"
          }
        },
        "next_free_bookable_slot": {
          "data": null
        }
      }
    },
    {
      "type": "muntra_google_place_detail",
      "id": "EiFWYXNhZ2F0YW4gMjAsIFbDpHN0ZXLDpXMsIFN2ZXJpZ2UiUBJOCjQKMgmd-x7WPmFeRhHAwBUIQkU9QBoeCxDuwe6hARoUChIJY9LQ6U5hXkYR0hNhGPP-ABMMEBQqFAoSCVnAvVJJYV5GEd0qEXVCiTOn",
      "attributes": {
        "include_in_sitemap": false,
        "name": "Vasagatan 20",
        "location_lat": "59.6109816",
        "location_lng": "16.5458181",
        "viewport_northeast_lat": "59.6122974302915",
        "viewport_northeast_lng": "16.5470022802915",
        "viewport_southwest_lat": "59.60959946970848",
        "viewport_southwest_lng": "16.54430431970849",
        "reference": "",
        "place_id": "EiFWYXNhZ2F0YW4gMjAsIFbDpHN0ZXLDpXMsIFN2ZXJpZ2UiUBJOCjQKMgmd-x7WPmFeRhHAwBUIQkU9QBoeCxDuwe6hARoUChIJY9LQ6U5hXkYR0hNhGPP-ABMMEBQqFAoSCVnAvVJJYV5GEd0qEXVCiTOn",
        "formatted_address": null
      },
      "relationships": {
        "parent_place": {
          "data": {
            "type": "muntra_google_place_detail",
            "id": "ChIJp6lbRYFCXkYRIEBl4rZdQbw"
          }
        }
      }
    },
    {
      "type": "muntra_clinic_image",
      "id": "4814",
      "attributes": {
        "name": "acab1398327437d0_org.png",
        "type": "image/png",
        "size_in_bytes": "43086",
        "backup": null,
        "backup_path": null,
        "st_ctim": null,
        "st_gid": null,
        "st_ino": null,
        "st_mode": null,
        "st_mtim": null,
        "st_size": null,
        "st_uid": null,
        "creation_date": "2022-04-11T13:28:41+02:00",
        "original": "https://fileapi.muntra.se/images/eyJpdiI6IjBwRk1LanNpTWxzaVp1XC9zNHpmdmhBPT0iLCJ2YWx1ZSI6InJsT3JsY1dVVXoreTQxU2VFUEdwSWlPdklpbVA3djhZdEtmMU1MMDFXTU01Q3J5VEg5ZWh4d1ZpTHJ4NmFSUjE1UzZqSWc0V2lSMk9zM2dHOUVXZ0V2d0M5WURWeUJYNTR2UnRDRHBReU1zPSIsIm1hYyI6ImQ4NTZiODY3YjI1MTM5N2M0YTBjZjMzNzFiNmZlNGFjY2I0YzM1MGYwODY2NWM2ZmJmN2YyODM4MzUzNGQwYTIifQ==",
        "small_thumbnail": "https://fileapi.muntra.se/images/eyJpdiI6IjBwRk1LanNpTWxzaVp1XC9zNHpmdmhBPT0iLCJ2YWx1ZSI6InJsT3JsY1dVVXoreTQxU2VFUEdwSWlPdklpbVA3djhZdEtmMU1MMDFXTU01Q3J5VEg5ZWh4d1ZpTHJ4NmFSUjE1UzZqSWc0V2lSMk9zM2dHOUVXZ0V2d0M5WURWeUJYNTR2UnRDRHBReU1zPSIsIm1hYyI6ImQ4NTZiODY3YjI1MTM5N2M0YTBjZjMzNzFiNmZlNGFjY2I0YzM1MGYwODY2NWM2ZmJmN2YyODM4MzUzNGQwYTIifQ==?h=140&w=140&fit=crop",
        "large_thumbnail": "https://fileapi.muntra.se/images/eyJpdiI6IjBwRk1LanNpTWxzaVp1XC9zNHpmdmhBPT0iLCJ2YWx1ZSI6InJsT3JsY1dVVXoreTQxU2VFUEdwSWlPdklpbVA3djhZdEtmMU1MMDFXTU01Q3J5VEg5ZWh4d1ZpTHJ4NmFSUjE1UzZqSWc0V2lSMk9zM2dHOUVXZ0V2d0M5WURWeUJYNTR2UnRDRHBReU1zPSIsIm1hYyI6ImQ4NTZiODY3YjI1MTM5N2M0YTBjZjMzNzFiNmZlNGFjY2I0YzM1MGYwODY2NWM2ZmJmN2YyODM4MzUzNGQwYTIifQ==?h=216&w=216&fit=crop"
      }
    }
  ]
}
```
