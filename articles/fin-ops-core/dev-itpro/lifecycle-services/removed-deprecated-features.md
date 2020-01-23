---
title: Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler
description: Bu konu, Microsoft Dynamics Lifecycle Services'ten (LCS) kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885467"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a><span data-ttu-id="0bbfe-103">Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler</span><span class="sxs-lookup"><span data-stu-id="0bbfe-103">Removed or deprecated features in Lifecycle Services (LCS)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0bbfe-104">Bu konu, Microsoft Dynamics Lifecycle Services (LCS) için kaldırılmış veya artık kullanılmayan özellikleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-104">This topic describes features that have been removed or deprecated for Microsoft Dynamics Lifecycle Services (LCS).</span></span>

- <span data-ttu-id="0bbfe-105">*Kaldırılan* özellik artık hizmette bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-105">A *removed* feature is no longer available in the service.</span></span>
- <span data-ttu-id="0bbfe-106">*Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-106">A *deprecated* feature isn't in active development and might be removed in a future update.</span></span>

<span data-ttu-id="0bbfe-107">Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-107">This list is provided so that you can consider these removals and deprecations as you do your own planning.</span></span>

## <a name="october-2019-announcements"></a><span data-ttu-id="0bbfe-108">Ekim 2019 duyuruları</span><span class="sxs-lookup"><span data-stu-id="0bbfe-108">October 2019 announcements</span></span>

### <a name="flowchart-diagrams-in-business-process-modeler"></a><span data-ttu-id="0bbfe-109">İş süreci modelleyicideki akış tabloları</span><span class="sxs-lookup"><span data-stu-id="0bbfe-109">Flowchart diagrams in Business process modeler</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="0bbfe-110"><strong>Kullanımı sonlandırma/kaldırma nedeni</strong></span><span class="sxs-lookup"><span data-stu-id="0bbfe-110"><strong>Reason for deprecation/removal</strong></span></span></td>
<td><span data-ttu-id="0bbfe-111">Eski tasarım düşük kullanıma neden olduğundan, İş süreci modelleyici (BPM) içindeki akış çizelgesi diyagramları bileşenini yeniden modelliyoruz.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-111">We are deprecating the flowchart diagrams component in Business process modeler (BPM), because the legacy design caused low usage.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bbfe-112"><strong>Başka bir özellik ile değiştirildi?</strong></span><span class="sxs-lookup"><span data-stu-id="0bbfe-112"><strong>Replaced by another feature?</strong></span></span></td>
<td><span data-ttu-id="0bbfe-113">Hayır</span><span class="sxs-lookup"><span data-stu-id="0bbfe-113">No</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bbfe-114"><strong>Etkilenen alanlar</strong></span><span class="sxs-lookup"><span data-stu-id="0bbfe-114"><strong>Areas affected</strong></span></span></td>
<td><span data-ttu-id="0bbfe-115">İş süreci modelleyici</span><span class="sxs-lookup"><span data-stu-id="0bbfe-115">Business process modeler</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0bbfe-116"><strong>Durum</strong></span><span class="sxs-lookup"><span data-stu-id="0bbfe-116"><strong>Status</strong></span></span></td>
<td><span data-ttu-id="0bbfe-117">Kullanım dışı: BPM içindeki akış grafiği diyagramları bileşeninin 2020 Şubat tarihinde ilk olarak kaldırılması beklenir.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-117">Deprecated: The flowchart diagrams component in BPM is expected to be removed by early February 2020.</span></span> <span data-ttu-id="0bbfe-118">Aşağıdaki işlevler kaldırılacak:</span><span class="sxs-lookup"><span data-stu-id="0bbfe-118">The following functionality will be removed:</span></span>
<ul>
<li><span data-ttu-id="0bbfe-119">Varolan akış çizelgeleri görüntülemek veya düzenlemek için kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-119">Existing flowcharts will be unavailable for viewing or editing.</span></span> <span data-ttu-id="0bbfe-120">Akış çizelgesi etkinlikleriyle ilişkilendirilmiş şekil özellikleri de kullanılamayacak, çünkü <strong>akış grafiği</strong> sekmesinin tamamı kaldırılacak.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-120">The shape properties that are associated with flowchart activities will also be unavailable, because the whole <strong>Flowchart</strong> tab will be removed.</span></span> <span data-ttu-id="0bbfe-121">Bu akış çizelgeleri, otomatik olarak oluşturulan varsayılan akış çizelgeleri ve varsayılan akış çizelgeleri temel alınarak değiştirilmiş özel akış çizelgeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-121">These flowcharts include both the default flowcharts that are automatically generated and customized flowcharts that are modified based on those default flowcharts.</span></span></li>
<li><span data-ttu-id="0bbfe-122">Eski sığdırma/boşluk analizi özelliği kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-122">The legacy fit/gap analysis feature will be unavailable.</span></span> <span data-ttu-id="0bbfe-123">Bu nedenle, hiçbir Aralık listesi otomatik olarak oluşturulmayacak veya dışa aktarma için kullanılabilir olmayacak.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-123">Therefore, no gap list will be automatically created or available for export.</span></span>
<p><span data-ttu-id="0bbfe-124"><strong>Not:</strong> Bu özellik daha önce kaldırılmış ve Microsoft Azure DevOps tümleştirmeviyle değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-124"><strong>Note:</strong> This feature had previously been deprecated and replaced by Microsoft Azure DevOps integrations.</span></span></p>
</li>
<li><span data-ttu-id="0bbfe-125">Akış çizelgesinin sürüm geçmişi kullanılamayacak.</span><span class="sxs-lookup"><span data-stu-id="0bbfe-125">The version history of the flowchart will be unavailable.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
