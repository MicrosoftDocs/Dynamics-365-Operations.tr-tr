---
title: Perakende kanallarını tanımla ve koru
description: Bu konu, Dynamics 365 Commerce'da mağazalar olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir. Makalede, mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057926"
---
# <a name="define-and-maintain-retail-channels"></a>Perakende kanallarını tanımlama ve koruma

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce'da mağazalar olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir. Makalede, mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.

Commerce, çevrimiçi mağazalar, çağrı merkezleri ve fiziki mağazalar gibi birden fazla kanalı destekler. Geleneksel bir mağazaya mağaza adı verilir. Her mağazanın kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir. Bir mağaza oluşturmadan önce tüm bu öğeleri ayarlamanız gerekir. Mağaza oluşturduktan sonra gerçekleştirmek istediğiniz ürünleri atarsınız. Ayrıca mağazaya çalışanlar, kasalar ve müşteriler atarsınız. Son olarak, yeni mağazayı bir organizasyon hiyerarşisine eklersiniz.

## <a name="setting-up-stores"></a>Mağazaları ayarlama

Commerce'te bir perakende mağaza kurmadan önce bazı önkoşul görevleri tamamlamanız gerekir. Bundan sonra mağazayı oluşturabilir ve ayrıntılar ekleyebilirsiniz.

### <a name="prerequisites"></a>Önkoşullar

Bir mağaza kurmadan önce aşağıdaki görevleri tamamlamanız gerekir:

1. Organizasyon yapınızı yapılandırın ve perakende sınıflamalar, stok yenileme ve raporlama için kuruluş hiyerarşilerini ayarlayın.
2. Mağazayı temsil eden bir ambar ayarlayın.
3. Mağazalar, mağaza ekstreleri ve ekstre fişleri için numara sıraları ayarlayın.
4. Commerce için parametreleri yapılandırın.
5. Mağazanın kabul ettiği ödeme yöntemleri ayarlayın.
6. POS kasalarında kredi kartı işlemleri yürütmek için, ödeme hizmetleri de ayarlayabilirsiniz.
7. Satış vergisi gruplarını ayarla.
8. Ürünlerini ayarlayn. Bu görevin bir parçası olarak, ayrıca ürün hiyerarşileri, ürün çeşitleri ve ürün sınıflamaları ayarlayın.
9. Ürün fiyat gruplarını ayarlayın.
10. Ürün fiyatlandırmalarını ayarlayın. Bu görevin bir parçası olarak, aynı zamanda fiyat ayarlamaları, iskontolar ve iskonto dönemlerini ayarlayın.
11. Personeli ayarlayın.

    > [!NOTE]
    > POS sistemini kullanarak görevleri yürütebilmeleri için, çalışanlara uygun izinleri de atamanız gerekir.

12. Mağazaya atanacak POS profillerini yapılandırın. Bu görev kayıtları ayarlamak, çevrimdışı profilleri ayarlamak ve makbuz biçimleri ve profilleri ayarlamak gibi birçok diğer görevi içerir.

Önkoşullara dahil edilen tüm görevleri gözden geçirin ve yalnızca sizin için geçerli görevleri tamamlayın.

### <a name="set-up-a-store"></a>Mağaza ayarlama

Önkoşul görevlerini tamamladıktan sonra mağaza ayrıntılarını ayarlamak için aşağıdaki görevleri tamamlayın:

1. Bir mağaza oluşturun.
2. Mağazaya bir satış vergisi grubu atayın.
3. Çevrimiçi mağaza tarafından kabul edilen ödeme yöntemleri atayın.
4. Mağazada sunduğunuz ürünler için ürün açıklamalarına ayrıntılar ekleyin. Örneğin, zengin metin ve resimler ekleyebilirsiniz. Bu ürün ayrıntıları çeşitli bağlamlarda POS kasası veya yazdırılan etiketlerde görünür.
5. **Perakende sınıflama**, **Perakende stok yenileme**, veya **Perakende raporlama** amacıyla mağazayı varsayılan kuruluş hiyerarşisine ekleyin.

### <a name="after-you-set-up-a-store"></a>Mağaza kurduktan sonra

Mağaza için ayrıntıları girdikten sonra, yeni mağaza verilerini POS'a göndermek için şu görevleri tamamlayın:

1. Mağaza için POS kasalarını yapılandırın.
2. Mağazaya ürün çeşitleri atayın.
3. Sınıflama içinde bulunan ürün listesini oluşturmak ve ürünleri mağazada erişilebilir hale getirmek için sınıflamaları işleyin.
4. Numara serileri, donanım profilleri ve POS ekran düzeni gibi verileri POS kasalarına gönderin.
5. POS'a mağaza verilerini göndermek için mağazayı yayımlayın.
6. POS'a mağaza verilerini göndermek için işleri çalıştırın.

## <a name="organization-hierarchies"></a>Kuruluş hiyerarşileri

Commerce, kanalları yapılandırmak için kuruluş hiyerarşilerini kullanır. Organizasyon hiyerarşileri, organizasyonlar arasındaki işinizi meydana getiren ilişkileri temsil eder. Mağazalar kurduğunuzda, onları bir organizasyon hiyerarşisine ekleyebilirsiniz. Ardından mağazalar ürün çeşitleri, stok yenileme ve raporlama için kullanılan verileri paylaşır.

> [!NOTE]
> Commerce satış işlevlerini kullanabilmeniz için **çoklu sevk edilecek** konfigürasyon anahtarının etkinleştirilmesi gerekir. Bu konfigürasyon anahtarı, **Sistem yönetimi** \> **Kurulum** \> **Lisans konfigürasyonu** altındaki **ticaret konfigürasyon** anahtarlarında bulunabilir. Bu, satış siparişi satırı düzeyinde konfigüre edilen teslimat adresine dayalı olarak çeşitli doğrulamaları gereklidir.

