---
title: "Perakende kanallarını tanımla ve koru"
description: "Bu makalede, Microsoft Dynamics 365 perakende mağazasında işlemleri için olarak adlandırılır Tuğla Dibek mağazalar ayarlama işlemine genel bakış sağlar. Makalede, perakende mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b775ba34ef7d88dd0b47904e4a3e9be79664f14b
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-maintain-retail-channels"></a>Perakende kanallarını tanımla ve koru

Bu makalede, Microsoft Dynamics 365 perakende mağazasında işlemleri için olarak adlandırılır Tuğla Dibek mağazalar ayarlama işlemine genel bakış sağlar. Makalede, perakende mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.

Perakende ve ticaret işlemleri için Dynamics 365, çevrimiçi mağazalar, çağrı merkezleri ve Tuğla Dibek depoları gibi birden fazla perakende kanal destekler. Perakende ve ticarette, tuğla dibek mağazaya perakende mağaza adı verilir. Her perakende mağazasının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir. Bir perakende mağazası oluşturmadan önce tüm bu öğeleri ayarlamanız gerekir. Perakende mağaza oluşturduktan sonra gerçekleştirmek istediğiniz ürünleri atarsınız. Ayrıca mağazaya çalışanlar, kasalar ve müşteriler atarsınız. Son olarak, yeni mağazayı bir organizasyon hiyerarşisine eklersiniz.

## <a name="setting-up-retail-stores"></a>Perakende mağazaları kurma
Dynamics 365 işlemleri için de bir perakende mağaza ayarlayabilirsiniz önce bazı önkoşul görevleri tamamlamanız gerekir. Sonrasında perakende mağazayı oluşturabilir ve ayrıntılar ekleyebilirsiniz.

### <a name="prerequisites"></a>Önkoşullar

Bir perakende mağaza kurmadan önce aşağıdaki görevleri tamamlamanız gerekir:

1.  Organizasyon yapınızı yapılandırın ve perakende sınıflamalar, stok yenileme ve raporlama için kuruluş hiyerarşilerini ayarlayın.
2.  Perakende mağazayı temsil eden bir ambar ayarlayın.
3.  Perakende mağazalar, mağaza ekstreleri ve ekstre fişleri için numara sıraları ayarlayın.
4.  Perakende için parametreleri konfigüre et.
5.  Mağazanın kabul ettiği ödeme yöntemleri ayarlayın.
6.  Perakende POS kasalarında kredi kartı işlemleri yürütmek için, ödeme hizmetleri de ayarlayabilirsiniz.
7.  Satış vergisi gruplarını ayarla.
8.  Perakende ürünleri ayarlayın. Bu görevin bir parçası olarak, ayrıca perakende ürün hiyerarşileri, ürün çeşitleri ve ürün sınıflamaları ayarlayın.
9.  Ürün fiyat gruplarını ayarlayın.
10. Perakende ürün fiyatlandırmasını ayarlayın. Bu görevin bir parçası olarak, aynı zamanda fiyat ayarlamaları, iskontolar ve iskonto dönemlerini ayarlayın.
11. Personeli ayarlayın. **Not:** oturum açma ve Retail POS sistemi işlemleri için Dynamics 365 kullanarak görevleri gerçekleştirmek için işçilere uygun izinleri de atamalısınız.
12. Mağazaya atamak için Perakende POS profillerini yapılandırın. Bu görev kayıtları ayarlamak, çevrimdışı profilleri ayarlamak ve makbuz biçimleri ve profilleri ayarlamak gibi birçok diğer görevi içerir.

Önkoşula dahil tüm görevleri gözden geçirin ve yalnızca sizin için geçerli görevleri tamamlayın.

### <a name="set-up-a-retail-store"></a>Bir perakende mağaza kurun

+Önkoşul görevlerini tamamladıktan sonra perakende mağaza ayrıntılarını ayarlamak için aşağıdaki görevleri tamamlayın:

1.  Bir perakende mağazası oluşturun.
2.  Mağazaya bir satış vergisi grubu atayın.
3.  Çevrimiçi mağaza tarafından kabul edilen ödeme yöntemleri atayın.
4.  Perakende mağazasında sunduğunuz ürünler için ürün açıklamalarına ayrıntılar ekleyin. Örneğin, zengin metin ve resimler ekleyebilirsiniz. Bu ürün ayrıntıları çeşitli bağlamlarda POS kasası veya yazdırılan etiketlerde görünür.
5.  **Perakende sınıflama**, **Perakende stok yenileme**, veya **Perakende raporlama** amacıyla mağazayı varsayılan kuruluş hiyerarşisine ekleyin.

### <a name="after-you-set-up-a-retail-store"></a>Bir perakende mağaza kurduktan sonra

Perakende mağaza için ayrıntıları girdikten sonra, yeni perakende mağaza verilerini Perakende POS'una göndermek için şu görevleri tamamlayın:

1.  Mağaza için POS kasalarını yapılandırın.
2.  Mağazaya ürün çeşitleri atayın.
3.  Sınıflama içinde bulunan ürün listesini oluşturmak ve ürünleri perakende mağazada erişilebilir hale getirmek için sınıflamaları işleyin.
4.  Numara serileri, donanım profilleri ve POS ekran düzeni gibi verileri Perakende POS kasalarına gönderin.
5.  Perakende POS'una mağaza verisini göndermek için perakende mağazayı yayımlayın.
6.  Perakende POS'una mağaza verisini göndermek için işleri yürütün.

## <a name="organization-hierarchies"></a>Kuruluş hiyerarşileri
Perakende, perakende kanallarını yapılandırmak için Microsoft Dynamics AX'teki kuruluş hiyerarşilerini kullanır. Organizasyon hiyerarşileri, organizasyonlar arasındaki işinizi meydana getiren ilişkileri temsil eder. Mağazalar kurduğunuzda, onları bir organizasyon hiyerarşisine ekleyebilirsiniz. Ardından mağazalar ürün çeşitleri, stok yenileme ve raporlama için kullanılan verileri paylaşır.


