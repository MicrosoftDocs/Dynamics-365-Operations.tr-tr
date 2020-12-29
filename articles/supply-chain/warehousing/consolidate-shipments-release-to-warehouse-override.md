---
title: Sevkiyat konsolidasyon ilkesi, Ambara serbest bırakma sayfasından geçersiz kılındığında sevkiyatları konsolide etme
description: Bu konu, bir veya daha fazla satış satırının Ambara serbest bırakma sayfasından manuel olarak ambara serbest bırakılmasının ve serbest bırakmadan önce sistem tarafından tanımlanan sevkiyat konsolidasyon ilkesinin geçersiz kılınmasının gerektiği bir senaryo sunar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 96f994e9f3440721105545f96d7d8475fcab2b6b
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439639"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a>Sevkiyat konsolidasyon ilkesi, Ambara serbest bırakma sayfasından geçersiz kılındığında sevkiyatları konsolide etme

[!include [banner](../includes/banner.md)]

Bu konu, bir veya daha fazla satış satırının **Ambara serbest bırakma** sayfasından manuel olarak ambara serbest bırakılmasının ve serbest bırakmadan önce sistem tarafından tanımlanan sevkiyat konsolidasyon ilkesinin geçersiz kılınmasının gerektiği bir senaryo sunar. Örneğin, genellikle açık sevkiyatlarla konsolide edilmemiş bir siparişin açık sevkiyatlarla konsolide edilmesi gerekirse sevkiyat konsolidasyon ilkesinin geçersiz kılınması gerekebilir.

Senaryo sırasında, bir satış siparişleri kümesi oluşturacak ve siparişleri ambara serbest bırakmadan önce varsayılan sevkiyat konsolidasyon ilkesini geçersiz kılacaksınız.

## <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu konudaki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Sevkiyat konsolidasyon ilkelerini ve ürün filtrelerini ayarlama

Burada açıklanan senaryo, özelliği önceden açtığınız, [Sevkiyat konsolidasyonu ilkelerini yapılandırma](configure-shipment-consolidation-policies.md) alıştırmalarını yaptığınız ve burada açıklanan ilkeleri ve diğer kayıtları oluşturduğunuz varsayımına dayanır. Bu senaryoya devam etmeden önce söz konusu alıştırmaları yaptığınızdan emin olun.

## <a name="create-the-sales-orders-for-this-scenario"></a>Bu senaryo için satış siparişleri oluşturma

1. **Alacak hesapları \> Siparişler \> Tüm satış siparişleri** öğesine gidin ve aşağıdaki ayarlara sahip birbirinin aynı üç satış siparişi oluşturun:

    - **Müşteri hesabı:** *US-002*

1. Aşağıdaki ayarlara sahip bir satış siparişi satırı ekleyin:

    - **Madde numarası:** *A0001* (**Kod 4** filtresi atanmamış bir madde)
    - **Miktar:** *1.00*

1. **Stok \> Rezervasyon**'u ve sonra, Eylem Bölmesi'nde sipariş satırını rezerve etmek için **Lotu rezerve et**'i seçin.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Satış siparişlerini Ambara serbest bırakma sayfasından serbest bırakma

Ambara serbest bırakma sırasında sevkiyat konsolidasyon ilkesini geçersiz kılmak için bu adımları izleyin.

1. **Ambar yönetimi \> Ambara serbest bırak \> Ambara serbest bırak** öğesine gidin.
1. Üst bölmede, bu senaryo için oluşturduğunuz ilk satış siparişini seçin.
1. Satırı, ambara serbest bırakmaya eklemek için **Ekle**'yi seçin. *Varsayılan* sevkiyat konsolidasyon ilkesinin alt bölmede uygulandığına dikkat edin.
1. Alt bölmede, **Yeni sevkiyat konsolidasyon ilkesini seç** seçeneğini belirleyin.
1. Aynı ilkenin diğer açık sevkiyatlarıyla konsolidasyona olanak veren bir ilke seçin. Örneğin, *CustomerOrderNo* ilkesini seçin.
1. **Ambara serbest bırak**'ı seçin.
1. Bu senaryo için oluşturduğunuz ikinci ve üçüncü satış siparişlerini seçin.
1. Satırları, ambara serbest bırakmaya eklemek için **Ekle**'yi seçin. *Varsayılan* ilkesinin alt bölmede uygulandığına dikkat edin.
1. İkinci satırı seçin ve sonra, **Yeni sevkiyat konsolidasyon ilkesi seç** alanında, *CustomerOrderNo* ilkesini seçin.
1. Her iki satır için **Ambara serbest bırak**'ı seçin.

## <a name="verify-the-shipments"></a>Sevkiyatları doğrulama

İki sevkiyat oluşturulmuş olmalıdır:

- İlk sevkiyat iki satır içerir ve *CustomerOrderNo* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.
- İkinci sevkiyat bir satır içerir ve *Varsayılan* sevkiyat konsolidasyon ilkesi kullanılarak oluşturulmuştur.

Oluşturulan sevkiyatları gözden geçirmek için bu adımları izleyin.

1. **Ambar yönetimi \> Sevkiyatlar \> Tüm sevkiyatlar**'a gidin.
1. Gerekli sevkiyatı bulun ve seçin.
1. **Sevkiyat konsolidasyon ilkesi** alanında, sevkiyat oluşturulduğunda kullanılan konsolidasyon ilkesini gözden geçirin.

## <a name="additional-resources"></a>Ek kaynaklar

- [Sevkiyat konsolidasyonu ilkeleri](about-shipment-consolidation-policies.md)
- [Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md)
