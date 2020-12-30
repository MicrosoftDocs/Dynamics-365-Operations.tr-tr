---
title: Finance ile tümleştirmeyi yapılandırma
description: Bu makalede, Dynamics 365 Human Resources'tan Dynamics 365 Finance'e tümleştirme için kullanılabilecek işlevler açıklanmaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b4d6369ab567879e23e1f132265aaff45c8ce47
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527939"
---
# <a name="configure-integration-with-finance"></a>Finance ile tümleştirmeyi yapılandırma

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resources İle Dynamics 365 Finance'i birleştirmek için, [veri tümleştirici](https://docs.microsoft.com/powerapps/administrator/data-integrator) alanındaki insan kaynakları finans şablonunu kullanabilirsiniz. Finans şablonuna İnsan Kaynakları işler, pozisyonlar ve çalışanlar için veri akışını etkinleştirir. Şablon verilerin İnsan Kaynakları'nden finansa akmasını sağlar, ancak verilerin finans'tan İnsan Kaynakları akamasına izin vermez.

![Human Resources'tan Finance'e Tümleştirme Akışı](./media/hr-admin-integration-finance-flow.png)

Human Resources'tan Finance'e çözümü aşağıdaki veri eşitleme türlerini sağlar:

- Human Resources'taki işleri koruyun ve Human Resources'tan Finance'e eşitleyin
- Human Resources'taki pozisyonları ve pozisyon atamalarını koruyun ve Human Resources'tan Finance'e eşitleyin
- Human Resources'taki istihdamları koruyun ve Human Resources'tan Finance'e eşitleyin
- Human Resources'taki çalışanları ve çalışan adreslerini koruyun ve Human Resources'tan Finance'e eşitleyin

## <a name="system-requirements-for-human-resources"></a>Human Resources için sistem gereksinimleri

Tümleştirme çözümü için aşağıdaki Human Resources ve Finance sürümleri gereklidir: 

- Common Data Service üzerinde Dynamics 365 Human Resources
- Dynamics 365 Finance 7.2 veya daha ileri bir sürüm

## <a name="template-and-tasks"></a>Şablon ve görevler

İnsan Kaynakları finans şablonuna erişmek için.

1. [Power Apps Yönetim Merkezi](https://admin.powerapps.com/)'ni açın. 

2. **Projeleri** seçin ve sonra sağ üst köşedeki **Yeni proje** 'yi seçin. Finance'e tümleştirmek istediğiniz her tüzel kişilik için yeni bir proje oluşturun.

3. Kayıtları **İnsan Kaynakları (insan kaynakları Common Data Service ile finans)** ile eşitlemek için insan kaynakları (Finans için) öğesini seçin.

Şablon, Human Resources'tan kayıtları Finance'e eşitlemek için aşağıdaki temel görevler kullanır.

- **İş İşlevleri'nden Maaş İş İşlevi'ne**
- **Departmanlar'dan Faaliyet Birimi'ne**
- **İş Türleri'nden Maaş İş Türü'ne**
- **İşler'den İşler'e**
- **İşler'den İş Ayrıntısı'na**
- **Pozisyon Türleri'nden Pozisyon Türü'ne**
- **İş Pozisyonları'ndan Temel Pozisyon'a**
- **İş Pozisyonları'ndan Pozisyon Ayrıntıları'na**
- **İş Pozisyonları'ndan Pozisyon Süreleri'ne**
- **İş Pozisyonları'ndan Pozisyon Hiyerarşileri'ne**
- **Çalışanlar'dan Çalışan'a**
- **İstihdamlar'dan İstihdam'a**
- **İstihdamlar'dan İstihdam Ayrıntısı'na**
- **Pozisyon Çalışan Ataması'ndan Pozisyon Çalışan Atamaları'na**
- **Çalışan Adresleri'nden Çalışan Posta Adresi V2'ye**

## <a name="template-mappings"></a>Şablon eşlemeleri

Aşağıdaki şablon eşleme tablolarında, görevin adı her bir uygulamada kullanılan varlıkları içerir. Kaynak (Human Resources) solda, hedef (Finans) sağdadır.

### <a name="job-functions-to-compensation-job-function"></a>İş İşlevleri'nden Maaş İş İşlevi'ne

| Common Data Service varlığı (kaynak) | Fİnans varlığı (hedef) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   İşlev Adı)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Departmanlar'dan Faaliyet Birimi'ne

| Common Data Service varlığı (kaynak)           | Fİnans varlığı (hedef) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NAME)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>İş Türleri'nden Maaş İş Türü'ne

| Common Data Service varlığı (kaynak)   | Fİnans varlığı (hedef) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (DESCRIPTION)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>İşler'den İşler'e

