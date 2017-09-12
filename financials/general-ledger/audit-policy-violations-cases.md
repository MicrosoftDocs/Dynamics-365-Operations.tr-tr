---
title: "İlke ihlallerini ve vakalarını denetleme"
description: "Makalede, denetim ilkesi kuralları ihlallerinden nasıl denetim çalışmaları oluşturulduğu açıklanmaktadır. Makalede, denetim ilkelerinin belge seçim tarihi aralığını kullanmasının çeşitli yolları da yer almaktadır."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 24ee0dbf01208f8decc167e11e84191eaae03edf
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---

# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="70b50-104">İlke ihlallerini ve vakalarını denetleme</span><span class="sxs-lookup"><span data-stu-id="70b50-104">Audit policy violations and cases</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="70b50-105">Makalede, denetim ilkesi kuralları ihlallerinden nasıl denetim çalışmaları oluşturulduğu açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="70b50-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="70b50-106">Makalede, denetim ilkelerinin belge seçim tarihi aralığını kullanmasının çeşitli yolları da yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="70b50-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="70b50-107">Denetim vakaları nasıl oluşturulur</span><span class="sxs-lookup"><span data-stu-id="70b50-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="70b50-108">Denetim ilkeleri, tanımladığınız ve denetim ilke kuralları olarak yapılandırdığınız iş kurallarına uymayan gider raporlarının, satın alma emirlerinin ve satıcı faturalarının tanımlanması için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="70b50-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="70b50-109">Denetim ilkeleri toplu iş modunda çalışır.</span><span class="sxs-lookup"><span data-stu-id="70b50-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="70b50-110">Bir denetim İlkesini çalıştırdığınızda, bu ilkenin bir parçası olan tüm ilke kuralları aynı anda çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="70b50-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="70b50-111">Her bir ilke kuralı bir belgeler kümesini değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="70b50-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="70b50-112">İlke kuralı, belge seçim tarihi aralığında bulunan ve belirtilen ölçütle eşleşen belgeleri seçer.</span><span class="sxs-lookup"><span data-stu-id="70b50-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="70b50-113">Örneğin, bir ilke kuralı 50.00 tutarını aşan yemek faturaları içeren gider raporlarını seçebilir.</span><span class="sxs-lookup"><span data-stu-id="70b50-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="70b50-114">Başka bir ilke kuralı belirli bir satıcıya ödenecek satıcı faturalarını seçebilir.</span><span class="sxs-lookup"><span data-stu-id="70b50-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="70b50-115">Kümede seçilen her bir belge için bir ihlal oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="70b50-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="70b50-116">Bu ihlal, örneğin fatura 12345 gibi belirli bir belgenin ilke kuralı ile uyumlu olmadığını gösteren bir kayıttır.</span><span class="sxs-lookup"><span data-stu-id="70b50-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="70b50-117">Birden fazla denetim ihlali kaydı gruplandırılır ve denetim vakaları ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="70b50-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="70b50-118">Varsayılan olarak, her denetim ilkesi için vakalar denetim ilkesi kuralına göre gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="70b50-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="70b50-119">İsterseniz, **Vaka gruplandırma ölçütleri** sayfasını kullanarak diğer gruplandırma ölçütlerini de seçebileceğiniz.</span><span class="sxs-lookup"><span data-stu-id="70b50-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="70b50-120">Örneğin, proje kodu ve satıcı faturaları gider üstbilgilerini satıcı hesabına göre gruplandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="70b50-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="70b50-121">Bu durumda, aynı proje kimliğine sahip olan tüm gider başlığı ihlalleri aynı vakada gruplandırılır ve aynı satıcı hesabına sahip tüm satıcı faturaları aynı vakada gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="70b50-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="70b50-122">Bir **Tekrarlanan** sorgu türüne dayalı denetim ilkesi kuralları için ihlaller, ilke kuralına veya **Vaka gruplandırma ölçütleri** sayfasında belirtilen ölçütlere göre gruplandırılmaz.</span><span class="sxs-lookup"><span data-stu-id="70b50-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="70b50-123">Bunun yerine, denetim ilkesi kuralına entegre edilen ölçütlere göre gruplandırılır.</span><span class="sxs-lookup"><span data-stu-id="70b50-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="70b50-124">Örneğin, bir ilke kuralı aynı tutar, satıcı kimliği ve tarih ile tekrarlanan giderler için gider raporlarını değerlendiriyorsa bu alanlarda aynı değerlere sahip olan tüm giderler bir vakada toplanır.</span><span class="sxs-lookup"><span data-stu-id="70b50-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="70b50-125">Farklı değerlere sahip giderler ise ayrı bir vaka olur.</span><span class="sxs-lookup"><span data-stu-id="70b50-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="70b50-126">Denetim vakaları oluşturulduktan sonra standart vaka yönetimi süreçleri kullanılarak işlenir.</span><span class="sxs-lookup"><span data-stu-id="70b50-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="70b50-127">Belge seçimi tarih aralıkları</span><span class="sxs-lookup"><span data-stu-id="70b50-127">Document selection date ranges</span></span>
<span data-ttu-id="70b50-128">Bir denetim ilkesi çalıştırıldığında her bir ilke kuralı, tarihi belge seçim tarihi aralığında bulunan, belirtilen türde belgeleri seçer.</span><span class="sxs-lookup"><span data-stu-id="70b50-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="70b50-129">Belge seçimi tarih aralığı, **Ek seçenekler** sayfasında belirtilir.</span><span class="sxs-lookup"><span data-stu-id="70b50-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="70b50-130">Birçok belge, kendileriyle ilişkilendirilmiş birden fazla tarih içerir.</span><span class="sxs-lookup"><span data-stu-id="70b50-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="70b50-131">Denetim ilkesi kuralının kullandığı tarih alanı, **İlke kuralı türü** sayfasında belirtilir.</span><span class="sxs-lookup"><span data-stu-id="70b50-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="70b50-132">Burada, bir denetim ilkesinin, belge seçim tarihi aralığını nasıl başka şekillerde kullandığı verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="70b50-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="70b50-133">İlke, belge seçim tarihi aralığının son gününde geçerli olan her bir ilke kuralının sürümünü kullanır.</span><span class="sxs-lookup"><span data-stu-id="70b50-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="70b50-134">Her bir ilke kuralının geçerlilik tarihlerini **Denetim ilkeleri** listesi sayfasında bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="70b50-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="70b50-135">İlke, belge seçim tarihi aralığının son gününde politikayla ilişkilendirilmiş organizasyon düğümlerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="70b50-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="70b50-136">**Denetim ilkeleri** listesi sayfasında sadece mevcut durumda ilkeyle ilişkilendirilmiş organizasyon düğümleri görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="70b50-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="70b50-137">Bir **Liste arama** sorgu türüne dayalı ilke kuralları için ilke, belge seçim tarihi aralığının son günü geçerli olan, takip edilen varlıklar için belgeleri değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="70b50-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="70b50-138">Daha fazla bilgi için bkz: [Denetim İlkesi kuralları](audit-policy-rules.md)</span><span class="sxs-lookup"><span data-stu-id="70b50-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>




