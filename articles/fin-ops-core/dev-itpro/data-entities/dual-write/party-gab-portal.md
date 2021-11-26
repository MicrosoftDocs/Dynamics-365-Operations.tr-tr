---
title: Microsoft Power Apps portallarını Taraf veri modeliyle kullanma
description: Bu konuda, çift yazmadaki taraf veri modeli nedeniyle Microsoft Power Apps portalları için web rollerinde yapılan değişiklikler açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 872b477ae73a374cd62b9e86048bfc27c84064c1
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781380"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>Microsoft Power Apps portallarını Taraf veri modeliyle kullanma

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Çift yazma uygulama düzenleme çözümü sürüm 2.0.999.0 ve sonraki sürümleri, Hesap ve İlgili kişi tabloları için tarafta ve genel adres defterindeki veri modeli değişikliklerini içerir. Değişiklikler, gelişmiş iş senaryolarını destekleyen çok-çok ilişkisi sağlar. Bu değişiklikler, müşteri portalı dahil, kullanıma hazır veya çift yazma yüklenmeden önce ortamınızda varolan portal web rolleri tarafından desteklenmez. Web rollerinin beklendiği gibi çalışması için yeni veri modelini kullanarak yeni web rolleri oluşturmanız gerekir. 

Özetle, tabloların etkileşim şekli değişti, ancak müşteri portalındaki tablo izinleri değişmedi. Bu konu, yeni gelişmiş veri modeliyle çalışan yeni Web rollerinin nasıl oluşturulacağını açıklamaktadır.

Bu diyagram, taraf ve genel adres defteri veri modeli **olmadan** tablo ilişkisini gösterir:

   ![taraf modeli olmadan.](media/without-party-model.PNG)

Bu diyagram, taraf ve genel adres defteri veri modeli **ile birlikte** tablo ilişkisini gösterir:

   ![taraf modeli ile birlikte.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Yeni tablo izni oluşturma

Bu yeni tablo izinlerini oluşturmak için şu adımları izleyin:

1. [Power Apps](https://make.powerapps.com)'te oturum açın ve uygulamalarınıza gidin.
2. Portal yönetimi uygulamanızı seçin.
3. Yan çubukta **güvenlik > tablo izinlerini** seçin.

    Üç yeni izin oluşturmalısınız:

    + **İlgili Kişi** ile **Taraf** tablo bağlantısı
    + **Taraf** ile **Hesap** tablo bağlantısı
    + **Hesap** ile **Sipariş** tablo bağlantısı

4. Şu parameteleri ayarlayarak İlgili kişi - taraf bağlantısı için yeni bir izin oluştup Kaydedin:

    + **Ad**: **Taraf** ile **Hesap** tablo bağlantısı (veya seçiminiz)
    + **Tablo adı**: msdyn_contactforparty
    + **Web sitesi**: Müşteri Portalı
    + **Kapsam**: İlgili kişi
    + **Ayrıcalıklar**: Tümünü Seç
    + **Web rolleri**: Kimliği doğrulanmış kullanıcılar, müşteri temsilcisi (veya seçiminiz)

5. Şu parameteleri ayarlayarak Taraf - Hesap bağlantısı için yeni bir izin oluştup Kaydedin:

    + **Ad**: Taraf - hesap bağlantısı (veya sizin seçiminiz)
    + **Tablo adı**: hesap
    + **Web sitesi**: Müşteri Portalı
    + **Kapsam**: üst
    + **Ayrıcalıklar**: Tümünü Seç
    + **Üst tablo izni**: İlgili kişi - Taraf bağlantısı

6. Şu parameteleri ayarlayarak Hesap - Sipariş bağlantısı için yeni bir izin oluştup Kaydedin:

    + **Ad**: Hesap - Sipariş bağlantısı (veya sizin seçiminiz)
    + **Tablo adı**: salesorder
    + **Web sitesi**: Müşteri Portalı
    + **Kapsam**: üst
    + **Ayrıcalıklar**: Tümünü Seç
    + **Üst tablo izni**: Taraf - Hesap bağlantısı

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