| Common Data Service varlığı (kaynak)                           | Fİnans varlığı (hedef)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (DESCRIPTION)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>İşler'den İş Ayrıntısı'na

| Common Data Service varlığı (kaynak)                             | Fİnans varlığı (hedef) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (İş Türü (İş Türü Adı))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (İş İşlevi (İş İşlevi Adı)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Geçerlilik Başlangıcı)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Geçerlilik Sonu)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Varsayılan Tam Zamanlı Eşdeğeri)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Pozisyon Türleri'nden Pozisyon Türü'ne

| Common Data Service varlığı (kaynak)       | Fİnans varlığı (hedef) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>İş Pozisyonları'ndan Temel Pozisyon'a

| Common Data Service varlığı (kaynak)           | Fİnans varlığı (hedef) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (İş Pozisyonu Numarası) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>İş Pozisyonları'ndan Pozisyon Ayrıntıları'na

| Common Data Service varlığı (kaynak)              | Fİnans varlığı (hedef)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber   (İş Pozisyonu Numarası)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (İş Adı)                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (Departman (Departman Numarası)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Pozisyon Türü (Ad))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Atama için Kullanılabilir)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (Geçerlilik Başlangıcı)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (Geçerlilik Sonu)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Tam Zamanlı Eşdeğeri)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>İş Pozisyonları'ndan Pozisyon Süreleri'ne

| Common Data Service varlığı (kaynak)             | Fİnans varlığı (hedef) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (İş Pozisyonu Numarası)   | POSITIONID (POSITIONID)                      |
| Hesaplanan   Etkinleştirme (Hesaplanan Etkinleştirme) | VALIDFROM (VALIDFROM)                        |
| Hesaplanan   Emeklilik (Hesaplanan Emeklilik) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>İş Pozisyonları'ndan Pozisyon Hiyerarşileri'ne

| Common Data Service varlığı (kaynak)        | Fİnans varlığı (hedef) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (İş Pozisyonu Numarası)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (Geçerlilik Başlangıcı)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Geçerlilik Sonu)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Çalışanlar'dan Çalışan'a
| Common Data Service varlığı (kaynak)           | Fİnans varlığı (hedef)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (GENDER)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>İstihdamlar'dan İstihdam'a

| Common Data Service varlığı (kaynak)                             | Fİnans varlığı (hedef) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>İstihdamlar'dan İstihdam Ayrıntısı'na

| Common Data Service varlığı (kaynak)                             | Fİnans varlığı (hedef)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (Geçerlilik Başlangıcı)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Geçerlilik Sonu)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Pozisyon Çalışan Ataması'ndan Pozisyon Çalışan Atamaları'na

| Common Data Service varlığı (kaynak)                             | Fİnans varlığı (hedef)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (İş Pozisyonu Numarası)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (Geçerlilik Başlangıcı)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (Geçerlilik Sonu)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Çalışan Adresleri'nden Çalışan Posta Adresi V2'ye

| Common Data Service varlığı (kaynak)                             | Fİnans varlığı (hedef)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Tümleştirmeyle ilgili değerlendirmeler

Human Resources'tan Finance'e tümleştirme, kayıtları kodlarına göre eşlemeye çalışır. Kayıtlar eşleşirse Veri Tümleştirici, Human Resources'taki değerler Finance'teki verilerin üzerine yazılır. Ancak, bunlar mantıksal olarak farklı kayıtlar olduğu halde Human Resources'ta veya Finance'te ilgili numara serisine aynı kod üretildiyse bir sorun oluşabilir.

Sorun, eşlemeyi yapmak için **Personel numarası** kullanılan **Çalışan** ve **Pozisyonlar**'da oluşabilir. İşler numara serileri kullanmaz. Sonuç olarak, hem Human Resources'ta hem de Finance'te aynı iş kodu mevcutsa, Human Resources bilgileri Dynamics 365 Finance bilgilerinin üzerine yazılır. 

Yinelenen kodlarla ilgili sorunları önlemek için [numara serisine](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json)bir önek ekleyebilir veya numara serisinde, diğer sistemin aralığının dışında bir başlangıç numarası ayarlayabilirsiniz. 

Çalışan adresi için kullanılan konum kodu, bir numara serisinin parçası değildir. Human Resources'tan bir çalışan adresi Finance'e tümleştirilirken, çalışan adresi Finance'te zaten varsa yinelenen bir adres kaydı oluşturulabilir. 

Aşağıdaki çizim, Veri Tümleştirici'de bir şablon eşleme örneği gösteriyor. 

![Şablon Eşleme](./media/IntegrationMapping.png)