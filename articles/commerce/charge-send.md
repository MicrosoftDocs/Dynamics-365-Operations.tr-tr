---
title: Gönderimle görevlendir özelliğini kullanarak siparişleri başka bir mağazaya sevk etme
description: Bu konuda Gönderimle görevlendir özelliği açıklanmaktadır.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 37ef0234df4ee983c44c183fe884c73b17eb0e06
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219041"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="515a1-103">Gönderimle görevlendir özelliğini kullanarak siparişleri başka bir mağazaya sevk etme</span><span class="sxs-lookup"><span data-stu-id="515a1-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="515a1-104">Commerce'teki Gönderimle görevlendirme özelliğiyle, müşteri siparişleri bir mağazadan alınabilir ve başka bir mağazadan sevk edilebilir.</span><span class="sxs-lookup"><span data-stu-id="515a1-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="515a1-105">Satış noktası (POS) istemcisindeki müşteri siparişleri birden fazla karşılama seçeneğini destekler.</span><span class="sxs-lookup"><span data-stu-id="515a1-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="515a1-106">Karşılama seçeneklerine örnek olarak aşağıdakiler verilebilir:</span><span class="sxs-lookup"><span data-stu-id="515a1-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="515a1-107">Farklı bir tarihte aynı mağazadan alma.</span><span class="sxs-lookup"><span data-stu-id="515a1-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="515a1-108">Aynı tarihte veya farklı bir tarihte farklı bir mağazadan alma.</span><span class="sxs-lookup"><span data-stu-id="515a1-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="515a1-109">Mağazaya atanan varsayılan sevk deposundan sevk etme ve belirli bir tarihte teslim etme.</span><span class="sxs-lookup"><span data-stu-id="515a1-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="515a1-110">Gönderimle görevlendir özelliği şu POS işlemlerini kullanır: Tüm ürünleri sevk et ve Seçilen ürünleri sevk et.</span><span class="sxs-lookup"><span data-stu-id="515a1-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="515a1-111">Bu, mağaza görevlisinin, siparişin veya sipariş satırının karşılanacağı "sevkiyat çıkış yeri" konumunu seçmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="515a1-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="515a1-112">Varsayılan olarak, "sevkiyat çıkış yeri" konumu mağazayla ilişkili sevkiyat deposudur.</span><span class="sxs-lookup"><span data-stu-id="515a1-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="515a1-113">Ancak, mağaza görevlisi bu konumu değiştirebilir ve mağazaya atanmış mağaza konumlandırıcı grubunda tanımlanan herhangi bir mağazayı seçebilir.</span><span class="sxs-lookup"><span data-stu-id="515a1-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="515a1-114">"Sevkiyat varış yeri" adresini seçme özelliği değişmez.</span><span class="sxs-lookup"><span data-stu-id="515a1-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="515a1-115">Sipariş satırını karşılamak için kullanılabilecek sevkiyat yöntemleri ürünler ve adresler için geçerli teslimat modlarının yapılandırmasını temel alır.</span><span class="sxs-lookup"><span data-stu-id="515a1-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="515a1-116">Geçerli teslimat modlarıyla ilgili kurallar yalnızca Headquarters (HQ) içinde korunacağından, POS istemcisi bir sevkiyat satırı için geçerli teslim modlarını getirmek üzere gerçek zamanlı bir çağrı yapar.</span><span class="sxs-lookup"><span data-stu-id="515a1-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]