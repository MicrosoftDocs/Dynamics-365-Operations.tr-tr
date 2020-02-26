## <a name="cds-contacts-v2-to-contacts"></a>CDS İlgili Kişileri V2 ve contacts

Bu şablon, Finance and Operations uygulamaları ve Common Data Service arasında verileri eşitler.

Kaynak filtresi: (AssociatedContactType = 1)

Ters kaynak filtresi: msdyn_contactforvendor eq doğru ve msdyn_sellable eq yanlış ve msdyn_contactpersonid ne ''

Finance and Operations alanı | Eşleme türü | Diğer Dynamics 365 alanı | Varsayılan değer
---|---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn_partynumber | 
ASSOCIATEDCONTACTTYPE | << | hiçbiri | Satıcı
FIRSTNAME | = | firstname | 
MIDDLENAME | = | middlename | 
LASTNAME | = | lastname | 
ASSOCIATEDCONTACTNUMBER | = | msdyn_vendorcontactid.msdyn_vendoraccountnumber | 
PRIMARYADDRESSCITY | = | address1_city | 
PRIMARYADDRESSCOUNTRYREGIONID | = | address1_country | 
PRIMARYADDRESSCOUNTYID | = | address1_county | 
PRIMARYFAXNUMBER | = | fax | 
PRIMARYADDRESSSTATEID | = | address1_stateorprovince | 
PRIMARYADDRESSSTREET | = | address1_line1 | 
PRIMARYADDRESSZIPCODE | = | address1_postalcode | 
PRIMARYPHONENUMBER | = | telephone1 | 
PRIMARYEMAILADDRESS | = | emailaddress1 | 
EMPLOYMENTDEPARTMENT | = | departman | 
NOTES | = | description | 
GENDER | >< | gendercode | 
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid | 
PRIMARYURL | = | websiteurl | 
MARITALSTATUS | >< | familystatuscode | 
ISRECEIVINGDIRECTMAIL | >< | donotemail | 
EMPLOYMENTPROFESSION | = | jobtitle | 
SPOUSENAME | = | spousesname | 
hiçbiri | >> | msdyn_contactforvendor | Doğru
CONTACTPERSONID | = | msdyn_contactpersonid | 
