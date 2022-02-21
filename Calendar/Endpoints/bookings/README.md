## Properties
| ------------- | ------------- | ------------- |
| class | "PUBLIC" / "PRIVATE" / "CONFIDENTIAL". PUBLIC is default. | string |
| description |  | string |
| done |  | boolean |
| dtend |  | isodate |
| dtstamp |  | isodate |
| dtstart |  | isodate |
| duration_in_minutes |  | number |
| location |  | string |
| new_patient |  | boolean |
| patient_declaration_allowed |  | boolean |
| patient_failed_to_appear |  | boolean |
| patient_failed_to_appear_handled |  | boolean |
| patient_made_late_cancellation |  | boolean |
| patient_wants_earlier_slot |  | boolean |
| price |  | number |
| reschedulable |  | boolean |
| status |  | string |
| summary |  | string |
| text |  | string |
| transparent |  | boolean |

## Relations
| ------------- | ------------- | ------------- |
| booking_attendees |hasMany| booking-attendee |
| booking_exdates | hasMany | booking-exdate |
| booking_rrules | hasMany | booking-rrule |
| booking_type | belongsTo | booking-type |
| change_logs | hasMany | change-log |
| clinic | belongsTo | clinic |
| events | hasMany | event |
| organizer | belongsTo | user |
| procedure | belongsTo | procedure |
| promo_code | belongsTo | promo-code |
| rebooking | belongsTo | rebooking |
