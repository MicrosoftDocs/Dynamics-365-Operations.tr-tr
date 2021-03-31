---
title: Belirli ürün yaşam döngüsü durumlarına sahip ürünleri hariç tutma
description: Bu konuda, Planlama İyileştirmesi işlevi kullanılırken ürünlerin yaşam döngüsü durumlarına göre nasıl hariç tutulacağı açıklanmaktadır.
author: ChristianRytt
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a1e0c734db763ffa69e2d6540a07d5fa04c22ea1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227830"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a><span data-ttu-id="7ee9e-103">Belirli ürün yaşam döngüsü durumlarına sahip ürünleri hariç tutma</span><span class="sxs-lookup"><span data-stu-id="7ee9e-103">Exclude products that have specific product lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ee9e-104">Serbest bırakılmış ürünler ve serbest bırakılmış ürün sürümleri bir **Ürün yaşam döngüsü durumu** alanı içerir.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-104">Released products and released product versions include a **Product lifecycle state** field.</span></span> <span data-ttu-id="7ee9e-105">Bu alan, diğer işlemlerin yanı sıra master planlama sırasında dahil edilen ürünleri denetlemenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-105">This field lets you control, among other things, which products are included during master planning.</span></span> <span data-ttu-id="7ee9e-106">**Ürün bilgileri yönetimi \> Kurulum \> Ürün yaşam döngüsü durumu**'na giderek yaşam döngüsü durumlarını gerektiği gibi ekleyebilir, kaldırabilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-106">You can add, remove, and edit lifecycle states as required by going to **Product information management \> Setup \> Product lifecycle state**.</span></span> <span data-ttu-id="7ee9e-107">Ürünlerin master planlama sırasında dahil edilmesi gerekiyorsa her ürün yaşam döngüsü durumu için **Planlama için etkin** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-107">For each product lifecycle state, set the **Is active for planning** option to *Yes* if products that have that state should be included during master planning.</span></span> <span data-ttu-id="7ee9e-108">Seçenek *Hayır* olarak ayarlandığında, ilişkili ürünler ve varyantlar tüm master planlamalardan ve ürün reçetesi düzeyindeki tüm hesaplamalardan hariç tutulur.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-108">When the option is set to *No*, the associated products and variants will be excluded from all master planning and all calculations at the bill of materials (BOM) level.</span></span>

<span data-ttu-id="7ee9e-109">**Ürün yaşam döngüsü durumu** alanının boş bırakıldığı serbest bırakılan ürünler ve varyantlar, **Planlama için etkin** seçeneği *Evet* olarak ayarlanmış bir ürün yaşam döngüsü durumuna sahipmiş gibi kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-109">Released products and variants where the **Product lifecycle state** field is left blank are treated as though they have a product lifecycle state where the **Is active for planning** option is set to *Yes*.</span></span> <span data-ttu-id="7ee9e-110">Başka bir deyişle, master planlama sırasında dahil edilirler.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-110">In other words, they will be included during master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="7ee9e-111">Gereksiz tedarik önerilerini önlemek için kullanım dışı bırakılmış tüm serbest bırakılan ürünleri ve varyantları **Planlama için etkin** seçeneğinin *Hayır* olarak ayarlandığı bir ürün yaşam döngüsü durumuyla ilişkilendirmenizi öneririz.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-111">To help avoid unnecessary supply suggestions, we strongly recommend that you associate all obsolete released products and variants with a product lifecycle state where the **Is active for planning** option is set to *No*.</span></span> <span data-ttu-id="7ee9e-112">Bu yaklaşım özellikle, yeniden kullanılabilir olmayan ürün yapılandırma varyantlarıyla çalışırken önemlidir çünkü atığı önlemeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-112">This approach is especially important when you work with product configuration variants that aren't reusable, because it will help prevent waste.</span></span>

## <a name="related-resources"></a><span data-ttu-id="7ee9e-113">İlgili kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7ee9e-113">Related resources</span></span>

<span data-ttu-id="7ee9e-114">Ürün yaşam döngüsü durumları hakkında daha fazla bilgi edinmek için [Ürün yaşam döngüsü durumuna genel bakış](../../pim/product-lifecycle.md) başlıklı makaleye bakın.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-114">For more information about product lifecycle states, see [Product lifecycle state overview](../../pim/product-lifecycle.md).</span></span>

<span data-ttu-id="7ee9e-115">Ürünleri master planlama ve ürün reçetesi düzeyinde hesaplamalar dışında tutmak amacıyla ürün yaşam döngüsü durumlarının nasıl kullanılacağı ile ilgili adımları içeren daha fazla bilgi edinmek için [Ürünleri Master planlama dışında tutmak için bir ürün yaşam döngüsü durumu oluşturma](../../pim/tasks/exclude-products-master-planning.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="7ee9e-115">For detailed information that includes steps for using product lifecycle states to exclude products from master planning and BOM-level calculations, see [Create a product lifecycle state to exclude products from Master planning](../../pim/tasks/exclude-products-master-planning.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]