---
title: Satınalma ilkeleri oluşturma
description: Bu konu satınalma için iş süreçlerinize uygun olacak şekilde satınalma ilkelerinin nasıl oluşturulacağını gösterir.
author: mkirknel
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8416f9a869b9144a63a6fb08c667cc32dec9854
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149723"
---
# <a name="create-purchasing-policies"></a><span data-ttu-id="e23f4-103">Satınalma ilkeleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="e23f4-103">Create purchasing policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e23f4-104">Bu konu satınalma için iş süreçlerinize uygun olacak şekilde satınalma ilkelerinin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e23f4-104">This topic shows you how to create purchasing policies to align with your business processes for purchasing.</span></span> <span data-ttu-id="e23f4-105">Satınalma ilkelerini oluşturmadan önce satın alma ilkesi parametrelerini ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e23f4-105">Before you can create purchasing policies, you must set up the purchasing policy parameters.</span></span> <span data-ttu-id="e23f4-106">Bir satınalma ilkesini oluşturmak, değiştirmek ve çıkarmak mümkündür ancak satınalma ilkesini silemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-106">It's possible to create, modify, and retire a purchasing policy, but you can't delete a purchasing policy.</span></span> <span data-ttu-id="e23f4-107">Bu prosedür genellikle bir satınalma yöneticisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e23f4-107">This procedure would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="e23f4-108">Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-108">You can use this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-policy-parameters"></a><span data-ttu-id="e23f4-109">İlke parametrelerini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="e23f4-109">Set up policy parameters</span></span>
1. <span data-ttu-id="e23f4-110">Gezinti bölmesinde **Modüller > Tedarik ve kaynak atama > Ayar > İlkeler > Satınalma ilkeleri**.</span><span class="sxs-lookup"><span data-stu-id="e23f4-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="e23f4-111">Eylem Bölmesinde, **Parametreler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-111">In the Action Pane, select **Parameters**.</span></span>
- <span data-ttu-id="e23f4-112">İlke önceliği kuralları kuruluşunuzdaki farklı düzeylere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="e23f4-112">Policy precedence rules apply to different levels in your organization.</span></span> <span data-ttu-id="e23f4-113">Kuruluş hiyerarşinize göre gösterilen kuruluş birimleri ve Tedarik dahili kontrolü amacına atanan hiyerarşideki düzeyler.</span><span class="sxs-lookup"><span data-stu-id="e23f4-113">The organizational units that are shown depend on your organizational hierarchy, and on which levels in the hierarchy have been assigned the purpose of Procurement internal control.</span></span> <span data-ttu-id="e23f4-114">Örneğin, kuruluşunuzun yasal varlıkları, maliyet merkezleri, bölgeleri ve departmanları olabilir, ancak yalnızca bazıları Tedarik dahili kontrolünün hiyerarşi amacına sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="e23f4-114">For example, your organization might have legal entities, cost centers, regions, and departments, but it may be that only some of these have a hierarchy purpose of Procurement internal control.</span></span> <span data-ttu-id="e23f4-115">Varsayılan olarak, kuruluşun Şirket türü kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e23f4-115">As a default, the organization of type Company is available.</span></span>  
3. <span data-ttu-id="e23f4-116">**İlke kuralı türü parametreleri** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-116">Select the **Policy rule type parameters** tab.</span></span>
4. <span data-ttu-id="e23f4-117">Ağaçta, **Satınalma ilkesi > Satınalma talebi kontrol kuralı**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-117">In the tree, go to **Purchasing policy > Purchase requisition control rule**.</span></span>
- <span data-ttu-id="e23f4-118">İlke düzeyinde ilke çözümü için öncelik sırasını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="e23f4-118">You define the order of precedence for policy resolution at the policy level.</span></span> <span data-ttu-id="e23f4-119">Ancak, bazı ilke türleri için tek tek ilke kuralı türlerine ilişkin öncelik sırasını geçersiz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-119">However, for some policy types, you can override the order of precedence for individual policy rule types.</span></span> <span data-ttu-id="e23f4-120">Örneğin, satınalma ilkeleri için öncelik sırasını maliyet merkezi, departman, şirket olarak tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-120">For example, you might define the order of precedence for purchasing policies to be: cost center, department, company.</span></span> <span data-ttu-id="e23f4-121">Katalog ilke kuralı için öncelik sırasını departman, maliyet merkezi, şirket olarak tanımlamak isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-121">For the catalog policy rule, you might want the order of precedence to be: department, cost center, company.</span></span> <span data-ttu-id="e23f4-122">Katalog ilke kuralı için öncelik sırasını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-122">You can change the order of precedence for the Catalog policy rule.</span></span> <span data-ttu-id="e23f4-123">Bir çalışan talep oluşturduğunda görüntülenecek katalog çalışanın departmanı, sonra maliyet merkezi ve son olarak şirketiyle ilişkili ilkeler tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="e23f4-123">When a worker creates a requisition, the catalog that is displayed is determined by the policies that are associated with the worker's department, then their cost center, and then their company.</span></span>  
- <span data-ttu-id="e23f4-124">Birden fazla organizasyon düzeyi listelenmişse Satınalma talebi kontrol kuralı için öncelik sırasını ayarlamak amacıyla Yukarı/Aşağı okları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-124">If there's more than one organizational level listed, you can use the Up/Down arrows to set the order of precedence for the Purchase requisition control rule.</span></span>  
5. <span data-ttu-id="e23f4-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e23f4-125">Close the page.</span></span>

