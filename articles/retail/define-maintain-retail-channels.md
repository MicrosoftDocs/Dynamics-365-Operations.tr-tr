---
title: "Perakende kanallarını tanımla ve koru"
description: "Bu konuda, Microsoft Dynamics 365 for Retail perakende mağazaları olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir. Makalede, perakende mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 53ba6cdb2378ce9011c6e7e3ce4e67c789adb1e6
ms.contentlocale: tr-tr
ms.lasthandoff: 01/04/2019

---

# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="7e2b7-104">Perakende kanallarını tanımla ve koru</span><span class="sxs-lookup"><span data-stu-id="7e2b7-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e2b7-105">Bu konuda, Microsoft Dynamics 365 for Retail perakende mağazaları olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="7e2b7-106">Makalede, perakende mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="7e2b7-107">Dynamics 365 for Retail, çevrimiçi mağazalar, çağrı merkezleri ve fiziki mağazalar gibi birden fazla perakende kanalını destekler.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="7e2b7-108">Bir tuğla dibek mağazaya perakende mağaza adı verilir.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="7e2b7-109">Her perakende mağazasının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="7e2b7-110">Bir perakende mağazası oluşturmadan önce tüm bu öğeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="7e2b7-111">Perakende mağaza oluşturduktan sonra gerçekleştirmek istediğiniz ürünleri atarsınız.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="7e2b7-112">Ayrıca mağazaya çalışanlar, kasalar ve müşteriler atarsınız.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="7e2b7-113">Son olarak, yeni mağazayı bir organizasyon hiyerarşisine eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="7e2b7-114">Perakende mağazaları kurma</span><span class="sxs-lookup"><span data-stu-id="7e2b7-114">Setting up retail stores</span></span>

<span data-ttu-id="7e2b7-115">Microsoft Dynamics 365 for Retail, bir perakende mağaza kurmadan önce bazı önkoşul görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="7e2b7-116">Sonrasında perakende mağazayı oluşturabilir ve ayrıntılar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7e2b7-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7e2b7-117">Prerequisites</span></span>

<span data-ttu-id="7e2b7-118">Bir perakende mağaza kurmadan önce aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="7e2b7-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="7e2b7-119">Organizasyon yapınızı yapılandırın ve perakende sınıflamalar, stok yenileme ve raporlama için kuruluş hiyerarşilerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="7e2b7-120">Perakende mağazayı temsil eden bir ambar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="7e2b7-121">Perakende mağazalar, mağaza ekstreleri ve ekstre fişleri için numara sıraları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="7e2b7-122">Perakende için parametreleri konfigüre et.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="7e2b7-123">Mağazanın kabul ettiği ödeme yöntemleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="7e2b7-124">Perakende POS kasalarında kredi kartı işlemleri yürütmek için, ödeme hizmetleri de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="7e2b7-125">Satış vergisi gruplarını ayarla.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="7e2b7-126">Perakende ürünleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-126">Set up retail products.</span></span> <span data-ttu-id="7e2b7-127">Bu görevin bir parçası olarak, ayrıca perakende ürün hiyerarşileri, ürün çeşitleri ve ürün sınıflamaları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="7e2b7-128">Ürün fiyat gruplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-128">Set up product price groups.</span></span>
10. <span data-ttu-id="7e2b7-129">Perakende ürün fiyatlandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-129">Set up retail product pricing.</span></span> <span data-ttu-id="7e2b7-130">Bu görevin bir parçası olarak, aynı zamanda fiyat ayarlamaları, iskontolar ve iskonto dönemlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="7e2b7-131">Personeli ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e2b7-132">Perakende POS sistemi için oturum açıp Microsoft Dynamics 365 for Retail for Retail POS sistemi kullanarak görevleri yürütebilmeleri için, çalışanlara uygun izinleri de atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>

12. <span data-ttu-id="7e2b7-133">Mağazaya atamak için Perakende POS profillerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="7e2b7-134">Bu görev kayıtları ayarlamak, çevrimdışı profilleri ayarlamak ve makbuz biçimleri ve profilleri ayarlamak gibi birçok diğer görevi içerir.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="7e2b7-135">Önkoşula dahil tüm görevleri gözden geçirin ve yalnızca sizin için geçerli görevleri tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="7e2b7-136">Bir perakende mağaza kurun</span><span class="sxs-lookup"><span data-stu-id="7e2b7-136">Set up a retail store</span></span>

<span data-ttu-id="7e2b7-137">+Önkoşul görevlerini tamamladıktan sonra perakende mağaza ayrıntılarını ayarlamak için aşağıdaki görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="7e2b7-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="7e2b7-138">Bir perakende mağazası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-138">Create a retail store.</span></span>
2. <span data-ttu-id="7e2b7-139">Mağazaya bir satış vergisi grubu atayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="7e2b7-140">Çevrimiçi mağaza tarafından kabul edilen ödeme yöntemleri atayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="7e2b7-141">Perakende mağazasında sunduğunuz ürünler için ürün açıklamalarına ayrıntılar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="7e2b7-142">Örneğin, zengin metin ve resimler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="7e2b7-143">Bu ürün ayrıntıları çeşitli bağlamlarda POS kasası veya yazdırılan etiketlerde görünür.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="7e2b7-144">**Perakende sınıflama**, **Perakende stok yenileme**, veya **Perakende raporlama** amacıyla mağazayı varsayılan kuruluş hiyerarşisine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="7e2b7-145">Bir perakende mağaza kurduktan sonra</span><span class="sxs-lookup"><span data-stu-id="7e2b7-145">After you set up a retail store</span></span>

<span data-ttu-id="7e2b7-146">Perakende mağaza için ayrıntıları girdikten sonra, yeni perakende mağaza verilerini Perakende POS'una göndermek için şu görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="7e2b7-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="7e2b7-147">Mağaza için POS kasalarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="7e2b7-148">Mağazaya ürün çeşitleri atayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="7e2b7-149">Sınıflama içinde bulunan ürün listesini oluşturmak ve ürünleri perakende mağazada erişilebilir hale getirmek için sınıflamaları işleyin.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="7e2b7-150">Numara serileri, donanım profilleri ve POS ekran düzeni gibi verileri Perakende POS kasalarına gönderin.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="7e2b7-151">Perakende POS'una mağaza verisini göndermek için perakende mağazayı yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="7e2b7-152">Perakende POS'una mağaza verisini göndermek için işleri yürütün.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="7e2b7-153">Kuruluş hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="7e2b7-153">Organization hierarchies</span></span>

<span data-ttu-id="7e2b7-154">Retail, perakende kanallarını yapılandırmak için kuruluş hiyerarşilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="7e2b7-155">Organizasyon hiyerarşileri, organizasyonlar arasındaki işinizi meydana getiren ilişkileri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="7e2b7-156">Mağazalar kurduğunuzda, onları bir organizasyon hiyerarşisine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="7e2b7-157">Ardından mağazalar ürün çeşitleri, stok yenileme ve raporlama için kullanılan verileri paylaşır.</span><span class="sxs-lookup"><span data-stu-id="7e2b7-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

