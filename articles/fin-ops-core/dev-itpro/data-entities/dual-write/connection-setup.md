---
title: Çift yazmayı ayarlama kılavuzu
description: Bu konu, çift yazma kurulumu için desteklenen senaryoları açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088518"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a><span data-ttu-id="b31f6-103">Çift yazmayı ayarlama kılavuzu</span><span class="sxs-lookup"><span data-stu-id="b31f6-103">Guidance for how to set up dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b31f6-104">Finance and Operations ortamı ve Common Data Service ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b31f6-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="b31f6-105">**Finance and Operations ortamı** , **Finance and Operations uygulamalarının** (ör. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management ve Dynamics 365 Retail) temelindeki platformu sağlar.</span><span class="sxs-lookup"><span data-stu-id="b31f6-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="b31f6-106">**Common Data Service ortamı** **müşteri etkileşimi uygulamaları** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation) için temel alınan platformu sağlar.</span><span class="sxs-lookup"><span data-stu-id="b31f6-106">A **Common Data Service environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="b31f6-107">Finance and Operations'taki Human Resources, çift yazma bağlantılarını desteklerken Dynamics 365 Human Resources uygulaması desteklemez.</span><span class="sxs-lookup"><span data-stu-id="b31f6-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="b31f6-108">Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir.</span><span class="sxs-lookup"><span data-stu-id="b31f6-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="b31f6-109">Finance and Operations uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) ile başlar.</span><span class="sxs-lookup"><span data-stu-id="b31f6-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b31f6-110">Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Common Data Service ortamı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="b31f6-110">If you have a license for Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="b31f6-111">Mevcut Finance and Operations kurulumları için, çift yazma bağlantısı kurulumu Finance and Operations ortamında başlar.</span><span class="sxs-lookup"><span data-stu-id="b31f6-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="b31f6-112">Bir varlıkta çift yazmaya başlamadan önce, Finance and Operations uygulamaların ve müşteri etkileşimi uygulamalarının her iki tarafında varolan verileri işlemek için bir başlangıç eşitlemesi çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b31f6-112">Before you start dual-write on an entity, you can run an initial sync to handle existing data on both sides of Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="b31f6-113">İki ortam arasında veri eşitlemeniz gerekmiyorsa, ilk eşitlemeyi atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b31f6-113">You can skip the initial sync if you don't need to synchronize data between the two environments.</span></span>

<span data-ttu-id="b31f6-114">İlk eşitleme, varolan verileri bir uygulamadan diğerine çift yönlü olarak kopyalamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="b31f6-114">An initial sync lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="b31f6-115">Sahip olduğunuz ortamlara ve ortamlardaki veri türüne bağlı olarak birçok farklı kurulum senaryosu vardır.</span><span class="sxs-lookup"><span data-stu-id="b31f6-115">There are several different setup scenarios depending on which environments you already have and what type of data is in the environments.</span></span>

<span data-ttu-id="b31f6-116">Aşağıdaki kurulum senaryoları desteklenir:</span><span class="sxs-lookup"><span data-stu-id="b31f6-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="b31f6-117">Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="b31f6-118">Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="b31f6-119">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="b31f6-120">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="b31f6-121">Mevcut Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="b31f6-122">Mevcut Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="b31f6-123">Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="b31f6-124">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b31f6-125">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="b31f6-125">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="b31f6-126">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="b31f6-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b31f6-127">CRM ana çözümünün yüklendiği, müşteri etkileşimi uygulamasının yeni ve boş bir kurulumu sağlanır.</span><span class="sxs-lookup"><span data-stu-id="b31f6-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="b31f6-128">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="b31f6-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b31f6-129">Varlık eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b31f6-129">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b31f6-130">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="b31f6-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="b31f6-131">Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="b31f6-132">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b31f6-133">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="b31f6-133">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="b31f6-134">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="b31f6-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b31f6-135">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="b31f6-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b31f6-136">Varlık eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b31f6-136">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b31f6-137">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="b31f6-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="b31f6-138">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-138">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b31f6-139">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b31f6-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b31f6-140">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b31f6-141">Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="b31f6-141">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="b31f6-142">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b31f6-143">Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).</span><span class="sxs-lookup"><span data-stu-id="b31f6-143">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="b31f6-144">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="b31f6-145">Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-new)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="b31f6-146">Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="b31f6-147">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma** 'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b31f6-148">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-148">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b31f6-149">Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).</span><span class="sxs-lookup"><span data-stu-id="b31f6-149">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="b31f6-150">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="b31f6-151">Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-existing)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="b31f6-152">Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="b31f6-153">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma** 'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b31f6-154">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-154">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b31f6-155">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-155">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b31f6-156">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b31f6-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b31f6-157">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b31f6-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b31f6-158">Üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="b31f6-158">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="b31f6-159">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-159">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b31f6-160">Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).</span><span class="sxs-lookup"><span data-stu-id="b31f6-160">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="b31f6-161">Mevcut Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="b31f6-162">Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının yeni kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="b31f6-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="b31f6-163">[Finance and Operations uygulamasından bağlantıyı ayarlayın](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="b31f6-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="b31f6-164">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-164">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b31f6-165">Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).</span><span class="sxs-lookup"><span data-stu-id="b31f6-165">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="b31f6-166">Mevcut Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b31f6-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="b31f6-167">Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="b31f6-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app  occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="b31f6-168">Finance and Operations uygulamasından bağlantıyı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-168">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="b31f6-169">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için, üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="b31f6-169">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="b31f6-170">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b31f6-170">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="b31f6-171">Bir örnek ve alternatif yaklaşım için bkz. [Örnek](#example).</span><span class="sxs-lookup"><span data-stu-id="b31f6-171">For an example and alternative approach, see [Example](#example).</span></span>

## <a name="example"></a><span data-ttu-id="b31f6-172">Örnek</span><span class="sxs-lookup"><span data-stu-id="b31f6-172">Example</span></span>

<span data-ttu-id="b31f6-173">Örneğin, bkz. [Müşterileri Etkinleştirme V3 — İlgili kişiler varlık haritası](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span><span class="sxs-lookup"><span data-stu-id="b31f6-173">For an example, see [Enabling the Customers V3—Contacts entity map](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)</span></span>

<span data-ttu-id="b31f6-174">İlk eşitlemeyi çalıştırması gereken her bir varlıktaki veri birimlerine dayalı alternatif bir yaklaşım için, bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="b31f6-174">For an alternative approach based on data volumes in each entity that need to run initial sync, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