## <a name="create-a-new-policy"></a><span data-ttu-id="e23f4-126">Yeni bir ilke oluştur</span><span class="sxs-lookup"><span data-stu-id="e23f4-126">Create a new policy</span></span>
1. <span data-ttu-id="e23f4-127">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-127">Select **New**.</span></span>
2. <span data-ttu-id="e23f4-128">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e23f4-128">In the **Name** field, type a value.</span></span>
3. <span data-ttu-id="e23f4-129">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-129">In the **Description** field, type a value.</span></span>
- <span data-ttu-id="e23f4-130">Tek bir satın alma ilkesini yalnızca bir kuruluş hiyerarşisine uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-130">A single purchasing policy can only apply to one organization hierarchy.</span></span> <span data-ttu-id="e23f4-131">Örneğin, 'Coğrafi' olarak ve "Bölüm" olarak adlandırılan bir hiyerarşiye sahipseniz her biri için farklı bir satın alma ilkesi vardır.</span><span class="sxs-lookup"><span data-stu-id="e23f4-131">For example, you could have one hierarchy called "Geographic" and one called "Department", and have a different purchasing policy for each.</span></span>  
- <span data-ttu-id="e23f4-132">İlkenin uygulanması gereken bir kuruluş seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-132">Select an organization that the policy should apply to.</span></span>  
4. <span data-ttu-id="e23f4-133">Seçilen kuruluşu eklemek için oku seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-133">Select the arrow to add the selected organization.</span></span>
- <span data-ttu-id="e23f4-134">Daha fazla kuruluş eklemek için bu işlemi yineleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-134">You can repeat this process to add more organizations.</span></span>  

## <a name="add-a-policy-rule"></a><span data-ttu-id="e23f4-135">İlke kuralı ekleyin</span><span class="sxs-lookup"><span data-stu-id="e23f4-135">Add a policy rule</span></span>
1. <span data-ttu-id="e23f4-136">**İlke kuralı türü** listesinde **Talep amacı kuralı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-136">In the **Policy rule type** list, select **Requisition purpose rule**.</span></span>
- <span data-ttu-id="e23f4-137">Varsayılan talep amacını Tüketim türüne ayarlayan ancak bunun yerine seçilecek Stok yenileme türüne izin veren bir kural oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="e23f4-137">You'll create a rule that sets the default requisition purpose to type Consumption but allows the Replenishment type to be selected instead.</span></span>  
2. <span data-ttu-id="e23f4-138">**İlke kuralı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-138">Select **Create policy rule**.</span></span>
3. <span data-ttu-id="e23f4-139">**El ile geçersiz kılmaya izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-139">Select **Yes** in the **Allow manual override** field.</span></span>
4. <span data-ttu-id="e23f4-140">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-140">Select **Close**.</span></span>
- <span data-ttu-id="e23f4-141">Şimdi satın alma ilkesi için diğer ilke kurallarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e23f4-141">Now you can set up other policy rules for the purchasing policy.</span></span> <span data-ttu-id="e23f4-142">İlke kuralı türünün tek bir tedarik ilkesi ile aynı sürede etkin olan çakışan kurallara sahip olamayacağına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="e23f4-142">Note that a Policy rule type cannot have overlapping rules that are active at the same time within a single procurement policy.</span></span>  

