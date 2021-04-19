---
title: Perakende kanallarını tanımla ve koru
description: Bu konu, Dynamics 365 Commerce'da mağazalar olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir. Makalede, mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.
author: mugunthanm
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7a2db169adafa1b8a0113024f3f58522c2cee6d2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802033"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="5844d-104">Perakende kanallarını tanımlama ve koruma</span><span class="sxs-lookup"><span data-stu-id="5844d-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5844d-105">Bu konu, Dynamics 365 Commerce'da mağazalar olarak adlandırılan geleneksel mağazaları ayarlama işlemine genel bakış verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="5844d-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5844d-106">Makalede, mağaza ayarlamanızdan önce ve sonra tamamlamanız gereken görevleri hakkında bilgiler yer almaktadır.</span><span class="sxs-lookup"><span data-stu-id="5844d-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="5844d-107">Commerce, çevrimiçi mağazalar, çağrı merkezleri ve fiziki mağazalar gibi birden fazla kanalı destekler.</span><span class="sxs-lookup"><span data-stu-id="5844d-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="5844d-108">Geleneksel bir mağazaya mağaza adı verilir.</span><span class="sxs-lookup"><span data-stu-id="5844d-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="5844d-109">Her mağazanın kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir.</span><span class="sxs-lookup"><span data-stu-id="5844d-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="5844d-110">Bir mağaza oluşturmadan önce tüm bu öğeleri ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5844d-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="5844d-111">Mağaza oluşturduktan sonra gerçekleştirmek istediğiniz ürünleri atarsınız.</span><span class="sxs-lookup"><span data-stu-id="5844d-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="5844d-112">Ayrıca mağazaya çalışanlar, kasalar ve müşteriler atarsınız.</span><span class="sxs-lookup"><span data-stu-id="5844d-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="5844d-113">Son olarak, yeni mağazayı bir organizasyon hiyerarşisine eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="5844d-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="5844d-114">Mağazaları ayarlama</span><span class="sxs-lookup"><span data-stu-id="5844d-114">Setting up stores</span></span>

<span data-ttu-id="5844d-115">Commerce'te bir perakende mağaza kurmadan önce bazı önkoşul görevleri tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5844d-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="5844d-116">Bundan sonra mağazayı oluşturabilir ve ayrıntılar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5844d-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="5844d-117">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="5844d-117">Prerequisites</span></span>

<span data-ttu-id="5844d-118">Bir mağaza kurmadan önce aşağıdaki görevleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="5844d-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="5844d-119">Organizasyon yapınızı yapılandırın ve perakende sınıflamalar, stok yenileme ve raporlama için kuruluş hiyerarşilerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="5844d-120">Mağazayı temsil eden bir ambar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="5844d-121">Mağazalar, mağaza ekstreleri ve ekstre fişleri için numara sıraları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="5844d-122">Commerce için parametreleri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5844d-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="5844d-123">Mağazanın kabul ettiği ödeme yöntemleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="5844d-124">POS kasalarında kredi kartı işlemleri yürütmek için, ödeme hizmetleri de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5844d-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="5844d-125">Satış vergisi gruplarını ayarla.</span><span class="sxs-lookup"><span data-stu-id="5844d-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="5844d-126">Ürünlerini ayarlayn.</span><span class="sxs-lookup"><span data-stu-id="5844d-126">Set up products.</span></span> <span data-ttu-id="5844d-127">Bu görevin bir parçası olarak, ayrıca ürün hiyerarşileri, ürün çeşitleri ve ürün sınıflamaları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="5844d-128">Ürün fiyat gruplarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-128">Set up product price groups.</span></span>
10. <span data-ttu-id="5844d-129">Ürün fiyatlandırmalarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-129">Set up product pricing.</span></span> <span data-ttu-id="5844d-130">Bu görevin bir parçası olarak, aynı zamanda fiyat ayarlamaları, iskontolar ve iskonto dönemlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="5844d-131">Personeli ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5844d-132">POS sistemini kullanarak görevleri yürütebilmeleri için, çalışanlara uygun izinleri de atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5844d-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="5844d-133">Mağazaya atanacak POS profillerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5844d-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="5844d-134">Bu görev kayıtları ayarlamak, çevrimdışı profilleri ayarlamak ve makbuz biçimleri ve profilleri ayarlamak gibi birçok diğer görevi içerir.</span><span class="sxs-lookup"><span data-stu-id="5844d-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="5844d-135">Önkoşullara dahil edilen tüm görevleri gözden geçirin ve yalnızca sizin için geçerli görevleri tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="5844d-136">Mağaza ayarlama</span><span class="sxs-lookup"><span data-stu-id="5844d-136">Set up a store</span></span>

