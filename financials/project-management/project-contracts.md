---
title: "Proje sözleşmeleri"
description: "Bu makalede Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümünde çeşitli proje türleri ve finansman kaynakları için oluşturabileceğiniz proje sözleşmeleri örneklerle açıklanmakta, sözleşmeleri nasıl yöneteceğiniz ve proje müşterilerini nasıl faturalandıracağınız anlatılmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d13362acf70edc03a47662c4c3eff680cc04bd8f
ms.contentlocale: tr-tr
ms.lasthandoff: 07/18/2017

---

# <a name="project-contracts"></a><span data-ttu-id="879ea-103">Proje sözleşmeleri</span><span class="sxs-lookup"><span data-stu-id="879ea-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="879ea-104">Bu makalede Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümünde çeşitli proje türleri ve finansman kaynakları için oluşturabileceğiniz proje sözleşmeleri örneklerle açıklanmakta, sözleşmeleri nasıl yöneteceğiniz ve proje müşterilerini nasıl faturalandıracağınız anlatılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="879ea-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="879ea-105">Bir proje sözleşmesi için oluşturduğunuz proje türü, projenin müşterilerinin faturalandırılması için kullanılacak yöntemi belirleyecektir.</span><span class="sxs-lookup"><span data-stu-id="879ea-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="879ea-106">Bir proje sözleşmesini ve ilgili projeyi değiştirebilirsiniz, ancak proje türünü değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="879ea-107">Proje sözleşmesi kullanarak, aynı anda bir ya da birden fazla projeyi faturalandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="879ea-108">Proje sözleşmesi aynı zamanda, bir proje yapısındaki tüm alt projeler için tutarlı bir faturalandırma yordamının uygulanmasını garantilemeye yarar.</span><span class="sxs-lookup"><span data-stu-id="879ea-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="879ea-109">Faturalanacak her projenin bir proje sözleşmesi ile ilişkilendirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="879ea-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="879ea-110">Bir proje sözleşmesi için ayarlar, bu proje sözleşmesi ile ilişkilendirilmiş tüm projelere ve alt projelere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="879ea-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="879ea-111">Bir proje sözleşmesi bir ya da daha fazla finansman kaynağını belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="879ea-112">Bu nedenle faturalamayı çeşitli finansörlere bölebilir, finansman kaynakları belirli bir tutarın üstünde faturalandırılmasın diye finansman sınırları ayarlayabilir ve borçlandırma harcamalarını için yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="879ea-113">Proje sözleşmeleri için finansman</span><span class="sxs-lookup"><span data-stu-id="879ea-113">Funding for project contracts</span></span>
<span data-ttu-id="879ea-114">Bazı proje sözleşmeleri, proje maliyetlerinin finansmanını üstlenme sorumluluğunu birden çok tarafta olduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="879ea-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="879ea-115">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="879ea-115">Here are some examples:</span></span>

