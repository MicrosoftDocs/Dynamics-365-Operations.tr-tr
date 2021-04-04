---
title: Raporlama seçenekleri
description: Bu konu, bir müşteri Microsoft Dynamics 365 Human Resources raporlarını özelleştirmek istediğinde veya yeni raporlar oluşturmak istediğinde ortaya çıkan sorunun nasıl çözüleceğini açıklar.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 66581331dceacc1c0fa1816bf336339693db5339
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463298"
---
# <a name="reporting-options"></a><span data-ttu-id="4108b-103">Raporlama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="4108b-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4108b-104">**Ortam ayrıntıları**</span><span class="sxs-lookup"><span data-stu-id="4108b-104">**Environment details**</span></span>

<span data-ttu-id="4108b-105">Bu sorun tüm ortamlar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="4108b-105">This issue applies to all environments.</span></span>

<span data-ttu-id="4108b-106">**Belirti**</span><span class="sxs-lookup"><span data-stu-id="4108b-106">**Symptom**</span></span>

<span data-ttu-id="4108b-107">Müşteri, Microsoft Dynamics 365 Human Resources raporlarını özelleştirmek veya yeni raporlar oluşturmak istiyor.</span><span class="sxs-lookup"><span data-stu-id="4108b-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="4108b-108">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="4108b-108">**Issue**</span></span>

<span data-ttu-id="4108b-109">Kullanıcı, katıştırılmış Microsoft Power BI raporlarını özelleştiremiyor.</span><span class="sxs-lookup"><span data-stu-id="4108b-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="4108b-110">**Çözüm**</span><span class="sxs-lookup"><span data-stu-id="4108b-110">**Solution**</span></span>

- <span data-ttu-id="4108b-111">Dataverse'e akan İnsan Kaynakları verileri, Power Apps Dataverse bağlayıcısı aracılığıyla Power BI Desktop'a raporlanabilir.</span><span class="sxs-lookup"><span data-stu-id="4108b-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="4108b-112">Dataverse'in, İnsan Kaynakları verisinin bir alt kümesini içerdiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4108b-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="4108b-113">Power BI ve panolar hakkında daha fazla bilgi için bkz. [Power BI raporlarını ve panolarını Power Apps Common Data Service ile oluşturma](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="4108b-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="4108b-114">Elektronik raporlama (ER), İnsan Kaynakları içindeki bazı raporlar için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4108b-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="4108b-115">Müşteri odaklı özelleştirmeler, ER yapılandırma seçenekleri aracılığıyla yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="4108b-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="4108b-116">Veri, Microsoft Excel veya Microsoft Word'e, İnsan Kaynakları'nın Microsoft Office tümleştirmesi aracılığıyla sunduğu çeşitli veri varlıkları kullanılarak dışa aktarılabilir.</span><span class="sxs-lookup"><span data-stu-id="4108b-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="4108b-117">**Uzun vadeli çözüm**</span><span class="sxs-lookup"><span data-stu-id="4108b-117">**Long-term solution**</span></span>

<span data-ttu-id="4108b-118">Ek Power BI seçenekleri kullanılabilir olacaktır ve daha fazla veri ve varlık Dataverse'in parçası olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4108b-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]