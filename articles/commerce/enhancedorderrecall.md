---
title: Satış noktasında sipariş işlemini geri çekme
description: Bu konu, POS'taki geliştirilmiş sipariş geri çekme sayfaları için kullanılabilen özellik yeteneklerini açıklar.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 41944fb7819b5527f6bc023a60acd9450d9e43c2
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974850"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="91269-103">Satış noktasında sipariş işlemini geri çekme</span><span class="sxs-lookup"><span data-stu-id="91269-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91269-104">Commerce satış noktasındaki (POS) sipariş geri çekme işlemi, güncelleştirilmiş sipariş arama ve filtreleme özellikleri ve siparişe özel bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="91269-104">The Recall order operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="91269-105">Bu özellik Commerce 10.0.15 sürümü ve sonrasında bulunur.</span><span class="sxs-lookup"><span data-stu-id="91269-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="91269-106">Bu işlevi etkinleştirmek için, Commerce Headquarters'daki **Özellik yönetimi** çalışma alanında yer alan **POS'taki iyileştirilmiş sipairş geri çekme işlemi** özelliğini açın.</span><span class="sxs-lookup"><span data-stu-id="91269-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="91269-107">Özellik etkinleştirildikten sonra, değiştirilen bazı yeteneklerden yararlanmak için [ekran düzenlerini](pos-screen-layouts.md) güncelleştirmeyi düşünebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="91269-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="91269-108">**Sipariş geri çekme** işlemi düğmesinin yapılandırması, kuruluşların işlemi önceden tanımlanmış bir görüntü ile dağıtmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="91269-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Düğme grubu yapılandırması](media/recallorderbuttongrid.png)

<span data-ttu-id="91269-110">Ekran seçenekleri şunlardır:</span><span class="sxs-lookup"><span data-stu-id="91269-110">The display options are as follows.</span></span>
- <span data-ttu-id="91269-111">**Hiçbiri** – Bu seçenek, işlemi belirli bir ekran olmadan dağıtır.</span><span class="sxs-lookup"><span data-stu-id="91269-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="91269-112">Kullanıcı bu yapılandırmayla işlemi açtığında, sipariş araması ve bulması veya önceden tanımlanmış bir sipariş filtresi seçmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="91269-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="91269-113">**Karşılanacak siparişler** – Kullanıcı operasyonu başlattığında, mağaza tarafından karşılanması gereken siparişlerin listesini arayıp görüntülemek için bir sorgu otomatik olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="91269-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="91269-114">Bu siparişler, mağaza içi malzeme çekme veya mağaza sevkiyatı için yapılandırılır ve bu siparişlerin satırları henüz çekilmemiştir veya paketlenememiştir.</span><span class="sxs-lookup"><span data-stu-id="91269-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="91269-115">**Çekilecek siparişler** – Kullanıcı operasyonu başlattığında, kullanıcının geçerli mağazasında mağazadan çekme için yapılandırılan siparişlerin listesini arayıp görüntülemek için bir sorgu otomatik olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="91269-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="91269-116">**Sevk edilecek siparişler** – Kullanıcı operasyonu başlattığında, kullanıcının geçerli mağazasından sevkiyat için yapılandırılan siparişlerin listesini arayıp görüntülemek için bir sorgu otomatik olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="91269-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="91269-117">POS'tan **Sipariş geri çekme** işlemi başlatılırken, görüntü **Hiçbiri** olarak yapılandırıldığında, kullanıcı siparişleri aşağıdaki yollardan biriyle arayabilir ve alabilir.</span><span class="sxs-lookup"><span data-stu-id="91269-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="91269-118">Sipariş barkodlarını tarama.</span><span class="sxs-lookup"><span data-stu-id="91269-118">Scan order barcodes.</span></span> <span data-ttu-id="91269-119">Bu, eşleştirmeler için sipariş numarası, kanal referansı ve giriş kodu alanlarını arar.</span><span class="sxs-lookup"><span data-stu-id="91269-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="91269-120">Filtre ölçütüne uyan siparişleri bulmak üzere filtreleme mekanizmasını kullanmak için uygulama çubuğunda **Siparişleri ara** veya **Ara ve filtrele** simgesini seçin.</span><span class="sxs-lookup"><span data-stu-id="91269-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="91269-121">**Siparişleri Göster** açılır menüsünden (karşılanacak siparişler, alınacak siparişler veya sevk edilecek siparişler) önceden tanımlanmış filtreler arasından seçim yapın.</span><span class="sxs-lookup"><span data-stu-id="91269-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="91269-123">Arama ölçütleri uygulandıktan sonra, uygulama eşleşen satış siparişlerinin listesini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="91269-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="91269-125">Bir kullanıcı ek ayrıntıları görüntülemek için listeden bir sipariş seçebilir.</span><span class="sxs-lookup"><span data-stu-id="91269-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="91269-126">Ekranın sağ tarafındaki bilgi paneli sipariş satırı detayları, teslimat detayları ve karşılama detayları da dahil olmak üzere seçili siparişle ilgili özellikleri görüntüler.</span><span class="sxs-lookup"><span data-stu-id="91269-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="91269-127">Uygulama çubuğunda, kullanıcı bir operasyon seçebilir.</span><span class="sxs-lookup"><span data-stu-id="91269-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="91269-128">Siparişin durumuna bağlı olarak, belirli operasyonlar etkinleştirilmemiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="91269-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="91269-129">**İade** – Seçilen müşteri siparişiyle ilgili bir veya daha fazla fatura için bir iade yürütür.</span><span class="sxs-lookup"><span data-stu-id="91269-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="91269-130">**İptal** – Seçili satış siparişinin tam iptalini yapar.</span><span class="sxs-lookup"><span data-stu-id="91269-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="91269-131">**Karşıla** – Kullanıcıyı, seçilen sipariş için ön filtre uygulanacak sipariş karşılama sayfasına aktarır.</span><span class="sxs-lookup"><span data-stu-id="91269-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="91269-132">Yalnızca seçili sipariş için kullanıcının mağazası tarafından karşılanmaya açık olan sipariş satırları görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="91269-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="91269-133">**Düzenle** – Kullanıcıların seçili müşteri siparişinde değişiklik yapmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="91269-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="91269-134">**Çek** – Kullanıcının çekilecek ürünleri seçmesine ve malzeme çekme satış hareketini oluşturulmasına olanak sağlayan malzeme çekme akışını başlatır.</span><span class="sxs-lookup"><span data-stu-id="91269-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
