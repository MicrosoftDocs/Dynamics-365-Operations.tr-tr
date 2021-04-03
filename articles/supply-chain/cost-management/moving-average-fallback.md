---
title: Hareketli ortalama, geri dönüş maliyet sırası
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'ta hareketli ortalama hesaplamaları için geri dönüş maliyet sıraları hakkında bilgi sağlar.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 1f5b1307f039bb9e921d50aed411b3dc603ada65
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263626"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="c5458-103">Hareketli ortalama, geri dönüş maliyet sırası</span><span class="sxs-lookup"><span data-stu-id="c5458-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="c5458-104">Stoğunuzun maliyetini hesaplamak için kullanabileceğiniz bir yöntem _hareketli ortalama_ kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="c5458-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="c5458-105">Her stok maddesiyle en fazla üç maliyet değeri ilişkilendirilebilir:</span><span class="sxs-lookup"><span data-stu-id="c5458-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="c5458-106">**Son çıkış** – Stok eksiye düşmeden önce atanan son çıkış maliyeti</span><span class="sxs-lookup"><span data-stu-id="c5458-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="c5458-107">**Etkin maliyet** – Maliyetlendirme sürümünde etkinleştirilen en son maliyet</span><span class="sxs-lookup"><span data-stu-id="c5458-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="c5458-108">**Madde fiyatı** - Serbest bırakılan ürün için belirtilen maliyet</span><span class="sxs-lookup"><span data-stu-id="c5458-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="c5458-109">Hareketli ortalama hesaplamalarında bu maliyet değerlerinin hangisinin kullanılacağını belirlemek için, sistem değerler için tercih sırasını oluşturmak üzere _geri dönüş maliyet sırasını_ kullanır.</span><span class="sxs-lookup"><span data-stu-id="c5458-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="c5458-110">Tercih edilen maliyet değeri kullanılamıyorsa, sistem bir sonraki tercih edilen değeri kullanır.</span><span class="sxs-lookup"><span data-stu-id="c5458-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="c5458-111">Microsoft Dynamics 365 Supply Chain Management'ın önceki sürümlerinde, sistem sabit bir geri dönüş maliyet sırası (_Son çıkış – Etkin maliyet – Madde fiyatı_) kullanıyordu.</span><span class="sxs-lookup"><span data-stu-id="c5458-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="c5458-112">Sürüm 10.0.11'de bu sıra varsayılan olarak kalır.</span><span class="sxs-lookup"><span data-stu-id="c5458-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="c5458-113">Ancak, üç adet geri dönüş maliyeti sırası arasından seçim yapmanızı sağlayan bir özelliği de açabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c5458-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="c5458-114">Bu özellik, özellikle negatif stok değerlerini düzenli olarak kullanan kuruluşlar için kullanışlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c5458-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="c5458-115">Geri dönüş maliyet sırası için seçiciyi kullanılabilir hale getirmek üzere sizin (veya bir yöneticinin), _Hareketli ortalama geri dönüş maliyeti sırası_ adlı özelliği etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c5458-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="c5458-116">Hareketli ortalama hesaplamaları için geri dönüş maliyet sırasını seçmek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c5458-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="c5458-117">**Parametreler** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="c5458-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="c5458-118">**Stok muhasebesi** sekmesinde, **Hareketli ortalama** bölümünde, **Geri dönüş maliyet sırası** alanını aşağıdaki değerlerden birine ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c5458-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="c5458-119">**Son çıkış - Etkin maliyet – Madde fiyatı** – Bu sıra varsayılan sıradır.</span><span class="sxs-lookup"><span data-stu-id="c5458-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="c5458-120">_Hareketli ortalama geri dönüş maliyet sırası_ özelliği etkin olduğunda kullanılan sırayla aynı sıradır.</span><span class="sxs-lookup"><span data-stu-id="c5458-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="c5458-121">**Etkin maliyet - Son çıkış**</span><span class="sxs-lookup"><span data-stu-id="c5458-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="c5458-122">**Etkin maliyet – Madde fiyatı** - Kuruluşlar, stoklarda düzenli olarak negatif olan ve aynı anda hareket hacmi yüksek olan iş süreçlerini kullandıklarında, performans sorunlarıyla karşılaşabilir.</span><span class="sxs-lookup"><span data-stu-id="c5458-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="c5458-123">Bu ayar, bu performans sorunlarının etkilerini hafifletmeye yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c5458-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="c5458-124">![Stok muhasebesi parametreleri](media/inventory-accounting-parameters.png "Stok muhasebesi parametreleri")</span><span class="sxs-lookup"><span data-stu-id="c5458-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]