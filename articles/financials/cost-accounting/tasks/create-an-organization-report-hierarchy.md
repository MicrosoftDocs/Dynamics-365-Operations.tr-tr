---
title: Kuruluş raporu hiyerarşisi oluşturma
description: Bu yordamı bir kuruluş raporlaması için bir raporlama hiyerarşisi oluşturmak üzere kullanın.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9a06a67f851e4a73df90f999683d5ea27f38e66
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "365512"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="288a4-103">Kuruluş raporu hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="288a4-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="288a4-104">Bu yordamı bir kuruluş raporlaması için bir raporlama hiyerarşisi oluşturmak üzere kullanın.</span><span class="sxs-lookup"><span data-stu-id="288a4-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="288a4-105">Bu kaydın amacı, tüm kuruluşun raporlama yapısı oluşturulana kadar devam etmenizi sağlamak için boyut hiyerarşisinde size kılavuzluk etmektir.</span><span class="sxs-lookup"><span data-stu-id="288a4-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="288a4-106">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="288a4-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="288a4-107">Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="288a4-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="288a4-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-108">Click New.</span></span>
3. <span data-ttu-id="288a4-109">HierarchyTypeComboBox alanında 'Boyut sınıflandırma hiyerarşisi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="288a4-110">Boyut sınıflandırması hiyerarşisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="288a4-111">Boyut sınıflandırma hiyerarşisi türü kuralları tanımlamak ve raporlama amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="288a4-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="288a4-112">Maliyet nesneleri, maliyet öğeleri ve istatistiksel boyutlar gibi tüm boyutları destekler.</span><span class="sxs-lookup"><span data-stu-id="288a4-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="288a4-113">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-113">Click Create.</span></span>
5. <span data-ttu-id="288a4-114">Boyut hiyerarşisi adı alanına 'Kuruluş USP2' girin.</span><span class="sxs-lookup"><span data-stu-id="288a4-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="288a4-115">Boyut alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="288a4-116">Maliyet Merkezleri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="288a4-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-117">Click Save.</span></span>
8. <span data-ttu-id="288a4-118">Hiyerarşiyi görüntüle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="288a4-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-119">Click New.</span></span>
10. <span data-ttu-id="288a4-120">Düğüm adı alanına 'CEO' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="288a4-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-121">Click Save.</span></span>
12. <span data-ttu-id="288a4-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-122">Click New.</span></span>
13. <span data-ttu-id="288a4-123">Düğüm adı alanına 'CEO maliyet merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="288a4-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-124">Click Save.</span></span>
15. <span data-ttu-id="288a4-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-125">Click New.</span></span>
16. <span data-ttu-id="288a4-126">Düğüm adı alanına 'Bölge Doğu' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="288a4-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-127">Click Save.</span></span>
18. <span data-ttu-id="288a4-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-128">Click New.</span></span>
19. <span data-ttu-id="288a4-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="288a4-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="288a4-130">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="288a4-131">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="288a4-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-132">Click Save.</span></span>
22. <span data-ttu-id="288a4-133">Ağaçta 'Kuruluş USP2\CEO\CEO maliyet merkezleri' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="288a4-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-134">Click New.</span></span>
24. <span data-ttu-id="288a4-135">Düğüm adı alanına 'Bölge Batı' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="288a4-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-136">Click Save.</span></span>
26. <span data-ttu-id="288a4-137">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-137">Click New.</span></span>
27. <span data-ttu-id="288a4-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="288a4-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="288a4-139">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="288a4-140">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="288a4-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-141">Click Save.</span></span>
30. <span data-ttu-id="288a4-142">Ağaçta 'Kuruluş USP2\CEO' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="288a4-143">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-143">Click New.</span></span>
32. <span data-ttu-id="288a4-144">Düğüm adı alanına 'CFO maliyet merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="288a4-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-145">Click Save.</span></span>
34. <span data-ttu-id="288a4-146">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-146">Click New.</span></span>
35. <span data-ttu-id="288a4-147">Düğüm adı alanına 'Pazarlama kampa' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="288a4-148">Düğüm adı alanına 'Pazarlama kampanyası' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="288a4-149">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-149">Click Save.</span></span>
38. <span data-ttu-id="288a4-150">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-150">Click New.</span></span>
39. <span data-ttu-id="288a4-151">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="288a4-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="288a4-152">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="288a4-153">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="288a4-154">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-154">Click Save.</span></span>
42. <span data-ttu-id="288a4-155">Ağaçta 'Kuruluş USP2\CEO\CFO maliyet merkezleri' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="288a4-156">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-156">Click New.</span></span>
44. <span data-ttu-id="288a4-157">Düğüm adı alanına 'Ticaret sergisi' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="288a4-158">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-158">Click Save.</span></span>
46. <span data-ttu-id="288a4-159">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-159">Click New.</span></span>
47. <span data-ttu-id="288a4-160">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="288a4-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="288a4-161">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="288a4-162">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="288a4-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-163">Click Save.</span></span>
50. <span data-ttu-id="288a4-164">Ağaçta 'Kuruluş USP2\CEO' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="288a4-165">Düğüm adı alanına 'CIO maliyet merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="288a4-166">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-166">Click Save.</span></span>
53. <span data-ttu-id="288a4-167">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-167">Click New.</span></span>
54. <span data-ttu-id="288a4-168">Düğüm adı alanına 'Çağrı merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="288a4-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="288a4-169">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-169">Click Save.</span></span>
56. <span data-ttu-id="288a4-170">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-170">Click New.</span></span>
57. <span data-ttu-id="288a4-171">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="288a4-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="288a4-172">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="288a4-173">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="288a4-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="288a4-174">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="288a4-174">Click Save.</span></span>

