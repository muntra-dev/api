## Supported HTTP Methods
| Method | URL | Query Parameters |
| ------ | --- | ---------------- |
| GET | /journal-entries | check_exceeds_page, deleted, include, order, patient_id, per_page, sort_by, status, teeth, type |

## Properties
| Name | Info | Type |
| ---- | ---- | ---- |
| deleted |  | boolean |
| discount_excluding_vat |  | number |
| draft |  | boolean |
| editable |  | boolean |
| entry_date |  | isodate |
| entry_type |  | string |
| fee |  | number |
| imported |  | boolean |
| included_in_insurance |  | boolean |
| lab_fee |  | number |
| price_code |  | number |
| price_text |  | string |
| referral |  | boolean |
| signed_at |  | isodate |
| text |  | string |


## Relations
| Name | Cardinality | Data Model |
| ---- | ----------- | ---------- |
| claim_row | belongsTo | claim-row |
| clinic | belongsTo | clinic |
| county_council_price | belongsTo | county-council-price |
| currency | belongsTo | currency |
| elements | hasMany | element |
| files | hasMany | file |
| history | belongsTo | history |
| journal_diagnosis | belongsTo | journal-diagnosis |
| journal_validation | belongsTo | journal-validation |
| patient | belongsTo | patient |
| patient_invoice_row | belongsTo | patient-invoice-row |
| position_elements | hasMany | element |
| prescription | belongsTo | prescription |
| price | belongsTo | price |
| received_remittance | belongsTo | received-remittance |
reimbursement_type | belongsTo | reimbursement-type |
| remittance | belongsTo | remittance |
| remittance_response | belongsTo | remittance-response |
| sent_remittance | belongsTo | remittance |
| signer | belongsTo | user |
| teeth | hasMany | tooth |
| treatment | belongsTo | treatment |
| treatment_plan_item | belongsTo | treatment-plan-item |
| unsigner | belongsTo | user |
| user | belongsTo | user |
| vat_code | belongsTo | vat-code |
| verification | belongsTo | verification |

