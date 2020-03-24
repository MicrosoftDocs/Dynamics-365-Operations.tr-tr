---
title: Çift yazma kurulumu için desteklenen senaryolar
description: Bu konu, çift yazma kurulumu için desteklenen senaryoları açıklamaktadır.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 1319f1228b635e207754f7c2516cb2b5353a9edd
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112535"
---
# <a name="supported-scenarios-for-dual-write-setup"></a><span data-ttu-id="e230f-103">Çift yazma kurulumu için desteklenen senaryolar</span><span class="sxs-lookup"><span data-stu-id="e230f-103">Supported scenarios for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e230f-104">Finance and Operations ortamı ve Common Data Service ortamı arasında çift yazma bağlantısı ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e230f-104">You can set up a dual-write connection between a Finance and Operations environment and a Common Data Service environment.</span></span>

+ <span data-ttu-id="e230f-105">**Finance and Operations ortamı** **Finance and Operations uygulamaları** için temel alınan platformu sağlar (örneğin, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail ve Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="e230f-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Retail, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="e230f-106">**Common Data Service ortamı** **Dynamics 365'teki model yönetimli uygulamalar** için temel alınan platformu sağlar (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ve Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="e230f-106">A **Common Data Service environment** provides the underlying platform for **model-driven apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

<span data-ttu-id="e230f-107">Kurulum mekanizması aboneliğinize ve ortamınıza göre değişir.</span><span class="sxs-lookup"><span data-stu-id="e230f-107">The setup mechanism varies, depending on your subscription and the environment.</span></span>

+ <span data-ttu-id="e230f-108">Finance and Operations uygulamaların yeni kurulumları için, çift yazma bağlantısı kurulumu Microsoft Dynamics Lifecycle Services'ta (LCS) ile başlar.</span><span class="sxs-lookup"><span data-stu-id="e230f-108">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e230f-109">Microsoft Power Platform lisansına sahipseniz, kiracınızın ortamı yoksa yeni bir Common Data Service ortamı alırsınız.</span><span class="sxs-lookup"><span data-stu-id="e230f-109">If you have a license for Microsoft Power Platform, you will get a new Common Data Service environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="e230f-110">Mevcut Finance and Operations kurulumları için, çift yazma bağlantısı kurulumu Finance and Operations ortamında başlar.</span><span class="sxs-lookup"><span data-stu-id="e230f-110">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="e230f-111">Aşağıdaki kurulum senaryoları desteklenir:</span><span class="sxs-lookup"><span data-stu-id="e230f-111">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="e230f-112">Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-112">A new Finance and Operations app instance and a new model-driven app instance</span></span>](#new-new)
+ [<span data-ttu-id="e230f-113">Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-113">A new Finance and Operations app instance and an existing model-driven app instance</span></span>](#new-existing)
+ [<span data-ttu-id="e230f-114">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-114">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>](#new-demo-new)
+ [<span data-ttu-id="e230f-115">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-115">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>](#new-demo-existing)
+ [<span data-ttu-id="e230f-116">Mevcut Finance and Operations uygulaması kurulumu ve yeni veya mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-116">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a><span data-ttu-id="e230f-117">Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-117">A new Finance and Operations app instance and a new model-driven app instance</span></span>

<span data-ttu-id="e230f-118">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365'teki model yönetimli uygulamanın yeni bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-118">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="e230f-119">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="e230f-119">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="e230f-120">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="e230f-120">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="e230f-121">CRM ana çözümünün yüklendiği, model yönetimli uygulamanın yeni ve boş bir örneğini sağlanır.</span><span class="sxs-lookup"><span data-stu-id="e230f-121">A new, empty instance of a model-driven app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="e230f-122">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="e230f-122">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="e230f-123">Varlık eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e230f-123">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="e230f-124">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="e230f-124">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a><span data-ttu-id="e230f-125">Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-125">A new Finance and Operations app instance and an existing model-driven app instance</span></span>

<span data-ttu-id="e230f-126">Veri içermeyen yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365'teki model yönetimli uygulamanın mevcut bir kurulumu arasında çift yazma bağlantısı kurmak için, [Lifecycle Services'tan çift yazma kurulumu](lcs-setup.md) bölümündeki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-126">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a model-driven app in Dynamics 365, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="e230f-127">Bağlantı kurulumu tamamlandığında, aşağıdaki eylemler otomatik olarak gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="e230f-127">When the connection setup is completed, the following actions occur automatically:</span></span>

- <span data-ttu-id="e230f-128">Yeni, boş bir Finance and Operations ortamı sağlanır.</span><span class="sxs-lookup"><span data-stu-id="e230f-128">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="e230f-129">DAT şirket verileri içinçift yazma bağlantısı kurulur.</span><span class="sxs-lookup"><span data-stu-id="e230f-129">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="e230f-130">Varlık eşlemeleri canlı eşitleme için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e230f-130">Entity maps are enabled for live synchronization.</span></span>

<span data-ttu-id="e230f-131">Bu durumda, her iki ortam da canlı veri eşitlemesi için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="e230f-131">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="e230f-132">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-132">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="e230f-133">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e230f-133">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="e230f-134">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-134">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="e230f-135">Üç harfli Uluslararası Standartlaştırma Kuruluşu (ISO) şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="e230f-135">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>

<span data-ttu-id="e230f-136">Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="e230f-136">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a><span data-ttu-id="e230f-137">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-137">A new Finance and Operations app instance that has demo data and a new model-driven app instance</span></span>

<span data-ttu-id="e230f-138">Demo verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365 model yönetimli uygulamanın yeni örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve yeni model yönetimli uygulama kurulumu](#new-new)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="e230f-138">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and a new instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and a new model-driven app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="e230f-139">Bağlantı kurulumu tamamlandığında, demo verilerini model yönetimli uygulamayla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-139">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="e230f-140">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="e230f-140">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="e230f-141">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e230f-141">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a><span data-ttu-id="e230f-142">Demo verilere sahip yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-142">A new Finance and Operations app instance that has demo data and an existing model-driven app instance</span></span>

<span data-ttu-id="e230f-143">Demo verilere sahip yeni bir Finance and Operations uygulaması kurulumu ile Dynamics 365 model yönetimli uygulamanın mevcut örneği arasında çift yazma bağlantısı kurmak için, bu konunun önceki bölümlerinde yer alan [Yeni Finance and Operations uygulaması kurulumu ve mevcut model yönetimli uygulama kurulumu](#new-existing)'ndaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="e230f-143">To set up a dual-write connection between a new instance of a Finance and Operations app that has demo data and an existing instance of a model-driven app in Dynamics 365, follow the steps in the [A new Finance and Operations app instance and an existing model-driven app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="e230f-144">Bağlantı kurulumu tamamlandığında, demo verilerini model yönetimli uygulamayla eşitlemek istiyorsanız, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-144">When the connection setup is completed, if you want to sync the demo data to the model-driven app, follow these steps.</span></span>

1. <span data-ttu-id="e230f-145">Finance and Operations uygulamasını LCS sayfasından açın, oturum açın ve sonra **Veri Yönetimi \> Çift yazma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="e230f-145">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="e230f-146">Verilerini eşitlemek istediğiniz varlıklar için **İlk eşitleme** işlevini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e230f-146">Run the **Initial sync** functionality for the entities that you want to sync data for.</span></span>

<span data-ttu-id="e230f-147">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-147">To sync the existing Common Data Service data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="e230f-148">Finance and Operations uygulamasında yeni bir şirket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e230f-148">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="e230f-149">Şirketi çift yazma bağlantı kurulumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e230f-149">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="e230f-150">Üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="e230f-150">[Bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="e230f-151">Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="e230f-151">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="e230f-152">Mevcut Finance and Operations uygulaması kurulumu ve yeni veya mevcut model yönetimli uygulama kurulumu</span><span class="sxs-lookup"><span data-stu-id="e230f-152">An existing Finance and Operations app instance and a new or existing model-driven app instance</span></span>

<span data-ttu-id="e230f-153">Finance and Operations uygulamasının mevcut kurulumu ile Dynamics 365 model yönetimli uygulamasının yeni veya mevcut kurulumu arasında çift yazma bağlantısı kurulumu Finance and Operations ortamında gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="e230f-153">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new or existing instance of a model-driven app in Dynamics 365 occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="e230f-154">Finance and Operations uygulamasından bağlantıyı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e230f-154">Set up the connection from the Finance and Operations app.</span></span>
2. <span data-ttu-id="e230f-155">Mevcut Common Data Service verilerini Finance and Operations uygulamasıyla eşitlemek için, üç harfli ISO şirket kodunu kullanarak Common Data Service verilerini [önyükleyin](bootstrap-company-data.md).</span><span class="sxs-lookup"><span data-stu-id="e230f-155">To sync the existing Common Data Service data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Common Data Service data by using a three-letter ISO company code.</span></span>

<span data-ttu-id="e230f-156">Çift yazma canlı eşitleme modunda olduğundan, Common Data Service'taki veriler otomatik olarak Finance and Operations uygulamasına akmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="e230f-156">Because dual-write is in live synchronization mode, the data from Common Data Service automatically starts to flow to the Finance and Operations app.</span></span>
