---
title: Finans ve operasyon uygulamalarında çift yazma ile ilgili sorunları giderme
description: Bu makalede, finans ve operasyon uygulamalarındaki çift yazma modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlanmaktadır.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 5678cd38e48eb5226e36851679436d3b6c117cf9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289589"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Finans ve operasyon uygulamalarında çift yazma ile ilgili sorunları giderme

[!include [banner](../../includes/banner.md)]



Bu makalede, finans ve operasyon uygulamaları ile Dataverse arasında çift yazma tümleştirmesi hakkında sorun giderme bilgileri sağlanmaktadır. Bu konu, finans ve operasyon uygulamalarındaki **Çift Yazma** modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.

> [!IMPORTANT]
> Bu makalede ele alınan bazı sorunlar için sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Finans ve operasyon uygulamasında çift yazma modülü yüklenemiyor

**Çift- yazılır** sayfayı, **veri yönetimi** çalışma alanında **ikili yazma** kutucuğunu seçerek açamazsınız, veri tümleştirme hizmeti büyük olasılıkla çalışmıyor olabilir. Veri tümleştirme hizmetinin yeniden başlatılmasını istemek için bir destek bileti oluşturun.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Yeni bir tablo eşlemesi oluşturmaya çalıştığınızda hata oluştu

**Sorunu düzeltmek için gerekli kimlik bilgileri:** Çift yazma kurulumu yapan aynı kullanıcı.

Çift yazma için yeni bir tablo yapılandırmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz. Eşleme oluşturabilecek tek kullanıcı, çift yazma bağlantısını kuran kullanıcıdır.

*Yanıt durum kodu başarıyı göstermiyor: 401 (Yetkisiz).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>İkili yazma Kullanıcı arabirimini açtığınızda hata oluştu

**Veri yönetimi** çalışma alanından çift-yazılabilir erişmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*login.microsoftonline.com bağlanmayı reddetti.*

Sorunu gidermek için, Microsoft Edge'de bir InPrivate pencere, Chromium'da bir gizli penceresi veya Google Chrome 'da bir gizli penceresi kullanarak oturum açın. Ayrıca, üçüncü taraf tanımlama bilgilerini engellemeyi veya temizlemeniz gerekir.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Çift yazma için ortam bağladığınızda veya yeni bir tablo eşlemesi eklediğinizde hata oluştu

**Sorunu düzeltmek için gereken rol:** Finans ve operasyon uygulamaları ve Dataverse'te sistem yöneticisi.

Haritaları bağlarken veya oluştururken aşağıdaki hata ile karşılaşabilirsiniz:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Bu hata, Çift-yazılabilir veya haritalar oluşturmak için yeterli izniniz yoksa oluşabilir. Bu hata, Dataverse ortamı çift yazma bağlantısını kaldırmadan sıfırlanırsa da oluşabilir. Hem finans ve operasyon uygulamaları hem de Dataverse'te sistem yöneticisi rolüne sahip herhangi bir kullanıcı ortamları bağlayabilir. Yalnızca çift yazma bağlantısını kuran kullanıcı yeni tablo eşlemeleri ekleyebilir. Kurulumdan sonra, sistem yöneticisi rolüne sahip tüm kullanıcılar durumu izleyebilir ve eşlemeleri düzenleyebilir.

## <a name="error-when-you-stop-the-table-mapping"></a>Tablo eşlemesini durdurduğunuzda hata oluştu

