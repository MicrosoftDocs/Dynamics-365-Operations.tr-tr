---
title: Mali raporlama
description: Finance and Operations için mali raporlama, finans ve şirket profesyonellerinin mali tabloları oluşturmasını, güncelleştirmesini, dağıtmasını ve görüntülemesini sağlar. Farklı türlerde raporlar tasarlamanıza yardımcı olmak için geleneksel raporlama kısıtlamalarının ötesine geçer.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1a1221f12024060f324e2a61f1de39959bfbd868
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849617"
---
# <a name="financial-reporting"></a><span data-ttu-id="2899f-104">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="2899f-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2899f-105">Finance and Operations için mali raporlama, finans ve şirket profesyonellerinin mali tabloları oluşturmasını, güncelleştirmesini, dağıtmasını ve görüntülemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2899f-105">Financial reporting for Finance and Operations allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="2899f-106">Geleneksel raporlama kısıtlamalarının ötesine geçerek çeşitli rapor türlerini etkin şekilde oluşturmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="2899f-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="2899f-107">Mali raporlama boyut desteği içerir.</span><span class="sxs-lookup"><span data-stu-id="2899f-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="2899f-108">Bu nedenle, hesap segmentleri veya boyutları derhal kullanılabilir hale gelir</span><span class="sxs-lookup"><span data-stu-id="2899f-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="2899f-109">Ek araçlar veya yapılandırma adımları gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="2899f-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="2899f-110">Mali raporlama ayarı</span><span class="sxs-lookup"><span data-stu-id="2899f-110">Financial reporting setup</span></span>
<span data-ttu-id="2899f-111">**Mali raporlama kurulumu** sayfası sistemdeki tüm finansal boyutların listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="2899f-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="2899f-112">**Genel muhasebe** \> **Genel muhasebe ayarı** \> **Mali raporlama ayarı**.</span><span class="sxs-lookup"><span data-stu-id="2899f-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="2899f-113">**Mali raporlama kurulumu** sayfası, Mali raporda bildirdiğiniz verileri belirleyen iki bölüm içerir:</span><span class="sxs-lookup"><span data-stu-id="2899f-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="2899f-114">**Boyutlar sekmesi**: Farklı şirketler farklı boyutlar ve hesap yapıları kullandığından, kullanıcıların raporlarda tüm mali boyutları görüntülemek istediği sırayı belirlemenin bir yolu yoktur.</span><span class="sxs-lookup"><span data-stu-id="2899f-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="2899f-115">Bu sayfa, Mali raporlamada bir rapor oluşturduğunuzda ve görüntülediğinizde mali boyutların görünmesini istediğiniz sırayı ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2899f-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="2899f-116">**Öznitelikler sekmesi**, **Satıcılar** ve **Müşteriler**'i filtreleme ve rapor tasarımı için öznitelik olarak kullanmayı isteyip istemediğinizi seçebileceğiniz alandır.</span><span class="sxs-lookup"><span data-stu-id="2899f-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="2899f-117">Satıcı ve Müşteri üzerinde raporlama yapmak ancak hareketleri deftere naklederken birden çok müşteri veya satıcıyı tek bir fişe girmiyor olmanız durumunda değerlidir.</span><span class="sxs-lookup"><span data-stu-id="2899f-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="2899f-118">Müşteri ve/veya Satıcı seçme tümleştirmeye ek süre ekler.</span><span class="sxs-lookup"><span data-stu-id="2899f-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="2899f-119">Mali raporlama bileşenleri</span><span class="sxs-lookup"><span data-stu-id="2899f-119">Financial reporting components</span></span>
<span data-ttu-id="2899f-120">Mali raporlamanın aşağıdaki bileşenleri raporların oluşturulmasını, görüntülenmesini ve programlanmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="2899f-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="2899f-121">Bileşen</span><span class="sxs-lookup"><span data-stu-id="2899f-121">Component</span></span>        | <span data-ttu-id="2899f-122">İşlevler</span><span class="sxs-lookup"><span data-stu-id="2899f-122">Functions</span></span> | <span data-ttu-id="2899f-123">Ek bilgiler</span><span class="sxs-lookup"><span data-stu-id="2899f-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="2899f-124">Rapor Tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="2899f-124">Report Designer</span></span>  | <span data-ttu-id="2899f-125">Bir rapor tanımlamak ve oluşturmak için birleştirilebilecek rapor yapı taşları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="2899f-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="2899f-126">Rapor sihirbazı daha az deneyimli kullanıcılara tasarım süreci boyunca rehberlik eder.</span><span class="sxs-lookup"><span data-stu-id="2899f-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="2899f-127">İleri düzey kullanıcılar, yeni rapor yapı taşları oluşturabilir veya mevcut yapı taşlarını gereksinimlerini karşılayacak şekilde değiştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="2899f-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="2899f-128">Rapor programları</span><span class="sxs-lookup"><span data-stu-id="2899f-128">Report schedules</span></span> | <span data-ttu-id="2899f-129">Düzenli aralıklarla oluşturulması için tek bir raporu veya bir raporlar grubu planlayın.</span><span class="sxs-lookup"><span data-stu-id="2899f-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="2899f-130">Mali rapor oluşturma</span><span class="sxs-lookup"><span data-stu-id="2899f-130">Generate a financial report</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="2899f-131">Özellikler</span><span class="sxs-lookup"><span data-stu-id="2899f-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="2899f-132">Özellik</span><span class="sxs-lookup"><span data-stu-id="2899f-132">Feature</span></span></th>
<th><span data-ttu-id="2899f-133">Açıklama</span><span class="sxs-lookup"><span data-stu-id="2899f-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2899f-134">Rapor tasarım esnekliği</span><span class="sxs-lookup"><span data-stu-id="2899f-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="2899f-135">Rapor Tasarımcısı, bir rapor tasarlarken size şu raporlama seçeneklerini sağlar:</span><span class="sxs-lookup"><span data-stu-id="2899f-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="2899f-136">Boyut birleşimlerini kaydedin ve boyutları birden fazla rapor için yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="2899f-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="2899f-137">Boyut açıklamalarının nasıl biçimlendirilip görüntülendiğini kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="2899f-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="2899f-138">Rapor yapı taşlarında atlanan hesapları veya boyutları belirleyin.</span><span class="sxs-lookup"><span data-stu-id="2899f-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="2899f-139">Toplanan tahminler için başlıkları biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="2899f-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="2899f-140">Mali rapor işbirliği</span><span class="sxs-lookup"><span data-stu-id="2899f-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="2899f-141">Aşağıdaki özellikler raporların oluşturulmasını ve dağıtılmasını yönetmenize yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="2899f-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="2899f-142">Raporları günlük, haftalık, aylık veya yıllık olarak otomatik şekilde oluşturulmaları için planlayın.</span><span class="sxs-lookup"><span data-stu-id="2899f-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="2899f-143">Dijital imzalarla daha iyi belge güvenliği sunan salt okunur XPS biçiminde dışa aktarın.</span><span class="sxs-lookup"><span data-stu-id="2899f-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="2899f-144">Bir Microsoft Excel çalışma sayfasına aktarın.</span><span class="sxs-lookup"><span data-stu-id="2899f-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="2899f-145">Raporları paylaşmak için, raporlara ait bağlantılar içeren e-posta iletileri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2899f-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="2899f-146">Etkileşimli rapor görüntüleme</span><span class="sxs-lookup"><span data-stu-id="2899f-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="2899f-147">Etkileşimli özellikler aşağıdaki görevleri yerine getirmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="2899f-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="2899f-148">Görüntülediğiniz raporun rapor tarihini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2899f-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="2899f-149">Görüntülediğiniz raporun para birimini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2899f-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="2899f-150">Raporu özet veya ayrıntılı görünümde görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="2899f-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="2899f-151">Rapor içeriğini belirli bir boyutla veya boyut birleşimiyle sınırlandırmak için boyut filtreleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2899f-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="2899f-152">Rapor içeriğini belirli bir öznitelikle veya öznitelik birleşimiyle sınırlandırmak için öznitelik filtreleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2899f-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="2899f-153">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2899f-153">Additional resources</span></span>
[<span data-ttu-id="2899f-154">Mali rapor oluşturma</span><span class="sxs-lookup"><span data-stu-id="2899f-154">Generate a financial report</span></span>](generate-financial-report.md)
