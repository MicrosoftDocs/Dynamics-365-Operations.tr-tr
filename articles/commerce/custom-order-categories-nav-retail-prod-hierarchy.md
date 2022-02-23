---
title: Alım satım varlıkların sıralama düzenini değiştirme
description: Bu konu, alım satım ilgili çeşitli kuruluşlar için Dynamics 365 Commerce'deki görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b983cb5c63db171c76d34375a93a2b9086185d3a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416433"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Alım satım varlıkların sıralama düzenini değiştirme


[!include [banner](includes/banner.md)]

Perakendeciler, tüm kanallarda müşteri etkileşimi için ürün keşfini bir ana araç olarak kabul edin. Çeşitli işlevler müşterilerin ürünleri kolayca bulmasına yardımcı olabilir. Örneğin kategorilerine, aramaya ve filtreye göz atabilirler.

Bu konu, alım satım ilgili çeşitli kuruluşlar için görüntüleme sırasını denetlemeyle ilgili kavramları açıklamaktadır. Sıralama düzenini nasıl değiştireceğinizi de açıklar.

## <a name="overview"></a>Genel bakış

Çeşitli alım satım ilişkili varlıkları sıralama desteği geliştirilmiştir. Bu destek şimdi, daha önce uygulama ortaklarından eklenti gerektiren mevcut müşteri senaryoları ile daha uyumludur.

Sürüm 10.0.5'ten önceki Retail sürümlerinde, gezinti hiyerarşisindeki kategorilerin sıralama düzeni alfabetik idi. Yeni özel sıralama düzeni işlevi alım ve satım yöneticilerinin tüm Son Kullanıcı istemcileri üzerinde Merchandising ile ilgili çeşitli varlıklar için sıralama düzenini konfigüre etmenize olanak tanır. Bu istemciler Yönetim Merkezleri (HQ) ve çağrı merkezleri içerirler.

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

![Özel negatif değerlerle sıralanan ürün hiyerarşisi](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Ürün hiyerarşisine göre özel sıralanmış, kategoriye göre yayınlanan ürünler](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kanal gezinme hiyerarşisindeki kategorilerin görüntülenme sırasını konfigüre etme

Bu yordamı tamamlayabilmek için, demo verilerinin çalışma ortamınıza yüklenmiş olması gerekir.

1. **Retail and Commerce \> Ürünler ve kategoriler \> Kanal gezinme kategorileri**'ne gidin.
2. Listesinde, **Moda göre gezinti** hiyerarşisini seçin.
3. **Kategori hiyerarşisi düzenle**'ye tıklayın.
4. **Düzenle**'yi tıklatın.
5. Ağaçta **Moda \> Womenswear \> Kadın Ayakkabısı**'nı seçin.
6. **Görüntüleme sırası** alanına bir sayı girin.
7. Ağaçta **Moda \> Womenswear \> Üstler**'i seçin.

    Benzer şekilde, alt kategorilerin sıralama düzenini de tanımlayabilirsiniz.

8. Ağaçta **Moda \> Menswear \> Günlük Gömlekler**'i seçin.
9. **Görüntüleme sırası** alanına bir sayı girin.
10. Ağaçta **Moda \> Menswear \> Montlar ve Ceketler**'i seçin.
11. **Görüntüleme sırası** alanına bir sayı girin.
12. Sırasını değiştirmek istediğiniz ek kategoriler için adımları yineleyin.

Kanal gezinme hiyerarşisinin görüntüleme sırası HQ, Katalog ve kanallarda yansıtılır.

![Kanal gezinme hiyerarşisi özel sıralandı](./media/ChannelNavCustomSorted.png)

![Katalog Gezinti hiyerarşisi kanal gezinti hiyerarşisine göre özel sıralandı](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Özel sıralı kategorileri olan POS](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Varsayılan olarak, özel sıralama düzeni özelliği kapalıdır. Bu özelliği ve diğer özellikleri nasıl açacağınızı öğrenmek için [Özellik Yönetimi](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)'ne bakın.
