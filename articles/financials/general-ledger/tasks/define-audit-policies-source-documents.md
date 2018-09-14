--- 
title: "Kaynak belgeler için denetim ilkeleri tanımlama"
description: "Bu prosedür, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını gösterir."
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a82c3e8e8787beb309b75b73cda36f4ca8031d6f
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="dd2fa-103">Kaynak belgeler için denetim ilkeleri tanımlama</span><span class="sxs-lookup"><span data-stu-id="dd2fa-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd2fa-104">Bu prosedür, denetim ilkesi kurallarının nasıl belirlenip uygulanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="dd2fa-105">Örnekte, otel gideri türünde gider raporları kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="dd2fa-106">Bu yordam, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="dd2fa-107">Denetçi rolü bu görevleri gerçekleştirmek için uygun izinleri içerir.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="dd2fa-108">Audit workbench > Setup > Policy rule type (Denetim çalışma ekranı > Ayar > İlke kuralı türü) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="dd2fa-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-109">Click New.</span></span>
3. <span data-ttu-id="dd2fa-110">Kural adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="dd2fa-111">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dd2fa-112">Sorgu adı alanında Gider raporu satırı'nı seçin</span><span class="sxs-lookup"><span data-stu-id="dd2fa-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="dd2fa-113">Sorgu türü alanında Topla'yı seçin</span><span class="sxs-lookup"><span data-stu-id="dd2fa-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="dd2fa-114">Tüzel kişilik alanında Tüzel kişilik'i seçin</span><span class="sxs-lookup"><span data-stu-id="dd2fa-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="dd2fa-115">Belge tarihi referansı alanında Değiştirilme tarihi ve saati'ni seçin</span><span class="sxs-lookup"><span data-stu-id="dd2fa-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="dd2fa-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-116">Click Save.</span></span>
10. <span data-ttu-id="dd2fa-117">Audit workbench > Setup > Audit policies (Denetim çalışma ekranı > Ayar > Denetim ilkeleri) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="dd2fa-118">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-118">Click New.</span></span>
12. <span data-ttu-id="dd2fa-119">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="dd2fa-120">İlke organizasyonları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="dd2fa-121">Ağaçta "Contoso Eğlence Sistemi Türkiye"yi (Contoso Entertainment System USA) seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="dd2fa-122">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-122">Click Add.</span></span>
16. <span data-ttu-id="dd2fa-123">Ağaçta "Contoso Danışmanlık Türkiye"yi (Contoso Consulting USA) seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="dd2fa-124">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-124">Click Add.</span></span>
18. <span data-ttu-id="dd2fa-125">Ağaçta "Contoso Perakende Türkiye"yi (Contoso Retail USA) seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="dd2fa-126">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-126">Click Add.</span></span>
20. <span data-ttu-id="dd2fa-127">İlke organizasyonları bölümünü daraltın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="dd2fa-128">İlke kuralları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="dd2fa-129">Listede, önceden oluşturulmuş İlke Kuralı'nı bulup seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="dd2fa-130">İlke kuralı oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="dd2fa-131">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="dd2fa-132">Filtre'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-132">Click Filter.</span></span>
26. <span data-ttu-id="dd2fa-133">Listede, Gider kategorisi için satırı seçin ve Ayrıntılar ayarını Otel yapın</span><span class="sxs-lookup"><span data-stu-id="dd2fa-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="dd2fa-134">Ölçütler alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="dd2fa-135">Topla sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="dd2fa-136">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-136">Click Add.</span></span>
30. <span data-ttu-id="dd2fa-137">Listeden, Hareket tutarı için bir alan değeri seçin</span><span class="sxs-lookup"><span data-stu-id="dd2fa-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="dd2fa-138">Alan alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="dd2fa-139">Toplama İşlevi (AggregateFunction) alanında Toplam'ı (Sum) seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="dd2fa-140">Gruplama ölçütü sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="dd2fa-141">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-141">Click Add.</span></span>
35. <span data-ttu-id="dd2fa-142">Listeden, Çalışan için bir değer seçin </span><span class="sxs-lookup"><span data-stu-id="dd2fa-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="dd2fa-143">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-143">Click Add.</span></span>
37. <span data-ttu-id="dd2fa-144">Listeden, Gider kategorisi için bir değer seçin</span><span class="sxs-lookup"><span data-stu-id="dd2fa-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="dd2fa-145">Alan alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="dd2fa-146">Sahip sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-146">Click the Having tab.</span></span>
40. <span data-ttu-id="dd2fa-147">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-147">Click Add.</span></span>
41. <span data-ttu-id="dd2fa-148">Hareket tutarı'nı seçin</span><span class="sxs-lookup"><span data-stu-id="dd2fa-148">Select Transaction amount</span></span>
42. <span data-ttu-id="dd2fa-149">Alan alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="dd2fa-150">Toplama İşlevi (AggregateFunction) alanında Toplam'ı (Sum) seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="dd2fa-151">Ölçütler alanına '>2000' yazın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="dd2fa-152">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-152">Click OK.</span></span>
46. <span data-ttu-id="dd2fa-153">Sına'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-153">Click Test.</span></span>
47. <span data-ttu-id="dd2fa-154">Belge seçim başlangıç tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="dd2fa-155">Belge seçim bitiş tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="dd2fa-156">Testi çalıştır'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-156">Click Run test.</span></span>
50. <span data-ttu-id="dd2fa-157">Eylem Bölmesinde, Denetim ilkesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="dd2fa-158">Ek seçenekler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-158">Click Additional options.</span></span>
52. <span data-ttu-id="dd2fa-159">Başlangıç tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="dd2fa-160">Bitiş tarihi alanına tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="dd2fa-161">Toplu iş'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-161">Click Batch.</span></span>
55. <span data-ttu-id="dd2fa-162">Arka planda çalıştır bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="dd2fa-163">Toplu işleme alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="dd2fa-164">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-164">Click OK.</span></span>
58. <span data-ttu-id="dd2fa-165">Audit workbench > Audit cases (Denetim çalışma ekranı > Denetim vakaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="dd2fa-166">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="dd2fa-167">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="dd2fa-168">İlişkilendirmeler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="dd2fa-169">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="dd2fa-170">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd2fa-170">In the list, click the link in the selected row.</span></span>


