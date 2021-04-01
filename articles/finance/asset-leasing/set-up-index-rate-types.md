---
title: Endeks oranlarını ayarlama
description: Bu konuda, endeks oranlarının nasıl ayarlanacağı açıklanmaktadır. Kuruluşunuz, kira ödeme tutarlarını bir endeks oranları kümesiyle ilişkilendiriyorsa endeks oranları gereklidir.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b6d201329996f23d94c0fc76a9635d3bb99c931e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249689"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="f66a4-104">Endeks oranlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="f66a4-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f66a4-105">Kira ödemeleri bir endekse bağlıysa endeks oranı türleri sisteme eklenebilir ve korunabilir.</span><span class="sxs-lookup"><span data-stu-id="f66a4-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="f66a4-106">Kira ödemelerini **Endeks oranı türü** sayfasında yeniden değerlemek için, endeks oranı yeniden değerleme işleminde yeniden değerleme tarihindeki en güncel endeks oranı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f66a4-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="f66a4-107">Endeks oranı türleri ve endeks oranları eklemek için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="f66a4-108">**Varlık kiralama \> Kurulum \> Endeks oranı türü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="f66a4-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-109">Select **New**.</span></span>
3. <span data-ttu-id="f66a4-110">Uygun alanlara oran türünü ve endeks oranı adını girin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="f66a4-111">Yeni bir endeks oranı değeri eklemek için endeks oranı türünü seçin ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="f66a4-112">Oranın efektif başlangıç tarihini seçin ve oran değerini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="f66a4-113">Endeks oranı yöntemi olarak **Endeks oranı değer farkı**'nı veya **Endeks oranı değeri**'ni seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="f66a4-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="f66a4-114">Başlangıç tarihindeki endeks oranı ve en güncel endeks oranı arasındaki farkı temel alarak yeni bir kira ödemesini hesaplamak için **Endeks oranı değer farkı** yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="f66a4-115">Endeks oranı **Endeks oranı (%)** alanında tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f66a4-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="f66a4-116">**Endeks oranı (%)** alanında belirtilen yüzdeyi kullanarak kira ödemesini hesaplamak için **Endeks oranı değeri** yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="f66a4-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]