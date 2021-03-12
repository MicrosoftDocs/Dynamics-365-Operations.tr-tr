---
title: Otomatik navlun mutabakatını ayarlama
description: Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bfd96fcae78fd0fe383781112c17c7a3b5ea1d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974022"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="99874-103">Otomatik navlun mutabakatını ayarlama</span><span class="sxs-lookup"><span data-stu-id="99874-103">Set up automatic freight reconciliation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99874-104">Bu yordam, otomatik navlun mutabakatı için verilerin nasıl ayarlanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99874-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="99874-105">Bu, genellikle ambar yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="99874-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="99874-106">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="99874-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="99874-107">Navlun fatura türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="99874-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="99874-108">Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Navlun faturası türü'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="99874-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="99874-109">Navlun fatura kodu, navlun faturalarının ve taşıyıcı faturalarının nasıl eşleştirilmesi gerektiğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="99874-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="99874-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99874-110">Click New.</span></span>
3. <span data-ttu-id="99874-111">Navlun faturası türü alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="99874-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="99874-112">Altyapı grubu alanına "Microsoft.Dynamics.Ax.Tms.dll" yazın.</span><span class="sxs-lookup"><span data-stu-id="99874-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="99874-113">Bu, altyapı kodu kitaplığını eşleştiren standart Taşıma yönetimidir.</span><span class="sxs-lookup"><span data-stu-id="99874-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="99874-114">Altyapı sınıfı alanına "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer" yazın.</span><span class="sxs-lookup"><span data-stu-id="99874-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="99874-115">Bu, altyapı sınıfını eşleştiren standart Taşıma yönetimidir.</span><span class="sxs-lookup"><span data-stu-id="99874-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="99874-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99874-116">Click New.</span></span>
7. <span data-ttu-id="99874-117">Açıklama alanında, navlun faturası ve taşıyıcı faturasında eşleşmesi gereken değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="99874-118">Eşleşme gerekli alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="99874-119">Bu alanı Evet olarak ayarlarsanız bu, Tanımlama alanında seçilen değerin, navlun faturası ve taşıyıcı fatura ile eşleşmesi gerektiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="99874-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="99874-120">Hayır olarak ayarlarsanız alan bunların birinde boş kalabilir.</span><span class="sxs-lookup"><span data-stu-id="99874-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="99874-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99874-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="99874-122">Navlun fatura türü atamasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="99874-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="99874-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99874-123">Close the page.</span></span>
2. <span data-ttu-id="99874-124">Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Navlun fatura türü atamaları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="99874-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="99874-125">Navlun fatura türü atamaları, belirli bir taşıyıcı için hangi navlun faturası türünün kullanıldığını tanımlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99874-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="99874-126">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99874-126">Click New.</span></span>
4. <span data-ttu-id="99874-127">Mod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="99874-128">Sevkiyat taşıyıcısı alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="99874-129">Navlun fatura türü alanında daha önce oluşturduğunuz navlun fatura türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="99874-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99874-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="99874-131">Ana denetimi ayarlama</span><span class="sxs-lookup"><span data-stu-id="99874-131">Set up the audit master</span></span>
1. <span data-ttu-id="99874-132">Taşımacılık yönetimi > Kurulum > Navlun mutabakatı > Ana denetim'e gidin.</span><span class="sxs-lookup"><span data-stu-id="99874-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="99874-133">Ana denetim, otomatik navlun mutabakatı için tolerans sınırlarını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="99874-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="99874-134">Navlun faturası ve taşıyıcı faturasında parasal tutarların ne kadar değiştiğini belirtir ve yine de mutabakatın gerçekleşmesine izin verir.</span><span class="sxs-lookup"><span data-stu-id="99874-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="99874-135">Ayrıca tutarsızlıkların nasıl ele alınacağını da tanımlar.</span><span class="sxs-lookup"><span data-stu-id="99874-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="99874-136">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="99874-136">Click New.</span></span>
3. <span data-ttu-id="99874-137">Ana denetim kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="99874-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="99874-138">Sevkiyat taşıyıcısı alanında önceden seçtiğiniz gibi sevkiyat taşıyıcısını seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="99874-139">Navlun fatura türü alanında daha önce oluşturduğunuz navlun fatura türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="99874-140">Tolerans bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="99874-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="99874-141">Minimum tolerans düzeyi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="99874-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="99874-142">Maksimum tolerans düzeyi alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="99874-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="99874-143">Sonuç bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="99874-143">Expand the Result section.</span></span>
10. <span data-ttu-id="99874-144">Fazla ödeme neden kodu alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="99874-145">Parasal tutarlar navlun faturasında ve taşıyıcı faturasında farklılık gösterirse fazla ödeme ve eksik ödeme neden kodları, farklılıklar tolerans düzeyleri içinde kaldığı sürece farklılıkların kaydedilmesinin gerekli olduğu hesapları belirtir.</span><span class="sxs-lookup"><span data-stu-id="99874-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="99874-146">Eksik ödeme neden kodu alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="99874-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="99874-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="99874-147">Close the page.</span></span>

