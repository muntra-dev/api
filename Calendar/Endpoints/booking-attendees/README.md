## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /booking-attendees |  |


## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| arrived_at | `null` if the patient hasn't arrived yet | isodate |
| dtend |  | isodate |
| dtstart |  | isodate |
| first_sendout_on |  | isodate |
| partstat | Can be 'TENTATIVE', 'ACCEPTED', 'DECLINED', 'NEEDS-ACTION' (this last one is default). | string |
| rsvp | Used to specify whether there is an expectation of reply from the calendar user specified by the property value. | boolean |


## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| booking | belongsTo | booking |
| booking_attendee_external_binding | belongsTo | booking-attendee-external-binding |
| declaration_emails | hasMany | declaration-email |
| declaration_sms | hasMany | declaration-sms |
| email_ics | hasMany | email-ics |
| patient | belongsTo | patient |
| resource | belongsTo | resource |
| room | belongsTo | room |
| sms_invitations | hasMany | sms-invitation |
| sms_reminders | hasMany | sms-reminder |
| snail_mails | hasMany | snail-mail |
| user | belongsTo | user |


## Sample JSON Payload
```

```
