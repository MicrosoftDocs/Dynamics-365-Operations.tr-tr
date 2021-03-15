---
title: Sevkiyatları konsolide etme sayfası kullanılarak sevkiyatları manuel olarak konsolide etme
description: Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, Sevkiyatları konsolide etme sayfası kullanılarak konsolide edildiği bir senaryo sunar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983029"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Sevkiyatları konsolide etme sayfası kullanılarak sevkiyatları manuel olarak konsolide etme

[!include [banner](../includes/banner.md)]

Bu konu, çoklu siparişlerin aynı yükte yer alarak ambara serbest bırakıldığı ve ardından, **Sevkiyatları konsolide etme** sayfası kullanılarak konsolide edildiği bir senaryo sunar.

## <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama

Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır. Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.

## <a name="create-the-sales-orders-for-this-scenario"></a>Bu senaryo için satış siparişleri oluşturma

Çalışabileceğiniz bir satış siparişleri koleksiyonu oluşturarak başlayın. Gelişmiş ambar (WMS) işlemleri için etkinleştirilen bir ambarla çalışmanız gerekir. Başka bir ambar açıkça belirtilmedikçe, aşağıdaki sipariş kümelerinin her biri için aynı ambar kullanılmalıdır.

**Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki alt bölümlerde açıklanan ayarlara sahip bir satış siparişleri koleksiyonu oluşturun.

### <a name="create-sales-orders-1-and-2"></a>Satış siparişi 1 ve 2'yi oluşturma

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-007*
    - **Havuz:** *ShipCons*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

### <a name="create-sales-orders-3-and-4"></a>Satış siparişi 3 ve 4'ü oluşturma

1. Aşağıdaki ayarlara sahip birbirinin aynı iki satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-007*
    - **Havuz:** Bu alanı boş bırakın.

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

## <a name="release-the-orders-to-the-warehouse"></a>Siparişleri ambara serbest bırakma

Bu senaryo için oluşturduğunuz her satış siparişini ambara serbest bırakmak için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Siparişler \> Tüm satış siparişleri**'ne gidin.
1. Serbest bırakılacak satış siparişini bulun ve seçin.
1. Eylem Bölmesi'ndeki **Ambar** sekmesinde, seçili satış siparişini serbest bırakmak için **Eylemler \> Ambara serbest bırak**'ı seçin.
1. Bu yordamı, bu senaryo için oluşturduğunuz diğer satış siparişlerinin her biri için yineleyin.

## <a name="consolidate-shipments"></a>Sevkiyatları konsolide et

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. Satış siparişi 1 ambara serbest bırakıldığında oluşturulan bir sevkiyatı bulun ve seçin. (**Sevkiyat konsolidasyon ilkesi** alanı *Sipariş havuzu* olarak ayarlanmalıdır.)
1. Eylem Bölmesi'ndeki **Sevkiyatlar** sekmesinde, **Sevkiyatlar \> Sevkiyatları konsolide et**'i seçin.
1. Konsolidasyon için önerilen sevkiyatları doğrulayın. Konsolidasyon için yalnızca aynı ilkeye sahip bir sevkiyat önerilmesi gerekir.
1. **Sevkiyat konsolidasyonu** sayfasını kapatın.
1. Satış siparişi 3 ambara serbest bırakıldığında oluşturulan bir sevkiyatı bulun ve seçin. (**Sevkiyat konsolidasyon ilkesi** alanı *Varsayılan* olarak ayarlanmalıdır.)
1. Eylem Bölmesi'ndeki **Sevkiyatlar** sekmesinde, **Sevkiyatlar \> Sevkiyatları konsolide et**'i seçin.
1. Konsolidasyon için herhangi bir sevkiyatın önerilmediğini doğrulayın.
1. **Filtreleri göster**'i seçin.
1. **Filtreler** bölmesinde, **Sipariş numarası** filtresini kaldırın ve sonra **Uygula**'yı seçin.
1. Konsolidasyon için önerilen sevkiyatları doğrulayın. Konsolidasyon için yalnızca aynı ilkeye sahip bir sevkiyat önerilmesi gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Sevkiyat konsolidasyonu ilkeleri](about-shipment-consolidation-policies.md)
- [Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]