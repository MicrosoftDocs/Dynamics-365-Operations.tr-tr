---
title: Alım satım varlıkların sıralama düzenini değiştirme
description: Bu makale, alım satım ilgili çeşitli kuruluşlar için Dynamics 365 Commerce'deki görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır.
author: josaw1
ms.date: 08/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265849"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Alım satım varlıkların sıralama düzenini değiştirme


[!Include [banner](includes/banner.md)]

Perakendeciler, tüm kanallarda müşteri etkileşimi için ürün keşfini bir ana araç olarak kabul edin. Müşterilerin ürünleri kolayca bulmasına yardımcı olabilecek çeşitli özellikler vardır. Örneğin müşteriler, kategorilere göz atabilir, arayabilir ve filtreleyebilir.

Bu makale, alım satım ilgili çeşitli kuruluşlar için görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır. Sıralama düzenini nasıl değiştireceğinizi de açıklar.

## <a name="overview"></a>Genel Bakış

Commerce'te, alım satımla ilgili çeşitli varlıkları sıralama işlemi, varolan müşteri senaryolarıyla uyumlu hale getirilmiştir ve artık uygulama ortaklarından gelen uzantıları gerektirmez.

10.0.5 ve önceki Commerce sürümlerinde, gezinti hiyerarşisindeki kategorilerin sıralama düzeni alfabetik idi. Mevcut özel sıralama düzeni işlevi, alım satım yöneticilerinin tüm son kullanıcı istemcileri genelinde alım satım ile ilgili çeşitli varlıklar için sıralama düzenini yapılandırmasına olanak tanır. Bu istemciler Yönetim Merkezleri (HQ) ve çağrı merkezleri içerirler.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Ürün hiyerarşisindeki kategorilerin görüntülenme sırasını yapılandırma

Bu yordamı tamamlayabilmek için, demo verilerinin çalışma ortamınıza yüklenmiş olması gerekir.

1. **Retail ve Commerce \> Ürünler ve kategoriler \> Commerce ürün hiyerarşisi**'ne gidin.
2. **Kategori hiyerarşisi düzenle**'ye tıklayın.
3. **Düzenle**'yi tıklatın.
4. Ağaçta **TÜMÜ \> Eylem Sporları**'nı genişletin.
5. Ağaçta **TÜMÜ \> Takım Sporları**'nı genişletin.
6. **Görüntüleme sırası** alanına bir sayı girin. (Bu sayı eksi olabilir.)
7. Sırasını değiştirmek istediğiniz ek kategoriler için 4 ile 6 arasındaki adımları yineleyin.

Kanal gezinti hiyerarşisinin görüntüleme sırası, Commerce ürün hiyerarşisi için HQ ve kategoriye göre serbest bırakılan Ürünler için yansıtılır.

![Özel negatif değerlerle sıralanan ürün hiyerarşisi.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Ürün hiyerarşisine göre özel sıralanmış, kategoriye göre yayınlanan ürünler.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kanal gezinme hiyerarşisindeki kategorilerin görüntülenme sırasını konfigüre etme

Bu yordamı tamamlayabilmek için, demo verilerinin çalışma ortamınıza yüklenmiş olması gerekir.

1. **Retail and Commerce \> Ürünler ve kategoriler \> Kanal gezinme kategorileri**'ne gidin.
2. Listesinde, **Moda göre gezinti** hiyerarşisini seçin.
3. **Kategori hiyerarşisi düzenle**'ye tıklayın.
4. **Düzenle**'yi tıklatın.
5. Ağaçta **Moda \> Kadın Giyim \> Kadın Ayakkabıları**'nı seçin.
6. **Görüntüleme sırası** alanına bir sayı girin.
7. Ağaçta **Moda \> Womenswear \> Üstler**'i seçin.

Benzer şekilde, alt kategorilerin sıralama düzenini de tanımlayabilirsiniz.

8. Ağaçta **Moda \> Menswear \> Günlük Gömlekler**'i seçin.
9. **Görüntüleme sırası** alanına bir sayı girin.
10. Ağaçta **Moda \> Menswear \> Montlar ve Ceketler**'i seçin.
11. **Görüntüleme sırası** alanına bir sayı girin.
12. Sırasını değiştirmek istediğiniz ek kategoriler için adımları yineleyin.

Kanal gezinme hiyerarşisinin görüntüleme sırası HQ, Katalog ve kanallarda yansıtılır.

![Kanal gezinme hiyerarşisi özel sıralandı.](./media/ChannelNavCustomSorted.png)

![Katalog Gezinti hiyerarşisi kanal gezinti hiyerarşisine göre özel sıralandı.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Özel sıralı kategorileri olan POS.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Varsayılan olarak, **Alım satım varlıkları için görüntüleme düzenini etkinleştir** özelliği kapalıdır. Etkinleştirmek için [özellik yönetimini](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) kullanın. Özelliği etkinleştirdikten sonra, dağıtım zamanlamasından **Genel yapılandırma -1110** CDX işini çalıştırın.
> POS'taki kategori sıranız güncelleştirilmemişse, aygıtı yeniden etkinleştirin. Kategori bilgileri, aygıt etkinleştirme işlemi gerçekleştiğinde getiriliyorsa aygıtın, kategori bilgilerini güncelleştirilmiş görüntüleme sıralarıyla yeniden alması gerekebilir. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
