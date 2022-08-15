## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /remittances | TBD |

## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| closed_at |  | isodate |
| confirmed_receipt_at |  | isodate |
consultation |  | boolean |
| created_at |  | isodate |
| declined_at |  | isodate |
| desired_treatment |  | string |
| due_date |  | isodate |
| keep_patient_informed |  | boolean |
| patient_address_1 |  | string |
| patient_address_2 |  | string |
| patient_city |  | string |
| patient_date_of_birth |  | isodate |
| patient_e_mail_address |  | string |
| patient_first_name |  | string |
| patient_gender |  | string |
| patient_last_name |  | string |
| patient_municipality |  | string |
| patient_phone_number_cell |  | string |
| patient_phone_number_home |  | string |
| patient_phone_number_work |  | string |
| patient_postal_code |  | number |
| patient_social_security_number |  | string |
| printed_at |  | isodate |
| receiver_clinic_address_1 |  | string |
| receiver_clinic_address_2 |  | string |
| receiver_clinic_city |  | string |
| receiver_clinic_email_address |  | string |
| receiver_clinic_name |  | string |
| receiver_clinic_phone_number |  | string |
| receiver_clinic_postal_code |  | string |
| receiver_first_view_at |  | isodate |
| receiver_user_email_address |  | string |
| receiver_user_first_name |  | string |
| receiver_user_last_name |  | string |
| receiver_user_phone_number |  | string |
| receiver_user_signed_at |  | isodate |
| receiver_user_social_security_number |  | string |
| remittance_background |  | string |
| remittance_comment |  | string |
| remittance_question |  | string |
| remittance_response |  | string |
| sender_clinic_address_1 |  | string |
| sender_clinic_address_2 |  | string |
| sender_clinic_city |  | string |
| sender_clinic_email_address |  | string |
| sender_clinic_name |  | string |
| sender_clinic_phone_number |  | string |
| sender_clinic_postal_code |  | string |
| sender_user_email_address |  | string |
| sender_user_first_name |  | string |
| sender_user_last_name |  | string |
| sender_user_phone_number |  | string |
| sender_user_social_security_number |  | string |
| signed_at |  | isodate |
| updated_at |  | isodate |
| urgent |  | boolean |


## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| journal_entry | belongsTo | journal-entry |
| patient | belongsTo | [patient](../../../Patient/Endpoints/patients/) |
| receiver_clinic | belongsTo | clinic |
| receiver_creation_signer | belongsTo | user |
| receiver_files | hasMany | file |
| receiver_signer | belongsTo | user |
| receiver_user | belongsTo | user |
| remittance_emails | hasMany | remittance-email |
| remittance_responses | hasMany | remittance-response |
| sender_clinic | belongsTo | clinic |
| sender_files | hasMany | file |
| sender_journal_entry | belongsTo | journal-entry |
| sender_signer | belongsTo | user |
| sender_user | belongsTo | user |
| snail_mails | hasMany | snail-mail |
| wanted_receiver_user | belongsTo | user |

## Samples
### GET Request
#### URL
```
```
#### Response Payload
```
```
