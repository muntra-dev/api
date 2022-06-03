## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /muntra-bookings | order |
|  | | per_page |
|  | | sort_by |
|  | | status |
|  | | from_date |
|  | | include |

## Properties
| Name | Info | Type |
| ------------- | ------------- | ------------- |
| booked_by_patient |  | boolean |
| class |  | string |
| description |  | string |
| dtend |  | isodatae |
| dtstamp |  | isodatae |
| dtstart |  | isodatae |
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

## Sample JSON Payload
```
include: booking_attendees.patient,booking_attendees.user.default_user_image,booking_attendees.user.role,clinic.default_clinic_image
order: asc
per_page: 12
sort_by: dtstart
status: CONFIRMED,TENTATIVE
from_date: 2022-06-03T09:46:10+02:00
```
