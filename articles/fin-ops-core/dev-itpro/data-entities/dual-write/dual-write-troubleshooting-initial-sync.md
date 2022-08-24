---
title: Başlangıç eşitlemesi sırasında sorunları giderme
description: Bu makalede, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 06/24/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d9d74eea90cc2dfca2d5decf6e5cd1d7f52da2a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289499"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Başlangıç eşitlemesi sırasında sorunları giderme

[!include [banner](../../includes/banner.md)]



Bu makalede, finans ve operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında sorun giderme bilgileri sağlanmaktadır. Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu makalede ele alınan bazı sorunlar için sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finans ve operasyon uygulamasında başlangıçtaki eşitleme hatalarını denetleme

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

1. Finans ve operasyon uygulamasının sanal makinesinde (VM) oturum açın.
2. Microsoft Yönetim Konsolu 'Nu açın.
3. **Hizmetler** bölmesinde, Microsoft Dynamics 365 veri alma verme çerçevesi hizmetinin çalışmakta olduğundan emin olun. Durdurulmuşsa, ilk eşitleme gerektirdiğinden yeniden Başlat.

## <a name="initial-synchronization-error-403-forbidden"></a>İlk eşitleme hatası: 403 Yasak

İlk eşitlemede aşağıdaki hata iletisini alabilirsiniz:

*(\[Yasak\], Uzak sunucu hata verdi: (403) Yasak), AX dışarı aktarma bir hatayla karşılaştı*

Sorunu düzeltmek için şu adımları izleyin.

1. Finans ve operasyon uygulamasında oturum açın.
2. **Azure Active Directory uygulamalar** sayfasında **DtAppID** istemcisini silin ve sonra yeniden ekleyin.

