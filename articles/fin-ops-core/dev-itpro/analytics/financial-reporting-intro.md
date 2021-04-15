---
title: Mali raporlama
description: Mali raporlama, finans ve şirket profesyonellerinin mali tabloları oluşturmasını, güncelleştirmesini, dağıtmasını ve görüntülemesini sağlar.
author: aprilolson
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0dbe9621760fbb56eb8123d58f72e2fb0080c4f4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743422"
---
# <a name="financial-reporting"></a><span data-ttu-id="9d9bc-103">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="9d9bc-103">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d9bc-104">Uygulama için finansal raporlama, finans ve şirket profesyonellerinin mali tabloları oluşturmasını, güncellemesini, dağıtmasını ve görüntülemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-104">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="9d9bc-105">Geleneksel raporlama kısıtlamalarının ötesine geçerek çeşitli rapor türlerini etkin şekilde oluşturmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-105">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="9d9bc-106">Mali raporlama boyut desteği içerir.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-106">Financial reporting includes dimension support.</span></span> <span data-ttu-id="9d9bc-107">Bu nedenle, hesap segmentleri veya boyutları derhal kullanılabilir hale gelir</span><span class="sxs-lookup"><span data-stu-id="9d9bc-107">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="9d9bc-108">Ek araçlar veya yapılandırma adımları gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-108">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="9d9bc-109">Mali raporlama ayarı</span><span class="sxs-lookup"><span data-stu-id="9d9bc-109">Financial reporting setup</span></span>
<span data-ttu-id="9d9bc-110">**Mali raporlama kurulumu** sayfası sistemdeki tüm finansal boyutların listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-110">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="9d9bc-111">**Genel muhasebe** \> **Genel muhasebe ayarı** \> **Mali raporlama ayarı**.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-111">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="9d9bc-112">**Mali raporlama kurulumu** sayfası, Mali raporda bildirdiğiniz verileri belirleyen iki bölüm içerir:</span><span class="sxs-lookup"><span data-stu-id="9d9bc-112">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="9d9bc-113">**Boyutlar sekmesi**: Farklı şirketler farklı boyutlar ve hesap yapıları kullandığından, kullanıcıların raporlarda tüm mali boyutları görüntülemek istediği sırayı belirlemenin bir yolu yoktur.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-113">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="9d9bc-114">Bu sayfa, Mali raporlamada bir rapor oluşturduğunuzda ve görüntülediğinizde mali boyutların görünmesini istediğiniz sırayı ayarlamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-114">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="9d9bc-115">**Öznitelikler sekmesi**, **Satıcılar** ve **Müşteriler**'i filtreleme ve rapor tasarımı için öznitelik olarak kullanmayı isteyip istemediğinizi seçebileceğiniz alandır.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-115">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="9d9bc-116">Satıcı ve Müşteri üzerinde raporlama yapmak ancak hareketleri deftere naklederken birden çok müşteri veya satıcıyı tek bir fişe girmiyor olmanız durumunda değerlidir.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-116">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="9d9bc-117">Müşteri ve/veya Satıcı seçme tümleştirmeye ek süre ekler.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-117">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="9d9bc-118">Mali raporlama bileşenleri</span><span class="sxs-lookup"><span data-stu-id="9d9bc-118">Financial reporting components</span></span>
<span data-ttu-id="9d9bc-119">Mali raporlamanın aşağıdaki bileşenleri raporların oluşturulmasını, görüntülenmesini ve programlanmasını kolaylaştırır.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-119">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="9d9bc-120">Bileşen</span><span class="sxs-lookup"><span data-stu-id="9d9bc-120">Component</span></span>        | <span data-ttu-id="9d9bc-121">İşlevler</span><span class="sxs-lookup"><span data-stu-id="9d9bc-121">Functions</span></span> | <span data-ttu-id="9d9bc-122">Ek bilgiler</span><span class="sxs-lookup"><span data-stu-id="9d9bc-122">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="9d9bc-123">Rapor Tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="9d9bc-123">Report Designer</span></span>  | <span data-ttu-id="9d9bc-124">Bir rapor tanımlamak ve oluşturmak için birleştirilebilecek rapor yapı taşları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-124">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="9d9bc-125">Rapor sihirbazı daha az deneyimli kullanıcılara tasarım süreci boyunca rehberlik eder.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-125">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="9d9bc-126">İleri düzey kullanıcılar, yeni rapor yapı taşları oluşturabilir veya mevcut yapı taşlarını gereksinimlerini karşılayacak şekilde değiştirebilirler.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-126">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="9d9bc-127">Rapor programları</span><span class="sxs-lookup"><span data-stu-id="9d9bc-127">Report schedules</span></span> | <span data-ttu-id="9d9bc-128">Düzenli aralıklarla oluşturulması için tek bir raporu veya bir raporlar grubu planlayın.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-128">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="9d9bc-129">Mali raporlar oluşturma</span><span class="sxs-lookup"><span data-stu-id="9d9bc-129">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="9d9bc-130">Özellikler</span><span class="sxs-lookup"><span data-stu-id="9d9bc-130">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="9d9bc-131">Özellik</span><span class="sxs-lookup"><span data-stu-id="9d9bc-131">Feature</span></span></th>
<th><span data-ttu-id="9d9bc-132">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d9bc-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d9bc-133">Rapor tasarım esnekliği</span><span class="sxs-lookup"><span data-stu-id="9d9bc-133">Report design flexibility</span></span></td>
<td><span data-ttu-id="9d9bc-134">Rapor Tasarımcısı, bir rapor tasarlarken size şu raporlama seçeneklerini sağlar:</span><span class="sxs-lookup"><span data-stu-id="9d9bc-134">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="9d9bc-135">Boyut birleşimlerini kaydedin ve boyutları birden fazla rapor için yeniden kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-135">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="9d9bc-136">Boyut açıklamalarının nasıl biçimlendirilip görüntülendiğini kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-136">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="9d9bc-137">Rapor yapı taşlarında atlanan hesapları veya boyutları belirleyin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-137">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="9d9bc-138">Toplanan tahminler için başlıkları biçimlendirin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-138">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d9bc-139">Mali rapor iş birliği</span><span class="sxs-lookup"><span data-stu-id="9d9bc-139">Financial report collaboration</span></span></td>
<td><span data-ttu-id="9d9bc-140">Aşağıdaki özellikler raporların oluşturulmasını ve dağıtılmasını yönetmenize yardımcı olur:</span><span class="sxs-lookup"><span data-stu-id="9d9bc-140">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="9d9bc-141">Raporları günlük, haftalık, aylık veya yıllık olarak otomatik şekilde oluşturulmaları için planlayın.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-141">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="9d9bc-142">Dijital imzalarla daha iyi belge güvenliği sunan salt okunur XPS biçiminde dışa aktarın.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-142">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="9d9bc-143">Bir Microsoft Excel çalışma sayfasına aktarın.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-143">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="9d9bc-144">Raporları paylaşmak için, raporlara ait bağlantılar içeren e-posta iletileri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-144">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="9d9bc-145">Etkileşimli rapor görüntüleme</span><span class="sxs-lookup"><span data-stu-id="9d9bc-145">Interactive report viewing</span></span></td>
<td><span data-ttu-id="9d9bc-146">Etkileşimli özellikler aşağıdaki görevleri yerine getirmenizi sağlar:</span><span class="sxs-lookup"><span data-stu-id="9d9bc-146">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="9d9bc-147">Görüntülediğiniz raporun rapor tarihini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-147">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="9d9bc-148">Görüntülediğiniz raporun para birimini değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-148">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="9d9bc-149">Raporu özet veya ayrıntılı görünümde görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-149">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="9d9bc-150">Rapor içeriğini belirli bir boyutla veya boyut birleşimiyle sınırlandırmak için boyut filtreleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-150">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="9d9bc-151">Rapor içeriğini belirli bir öznitelikle veya öznitelik birleşimiyle sınırlandırmak için öznitelik filtreleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="9d9bc-151">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="9d9bc-152">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9d9bc-152">Additional resources</span></span>
[<span data-ttu-id="9d9bc-153">Mali raporlar oluşturma</span><span class="sxs-lookup"><span data-stu-id="9d9bc-153">Generate financial reports</span></span>](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]