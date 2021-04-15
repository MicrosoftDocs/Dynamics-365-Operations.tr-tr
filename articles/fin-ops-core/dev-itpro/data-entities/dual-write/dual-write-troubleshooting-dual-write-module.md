---
title: Finance and Operations uygulamalarında çift yazma sorunlarını giderme
description: Bu konu, Finance and Operations uygulamalardaki çift-yazma modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 46f561d3cddf1a94ff71e284e8085ff86d678600
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754074"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Finance and Operations uygulamalarında çift yazma sorunlarını giderme

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, Finance and Operations uygulamaları ve Dataverse arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, Finance and Operations uygulamalardaki **çift-yazma** modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Çift yazma modülü bir Finance and Operations uygulamaya yüklenemez

**Çift- yazılır** sayfayı, **veri yönetimi** çalışma alanında **ikili yazma** kutucuğunu seçerek açamazsınız, veri tümleştirme hizmeti büyük olasılıkla çalışmıyor olabilir. Veri tümleştirme hizmetinin yeniden başlatılmasını istemek için bir destek bileti oluşturun.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Yeni bir tablo eşlemesi oluşturmaya çalıştığınızda hata oluştu

**Sorunu düzeltmek için gerekli kimlik bilgileri:** Çift yazma kurulumu yapan aynı kullanıcı.

Çift yazma için yeni bir tablo yapılandırmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz. Eşleme oluşturabilecek tek kullanıcı, çift yazma bağlantısını kuran kullanıcıdır.

*Yanıt durum kodu başarıyı göstermiyor: 401 (yetkisiz)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>İkili yazma Kullanıcı arabirimini açtığınızda hata oluştu

**Veri yönetimi** çalışma alanından çift-yazılabilir erişmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*login.microsoftonline.com bağlanmayı reddetti.*

Sorunu gidermek için, Microsoft Edge'de bir InPrivate pencere, Chromium'da bir gizli penceresi veya Google Chrome 'da bir gizli penceresi kullanarak oturum açın. Ayrıca, üçüncü taraf tanımlama bilgilerini engellemeyi veya temizlemeniz gerekir.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Çift yazma için ortam bağladığınızda veya yeni bir tablo eşlemesi eklediğinizde hata oluştu

**Sorunu düzeltmek için gereken rol:** Hem Finance and Operations uygulamalarında hem de Dataverse'ta sistem yöneticisi.

Haritaları bağlarken veya oluştururken aşağıdaki hata ile karşılaşabilirsiniz:

*Yanıt durum kodu başarı göstermiyor: 403 (tokenexchange).<br>Oturum kodu: \<your session id\><br> Kök etkinlik kimliği: \<your root activity id\>*

Bu hata, Çift-yazılabilir veya haritalar oluşturmak için yeterli izniniz yoksa oluşabilir. Bu hata, Dataverse ortamı çift yazma bağlantısını kaldırmadan sıfırlanırsa da oluşabilir. Hem Finance and Operations uygulamaları hem de Dataverse'ta sistem yöneticisi rolüne sahip herhangi bir kullanıcı ortamları bağlayabilir. Yalnızca çift yazma bağlantısını kuran kullanıcı yeni tablo eşlemeleri ekleyebilir. Kurulumdan sonra, sistem yöneticisi rolüne sahip tüm kullanıcılar durumu izleyebilir ve eşlemeleri düzenleyebilir.

## <a name="error-when-you-stop-the-table-mapping"></a>Tablo eşlemesini durdurduğunuzda hata oluştu

Tablo eşlemelerini durdurmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*\[Yasak\], \[{"durum": 403, "kaynak": "", "mesaj": "belirteç değiş tokuşu nedeniyle hata: kullanıcının dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]bağlantısına erişmesine izin verilmiyor uzak sunucu hata verdi: (403) yasak.*

Bu hata, bağlı Dataverse ortam kullanılabilir olmadığında oluşur.

Bu sorunu gidermek için, veri tümleştirme ekibi için bir bilet oluşturun. Veri tümleştirme ekibinin eşlemeleri arka uçta **çalışmıyor** olarak işaretlemesi için ağ izlemesini iliştirin.

## <a name="error-while-trying-to-start-a-table-mapping"></a>Bir tablo eşlemesi başlatılmaya çalışılırken hata oluştu

Bir eşlemenin o durumunu **Çalıştırma** olarak ayarlamaya çalıştığınızda aşağıdakine benzer bir hata alabilirsiniz:

*İlk veri eşitlemesi tamamlanamıyor. Hata: Çift yazma hatası - eklenti kaydı başarısız oldu: Çift yazma arama meta verileri oluşturulamadı. Hata nesne başvurusu bir nesnenin örneğine ayarlanmadı.*

Bu hata için düzeltme hatanın nedenine bağlıdır:

+ Eşlemeye bağımlı eşlemeler varsa bu tablo eşlemesinin bağımlı eşlemelerini etkinleştirdiğinizden emin olun.
+ Eşlemede kaynak veya hedef sütunlar eksik olabilir. Finance and Operations uygulamalarında bir sütun eksikse, [Eşlemelerde eksik tablo sütunları sorunu](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps) bölümündeki adımları izleyin. Dataverse'teki bir sütun eksikse sütunların otomatik olarak eşlemede geri doldurulması için eşlemede **Tabloları yenile** düğmesine tıklayın.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]