-   <span data-ttu-id="879ea-116">Birden çok bölüme sahip olan bir müşteri, bir projenin finansmanının bölümler arasında bölünmesini talep eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="879ea-117">Şirketiniz büyük bir projenin maliyetlerini harici bir kuruluşla paylaşır.</span><span class="sxs-lookup"><span data-stu-id="879ea-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="879ea-118">Bir yol projesi iki belediye tarafından ortaklaşa finanse edilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="879ea-119">Bir köprü projesi bir hükümeti desteği ve bir özel şirket tarafından finanse edilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="879ea-120">Finance and Operations'da tek bir işlemin veya tüm bir projenin faturalamasını birden fazla müşteri, bağış veya kuruluş arasında bölebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="879ea-121">Birden fazla finansöre sahip projelerde, gelişmiş finansman projesine katkıda bulunan tüm taraflar finansman kaynakları olarak adlandırılırlar.</span><span class="sxs-lookup"><span data-stu-id="879ea-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="879ea-122">Bir müşteri, organizasyon veya destek bir finansman kaynağı olarak tanımlandıktan sonra, bu bir veya daha fazla finansman kuralına atanabilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="879ea-123">Finansman kuralları, giderlerin bir proje için çeşitli finans kaynaklarına nasıl ayrılacağını belirleyen kriterleri içerir.</span><span class="sxs-lookup"><span data-stu-id="879ea-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="879ea-124">Örneğin satınalma taleplerinde veya satınalma siparişlerinde görünenler gibi stoğu tutulan maddeler, bölünemiyor olduklarından, gider tutarı dağıtım zamanında birden fazla finansman kaynağına bölünemez.</span><span class="sxs-lookup"><span data-stu-id="879ea-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="879ea-125">Bu nedenle, stok çıkışı deftere nakledilene kadar finansman kaynağı değeri 0 (sıfır) kalır.</span><span class="sxs-lookup"><span data-stu-id="879ea-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="879ea-126">Stok çıkışı deftere nakledildiğinde, maliyet tutarı proje hesap dağıtım kurallarına göre dağıtılır.</span><span class="sxs-lookup"><span data-stu-id="879ea-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="879ea-127">Faturalamayı birden fazla fon kaynakları arasında bölmeyi daha kolay hale getirmek için uygulayabileceğiniz bazı adımlar şunlardır:</span><span class="sxs-lookup"><span data-stu-id="879ea-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="879ea-128">Bir proje için girilen tüm hareketlerin proje sözleşmesindeki para biriminin aynısını kullandığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="879ea-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="879ea-129">Finansman kaynağının bir proje için belirtilen miktardan daha fazla faturalanmaması için finansman sınırları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="879ea-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="879ea-130">Her bir çalışan, kategori, kategori grubu ve hareket türü (veya tüm hareket türleri) için finansman kuralları ve finansman sınırları yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="879ea-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="879ea-131">Her bir fon kuralının geçerli olacağı dönemi tanımlayan isteğe bağlı başlangıç ve bitiş tarihleri seçin.</span><span class="sxs-lookup"><span data-stu-id="879ea-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="879ea-132">Her fon kaynağının sorumlu olduğu yüzdeyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="879ea-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="879ea-133">Hangi finansman kaynağının finansman tahsisat hesaplamalarından kaynaklanacak yuvarlama farklılıklarından sorumlu olduğunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="879ea-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="879ea-134">Proje maliyetlerinin harici müşterilere nasıl faturalanacağını ve dahili kuruluşlara nasıl masraflandırılacağını belirleyen kurallar ayarların.</span><span class="sxs-lookup"><span data-stu-id="879ea-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="879ea-135">Hareketleri bir durdurma finans hesabında ek finansman elde edilebilene veya masrafları dahili olarak karşılamaya karar verene kadar kaydedin.</span><span class="sxs-lookup"><span data-stu-id="879ea-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="879ea-136">Bir hareket ile hangi vergi grubunun ilişkilendirileceğini belirlemek için, projede bir vergi grubu ataması aranır.</span><span class="sxs-lookup"><span data-stu-id="879ea-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="879ea-137">Eğer proje düzeyinde hiçbir vergi grubu ataması yapılmadıysa, proje sözleşmesi aranır.</span><span class="sxs-lookup"><span data-stu-id="879ea-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="879ea-138">Örnek: Birden fazla finansman kaynağı (basit)</span><span class="sxs-lookup"><span data-stu-id="879ea-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="879ea-139">Aşağıdaki tablo, birden çok finansman kaynağı arasında finansman tahsisatını yönetmek için senaryolar sağlar.</span><span class="sxs-lookup"><span data-stu-id="879ea-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="879ea-140">Bu senaryolar aşağıdaki varsayımlar dayanırlar:</span><span class="sxs-lookup"><span data-stu-id="879ea-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="879ea-141">Öncelik ayarları fonların tahsisatına diğer finansman kuralı ölçütlerinin uygulanmasından önce dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="879ea-142">Finansman kuralının geçerli olduğu dönem d'yi tanımlamak için hiçbir tarih aralığı belirtilmedi.</span><span class="sxs-lookup"><span data-stu-id="879ea-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="879ea-143"><strong>Senaryo</strong></span><span class="sxs-lookup"><span data-stu-id="879ea-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="879ea-144"><strong>Finansman kaynağı </strong></span><span class="sxs-lookup"><span data-stu-id="879ea-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="879ea-145"><strong>Tahsisat yüzdesi </strong></span><span class="sxs-lookup"><span data-stu-id="879ea-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="879ea-146"><strong>Ayırma önceliği </strong></span><span class="sxs-lookup"><span data-stu-id="879ea-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="879ea-147">Maliyetleri fonu tükenene kadar bir finansman kaynağına tahsis etmek istiyorsunuz, daha sonra fonları tükenene kadar ikinci bir finansman kaynağına, en sonunda da kalan maliyetleri üçüncü bir finansman kaynağına tahsis etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="879ea-148">Finansman　kaynağı　1</span><span class="sxs-lookup"><span data-stu-id="879ea-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="879ea-149">Finansman　kaynağı　2</span><span class="sxs-lookup"><span data-stu-id="879ea-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="879ea-150">Finansman　kaynağı　3</span><span class="sxs-lookup"><span data-stu-id="879ea-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-151">%100</span><span class="sxs-lookup"><span data-stu-id="879ea-151">100%</span></span></li>
<li><span data-ttu-id="879ea-152">%100</span><span class="sxs-lookup"><span data-stu-id="879ea-152">100%</span></span></li>
<li><span data-ttu-id="879ea-153">%100</span><span class="sxs-lookup"><span data-stu-id="879ea-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-154">1</span><span class="sxs-lookup"><span data-stu-id="879ea-154">1</span></span></li>
<li><span data-ttu-id="879ea-155">2</span><span class="sxs-lookup"><span data-stu-id="879ea-155">2</span></span></li>
<li><span data-ttu-id="879ea-156">3</span><span class="sxs-lookup"><span data-stu-id="879ea-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="879ea-157">Maliyetlerin yüzde 75'ini bir finansman kaynağına, kalan yüzde 25'i ise ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="879ea-158">Bu finansman kaynaklarından herhangi birisi tükendiğinde, kalan maliyetleri üçüncü bir finansman kaynağından ödemek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="879ea-159">Finansman　kaynağı　1</span><span class="sxs-lookup"><span data-stu-id="879ea-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="879ea-160">Finansman　kaynağı　2</span><span class="sxs-lookup"><span data-stu-id="879ea-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="879ea-161">Finansman　kaynağı　3</span><span class="sxs-lookup"><span data-stu-id="879ea-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-162">%75</span><span class="sxs-lookup"><span data-stu-id="879ea-162">75%</span></span></li>
<li><span data-ttu-id="879ea-163">%25</span><span class="sxs-lookup"><span data-stu-id="879ea-163">25%</span></span></li>
<li><span data-ttu-id="879ea-164">%100</span><span class="sxs-lookup"><span data-stu-id="879ea-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-165">1</span><span class="sxs-lookup"><span data-stu-id="879ea-165">1</span></span></li>
<li><span data-ttu-id="879ea-166">1</span><span class="sxs-lookup"><span data-stu-id="879ea-166">1</span></span></li>
<li><span data-ttu-id="879ea-167">2</span><span class="sxs-lookup"><span data-stu-id="879ea-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="879ea-168">Maliyetlerin yüzde 75'ini bir finansman kaynağına, kalan yüzde 25'i ise ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="879ea-169">Bu finansman kaynaklarından herhangi birisi tükendiğinde, kalan maliyetleri üçüncü ve dördüncü finansman kaynakları arasında bölüştürmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="879ea-170">Finansman　kaynağı　1</span><span class="sxs-lookup"><span data-stu-id="879ea-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="879ea-171">Finansman　kaynağı　2</span><span class="sxs-lookup"><span data-stu-id="879ea-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="879ea-172">Finansman　kaynağı　3</span><span class="sxs-lookup"><span data-stu-id="879ea-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="879ea-173">Finansman　kaynağı　4</span><span class="sxs-lookup"><span data-stu-id="879ea-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-174">%75</span><span class="sxs-lookup"><span data-stu-id="879ea-174">75%</span></span></li>
<li><span data-ttu-id="879ea-175">%25</span><span class="sxs-lookup"><span data-stu-id="879ea-175">25%</span></span></li>
<li><span data-ttu-id="879ea-176">%50</span><span class="sxs-lookup"><span data-stu-id="879ea-176">50%</span></span></li>
<li><span data-ttu-id="879ea-177">%50</span><span class="sxs-lookup"><span data-stu-id="879ea-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-178">1</span><span class="sxs-lookup"><span data-stu-id="879ea-178">1</span></span></li>
<li><span data-ttu-id="879ea-179">1</span><span class="sxs-lookup"><span data-stu-id="879ea-179">1</span></span></li>
<li><span data-ttu-id="879ea-180">2</span><span class="sxs-lookup"><span data-stu-id="879ea-180">2</span></span></li>
<li><span data-ttu-id="879ea-181">2</span><span class="sxs-lookup"><span data-stu-id="879ea-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="879ea-182">Maliyetlerin ilk yüzde 25'ini bir finansman kaynağına, kalanını ise ikinci bir finansman kaynağına tahsis etmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="879ea-183">Finansman　kaynağı　1</span><span class="sxs-lookup"><span data-stu-id="879ea-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="879ea-184">Finansman　kaynağı　2</span><span class="sxs-lookup"><span data-stu-id="879ea-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-185">%25</span><span class="sxs-lookup"><span data-stu-id="879ea-185">25%</span></span></li>
<li><span data-ttu-id="879ea-186">%100</span><span class="sxs-lookup"><span data-stu-id="879ea-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="879ea-187">1</span><span class="sxs-lookup"><span data-stu-id="879ea-187">1</span></span></li>
<li><span data-ttu-id="879ea-188">2</span><span class="sxs-lookup"><span data-stu-id="879ea-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="879ea-189">Örnek: Birden fazla finansman kaynağı (karmaşık)</span><span class="sxs-lookup"><span data-stu-id="879ea-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="879ea-190">Aşağıdaki sıralamayla kullanmak istediğiniz üç finansman kaynağınız var:</span><span class="sxs-lookup"><span data-stu-id="879ea-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="879ea-191">Finansman kaynağı 2 ve 3'ü, finansman kaynağı 2 tükenene kadar eşit kullanın.</span><span class="sxs-lookup"><span data-stu-id="879ea-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="879ea-192">Finansman kaynağı 3 tükenene kadar kullanmaya devam edin.</span><span class="sxs-lookup"><span data-stu-id="879ea-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="879ea-193">Finansman kaynağı 3 tükendikten sonra finansman kaynağı 1'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="879ea-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="879ea-194">Bu hedefe ulaşmak için, aşağıdakileri yapmalısınız:</span><span class="sxs-lookup"><span data-stu-id="879ea-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="879ea-195">Finansman kaynağı 2 ve finansman kaynağı 3 için, onlara karşılık gelen tutarlar için finansman sınırları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="879ea-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="879ea-196">Aşağıdaki finansman kurallarını oluşturun:</span><span class="sxs-lookup"><span data-stu-id="879ea-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="879ea-197">Kural 1 (Öncelik 1): Hareketlerin yüzde 50'sini finansman kaynağı 2'ye ve yüzde 50'sini finansman kaynağı 3'e tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="879ea-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="879ea-198">Kural 2 (Öncelik 2): Hareketlerin yüzde 100'ünün finansman kaynağı 3'e tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="879ea-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="879ea-199">Kural 3 (Öncelik 3): Hareketlerin yüzde 100'ünün finansman kaynağı 1'e tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="879ea-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="879ea-200">Bu kurulum çalışır, çünkü hareket kuralları ve bunlardan herhangi birinin hareketleri için geçerli olup olmadığını belirlemek için sınırları karşı denetlenir.</span><span class="sxs-lookup"><span data-stu-id="879ea-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="879ea-201">Hareket için hiçbir özel kural uygulanmıyorsa, Tüm hareketler kuralı uygulanır.</span><span class="sxs-lookup"><span data-stu-id="879ea-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="879ea-202">Tüm hareketler kuralı, tüm hareketlerle eşleşir.</span><span class="sxs-lookup"><span data-stu-id="879ea-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="879ea-203">Bir hareket ile eşleşen bir kural bulunursa, bu kuralda tahsis edilen yüzde ilk önce uygulanır, fakat önce bu eşleşmeler '.'n ayarlanmış olan mevcut sınırlara karşı denetlenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="879ea-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="879ea-204">Eğer bir sınırla karşılaşılırsa, ve bir finansman kaynağı'nın fonları tükenmişse, finansman sınırı ile ilişkilendirilmiş finansman kuralı göz ardı edilir ve program uygulanacak bir sonraki kuralı denetler.</span><span class="sxs-lookup"><span data-stu-id="879ea-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="879ea-205">Bazı durumlarda, bir hareketin yalnızca parçası bir kural altında tahsis edilebilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="879ea-206">Bu, hareket tahsis edildiğinde bir sınıra ulaşıldığında gerçekleşebilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="879ea-207">Bu durumda, kurala sadece belirli bir tutar tahsis edilir, örneğin her finansman kaynağına yüzde 50 gibi.</span><span class="sxs-lookup"><span data-stu-id="879ea-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="879ea-208">Bu durum, bu bölümde daha önce açıklanmış kural 1'de böyledir.</span><span class="sxs-lookup"><span data-stu-id="879ea-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="879ea-209">Kalan, sıradaki bir sonraki kurala göre tahsis edilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="879ea-210">Aşağıdaki tabloda bu senaryoyu daha ayrıntılı olarak inceler.</span><span class="sxs-lookup"><span data-stu-id="879ea-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="879ea-211"><strong>Odak </strong></span><span class="sxs-lookup"><span data-stu-id="879ea-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="879ea-212"><strong>Ayrıntılar</strong></span><span class="sxs-lookup"><span data-stu-id="879ea-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="879ea-213">Finansman kuralları</span><span class="sxs-lookup"><span data-stu-id="879ea-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="879ea-214">Kural 1 (öncelik 1): Tüm hareketler.</span><span class="sxs-lookup"><span data-stu-id="879ea-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="879ea-215">Finansman kaynağı 2'yi %50'de ve finansman kaynağı 3'ü %50'de tahsis edin.</span><span class="sxs-lookup"><span data-stu-id="879ea-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="879ea-216">Kural 2 (Öncelik 2): Tüm hareketler.</span><span class="sxs-lookup"><span data-stu-id="879ea-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="879ea-217">Finansman kaynağı 3'ü %100'de tahsis edin</span><span class="sxs-lookup"><span data-stu-id="879ea-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="879ea-218">Kural 3 (Öncelik 2): Tüm hareketler.</span><span class="sxs-lookup"><span data-stu-id="879ea-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="879ea-219">Finansman kaynağı 1'ü %100'de tahsis edin</span><span class="sxs-lookup"><span data-stu-id="879ea-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="879ea-220">Finansman sınırları</span><span class="sxs-lookup"><span data-stu-id="879ea-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="879ea-221">Finansman kaynağı 1 sınırı = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="879ea-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="879ea-222">Finansman kaynağı 2 sınırı = 500,00</span><span class="sxs-lookup"><span data-stu-id="879ea-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="879ea-223">Finansman kaynağı 3 sınırı = 750,00</span><span class="sxs-lookup"><span data-stu-id="879ea-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="879ea-224">Hareket 1</span><span class="sxs-lookup"><span data-stu-id="879ea-224">Transaction 1</span></span></td>
<td><span data-ttu-id="879ea-225"><strong>Hareket tutarı:</strong> 100,00<strong>Finansman:</strong> Hareket sadece kural 1'e göre ödenecektir çünkü kural 1 uygulandıktan sonra hareket tamamen ödenmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="879ea-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="879ea-226">Hareket, finansman kaynağı 2 ve finansman kaynağı 3 arasında eşit olarak finanse edilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="879ea-227">Finansman kaynağı 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="879ea-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="879ea-228">Finansman kaynağı 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="879ea-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="879ea-229">Hareket 2</span><span class="sxs-lookup"><span data-stu-id="879ea-229">Transaction 2</span></span></td>
<td><span data-ttu-id="879ea-230"><strong>Hareket tutarı:</strong> 5.000,00<strong>Finansman:</strong> Hareket üç kuralın tümüne göre ödenir.<strong>Kural 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="879ea-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="879ea-231">Finansman kaynağı 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="879ea-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="879ea-232">Finansman kaynağı 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="879ea-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="879ea-233">
<strong>Kural 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="879ea-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="879ea-234">Finansman kaynağı 3: 250,00 (= 750,00 – 50,00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="879ea-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="879ea-235">
<strong>Kural 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="879ea-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="879ea-236">Finansman kaynağı 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="879ea-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="879ea-237">Her finansman kaynağına dağıtılan toplam fon</span><span class="sxs-lookup"><span data-stu-id="879ea-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="879ea-238">Finansman kaynağı 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="879ea-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="879ea-239">Finansman kaynağı 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="879ea-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="879ea-240">Finansman kaynağı 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="879ea-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="879ea-241">Faturalama kuralları</span><span class="sxs-lookup"><span data-stu-id="879ea-241">Billing rules</span></span>
<span data-ttu-id="879ea-242">Bir proje sözleşmesi üzerine bir müşteri ile görüşürken, bir proje üzerindeki iş için müşteriye ne zaman ve nasıl fatura kesebileceğinizi tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="879ea-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="879ea-243">Proje sözleşmesini ve projeyi ayarladıktan sonra, proje için faturalama kurallarını ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="879ea-244">Faturalama kuralları, proje sözleşmesinde belirtilen proje koşullarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="879ea-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="879ea-245">Oluşturabileceğiniz faturalama kuralları, Zaman ve malzeme veya sabit-fiyat gibi proje sözleşmesindeki faturalama kuralları ile ilişkilendirdiğiniz koşullara ve proje türüne bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="879ea-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="879ea-246">Proje sözleşmesi için birden fazla ödeme kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="879ea-247">Aynı proje sözleşmesine ve benzer faturalama kurallarına sahip birden fazla projeye bir faturalama kuralı atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="879ea-248">Aşağıdaki faturalama kural türlerini ayarlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="879ea-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="879ea-249">**Teslimat birimi** – Bir teslimat birimini tamamladığınızda müşteriye fatura kesin.</span><span class="sxs-lookup"><span data-stu-id="879ea-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="879ea-250">Teslimat birimlerini sözleşmede tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="879ea-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="879ea-251">**İlerleme** – Projenin belirli bir yüzdesini bitirdiğinizde müşteriye fatura kesin.</span><span class="sxs-lookup"><span data-stu-id="879ea-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="879ea-252">Tamamlanan çalışma yüzdesini otomatik olarak hesaplamak için bir ödeme kuralı ayarlayabilirsiniz veya yüzdesi tamamlanan çalışmayı ve müşteriye kesilecek fatura tutarını el ile hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="879ea-253">**Kilometre Taşı** – Projenin kilometre taşına ulaşıldığında müşteriye proje tutarının tamamını faturalandırın.</span><span class="sxs-lookup"><span data-stu-id="879ea-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="879ea-254">**Ücret** – Müşteriye hizmetleriniz artı (genellikle hizmetlerin bir yüzdesi olan) bir yönetim ücreti için fatura kesin.</span><span class="sxs-lookup"><span data-stu-id="879ea-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="879ea-255">**Zaman ve malzeme** – Müşteriye projede kullanılan malzemenin ve zamanın değerine göre fatura kesin.</span><span class="sxs-lookup"><span data-stu-id="879ea-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="879ea-256">Tüm faturalama kural türleri için, proje önceden anlaşılan bir aşamaya gelene kadar müşteri faturasından düşülecek bir tutma miktarı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="879ea-257">Ödeme tutma yüzdesi proje sözleşmesinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="879ea-258">Tutar müşteri faturasındaki satıların toplam değerine dayanarak hesaplanır ve bundan çıkartılır.</span><span class="sxs-lookup"><span data-stu-id="879ea-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="879ea-259">**Zaman ve malzeme** ve **Devam eden** faturalama kuralları için, borçlandırılabilir kategoriler atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="879ea-260">Borçlandırılabilir kategoriler müşteri faturalarına dahil edilmesi gereken hareketleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="879ea-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="879ea-261">Müşteriyi faturalamaya hazır olduğunuzda, proje için faturalanacak tutar ödeme kuralları esas alınarak hesaplanır ve bir proje fatura teklifi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="879ea-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="879ea-262">Aşağıdaki bölümlerde bir proje için ödeme kuralları kurmayı ve yönetmeyi gösteren örnekler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="879ea-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="879ea-263">Örnek: Teslim edilen birim sayısını temel alarak bir ödeme kuralı oluşturun</span><span class="sxs-lookup"><span data-stu-id="879ea-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="879ea-264">Kuruluşunuz, müşterinin çalışanlarına her biri 10.000 tutarında olacak 5 eğitim seansı vermek üzere bir anlaşmaya imza atar.</span><span class="sxs-lookup"><span data-stu-id="879ea-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="879ea-265">Her eğitim oturumu sonrasında müşteriye fatura kesersiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="879ea-266">Sözleşme için faturalama kuralları ayarladığınızda, aşağıdaki değerleri kullanırsınız:</span><span class="sxs-lookup"><span data-stu-id="879ea-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="879ea-267">Bir teslimat birimi, bir eğitim oturumudur.</span><span class="sxs-lookup"><span data-stu-id="879ea-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="879ea-268">Birim fiyatı eğitim oturumu başına 10.000'dir.</span><span class="sxs-lookup"><span data-stu-id="879ea-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="879ea-269">Toplam birim sayısı beş eğitim oturumudur.</span><span class="sxs-lookup"><span data-stu-id="879ea-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="879ea-270">Bir eğitim oturumunu tamamladığınızda, teslim edilen ilk birim için 10.000'lik bir fatura oluşturabilirsiniz ve faturayı müşteriye gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="879ea-271">Örnek: Projenin belirli bir tamamlanma yüzdesine dayanan bir faturalama kuralı oluşturun (el ile hesaplama).</span><span class="sxs-lookup"><span data-stu-id="879ea-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="879ea-272">Bir yazılım danışmanlık şirketi olan kuruluşunuz, bir müşteri ile müşterinin geliştirmekte olduğu bir ürünün bir bölümünü geliştirmek üzere anlaşmaya girer.</span><span class="sxs-lookup"><span data-stu-id="879ea-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="879ea-273">Kuruluşunuz yazılım kodunu altı aylık bir dönemde teslim etmeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="879ea-274">Müşteri, bu çalışma için kuruluşunuza toplam 100.000 ödemeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="879ea-275">Müşteriye, sözleşmede belirtildiği üzere, tamamlanan işin yüzdesine dayanacak şekilde fatura kesmek üzere bir faturalama kural oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="879ea-276">İlk ayın sonunda tamamlanan çalışma yüzdesini belirlemek için müşteri ile görüşürsünüz.</span><span class="sxs-lookup"><span data-stu-id="879ea-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="879ea-277">Siz ve müşteri projeyi gözden geçirdikten sonra, projenin tamamlanan yüzdesinin yüzde 15 olduğunu karar verilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="879ea-278">15.000 (100.000'ün yüzde 15'i) için bir fatura oluşturup bunu müşteriye gönderirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="879ea-279">Örnek: Projenin belirli bir tamamlanma yüzdesine dayanan bir faturalama kuralı oluşturun (otomatik hesaplama).</span><span class="sxs-lookup"><span data-stu-id="879ea-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="879ea-280">Bir yazılım geliştirme şirketi olan kuruluşunuz, bir müşteri ile muhasebe bordo paketi yazılımı geliştirmek üzere 30.000'e anlaşır.</span><span class="sxs-lookup"><span data-stu-id="879ea-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="879ea-281">Müşteri, kuruluşunuza işin tamamlanan yüzdesine dayanarak ödeme yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="879ea-282">Proje maliyetinin 20.000 olduğunu tahmin edersiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="879ea-283">Proje sözleşmesi, faturalama işleminde kullanacağınız iş kategorilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="879ea-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="879ea-284">Her kategori için tamamlanan çalışma yüzdesi için fatura tutarlarını otomatik olarak hesaplayacak faturalama kurallarını ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="879ea-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="879ea-285">Her kategori için bir bütçe ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="879ea-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="879ea-286">**Geliştirme** – 15.000'lik maliyet ve 20.000'lik gelir</span><span class="sxs-lookup"><span data-stu-id="879ea-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="879ea-287">**Kurulum** – 5.000'lik maliyet ve 10.000'lik gelir</span><span class="sxs-lookup"><span data-stu-id="879ea-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="879ea-288">İlk kez bir müşteri faturası oluşturduğunuzda, fatura tutarı aşağıdaki bilgilere dayanarak otomatik olarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="879ea-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="879ea-289">Bir ayın sonunda, projeye bakan çalışan, proje için bir zaman çizelgesi gönderir.</span><span class="sxs-lookup"><span data-stu-id="879ea-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="879ea-290">Çalışanın saatlerinin maliyeti, geliştirme için 5.000 ve kurulum için 1.000'dir.</span><span class="sxs-lookup"><span data-stu-id="879ea-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="879ea-291">Geliştirme işi yüzde 33 tamamlanmıştır (5.000 fiili maliyet/15.000 bütçe maliyeti) ve kurulum işi yüzde 20 tamamlanmıştır (1.000 fiili maliyet/5.000 bütçe maliyeti).</span><span class="sxs-lookup"><span data-stu-id="879ea-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="879ea-292">8.667'lik fatura tutarı otomatik olarak hesaplanmış (20.000'in yüzde 33'ü + 10.000'in yüzde 20'si) olur.</span><span class="sxs-lookup"><span data-stu-id="879ea-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="879ea-293">8.667 için bir fatura oluşturup bunu müşteriye gönderirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="879ea-294">Örnek: Üzerinde anlaşılmış kilometre taşlarını temel faturalama kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="879ea-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="879ea-295">Bir yönetim danışmanlık şirketi olan kuruluşunuz, müşterinin satmayı amaçladığı bir ürün için piyasaya araştırması yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="879ea-296">Müşteri hizmetlerinizi Mart ayından başlayarak üç aylık bir sürede almayı ve kuruluşunuza 50.000 ödeme yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="879ea-297">Projenin üç kilometre taşı vardır:</span><span class="sxs-lookup"><span data-stu-id="879ea-297">The project has three milestones:</span></span>

