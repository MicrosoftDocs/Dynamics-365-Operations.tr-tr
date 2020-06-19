---
title: Başlangıç eşitlemesi sırasında sorunları giderme
description: Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410093"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Başlangıç eşitlemesi sırasında sorunları giderme

[!include [banner](../../includes/banner.md)]

Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, ilk eşitlemede olabilecek sorunları çözmenize yardımcı olabilecek bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finance and Operations uygulamadaki ilk eşitleme hatalarını denetle

Eşleme şablonları etkinleştirildikten sonra, haritaların durumu **çalışıyor** olmalıdır. Durum **çalışmıyorsa**, ilk eşitleme sırasında hata meydana geldi. Hataları görüntülemek için **çift-yazma** sayfasında **ilk eşitleme ayrıntıları** sekmesini seçin.

![İlk eşitleme Ayrıntıları sekmesi](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>İlk eşitlemeyi tamamlayamıyoruz: 400 Hatalı Istek

**Sorunu düzeltmek için gerekli rol:** Sistem Yöneticisi

Eşlemeyi ve ilk senkronizasyonu çalıştırmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*Uzak sunucu hata verdi: (400) hatalı Istek.), AX dışarı aktarma bir hatayla karşılaştı*

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

![Azure AD uygulamalar listesi](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>İlk eşitleme sırasında kendi kendine referans veya döngüsel referans hataları

Eşlemelerinizin kendi kendine veya çevresel referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz: Hatalar aşağıdaki kategorilere ayrılır:

- [Satıcılar V2 ve msdyn_vendors varlık eşlemesi](#error-vendor-map)
- [Müşteriler V3 ile Firmalar varlık eşlemesi](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Varlık eşleştirmesini msdyn_vendors üzere Satıcılar V2'deki bir hatayı giderme

Varlıkların, **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarında değerleri bulunan mevcut kayıtları varsa **msdyn_vendors** eşlemeyi yapmak için **satıcı v2** üzerinde aşağıdaki ilk eşitleme hatalarını kullanabilirsiniz. Bu **InvoiceVendorAccountNumber**, kendine referans bir alan olduğundan ve **PrimaryContactPersonId** satıcı eşlemesindeki bir döngüsel başvurudur.

*Alan için GUID çözümlenemedi:<field>. Arama bulunamadı: <value>Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

İşte birkaç örnek:

- *Şu alan için GUID çözülemedi: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Şu alan için GUID çözülemedi: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Arama bulunamadı: V24-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Satıcı varlığındaki bu alanlardaki değerleri bulunan kayıtlarınız varsa, ilk eşitlemeyi başarıyla tamamlamak için aşağıdaki adımları takip edin.

1. Finance and Operations uygulamada, eşlemeden önce **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarını silin ve değişiklikleri kaydedin.

    1. Satıcılar v2 (msdyn_vendors) için ikili yazma eşleme sayfasına gidin **Vendors V2 (msdyn_vendors)** ve **varlık eşleştirmeleri** sekmesini seçin. Sol filtrede, **Finance and Operations uygulamaları. Satıcıları sürüm 2** seçin. Sağ filtrede, **Sales.Vendor**'u seçin.

    2. **primarycontactperson**'ı arayıp **PrimaryContactPersonId** kaynak alanını bulur .
    
    3. **Eylemler** düğmesine tıklayın ve **Sil**'i seçin.
    
        ![kendinden veya dairesel referans 3](media/vend_selfref3.png)
    
    4. **InvoiceVendorAccountNumber** alanını silmek için tekrarlayın .
    
        ![kendinden veya dairesel referans 4](media/vend-selfref4.png)
    
    5. Eşleme değişikliklerini kaydedin.

2. **Vendors V2** varlığı için değişiklik izlemeyi devre dışı bırakın .

    1. **Veri yönetimi \> veri varlıklarına** gidin .
    
    2. **Satıcılar V2** tüzel kişiliğini seçin.
    
    3. Menü çubuğundan **seçenekler**'i tıklatın ve sonra **izlemeyi değiştirin**.
    
        ![kendinden veya dairesel referans 5](media/selfref_options.png)
    
    4. **Değişiklik izlemeyi devre dışı bırak**'ı tıklayın.
    
        ![kendinden veya dairesel referans 6](media/selfref_tracking.png)

3. **Satıcı v2 (msdyn_vendors)** eşlemesinin ilk eşitlemesini çalıştırın . İlk eşitleme hatasız olarak çalışmalıdır.

4. **CD kişilerinin v2 (kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın . İlgili kişi kayıtlarının de ilk eşitlenmesi gerektiğinde, satıcı varlığındaki birincil ilgili kişi alanını eşitlemek istiyorsanız bu eşlemeyi eşitlemeniz gerekir.

5. **PrimaryContactPersonId** ve **InvoiceVendorAccountNumber** alanlarını **satıcı v2 (msdyn_vendors)** eşleme alanlarına geri ekleyin ve eşlemeyi kaydedin.

6. **Satıcı v2 (msdyn_vendors)** eşlemesinin ilk eşitlemesini çalıştırın . Değişiklik izleme devre dışı bırakıldığından tüm kayıtlar eşitlenecek.

7. **Vendors V2** varlığı için değişiklik izlemeyi etkinleştirin.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Müşteriler V3 ile Firmalar varlık eşleme müşterilerine hata giderme

Varlıkların, **ContactPersonID** ve **InvoiceAccount** alanlarında değerleri bulunan mevcut kayıtları varsa **Firmalar** eşlemeyi yapmak için **Müşteriler v3** üzerinde aşağıdaki ilk eşitleme hatalarını kullanabilirsiniz. Bu **InvoiceAccount**, kendine referans bir alan olduğundan ve **ContactPersonID** satıcı eşlemesindeki bir döngüsel başvurudur.

*Alan için GUID çözümlenemedi:<field>. Arama bulunamadı: <value>Başvuru verilerinin var olup olmadığını denetlemek için bu URL'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Şu alan için GUID çözülemedi: primarycontactid.msdyn_contactpersonid. Arama bulunamadı: 000056. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Şu alan için GUID çözülemedi: msdyn_billingaccount.accountnumber. Arama bulunamadı: 1206-1. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Müşteri varlığındaki bu alanlardaki değerleri bulunan kayıtlarınız varsa, ilk eşitlemeyi başarıyla tamamlamak için aşağıdaki adımları takip edin. Bu yaklaşımı, firma ve Ilgili kişiler gibi, kutudan çıkan herhangi bir varlık için kullanabilirsiniz.

1. Finance and Operations uygulamada, **Müşteriler V3 (firmalar)** eşlemesinden önce **ContactPersonID** ve **InvoiceAccount** alanlarını silin ve değişiklikleri kaydedin.

    1. **Müşteriler V3 (firmalar)** için ikili yazma eşleme sayfasına gidin, **varlık eşleştirmeleri** sekmesini seçin. Sol filtrede, **Finance and Operations uygulamaları.Müşteriler sürüm 2** seçin. Sağ filtrede, **Common Data Service.Firma**'yı seçin.

    2. **contactperson**'ı arayıp **ContactPersonID** kaynak alanını bulur .
    
    3. **Eylemler** düğmesine tıklayın ve **Sil**'i seçin.
    
        ![kendinden veya dairesel referans 3](media/cust_selfref3.png)
    
    4. **InvoiceAccount** alanını silmek için tekrarlayın .
    
        ![kendinden veya dairesel referans](media/cust_selfref4.png)
    
    5. Eşleme değişikliklerini kaydedin.

2. **Müşteriler V3** varlığı için değişiklik izlemeyi devre dışı bırakın .

    1. **Veri yönetimi \> veri varlıklarına** gidin .
    
    2. **Müşteriler V3** tüzel kişiliğini seçin.
    
    3. Menü çubuğundan **seçenekler**'i tıklatın ve sonra **izlemeyi değiştirin**.
    
        ![kendinden veya dairesel referans 5](media/selfref_options.png)
    
    4. **Değişiklik izlemeyi devre dışı bırak**'ı tıklayın.
    
        ![kendinden veya dairesel referans 6](media/selfref_tracking.png)

3. **Müşteriler V3 (Firmalar)** eşlemesi için başlangıç eşitlemesini çalıştırın . İlk eşitleme hatasız olarak çalışmalıdır.

4. **CD kişilerinin v2 (kişiler)** eşlemesi için başlangıç eşitlemesini çalıştırın . Aynı adda 2 eşleme var. **FO.CDS Vendor Contacts V2 ve CDS.Contacts arasında eşitleme için çift yazma şablonu. yeni paket gerekli \[Dynamics365SupplyChainExtended\].** açıklaması olanı seçin. Haritanın **Ayrıntılar** sekmesinde yapın.

5. **Müşteriler V3 (firmalar)** eşlemesinden önce **ContactPersonID** ve **InvoiceAccount** alanlarını silin ve değişiklikleri kaydedin. Şimdi, hem **InvoiceAccount** alanını hem de **ContactPersonId** alanı canlı eşitleme modunun parçası olarak kullanılır. Sonraki adımda, bu alanlar için başlangıç eşitlemesini tamamdınız.

6. **Müşteriler V3 (Firmalar)** eşlemesi için başlangıç eşitlemesini çalıştırın . Değişiklik izleme devre dışı bırakıldığından, Finance and Operations uygulamasından Common Data Service'e eşitleme çalıştırmak **InvoiceAccount** ve **ContactPersonId** verilerini uygulamadan eşitler.

7. **InvoiceAccount** ve **ContactPersonId** için verileri Common Data Service'dan Finance and Operations'a eşitlemek için bir veri tümleştirme projesi kullanırsınız.

    1. Power Apps içinde , **Satış. firma** ve **Finance and Operations uygulamalar.Müşteriler V3** varlıkları arasında veri entegrasyonu projesi oluşturunuygulamalar arasında bir veri tümleştirme projesi oluşturun. Veri yönü, Common Data Service'ten Finance and Operations uygulamasına olmalıdır.  **InvoiceAccount** çift-yazılabilir olarak yeni bir öznitelik olduğundan, bu öznitelik için ilk eşitlemeyi atlamak isteyebilirsiniz. Daha fazla bilgi için bkz. [Common Data Service'e veri entegre edin](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Aşağıdaki resimde **CustomerAccount** ve **ContactPersonId**'yi güncelleştiren bir proje gösterilmektedir .

        ![kendinden veya dairesel referans](media/cust_selfref6.png)

    2. Finance and Operations Uygulamasında, filtre ölçütleriyle eşleşen kayıtlar güncelleştirilecek şekilde şirket ölçütlerini Common Data Service kenarına ekleyin. Filtre eklemek için filtre simgesini tıklatın. **Sorgu düzenle** iletişim kutusunda, **_msdyn_company_value eq '\<guid\>** gibi bir filtre sorgusu ekleyebilirsiniz . Filtre simgesi yoksa, veri tümleştirme ekibinin kiracınızda filtre yeteneğini etkinleştirmesini istemek için bir destek bileti oluşturun. **_Msdyn_company_value** için bir filtre sorgusu girmezseniz , tüm kayıtlar eşitlenir.

        ![kendinden veya dairesel referans](media/cust_selfref7.png)

        Böylece, kayıtların ilk eşitlenmesi tamamlanır.

8. Finance and Operations uygulamasında **Müşteriler V3** varlığı için değişiklik izlemeyi etkinleştirin.

