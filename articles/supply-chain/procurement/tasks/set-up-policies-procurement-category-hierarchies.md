--- 
title: "Tedarik kategorisi hiyerarşileri için ilkeler ayarlama"
description: "Bir kategorideki ürünleri sipariş etmek amacıyla kuralları ayarlamak için bu prosedürü kullanın."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 1c5e4b70897af5e45350d1b3766fc1d303a36ea1
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="48dfd-103">Tedarik kategorisi hiyerarşileri için ilkeler ayarlama</span><span class="sxs-lookup"><span data-stu-id="48dfd-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48dfd-104">Bir kategorideki ürünleri sipariş etmek amacıyla kuralları ayarlamak için bu prosedürü kullanın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="48dfd-105">Kurallar belirli bir satın alma ilkesi için tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="48dfd-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="48dfd-106">Kategori erişimi kuralı, talep oluşturulduğunda hangi tedarik kategorisi çalışanlarının erişime sahip olacağını denetler.</span><span class="sxs-lookup"><span data-stu-id="48dfd-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="48dfd-107">Bir talep oluşturulduktan sonra uygulanması gereken satınalma ilkesi ve kategori erişim kuralı çalışanların bağlı olduğu tüzel kişilik ve işletme birimi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="48dfd-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="48dfd-108">Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="48dfd-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="48dfd-109">Genellikle bu görev bir satınalma yöneticisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="48dfd-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="48dfd-110">Tedarik ilkesini bulun</span><span class="sxs-lookup"><span data-stu-id="48dfd-110">Find the procurement policy</span></span>
1. <span data-ttu-id="48dfd-111">Tedarik ve kaynak atama > Ayarlar > İlkeler > Satınalma ilkeleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="48dfd-112">Tedarik İlkesi USMF'deki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="48dfd-113">Bu, kuralı ekleyeceğiniz ilkedir.</span><span class="sxs-lookup"><span data-stu-id="48dfd-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="48dfd-114">Etkin ilke olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="48dfd-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="48dfd-115">Kategori erişimi kuralı oluşturun</span><span class="sxs-lookup"><span data-stu-id="48dfd-115">Create a category access rule</span></span>
1. <span data-ttu-id="48dfd-116">Kategori erişimi ilke kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="48dfd-117">İlke kuralı oluştur düğmesi soluk görünüyorsa bunun nedeni Kategori erişimi için zaten etkin bir ilke kuralının olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="48dfd-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="48dfd-118">Hangisi olduğunu belirlemek için Yürürlük ve Bitiş tarihi alanlarını işaretleyin, sonra seçin ve İlke kuralını kullanımdan kaldır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="48dfd-119">İlke kuralı oluştur düğmesi kullanılabilir durumdaysa başka bir işlem yapmanız gerekmez.</span><span class="sxs-lookup"><span data-stu-id="48dfd-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="48dfd-120">İlke kuralı oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="48dfd-121">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="48dfd-122">Süre zaten etkin olan başka bir kuralla çakışmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="48dfd-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="48dfd-123">Kuralın uygulanacağı bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="48dfd-124">Bunun hangi kategori olduğunu not edin, daha sonra ihtiyacınız olacak.</span><span class="sxs-lookup"><span data-stu-id="48dfd-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="48dfd-125">Bir kategori seçtiğinizde, üst kategorisi veya kategorileri de Seçili kategoriler listesine eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="48dfd-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="48dfd-126">Kuralı seçili kategorinin tüm alt kategorilerine uygulamak istiyorsanız alt kategorileri dahil et onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="48dfd-127">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-127">Click Add.</span></span>
    * <span data-ttu-id="48dfd-128">Üst kuralı dahil et seçeneğini Evet olarak ayarlarsanız üst kategori için tanımladığınız ilke kuralı, alt kategoriler için ilke kuralı tanımlanmamışsa alt kategorilerine de atanır.</span><span class="sxs-lookup"><span data-stu-id="48dfd-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="48dfd-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="48dfd-130">Kategori ilkesi kuralı oluşturun</span><span class="sxs-lookup"><span data-stu-id="48dfd-130">Create a category policy rule</span></span>
1. <span data-ttu-id="48dfd-131">Kategori ilke kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="48dfd-132">İlke kuralı oluştur düğmesi soluksa etkin ilke kuralını seçin ve İlke kuralını kullanımdan kaldır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="48dfd-133">İlke kuralı oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="48dfd-134">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="48dfd-135">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-135">Click Add.</span></span>
5. <span data-ttu-id="48dfd-136">Kategori erişimi kuralı için kullandığınız aynı kategoriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="48dfd-137">Satıcı seçimi alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="48dfd-138">Talepler oluşturulduğunda kategori için hangi tür satıcıların seçilebileceğini denetleyen bir kural seçin.</span><span class="sxs-lookup"><span data-stu-id="48dfd-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="48dfd-139">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="48dfd-139">Click Close.</span></span>
    * <span data-ttu-id="48dfd-140">Tanımladığınız ilke kuralları Tüketim türü talepleri içindir.</span><span class="sxs-lookup"><span data-stu-id="48dfd-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="48dfd-141">Stok yenileme türü talepleri için ilkeleri tanımlamak isterseniz "Stok yenileme kategorisi erişim ilkesi kuralı" olarak adlandırılan İlke kuralı türü için bir kural oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="48dfd-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  