-   <span data-ttu-id="879ea-298">1. Kilometre Taşı: Tüketici verisi toplama - 31 Mart</span><span class="sxs-lookup"><span data-stu-id="879ea-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="879ea-299">2. Kilometre Taşı: Tüketici verilerini çözümleme – 30 Nisan</span><span class="sxs-lookup"><span data-stu-id="879ea-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="879ea-300">3. Kilometre Taşı: Ürün uygunluk teklifi sunmak – 31 Mayıs</span><span class="sxs-lookup"><span data-stu-id="879ea-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="879ea-301">Müşteri, kuruluşunuza ilk kilometre taşı için 10.000, ikinci kilometre taşı için 20.000 ve üçüncü kilometre taşı için 20.000 ödeme yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="879ea-302">Proje sözleşmesini ayarladığınızda, müşteriye tamamlanan kilometre taşlarına dayanarak fatura kesmeyi kabul edersiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="879ea-303">Faturalama kuralı ayarlaması aşağıdaki adımları içerir:</span><span class="sxs-lookup"><span data-stu-id="879ea-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="879ea-304">Proje kilometre taşlarını tanımla.</span><span class="sxs-lookup"><span data-stu-id="879ea-304">Define the project milestones.</span></span>
-   <span data-ttu-id="879ea-305">Her kilometre taşı tamamlandığında, müşteriye faturalanacak miktarı tanımlama.</span><span class="sxs-lookup"><span data-stu-id="879ea-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="879ea-306">İlk kilometre taşı 31 Mart tarihinde tamamlandığında, kilometre taşını tamamlandı olarak işaretleyip, 10.000 değerindeki bir faturayı oluşturmak ve müşteriye göndermek.</span><span class="sxs-lookup"><span data-stu-id="879ea-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="879ea-307">Kilometre taşını tamamlandı olarak seçmediğiniz sürece, bir kilometre taşı için fatura oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="879ea-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="879ea-308">Örnek: Hizmetlerin yanı sıra yönetim ücretini de temel alan faturalama kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="879ea-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="879ea-309">Bir yönetim danışmanlık şirketi olan kuruluşunuz, bir perakende şirketi olan müşterinizin geliştirmekte olduğu bir ürünün uygunluğunu değerlendirmek için piyasa araştırması yapmayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="879ea-310">Anlaşmanın koşulları, zaman ve malzeme tabanlı bir araştırma gerçekleştirecek olan en iyi üç yönetim danışmanınızın hizmetlerini sunacağınızı belirtir.</span><span class="sxs-lookup"><span data-stu-id="879ea-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="879ea-311">Müşteri saat başına 100 artı projeye dahil edilen danışmanlık saatleri için yüzde 10 yönetim ücreti ödemeyi kabul etmiş sayılır.</span><span class="sxs-lookup"><span data-stu-id="879ea-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="879ea-312">Proje sözleşmeni ayarladığınızda, projeye ücretlendirilen danışmanlık saatlerine yüzde 10 yönetim ücret eklemek için bir ödeme kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="879ea-313">Müşteri için bir müşteri faturası oluşturduğunuzda, müşteriye danışmanlık saatlerine ek olarak yüzde 10 yönetim ücreti faturalanır.</span><span class="sxs-lookup"><span data-stu-id="879ea-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="879ea-314">Örneğin, üç danışman projede toplam 200 saat çalıştıysa, 22.000'lik fatura aşağıdaki hesaplama temel alınarak oluşturulur:</span><span class="sxs-lookup"><span data-stu-id="879ea-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="879ea-315">Kişi başı 100'den 200 saat = 20.000</span><span class="sxs-lookup"><span data-stu-id="879ea-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="879ea-316">Yüzde 10 yönetim ücreti = 2.000</span><span class="sxs-lookup"><span data-stu-id="879ea-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="879ea-317">Toplam fatura tutarı = 22.000</span><span class="sxs-lookup"><span data-stu-id="879ea-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="879ea-318">Eğer ücretler müşteriye vergilendirilecekse, proje sözleşmesinde bir vergi grubu seçtiyseniz, vergi grubu ücretlerin faturalama kuralına otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="879ea-319">Örnek: Zaman ve malzemenin değeri için bir faturalama kuralı oluşturma</span><span class="sxs-lookup"><span data-stu-id="879ea-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="879ea-320">Bir yazılım danışmanlık firması olan kuruluşunuz, beş teknik danışmanını bir kullanıcının yazılım geliştirme projesi için önümüzdeki altı ay boyunca sağlamak üzere kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="879ea-321">Müşteri her danışmanlık saati için 150 artı ofis malzemelerinin maliyetini ödemeyi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="879ea-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="879ea-322">Kuruluşunuz, müşteriye her ay sonunda fatura gönderir.</span><span class="sxs-lookup"><span data-stu-id="879ea-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="879ea-323">Proje sözleşmesini ayarladığınızda, projedeki malzeme ve zaman için müşteriye her ay fatura kesmeyi kabul edersiniz.</span><span class="sxs-lookup"><span data-stu-id="879ea-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="879ea-324">Aşağıdaki bilgileri içeren bir ödeme kuralı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="879ea-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="879ea-325">Sözleşme dönemi altı aydır.</span><span class="sxs-lookup"><span data-stu-id="879ea-325">The contract period is six months.</span></span>
-   <span data-ttu-id="879ea-326">Danışmanlık süresi saatlik 150 olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="879ea-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="879ea-327">Ofis malzemeleri maliyetinden faturalanır ve proje için maliyeti toplam 10.000'i aşmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="879ea-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="879ea-328">Proje süresince her takvim ayının sonunda bir müşteri faturası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="879ea-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="879ea-329">İlk ay boyunca danışmanlar tarafından proje üzerinde toplam 800 saat kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="879ea-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="879ea-330">Projeye harcanan ofis malzemelerinin maliyeti 2.000'dir.</span><span class="sxs-lookup"><span data-stu-id="879ea-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="879ea-331">Bu nedenle ay sonunda, saatlik 150'den 800 saat artı ofis malzemeleri için 2.000 toplamında 122.000'lik bir fatura oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="879ea-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




