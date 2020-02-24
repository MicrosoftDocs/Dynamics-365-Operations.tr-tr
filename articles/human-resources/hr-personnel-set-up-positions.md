---
title: Pozisyonları ayarlama
description: Pozisyonlar, organizasyon hiyerarşisinin alt düzeylerinin önemli bir öğesidir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22598869a673e91dd17546c46eb12c4d53ef0c9b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010890"
---
# <a name="set-up-positions"></a><span data-ttu-id="01d58-103">Pozisyonları ayarlama</span><span class="sxs-lookup"><span data-stu-id="01d58-103">Set up positions</span></span>



<span data-ttu-id="01d58-104">Pozisyonlar, organizasyon hiyerarşisinin alt düzeylerinin önemli bir öğesidir.</span><span class="sxs-lookup"><span data-stu-id="01d58-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="01d58-105">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="01d58-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="01d58-106">Örneğin "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş işlerden biridir.</span><span class="sxs-lookup"><span data-stu-id="01d58-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="01d58-107">Bu konum bir departman içinde mevcuttur ve yalnızca bir çalışan ile ilişkilendirilmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="01d58-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="01d58-108">Bu görev, bir konum oluşturmak için gerekli adımlar hakkında siz yol gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="01d58-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="01d58-109">Bu yordam, İnsan Kaynakları Uzmanlarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="01d58-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="01d58-110">İş gücü yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01d58-110">Click Workforce management.</span></span>
2. <span data-ttu-id="01d58-111">Açık pozisyonlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01d58-111">Click Open positions.</span></span>
3. <span data-ttu-id="01d58-112">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01d58-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="01d58-113">İş alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="01d58-114">İş tanımı, unvan ve tam zamanlı eşdeğer çalışma faktörü, otomatik olarak pozisyondaki seçili işten kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="01d58-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="01d58-115">İşi ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="01d58-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="01d58-116">Pozisyon oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01d58-116">Click Create position.</span></span>
7. <span data-ttu-id="01d58-117">Departman alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="01d58-118">Pozisyon türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="01d58-119">Ücret alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="01d58-120">Ücret bölgesi alanı, bu konumdaki bir çalışanın ücret uygunluğu kurallarını ve sabit artan bütçelerini belirler.</span><span class="sxs-lookup"><span data-stu-id="01d58-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="01d58-121">Atanmaya uygun alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="01d58-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="01d58-122">Pozisyon süresi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="01d58-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="01d58-123">Konum süresi, varsayılan olarak daha önce girilen etkinleştirme ve sona erme tarihlerine dayalı olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="01d58-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="01d58-124">Pozisyonu konumlandırmak için Raporlar'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="01d58-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="01d58-125">Bir pozisyona başka bir pozisyona rapor veren bir işçi atadığınızda, iki pozisyona atanan işçiler arasında bir doğrudan raporlama ilişkisi oluşturmuş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="01d58-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="01d58-126">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01d58-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="01d58-127">Raporlar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="01d58-128">Oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01d58-128">Click Create.</span></span>
16. <span data-ttu-id="01d58-129">Çalışan atama bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="01d58-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="01d58-130">İlişkiler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="01d58-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="01d58-131">Organizasyonunuz bir matris hiyerarşisi veya başka bir özel hiyerarşi kullanıyorsa, pozisyon hiyerarşisi türleri ayarlayabilir ve ayarladığınız her bir hiyerarşi türü için pozisyonlara rapor ilişkileri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01d58-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="01d58-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="01d58-132">Click Add.</span></span>
19. <span data-ttu-id="01d58-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="01d58-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="01d58-134">Hiyerarşi adı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="01d58-135">Pozisyonlara raporlar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="01d58-136">Bordro bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="01d58-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="01d58-137">Ödeme döngüsü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="01d58-138">Tarafından ödendi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="01d58-139">Yıllık normal mesai saatleri alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="01d58-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="01d58-140">Bu, bu pozisyondaki bir çalışanın her yıl çalışması beklenen ücretli saatlerin sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="01d58-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="01d58-141">Sendika bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="01d58-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="01d58-142">Sendika bölümünü daraltın.</span><span class="sxs-lookup"><span data-stu-id="01d58-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="01d58-143">Mali boyutlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="01d58-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="01d58-144">Dağıtım şablonu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="01d58-145">Departman alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01d58-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="01d58-146">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01d58-146">Click Save.</span></span>

