---
title: Bakım bütçelerini güncelleştirme
description: Bu konuda Varlık Yönetimi'nde bakım bütçesini güncelleştirme işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 486782968816cc585d9cf2d753f32e82f85e4f7e
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874797"
---
# <a name="update-maintenance-budgets"></a><span data-ttu-id="1df2e-103">Bakım bütçelerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1df2e-103">Update maintenance budgets</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="1df2e-104">**Bakım bütçesi satırları** sayfası, **Bakım bütçeleri** sayfasında seçilen bütçe için oluşturulan tüm bütçe satırlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1df2e-104">The **Maintenance budget lines** page shows all the budget lines that have been created for the budget that is selected on the **Maintenance budgets** page.</span></span> <span data-ttu-id="1df2e-105">(Daha fazla bilgi için bkz. [Bakım bütçeleri oluşturma](create-maintenance-budget.md).) Bakım bütçesi onaylanana kadar bakım bütçesi satırlarını yeniden hesaplayabilir ve ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-105">(For more information, see [Create maintenance budgets](create-maintenance-budget.md).) You can recalculate and adjust maintenance budget lines until the maintenance budget is approved.</span></span> <span data-ttu-id="1df2e-106">Bütçe dönemi geçtikten ve maliyetler Varlık Yönetimine nakledildikten sonra bütçe satırlarını fiili maliyetlerle de güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-106">After the budget period has passed, and costs have been posted in Asset Management, you can also update the budget lines with actual costs.</span></span>

## <a name="recalculate-a-maintenance-budget"></a><span data-ttu-id="1df2e-107">Bakım bütçesini yeniden hesaplama</span><span class="sxs-lookup"><span data-stu-id="1df2e-107">Recalculate a maintenance budget</span></span>

<span data-ttu-id="1df2e-108">Bakım bütçesini **Bakım bütçesi satırları** sayfasında yeniden hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-108">You can recalculate a maintenance budget on the **Maintenance budget lines** page.</span></span> <span data-ttu-id="1df2e-109">Bakım bütçesini yeniden hesapladığınızda mevcut bütçe satırları silinir ve yeni bir hesaplama yapılır.</span><span class="sxs-lookup"><span data-stu-id="1df2e-109">When you recalculate a maintenance budget, the existing budget lines are deleted, and a new calculation is done.</span></span>

1. <span data-ttu-id="1df2e-110">**Bakım bütçesi satırları** sayfasında, **Yeniden hesapla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-110">On the **Maintenance budget lines** page, select **Recalculate**.</span></span>
2. <span data-ttu-id="1df2e-111">**Bütçeyi yeniden hesapla** iletişim kutusunda, yeni hesaplama için gerekli değişiklikleri yapın ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-111">In the **Recalculate budget** dialog box, make the required changes for the new calculation, and then select **OK**.</span></span>

<span data-ttu-id="1df2e-112">Yeni bütçe satırları, ayarladığınız değerlere göre oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="1df2e-112">New budget lines are created according to the values that you set.</span></span>

## <a name="adjust-budget-lines"></a><span data-ttu-id="1df2e-113">Bütçe satırlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="1df2e-113">Adjust budget lines</span></span>

<span data-ttu-id="1df2e-114">Tüm bakım bütçesini yeniden hesaplamak yerine bütçe maliyetleriyle ilgili seçili satırları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-114">Instead of recalculating the whole maintenance budget, you can adjust selected lines that are related to budget costs.</span></span>

1. <span data-ttu-id="1df2e-115">**Bakım bütçesi satırları** sayfasında, bütçe maliyetinin güncelleştirileceği satırları seçin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-115">On the **Maintenance budget lines** page, select the lines to update the budget cost for.</span></span>
2. <span data-ttu-id="1df2e-116">**Ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-116">Select **Adjust**.</span></span>
3. <span data-ttu-id="1df2e-117">Seçili satırlara bir miktar eklemek için **Maliyet ekle** onay kutusunu seçin ve ardından **Değer ekle** alanına değer girin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-117">To add an amount to the selected lines, select the **Add cost** check box, and then enter the value in the **Add value** field.</span></span>
4. <span data-ttu-id="1df2e-118">Seçilen bütçe satırlarında bütçe maliyetini bir katsayıyla çarpmak için **Maliyeti çarp** onay kutusunu seçin ve ardından **Değeri çarp** alanına katsayıyı girin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-118">To multiply the budget cost on the selected budget lines by a factor, select the **Multiply cost** check box, and enter the factor in the **Multiply value** field.</span></span>

    <span data-ttu-id="1df2e-119">Örneğin, **Değeri çarp** alanına **1,2** girerseniz seçili satırlardaki bütçe maliyetini yüzde 20 oranında artırırsınız.</span><span class="sxs-lookup"><span data-stu-id="1df2e-119">For example, if you enter **1.2** in the **Multiply value** field, you increase the budget cost on the selected lines by 20 percent.</span></span> <span data-ttu-id="1df2e-120">**0,7** girerseniz seçili satırlardaki bütçe maliyetini yüzde 30 oranında azaltırsınız.</span><span class="sxs-lookup"><span data-stu-id="1df2e-120">If you enter **0.7**, you reduce the budget cost on the selected lines by 30 percent.</span></span>

