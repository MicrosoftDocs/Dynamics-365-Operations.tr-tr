---
title: Perakende kanallarını tanımla ve koru
description: Bu konu, Dynamics 365 Retail'da perakende mağazaları olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir. Makalede, perakende mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
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
ms.openlocfilehash: 45d0386d215da15103a417502debb245c91f6309
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934620"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="3f469-104">Perakende kanallarını tanımla ve koru</span><span class="sxs-lookup"><span data-stu-id="3f469-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f469-105">Bu konu, Dynamics 365 Retail'da perakende mağazaları olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="3f469-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Dynamics 365 Retail.</span></span> <span data-ttu-id="3f469-106">Makalede, perakende mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="3f469-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="3f469-107">Retail çevrimiçi mağazalar, çağrı merkezleri ve fiziki mağazalar gibi birden fazla perakende kanalını destekler.</span><span class="sxs-lookup"><span data-stu-id="3f469-107">Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="3f469-108">Bir tuğla dibek mağazaya perakende mağaza adı verilir.</span><span class="sxs-lookup"><span data-stu-id="3f469-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="3f469-109">Her perakende mağazasının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="3f469-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="3f469-110">Bir perakende mağazası oluşturmadan önce tüm bu öğeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f469-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="3f469-111">Perakende mağaza oluşturduktan sonra gerçekleştirmek istediğiniz ürünleri atarsınız.</span><span class="sxs-lookup"><span data-stu-id="3f469-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="3f469-112">Ayrıca mağazaya çalışanlar, kasalar ve müşteriler atarsınız.</span><span class="sxs-lookup"><span data-stu-id="3f469-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="3f469-113">Son olarak, yeni mağazayı bir organizasyon hiyerarşisine eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="3f469-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="3f469-114">Perakende mağazaları kurma</span><span class="sxs-lookup"><span data-stu-id="3f469-114">Setting up retail stores</span></span>

<span data-ttu-id="3f469-115">Retail'de bir perakende mağaza kurmadan önce bazı önkoşul görevlerini tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f469-115">Before you can set up a retail store in Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="3f469-116">Sonrasında perakende mağazayı oluşturabilir ve ayrıntılar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f469-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3f469-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="3f469-117">Prerequisites</span></span>

<span data-ttu-id="3f469-118">Bir perakende mağaza kurmadan önce aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="3f469-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="3f469-119">Organizasyon yapınızı yapılandırın ve perakende sınıflamalar, stok yenileme ve raporlama için kuruluş hiyerarşilerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="3f469-120">Perakende mağazayı temsil eden bir ambar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="3f469-121">Perakende mağazalar, mağaza ekstreleri ve ekstre fişleri için numara sıraları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="3f469-122">Perakende için parametreleri konfigüre et.</span><span class="sxs-lookup"><span data-stu-id="3f469-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="3f469-123">Mağazanın kabul ettiği ödeme yöntemleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="3f469-124">Perakende POS kasalarında kredi kartı işlemleri yürütmek için, ödeme hizmetleri de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f469-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="3f469-125">Satış vergisi gruplarını ayarla.</span><span class="sxs-lookup"><span data-stu-id="3f469-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="3f469-126">Perakende ürünleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-126">Set up retail products.</span></span> <span data-ttu-id="3f469-127">Bu görevin bir parçası olarak, ayrıca perakende ürün hiyerarşileri, ürün çeşitleri ve ürün sınıflamaları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="3f469-128">Ürün fiyat gruplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-128">Set up product price groups.</span></span>
10. <span data-ttu-id="3f469-129">Perakende ürün fiyatlandırmasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-129">Set up retail product pricing.</span></span> <span data-ttu-id="3f469-130">Bu görevin bir parçası olarak, aynı zamanda fiyat ayarlamaları, iskontolar ve iskonto dönemlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="3f469-131">Personeli ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f469-132">Retail POS sistemini kullanarak görevleri yürütebilmeleri için, çalışanlara uygun izinleri de atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f469-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Retail POS system.</span></span>

