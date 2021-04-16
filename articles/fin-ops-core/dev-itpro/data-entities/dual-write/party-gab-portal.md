---
title: Taraf veri modeli ile Power Portal'ı kullanma
description: Bu konu, Çift yazma taraf veri modeli nedeniyle Power Portal Web rollerine yapılan değişiklikleri açıklamaktadır.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833102"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Taraf veri modeli ile Power Portal'ı kullanma

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Çift yazma uygulama düzenleme çözümü sürüm 2.0.999.0 ve sonraki sürümleri, Hesap ve İlgili kişi tabloları için tarafta ve genel adres defterindeki veri modeli değişikliklerini içerir. Değişiklikler, gelişmiş iş senaryolarını destekleyen çok-çok ilişkisi sağlar. Bu değişiklikler, müşteri portalı dahil, kullanıma hazır veya çift yazma yüklenmeden önce ortamınızda varolan portal web rolleri tarafından desteklenmez. Web rollerinin beklendiği gibi çalışması için yeni veri modelini kullanarak yeni Web rolleri oluşturmanız gerekir. 

Özetle, tabloların etkileşim şekli değişti, ancak müşteri portalındaki tablo izinleri değişmedi. Bu konu, yeni gelişmiş veri modeliyle çalışan yeni Web rollerinin nasıl oluşturulacağını açıklamaktadır.

Bu diyagram, taraf ve genel adres defteri veri modeli **olmadan** tablo ilişkisini gösterir:

   ![Taraf modeli olmadan](media/without-party-model.PNG)

Bu diyagram, taraf ve genel adres defteri veri modeli **ile birlikte** tablo ilişkisini gösterir:

   ![Taraf modeli ile birlikte](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Yeni tablo izni oluşturma

Bu yeni tablo izinlerini oluşturmak için şu adımları izleyin:

1. [Power Apps](https://make.powerapps.com)'te oturum açın ve uygulamalarınıza gidin.
2. Portal yönetimi uygulamanızı seçin.
3. Yan çubukta **güvenlik > tablo izinlerini** seçin.

    Üç yeni izin oluşturmalısınız:

    + İlgili kişi - Taraf bağlantısı
    + Taraf - Hesap bağlantısı
    + Hesap - Sipariş bağlantısı

4. Şu parameteleri ayarlayarak İlgili kişi - taraf bağlantısı için yeni bir izin oluştup Kaydedin:

    + **Ad**: Taraf - hesap bağlantısı (veya sizin seçiminiz)
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