5. <span data-ttu-id="1df2e-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-121">Select **OK**.</span></span>

<span data-ttu-id="1df2e-122">Seçili bütçe satırları, adım 3 veya 4'te ayarladığınız değerlere göre güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1df2e-122">The selected budget lines are updated according to the values that you set in step 3 or 4.</span></span>

## <a name="update-actual-costs"></a><span data-ttu-id="1df2e-123">Fiili maliyetleri güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="1df2e-123">Update actual costs</span></span>

<span data-ttu-id="1df2e-124">Bütçe satırlarındaki tarihler geçtikten ve fiili maliyetler Varlık Yönetimine nakledildikten sonra bakım bütçesindeki fiili maliyetleri güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-124">After the dates on the budget lines have passed, and actual costs have been posted in Asset Management, you can update the actual costs on the maintenance budget.</span></span>

1. <span data-ttu-id="1df2e-125">**Bakım bütçesi satırları** sayfasında, **Maliyeti güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-125">On the **Maintenance budget lines** page, select **Update cost**.</span></span>
2. <span data-ttu-id="1df2e-126">**Fiili maliyeti hesapla** iletişim kutusunda, **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="1df2e-126">In the **Calculate actual cost** dialog box, select **OK**.</span></span>

<span data-ttu-id="1df2e-127">Fiili maliyetler nakledilmişse bütçe satırlarındaki **Fiili maliyet** alanları güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1df2e-127">The **Actual cost** fields on the budget lines are updated if actual costs have been posted.</span></span> <span data-ttu-id="1df2e-128">Bütçeyi oluşturduktan sonra yeni varlık türleri oluşturulmuşsa ve bu varlık türleri, iş emirlerinin oluşturulduğu ve ilgili maliyetlerin nakledildiği varlıklarda kullanılmışsa yeni bütçe satırları oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="1df2e-128">New budget lines might be generated if new asset types have been created since you created the budget, and if those asset types have been used on assets that work orders have been created for and related costs have been posted for.</span></span> <span data-ttu-id="1df2e-129">Yeni bütçe satırları bunlar için bütçe maliyetleri hesaplanmadığından yalnızca fiili maliyetleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="1df2e-129">New budget lines show only actual costs, because no budget costs were calculated for them.</span></span>

> [!NOTE]
> <span data-ttu-id="1df2e-130">Önleyici, düzeltici ve yatırım maliyetlerine bölünmüş fiili maliyetlere genel bakışı görmek için **Varlık maliyeti denetimi** sayfasında aynı dönem için bir hesaplama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-130">To see an overview of actual costs divided into preventive, corrective, and investment costs, you can do a calculation for the same period on the **Asset cost control** page.</span></span> 

## <a name="manually-add-budget-lines"></a><span data-ttu-id="1df2e-131">Bütçe satırlarını el ile ekleme</span><span class="sxs-lookup"><span data-stu-id="1df2e-131">Manually add budget lines</span></span>

<span data-ttu-id="1df2e-132">**Bakım bütçesi satırları** sayfasında, **Yeni**'yi seçerek ve satır üzerinde seçimler yaparak el ile yeni bir bütçe satırı ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-132">On the **Maintenance budget lines** page, you can manually add a new budget line by selecting **New** and then making selections on the line.</span></span> <span data-ttu-id="1df2e-133">Bu yaklaşımın yararlı olabileceği durumlara yönelik birkaç örnek aşağıda gösterilmiştir:</span><span class="sxs-lookup"><span data-stu-id="1df2e-133">Here are some examples of situations where this approach might be useful:</span></span>

- <span data-ttu-id="1df2e-134">Bazı varlıkların yenilenmesinin şu anda planlama aşamasında olduğunu biliyorsunuz ancak ilgili işler henüz Varlık Yönetiminde oluşturulmadı.</span><span class="sxs-lookup"><span data-stu-id="1df2e-134">You know that refurbishment of some assets is currently in the planning phase, but related jobs haven't yet been created in Asset Management.</span></span> <span data-ttu-id="1df2e-135">Ancak bu işlerin bütçe maliyetlerinin bakım bütçesine dahil edilmesini istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-135">However, you want budget costs for those jobs to be included in the maintenance budget.</span></span>
- <span data-ttu-id="1df2e-136">Bakım bütçesi yaptığınız tarihten itibaren yeni varlıklar veya varlık türleri oluşturuldu ancak bakım planları henüz bu varlıklar veya varlık türlerinde ayarlanmadı.</span><span class="sxs-lookup"><span data-stu-id="1df2e-136">New assets or asset types have been created since you made the maintenance budget, but maintenance plans haven't yet been set up on those assets or asset types.</span></span> <span data-ttu-id="1df2e-137">Ancak bu varlık türlerinin bütçe maliyetlerinin bakım bütçesine dahil edilmesini istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="1df2e-137">However, you want budget costs for those asset types to be included in the maintenance budget.</span></span>