12. <span data-ttu-id="3f469-133">Mağazaya atamak için Perakende POS profillerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3f469-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="3f469-134">Bu görev kayıtları ayarlamak, çevrimdışı profilleri ayarlamak ve makbuz biçimleri ve profilleri ayarlamak gibi birçok diğer görevi içerir.</span><span class="sxs-lookup"><span data-stu-id="3f469-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="3f469-135">Önkoşula dahil tüm görevleri gözden geçirin ve yalnızca sizin için geçerli görevleri tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="3f469-136">Bir perakende mağaza kurun</span><span class="sxs-lookup"><span data-stu-id="3f469-136">Set up a retail store</span></span>

<span data-ttu-id="3f469-137">+Önkoşul görevlerini tamamladıktan sonra perakende mağaza ayrıntılarını ayarlamak için aşağıdaki görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="3f469-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="3f469-138">Bir perakende mağazası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3f469-138">Create a retail store.</span></span>
2. <span data-ttu-id="3f469-139">Mağazaya bir satış vergisi grubu atayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="3f469-140">Çevrimiçi mağaza tarafından kabul edilen ödeme yöntemleri atayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="3f469-141">Perakende mağazasında sunduğunuz ürünler için ürün açıklamalarına ayrıntılar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3f469-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="3f469-142">Örneğin, zengin metin ve resimler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f469-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="3f469-143">Bu ürün ayrıntıları çeşitli bağlamlarda POS kasası veya yazdırılan etiketlerde görünür.</span><span class="sxs-lookup"><span data-stu-id="3f469-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="3f469-144">**Perakende sınıflama**, **Perakende stok yenileme**, veya **Perakende raporlama** amacıyla mağazayı varsayılan kuruluş hiyerarşisine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="3f469-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="3f469-145">Bir perakende mağaza kurduktan sonra</span><span class="sxs-lookup"><span data-stu-id="3f469-145">After you set up a retail store</span></span>

<span data-ttu-id="3f469-146">Perakende mağaza için ayrıntıları girdikten sonra, yeni perakende mağaza verilerini Perakende POS'una göndermek için şu görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="3f469-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="3f469-147">Mağaza için POS kasalarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="3f469-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="3f469-148">Mağazaya ürün çeşitleri atayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="3f469-149">Sınıflama içinde bulunan ürün listesini oluşturmak ve ürünleri perakende mağazada erişilebilir hale getirmek için sınıflamaları işleyin.</span><span class="sxs-lookup"><span data-stu-id="3f469-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="3f469-150">Numara serileri, donanım profilleri ve POS ekran düzeni gibi verileri Perakende POS kasalarına gönderin.</span><span class="sxs-lookup"><span data-stu-id="3f469-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="3f469-151">Perakende POS'una mağaza verisini göndermek için perakende mağazayı yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="3f469-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="3f469-152">Perakende POS'una mağaza verisini göndermek için işleri yürütün.</span><span class="sxs-lookup"><span data-stu-id="3f469-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="3f469-153">Kuruluş hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="3f469-153">Organization hierarchies</span></span>

<span data-ttu-id="3f469-154">Retail, perakende kanallarını yapılandırmak için kuruluş hiyerarşilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3f469-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="3f469-155">Organizasyon hiyerarşileri, organizasyonlar arasındaki işinizi meydana getiren ilişkileri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3f469-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="3f469-156">Mağazalar kurduğunuzda, onları bir organizasyon hiyerarşisine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f469-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="3f469-157">Ardından mağazalar ürün çeşitleri, stok yenileme ve raporlama için kullanılan verileri paylaşır.</span><span class="sxs-lookup"><span data-stu-id="3f469-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="3f469-158">Perakende satış işlevlerini kullanabilmeniz için **çoklu sevk edilecek** konfigürasyon anahtarının etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f469-158">To use Retail sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="3f469-159">Bu konfigürasyon anahtarı, **Sistem yönetimi** \> **Kurulum** \> **Lisans konfigürasyonu** altındaki **ticaret konfigürasyon** anahtarlarında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="3f469-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="3f469-160">Bu, satış siparişi satırı düzeyinde konfigüre edilen teslimat adresine dayalı olarak çeşitli doğrulamaları gerçekleştiren perakende işlevselliğe bağlı olarak gereklidir.</span><span class="sxs-lookup"><span data-stu-id="3f469-160">This is required due to Retail functionality that performs various validations based on the delivery address configured at the sales order line level.</span></span>
