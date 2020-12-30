---
title: Raporlama seçenekleri
description: Bu konu, bir müşteri Microsoft Dynamics 365 Human Resources raporlarını özelleştirmek istediğinde veya yeni raporlar oluşturmak istediğinde ortaya çıkan sorunun nasıl çözüleceğini açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51d84df5c3c29510e2742148b8c260a2cf402639
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527729"
---
# <a name="reporting-options"></a><span data-ttu-id="51663-103">Raporlama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="51663-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="51663-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="51663-104">**Environment details**</span></span>

<span data-ttu-id="51663-105">Bu sorun tüm ortamlar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="51663-105">This issue applies to all environments.</span></span>

<span data-ttu-id="51663-106">**Belirti**</span><span class="sxs-lookup"><span data-stu-id="51663-106">**Symptom**</span></span>

<span data-ttu-id="51663-107">Müşteri, Microsoft Dynamics 365 Human Resources raporlarını özelleştirmek veya yeni raporlar oluşturmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="51663-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="51663-108">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="51663-108">**Issue**</span></span>

<span data-ttu-id="51663-109">Kullanıcı, katıştırılmış Microsoft Power BI raporlarını özelleştiremiyor.</span><span class="sxs-lookup"><span data-stu-id="51663-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="51663-110">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="51663-110">**Solution**</span></span>

- <span data-ttu-id="51663-111">Common Data Service'e akan İnsan Kaynakları verileri, Power Apps Common Data Service bağlayıcısı aracılığıyla Power BI Desktop'a raporlanabilir.</span><span class="sxs-lookup"><span data-stu-id="51663-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="51663-112">Common Data Service'in, İnsan Kaynakları verisinin bir alt kümesini içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="51663-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="51663-113">Power BI ve panolar hakkında daha fazla bilgi için bkz. [Power BI raporlarını ve panolarını Power Apps Common Data Service ile oluşturma](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="51663-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="51663-114">Elektronik raporlama (ER), İnsan Kaynakları içindeki bazı raporlar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="51663-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="51663-115">Müşteri odaklı özelleştirmeler, ER yapılandırma seçenekleri aracılığıyla yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="51663-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="51663-116">Veri, Microsoft Excel veya Microsoft Word'e, İnsan Kaynakları'nın Microsoft Office tümleştirmesi aracılığıyla sunduğu çeşitli veri varlıkları kullanılarak dışa aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="51663-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="51663-117">**Uzun vadeli çözüm**</span><span class="sxs-lookup"><span data-stu-id="51663-117">**Long-term solution**</span></span>

<span data-ttu-id="51663-118">Ek Power BI seçenekleri kullanılabilir olacaktır ve daha fazla veri ve varlık Common Data Service'in parçası olacaktır.</span><span class="sxs-lookup"><span data-stu-id="51663-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