## Samples
### GET Request
#### URL
```
/api/journal-entries?check_exceeds_page=1&deleted=false&include=claim_row.claims%2Cclinic%2Ccounty_council_price%2Ccurrency%2Celements%2Chistory%2Cjournal_diagnosis%2Cpatient%2Cpatient_invoice_row.patient_invoices%2Cprice.state_price%2Creceived_remittance%2Creimbursement_type%2Csent_remittance%2Csigner%2Cteeth%2Ctreatment%2Cuser%2Cvat_code&order=desc&patient_id=462&per_page=50&sort_by=entry_date&status=to-handle&teeth=&type=
```
#### Response Payload
```
{"data":[{"type":"journal_entry","id":"9298","attributes":{"entry_date":"2022-06-15T18:49:16+02:00","text":"Basunders\u00f6knin m labbkost.","referral":false,"fee":900,"lab_fee":15,"discount_excluding_vat":0,"entry_type":"treatment","included_in_insurance":false,"draft":false,"imported":false,"editable":false,"deleted":false,"signed_at":"2022-06-17T05:30:50+02:00"},"relationships":{"clinic":{"data":{"type":"clinic","id":"2"}},"patient":{"data":{"type":"patient","id":"462"}},"user":{"data":{"type":"user","id":"4"}},"history":{"data":null},"treatment":{"data":{"type":"treatment","id":"1"}},"reimbursement_type":{"data":{"type":"reimbursement_type","id":"5"}},"price":{"data":{"type":"price","id":"11022"}},"county_council_price":{"data":null},"currency":{"data":{"type":"currency","id":"1"}},"vat_code":{"data":{"type":"vat_code","id":"5"}},"journal_diagnosis":{"data":null},"teeth":{"data":[]},"elements":{"data":[{"type":"element","id":"NA"}]},"patient_invoice_row":{"data":null},"claim_row":{"data":null},"signer":{"data":{"type":"user","id":"4"}},"received_remittance":{"data":null},"sent_remittance":{"data":null}}}],"included":[{"type":"payer_type","id":"8","attributes":{"name":"patient","object_model":"patient","object_property":"id"}},{"type":"payer_type","id":"9","attributes":{"name":"state","object_model":"state","object_property":"id"}},{"type":"clinic","id":"2","attributes":{"clinic_name":"Muntra, test","clinic_address_1":"Katarinav\u00e4gen 15 ","clinic_address_2":"C\/O Epicenter","clinic_postal_code":"11645","clinic_city":"Stockholm","clinic_reference":null,"clinic_email_address":"a.haseeb19@gmail.com","clinic_phone_number":"+4632240541","clinic_phone_number_2":"+46734100450","clinic_phone_mobile":"+46734100450","clinic_fax":"","clinic_professional_statement":"Specialistklinik fokuserad p\u00e5 estetiska behandlingar. Tandl\u00e4kare med specialistexamen.  Ny rad.","workplace_code":"4000000000000","website_address":"https:\/\/www.muntra.se","booking_requires_two_factor_authentication":false,"active":true,"timezone":"Europe\/Stockholm","latitude":59.339073,"longitude":17.965555,"google_places_description":"Frans Kriegs V\u00e4g 16, Bromma, Sverige","journal_entry_autosign_limit_in_days":1,"journal_entry_unsign_limit_in_days":30,"default_sms_invitation_text":"Hej [patient_first_name]! V\u00e4lkommen [booking_daydatetime] till [clinic_address_1]. Bekr\u00e4fta tiden via [booking_confirmation_link]","default_sms_reminder_text":"P\u00c5MINNELSE: Hej [patient_first_name]! Nu \u00e4r det dags att bes\u00f6ka oss. V\u00e4lkommen till [clinic_name] p\u00e5 [clinic_address_1] kl. [booking_time] den [booking_date]. Mvh, [caregiver_first_name] [caregiver_last_name], [caregiver_title]","default_snail_mail_invitation_text":"Hej [patient_first_name]!\r\n\r\n\r\n\r\nNu \u00e4r det dags att bes\u00f6ka oss.\r\n\r\nV\u00e4lkommen till [clinic_name] p\u00e5 [clinic_address_1] kl. [booking_time] den [booking_date].\r\n\r\nBekr\u00e4fta g\u00e4rna tiden genom att g\u00e5 till f\u00f6ljande l\u00e4nk: [booking_confirmation_link]\r\n\r\nMed v\u00e4nlig h\u00e4lsning,\r\n[caregiver_first_name] [caregiver_last_name], [caregiver_title]","default_hours_until_sms_invitation_sent":72,"default_hours_before_sms_reminder_sent":48,"default_hours_until_snail_mail_invitation_sent":168,"allow_remittance_without_individual_recipient":true,"accepts_digital_remittance":true,"has_cbct":true,"created_at":"2017-09-11T15:30:22+02:00","updated_at":"2022-08-16T09:02:48+02:00"}},{"type":"patient","id":"462","attributes":{"social_security_number":"198912241224","first_name":"Test","last_name":"Testsson","maiden_name":null,"initials":null,"gender":null,"address_1":null,"address_2":null,"city":null,"postal_code":null,"municipality":null,"date_of_birth":null,"passport_number":null,"phone_number_cell":"+46708123123","phone_number_home":null,"phone_number_work":null,"fax_number":null,"e_mail_address":"test123@test.com","deleted":false,"created_at":"2022-05-24T16:02:13+02:00","updated_at":"2022-08-22T19:23:23+02:00","patient_number":"462","invoice_reference":null,"status":"active","wants_anestesia":false,"start_date_free_card":null,"end_date_free_card":null,"free_card_number":null,"county_council_certificate_number":null,"county_council_certificate_end_date":null,"euro_certificate_number":null,"protected_identity":false,"warning":false,"warning_text":null,"xray_id":null,"notes":null,"external_dentist":null,"external_hygienist":null,"auto_include_email_invitation":null,"auto_include_sms_invitation":null,"auto_include_sms_reminder":null,"auto_include_snail_mail_invitation":null,"prefers_not_to_be_contacted_by_clinic":false,"recurring":false,"referral_source":"localhost","teeth_count":null,"untreated_teeth_count":null,"signed_at":null}},{"type":"user","id":"4","attributes":{"social_security_number":"198108111496","first_name":"Niels","last_name":"Rask","maiden_name":"","initials":"NR","gender":"male","address_1":"Hejgatan 4","address_2":"","city":"Bromma","postal_code":"16733","municipality":"Bromma kommun","date_of_birth":"1981-08-18T00:00:00+02:00","passport_number":"","phone_number_cell":"+46734100450","phone_number_home":"+46840906890","phone_number_work":"+46840906890","fax_number":"","e_mail_address":"niels@muntra.se","deleted":null,"created_at":"2017-09-11T15:28:20+02:00","updated_at":"2022-06-15T16:26:37+02:00","active":true,"prescriber_code":"9001","professional_statement":"Tandl\u00e4kare med specialistexamen. Tandl\u00e4kare med specialistexamen. Tandl\u00e4kare med specialistexamen. Tandl\u00e4kare med specialistexamen. Tandl\u00e4kare med specialistexamen. Tandl\u00e4kare med specialistexamen. Tandl\u00e4kare med specialistexamen. Tandl\u00e4kare med specialistexamen. \r\nNy rad.","title":"Specialisttandl\u00e4kare Ortodonti, Odont. Dr.","hide_reviews":false,"hide_reviews_discreetly":false,"number_of_reviews":21,"overall_rating":4.38}},{"type":"treatment","id":"1","attributes":{"text":"Unders\u00f6kning","selectable":"mouth,tooth","crown_background_color":null,"crown_border_color":null,"root_background_color":null,"root_border_color":null,"clear_history":false,"surface_text":null,"surface_text_color":null,"tooth_status":null}},{"type":"reimbursement_type","id":"5","attributes":{"name":"HELFO","active":true},"relationships":{"payer_types":{"data":[{"type":"payer_type","id":"8"},{"type":"payer_type","id":"9"}]},"reimbursement_rules":{"data":[]}}},{"type":"price","id":"11022","attributes":{"price_code":"101","description":"Basunders\u00f6knin m labbkost.","total_excluding_vat":900,"lab_fee":15,"included_material":"test","multi_tooth":false,"class":"","deleted":false},"relationships":{"state_price":{"data":null}}},{"type":"currency","id":"1","attributes":{"code":"SEK","name":"Svenska kroner","suffix":"kr"}},{"type":"vat_code","id":"5","attributes":{"name":"6%","vat_percentage":0.06}},{"type":"element","id":"NA","attributes":{"surface":"","selectable":"mouth","tooth":"NA"}}],"meta":{"pagination":{"count":1,"per_page":50,"current_page":1,"total_pages_exceed":0}},"links":[]}
```
