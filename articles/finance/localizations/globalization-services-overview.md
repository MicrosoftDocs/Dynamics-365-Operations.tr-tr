---
title: Dynamics 365 genelleştirme hizmetleri
description: Bu konu, Microsoft Dynamics 365 genelleştirme hizmetlerine genel bir bakış sağlar.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893060"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="0b6ab-103">Dynamics 365 genelleştirme hizmetleri</span><span class="sxs-lookup"><span data-stu-id="0b6ab-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b6ab-104">Aşağıdaki genelleştirme hizmetleri, bazı Microsoft Dynamics 365 çevrimiçi hizmetlerinde bulunan özellikleri genişletmek için yapılandırılabilir:</span><span class="sxs-lookup"><span data-stu-id="0b6ab-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="0b6ab-105">**Regulatory Configuration Service (RCS)**, farklı türdeki elektronik belge ve raporların yapılandırılmasını destekler.</span><span class="sxs-lookup"><span data-stu-id="0b6ab-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="0b6ab-106">RCS, Elektronik raporlama (ER) tasarımcısının, yapılandırma deposunun bağımsız bir hizmet olduğu gelişmiş bir sürümünü sağlar.</span><span class="sxs-lookup"><span data-stu-id="0b6ab-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="0b6ab-107">Daha fazla bilgi için, bkz. [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b6ab-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="0b6ab-108">**Elektronik Faturalama** dönüştürmeleri, dijital imzaları ve sertifika ve yanıt işleme dahil olmak üzere harici web hizmetleriyle bağlantı için yapılandırılabilen tümleştirmeleri bir araya getirir.</span><span class="sxs-lookup"><span data-stu-id="0b6ab-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="0b6ab-109">Daha fazla bilgi için bkz. [Elektronik Faturalama](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b6ab-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="0b6ab-110">**Vergi Hesaplama** çoklu vergi kodlarını, vergi kodu belirlemeyi, vergi hesaplama tasarımcısını ve dünya çapında karmaşık vergi düzenlemelerine uymak amacıyla bir çalışma zamanı altyapısını destekleyerek gelişmiş esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="0b6ab-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="0b6ab-111">Daha fazla bilgi için bkz. [Vergi Hesaplama](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0b6ab-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="0b6ab-112">Bu genelleştirme hizmetleri, aşağıdaki Dynamics 365 çevrimiçi hizmetleriyle kullanıma hazır tümleştirme sağlar.</span><span class="sxs-lookup"><span data-stu-id="0b6ab-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="0b6ab-113">Çevrimiçi hizmet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-113">Online service</span></span> | <span data-ttu-id="0b6ab-114">DYH</span><span class="sxs-lookup"><span data-stu-id="0b6ab-114">RCS</span></span> | <span data-ttu-id="0b6ab-115">Elektronik Faturalama</span><span class="sxs-lookup"><span data-stu-id="0b6ab-115">Electronic Invoicing</span></span> | <span data-ttu-id="0b6ab-116">Vergi Hesaplama (Önizleme)</span><span class="sxs-lookup"><span data-stu-id="0b6ab-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="0b6ab-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="0b6ab-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="0b6ab-118">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-118">Yes</span></span> | <span data-ttu-id="0b6ab-119">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-119">Yes</span></span> | <span data-ttu-id="0b6ab-120">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-120">Yes</span></span> | 
| <span data-ttu-id="0b6ab-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0b6ab-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="0b6ab-122">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-122">Yes</span></span> | <span data-ttu-id="0b6ab-123">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-123">Yes</span></span> | <span data-ttu-id="0b6ab-124">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-124">Yes</span></span> | 
| <span data-ttu-id="0b6ab-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="0b6ab-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="0b6ab-126">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-126">Yes</span></span> | <span data-ttu-id="0b6ab-127">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-127">Yes</span></span> | <span data-ttu-id="0b6ab-128">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="0b6ab-128">Not applicable</span></span> | 
| <span data-ttu-id="0b6ab-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="0b6ab-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="0b6ab-130">Evet</span><span class="sxs-lookup"><span data-stu-id="0b6ab-130">Yes</span></span> | <span data-ttu-id="0b6ab-131">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="0b6ab-131">Not applicable</span></span> | <span data-ttu-id="0b6ab-132">Geçerli değil</span><span class="sxs-lookup"><span data-stu-id="0b6ab-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="0b6ab-133">Azure coğrafi konumlarının (coğrafi bölgeler) RCS için kullanılabilirliğine ilişkin farklılıklar nedeniyle, bu hizmetin yapılandırması müşteri verilerinin geçerli Dynamics 365 çevrimiçi hizmeti için seçilen coğrafi bölge dışına aktarılmasına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="0b6ab-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="0b6ab-134">Daha fazla bilgi için bkz. [Dynamics 365 ve Power Platform: Kullanılabilirlik, veri konumu, dil ve yerelleştirme](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="0b6ab-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>