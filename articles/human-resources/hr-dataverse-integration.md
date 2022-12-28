---
title: Dataverse tabloları ile tümleştirmeyi yapılandırma
description: Bu makalede, Microsoft Dynamics 365 Human Resources ve Dataverse arasındaki tümleştirme açıklanmaktadır.
author: anschmidt
ms.date: 12/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63c25020b7026a76ecc6e2c3563f8299627ec8a8
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838635"
---
# <a name="configure-integration-with-dataverse-tables"></a>Dataverse tabloları ile tümleştirmeyi yapılandırma

>[!Important]
>Bu makalede belirtilen işlevler şu anda Finans ve Operasyonlar altyapısında Dynamics 365 Human Resources müşterileri için kullanıma sunulmaktadır. 


Microsoft Dynamics 365 Human Resourcesile Dataverse'ü tümleşik hale getirmek için [Veri Entegratörü](/powerapps/administrator/data-integrator) kullanabilirsiniz. HumanResources-to- Dataverse şablonu, projelerin, pozisyonların, çalışanların ve diğer kişilerin verilerini Human Resources'tan Dataverse'e, ve Dataverse'ten Human Resources'a veri akışına olanak tanır, her iki sistemde de yazı oluşturur.

## <a name="system-requirements-for-human-resources"></a>Human Resources için sistem gereksinimleri

Tümleştirme çözümü için aşağıdaki Human Resources ve Dynamics 365 Finance sürümleri gereklidir: 

- Dynamics 365 Finance sürüm 7.2 ve sonrası
- Dynamics CRM, bir veritabanının oluşturulduğu ve Dynamics 365 uygulamalarına izin verilen ortam

## <a name="template-and-tasks"></a>Şablon ve görevler

Human Resources–to–Finance şablonuna erişim için bu adımları izleyin.

