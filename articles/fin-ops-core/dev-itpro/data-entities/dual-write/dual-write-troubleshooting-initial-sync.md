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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172726"
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

## <a name="self-reference-failures-during-initial-synchronization"></a>İlk eşitleme sırasında kendi kendine referans hataları

Eşlemelerinizin kendi kendine referansları varsa, aşağıdaki örneğe benzer bir hata iletisi alabilirsiniz:

*Satıcılar sürüm 2'de aşağıdaki hata: kayıt kodu: yeni kayıt, ErrorMessage: alan için GUID çözülemedi: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Arama değeri bulunamadı: CN-001. Başvuru verilerinin var olup olmadığını denetlemek için bu URL 'yi deneyin: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber`  eq 'CN-001'*

Bu tür bir hata, kendi kendine referansları olan eşlemelerin ilk eşitlemesi sırasında oluşur. Önceki örnekte, fatura hesabı alanı satıcı varlığına referans gösterir.

Sorunu gidermek için, ilk eşitleme başarılı olmadan eşlemeyi iki kez çalıştırmanız gerekebilir.

