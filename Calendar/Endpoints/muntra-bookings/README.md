## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /muntra-bookings | order, per_page, sort_by, status, from_date, iclude|
| POST | /muntra-bookings | caregiver_id, patient_personal_id |
| POST | /muntra-bookings/${bookingData.id}/reschedule | new_dtstart |

## Attributes
| Name | Info | Type |
| ------------- | ------------- | ------------- |
| booked_by_patient |  | boolean |
| class |  | string |
| description |  | string |
| dtend |  | isodate |
| dtstamp |  | isodate |
| dtstart |  | isodate |
| duration_in_minutes |  | number |
| location |  | string |
| new_patient |  | boolean |
| patient_declaration_allowed |  | boolean |
| price |  | number |
| promo_code |  | string |
| referral_source |  | string |
| reschedulable |  | boolean |
| status |  | string |
| summary |  | string |
| text |  | string |
| transparent |  | boolean |

## Relations
| Name | Cardinality | Data Model |
| ------------- | ------------- | ------------- |
| booking_attendees | hasMany | muntra_booking_attendee |
| clinic | belongsTo | muntra_clinic |
| organizer | belongsTo | muntra_caregiver |
| procedure | belongsTo | muntra_procedure |

## Samples
### GET Request
#### URL
```
/api/muntra-bookings?x=y
```
#### Response Payload
```
{
   "data":[
      {
         "type":"muntra_booking",
         "id":"BK003i3iany4",
         "attributes":{
            "class":"PUBLIC",
            "summary":"Pat.bokning: Basunders\u00f6kning av tandl\u00e4kare",
            "text":"",
            "dtstamp":"2022-06-02T09:18:00+02:00",
            "dtstart":"2022-06-03T09:30:00+02:00",
            "dtend":"2022-06-03T10:00:00+02:00",
            "reschedulable":true,
            "duration_in_minutes":null,
            "description":"Hej Hanna,\r\n \r\nV\u00e4lkommen till Muntra 2 AB. H\u00e4r \u00e4r en bekr\u00e4ftelse av din tid hos oss kl. 9:30 den 3 juni 2022.\r\n \r\nMed v\u00e4nliga h\u00e4lsningar,\r\nTandl\u00e4kare Filip Heinel\r\n \r\nBoka din n\u00e4sta behandling direkt online p\u00e5 www.muntra.com",
            "location":"Convendum, 12341 Stockholm",
            "transparent":false,
            "status":"CONFIRMED",
            "price":null,
            "booked_by_patient":true,
            "new_patient":true,
            "patient_declaration_allowed":false,
            "referral_source":"",
            "promo_code":null
         },
         "relationships":{
            "organizer":{
               "data":{
                  "type":"muntra_caregiver",
                  "id":"2040"
               }
            },
            "procedure":{
               "data":{
                  "type":"muntra_procedure",
                  "id":"2"
               }
            },
            "booking_attendees":{
               "data":[
                  {
                     "type":"muntra_booking_attendee",
                     "id":"BA0307186h1c"
                  },
                  {
                     "type":"muntra_booking_attendee",
                     "id":"BAiq21eas14v"
                  }
               ]
            },
            "clinic":{
               "data":{
                  "type":"muntra_clinic",
                  "id":"768"
               }
            }
         }
      }
   ],
   "included":[
      {
         "type":"muntra_role",
         "id":"3",
         "attributes":{
            "name":"Tandl\u00e4kare",
            "slug":"dentist",
            "occupational_code":"TAN",
            "is_caregiver_role":true
         }
      },
      {
         "type":"muntra_patient",
         "id":"202",
         "attributes":{
            "social_security_number":"198204114063",
            "first_name":"Hanna",
            "last_name":"Van Gilse Van Der Pals",
            "gender":"female",
            "city":"Bromma",
            "address_1":"Frans Kriegs v\u00e4g 16",
            "address_2":null,
            "postal_code":"16733",
            "accepts_review_request_emails":true
         }
      },
      {
         "type":"muntra_caregiver",
         "id":"2040",
         "attributes":{
            "first_name":"Filip",
            "last_name":"Heinel",
            "professional_statement":"",
            "title":"",
            "hide_reviews":false,
            "gender":"male",
            "active":true,
            "number_of_reviews":0,
            "overall_rating":0,
            "info_rating_advice_and_tips":0,
            "info_rating_follow_up":0,
            "info_rating_how_to_find_place":0,
            "info_rating_patient_health":0,
            "info_rating_patient_treatment":0,
            "info_rating_pre_meeting":0,
            "info_rating_pricing":0,
            "rating_quality":0,
            "rating_bedside_manner":0,
            "rating_hygiene":0,
            "rating_reception_on_arrival":0,
            "rating_thoroughness":0,
            "rating_wait_time":0
         },
         "relationships":{
            "role":{
               "data":{
                  "type":"muntra_role",
                  "id":"3"
               }
            },
            "specialities":{
               "data":[
                  
               ]
            },
            "educations":{
               "data":[
                  
               ]
            },
            "languages":{
               "data":[
                  
               ]
            },
            "default_user_image":{
               "data":null
            }
         }
      },
      {
         "type":"muntra_procedure",
         "id":"2",
         "attributes":{
            "name":"Basunders\u00f6kning av tandl\u00e4kare"
         }
      },
      {
         "type":"muntra_booking_attendee",
         "id":"BA0307186h1c",
         "attributes":{
            "partstat":"ACCEPTED",
            "rsvp":true
         },
         "relationships":{
            "patient":{
               "data":{
                  "type":"muntra_patient",
                  "id":"202"
               }
            },
            "user":{
               "data":null
            }
         }
      },
      {
         "type":"muntra_booking_attendee",
         "id":"BAiq21eas14v",
         "attributes":{
            "partstat":"ACCEPTED",
            "rsvp":false
         },
         "relationships":{
            "patient":{
               "data":null
            },
            "user":{
               "data":{
                  "type":"muntra_caregiver",
                  "id":"2040"
               }
            }
         }
      },
      {
         "type":"muntra_clinic",
         "id":"768",
         "attributes":{
            "clinic_name":"Muntra 2 AB",
            "clinic_address_1":"Convendum",
            "clinic_address_2":"",
            "clinic_postal_code":"12341",
            "clinic_city":"Stockholm",
            "clinic_email_address":"niels@muntra.se",
            "clinic_phone_number":"",
            "clinic_phone_number_2":"",
            "clinic_phone_mobile":"",
            "clinic_fax":"",
            "clinic_professional_statement":"",
            "default_sms_reminder_text":"Hej [patient_first_name]! H\u00e4r \u00e4r en p\u00e5minnelse om din tid p\u00e5 [clinic_name] p\u00e5 [clinic_address_1] kl. [booking_time] den [booking_date]. Mvh, [caregiver_first_name] [caregiver_last_name], [caregiver_title]",
            "website_address":"",
            "booking_requires_two_factor_authentication":true,
            "active":true,
            "latitude":0,
            "longitude":0,
            "google_places_description":"",
            "accepts_children":null,
            "accessible_via_elevator":null,
            "accessible_via_stairs":null,
            "capable_of_handling_fear_of_medical_procedures":null,
            "handicap_accessible":null,
            "has_drinks":null,
            "has_free_parking_directly_outside_of_clinic":null,
            "has_free_parking_near_the_clinic":null,
            "has_magazines":null,
            "has_music":null,
            "has_paid_parking_directly_outside_of_clinic":null,
            "has_paid_parking_near_the_clinic":null,
            "has_restroom":null,
            "has_toys":null,
            "has_tv":null,
            "has_waiting_room":null,
            "has_wifi":null,
            "number_of_reviews":0,
            "overall_rating":0,
            "info_rating_advice_and_tips":0,
            "info_rating_follow_up":0,
            "info_rating_how_to_find_place":0,
            "info_rating_patient_health":0,
            "info_rating_patient_treatment":0,
            "info_rating_pre_meeting":0,
            "info_rating_pricing":0,
            "rating_quality":0,
            "rating_bedside_manner":0,
            "rating_hygiene":0,
            "rating_reception_on_arrival":0,
            "rating_thoroughness":0,
            "rating_wait_time":0
         },
         "relationships":{
            "default_clinic_image":{
               "data":null
            }
         }
      }
   ],
   "meta":{
      "pagination":{
         "total":1,
         "count":1,
         "per_page":12,
         "current_page":1,
         "total_pages":1
      }
   },
   "links":{
      "self":"https:\/\/journalapitest.prodentor.se\/api\/muntra-bookings?page=1",
      "first":"https:\/\/journalapitest.prodentor.se\/api\/muntra-bookings?page=1",
      "last":"https:\/\/journalapitest.prodentor.se\/api\/muntra-bookings?page=1"
   }
}
```
