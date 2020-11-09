---
title: Finance and Operations uygulamalarında çift yazma modülüyle ilgili sorunları giderme
description: Bu konu, Finance and Operations uygulamalardaki çift-yazma modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f99f3760e75ec1bbf2ccdea497cf2eec3e28e233
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997386"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Finance and Operations uygulamalarında çift yazma modülüyle ilgili sorunları giderme

[!include [banner](../../includes/banner.md)]

Bu konu, Finance and Operations uygulamaları ve Common Data Service arasında çift yazma tümleştirme hakkında sorun giderme bilgileri sağlar. Bu konu, Finance and Operations uygulamalardaki **çift-yazma** modülüyle ilgili sorunları çözmenize yardımcı olabilecek sorun giderme bilgileri sağlar.

> [!IMPORTANT]
> Bu konu adresiyle ilgili bazı sorunların sistem yöneticisi rolü veya Microsoft Azure Active Directory (Azure AD) kiracı yöneticisi kimlik bilgileri gerekebilir. Her konunun bölümünde belirli bir rol veya kimlik bilgilerinin gerekli olup olmadığı açıklanmaktadır.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Çift yazma modülü bir Finance and Operations uygulamaya yüklenemez

**Çift- yazılır** sayfayı, **veri yönetimi** çalışma alanında **ikili yazma** kutucuğunu seçerek açamazsınız, veri tümleştirme hizmeti büyük olasılıkla çalışmıyor olabilir. Veri tümleştirme hizmetinin yeniden başlatılmasını istemek için bir destek bileti oluşturun.

## <a name="error-when-you-try-to-create-a-new-entity-map"></a>Yeni bir varlık eşlemesi oluşturmaya çalıştığınızda hata oluştu

**Sorunu düzeltmek için gerekli kimlik bilgileri:** Çift yazma kurulumu yapan aynı kullanıcı.

Çift yazma için yeni bir varlık yapılandırmaya çalıştığınızda aşağıdaki hata iletisini alabilirsiniz. Eşleme oluşturabilecek tek kullanıcı, çift yazma bağlantısını kuran kullanıcıdır.

*Yanıt durum kodu başarıyı göstermiyor: 401 (yetkisiz)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>İkili yazma Kullanıcı arabirimini açtığınızda hata oluştu

**Veri yönetimi** çalışma alanından çift-yazılabilir erişmeye çalıştığınızda aşağıdaki hata iletisini alabilirsiniz:

*login.microsoftonline.com bağlanmayı reddetti.*

Sorunu gidermek için, Microsoft Edge'de bir InPrivate pencere, Chromium'da bir gizli penceresi veya Google Chrome 'da bir gizli penceresi kullanarak oturum açın. Ayrıca, üçüncü taraf tanımlama bilgilerini engellemeyi veya temizlemeniz gerekir.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Ortam ikili yazma için bağlantılandırma sırasında hata oluştu veya yeni bir varlık eşlemesi ekler

**Sorunu düzeltmek için gereken rol:** Hem Finance and Operations uygulamalarında hem de Common Data Service'ta sistem yöneticisi.

Haritaları bağlarken veya oluştururken aşağıdaki hata ile karşılaşabilirsiniz:

*Yanıt durum kodu başarı göstermiyor: 403 (tokenexchange).<br>Oturum kodu: \<your session id\><br> Kök etkinlik kimliği: \<your root activity id\>*

Bu hata, Çift-yazılabilir veya haritalar oluşturmak için yeterli izniniz yoksa oluşabilir. Bu hata, Common Data Service ortamı çift yazma bağlantısını kaldırmadan sıfırlanırsa da oluşabilir. Hem Finance and Operations uygulamaları hem de Common Data Service'ta sistem yöneticisi rolüne sahip herhangi bir kullanıcı ortamları bağlayabilir. Yalnızca çift yazma yazılır bağlantısını kuran kullanıcı yeni varlık eşlemeleri ekleyebilir. Kurulumdan sonra, sistem yöneticisi rolüne sahip tüm kullanıcılar durumu izleyebilir ve eşlemeleri düzenleyebilir.

## <a name="error-when-you-stop-the-entity-mapping"></a>Varlık eşlemesini durdurduğunuzda hata oluştu

Varlık eşlemelerini durdurmayı denediğinizde aşağıdaki hata iletisini alabilirsiniz:

*\[Yasak\], \[{"durum": 403, "kaynak": "", "mesaj": "belirteç değiş tokuşu nedeniyle hata: kullanıcının dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]bağlantısına erişmesine izin verilmiyor uzak sunucu hata verdi: (403) yasak.*

Bu hata, bağlı Common Data Service ortam kullanılabilir olmadığında oluşur.

Bu sorunu gidermek için, veri tümleştirme ekibi için bir bilet oluşturun. Veri tümleştirme ekibinin eşlemeleri arka uçta **çalışmıyor** olarak işaretlemesi için ağ izlemesini iliştirin.

## <a name="error-while-trying-to-start-an-entity-mapping"></a>Bir varlık eşlemesi başlatılmaya çalışılırken hata

Bir eşlemenin o durumunu **Çalıştırma** olarak ayarlamaya çalıştığınızda aşağıdakine benzer bir hata alabilirsiniz:

*İlk veri eşitlemesi tamamlanamıyor. Hata: Çift yazma hatası - eklenti kaydı başarısız oldu: Çift yazma arama meta verileri oluşturulamadı. Hata nesne başvurusu bir nesnenin örneğine ayarlanmadı.*

Bu hata için düzeltme hatanın nedenine bağlıdır:

+ Eşlemeye bağımlı eşlemeler varsa, bu varlık eşlemesinin bağımlı eşlemelerini etkinleştirdiğinizden emin olun.
+ Eşlemede kaynak veya hedef alanlar eksik olabilir. Finance and Operations uygulamalarında bir alan eksikse, [Eşlemelerde eksik varlık alanları sorunu](dual-write-troubleshooting-finops-upgrades.md#missing-entity-fields-issue-on-maps) bölümlerindeki adımları izleyin. Common Data Service'taki bir alan eksikse, alanların otomatik olarak eşlemeye geri doldurulması için eşlemede **Varlıkları yenile** düğmesine tıklayın.
