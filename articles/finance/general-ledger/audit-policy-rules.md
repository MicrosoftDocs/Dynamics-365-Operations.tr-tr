---
title: Denetim ilkesi kuralları
description: Gider raporlarını, satıcı faturalarını ve satınalma siparişlerini değerlendirerek, oluşturduğunuz ilke kurallarına uygun olup olmadıklarından emin olmak için denetim ilkelerini kullanabilirsiniz. Bir denetim ilkesiyle ilişkili kuralların tümü, belirlediğiniz bir zaman planına göre top iş modunda çalıştırılır.  Her ilke kuralı, ilke kuralı türünün bir örneğidir. Her ilke kuralı türü için aynı anda yalnızca bir ilke kuralı etkin olabilir.
author: panolte
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3a0ffe81f4b56bdd388dc1ce2c00a99e0278cdf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5262850"
---
# <a name="audit-policy-rules"></a><span data-ttu-id="fcf48-106">Denetim ilkesi kuralları</span><span class="sxs-lookup"><span data-stu-id="fcf48-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fcf48-107">Gider raporlarını, satıcı faturalarını ve satınalma siparişlerini değerlendirerek, oluşturduğunuz ilke kurallarına uygun olup olmadıklarından emin olmak için denetim ilkelerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fcf48-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="fcf48-108">Bir denetim ilkesiyle ilişkili kuralların tümü, belirlediğiniz bir zaman planına göre top iş modunda çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="fcf48-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="fcf48-109">Her ilke kuralı, ilke kuralı türünün bir örneğidir.</span><span class="sxs-lookup"><span data-stu-id="fcf48-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="fcf48-110">Her ilke kuralı türü için aynı anda yalnızca bir ilke kuralı etkin olabilir.</span><span class="sxs-lookup"><span data-stu-id="fcf48-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="fcf48-111">Sorgular ve sorgu türleri</span><span class="sxs-lookup"><span data-stu-id="fcf48-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="fcf48-112">Bir denetim ilkesi kuralı oluşturduğunuzda öncelikle bir ilke kuralı türü seçersiniz.</span><span class="sxs-lookup"><span data-stu-id="fcf48-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="fcf48-113">İlke kuralı türü, ilke kuralının oluşturulmasında başlangıç noktası olarak kullanılmak üzere Uygulama Nesne Ağacı (AOT) sorgusunu belirler.</span><span class="sxs-lookup"><span data-stu-id="fcf48-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="fcf48-114">Ayrıca, ilke kuralı için kullanmak üzere sorgu türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fcf48-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="fcf48-115">Sorgu, İlke kuralının değerlendirdiği kaynak belgeyi belirler.</span><span class="sxs-lookup"><span data-stu-id="fcf48-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="fcf48-116">Ayrıca, kaynak belgesinde hem tüzel kişiliği hem belgeler denetim için seçildiğinde kullanılacak tarihi tanımlayan alanları belirler.</span><span class="sxs-lookup"><span data-stu-id="fcf48-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="fcf48-117">Sorgu türü, sorgu sayfasındaki ve Denetim ilkesi kuralı sayfadaki varsayılan alanları kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="fcf48-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="fcf48-118">Aşağıdaki tabloda denetim ilkesi kuralları için mevcut sorgu türleri gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="fcf48-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fcf48-119">Sorgu tipi</span><span class="sxs-lookup"><span data-stu-id="fcf48-119">Query type</span></span></th>
<th><span data-ttu-id="fcf48-120">Amaç</span><span class="sxs-lookup"><span data-stu-id="fcf48-120">Purpose</span></span></th>
<th><span data-ttu-id="fcf48-121">Daha fazla bilgi</span><span class="sxs-lookup"><span data-stu-id="fcf48-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fcf48-122">Koşullu</span><span class="sxs-lookup"><span data-stu-id="fcf48-122">Conditional</span></span></td>
<td><span data-ttu-id="fcf48-123">Kaynak belge öznitelikleri belirtilen değerlerle karşılaştırarak değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fcf48-124">Topla</span><span class="sxs-lookup"><span data-stu-id="fcf48-124">Aggregate</span></span></td>
<td><span data-ttu-id="fcf48-125">Nümerik değerleri toplayarak birden fazla kaynak belgesini veya kaynak belge satırlarını bir ilke kuralıyla karşılaştırarak değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fcf48-126">Örnekleme</span><span class="sxs-lookup"><span data-stu-id="fcf48-126">Sampling</span></span></td>
<td><span data-ttu-id="fcf48-127">Politika ihlalleri için değerlendirmek üzere kaynak belgelerin belirli bir oranını rastgele seçin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="fcf48-128">Bu seçimi yaptığınızda, denetim için rastgele seçilecek belge yüzdesini belirlemek için Denetim ilkesi kuralı sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="fcf48-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fcf48-129">Çoğalt</span><span class="sxs-lookup"><span data-stu-id="fcf48-129">Duplicate</span></span></td>
<td><span data-ttu-id="fcf48-130">Belirtilen alanlarda tekrarlanan girdileri içerip içermediğini belirlemek için kaynak belgeleri değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="fcf48-131">Bu seçimi yaptığınızda, belgeler tekrarlanan girdiler için değerlendirildiğinde belge seçim tarihi aralığının başlangıcı olarak eklenecek gün sayısını belirlemek için Denetim İlkesi kuralı sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="fcf48-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fcf48-132">Liste araması</span><span class="sxs-lookup"><span data-stu-id="fcf48-132">List search</span></span></td>
<td><span data-ttu-id="fcf48-133">Belirli varlıklar için kaynak belgeleri değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="fcf48-134">Sorgu kök belgesi, denetlenen belgeyi tanımlar.</span><span class="sxs-lookup"><span data-stu-id="fcf48-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="fcf48-135">Sorgu mutlaka dirpartytable tablosuna bir referans içeren bir liste sorgusu olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fcf48-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="fcf48-136">Bu seçenek sadece aşağıdaki AOT sorgularıyla kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="fcf48-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="fcf48-137"><span class="ui">AuditPolicyExpenseList</span> (Gider raporu izlenen personel)</span><span class="sxs-lookup"><span data-stu-id="fcf48-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="fcf48-138"><span class="ui">AuditPolicyPurchList</span> (Satın alma emri izlenen satıcılar)</span><span class="sxs-lookup"><span data-stu-id="fcf48-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="fcf48-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Satıcı faturası izlenen satıcılar)</span><span class="sxs-lookup"><span data-stu-id="fcf48-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="fcf48-140">Bu seçimi yaptığınızda, Denetim İlkesi kuralı sayfasında izlenen varlıkları belirtin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fcf48-141">Anahtar sözcük araması</span><span class="sxs-lookup"><span data-stu-id="fcf48-141">Keyword search</span></span></td>
<td><span data-ttu-id="fcf48-142">Belirli sözcükleri içerip içermediklerini belirlemek için kaynak belgeleri değerlendirin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="fcf48-143">Bu seçimi yaptığınızda, Denetim İlkesi kuralı sayfasına aradığınız kelimeleri girin.</span><span class="sxs-lookup"><span data-stu-id="fcf48-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="fcf48-144">Denetim İlkesi kural sayfası ayrıca girdiğiniz sözcükler için değerlendirilecek tabloları ve alanları belirlemenizi sağlayan seçenekler de içerir.</span><span class="sxs-lookup"><span data-stu-id="fcf48-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="fcf48-145">Genel parametreler</span><span class="sxs-lookup"><span data-stu-id="fcf48-145">Common parameters</span></span>
<span data-ttu-id="fcf48-146">Belirli bir denetim ilkesi için ilke kurallarının tümü aynı toplu iş parametrelerini ve aynı belge seçimin tarihi aralığını paylaşır.</span><span class="sxs-lookup"><span data-stu-id="fcf48-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="fcf48-147">Bu parametreler, ilke için İlave seçenekler sayfasında belirlenir.</span><span class="sxs-lookup"><span data-stu-id="fcf48-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="fcf48-148">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fcf48-148">Additional resources</span></span>
--------

<span data-ttu-id="fcf48-149">[İlke ihlali ve olaylarını denetleme](audit-policy-violations-cases.md)
[Kaynak belgeler için denetleme ilkeleri tanımla](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="fcf48-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]