---
title: Talent içerisinde raporlama seçenekleri
description: Bu konu, bir müşteri Microsoft Dynamics 365 for Talent raporlarını özelleştirmek istediğinde veya yeni raporlar oluşturmak istediğinde ortaya çıkan sorunun nasıl çözüleceğini açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7e00a6e4fc01f72e1ef2347e08754997135215ed
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519326"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="ce88f-103">Talent'taki raporlama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="ce88f-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ce88f-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="ce88f-104">**Environment details**</span></span>

<span data-ttu-id="ce88f-105">Bu sorun tüm ortamlar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="ce88f-105">This issue applies to all environments.</span></span>

<span data-ttu-id="ce88f-106">**Belirti**</span><span class="sxs-lookup"><span data-stu-id="ce88f-106">**Symptom**</span></span>

<span data-ttu-id="ce88f-107">Müşteri, Microsoft Dynamics 365 for Talent raporlarını özelleştirmek veya yeni raporlar oluşturmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="ce88f-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="ce88f-108">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="ce88f-108">**Issue**</span></span>

<span data-ttu-id="ce88f-109">Kullanıcı, katıştırılmış Microsoft Power BI raporlarını özelleştiremiyor.</span><span class="sxs-lookup"><span data-stu-id="ce88f-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="ce88f-110">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="ce88f-110">**Solution**</span></span>

- <span data-ttu-id="ce88f-111">Common Data Service'a akan Core HR veriler, PowerApps Common Data Service bağlayıcısı aracılığıyla Power BI Desktop'a raporlanabilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ce88f-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="ce88f-112">Common Data Service'in, Core HR verisinin bir alt kümesini içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ce88f-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="ce88f-113">Power BI ve panolar hakkında daha fazla bilgi için bkz. [Power BI raporları ve panolarını PowerApps Common Data Service ile birlikte oluşturmak](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="ce88f-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="ce88f-114">Elektronik raporlama (ER), Talent içindeki bazı raporlar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce88f-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="ce88f-115">Müşteri odaklı özelleştirmeler, ER yapılandırma seçenekleri aracılığıyla yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce88f-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="ce88f-116">Veri, Microsoft Excel veya Microsoft Word'e, Talent'ın Microsoft Office tümleştirmesi aracılığıyla sunduğu çeşitli veri varlıkları kullanılarak dışa aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="ce88f-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="ce88f-117">**Uzun vadeli çözüm**</span><span class="sxs-lookup"><span data-stu-id="ce88f-117">**Long-term solution**</span></span>

<span data-ttu-id="ce88f-118">Ek Power BI seçenekleri kullanılabilir olacaktır ve daha fazla veri ve varlık Common Data Service'in parçası olacaktır.</span><span class="sxs-lookup"><span data-stu-id="ce88f-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
