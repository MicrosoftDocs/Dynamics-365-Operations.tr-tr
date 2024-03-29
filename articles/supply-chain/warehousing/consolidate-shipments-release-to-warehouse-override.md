---
title: Sevkiyat konsolidasyonu ilkesi geçersiz kılınmamışsa sevkiyatları konsolide et
description: Bu makale, bir veya daha fazla satış satırının Ambara serbest bırakma sayfasından manuel olarak ambara serbest bırakılmasının ve serbest bırakmadan önce sistem tarafından tanımlanan sevkiyat konsolidasyon ilkesinin geçersiz kılınmasının gerektiği bir senaryo sunar.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e2c4fed880c423790b979f27511d8d5697bd244c
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427968"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Sevkiyat konsolidasyonu ilkesi geçersiz kılınmamışsa sevkiyatları konsolide et

[!include [banner](../includes/banner.md)]

Bu makale, bir veya daha fazla satış satırının **Ambara serbest bırakma** sayfasından manuel olarak ambara serbest bırakılmasının ve serbest bırakmadan önce sistem tarafından tanımlanan sevkiyat konsolidasyon ilkesinin geçersiz kılınmasının gerektiği bir senaryo sunar. Örneğin, genellikle açık sevkiyatlarla konsolide edilmemiş bir siparişin açık sevkiyatlarla konsolide edilmesi gerekirse sevkiyat konsolidasyon ilkesinin geçersiz kılınması gerekebilir.

Senaryo sırasında, bir satış siparişleri kümesi oluşturacak ve siparişleri ambara serbest bırakmadan önce varsayılan sevkiyat konsolidasyon ilkesini geçersiz kılacaksınız.

## <a name="make-demo-data-available"></a>Tanıtım verilerini kullanılabilir hale getirme

Bu makaledeki senaryo, Microsoft Dynamics 365 Supply Chain Management için sağlanan standart tanıtım verilerinde bulunan değerlere ve kayıtlara başvurur. Alıştırmaları yaparken burada sağlanan değerleri kullanmak isterseniz tanıtım verisinin yüklü olduğu bir ortamda çalıştığınızdan ve başlamadan önce tüzel kişiliği **USMF** olarak ayarladığınızdan emin olun.

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

- [Sevkiyat konsolidasyon ilkelerine genel bakış](about-shipment-consolidation-policies.md)
- [Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]