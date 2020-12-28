---
title: Çift yazma kurulumu kılavuzu
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
ms.openlocfilehash: 47c07dd0e2f311b61297340a48a5a31cb1de3903
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685677"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="b0bc8-103">Çift yazma kurulumu kılavuzu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b0bc8-104">Finance and Operations ortamı ve Dataverse ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="b0bc8-105">**Finance and Operations ortamı** **Finance and Operations uygulamaları** için temel alınan platformu sağlar (örneğin, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ve Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="b0bc8-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="b0bc8-106">**Dataverse ortamı** **müşteri etkileşimi uygulamaları** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation) için temel alınan platformu sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0bc8-107">Dynamics 365 Finance'teki Human Resources modülü, çift yazma bağlantılarını desteklerken Dynamics 365 Human Resources uygulaması desteklemez.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="b0bc8-108">Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir:</span><span class="sxs-lookup"><span data-stu-id="b0bc8-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="b0bc8-109">Finance and Operations uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) ile başlar.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b0bc8-110">Microsoft Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Dataverse ortamı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="b0bc8-111">Mevcut Finance and Operations kurulumları için, çift yazma bağlantısı kurulumu Finance and Operations ortamında başlar.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="b0bc8-112">Bir varlıkta çift yazmaya başlamadan önce, hem Finance and Operations uygulamalarında hem de müşteri etkileşimi uygulamalarında varolan verileri işlemek için bir ilk eşitleme çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="b0bc8-113">İki ortam arasında veri eşitlemeniz gerekmiyorsa ilk eşitlemeyi atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="b0bc8-114">İlk eşitleme, mevcut verileri bir uygulamadan diğerine çift yönlü olarak kopyalamanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="b0bc8-115">Sahip olduğunuz ortamlara ve ortamlardaki veri türüne bağlı olarak birçok farklı kurulum senaryosu mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="b0bc8-116">Aşağıdaki kurulum senaryoları desteklenir:</span><span class="sxs-lookup"><span data-stu-id="b0bc8-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="b0bc8-117">Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="b0bc8-118">Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="b0bc8-119">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="b0bc8-120">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="b0bc8-121">Mevcut Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="b0bc8-122">Mevcut Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="b0bc8-123">Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="b0bc8-124">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b0bc8-125">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="b0bc8-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="b0bc8-126">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b0bc8-127">CRM ana çözümünün yüklendiği, müşteri etkileşimi uygulamasının yeni ve boş bir kurulumu sağlanır.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="b0bc8-128">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b0bc8-129">Tablo eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b0bc8-130">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="b0bc8-131">Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="b0bc8-132">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="b0bc8-133">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="b0bc8-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="b0bc8-134">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="b0bc8-135">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="b0bc8-136">Tablo eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="b0bc8-137">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="b0bc8-138">Mevcut Dataverse verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b0bc8-139">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b0bc8-140">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b0bc8-141">Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="b0bc8-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="b0bc8-142">Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="b0bc8-143">Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için bu konunun ilerleyen kısımlarındaki [Örnek](#example) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="b0bc8-144">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="b0bc8-145">Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının yeni örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu](#new-new)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="b0bc8-146">Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="b0bc8-147">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b0bc8-148">Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="b0bc8-149">Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="b0bc8-150">Verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="b0bc8-151">Verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile müşteri etkileşimi uygulamasının mevcut örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu](#new-existing)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="b0bc8-152">Bağlantı kurulumu tamamlandığında, verileri müşteri etkileşimi uygulamasıyla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="b0bc8-153">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="b0bc8-154">Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="b0bc8-155">Mevcut Dataverse verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="b0bc8-156">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="b0bc8-157">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="b0bc8-158">Üç harfli ISO şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="b0bc8-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="b0bc8-159">Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="b0bc8-160">Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="b0bc8-161">Mevcut Finance and Operations uygulaması kurulumu ve yeni müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="b0bc8-162">Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının yeni kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="b0bc8-163">[Finance and Operations uygulamasından bağlantıyı ayarlayın](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="b0bc8-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="b0bc8-164">Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="b0bc8-165">Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="b0bc8-166">Mevcut Finance and Operations uygulaması kurulumu ve mevcut müşteri etkileşimi uygulaması kurulumu</span><span class="sxs-lookup"><span data-stu-id="b0bc8-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="b0bc8-167">Finance and Operations uygulamasının mevcut kurulumu ile müşteri etkileşimi uygulamasının mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="b0bc8-168">[Finance and Operations uygulamasından bağlantıyı ayarlayın](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="b0bc8-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="b0bc8-169">Mevcut Dataverse verilerini Finance and Operations uygulamasıyla eşitlemek için, üç harfli ISO şirket kodunu kullanarak Dataverse verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="b0bc8-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="b0bc8-170">Verilerini eşitlemek istediğiniz tablolar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="b0bc8-171">Bir örnek ve alternatif yaklaşım ile ilgili bağlantılar için [Örnek](#example) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="b0bc8-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="b0bc8-172">Örnek</span><span class="sxs-lookup"><span data-stu-id="b0bc8-172">Example</span></span>

<span data-ttu-id="b0bc8-173">Örneğin, bkz. [Müşterileri Etkinleştirme V3 - İlgili kişiler tablo eşlemesi](enable-entity-map.md#enable-table-map)</span><span class="sxs-lookup"><span data-stu-id="b0bc8-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="b0bc8-174">İlk eşitlemeyi çalıştırması gereken her bir varlıktaki veri birimlerine dayalı alternatif bir yaklaşım için bkz. [İlk eşitleme için dikkat edilecek hususlar](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="b0bc8-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
