---
title: Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler
description: Bu konu, Microsoft Dynamics Lifecycle Services'ten (LCS) kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: AngelMarshall
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e583ec66f24940f44113433042f5e2340cf0f52c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748451"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="1025e-103">Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler</span><span class="sxs-lookup"><span data-stu-id="1025e-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1025e-104">Bu konu, Microsoft Dynamics Lifecycle Services (LCS) için kaldırılmış veya artık kullanılmayan özellikleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="1025e-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="1025e-105">*Kaldırılan* özellik artık hizmette bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="1025e-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="1025e-106">*Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="1025e-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="1025e-107">Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="1025e-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="1025e-108">Ekim 2019 duyuruları</span><span class="sxs-lookup"><span data-stu-id="1025e-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="1025e-109">İş süreci modelleyicideki akış tabloları</span><span class="sxs-lookup"><span data-stu-id="1025e-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="1025e-110"><strong>Kullanımı sonlandırma/kaldırma nedeni</strong></span><span class="sxs-lookup"><span data-stu-id="1025e-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="1025e-111">Eski tasarım düşük kullanıma neden olduğundan, İş süreci modelleyici (BPM) içindeki akış çizelgesi diyagramları bileşenini yeniden modelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="1025e-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1025e-112"><strong>Başka bir özellik ile değiştirildi?</strong></span><span class="sxs-lookup"><span data-stu-id="1025e-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="1025e-113">Hayır</span><span class="sxs-lookup"><span data-stu-id="1025e-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1025e-114"><strong>Etkilenen alanlar</strong></span><span class="sxs-lookup"><span data-stu-id="1025e-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="1025e-115">İş süreci modelleyici</span><span class="sxs-lookup"><span data-stu-id="1025e-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1025e-116"><strong>Durum</strong></span><span class="sxs-lookup"><span data-stu-id="1025e-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="1025e-117">Kullanım dışı: BPM içindeki akış grafiği diyagramları bileşeninin 2020 tarihinde ilk olarak kaldırılması beklenir.</span><span class="sxs-lookup"><span data-stu-id="1025e-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed in 2020.</span></span> <span data-ttu-id="1025e-118">Aşağıdaki işlevler kullanılamayacak:</span><span class="sxs-lookup"><span data-stu-id="1025e-118">The following functionality will be unavailable:</span></span>
<ul>
<li><span data-ttu-id="1025e-119">Tüm akış çizelgeleri salt okunur olacak ve düzenleme için uygun olmayacak.</span><span class="sxs-lookup"><span data-stu-id="1025e-119">All flowcharts will be read-only and unavailable for editing.</span></span> <span data-ttu-id="1025e-120">Akış çizelgesi etkinlikleriyle ilişkilendirilmiş şekil özellikleri de kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="1025e-120">The shape properties that are associated with flowchart activities will also be unavailable.</span></span> <span data-ttu-id="1025e-121">Bu akış çizelgeleri, otomatik olarak oluşturulan varsayılan akış çizelgeleri ve varsayılan akış çizelgeleri temel alınarak değiştirilmiş özel akış çizelgeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="1025e-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="1025e-122">İşlem adımları salt okunur olacak ve düzenleme için uygun olmayacak.</span><span class="sxs-lookup"><span data-stu-id="1025e-122">The process steps will be read-only and unavailable for editing.</span></span></li>     
<li><span data-ttu-id="1025e-123">Eski sığdırma/boşluk analizi özelliği kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="1025e-123">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="1025e-124">Bu nedenle, hiçbir Aralık listesi otomatik olarak oluşturulmayacak veya dışa aktarma için kullanılabilir olmayacak.</span><span class="sxs-lookup"><span data-stu-id="1025e-124">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="1025e-125"><strong>Not:</strong> Bu özellik daha önce kaldırılmış ve Microsoft Azure DevOps tümleştirmeviyle değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="1025e-125"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="1025e-126">Akış çizelgesinin sürüm geçmişi kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="1025e-126">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]