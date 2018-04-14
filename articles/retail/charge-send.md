---
title: "Bir siparişi farklı bir mağazadan sevk etme"
description: "Bu konuda Gönderimle görevlendir özelliği açıklanmaktadır."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 797058bdbbdb63a08eb35034ffe3c913307f38df
ms.openlocfilehash: 41434614b01f9a00f2b8a56765ecb90ee07e3d90
ms.contentlocale: tr-tr
ms.lasthandoff: 03/06/2018

---

# <a name="ship-an-order-from-a-different-store"></a>Bir siparişi farklı bir mağazadan sevk etme

[!INCLUDE [banner](includes/banner.md)]

Dynamics 365 for Retail'deki Gönderimle görevlendirme özelliğiyle, müşteri siparişleri bir mağazadan alınabilir ve başka bir mağazadan sevk edilebilir. Satış noktası (POS) istemcisindeki müşteri siparişleri birden fazla karşılama seçeneğini destekler. Karşılama seçeneklerine örnek olarak aşağıdakiler verilebilir:
-   Farklı bir tarihte aynı mağazadan alma.
-   Aynı tarihte veya farklı bir tarihte farklı bir mağazadan alma.
-   Mağazaya atanan varsayılan sevk deposundan sevk etme ve belirli bir tarihte teslim etme.

Gönderimle görevlendir özelliği şu POS işlemlerini kullanır: Tüm ürünleri sevk et ve Seçilen ürünleri sevk et. Bu, mağaza görevlisinin, siparişin veya sipariş satırının karşılanacağı "sevkiyat çıkış yeri" konumunu seçmesine olanak tanır. Varsayılan olarak, "sevkiyat çıkış yeri" konumu mağazayla ilişkili sevkiyat deposudur. Ancak, mağaza görevlisi bu konumu değiştirebilir ve mağazaya atanmış mağaza konumlandırıcı grubunda tanımlanan herhangi bir mağazayı seçebilir. 

"Sevkiyat varış yeri" adresini seçme özelliği değişmez. 

Sipariş satırını karşılamak için kullanılabilecek sevkiyat yöntemleri ürünler ve adresler için geçerli teslimat modlarının yapılandırmasını temel alır. Geçerli teslimat modlarıyla ilgili kurallar yalnızca Retail Headquarters (HQ) içinde korunacağından, POS istemcisi bir sevkiyat satırı için geçerli teslim modlarını getirmek üzere gerçek zamanlı bir çağrı yapar. 


