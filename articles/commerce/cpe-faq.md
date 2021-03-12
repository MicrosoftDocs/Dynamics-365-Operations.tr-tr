---
title: Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS
description: Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b8d7d7364087dacf3b4479ab008609ecffeaacb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000987"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="3ab33-103">Dynamics 365 Commerce değerlendirme ortamıyla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="3ab33-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ab33-104">Bu konu, Microsoft Dynamics 365 Commerce değerlendirme ortamı istemcisi hakkında sık sorulan soruların yanıtlarını verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3ab33-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="3ab33-105">**Commerce değerlendirme ortamı, şu anda Retail uygulayan müşteriler için bir e-Ticaret mağazası olarak kullanabilir mi?**</span><span class="sxs-lookup"><span data-stu-id="3ab33-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="3ab33-106">No</span><span class="sxs-lookup"><span data-stu-id="3ab33-106">No.</span></span> <span data-ttu-id="3ab33-107">Commerce değerlendirme ortamı yalnızca değerlendirme içindir.</span><span class="sxs-lookup"><span data-stu-id="3ab33-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="3ab33-108">Perakende satış teknolojisini kullanan bir müşteri için ortam gerekiyorsa Microsoft 'a başvurun.</span><span class="sxs-lookup"><span data-stu-id="3ab33-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="3ab33-109">**Commerce değerlendirme ortamı, Retail uygulayan mevcut bir uygulamanın/ortamın üstünde e-Ticaret özelliklerinin sağlanması için kullanılabilir mi?**</span><span class="sxs-lookup"><span data-stu-id="3ab33-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="3ab33-110">Hayır (çoğunlukla).</span><span class="sxs-lookup"><span data-stu-id="3ab33-110">No (mostly).</span></span> <span data-ttu-id="3ab33-111">Commerce değerlendirme bileşenleri, yalnızca önkoşullar ve sağlama kılavuzunda belirtilen yapılandırmalarla eşleşen ortamlar için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="3ab33-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="3ab33-112">Ek olarak, gerekli temel demo verileri 10.0.8 öncesindeki ilk sürümle dağıtılan ortamlarda kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="3ab33-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="3ab33-113">**Microsoft Dynamics Lifecycle Services (LCS) yoluyla Microsoft Azure üzerine Commerce değerlendirme ortamını dağıtmaya hangi maliyetler dahil edilecek?**</span><span class="sxs-lookup"><span data-stu-id="3ab33-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="3ab33-114">Geleneksel Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce genel merkezi demo ortamı (sanal makine \[VM\]) Azure aboneliğinizde barındırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="3ab33-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="3ab33-115">Bu maliyeti tahmin etmek için [Azure fiyatlandırma hesap makinesini](https://azure.microsoft.com/pricing/calculator/) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3ab33-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="3ab33-116">Commerce Scale Unit, Commerce Site Oluşturucu ve e-Ticaret siteniz gibi diğer bileşenler, hizmet olarak yazılım olarak kullanılacak ve Microsoft tarafından barındırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="3ab33-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="3ab33-117">**Şu anda Commerce değerlendirme ortamında hangi Azure coğrafyaları destekleniyor?**</span><span class="sxs-lookup"><span data-stu-id="3ab33-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="3ab33-118">Commerce değerlendirme ortamı yalnızca Kuzey Amerika Coğrafyasında dağıtılabilir.</span><span class="sxs-lookup"><span data-stu-id="3ab33-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="3ab33-119">**Tam OneBox sanal makinesi (VM) seçeneği olan bir indirilebilir sanal sabit disk (VHD) var mı?**</span><span class="sxs-lookup"><span data-stu-id="3ab33-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="3ab33-120">Dynamics 365 Commerce ve Commerce Scale Unit tamamen hizmet olarak yazılımdır (SaaS) ve bulutta barındırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="3ab33-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="3ab33-121">**Commerce değerlendirme ortamı ne kadar süreyle kullanılabilir?**</span><span class="sxs-lookup"><span data-stu-id="3ab33-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="3ab33-122">Commerce değerlendirme ortamının Commerce Scale Unit, Commerce site oluşturucu ve e-Ticaret gibi SaaS bileşenlerinin sağlandığı tarihten itibaren 30 günlük zaman sınırı vardır.</span><span class="sxs-lookup"><span data-stu-id="3ab33-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="3ab33-123">**Commerce değerlendirme ortamım için zaman sınırını genişletebilirim?**</span><span class="sxs-lookup"><span data-stu-id="3ab33-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="3ab33-124">Zaman sınırı genişletme norm için bir istisnadır ve duruma göre değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="3ab33-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="3ab33-125">Yardım için Microsoft iş ortağınıza başvurmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3ab33-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ab33-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="3ab33-126">Additional resources</span></span>

[<span data-ttu-id="3ab33-127">Dynamics 365 Commerce değerlendirme ortamına genel bakış</span><span class="sxs-lookup"><span data-stu-id="3ab33-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3ab33-128">Dynamics 365 Commerce değerlendirme ortamı sağlama</span><span class="sxs-lookup"><span data-stu-id="3ab33-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="3ab33-129">Dynamics 365 Commerce değerlendirme ortamı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3ab33-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3ab33-130">Dynamics 365 Commerce değerlendirme ortamında BOPIS yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3ab33-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="3ab33-131">Dynamics 365 Commerce değerlendirme ortamı için isteğe bağlı özellikleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="3ab33-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)
