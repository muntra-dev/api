## Supported HTTP Methods

| Method | URL                       | Query Parameters |
| ------ | ------------------------- | ---------------- |
| POST   | /muntra-booking-attendees |                  |

## Attributes

| Name     | Info | Type    |
| -------- | ---- | ------- |
| partstat |      | string  |
| rsvp     |      | boolean |

## Relations

| Name    | Cardinality | Data Model        |
| ------- | ----------- | ----------------- |
| booking | belongsTo   | muntra-bookings   |
| patient | belongsTo   | muntra_patient    |
| user    | belongsTo   | muntra-caregivers |

## Samples

### Post Request

#### URL

```
/api/muntra-booking-attendees
```

#### Response Payload

```
{
   "data":{
      "type":"muntra_booking_attendee",
      "id":"BAx4d8mq8sa0",
      "attributes":{
         "partstat":"ACCEPTED",
         "rsvp":false
      }
   }
}
```
