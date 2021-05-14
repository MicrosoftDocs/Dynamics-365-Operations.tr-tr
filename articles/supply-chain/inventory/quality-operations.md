---
title: Uygunsuzluklar için işlemler
description: Bu konu, uygunsuzluklar için işlemlerin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestOperations, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6454a56323ea66369696dd6e3310a41b4eb9ee58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956870"
---
# <a name="operations-for-nonconformances"></a><span data-ttu-id="1f080-103">Uygunsuzluklar için işlemler</span><span class="sxs-lookup"><span data-stu-id="1f080-103">Operations for nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f080-104">Bu konu, uygunsuzluklar için işlemlerin nasıl oluşturulacağını ve kullanılacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="1f080-104">This topic describes how to create and use operations for nonconformances.</span></span>

<span data-ttu-id="1f080-105">Onaylanan bir uygunsuzluk için gerçekleştirilebilecek işin sınıflandırmasını tanımlamak için **İşlemler** sayfasını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f080-105">You can use the **Operations** page to define classifications of the work that can be performed for an approved nonconformance.</span></span> <span data-ttu-id="1f080-106">Bir uygunsuzluğa ilgili bir işlem atadığınızda, işlemi gerçekleştirmek için gerekli ilgili malzemeler, işçilik saatleri ve ücretler vb. gibi ayrıntılar sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1f080-106">When you assign a related operation to a nonconformance, you can provide details such as the associated material, labor hours, and charges that are required to do the operation.</span></span> <span data-ttu-id="1f080-107">Sistem, bu bilgileri işlem için tahmini maliyetini hesaplanmasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1f080-107">The system uses this information to calculate an estimated cost for the operation.</span></span> <span data-ttu-id="1f080-108">Ayrıntılı bilgiler ve tahmini maliyetler bilgi amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="1f080-108">The detailed information and estimated costs are for reference.</span></span> <span data-ttu-id="1f080-109">Kalite için ilgili operasyonlar, bir üretim rotası için tanımlanabilecek operasyonlardan farklıdır.</span><span class="sxs-lookup"><span data-stu-id="1f080-109">The related operations for quality differ from the operations that can be defined for a production route.</span></span>

> [!NOTE]
> <span data-ttu-id="1f080-110">Uygunsuzlukla ilgili bir işlemde kullanılan maliyetleri, zamanı ve maddeleri izleyebilmenize karşın, girdiğiniz veriler yalnızca bilgilendirme amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="1f080-110">Although you can track costs, time, and the items that are used in an operation that is related to a nonconformance, the data that you enter is only informational.</span></span> <span data-ttu-id="1f080-111">Genel muhasebe, stok alt muhasebeyle veya **Zaman ve katılım** modülüyle otomatik olarak tümleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="1f080-111">It isn't automatically integrated with the general ledger, inventory subledger, or the **Time and attendance** module.</span></span>

## <a name="examples-of-operations"></a><span data-ttu-id="1f080-112">İşlem örnekleri</span><span class="sxs-lookup"><span data-stu-id="1f080-112">Examples of operations</span></span>

<span data-ttu-id="1f080-113">Bir üretim şirketi için çalışırsınız.</span><span class="sxs-lookup"><span data-stu-id="1f080-113">You work for a manufacturing company.</span></span> <span data-ttu-id="1f080-114">Kalite testi başarısız olan maddeler için bir uygunsuzluk oluşturuldu ve onaylandı.</span><span class="sxs-lookup"><span data-stu-id="1f080-114">A nonconformance was created and approved for items that failed a quality test.</span></span> <span data-ttu-id="1f080-115">Sorunun, bir makinedeki bozuk bir rulman ile ilişkili olduğunu göstermek için bir düzeltme oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="1f080-115">A correction was created to indicate that the problem was related to a bad bearing on a machine.</span></span> <span data-ttu-id="1f080-116">Rulmanı değiştirmek için birkaç adım gereklidir ve her işlemin sorumluluğu izlenir.</span><span class="sxs-lookup"><span data-stu-id="1f080-116">Several steps are required to replace the bearing, and the responsibility for each operation is tracked.</span></span> <span data-ttu-id="1f080-117">Örneğin, aşağıdaki adımlar gerekli olabilir:</span><span class="sxs-lookup"><span data-stu-id="1f080-117">For example, the following steps might be required:</span></span>

