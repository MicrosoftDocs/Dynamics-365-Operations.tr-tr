---
title: Çift yazma kurulumu için desteklenen senaryolar
description: Bu konu, çift yazma kurulumu için desteklenen senaryoları açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706264"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="00858-103">Çift yazma kurulumu için desteklenen senaryolar</span><span class="sxs-lookup"><span data-stu-id="00858-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="00858-104">Finance and Operations ortamı ve Common Data Service ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="00858-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="00858-105">**Finance and Operations ortamı**, **Finance and Operations uygulamalarının** (ör. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management ve Dynamics 365 Retail) temelindeki platformu sağlar.</span><span class="sxs-lookup"><span data-stu-id="00858-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, and Dynamics 365 Retail).</span></span>
+ <span data-ttu-id="00858-106">**Common Data Service ortamı** **Dynamics 365'teki model yönetimli uygulamalar** için temel alınan platformu sağlar (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="00858-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

>[!IMPORTANT]
><span data-ttu-id="00858-107">Finance and Operations'taki Human Resources, çift yazma bağlantılarını desteklerken Dynamics 365 Human Resources uygulaması desteklemez.</span><span class="sxs-lookup"><span data-stu-id="00858-107">Human Resources in Finance and Operations supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="00858-108">Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir.</span><span class="sxs-lookup"><span data-stu-id="00858-108">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="00858-109">Finance and Operations uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) ile başlar.</span><span class="sxs-lookup"><span data-stu-id="00858-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="00858-110">Microsoft Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Common Data Service ortamı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="00858-110">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="00858-111">Mevcut Finance and Operations kurulumları için, çift yazma bağlantısı kurulumu Finance and Operations ortamında başlar.</span><span class="sxs-lookup"><span data-stu-id="00858-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="00858-112">Aşağıdaki kurulum senaryoları desteklenir:</span><span class="sxs-lookup"><span data-stu-id="00858-112">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="00858-113">Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-113">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="00858-114">Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-114">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="00858-115">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-115">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="00858-116">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-116">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="00858-117">Mevcut Finance and Operations uygulaması kurulumu ve yeni veya mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-117">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="00858-118">Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-118">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="00858-119">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365'teki model yönetimli uygulamanın yeni bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-119">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="00858-120">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="00858-120">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="00858-121">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="00858-121">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="00858-122">CRM ana çözümünün yüklendiği, model yönetimli uygulamanın yeni ve boş bir örneğini sağlanır.</span><span class="sxs-lookup"><span data-stu-id="00858-122">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="00858-123">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="00858-123">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="00858-124">Varlık eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="00858-124">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="00858-125">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="00858-125">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="00858-126">Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-126">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="00858-127">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365'teki model yönetimli uygulamanın mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-127">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="00858-128">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="00858-128">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="00858-129">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="00858-129">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="00858-130">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="00858-130">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="00858-131">Varlık eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="00858-131">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="00858-132">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="00858-132">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="00858-133">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-133">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="00858-134">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00858-134">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="00858-135">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-135">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="00858-136">Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="00858-136">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="00858-137">Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="00858-137">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="00858-138">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-138">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="00858-139">Demo verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365 model yönetimli uygulamanın yeni örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu](#new-new)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="00858-139">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="00858-140">Bağlantı kurulumu tamamlandığında, demo verilerini model yönetimli uygulamayla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-140">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="00858-141">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="00858-141">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="00858-142">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="00858-142">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="00858-143">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-143">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="00858-144">Demo verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365 model yönetimli uygulamanın mevcut örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu](#new-existing)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="00858-144">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="00858-145">Bağlantı kurulumu tamamlandığında, demo verilerini model yönetimli uygulamayla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-145">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="00858-146">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="00858-146">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="00858-147">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="00858-147">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="00858-148">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-148">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="00858-149">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="00858-149">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="00858-150">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="00858-150">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="00858-151">Üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="00858-151">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="00858-152">Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="00858-152">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="00858-153">Mevcut Finance and Operations uygulaması kurulumu ve yeni veya mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="00858-153">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="00858-154">Finance and Operations uygulamasının mevcut kurulumu ile Dynamics 365 model yönetimli uygulamasının yeni veya mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="00858-154">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="00858-155">Finance and Operations uygulamasından bağlantıyı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="00858-155">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="00858-156">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için, üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="00858-156">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="00858-157">Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="00858-157">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
