---
title: Başlangıç eşitlemesi sırasında sorunları giderme
description: Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 985825d3a205f566a94ac7532e45895e7060edf5
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416993"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Başlangıç eşitlemesi sırasında sorunları giderme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finance and Operations uygulamadaki ilk eşitleme hatalarını denetle

Eşleme şablonları etkinleştirildikten sonra, haritaların durumu **çalışıyor** olmalıdır. Durum **çalışmıyorsa**, ilk eşitleme sırasında hata meydana geldi. Hataları görüntülemek için **çift-yazma** sayfasında **ilk eşitleme ayrıntıları** sekmesini seçin.

![İlk eşitleme ayrıntıları sekmesinde hata.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>İlk eşitlemeyi tamamlayamıyoruz: 400 Hatalı Istek

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Eşlemeyi ve ilk senkronizasyonu çalıştırmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*(\[Hatalı İstek\], Uzak sunucu bir hata döndürdü: (400) Hatalı İstek.), AX dışarı aktarma işlemi bir hatayla karşılaştı.*

Burada tam hata mesajı tablosu için bir örnek verilmiştir.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Bu hata sürekli olarak oluşuyorsa ve ilk eşitlemeyi tamamlayamıyorsa, sorunu düzeltmek için aşağıdaki adımları izleyin.

1. Finance and Operations uygulamanın sanal makinesine (VM) oturum açın.
2. Microsoft Yönetim Konsolu 'Nu açın.
3. **Hizmetler** bölmesinde, Microsoft Dynamics 365 veri alma verme çerçevesi hizmetinin çalışmakta olduğundan emin olun. Durdurulmuşsa, ilk eşitleme gerektirdiğinden yeniden Başlat.

## <a name="initial-synchronization-error-403-forbidden"></a>İlk eşitleme hatası: 403 Yasak

İlk eşitlemede aşağıdaki hata iletisini alabilirsiniz:

*(\[Yasak\], Uzak sunucu hata verdi: (403) Yasak), AX dışarı aktarma bir hatayla karşılaştı*

Sorunu düzeltmek için şu adımları izleyin.

1. Finance and Operations Uygulamaya oturum açın.
2. **Azure Active Directory uygulamalar** sayfasında **DtAppID** istemcisini silin ve sonra yeniden ekleyin.

![Azure AD uygulamaları listesinde DtAppID istemcisi.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>İlk eşitleme sırasında kendi kendine referans veya döngüsel referans hataları

Eşlemelerinizin kendi kendine veya çevresel referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz: Hatalar aşağıdaki kategorilere ayrılır:

- [Vendors V2–to–msdyn_vendors tablo eşlemesinde hatalar](#error-vendor-map)
- [Customers V3–to–Accounts tablo eşlemesinde hatalar](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Vendors V2–to–msdyn_vendors tablo eşlemesinde hataları çözümleme

Tabloların, **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarında değerleri bulunan mevcut satırları varsa **Satıcılar V2** ile **msdyn\_vendors** eşlemesinde ilk eşitleme hatalarıyla karşılaşabilirsiniz. Bu hatalar **InvoiceVendorAccountNumber** kendi kendine başvuran bir sütun olduğundan ve **PrimaryContactPersonId**, satıcı eşlemede döngüsel bir başvuru olduğundan gerçekleşir.

Aldığınız hata iletileri aşağıdaki şekilde olacaktır.

*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Burada bazı örnekler verilmiştir:

- *Alan için GUID çözümlenemedi: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Alan için GUID çözümlenemedi: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Arama bulunamadı: V24-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Satıcı tablosunda **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarında değerleri bulunan satırlarınız varsa ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin.

1. Finance and Operations uygulamasında, eşlemeden **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarını silin ve ardından eşlemeyi kaydedin.

    1. **Satıcılar V2 (msdyn\_vendors)** için çift yazma eşleme sayfasında, **Tablo eşlemeleri** sekmesinde, sol filtrede **Finance and Operations apps.Vendors V2**'yi seçin. Sağ filtrede, **Sales.Vendor**'u seçin.
    2. **primarycontactperson** öğesini arayıp **PrimaryContactPersonId** kaynak sütununu bulun.
    3. **Eylemler**'i ve sonra **Sil**'i seçin.

        ![PrimaryContactPersonId sütununu silme.](media/vend_selfref3.png)

    4. **InvoiceVendorAccountNumber** sütununu silmek için bu adımları tekrarlayın.

        ![InvoiceVendorAccountNumber sütununu silme.](media/vend-selfref4.png)

    5. Değişikliklerinizi eşlemeye kaydedin.

2. **Satıcılar V2** tablosu için değişiklik izlemeyi kapatın.

    1. **Veri yönetimi** çalışma alanında **Veri tabloları** kutucuğunu seçin.
    2. **Satıcılar V2** tablosunu seçin.
    3. Eylem Bölmesinde, **Seçenekler**'i ve sonra **Değişiklik izleme**'yi seçin.

        ![Değişiklik izleme seçeneğini belirleme.](media/selfref_options.png)

    4. **Değişiklik izlemeyi devre dışı bırak**'ı seçin.

        ![Değişiklik İzlemeyi Devre Dışı Bırak'ı seçme.](media/selfref_tracking.png)

3. **Satıcı v2 (msdyn\_vendors)** eşlemesinin ilk eşitlemesini çalıştırın. İlk eşitleme hatasız olarak çalışmalıdır.
4. **CDS İlgili Kişileri V2 (ilgili kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın. İlk eşitlemenin ilgili kişi satırları için de yapılması gerektiğinden, satıcılar tablosundaki birincil ilgili kişi sütununu eşitlemek istiyorsanız bu eşlemeyi eşitlemeniz gerekir.
5. **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarını **Satıcılar v2 (msdyn\_vendors)** eşlemesine geri ekleyin ve eşlemeyi kaydedin.
6. **Satıcı v2 (msdyn\_vendors)** eşlemesinin ilk eşitlemesini yeniden çalıştırın. Değişiklik izleme devre dışı bırakıldığından tüm satırlar eşitlenecek.
7. **Satıcılar V2** tablosu için değişiklik izlemeyi yeniden açın.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Customers V3–to–Accounts tablo eşlemesinde hataları çözümleme

Tabloların, **ContactPersonID** ve **InvoiceAccount** sütunlarında değerleri bulunan mevcut satırları varsa **Müşteriler V3** ile **Hesaplar** eşlemesinde ilk eşitleme hatalarıyla karşılaşabilirsiniz. Bu hataların oluşma nedeni, **InvoiceAccount** sütununun kendine başvuruda bulunan bir sütun olması ve **ContactPersonID**'nin satıcı eşlemesinde döngüsel bir başvuru olmasıdır.

Aldığınız hata iletileri aşağıdaki şekilde olacaktır.

*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Burada bazı örnekler verilmiştir:

- *Alan için GUID çözümlenemedi: primarycontactid.msdyn\_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Alan için GUID çözümlenemedi: msdyn\_billingaccount.accountnumber. Arama bulunamadı: 1206-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Müşteri tablosunda **ContactPersonID** ve **InvoiceAccount** sütunlarında değerler bulunan satırlar varsa ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin. Bu yaklaşımı, **Hesaplar** ve **İlgili kişiler** gibi kullanıma hazır tüm tablolar için kullanabilirsiniz.

1. Finance and Operations uygulamasında, **Müşteriler V3 (firmalar)** eşlemesinden **ContactPersonID** ve **InvoiceAccount** sütunlarını silin ve değişiklikleri kaydedin.

    1. **Müşteriler V3 (firmalar)** için çift yazma eşleme sayfasında, **Tablo eşlemeleri** sekmesinde, sol filtrede, **Finance and Operations app.Customers V3** öğesini seçin. Sağ filtrede, **Dataverse.Firma**'yı seçin.
    2. **contactperson** öğesini arayıp **ContactPersonID** kaynak sütununu bulun.
    3. **Eylemler**'i ve sonra **Sil**'i seçin.

        ![ContactPersonID sütununu silme.](media/cust_selfref3.png)

    4. **InvoiceAccount** sütununu silmek için bu adımları tekrarlayın.

        ![InvoiceAccount sütununu silme.](media/cust_selfref4.png)

    5. Değişikliklerinizi eşlemeye kaydedin.

2. **Müşteriler V3** tablosu için değişiklik izlemeyi kapatın.

    1. **Veri yönetimi** çalışma alanında **Veri tabloları** kutucuğunu seçin.
    2. **Müşteriler V3** tablosunu seçin.
    3. Eylem Bölmesinde, **Seçenekler**'i ve sonra **Değişiklik izleme**'yi seçin.

        ![Değişiklik izleme seçeneğini belirleme.](media/selfref_options.png)

    4. **Değişiklik izlemeyi devre dışı bırak**'ı seçin.

        ![Değişiklik İzlemeyi Devre Dışı Bırak'ı seçme.](media/selfref_tracking.png)

3. **Müşteriler V3 (Hesaplar)** eşlemesi için başlangıç eşitlemesini çalıştırın. İlk eşitleme hatasız olarak çalışmalıdır.
4. **CDS İlgili Kişileri V2 (ilgili kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın.

    > [!NOTE]
    > Aynı ada sahip iki eşleme var. **Ayrıntılar** sekmesinde şu açıklama bulunan eşlemeyi seçtiğinizden emin olun: **FO.CDS Satıcı İlgili Kişileri V2 ile CDS.İlgili Kişileri arasında eşitleme için çift yazma şablonu. \[Dynamics365SupplyChainExtended\] yeni paketini gerektirir.**

5. **Müşteriler V3 (Hesaplar)** eşlemesinden **InvoiceAccount** ve **ContactPersonId** sütunlarını silin ve değişiklikleri kaydedin. Şimdi, hem **InvoiceAccount** sütunu hem de **ContactPersonId** sütunu yeniden canlı eşitleme modunun parçası olarak kullanılır. Sonraki adımda, bu sütunlar için başlangıç eşitlemesini tamamlayacaksınız.
6. **Müşteriler V3 (Hesaplar)** eşlemesi için başlangıç eşitlemesini yeniden çalıştırın. Değişiklik izleme devre dışı bırakıldığından, **InvoiceAccount** ve **ContactPersonId** için veriler Finance and Operations uygulamasından Dataverse'e eşitlenecektir.
7. **InvoiceAccount** ve **ContactPersonId** için verileri Dataverse'dan Finance and Operations uygulamasına eşitlemek için bir veri tümleştirme projesi kullanmanız gerekir.

    1. Power Apps içinde, **Sales.Account** ve **Finance and Operations apps.Customers V3** tabloları arasında veri tümleştirme projesi oluşturun. Veri yönü, Dataverse'ten Finance and Operations uygulamasına olmalıdır. **InvoiceAccount** çift yazmada yeni bir öznitelik olduğundan, bunun için ilk eşitlemeyi atlamak isteyebilirsiniz. Daha fazla bilgi için bkz. [Dataverse'e veri entegre edin](/power-platform/admin/data-integrator).

        Aşağıdaki resimde **CustomerAccount** ve **ContactPersonId**'yi güncelleştiren bir proje gösterilmektedir .

        ![CustomerAccount ve ContactPersonId alanını güncelleştirmek için veri tümleştirme projesi.](media/cust_selfref6.png)

    2. Finance and Operations uygulamasında yalnızca filtre ölçütleriyle eşleşen satırların güncelleştirilmesi için şirket ölçütlerini Dataverse tarafında filtreye ekleyin. Filtre eklemek için filtre düğmesini seçin. Ardından, **Sorguyu düzenle** iletişim kutusunda **\_msdyn\_company\_value eq '\<guid\>'** gibi bir filtre sorgusu ekleyebilirsiniz.

        > [NOT] Filtre düğmesi yoksa, veri tümleştirme ekibinin kiracınızda filtre yeteneğini etkinleştirmesini istemek için bir destek bileti oluşturun.

        **\_msdyn\_company\_value** için bir filtre sorgusu girmezseniz tüm satırlar eşitlenir.

        ![Filtre sorgusu ekleme.](media/cust_selfref7.png)

    Satırların ilk eşitlenme işlemi şimdi tamamlandı.

8. Finance and Operations uygulamasında, **Müşteriler V3** tablosu için değişiklik izlemeyi yeniden açın.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>10'dan fazla arama alanına sahip eşlemelerde ilk eşitleme hataları

**Müşteriler V3 - Firmalar**, **Satış siparişleri** eşlemelerinde bir ilk eşitleme çalıştırmayı denediğinizde veya 10'dan fazla arama alanı olan bir eşlemede hata aldığınızda aşağıdaki hata iletisini alırsınız:

*CRMExport: Paket yürütme tamamlandı. Hata Açıklaması 5 https://xxxxx//datasets/yyyyy/tables/accounts/items?$select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq 'id')&$orderby=accountnumber asc'den veri alma girişimleri başarısız oldu.*

Sorgudaki arama sınırlaması nedeniyle varlık eşlemesi 10'dan fazla arama içerdiğinde ilk eşitleme başarısız olur. Daha fazla bilgi için bkz. [Sorguyla ilgili tablo kayıtlarını alma](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Bu sorunu düzeltmek için şu adımları izleyin:

1. Arama sayısının 10 veya daha az olması için çift yazma varlık eşlemesinden isteğe bağlı arama alanlarını kaldırın.
2. Eşlemeyi kaydedin ve ilk eşitlemeyi yapın.
3. İlk adım için ilk eşitleme başarılı olduğunda kalan arama alanlarını ekleyin ve ilk adımda eşitlediğiniz arama alanlarını kaldırın. Arama alanlarının sayısının 10 veya daha az olduğundan emin olun. Eşlemeyi kaydedin ve ilk eşitlemeyi çalıştırın.
4. Tüm arama alanları eşitlenene kadar bu adımları yineleyin.
5. Tüm arama alanlarını yeniden eşlemeye ekleyin, eşlemeyi kaydedin ve **İlk eşitlemeyi atla** ile eşlemeyi çalıştırın.

Bu işlem, eşlemeyi canlı eşitleme modu için etkinleştirir.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Taraf posta adreslerinin ve taraf elektronik adreslerinin ilk eşitlemesi sırasında bilinen bir sorun

Taraf posta adreslerinin ve taraf elektronik adreslerinin ilk eşitlemesini çalıştırmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*Taraf numarası Dataverse uygulamasında bulunamadı.*

Finance and Operations uygulamalarında **Kişi** ve **Kuruluş** türündeki tarafları filtreleyen **DirPartyCDSEntity** öğesinde ayarlanmış bir aralık vardır. Sonuç olarak, **CDS Tarafları – msdyn_parties** eşlemesinin ilk eşitlemesi, **Tüzel Kişilik** ve **Faaliyet Birimi** dahil olmak üzere diğer türdeki tarafları eşitlemez. İlk eşitleme **CDS Taraf posta adresleri (msdyn_partypostaladdresses)** veya **Taraf İlgili Kişileri V3 (msdyn_partyelectronicaddresses)** için çalıştığında bu hatayla karşılaşabilirsiniz.

Her türden partinin Dataverse ile başarılı bir şekilde eşitlenebilmesi için Finance and Operations varlığındaki taraf türü aralığını kaldırmak üzere bir düzeltme üzerinde çalışıyoruz.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Müşteriler veya İlgili Kişiler verileri için ilk eşitlemeyi çalıştırırken herhangi bir performans sorunu yaşıyor musunuz?

**Müşteri** verileri için ilk eşitlemeyi çalıştırdıysanız ve **Müşteri** eşlemelerini çalıştırıp ardından da **İlgili Kişiler** verileri için ilk eşitlemeyi çalıştırırsanız **İlgili Kişi** adresleri için **LogisticsPostalAddress** ve **LogisticsElectronicAddress** tablolarına yapılan eklemeler ve güncelleştirmeler sırasında performans sorunlarıyla karşılaşabilirsiniz. Aynı genel posta adresi ve elektronik adres tabloları **CustCustomerV3Entity** ve **VendVendorV2Entity** için izlenir ve çift yazma, diğer tarafa veri yazmak için daha fazla sorgu oluşturmaya çalışır. **Müşteri** için ilk eşitlemeyi zaten çalıştırdıysanız **İlgili Kişiler** verileri için ilk eşitlemeyi çalıştırmadan önce ilgili eşlemeyi durdurun. **Satıcı** verileri için de aynısını yapın. İlk eşitleme tamamlandığında ilk eşitlemeyi atlayarak tüm eşlemeleri çalıştırabilirsiniz.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
