---
title: Kaynak belgeler için denetim ilkeleri tanımlama
description: Bu konu, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını açıklar.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836973"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="7f758-103">Kaynak belgeler için denetim ilkeleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="7f758-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f758-104">Bu konu, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="7f758-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="7f758-105">Örnekte, otel gideri türünde gider raporları kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7f758-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="7f758-106">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7f758-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="7f758-107">Denetçi rolü bu görevleri gerçekleştirmek için uygun izinleri içerir.</span><span class="sxs-lookup"><span data-stu-id="7f758-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="7f758-108">Gezinti bölmesinde, **Modüller > Denetim çalışma ekranı > Kurulum > İlke kuralı türü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7f758-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="7f758-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-109">Select **New**.</span></span>
3. <span data-ttu-id="7f758-110">**Kural adı** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7f758-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="7f758-111">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7f758-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="7f758-112">**Sorgu adı** alanında **Gider raporu satırı** öğesini seçin</span><span class="sxs-lookup"><span data-stu-id="7f758-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="7f758-113">**Sorgu türü** alanında **Topla** öğesini seçin</span><span class="sxs-lookup"><span data-stu-id="7f758-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="7f758-114">**Tüzel kişilik** alanında **Tüzel kişilik** öğesini seçin</span><span class="sxs-lookup"><span data-stu-id="7f758-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="7f758-115">**Belge tarihi referansı** alanında **Değiştirilme tarihi ve saati** öğesini seçin</span><span class="sxs-lookup"><span data-stu-id="7f758-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="7f758-116">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-116">Select **Save**.</span></span>
10. <span data-ttu-id="7f758-117">Gezinti bölmesinde, **Modüller > Denetim çalışma ekranı > Kurulum > Denetim ilkeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="7f758-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="7f758-118">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-118">Select **New**.</span></span>
12. <span data-ttu-id="7f758-119">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="7f758-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="7f758-120">**İlke organizasyonları**  bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="7f758-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="7f758-121">Ağaçta **Contoso Entertainment System USA** seçeneğini ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="7f758-122">Ağaçta **Contoso Consulting USA** seçeneğini ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="7f758-123">Ağaçta **Contoso Retail USA** seçeneğini ve ardından **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="7f758-124">**İlke organizasyonları** bölümünü daraltın.</span><span class="sxs-lookup"><span data-stu-id="7f758-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="7f758-125">**İlke kuralları**  bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="7f758-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="7f758-126">Listede, önceden oluşturulmuş İlke Kuralı'nı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="7f758-127">**İlke kuralı oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="7f758-128">**Yürürlük tarihi** alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7f758-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="7f758-129">**Filtre**'yi seç.</span><span class="sxs-lookup"><span data-stu-id="7f758-129">Select **Filter**.</span></span>
23. <span data-ttu-id="7f758-130">Listede, **Gider kategorisi** satırını seçin ve ayrıntıları **Otel** olarak ayarlayın</span><span class="sxs-lookup"><span data-stu-id="7f758-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="7f758-131">**Ölçütler** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="7f758-132">**Toplam** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="7f758-133">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-133">Select **Add**.</span></span>
27. <span data-ttu-id="7f758-134">Listeden, **Hareket tutarı** için bir alan değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="7f758-135">**Alan** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="7f758-136">**AggregateFunction** alanında **Toplam** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="7f758-137">**Gruplandırma ölçütü** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="7f758-138">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-138">Select **Add**.</span></span>
32. <span data-ttu-id="7f758-139">Listeden **Personel** için bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="7f758-140">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-140">Select **Add**.</span></span>
34. <span data-ttu-id="7f758-141">Listeden **Gider kategorisi** için bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="7f758-142">**Alan** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="7f758-143">**Sahip** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="7f758-144">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-144">Select **Add**.</span></span>
38. <span data-ttu-id="7f758-145">**Hareket tutarı**  öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="7f758-146">**Alan** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="7f758-147">**AggregateFunction** alanında **Toplam** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="7f758-148">**Ölçütler** alanına `>2000` yazın.</span><span class="sxs-lookup"><span data-stu-id="7f758-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="7f758-149">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-149">Select **OK**.</span></span>
43. <span data-ttu-id="7f758-150">**Test**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-150">Select **Test**.</span></span>
44. <span data-ttu-id="7f758-151">**Belge seçim başlangıç tarihi** alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7f758-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="7f758-152">**Belge seçim bitiş tarihi** alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7f758-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="7f758-153">**Testi çalıştır**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-153">Select **Run test**.</span></span>
47. <span data-ttu-id="7f758-154">Eylem Bölmesinde **Denetim ilkesi** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7f758-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="7f758-155">**Ek seçenekler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="7f758-156">**Başlangıç tarihi** alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7f758-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="7f758-157">**Bitiş tarihi** alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7f758-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="7f758-158">**Toplu iş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-158">Select **Batch**.</span></span>
52. <span data-ttu-id="7f758-159">**Arka planda çalıştır** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="7f758-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="7f758-160">**Toplu işlem** alanında **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="7f758-161">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-161">Select **OK**.</span></span>
55. <span data-ttu-id="7f758-162">Gezinti bölmesinde **Modüller > Denetim çalışma ekranı > Denetim vakaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7f758-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="7f758-163">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="7f758-164">**İlişkilendirmeler**  bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="7f758-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="7f758-165">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7f758-165">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]