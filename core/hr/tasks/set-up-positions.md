--- 
title: "Pozisyonları ayarlama"
description: "Pozisyonlar, organizasyon hiyerarşisinin alt düzeylerinin önemli bir öğesidir."
author: DarinKramer
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c902f532e189753a375d4b48edd9ef0b6d74020e
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-positions"></a><span data-ttu-id="17446-103">Pozisyonları ayarlama</span><span class="sxs-lookup"><span data-stu-id="17446-103">Set up positions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17446-104">Pozisyonlar, organizasyon hiyerarşisinin alt düzeylerinin önemli bir öğesidir.</span><span class="sxs-lookup"><span data-stu-id="17446-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="17446-105">Bir pozisyon, bir işin bireysel eşdüşümüdür.</span><span class="sxs-lookup"><span data-stu-id="17446-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="17446-106">Örneğin "Satış yöneticisi (Doğu)" pozisyonu, "Satış yöneticisi" işiyle ilişkilendirilmiş işlerden biridir.</span><span class="sxs-lookup"><span data-stu-id="17446-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="17446-107">Bu konum bir departman içinde mevcuttur ve yalnızca bir çalışan ile ilişkilendirilmiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="17446-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="17446-108">Bu görev, bir konum oluşturmak için gerekli adımlar hakkında siz yol gösterecektir.</span><span class="sxs-lookup"><span data-stu-id="17446-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="17446-109">Bu yordam, İnsan Kaynakları Uzmanlarına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="17446-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="17446-110">İş gücü yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17446-110">Click Workforce management.</span></span>
2. <span data-ttu-id="17446-111">Açık pozisyonlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17446-111">Click Open positions.</span></span>
3. <span data-ttu-id="17446-112">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17446-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="17446-113">İş alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="17446-114">İş tanımı, unvan ve tam zamanlı eşdeğer çalışma faktörü, otomatik olarak pozisyondaki seçili işten kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="17446-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="17446-115">İşi ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="17446-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="17446-116">Pozisyon oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17446-116">Click Create position.</span></span>
7. <span data-ttu-id="17446-117">Departman alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="17446-118">Pozisyon türü alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="17446-119">Ücret alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="17446-120">Ücret bölgesi alanı, bu konumdaki bir çalışanın ücret uygunluğu kurallarını ve sabit artan bütçelerini belirler.</span><span class="sxs-lookup"><span data-stu-id="17446-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="17446-121">Atanmaya uygun alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="17446-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="17446-122">Pozisyon süresi bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="17446-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="17446-123">Konum süresi, varsayılan olarak daha önce girilen etkinleştirme ve sona erme tarihlerine dayalı olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="17446-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="17446-124">Pozisyonu konumlandırmak için Raporlar'ı genişletin.</span><span class="sxs-lookup"><span data-stu-id="17446-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="17446-125">Bir pozisyona başka bir pozisyona rapor veren bir işçi atadığınızda, iki pozisyona atanan işçiler arasında bir doğrudan raporlama ilişkisi oluşturmuş olursunuz.</span><span class="sxs-lookup"><span data-stu-id="17446-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="17446-126">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17446-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="17446-127">Raporlar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="17446-128">Oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17446-128">Click Create.</span></span>
16. <span data-ttu-id="17446-129">Çalışan atama bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="17446-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="17446-130">İlişkiler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="17446-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="17446-131">Organizasyonunuz bir matris hiyerarşisi veya başka bir özel hiyerarşi kullanıyorsa, pozisyon hiyerarşisi türleri ayarlayabilir ve ayarladığınız her bir hiyerarşi türü için pozisyonlara rapor ilişkileri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17446-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="17446-132">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="17446-132">Click Add.</span></span>
19. <span data-ttu-id="17446-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="17446-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="17446-134">Hiyerarşi adı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="17446-135">Pozisyonlara raporlar alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="17446-136">Bordro bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="17446-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="17446-137">Ödeme döngüsü alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="17446-138">Tarafından ödendi alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="17446-139">Yıllık normal mesai saatleri alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="17446-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="17446-140">Bu, bu pozisyondaki bir çalışanın her yıl çalışması beklenen ücretli saatlerin sayısıdır.</span><span class="sxs-lookup"><span data-stu-id="17446-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="17446-141">Sendika bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="17446-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="17446-142">Sendika bölümünü daraltın.</span><span class="sxs-lookup"><span data-stu-id="17446-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="17446-143">Mali boyutlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="17446-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="17446-144">Dağıtım şablonu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="17446-145">Departman alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="17446-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="17446-146">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="17446-146">Click Save.</span></span>