1. <span data-ttu-id="1f080-118">Üretim hattı durdurulur ve temizleme prosedürü gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1f080-118">The production line is stopped, and the clean-out routine is performed.</span></span>
1. <span data-ttu-id="1f080-119">Bakım personeli, rulmanı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1f080-119">Maintenance personnel replace the bearing.</span></span>
1. <span data-ttu-id="1f080-120">Kalite güvence personeli, makineyi yeniden açılmadan önce denetler.</span><span class="sxs-lookup"><span data-stu-id="1f080-120">Quality assurance personnel inspect the machine before it's turned back on.</span></span>

<span data-ttu-id="1f080-121">Bu örnekte, gerçekleştirilmesi gereken işi temsil etmek üzere aşağıdaki işlemler oluşturulabilir:</span><span class="sxs-lookup"><span data-stu-id="1f080-121">For this example, the following operations can be created to represent the work that must be done:</span></span>

- <span data-ttu-id="1f080-122">Üretim hattını durdurun.</span><span class="sxs-lookup"><span data-stu-id="1f080-122">Stop the production line.</span></span>
- <span data-ttu-id="1f080-123">Üretim hattını temizleyin.</span><span class="sxs-lookup"><span data-stu-id="1f080-123">Clean out the production line.</span></span>
- <span data-ttu-id="1f080-124">Makine bakımı gerçekleştirin.</span><span class="sxs-lookup"><span data-stu-id="1f080-124">Perform machine maintenance.</span></span>
- <span data-ttu-id="1f080-125">Makineyi inceleyin.</span><span class="sxs-lookup"><span data-stu-id="1f080-125">Inspect the machine.</span></span>

## <a name="create-an-operation"></a><span data-ttu-id="1f080-126">Bir işlem oluşturma</span><span class="sxs-lookup"><span data-stu-id="1f080-126">Create an operation</span></span>

1. <span data-ttu-id="1f080-127">**Stok yönetimi \> Kurulum \> Kalite yönetimi \> Operasyonlar** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="1f080-127">Go to **Inventory management \> Setup \> Quality management \> Operations**.</span></span>
1. <span data-ttu-id="1f080-128">Eylem bölmesinde, kılavuzuna satır eklemek için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1f080-128">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="1f080-129">Ardından yeni satırda aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="1f080-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="1f080-130">**İşlem** – İşlem için benzersiz bir kod ya da ad girin.</span><span class="sxs-lookup"><span data-stu-id="1f080-130">**Operation** – Enter a unique ID or name for the operation.</span></span>
    - <span data-ttu-id="1f080-131">**Açıklama**: – İşlemin detaylı bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="1f080-131">**Description** – Enter a detailed description of the operation.</span></span>
    - <span data-ttu-id="1f080-132">**Tür** – İşlem yalnızca belirli bir sipariş türüyle ilişkili uygunsuzluklarla kullanılabiliyorsa, sipariş türünü (*Satınalma siparişi* veya *Satış siparişi*) seçin.</span><span class="sxs-lookup"><span data-stu-id="1f080-132">**Type** – If the operation can be used only with nonconformances that are related to a specific type of order, select the order type (*Purchase order* or *Sales order*).</span></span>

1. <span data-ttu-id="1f080-133">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1f080-133">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f080-134">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="1f080-134">Additional resources</span></span>

- [<span data-ttu-id="1f080-135">Kalite yönetimine genel bakış</span><span class="sxs-lookup"><span data-stu-id="1f080-135">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="1f080-136">Kalite ve uygunsuzluk yönetimini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="1f080-136">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="1f080-137">Uygunsuzluk oluşturma ve işleme</span><span class="sxs-lookup"><span data-stu-id="1f080-137">Create and process nonconformances</span></span>](tasks/create-process-non-conformance.md)
- [<span data-ttu-id="1f080-138">Uygunsuzlukları onaylamaktan sorumlu çalışanlar</span><span class="sxs-lookup"><span data-stu-id="1f080-138">Workers responsible for approving nonconformances</span></span>](quality-responsible-workers.md)
- [<span data-ttu-id="1f080-139">Uygunsuzluklar için karantina bölgeleri</span><span class="sxs-lookup"><span data-stu-id="1f080-139">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="1f080-140">Uygunsuzluklar için tanılama türleri</span><span class="sxs-lookup"><span data-stu-id="1f080-140">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="1f080-141">Uygunsuzluklar için kalite masrafları</span><span class="sxs-lookup"><span data-stu-id="1f080-141">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="1f080-142">Uygunsuzluklar için sorun türleri</span><span class="sxs-lookup"><span data-stu-id="1f080-142">Problem types for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="1f080-143">Ambar işlemleri için kalite yönetimi</span><span class="sxs-lookup"><span data-stu-id="1f080-143">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