<span data-ttu-id="5844d-137">Önkoşul görevlerini tamamladıktan sonra mağaza ayrıntılarını ayarlamak için aşağıdaki görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="5844d-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="5844d-138">Bir mağaza oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5844d-138">Create a store.</span></span>
2. <span data-ttu-id="5844d-139">Mağazaya bir satış vergisi grubu atayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="5844d-140">Çevrimiçi mağaza tarafından kabul edilen ödeme yöntemleri atayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="5844d-141">Mağazada sunduğunuz ürünler için ürün açıklamalarına ayrıntılar ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5844d-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="5844d-142">Örneğin, zengin metin ve resimler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5844d-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="5844d-143">Bu ürün ayrıntıları çeşitli bağlamlarda POS kasası veya yazdırılan etiketlerde görünür.</span><span class="sxs-lookup"><span data-stu-id="5844d-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="5844d-144">**Perakende sınıflama**, **Perakende stok yenileme**, veya **Perakende raporlama** amacıyla mağazayı varsayılan kuruluş hiyerarşisine ekleyin.</span><span class="sxs-lookup"><span data-stu-id="5844d-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="5844d-145">Mağaza kurduktan sonra</span><span class="sxs-lookup"><span data-stu-id="5844d-145">After you set up a store</span></span>

<span data-ttu-id="5844d-146">Mağaza için ayrıntıları girdikten sonra, yeni mağaza verilerini POS'a göndermek için şu görevleri tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="5844d-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="5844d-147">Mağaza için POS kasalarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="5844d-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="5844d-148">Mağazaya ürün çeşitleri atayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="5844d-149">Sınıflama içinde bulunan ürün listesini oluşturmak ve ürünleri mağazada erişilebilir hale getirmek için sınıflamaları işleyin.</span><span class="sxs-lookup"><span data-stu-id="5844d-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="5844d-150">Numara serileri, donanım profilleri ve POS ekran düzeni gibi verileri POS kasalarına gönderin.</span><span class="sxs-lookup"><span data-stu-id="5844d-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="5844d-151">POS'a mağaza verilerini göndermek için mağazayı yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="5844d-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="5844d-152">POS'a mağaza verilerini göndermek için işleri çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="5844d-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="5844d-153">Kuruluş hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="5844d-153">Organization hierarchies</span></span>

<span data-ttu-id="5844d-154">Commerce, kanalları yapılandırmak için kuruluş hiyerarşilerini kullanır.</span><span class="sxs-lookup"><span data-stu-id="5844d-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="5844d-155">Organizasyon hiyerarşileri, organizasyonlar arasındaki işinizi meydana getiren ilişkileri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5844d-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="5844d-156">Mağazalar kurduğunuzda, onları bir organizasyon hiyerarşisine ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5844d-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="5844d-157">Ardından mağazalar ürün çeşitleri, stok yenileme ve raporlama için kullanılan verileri paylaşır.</span><span class="sxs-lookup"><span data-stu-id="5844d-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="5844d-158">Commerce satış işlevlerini kullanabilmeniz için **çoklu sevk edilecek** konfigürasyon anahtarının etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5844d-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="5844d-159">Bu konfigürasyon anahtarı, **Sistem yönetimi** \> **Kurulum** \> **Lisans konfigürasyonu** altındaki **ticaret konfigürasyon** anahtarlarında bulunabilir.</span><span class="sxs-lookup"><span data-stu-id="5844d-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="5844d-160">Bu, satış siparişi satırı düzeyinde konfigüre edilen teslimat adresine dayalı olarak çeşitli doğrulamaları gereklidir.</span><span class="sxs-lookup"><span data-stu-id="5844d-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]