1. [Power Apps yönetim merkezi](https://admin.powerapps.com/)'ni açın. 
2. Ortamınızın altında, **Dynamics 365 Uygulamaları**'nı seçin ve araç çubuğunda **Uygulama kaynağı**'nı seçin.
3. Şablonu yüklemek için, "Çift Yazma Human Resources" arayın veya doğrudan aşağıdaki adrese gidin: <https://appsource.microsoft.com/product/dynamics-365/mscrm.hcm_dualwrite>.
3. Yükleme tamamlandıktan sonra, Dynamics 365 Finance'i açın.
4. **Veri Yönetimi** çalışma alanını açın. 
5. **Çift Yazma** seçin. 
6. Ortamınızdaki en az bir şirket için ortamınızı bağlama sürecini takip edin. 
7. Dataverse ortamınıza bir bağlantı ayarlamayı bitirdiğinizde **Çözüm Uygula**'yı seçin. Çözüm uygulanır ve eşlemeler entegratör uygulamasına yüklenir.

## <a name="template-mappings"></a>Şablon eşlemeleri

Aşağıdaki şablon eşleme tablolarında, görevin adı her bir uygulamada kullanılan varlıkları gösterir. Finans solda ve Dataverse sağda.

### <a name="bank-account-disbursements-dual-write-to-bank-account-disbursement"></a>Bank hesabı tahsilatlarından (Çift yazma) Bank Hesabı Tahsilata

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATIONID        | cdm\_bankaccountid.cdm\_accountidentification        |
| TUTAR                         | cdm\_amount                                         |
| ÖNCELİK                       | cdm\_disbursementpriority                           |
| PERSONELNUMARASI                | cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber    |
| BAKİYE                      | cdm\_isremainder                                    |

### <a name="benefit-calculation-rate-detail-dual-write-to-benefit-calculation-rate-detail"></a>Kazanç hesaplama oranı ayrıntısından (Çift-yazma) Kazanç Hesaplama Oranı Ayrıntısına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| CONTRIBUTIONMETHOD             | cdm\_contributionmethod                             |
| ETKİLİ                      | cdm\_effective                                      |
| EMPLOYERCONTRIBUTION           | cdm\_employercontribution                           |
| BİTİŞ TARİHİ                     | cdm\_expiration                                     |
| WORKERDEDUCTION                | cdm\_workerdeduction                                |
| AD                           | cdm\_calculationrateid.cdm\_name                     |

### <a name="benefit-calculation-rate-header-to-benefit-calculation-rate"></a>Kazanç Hesaplama Oranına kazanç hesaplama oranı üst bilgisi

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| AD                           | cdm\_name                                           |
| TIERTYPE                       | cdm\_tiertype                                       |

### <a name="benefit-option-to-benefit-option"></a>Kazan seçeneğinden Kazanç Seçeneğine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| ALLOWBENEFICIARYDESIGNATIONS   | cdm\_allowbeneficiarydesignations                   |
| ALLOWDEPENDENTCOVERAGE         | cdm\_allowdependentcoverage                         |
| BENEFITOPTIONID                | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| ISWAIVE                        | cdm\_iswaived                                       |

### <a name="benefit-type-to-benefit-type"></a>Kazanç türünden Kazanç Türüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| BENEFITTYPEID                  | cdm\_name                                           |
| CONCURRENTENROLLMENT           | cdm\_concurrentenrollment                           |
| AÇIKLAMA                    | cdm\_description                                    |
| PAYROLLCATEGORY                | cdm\_payrollcategory                                |

### <a name="business-calendar-to-business-process-calendar"></a>İş takviminden İş İşlem Takvimine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| AD                           | cdm\_calendarname                                   |
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| ISOPENMONDAY                   | cdm\_ismondayopen                                   |
| ISOPENTUESDAY                  | cdm\_istuesdayopen                                  |
| ISOPENWEDNESDAY                | cdm\_iswednesdayopen                                |
| ISOPENTHURSDAY                 | cdm\_isthursdayopen                                 |
| ISOPENFRIDAY                   | cdm\_isfridayopen                                   |
| ISOPENSATURDAY                 | cdm\_issaturdayopen                                 |
| ISOPENSUNDAY                   | cdm\_issundayopen                                   |

### <a name="business-process-to-business-process-header"></a>İşlem sürecinden İşlem Süreç Üst Bilgisine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processid                                      |
| PROCESSTYPE                    | cdm\_processtype                                    |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| AD                           | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| DURUM                         | cdm\_status                                         |
| TARGETDATE                     | cdm\_targetdate                                     |
| STARTDATETIME                  | cdm\_startdatetime                                  |
| ENDDATETIME                    | cdm\_enddatetime                                    |
| RESOLVEDBYPERSONNELNUMBER      | cdm\_resolvedbyid.cdm\_workernumber                  |
| PROCESSOWNERPERSONNELNUMBER    | cdm\_processownerid.cdm\_workernumber                |
| SOURCETEMPLATENAME             | cdm\_sourcetemplateid.cdm\_name                      |
| SOURCETEMPLATEPROCESSTYPE      | cdm\_sourcetemplateid.cdm\_businessprocesstype       |
| SOURCETEMPLATEGENERICSUBTYPE   | cdm\_sourcetemplateid.cdm\_genericsubtype            |

### <a name="business-process-library-task-group-to-business-process-library-task-group"></a>İş süreci kitaplığı görev grubundan İş Süreci Kitaplık Görev Grubuna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_processtype                                    |
| AD                           | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |

### <a name="business-process-stage-to-business-process-stage"></a>İşlem süreci aşamasından İşlem Süreç Aşamasına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| AD                           | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| SEQUENCENUMBER                 | cdm\_sequencenumber                                 |

### <a name="business-process-task-to-business-process-task"></a>İşletme süreç görevinden İşletme Süreç Görevine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| DUEDATE                        | cdm\_duedate                                        |
| TASKID                         | cdm\_taskid                                         |
| YÖNERGELER                   | cdm\_instructions                                   |
| COMPLETIONDATETIME             | cdm\_completiondatetime                             |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| AD                           | cdm\_name                                           |
| DURUM                         | cdm\_status                                         |
| RESOLVEDBY\_PERSONNELNUMBER     | cdm\_resolvedbyid.cdm\_workernumber                  |
| TEMPLATETASKID                 | cdm\_templatetaskid.cdm\_taskid                      |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedposition.cdm\_jobpositionnumber         |

### <a name="business-process-template-to-checklist-template-header"></a>İş süreci şablonundan Denetim Listesi Şablon Üst Bilgisine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSTYPE                    | cdm\_businessprocesstype                            |
| GENERICSUBTYPE                 | cdm\_genericsubtype                                 |
| AD                           | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| CALENDARID                     | cdm\_businessprocesscalendarid.cdm\_name             |
| PERSONELNUMARASI                | cdm\_processownerid.cdm\_workernumber                |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="business-process-template-task-to-checklist-template-task"></a>İş süreci şablonu görevinden Denetim Listesi Şablon Görevine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| TASKID                         | cdm\_taskid                                         |
| AD                           | cdm\_name                                           |
| TEMPLATEHEADER\_PROCESSTYPE     | cdm\_businessprocesstemplateheaderid.cdm\_businessprocesstype |
| TEMPLATEHEADER\_GENERICSUBTYPE  | cdm\_businessprocesstemplateheaderid.cdm\_genericsubtype |
| TEMPLATEHEADER\_NAME            | cdm\_businessprocesstemplateheaderid.cdm\_name       |
| AÇIKLAMA                    | cdm\_description                                    |
| DUEDATEOFFSETDAYS              | cdm\_duedateoffsetdays                              |
| MENUITEMTYPE                   | cdm\_tasklinktype                                   |
| MENUITEM                       | cdm\_tasklink                                       |
| CONTACTPERSON\_PERSONNELNUMBER  | cdm\_contactpersonid.cdm\_workernumber               |
| ASSIGNMENTTYPE                 | cdm\_assignmenttype                                 |
| ASSIGNEDWORKER\_PERSONNELNUMBER | cdm\_assignedworkerid.cdm\_workernumber              |
| ASSIGNEDPOSITION\_POSITIONID    | cdm\_assignedpositionid.cdm\_jobpositionnumber       |
| ASSIGNEDGROUP\_NAME             | cdm\_assignedgroupid.cdm\_name                       |
| ISOPTIONAL                     | cdm\_isoptional                                     |
| YÖNERGELER                   | cdm\_instructions                                   |

### <a name="calculation-frequency-to-benefit-calculation-frequency"></a>Hesaplama sıklığından Kazanç Hesaplama Sıklığına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| FREQUENCY                      | cdm\_name                                           |
| FREQUENCYCONTROL               | cdm\_frequencycontrol                               |
| ISIMMUTABLE                    | cdm\_isimmutable                                    |

### <a name="calculation-frequency-pay-period-to-benefit-calculation-frequency-pay-period"></a>Hesaplama sıklık ödeme döneminden Kazanç Hesaplama Sıklığı Ödeme Dönemine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| CALCULATIONFREQUENCYID         | cdm\_benefitcalculationfrequencyid.cdm\_name         |
| PERIODSTARTDATE                | cdm\_payperiodid.cdm\_periodstartdate                |
| PAYCYCLEID                     | cdm\_payperiodid.cdm\_paycycleid.cdm\_name            |

### <a name="calendar-to-work-calendar"></a>Takvimden İş Takvimine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARID                     | cdm\_name                                           |
| CALENDARNAME                   | cdm\_description                                    |
| WORKCALENDARHOLIDAYID          | cdm\_workcalendarholidayid.cdm\_name                 |

### <a name="compensation-fixed-action-table-to-fixed-compensation-event"></a>Ücret sabit eylem tablosundan Sabit Ücret Olayına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| EYLEM                         | cdm\_name                                           |
| ETKİN                         | cdm\_isactive                                       |
| AÇIKLAMA                    | cdm\_description                                    |
| TÜR                           | cdm\_eventtype                                      |

### <a name="compensation-fixed-plan-to-compensation-fixed-plan"></a>Ücret sabit plandan Ücret Sabit Plana

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PLAN                           | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| TÜR                           | cdm\_type                                           |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| PARA BİRİMİ                       | cdm\_transactioncurrencyid.isocurrencycode          |
| PAYFREQUENCY                   | cdm\_payfrequency.cdm\_name                          |
| HIRERULE                       | cdm\_hirerule                                       |
| OUTOFRANGETOLERANCE            | cdm\_outofrangetolerance                            |
| RECOMMENDATIONALLOWED          | cdm\_recommendationallowed                          |
| COMPENSATIONSTRUCTURE          | cdm\_compensationgrid.cdm\_name                      |
| REFPOINTSETUPID                | cdm\_referencepointsetupline.cdm\_referencepointsetupid.cdm\_name |
| CONTROLPOINT                   | cdm\_referencepointsetupline.cdm\_name               |

### <a name="compensation-grids-to-compensation-grid"></a>Ücret kılavuzlarından Ücret Kılavuzuna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| GRIDID                         | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| REFERENCESETUP                 | cdm\_referencepointsetupid.cdm\_name                 |
| TÜR                           | cdm\_type                                           |
| PARA BİRİMİ                       | cdm\_transactioncurrencyid.isocurrencycode          |

### <a name="compensation-job-function-to-job-function"></a>Ücret iş işlevinden İş İşlevine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| JOBFUNCTIONID                  | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |

### <a name="compensation-job-type-to-job-type"></a>Ücret iş türünden İş Türüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| JOBTYPEID                      | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| EXEMPTSTATUS                   | cdm\_exemptstatus                                   |

### <a name="compensation-pay-frequency-to-compensation-pay-frequency"></a>Ücret ödeme sıklığından Ücret Ödeme Sıklığına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PAYRATECONVERSION              | cdm\_name                                           |
| PERIOD                         | cdm\_period                                         |
| AÇIKLAMA                    | cdm\_description                                    |
| ANNUALCONVERSIONFACTOR         | cdm\_annualconversionfactor                         |
| HOURLYCONVERSIONFACTOR         | cdm\_hourlyconversionfactor                         |
| MONTHLYCONVERSIONFACTOR        | cdm\_monthlyconversionfactor                        |
| WEEKLYCONVERSIONFACTOR         | cdm\_weeklyconversionfactor                         |

### <a name="compensation-regions-to-compensation-region"></a>Ücret bölgelerinden Ücret Bölgesine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| KONUM                       | cdm\_name                                           |

### <a name="compensation-variable-plan-v2-to-compensation-variable-plan"></a>Ücret değişken plan V2'den Ücret Değişken Plana

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| VARIABLEAWARDBASIS             | cdm\_awardbasis                                     |
| AWARDBASISCALCULATION          | cdm\_awardbasiscalculation                          |
| CALCULATIONTYPE                | cdm\_calculationtype                                |
| AÇIKLAMA                    | cdm\_description                                    |
| ENABLEENROLLMENT               | cdm\_enableenrollment                               |
| ENABLELEVELS                   | cdm\_enablelevels                                   |
| ENABLERECOMMENDATION           | cdm\_enablerecommendation                           |
| HIRERULE                       | cdm\_hirerule                                       |
| LEVERAGE100PERCENT             | cdm\_leverage100percent                             |
| LEVERAGEMAXIMUM                | cdm\_leveragemaximum                                |
| LEVERAGEMINIMUM                | cdm\_leverageminimum                                |
| LEVERAGEOVEROBJECTIVE          | cdm\_leverageoverobjective                          |
| LEVERAGEUNDEROBJECTIVE         | cdm\_leverageunderobjective                         |
| PERCENTOFBASIS                 | cdm\_percentofbasis                                 |
| PLANID                         | cdm\_name                                           |
| VARIABLECOMPENSATIONTYPE       | cdm\_variablecompensationtypeid.cdm\_name            |
| UNITCURRENCYCODE               | transactioncurrencyid.isocurrencycode              |
| UNITRELATIONSHIP               | cdm\_unitrelationship                               |
| UNITVALUE                      | cdm\_unitvalue                                      |
| NUMBEROFUNITSREAL              | cdm\_numberofunits                                  |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| VESTINGRULE                    | cdm\_vestingruleid.cdm\_name                         |
| LEVERAGETOLERANCEMAX           | cdm\_leveragetolerancemax                           |
| LEVERAGETOLERANCEMIN           | cdm\_leveragetolerancemin                           |

### <a name="compensation-variable-type-to-compensation-variable-plan-type"></a>Ücret değişken türünden Ücret Değişken Plan Türüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| TÜR                           | cdm\_awardtype                                      |
| VARIABLECOMPENSATIONTYPE       | cdm\_name                                           |

### <a name="compensation-vesting-rules-to-vesting-rule"></a>Ücret hakediş ödeme kurallarından Hakediş Ödeme Kuralına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| NOT                           | cdm\_notes                                          |
| VESTINGRULE                    | cdm\_name                                           |

### <a name="department-v2-to-department"></a>Departman V2'den Departmana

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| OPERATINGUNITNUMBER            | cdm\_departmentnumber                               |
| AD                           | cdm\_name                                           |
| SEARCHNAME                     | cdm\_description                                    |
| PARTYTYPE                      | cdm\_partytype                                      |

### <a name="dual-write-tax-region-to-tax-region"></a>İkili Yazma Vergi Bölgesinden Vergi Bölgesine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| ŞEHİR                           | cdm\_city                                           |
| COUNTRYORREGION                | cdm\_countryorregion                                |
| İLÇE                         | cdm\_county                                         |
| EYALET                          | cdm\_stateorprovince                                |
| TAXREGIONNAME                  | cdm\_name                                           |

### <a name="dual-write-worker-identification-to-worker-person-identification-number"></a>Çift Yazma İşçi Kimlik Saptamadan İşçi Kişi Kimlik Saptama Numarasına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| ENTRYTYPE                      | cdm\_entrytype                                      |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| IDENTIFICATIONNUMBER           | cdm\_identificationnumber                           |
| IDENTIFICATIONTYPEID           | cdm\_identificationtypeid.cdm\_name                  |
| ISPRIMARY                      | cdm\_isprimary                                      |
| ISSUEDATE                      | cdm\_issuedate                                      |
| ISSUINGAGENCYID                | cdm\_issuingagencyid.cdm\_name                       |
| WORKERNUMBER                   | cdm\_workerid.cdm\_workernumber                      |

### <a name="compensation-structure-to-compensation-structure"></a>Ücret yapısından Ücret Yapısına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| TUTAR                         | cdm\_amount                                         |
| KILAVUZ                           | cdm\_compensationgridid.cdm\_name                    |
| LEVELID                        | cdm\_compensationlevelid.cdm\_name                   |
| REFERENCEPOINTLINENUMBER       | cdm\_referencepointid.cdm\_linenumber                |
| REFERENCESETUP                 | cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name |
| REFERENCEPOINT                 | cdm\_referencepointid.cdm\_name                      |

### <a name="earning-code-to-payroll-earning-code"></a>Kazanç kodundan Maaş Kazanç Koduna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| EARNINGCODE                    | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| INCLUDEINPAYMENTTYPE           | cdm\_includeinpaymenttype                           |
| QUANTITYUNIT                   | cdm\_quantityunit                                   |
| TRACKFMLAHOURS                 | cdm\_trackfmlahours                                 |
| ISPRODUCTIVE                   | cdm\_isproductive                                   |

### <a name="employee-fixed-compensation-to-worker-fixed-compensation"></a>Personel sabit ücretten Çalışan Sabit Ücrete

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| TÜR                           | cdm\_compensationtype                               |
| EFFECTIVEDATE                  | cdm\_effectivedate                                  |
| EXPIRATIONDATE                 | cdm\_expirationdate                                 |
| LINENUMBER                     | cdm\_linenumber                                     |
| PAYFREQUENCY                   | cdm\_payfrequencyid.cdm\_name                        |
| PAYRATE                        | cdm\_payrate                                        |
| PLAN                           | cdm\_planid.cdm\_name                                |
| POSITIONID                     | cdm\_positionid.cdm\_jobpositionnumber               |
| PROCESSTYPE                    | cdm\_processtype                                    |
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |
| EYLEM                         | cdm\_eventid.cdm\_name                               |
| AŞAMA                           | cdm\_referencepointsetuplineid.cdm\_name             |
| REFPOINTSETUPID                | cdm\_referencepointsetuplineid.cdm\_referencepointsetupid.cdm\_name |

### <a name="employment-per-company-to-employment"></a>Şirket başına istihdamdan İstihdama

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| EMPLOYMENTENDDATE              | cdm\_employmentenddate                              |
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |
| EMPLOYMENTSTARTDATE            | cdm\_employmentstartdate                            |
| WORKERTYPE                     | cdm\_workertype                                     |
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| ADJUSTEDWORKERSTARTDATE        | cdm\_adjustedworkerstartdate                        |
| EMPLOYERNOTICEAMOUNT           | cdm\_employernoticeamount                           |
| EMPLOYERUNITOFNOTICE           | cdm\_employerunitofnotice                           |
| WORKERUNITOFNOTICE             | cdm\_workerunitofnotice                             |
| WORKERNOTICEAMOUNT             | cdm\_workernoticeamount                             |
| LASTDATEWORKED                 | cdm\_lastdateworked                                 |
| PROBATIONENDDATE               | cdm\_probationenddate                               |
| TRANSITIONDATE                 | cdm\_transitiondate                                 |
| TRANSITIONREASONCODENAME       | cdm\_transitionreasoncode.cdm\_name                  |
| WORKERSTARTDATE                | cdm\_workerstartdate                                |
| VALIDTO                        | cdm\_validto                                        |
| VALIDFROM                      | cdm\_validfrom                                      |

### <a name="ethnic-origins-to-ethnic-origin"></a>Etnik kökenden Etnik Kökene

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| ETHNICORIGINID                 | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |

### <a name="group-assignment-to-business-process-group-assignment"></a>Grup atamasından İş Süreci Grup Atamasına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AD                           | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| ISACTIVE                       | cdm\_isactive                                       |

### <a name="identification-type-to-worker-person-identification-type"></a>Kimlik saptama türünden Çalışan Kişi Kimlik Saptama Türüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| IDENTIFICATIONTYPEID           | cdm\_name                                           |
| ALLOWEDVALUES                  | cdm\_allowedvalues                                  |
| FIXEDLENGTH                    | cdm\_fixedlength                                    |
| IDENTIFICATIONNUMBERFORMAT     | cdm\_identificationnumberformat                     |

### <a name="issuing-agency-to-person-identification-issuing-agency"></a>Düzenleyen kurumdan Kişi Kimliğini Düzenleyen Kuruma

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| E-POSTA                          | cdm\_email                                          |
| UZANTI                      | cdm\_extension                                      |
| FAKS                            | cdm\_fax                                            |
| ISSUINGAGENCY                  | cdm\_name                                           |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| AD                           | cdm\_description                                    |
| ÇAĞRI CİHAZI                          | cdm\_pager                                          |
| Kısa mesaj                            | cdm\_sms                                            |
| TELEFON                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telex                                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |

### <a name="job-positions-dual-write-to-job-position"></a>İş Pozisyonları Çift Yazmadan İş Pozisyonuna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONID                     | cdm\_jobpositionnumber                              |
| ETKİNLEŞTİRME                     | cdm\_activation                                     |
| AVAILABLEFORASSIGNMENT         | cdm\_availableforassignment                         |
| COMPENSATIONREGIONID           | cdm\_compensationregionid.cdm\_name                  |
| DEPARTMENTID                   | cdm\_departmentid.cdm\_departmentnumber              |
| AÇIKLAMA                    | cdm\_description                                    |
| FULLTIMEEQUIVALENT             | cdm\_fulltimeequivalent                             |
| JOBID                          | cdm\_jobid.cdm\_name                                 |
| PARENTPOSITIONID               | cdm\_parentjobpositionid.cdm\_jobpositionnumber      |
| POSITIONTYPEID                 | cdm\_positiontypeid.cdm\_name                        |
| RETIREMENT                     | cdm\_retirement                                     |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |

### <a name="jobs-dual-write-to-job"></a>İşler Çift Yazmadan İşe

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| JOBID                          | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| JOBDESCRIPTION                 | cdm\_jobdescription                                 |
| ALLOWUNLIMITEDPOSITIONS        | cdm\_allowunlimitedpositions                        |
| MAXIMUMNUMBEROFPOSITIONS       | cdm\_maximumnumberofpositions                       |
| JOBFUNCTIONID                  | cdm\_jobfunctionid.cdm\_name                         |
| JOBTYPEID                      | cdm\_jobtypeid.cdm\_name                             |
| TITLEID                        | cdm\_titleid.cdm\_name                               |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| DEFAULTFULLTIMEEQUIVALENCY     | cdm\_defaultfulltimeequivalent                      |

### <a name="language-codes-to-language"></a>Dil kodlarından Dile

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| LANGUAGECODEID                 | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |

### <a name="leave-and-absence-bank-transaction-v2-to-leave-bank-transaction"></a>İzin ve yokluk banka hareketi V2'den İzin Bank Hareketine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| TUTAR                         | cdm\_amount                                         |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TRANSACTIONDATE                | cdm\_transactiondate                                |
| TRANSACTIONNUMBER              | cdm\_transactionnumber                              |
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |
| TRANSACTIONTYPE                | cdm\_transactiontype                                |

### <a name="leave-and-absence-enrollment-v2-to-leave-enrollment"></a>İzin ve yokluk kaydı V2'den İzin Kaydına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_startdate                                      |
| ENDDATE                        | cdm\_enddate                                        |
| CUSTOMDATE                     | cdm\_customdate                                     |
| ACCRUALSTARTDATE               | cdm\_accrualstartdate                               |
| ACCRUALDATEBASIS               | cdm\_accrualdatebasis                               |
| ISACCRUALSUSPENDED             | cdm\_isaccrualsuspended                             |
| LEAVEPLANID                    | cdm\_leaveplanid.cdm\_name                           |
| TIERBASIS                      | cdm\_tierbasis                                      |
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |

### <a name="leave-and-absence-plan-v2-to-leave-plan"></a>İzin ve yokluk planı V2'den İzin Planına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| ACCRUALFREQUENCY               | cdm\_accrualfrequency                               |
| AD                           | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| STARTDATE                      | cdm\_startdate                                      |
| LEAVETYPEID                    | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-and-absence-type-to-leave-type"></a>İzin ve devamsızlık türünden İzin Türüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| TÜR                           | cdm\_type                                           |
| EARNINGCODEID                  | cdm\_earningcodeid.cdm\_name                         |

### <a name="leave-and-absence-type-reason-code-to-leave-type-reason-code"></a>İzin ve yokluk türü neden kodundan İzin Türü Neden Koduna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| LEAVETYPE                      | cdm\_typeid.cdm\_type                                |
| REASONCODEID                   | cdm\_reasoncodeid.cdm\_name                          |

### <a name="leave-time-off-request-detail-to-leave-request-detail"></a>İzin yokluk isteği ayrıntısından İzin İsteği Ayrıntısı

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| TUTAR                         | cdm\_amount                                         |
| LEAVEDATE                      | cdm\_leavedate                                      |
| REQUESTID                      | cdm\_leaverequestid.cdm\_leaverequestnumber          |
| TÜR                           | cdm\_leavetypeid.cdm\_type                           |

### <a name="leave-time-off-request-header-to-leave-request"></a>İzin yokluk isteği üst bilgisinden İzin İsteğine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| REQUESTID                      | cdm\_leaverequestnumber                             |
| REQUESTDATE                    | cdm\_requestdate                                    |
| DURUM                         | cdm\_status                                         |
| YORUM                        | cdm\_comment                                        |
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |

### <a name="levels-to-compensation-level"></a>Düzeylerden Ücret Düzeyine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| TÜR                           | cdm\_type                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| DÜZEY                          | cdm\_name                                           |

### <a name="onboarding-process-header-to-onboard-process-header"></a>Ekleme süreci üst bilgisinden Ekleme Süreci Üst Bilgisi

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PROCESSID                      | cdm\_processheaderid.cdm\_processid                  |
| ONBOARDEDEMPLOYEEPERSONNELNUMBER | cdm\_onboardedemployeeid.cdm\_workernumber           |
| EMPLOYMENTPERSONNELNUMBER      | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| LEGALENTITYID                  | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |
| EMPLOYMENTSTARTDATE            | cdm\_employmentid.cdm\_employmentstartdate           |

### <a name="pay-cycle-to-pay-cycle"></a>Ödeme döngüsünden Ödeme Döngüsüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| PAYCYCLEFREQUENCY              | cdm\_frequency                                      |

### <a name="pay-period-to-pay-period"></a>Ödeme döneminden Ödeme Dönemine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| COMMENTS                       | cdm\_description                                    |
| DEFAULTPAYMENTDATE             | cdm\_defaultpaymentdate                             |
| PAYCYCLEID                     | cdm\_paycycleid.cdm\_name                            |
| PERIODENDDATE                  | cdm\_periodenddate                                  |
| PERIODSTARTDATE                | cdm\_periodstartdate                                |
| DURUM                         | cdm\_status                                         |

### <a name="payroll-details-for-positions-to-payroll-position-detail"></a>Pozisyonlar için bordro ayrıntılarından Bordro Pozisyonu Ayrıntısına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PAYCYCLEID                     | cdm\_paycycle.cdm\_name                              |
| POSITIONID                     | cdm\_position.cdm\_jobpositionnumber                 |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| ANNUALREGULARHOURS             | cdm\_annualregularhours                             |
| PAIDBYLEGALENTITY              | cdm\_paidby.cdm\_companycode                         |

### <a name="position-default-dimensions-dual-write-to-job-position-dimension"></a>Pozisyon Varsayılan Boyutlar Çift Yazmadan İş Pozisyon Boyutuna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| DIMENSIONDISPLAYVALUE          | cdm\_dimensiondisplayvalue                          |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |

### <a name="position-type-to-position-type"></a>Pozisyon türünden Pozisyon Türüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| POSITIONTYPEID                 | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| CLASSIFICATION                 | cdm\_classification                                 |

### <a name="position-worker-assignments-v2-to-position-worker-assignment"></a>Pozisyon çalışan atamaları V2'den Pozisyon Çalışma Atamasına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |
| POSITIONID                     | cdm\_jobpositionid.cdm\_jobpositionnumber            |
| VALIDFROM                      | cdm\_validfrom                                      |
| VALIDTO                        | cdm\_validto                                        |
| IsPrimaryPosition              | cdm\_isprimaryposition                              |

### <a name="reason-codes-to-reason-code"></a>Neden kodlarından Neden Koduna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| REASONCODEID                   | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| ISABSENCEAPPLICABLE            | cdm\_isabsenceapplicable                            |
| ISAPPLICATIONAPPLICABLE        | cdm\_isapplicationapplicable                        |
| ISCOMPENSATIONAPPLICABLE       | cdm\_iscompensationapplicable                       |
| ISCREATENEWPOSITIONAPPLICABLE  | cdm\_iscreatenewpositionapplicable                  |
| ISEDITPOSITIONAPPLICABLE       | cdm\_iseditpositionapplicable                       |
| ISHIREAPPLICABLE               | cdm\_ishireapplicable                               |
| ISSKILLMAPPINGAPPLICABLE       | cdm\_isskillmappingapplicable                       |
| ISTERMINATIONAPPLICABLE        | cdm\_isterminationapplicable                        |
| ISTRANSFERAPPLICABLE           | cdm\_istransferapplicable                           |

### <a name="reference-point-setup-line-dual-write-to-compensation-reference-point-setup-line"></a>Referans Noktası Kurulum Hattından (Çift yazma) Ödeme Referans Noktası Kurulum Hattına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AÇIKLAMA                    | cdm\_description                                    |
| LINENUM                        | cdm\_linenumber                                     |
| REFPOINTID                     | cdm\_name                                           |
| REFPOINTSETUPID                | cdm\_referencepointsetupid.cdm\_name                 |

### <a name="reference-point-setups-to-compensation-reference-point-setup"></a>Referans noktası kurulumlarından Ödeme Referans Noktası Kurulumuna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| REFERENCESETUP                 | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| TÜR                           | cdm\_compensationtype                               |

### <a name="skill-types-to-skill-type"></a>Beceri türlerinden Beceri Türüne

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| SKILLTYPE                      | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |

### <a name="titles-to-title"></a>Başlıklardan Başlığa

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| TITLEID                        | cdm\_name                                           |

### <a name="variable-compensation-level-v2-to-compensation-variable-plan-level"></a>Değişken ödeme düzeyi V2'den Ödeme Değişken Plan Düzeyine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| AWARDAMOUNT                    | cdm\_awardamount                                    |
| AWARDPERCENT                   | cdm\_awardpercent                                   |
| AWARDUNITSREAL                 | cdm\_awardunits                                     |
| COMPENSATIONLEVELID            | cdm\_compensationlevelid.cdm\_name                   |
| PLANID                         | cdm\_compensationvariableplanid.cdm\_name            |

### <a name="veteran-status-to-veteran-status"></a>Gazilik durumundan Gazi Durumuna

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| VETERANSTATUSID                | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |
| ISPROTECTEDVETERAN             | cdm\_isprotectedveteran                             |

### <a name="work-calendar-enrollments-to-work-calendar-enrollment"></a>İş Takvimi Kayıtlarından İş Takvimi Kaydına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| STARTDATE                      | cdm\_employmentid.cdm\_employmentstartdate           |
| PERSONELNUMARASI                | cdm\_employmentid.cdm\_workerid.cdm\_workernumber     |
| CALENDARID                     | cdm\_workcalendarid.cdm\_name                        |
| COMPANYID                      | cdm\_employmentid.cdm\_companyid.cdm\_companycode     |

### <a name="work-calendar-holiday-to-work-calendar-holiday"></a>İş takvimi tatilden İş Takvimi Tatile

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| Kimlik                             | cdm\_name                                           |
| AÇIKLAMA                    | cdm\_description                                    |

### <a name="work-calendar-holiday-line-to-work-calendar-holiday-line"></a>İş takvimi tatil hattından İş Takvimi Tatil Hattına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| HOLIDAYID                      | cdm\_workcalendarholidayid.cdm\_name                 |
| AD                           | cdm\_name                                           |
| HOLIDAYDATE                    | cdm\_holidaydate                                    |

### <a name="worker-to-worker"></a>Çalışandan Çalışana

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONELNUMARASI                | cdm\_workernumber                                   |
| FIRSTNAME                      | cdm\_firstname                                      |
| MIDDLENAME                     | cdm\_middlename                                     |
| LASTNAME                       | cdm\_lastname                                       |
| WORKERTYPE                     | cdm\_type                                           |
| WORKERSTATUS                   | cdm\_status                                         |
| PRIMARYCONTACTEMAIL            | cdm\_primaryemailaddress                            |
| PRIMARYCONTACTPHONE            | cdm\_primarytelephone                               |
| PRIMARYCONTACTFACEBOOK         | cdm\_facebookidentity                               |
| PRIMARYCONTACTTWITTER          | cdm\_twitteridentity                                |
| PRIMARYCONTACTLINKEDIN         | cdm\_linkedinidentity                               |
| PRIMARYCONTACTURL              | cdm\_websiteurl                                     |
| CİNSİYET                         | cdm\_gender                                         |
| BIRTHDATE                      | cdm\_birthdate                                      |
| AD                           | cdm\_fullname                                       |

### <a name="worker-bank-accounts-to-worker-bank-account"></a>Çalışan banka hesaplarından Çalışan Banka Hesabına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| ACCOUNTIDENTIFICATION          | cdm\_accountidentification                          |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONID         | cdm\_countryorregion                                |
| ADDRESSCOUNTY                  | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_addressdescription                             |
| ADDRESSDISTRICTNAME            | cdm\_districtname                                   |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |
| BANKACCOUNTNUMBER              | cdm\_bankaccountnumber                              |
| BANKACCOUNTTYPE                | cdm\_bankaccounttype                                |
| E-POSTA                          | cdm\_email                                          |
| UZANTI                      | cdm\_extension                                      |
| FAKS                            | cdm\_fax                                            |
| INTERNETADDRESS                | cdm\_websiteurl                                     |
| MOBILEPHONE                    | cdm\_mobilephone                                    |
| ROUTINGNUMBER                  | cdm\_routingnumber                                  |
| TELEFON                      | cdm\_telephone                                      |
| TELEXNUMBER                    | cdm\_telexnumber                                    |
| BANKIBAN                       | cdm\_iban                                           |
| SWIFTNO                        | cdm\_swiftcode                                      |
| BANKLOCATIONCODE               | cdm\_banklocationcode                               |
| BRANCHNAME                     | cdm\_branchname                                     |
| BRANCHNUMBER                   | cdm\_branchnumber                                   |
| ROUTINGNUMBERTYPE              | cdm\_routingnumbertype                              |
| ACCOUNTHOLDER                  | cdm\_accountholder                                  |
| NAMEOFPERSON                   | cdm\_nameofperson                                   |
| AD                           | cdm\_description                                    |
| ADDRESSSTREET                  | cdm\_line1                                          |
| ADDRESSSTREETNUMBER            | cdm\_line2                                          |

### <a name="worker-personal-details-to-worker-personal-detail"></a>Çalışan kişisel ayrıntılardan Çalışan Kişisel Ayrıntıya

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |
| BIRTHDATE                      | cdm\_birthdate                                      |
| PERSONBIRTHCITY                | cdm\_birthcity                                      |
| CİNSİYET                         | cdm\_gender                                         |
| EXPATRIATEENDDATE              | cdm\_expatriateenddate                              |
| EXPATRIATESTARTDATE            | cdm\_expatriatestartdate                            |
| DISABLEDVETERAN                | cdm\_isdisabledveteran                              |
| DECEASEDDATE                   | cdm\_deceaseddate                                   |
| DISABLEDVERIFICATIONDATE       | cdm\_disabledveteranverificationdate                |
| EĞİTİM                      | cdm\_education                                      |
| ETHNICORIGINID                 | cdm\_ethnicoriginid.cdm\_name                        |
| ISDISABLED                     | cdm\_isdisabled                                     |
| ISFULLTIMESTUDENT              | cdm\_isfulltimestudent                              |
| ISEXPATRIATERULINGAPPLICABLE   | cdm\_isexpatriaterulingapplicable                   |
| MARITALSTATUS                  | cdm\_maritalstatus                                  |
| MILITARYSERVICESTARTDATE       | cdm\_militaryservicestartdate                       |
| MILITARYSERVICEENDDATE         | cdm\_militaryserviceenddate                         |
| NUMBEROFDEPENDENTS             | cdm\_numberofdependents                             |
| NATIVELANGUAGEID               | cdm\_nativelanguageidid.cdm\_name                    |
| NATIONALITYCOUNTRYREGION       | cdm\_nationalitycountryregion                       |
| PERSONBIRTHCOUNTRYREGION       | cdm\_birthcountryregion                             |
| FATHERBIRTHCOUNTRYREGION       | cdm\_fatherbirthcountryregion                       |
| MOTHERBIRTHCOUNTRYREGION       | cdm\_motherbirthcountryregion                       |
| CITIZENSHIPCOUNTRYREGION       | cdm\_citizenshipcountryregion                       |
| VETERANSTATUSID                | cdm\_veteranstatusid.cdm\_name                       |

### <a name="worker-postal-addresses-dual-write-to-worker-address"></a>Çalışan posta adresi çift yazmadan Çalışan Adresine

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| PERSONELNUMARASI                | cdm\_workerid.cdm\_workernumber                      |
| ADDRESSLOCATIONID              | cdm\_addressnumber                                  |
| ADDRESSLOCATIONROLES           | cdm\_addresstype                                    |
| ETKİLİ                      | cdm\_effectivedate                                  |
| BİTİŞ TARİHİ                     | cdm\_expirationdate                                 |
| ADDRESSSTREET                  | cdm\_street                                         |
| ADDRESSSTREETNUMBER            | cdm\_streetnumber                                   |
| ADDRESSCITY                    | cdm\_city                                           |
| ADDRESSCOUNTRYREGIONISOCODE    | cdm\_countryregion                                  |
| ADDRESSSTATE                   | cdm\_stateorprovince                                |
| ADDRESSCOUNTYID                | cdm\_county                                         |
| ADDRESSDESCRIPTION             | cdm\_description                                    |
| ADDRESSLATITUDE                | cdm\_latitude                                       |
| ADDRESSLONGITUDE               | cdm\_longitude                                      |
| ADDRESSZIPCODE                 | cdm\_postalcode                                     |
| ADDRESSPOSTBOX                 | cdm\_postofficebox                                  |
| ISPRIMARY                      | cdm\_ispreferred                                    |

### <a name="working-time-to-work-calendar-time-interval"></a>Çalışma süresinden İş Takvim Süre Aralığına

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| ENDTIME                        | cdm\_endtime                                        |
| STARTTIME                      | cdm\_starttime                                      |
| WORKCALENDARDATE               | cdm\_workcalendardayid.cdm\_calendardate             |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKCALENDARID                 | cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name  |

### <a name="working-times-to-work-calendar-day"></a>Çalışma sürelerinden İş Takvim Gününe

| Finans varlığı                 | Dataverse tablosu                                    | 
|--------------------------------|----------------------------------------------------|
| CALENDARDATE                   | cdm\_calendardate                                   |
| WORKCALENDARID                 | cdm\_workcalendarid.cdm\_name                        |
| WORKINGDAYDEFINITION           | cdm\_status                                         |

## <a name="integration-considerations"></a>Tümleştirmeyle ilgili değerlendirmeler

- Her iki sistemde bulunan verilerde yapılan tüm değişiklikler, diğer sistemin doğrulanmasına tabi olacaktır. Bir hata oluşursa, veriler her iki sistemde de yazılmaz. 
- Tüm yazma işlemleri, varsayılan veriye tabidir (Finance'de özel mantık oluşursa).
- Çift yazılabilir entegratör alıcı uygulaması, iki sistem arasında eşleme yapmak için tümleştirme anahtarlarını kullanır. Bazen, özellikle birden fazla tümleştirme anahtarı gereksinimleri yerine getiriyorlarsa, doğru tümleştirme anahtarını seçmek zordur. Bu seçimle ilgili yardım için, aşağıdaki tabloda eşlemeleriniz için önerilen tümleştirme anahtarları listelenmektedir.

| Dataverse tablosu                          | Tümleştirme anahtarları |
|------------------------------------------|------------------|
| Banka hesabı ödemeleri                | cdm\_bankaccountid.cdm\_accountidentification, cdm\_bankaccountid.cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Kazanç Hesaplama Sıklığı            | cdm\_name |
| Kazanç Hesaplama sıklığı ödeme dönemi | cdm\_payperiodid.cdm\_periodstartdate, cdm\_payperiodid.cdm\_paycycleid.cdm\_name, cdm\_benefitcalculationfrequencyid.cdm\_name |
| Kazanç hesaplama oranı                 | cdm\_name |
| Kazanç hesaplama oranı ayrıntısı          | cdm\_workerdeduction, cdm\_effective, cdm\_calculationrateid.cdm\_name |
| Kazanç seçeneği                           | cdm\_name |
| Kazanç Türü                             | cdm\_name |
| İş Süreci Takvimi                | cdm\_name |
| İş Süreci Grup Ataması        | cdm\_name |
| İş Süreci Üst Bilgisi                  | cdm\_processid |
| İş Süreci Kitaplığı Görev Grubu      | cdm\_processtype, cdm\_name |
| İş Süreci Aşaması                   | cdm\_name, cdm\_businessprocesstype, cdm\_companyid.cdm\_companycode |
| İş Süreci Görevi                    | cdm\_taskid |
| İş Birimi                            | |
| Denetim Listesi Şablonu Başlığı                | cdm\_businessprocesstype, cdm\_name, cdm\_genericsubtype |
| Denetim Listesi Şablonu Görevi                  | cdm\_taskid |
| Şirket                                  | cdm\_companycode |
| Ücret Sabit Planı                  | cdm\_name, cdm\_company.cdm\_companycode |
| Ücret Izgarası                        | cdm\_name, cdm\_companyid.cdm\_companycode |
| Ücret Düzeyi                       | cdm\_name |
| Maaş ödeme sıklığı               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Ücret referans noktası ayarı       | cdm\_name, cdm\_companyid.cdm\_companycode |
| Ücret referans noktalarını ayar çizgisi  | cdm\_name, cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode |
| Ücret Bölgesi                      | cdm\_name |
| Maaş yapısı                   | cdm\_compensationlevelid.cdm\_name, cdm\_referencepointid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_name, cdm\_referencepointid.cdm\_referencepointsetupid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_compensationgridid.cdm\_name, cdm\_compensationgridid.cdm\_companyid.cdm\_companycode |
| Değişken Ücret Planı               | cdm\_name, cdm\_companyid.cdm\_companycode |
| Değişken Ücret Planı Düzeyi         | cdm\_companyid.cdm\_companycode, cdm\_compensationvariableplanid.cdm\_name, cdm\_compensationvariableplanid.cdm\_companyid.cdm\_companycode, cdm\_compensationlevelid.cdm\_name |
| Değişken Ücret Planı Türü          | cdm\_name, cdm\_companyid.cdm\_companycode |
| Para birimi                                 | isocurrencycode |
| Departman                               | cdm\_departmentnumber |
| İstihdam                               | cdm\_employmentstartdate, cdm\_workerid.cdm\_workernumber, cdm\_companyid.cdm\_companycode |
| Etnik Köken                            | cdm\_name |
| Sabit Ücret Etkinliği                 | cdm\_name, cdm\_companyid.cdm\_companycode |
| Görev                                      | cdm\_name |
| İş İşlevi                             | cdm\_name |
| İş Pozisyonu                             | cdm\_jobpositionnumber |
| İş Pozisyonu Boyutu                   | cdm\_jobpositionid.cdm\_jobpositionnumber, cdm\_companyid.cdm\_companycode |
| İş Türü                                 | cdm\_name |
| Dil                                 | cdm\_name |
| İzin Bankası Hareketi                   | cdm\_transactiondate, cdm\_transactiontype, cdm\_transactionnumber, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| İzin Kaydı                         | cdm\_startdate, cdm\_leaveplanid.cdm\_name, cdm\_leaveplanid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workerid.cdm\_workernumber |
| İzin Planı                               | cdm\_name, cdm\_companyid.cdm\_companycode |
| İzin İsteği                            | cdm\_leaverequestnumber, cdm\_companyid.cdm\_companycode |
| Ayrılma talebi ayrıntıları                     | cdm\_leavedate, cdm\_leavetypeid.cdm\_type, cdm\_leavetypeid.cdm\_companyid.cdm\_companycode, cdm\_leaverequestid.cdm\_leaverequestnumber, cdm\_leaverequestid.cdm\_companyid.cdm\_companycode |
| İzin Türü                               | cdm\_type, cdm\_companyid.cdm\_companycode |
| İzin Türü Neden Kodu                   | cdm\_reasoncodeid.cdm\_name, cdm\_typeid.cdm\_type, cdm\_typeid.cdm\_companyid.cdm\_companycode |
| İşe Alım Süreci Üst Başlığı                   | cdm\_processheaderid.cdm\_processid |
| Organizasyon                             | |
| Ödeme Döngüsü                                | cdm\_name |
| Ödeme Dönemi                               | cdm\_periodstartdate, cdm\_paycycleid.cdm\_name, cdm\_periodenddate |
| Bordro Kazanç Kodu                     | cdm\_name |
| Bordro Pozisyon Ayrıntısı                  | cdm\_validfrom, cdm\_validto, cdm\_position.cdm\_jobpositionnumber |
| Kişi Kimliğini Düzenleyen Kurum     | cdm\_name |
| Pozisyon türü                            | cdm\_name |
| Pozisyon Çalışan Ataması               | cdm\_validfrom, cdm\_jobpositionid.cdm\_jobpositionnumber |
| Neden Kodu                              | cdm\_name |
| Yetenek Türü                               | cdm\_name |
| Vergi Bölgesi                               | cdm\_stateorprovince, cdm\_name, cdm\_countryorregion, cdm\_county, cdm\_city |
| Takım                                     | azureactivedirectoryobjectid, membershiptype |
| Başlık                                    | cdm\_name |
| Kullanıcı                                     | azureactivedirectoryobjectid |
| Hakediş Ödeme Kuralı                             | cdm\_name, cdm\_companyid.cdm\_companycode |
| Gazilik Durumu                           | cdm\_name |
| İş Takvimi                            | cdm\_name, cdm\_companyid.cdm\_companycode |
| İş Takvimi Gün                        | cdm\_calendardate, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| İş Takvimi Kaydı                 | cdm\_employmentid.cdm\_employmentstartdate, cdm\_employmentid.cdm\_workerid.cdm\_workernumber, cdm\_employmentid.cdm\_companyid.cdm\_companycode |
| İş Takvimi Tatili                    | cdm\_name |
| Çalışma takvimi tatil satırı               | cdm\_holidaydate, cdm\_workcalendarholidayid.cdm\_name |
| Çalışma Takvimi Zaman Aralığı              | cdm\_starttime, cdm\_workcalendardayid.cdm\_calendardate, cdm\_workcalendardayid.cdm\_companyid.cdm\_companycode, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_name, cdm\_workcalendardayid.cdm\_workcalendarid.cdm\_companyid.cdm\_companycode, cdm\_companyid.cdm\_companycode, cdm\_workcalendarid.cdm\_name, cdm\_workcalendarid.cdm\_companyid.cdm\_companycode |
| Çalışan                                   | cdm\_workernumber |
| Çalışan Adresi                           | cdm\_addressnumber, cdm\_addresstype, cdm\_workerid.cdm\_workernumber |
| Çalışan Banka Hesabı                      | cdm\_accountidentification, cdm\_workerid.cdm\_workernumber |
| Çalışan Sabit Ücreti                | cdm\_linenumber, cdm\_effectivedate, cdm\_companyid.cdm\_companycode, cdm\_positionid.cdm\_jobpositionnumber, cdm\_workerid.cdm\_workernumber, cdm\_eventid.cdm\_name, cdm\_eventid.cdm\_companyid.cdm\_companycode, cdm\_planid.cdm\_name, cdm\_planid.cdm\_company.cdm\_companycode |
| Çalışan Kişi Tanımlama Numarası      | cdm\_identificationnumber, cdm\_workerid.cdm\_workernumber, cdm\_identificationtypeid.cdm\_name |
| Çalışan Kişi Tanımlama Türü        | cdm\_name |
| Çalışan Kişisel Bilgisi                   | cdm\_workerid.cdm\_workernumber |
