--- 
title: "Otomatik navlun mutabakatını ayarlama"
description: "Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir."
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d990efd7c929b15d57d64e850bc3308349abb978
ms.openlocfilehash: b7772ad779495b36941a3dc86cc456d80a964467
ms.contentlocale: tr-tr
ms.lasthandoff: 10/17/2018

---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="e456f-103">Otomatik navlun mutabakatını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e456f-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e456f-104">Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e456f-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="e456f-105">Bu, genellikle ambar yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="e456f-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="e456f-106">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e456f-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="e456f-107">Navlun fatura türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="e456f-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="e456f-108">Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Navlun faturası türü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e456f-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="e456f-109">Navlun fatura kodu, navlun faturalarının ve taşıyıcı faturalarının nasıl eşleştirilmesi gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e456f-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="e456f-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e456f-110">Click New.</span></span>
3. <span data-ttu-id="e456f-111">Navlun faturası türü alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e456f-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="e456f-112">Altyapı grubu alanına "Microsoft.Dynamics.Ax.Tms.dll" yazın.</span><span class="sxs-lookup"><span data-stu-id="e456f-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="e456f-113">Bu, altyapı kodu kitaplığını eşleştiren standart Taşıma yönetimidir.</span><span class="sxs-lookup"><span data-stu-id="e456f-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="e456f-114">Altyapı sınıfı alanına "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer" yazın.</span><span class="sxs-lookup"><span data-stu-id="e456f-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="e456f-115">Bu, altyapı sınıfını eşleştiren standart Taşıma yönetimidir.</span><span class="sxs-lookup"><span data-stu-id="e456f-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="e456f-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e456f-116">Click New.</span></span>
7. <span data-ttu-id="e456f-117">Açıklama alanında, navlun faturası ve taşıyıcı faturasında eşleşmesi gereken değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="e456f-118">Eşleşme gerekli alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="e456f-119">Bu alanı Evet olarak ayarlarsanız bu, Tanımlama alanında seçilen değerin, navlun faturası ve taşıyıcı fatura ile eşleşmesi gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="e456f-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="e456f-120">Hayır olarak ayarlarsanız alan bunların birinde boş kalabilir.</span><span class="sxs-lookup"><span data-stu-id="e456f-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="e456f-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e456f-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="e456f-122">Navlun fatura türü atamasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="e456f-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="e456f-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e456f-123">Close the page.</span></span>
2. <span data-ttu-id="e456f-124">Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Navlun fatura türü atamaları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e456f-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="e456f-125">Navlun fatura türü atamaları, belirli bir taşıyıcı için hangi navlun faturası türünün kullanıldığını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e456f-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="e456f-126">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e456f-126">Click New.</span></span>
4. <span data-ttu-id="e456f-127">Mod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="e456f-128">Sevkiyat taşıyıcısı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="e456f-129">Navlun fatura türü alanında daha önce oluşturduğunuz navlun fatura türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="e456f-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e456f-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="e456f-131">Ana denetimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="e456f-131">Set up the audit master</span></span>
1. <span data-ttu-id="e456f-132">Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Ana denetim'e gidin.</span><span class="sxs-lookup"><span data-stu-id="e456f-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="e456f-133">Ana denetim, otomatik navlun mutabakatı için tolerans sınırlarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e456f-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="e456f-134">Navlun faturası ve taşıyıcı faturasında parasal tutarların ne kadar değiştiğini belirtir ve yine de mutabakatın gerçekleşmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="e456f-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="e456f-135">Ayrıca tutarsızlıkların nasıl ele alınacağını da tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e456f-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="e456f-136">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="e456f-136">Click New.</span></span>
3. <span data-ttu-id="e456f-137">Ana denetim kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e456f-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="e456f-138">Sevkiyat taşıyıcısı alanında önceden seçtiğiniz gibi sevkiyat taşıyıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="e456f-139">Navlun fatura türü alanında daha önce oluşturduğunuz navlun fatura türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="e456f-140">Tolerans bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e456f-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="e456f-141">Minimum tolerans düzeyi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e456f-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="e456f-142">Maksimum tolerans düzeyi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="e456f-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="e456f-143">Sonuç bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="e456f-143">Expand the Result section.</span></span>
10. <span data-ttu-id="e456f-144">Fazla ödeme neden kodu alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="e456f-145">Parasal tutarlar navlun faturasında ve taşıyıcı faturasında farklılık gösterirse fazla ödeme ve eksik ödeme neden kodları, farklılıklar tolerans düzeyleri içinde kaldığı sürece farklılıkların kaydedilmesinin gerekli olduğu hesapları belirtir.</span><span class="sxs-lookup"><span data-stu-id="e456f-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="e456f-146">Eksik ödeme neden kodu alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="e456f-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="e456f-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e456f-147">Close the page.</span></span>