![Azure AD uygulamaları listesinde DtAppID istemcisi.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>İlk eşitleme sırasında kendi kendine referans veya döngüsel referans hataları

Eşlemelerinizin kendi kendine veya çevresel referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz: Hatalar aşağıdaki kategorilere ayrılır:

- [Vendors V2–to–msdyn_vendors tablo eşlemesinde hatalar](#error-vendor-map)
- [Customers V3–to–Accounts tablo eşlemesinde hatalar](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Vendors V2–to–msdyn_vendors tablo eşlemesinde hataları çözümleme

Tabloların, **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarında değerleri bulunan mevcut satırları varsa **Satıcılar V2** ile **msdyn\_vendors** eşlemesinde ilk eşitleme hatalarıyla karşılaşabilirsiniz. Bu hatalar **InvoiceVendorAccountNumber** kendi kendine başvuran bir sütun olduğundan ve **PrimaryContactPersonId**, satıcı eşlemede döngüsel bir başvuru olduğundan gerçekleşir.

Aldığınız hata iletileri aşağıdaki şekilde olacaktır.

*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Referans verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Burada bazı örnekler verilmiştir:

- *Alan için GUID çözümlenemedi: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Arama bulunamadı: 000056. Referans verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Alan için GUID çözümlenemedi: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Arama bulunamadı: V24-1. Referans verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Satıcı tablosunda **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarında değerleri bulunan satırlarınız varsa ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin.

1. Finans ve operasyon uygulamasında, **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** sütunlarını eşlemeden silin ve eşlemeyi kaydedin.

    1. **Satıcılar V2 (msdynvendors\_)** için çift yazma eşleme sayfasında, **Tablo eşlemeleri** sekmesinde, soldaki filtrede **Finans ve operasyon uygulamaları.Satıcılar V2**'yi seçin. Sağ filtrede, **Sales.Vendor**'u seçin.
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

*Alan için GUID çözümlenemedi: \<field\>. Arama bulunamadı: \<value\>. Referans verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Burada bazı örnekler verilmiştir:

- *Alan için GUID çözümlenemedi: primarycontactid.msdyn\_contactpersonid. Arama bulunamadı: 000056. Referans verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Alan için GUID çözümlenemedi: msdyn\_billingaccount.accountnumber. Arama bulunamadı: 1206-1. Referans verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Müşteri tablosunda **ContactPersonID** ve **InvoiceAccount** sütunlarında değerler bulunan satırlar varsa ilk eşitlemeyi tamamlamak için aşağıdaki adımları takip edin. Bu yaklaşımı, **Hesaplar** ve **İlgili kişiler** gibi kullanıma hazır tüm tablolar için kullanabilirsiniz.

1. Finans ve operasyon uygulamasında, **Müşteriler V3 (hesaplar)** eşlemesinden **ContactPersonID** ve **InvoiceAccount** sütunlarını silin ve eşlemeyi kaydedin.

    1. **Müşteriler V3 (hesaplar)** için çift yazma eşleme sayfasında, **Tablo eşlemeleri** sekmesinde, sol filtrede **finans ve operasyon uygulaması.Customers V3**'ü seçin. Sağ filtrede, **Dataverse.Firma**'yı seçin.
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
6. **Müşteriler V3 (Hesaplar)** eşlemesi için başlangıç eşitlemesini yeniden çalıştırın. Değişiklik izleme kapalı olduğundan, **InvoiceAccount** ve **ContactPersonId** verileri finans ve operasyon uygulamasından Dataverse'e eşitlenir.
7. **InvoiceAccount** ve **ContactPersonId** verilerini Dataverse'ten finans ve operasyon uygulamasına eşitlemek için bir veri tümleştirme projesi kullanmanız gerekir.

    1. Power Apps'te, **Satış.Hesabı** ve **finans ve operasyon uygulaması.Customers V3** tabloları arasında bir veri tümleştirme projesi oluşturun. Veri yönü Dataverse'ten finans ve operasyon uygulamasına doğru olmalıdır. **InvoiceAccount** çift yazmada yeni bir öznitelik olduğundan, bunun için ilk eşitlemeyi atlamak isteyebilirsiniz. Daha fazla bilgi için bkz. [Dataverse'e veri entegre edin](/power-platform/admin/data-integrator).

        Aşağıdaki resimde **CustomerAccount** ve **ContactPersonId**'yi güncelleştiren bir proje gösterilmektedir .

        ![CustomerAccount ve ContactPersonId alanını güncelleştirmek için veri tümleştirme projesi.](media/cust_selfref6.png)

    2. Şirket ölçütlerini Dataverse tarafındaki filtreye ekleyin, böylece finans ve operasyon uygulamasında yalnızca filtre ölçütleriyle eşleşen satırlar güncelleştirilir. Filtre eklemek için filtre düğmesini seçin. Ardından, **Sorguyu düzenle** iletişim kutusunda **\_msdyn\_company\_value eq '\<guid\>'** gibi bir filtre sorgusu ekleyebilirsiniz.

        > [NOT] Filtre düğmesi yoksa, veri tümleştirme ekibinin kiracınızda filtre yeteneğini etkinleştirmesini istemek için bir destek bileti oluşturun.

        **\_msdyn\_company\_value** için bir filtre sorgusu girmezseniz tüm satırlar eşitlenir.

        ![Filtre sorgusu ekleme.](media/cust_selfref7.png)

    Satırların ilk eşitlenme işlemi şimdi tamamlandı.

8. Finans ve operasyon uygulamasında, **Müşteriler V3** tablosu için değişiklik izlemeyi tekrar açın.

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

Finans ve operasyon uygulamalarında **DirPartyCDSEntity** üzerinde **Kişi** ve **Kuruluş** türündeki tarafları filtreleyen bir aralık kümesi vardır. Sonuç olarak, **CDS Tarafları – msdyn_parties** eşlemesinin ilk eşitlemesi, **Tüzel Kişilik** ve **Faaliyet Birimi** dahil olmak üzere diğer türdeki tarafları eşitlemez. İlk eşitleme **CDS Taraf posta adresleri (msdyn_partypostaladdresses)** veya **Taraf İlgili Kişileri V3 (msdyn_partyelectronicaddresses)** için çalıştığında bu hatayla karşılaşabilirsiniz.

Her türden tarafın Dataverse'e başarıyla eşitlenebilmesi için finans ve operasyon varlığındaki taraf türü aralığını kaldırmak için bir düzeltme üzerinde çalışıyoruz.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Müşteriler veya İlgili Kişiler verileri için ilk eşitlemeyi çalıştırırken herhangi bir performans sorunu yaşıyor musunuz?

**Müşteri** verileri için ilk eşitlemeyi çalıştırdıysanız ve **Müşteri** eşlemelerini çalıştırıp ardından da **İlgili Kişiler** verileri için ilk eşitlemeyi çalıştırırsanız **İlgili Kişi** adresleri için **LogisticsPostalAddress** ve **LogisticsElectronicAddress** tablolarına yapılan eklemeler ve güncelleştirmeler sırasında performans sorunlarıyla karşılaşabilirsiniz. Aynı genel posta adresi ve elektronik adres tabloları **CustCustomerV3Entity** ve **VendVendorV2Entity** için izlenir ve çift yazma, diğer tarafa veri yazmak için daha fazla sorgu oluşturmaya çalışır. **Müşteri** için ilk eşitlemeyi zaten çalıştırdıysanız **İlgili Kişiler** verileri için ilk eşitlemeyi çalıştırmadan önce ilgili eşlemeyi durdurun. **Satıcı** verileri için de aynısını yapın. İlk eşitleme tamamlandığında ilk eşitlemeyi atlayarak tüm eşlemeleri çalıştırabilirsiniz.

## <a name="float-data-type-that-has-a-zero-value-cant-be-synchronized"></a>Sıfır değerine sahip kayan noktalı veri türü eşitlenemiyor

**Sabit ödeme tutarı** veya hareket para birimindeki **Tutar** gibi fiyat alanlarında sıfır değerine sahip kayıtlar için ilk eşitleme başarısız olabilir. Bu durumda, aşağıdaki örneğe benzer bir hata iletisi alırsınız:

*Giriş parametreleri doğrulanırken hata oluştu: Microsoft.OData.ODataException: '000000' değişmez değeri 'Edm.Decimal' beklenen türüne dönüştürülemiyor,...*

Bu sorun, **Veri yönetimi** modülündeki **Kaynak veri biçimleri** altında bulunan **Dil yerel ayarları** işlevinden kaynaklanmaktadır. **Dil yerel ayarları** alanındaki değeri **en-us** olarak değiştirip tekrar deneyin.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