Tablo eşlemelerini durdurmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*\[Yasak\], \[{"durum": 403, "kaynak": "", "mesaj": "belirteç değiş tokuşu nedeniyle hata: kullanıcının dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]bağlantısına erişmesine izin verilmiyor uzak sunucu hata verdi: (403) yasak.*

Bu hata, bağlı Dataverse ortam kullanılabilir olmadığında oluşur.

Bu sorunu gidermek için, veri tümleştirme ekibi için bir bilet oluşturun. Veri tümleştirme ekibinin eşlemeleri arka uçta **çalışmıyor** olarak işaretlemesi için ağ izlemesini iliştirin.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Performansı artırmak için finans ve operasyon uygulamalarında paralel işlemeyi etkinleştirme

Paralel işlemeyi etkinleştirmek, Dynamics 365 Customer Engagement uygulamaları ve Microsoft Dataverse'den finans ve operasyon uygulamalarına veri aktarmak için gereken süreyi azaltabilir. 

Finans ve operasyon uygulamalarında paralel işlemeyi etkinleştirmek için aşağıdaki adımları tamamlayın.

1. Finans ve operasyon ortamınızda oturum açın.
2. **Veri yönetimi > Çerçeve parametreleri**'ne gidin.
3. **Varlık ayarları**'nı ve **Varlık yürütme parametrelerini yapılandır**'ı seçin.
4. Paralel işleme parametrelerini ekleyin:
    - **İçe aktarma eşiği kayıt sayısı** – Paralel işleme etkinleştirilmeden önce karşılanması gereken kayıt sayısı.
    - **İçe aktarma görev sayısı** – Paralel olarak çalıştırılacak iş parçacıklarının (görevler) sayısı.
5. **Kaydet**'i seçin.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Tablo eşlemesi başlatılmaya çalışılırken hatalar oluştu

### <a name="unable-to-complete-initial-data-sync"></a>İlk veri eşitlemesi tamamlanamıyor

İlk veri eşitlemesini çalıştırmayı denediğinizde aşağıdakine benzer bir hatayla karşılaşabilirsiniz:

*İlk veri eşitlemesi tamamlanamıyor. Hata: Çift yazma hatası - eklenti kaydı başarısız oldu: Çift yazma arama meta verileri oluşturulamadı. Hata nesne başvurusu bir nesnenin örneğine ayarlanmadı.*

Eşlemenin bu durumunu **Çalışıyor** olarak ayarlamak istediğinizde bu hatayı alabilirsiniz. Düzeltme, hatanın nedenine bağlıdır:

+ Eşlemeye bağımlı eşlemeler varsa bu tablo eşlemesinin bağımlı eşlemelerini etkinleştirdiğinizden emin olun.
+ Eşlemede kaynak veya hedef sütunlar eksik olabilir. Finans ve operasyon uygulamasında bir sütun eksikse, [Eşlemelerde eksik tablo sütunları sorunu](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) bölümündeki adımları izleyin. Dataverse'teki bir sütun eksikse sütunların otomatik olarak eşlemede geri doldurulması için eşlemede **Tabloları yenile** düğmesine tıklayın.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Sürüm uyuşmazlığı hatası ve çift yazma çözümlerini yükseltme

Tablo eşlemelerini çalıştırmayı denediğinizde aşağıdaki hata iletilerini alabilirsiniz:

+ *Müşteri grupları (msdyn_customergroups): Çift yazma hatası - "Dynamics365Company" Dynamics 365 for Sales çözümünde sürüm uyuşmazlığı var. Sürüm: "2.0.2.10" Gerekli sürüm: "2.0.133"*
+ *"Dynamics365FinanceExtended" Dynamics 365 for Sales çözümünde sürüm uyuşmazlığı var. Sürüm: "1.0.0.0" Gerekli sürüm: "2.0.227"*
+ *"Dynamics365FinanceAndOperationsCommon" Dynamics 365 for Sales çözümünde sürüm uyuşmazlığı var. Sürüm: "1.0.0.0" Gerekli sürüm: "2.0.133"*
+ *"CurrencyExchangeRates" Dynamics 365 for Sales çözümünde sürüm uyuşmazlığı var. Sürüm: "1.0.0.0" Gerekli sürüm: "2.0.133"*
+ *"Dynamics365SupplyChainExtended" Dynamics 365 for Sales çözümünde sürüm uyuşmazlığı var. Sürüm: "1.0.0.0" Gerekli sürüm: "2.0.227"*

Sorunları gidermek için Dataverse uygulamasındaki çift yazma çözümlerini güncelleştirin. Gerekli çözüm sürümüyle eşleşen en son çözüme yükseltmeyi yaptığınızdan emin olun.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

