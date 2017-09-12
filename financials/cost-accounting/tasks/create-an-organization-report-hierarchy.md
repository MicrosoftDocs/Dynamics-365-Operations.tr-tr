--- 
title: "Kuruluş raporu hiyerarşisi oluşturma"
description: "Bu yordamı bir kuruluş raporlaması için bir raporlama hiyerarşisi oluşturmak üzere kullanın."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f593c59660abcf5b0d5771ddd9daced6ec5fbfb4
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="bafe0-103">Kuruluş raporu hiyerarşisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="bafe0-103">Create an organization report hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bafe0-104">Bu yordamı bir kuruluş raporlaması için bir raporlama hiyerarşisi oluşturmak üzere kullanın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="bafe0-105">Bu kaydın amacı, tüm kuruluşun raporlama yapısı oluşturulana kadar devam etmenizi sağlamak için boyut hiyerarşisinde size kılavuzluk etmektir.</span><span class="sxs-lookup"><span data-stu-id="bafe0-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="bafe0-106">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bafe0-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="bafe0-107">Maliyet muhasebesi > Boyutlar > Boyut hiyerarşileri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="bafe0-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-108">Click New.</span></span>
3. <span data-ttu-id="bafe0-109">HierarchyTypeComboBox alanında 'Boyut sınıflandırma hiyerarşisi' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="bafe0-110">Boyut sınıflandırması hiyerarşisi'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="bafe0-111">Boyut sınıflandırma hiyerarşisi türü kuralları tanımlamak ve raporlama amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bafe0-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="bafe0-112">Maliyet nesneleri, maliyet öğeleri ve istatistiksel boyutlar gibi tüm boyutları destekler.</span><span class="sxs-lookup"><span data-stu-id="bafe0-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="bafe0-113">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-113">Click Create.</span></span>
5. <span data-ttu-id="bafe0-114">Boyut hiyerarşisi adı alanına 'Kuruluş USP2' girin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="bafe0-115">Boyut alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="bafe0-116">Maliyet Merkezleri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="bafe0-117">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-117">Click Save.</span></span>
8. <span data-ttu-id="bafe0-118">Hiyerarşiyi görüntüle düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="bafe0-119">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-119">Click New.</span></span>
10. <span data-ttu-id="bafe0-120">Düğüm adı alanına 'CEO' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="bafe0-121">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-121">Click Save.</span></span>
12. <span data-ttu-id="bafe0-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-122">Click New.</span></span>
13. <span data-ttu-id="bafe0-123">Düğüm adı alanına 'CEO maliyet merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="bafe0-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-124">Click Save.</span></span>
15. <span data-ttu-id="bafe0-125">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-125">Click New.</span></span>
16. <span data-ttu-id="bafe0-126">Düğüm adı alanına 'Bölge Doğu' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="bafe0-127">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-127">Click Save.</span></span>
18. <span data-ttu-id="bafe0-128">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-128">Click New.</span></span>
19. <span data-ttu-id="bafe0-129">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="bafe0-130">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="bafe0-131">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="bafe0-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-132">Click Save.</span></span>
22. <span data-ttu-id="bafe0-133">Ağaçta 'Kuruluş USP2\CEO\CEO maliyet merkezleri' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="bafe0-134">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-134">Click New.</span></span>
24. <span data-ttu-id="bafe0-135">Düğüm adı alanına 'Bölge Batı' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="bafe0-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-136">Click Save.</span></span>
26. <span data-ttu-id="bafe0-137">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-137">Click New.</span></span>
27. <span data-ttu-id="bafe0-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="bafe0-139">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="bafe0-140">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="bafe0-141">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-141">Click Save.</span></span>
30. <span data-ttu-id="bafe0-142">Ağaçta 'Kuruluş USP2\CEO' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="bafe0-143">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-143">Click New.</span></span>
32. <span data-ttu-id="bafe0-144">Düğüm adı alanına 'CFO maliyet merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="bafe0-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-145">Click Save.</span></span>
34. <span data-ttu-id="bafe0-146">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-146">Click New.</span></span>
35. <span data-ttu-id="bafe0-147">Düğüm adı alanına 'Pazarlama kampa' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="bafe0-148">Düğüm adı alanına 'Pazarlama kampanyası' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="bafe0-149">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-149">Click Save.</span></span>
38. <span data-ttu-id="bafe0-150">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-150">Click New.</span></span>
39. <span data-ttu-id="bafe0-151">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="bafe0-152">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="bafe0-153">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="bafe0-154">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-154">Click Save.</span></span>
42. <span data-ttu-id="bafe0-155">Ağaçta 'Kuruluş USP2\CEO\CFO maliyet merkezleri' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-155">In the tree, select 'Oganization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="bafe0-156">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-156">Click New.</span></span>
44. <span data-ttu-id="bafe0-157">Düğüm adı alanına 'Ticaret sergisi' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="bafe0-158">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-158">Click Save.</span></span>
46. <span data-ttu-id="bafe0-159">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-159">Click New.</span></span>
47. <span data-ttu-id="bafe0-160">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="bafe0-161">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="bafe0-162">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="bafe0-163">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-163">Click Save.</span></span>
50. <span data-ttu-id="bafe0-164">Ağaçta 'Kuruluş USP2\CEO' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="bafe0-165">Düğüm adı alanına 'CIO maliyet merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="bafe0-166">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-166">Click Save.</span></span>
53. <span data-ttu-id="bafe0-167">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-167">Click New.</span></span>
54. <span data-ttu-id="bafe0-168">Düğüm adı alanına 'Çağrı merkezleri' yazın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="bafe0-169">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-169">Click Save.</span></span>
56. <span data-ttu-id="bafe0-170">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-170">Click New.</span></span>
57. <span data-ttu-id="bafe0-171">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="bafe0-172">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="bafe0-173">Düğüme karşılık gelen boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bafe0-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="bafe0-174">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bafe0-174">Click Save.</span></span>


