---
title: RCS/genel depoda RCS gelişmiş filtre uygulama
description: Bu konu, ek filtreler içermek üzere geliştirilmiş olan RCS Genel deposu için gelişmiş filtreleme özelliklerini açıklamaktadır.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 87ada5a97d2b716145082b3845fa87a12df57ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235609"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a><span data-ttu-id="25b5d-103">RCS/Genel depoda yapılandırmaları bulmak için RCS gelişmiş filtreleme seçenekleri</span><span class="sxs-lookup"><span data-stu-id="25b5d-103">RCS enhanced filtering options for finding configurations in the RCS/Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25b5d-104">Bu konu, aşağıdaki ölçütlere sahip filtreleme olanağını içermek üzere geliştirilmiş olan Regulatory Configuration Services (RCS) Genel deposu için gelişmiş filtreleme özelliklerini açıklamaktadır:</span><span class="sxs-lookup"><span data-stu-id="25b5d-104">This topic describes enhanced filtering capabilities for Regulatory Configuration Services (RCS) Global repository, which have been improved to include the ability to filter with the following criteria:</span></span> 
- <span data-ttu-id="25b5d-105">**Ülke/bölge** - ISO ülke kodlarını temel alarak</span><span class="sxs-lookup"><span data-stu-id="25b5d-105">**Country/region** - Based on ISO country codes</span></span>  
- <span data-ttu-id="25b5d-106">**Etiket** türleri:</span><span class="sxs-lookup"><span data-stu-id="25b5d-106">**Tags** types for:</span></span>
  - <span data-ttu-id="25b5d-107">İşlevsel alan</span><span class="sxs-lookup"><span data-stu-id="25b5d-107">Functional area</span></span>
  - <span data-ttu-id="25b5d-108">Özellik alanı</span><span class="sxs-lookup"><span data-stu-id="25b5d-108">Feature area</span></span>
  - <span data-ttu-id="25b5d-109">Sektör</span><span class="sxs-lookup"><span data-stu-id="25b5d-109">Industry</span></span> 
  - <span data-ttu-id="25b5d-110">İş belgesi</span><span class="sxs-lookup"><span data-stu-id="25b5d-110">Business document</span></span> 

<span data-ttu-id="25b5d-111">Belirli veya ilgili yapılandırmaları daha kolay bulmak için, ayrı olarak veya grup halinde filtreler uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25b5d-111">To make it easier to discover specific or related configurations you can apply filters, either individually or as a group.</span></span> <span data-ttu-id="25b5d-112">Örneğin, satıcı faturalarıyla ilişkili yapılandırılabilir iş belgelerinin tek bir türünü bulmak için, bu belge türünü aramak üzere **İş belgesi türü** filtresi uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25b5d-112">For example, to find a single type of 'configurable business documents that are related to vendor invoices, you could apply a **Business document type** filter to search for that type of document.</span></span> 

<span data-ttu-id="25b5d-113">[![Genel depo için filtre bölümü](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span><span class="sxs-lookup"><span data-stu-id="25b5d-113">[![Filter section for Global repository](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG)</span></span> 

<span data-ttu-id="25b5d-114">Belge türünü seçip (örneğin 'satıcı faturası') **Filtre uygula**'ya tıklayarak aramayı daha da belirginleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="25b5d-114">You can further refine the search by selecting document type, for example 'vendor invoice' and clicking **Apply filter**.</span></span> <span data-ttu-id="25b5d-115">Aşağıdaki örnek, **İş belgesi türü**'nde filtre uygulandığındaki sonuçları belge türü eklenmiş şekilde gösterir.</span><span class="sxs-lookup"><span data-stu-id="25b5d-115">The following example shows the results when filtering on **Business document type** with the document type added.</span></span> 

<span data-ttu-id="25b5d-116">[![İş belgesi türü için uygulanan filtre ve içe aktarma](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span><span class="sxs-lookup"><span data-stu-id="25b5d-116">[![Applied filter and Import for business document type](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG)</span></span> 

<span data-ttu-id="25b5d-117">Filtre uygulanan sonuçlar bir kullanıcı RCS deposuna veya Dynamics 365 Finance ortamına tek başına veya küme olarak aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="25b5d-117">Filtered results can be imported into a users RCS repository or a Dynamics 365 Finance environment, either individually or as a set.</span></span> <span data-ttu-id="25b5d-118">Bunu yapmak için, yapılandırmalar grubunu seçin ve **İçe aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="25b5d-118">To do this, select the group of configurations, and click **Import**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]