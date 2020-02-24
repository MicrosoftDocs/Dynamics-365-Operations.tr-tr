---
title: Kanallara genel bakış
description: Bu konu, Microsoft Dynamics 365 Commerce'teki kanallar hakkında genel bilgi vermektedir.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002370"
---
# <a name="channels-overview"></a><span data-ttu-id="bc1cb-103">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="bc1cb-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bc1cb-104">Bu konu, Microsoft Dynamics 365 Commerce'teki kanallar hakkında genel bilgi vermektedir.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="bc1cb-105">Makalede, her bir kanalı ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="bc1cb-106">Kanal Türleri</span><span class="sxs-lookup"><span data-stu-id="bc1cb-106">Types of Channels</span></span>

<span data-ttu-id="bc1cb-107">Dynamics 365 Commerce üç farklı kanal türünü destekler: perakende, çağrı merkezi ve çevrimiçi kanallar.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="bc1cb-108">Perakende kanalları</span><span class="sxs-lookup"><span data-stu-id="bc1cb-108">Retail channels</span></span>

<span data-ttu-id="bc1cb-109">Perakende kanalları geleneksel mağazaları temsil eder.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="bc1cb-110">Her mağazanın kendi satış noktası (POS) kasaları, gelir ve gider hesapları ve personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="bc1cb-111">Çağrı merkezi kanalları</span><span class="sxs-lookup"><span data-stu-id="bc1cb-111">Call center channels</span></span>

<span data-ttu-id="bc1cb-112">Çağrı merkezi kanalları, çağrı merkezi sipariş ve müşteri yönetimini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="bc1cb-113">Çevrimiçi kanallar</span><span class="sxs-lookup"><span data-stu-id="bc1cb-113">Online channels</span></span>

<span data-ttu-id="bc1cb-114">Çevrimiçi kanallar, çevrimiçi e-ticaret mağazalarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="bc1cb-115">Çevrimiçi kanal oluşturulduktan sonra, Microsoft Dynamics 365 Commerce Site Builder aracı veya başka bir üçüncü taraf e-ticaret çözümü kullanılarak bir site oluşturulması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="bc1cb-116">Kanal kurulumu hakkında temel bilgiler</span><span class="sxs-lookup"><span data-stu-id="bc1cb-116">Channel setup basics</span></span>

<span data-ttu-id="bc1cb-117">Kanal kurulumu Commerce aracında yapılır.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="bc1cb-118">Her kanalın kendi ödeme yöntemleri, fiyat grupları, ürün hiyerarşileri, sınıflamaları ve ürün kümeleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="bc1cb-119">Bir kanal oluşturduktan sonra, kanalı taşımasını ve satmasını istediğiniz ürünleri atarsınız.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="bc1cb-120">Her kanal türünün yapılandırmanız gerekebilecek benzersiz bir özellikler kümesi vardır.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="bc1cb-121">Örneğin, bir perakende kanalında çalışanların, kasaların ve müşterilerin atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="bc1cb-122">Yeni bir kanal oluşturulunca, bir organizasyon hiyerarşisine atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="bc1cb-123">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="bc1cb-123">Channel setup prerequisites</span></span>

<span data-ttu-id="bc1cb-124">Bir kanalı ayarlamadan önce, kanal türüne göre önkoşul olan bazı görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="bc1cb-125">Daha fazla bilgi için bkz. [Kanal kurulum önkoşulları](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="bc1cb-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="bc1cb-126">Kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-126">Set up a channel</span></span>

<span data-ttu-id="bc1cb-127">Önkoşul görevleri tamamlandıktan sonra diğer kurulum yönergeleri için aşağıdaki bağlantıları kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc1cb-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="bc1cb-128">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="bc1cb-129">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="bc1cb-130">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="bc1cb-131">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="bc1cb-131">Additional resources</span></span>

[<span data-ttu-id="bc1cb-132">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="bc1cb-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="bc1cb-133">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="bc1cb-134">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="bc1cb-135">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="bc1cb-136">Kuruluş hiyerarşilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="bc1cb-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)
