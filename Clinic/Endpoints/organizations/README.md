## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /organizations/current |  |


## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| cert_exists |  | boolean |
| created_at |  | isodate |
| iban |  | string |
| invoice_account_number |  | string |
| invoice_address_1 |  | string |
| invoice_address_2 |  | string |
| invoice_bankgiro |  | string |
| invoice_city |  | string |
| invoice_clearing_number |  | string |
| invoice_country_code |  | string |
| invoice_email_address |  | string |
| invoice_fax |  | string |
| invoice_phone_mobile |  | string |
| invoice_phone_number |  | string |
| invoice_phone_number_2 |  | string |
| invoice_plusgiro |  | string |
| invoice_postal_code |  | string |
| invoice_reference |  | string |
| invoice_swish_number |  | string |
| organization_name |  | string |
| organization_number |  | string |
| type |  | string |
| updated_at |  | isodate |


## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| additional_owners | hasMany | user |
| bookkeeping_locks | hasMany | bookkeeping-lock |
| claims | hasMany | validate-claim |
| certificate | belongsTo | certificate |
| clinics | hasMany | clinic |
| contact_person | belongsTo | user |
| cost_centers | hasMany | cost-center |
| country | belongsTo | country |
| credit_checks | hasMany | credit-check |
| default_fiscal_year | belongsTo | fiscal-year |
| fiscal_years | hasMany | fiscal-year |
| invoice_payment_standard_option | belongsTo | payment-type |
| orders | hasMany | order |
| organization_clinic_settings | hasMany | organization-clinic-setting |
| patient_invoices | hasMany | patient-invoice |
| permission_policies | hasMany | permission-policy |
| supplier_settings_for_organizations | hasMany | supplier-settings-for-organization |
| user | belongsTo | user |
| users_at_clinic_defaults_with_default_organization | hasMany | user-at-clinic-defaults |
| users_at_clinic_defaults_with_organization_authorized_for_invoicing | hasMany | user-at-clinic-defaults |
| users_at_clinic_with_organization_authorized_for_invoicing | hasMany | user-at-clinic |
| users_at_clinic_with_default_organization | hasMany | user-at-clinic |
| verification_series | hasMany | verification-serie |


## Samples
### GET Request
#### URL
```
/api/organizations/current
```
#### Response Payload
```
{
  "data": {
    "type": "organization",
    "id": "2",
    "attributes": {
      "organization_number": "556935-2726",
      "organization_name": "Muntra AB",
      "invoice_address_1": "Mäster Samuelsgatan 36 (org)",
      "invoice_address_2": "",
      "invoice_postal_code": "11111",
      "invoice_city": "Bromma",
      "invoice_email_address": "niels@muntraorganisation.se",
      "invoice_phone_number": "",
      "invoice_phone_number_2": "",
      "invoice_phone_mobile": "+46734100450",
      "invoice_fax": "",
      "created_at": "2017-09-11T15:30:22+02:00",
      "updated_at": "2022-05-10T17:05:14+02:00",
      "invoice_reference": "",
      "invoice_country_code": "SE",
      "invoice_plusgiro": "",
      "invoice_bankgiro": "123-41233",
      "invoice_account_number": "",
      "invoice_clearing_number": "8264-4",
      "invoice_swish_number": "1230955831",
      "iban": "0680000832796936995288",
      "type": "individual",
      "cert_exists": true
    },
    "relationships": {
      "user": {
        "data": {
          "type": "user",
          "id": "4"
        }
      },
      "contact_person": {
        "data": {
          "type": "user",
          "id": "4"
        }
      },
      "invoice_payment_standard_option": {
        "data": {
          "type": "payment_type",
          "id": "1"
        }
      },
      "payment_types": {
        "data": []
      },
      "default_fiscal_year": {
        "data": {
          "type": "fiscal_year",
          "id": "732"
        }
      }
    }
  },
  "included": [
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
      "type": "payment_type",
      "id": "1",
      "attributes": {
        "name": "bankgiro",
        "label": "Bankgiro"
      }
    },
    {
      "type": "fiscal_year",
      "id": "732",
      "attributes": {
        "start_date": "2020-01-01T00:00:00+01:00",
        "end_date": "2020-12-31T00:00:00+01:00",
        "cash_accounting_method": false,
        "book_outstanding_treatments": true
      }
    }
  ]
}```
