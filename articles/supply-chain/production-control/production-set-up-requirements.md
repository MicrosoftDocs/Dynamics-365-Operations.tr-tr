---
title: Üretim kurulumu gereksinimleri
description: Bu makalede, Üretim denetimiyle çalışabilmenize ilişkin kurulum gereksinimleri hakkında bilgi verilmektedir.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0513392fe066e02f0789bcfadb0ee676559cb223
ms.sourcegitcommit: f3456df4d91cf0c51cd395ae64e3c192bd46835e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428412"
---
# <a name="production-setup-requirements"></a><span data-ttu-id="45c34-103">Üretim kurulumu gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="45c34-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45c34-104">Bu makalede, Üretim denetimiyle çalışabilmenize ilişkin kurulum gereksinimleri hakkında bilgi verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="45c34-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="45c34-105">Üretim denetimi, diğer modüllerin özellikler ile tümleşiktir.</span><span class="sxs-lookup"><span data-stu-id="45c34-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="45c34-106">Bu birbiriyle bağlantılı olma durumu, üretim emirlerini değiştirmenize ve bunların sistemdeki diğer tüm ilişkili işlemlerde ve hesaplamalarda otomatik olarak güncelleştirildiğinden emin olmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="45c34-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="45c34-107">Aşağıdaki kurulum yordamları, tamamlanmaları gereken sırada listelenmişlerdir.</span><span class="sxs-lookup"><span data-stu-id="45c34-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="45c34-108">Diğer modüllerdeki gerekli temel kurulum</span><span class="sxs-lookup"><span data-stu-id="45c34-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="45c34-109">Üretim kontrol ile çalışabilmeniz için diğer modüllerdeki bilgilerin ayarlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="45c34-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="45c34-110">Bu kurulum aşağıdaki görevleri içerir:</span><span class="sxs-lookup"><span data-stu-id="45c34-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="45c34-111">Genel şirket bilgilerini ayarlama.</span><span class="sxs-lookup"><span data-stu-id="45c34-111">Set up general company information.</span></span>
-   <span data-ttu-id="45c34-112">Genel muhasebeyi ayarlama.</span><span class="sxs-lookup"><span data-stu-id="45c34-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="45c34-113">Madde grupları tanımlama..</span><span class="sxs-lookup"><span data-stu-id="45c34-113">Define item groups.</span></span>
-   <span data-ttu-id="45c34-114">Madde grupları için genel muhasebe hesapları ayarlama.</span><span class="sxs-lookup"><span data-stu-id="45c34-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="45c34-115">Stok yönetimindeki stok tablosunu ayarlama.</span><span class="sxs-lookup"><span data-stu-id="45c34-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="45c34-116">Stok Yönetimi'nde ürün reçeteleri (BOM) ve ürün reçetesi versiyonları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="45c34-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="45c34-117">Gereken takvim ve kaynak kurulumu</span><span class="sxs-lookup"><span data-stu-id="45c34-117">Required calendar and resource setup</span></span>
<span data-ttu-id="45c34-118">Üretim Denetimi'ni kullanmadan önce Kuruluş Yönetimi'ni açın ve aşağıdaki sırayla takvim ve işlem kaynaklarını oluşturun ve tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="45c34-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="45c34-119">**Çalışma zamanı şablonları** – üretim planlaması için kullanılabilir zamanları tanımlamak için çalışma zamanı şablonları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="45c34-120">**Takvimler** - Üretim çizelgeleme için yılın hangi günlerinin mevcut olduğunu tanımlamak üzere çalışma zamanı takvimleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="45c34-121">**Kaynak grupları** – planlamayı çalıştırdığınızda mevcut boş kapasite hakkında genel bir bakış elde edebilmek için işlem kaynaklarını gruplayacak kaynak gruplarını ayarlamak.</span><span class="sxs-lookup"><span data-stu-id="45c34-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="45c34-122">İşlem kaynaklarını ayarlamadan önce kaynak gruplarını ayarlamak zorunda değilsiniz.</span><span class="sxs-lookup"><span data-stu-id="45c34-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="45c34-123">Ancak, Üretim kontrolü ayarladığınızda, kaynakları nasıl gruplayacağınızı öğrenmenizi tavsiye ederiz..</span><span class="sxs-lookup"><span data-stu-id="45c34-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="45c34-124">**Kaynaklar** – Kapasite planlamak ve üretim sürecini tamamlamak için kullanılacak kaynakları tanımlamak için işlem kaynaklarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="45c34-125">Gerekli üretim parametreleri kurulumu</span><span class="sxs-lookup"><span data-stu-id="45c34-125">Required production parameters setup</span></span>
<span data-ttu-id="45c34-126">**Üretim denetleme parametreleri** – Sistemin üretim emirlerini nasıl işleyeceğini ve ele alacağını tanımlamak için temel üretim parametrelerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="45c34-127">Üretim emirlerinin nasıl oluşturulduğunu, tahmin edildiğini, zamanlandığını ve tüketildiğini tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="45c34-128">Ne tür bir geri bildirim istediğinizi ve maliyet muhasebesinin nasıl yapılacağını da seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="45c34-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="45c34-129">Gerekli günlük adı tanımlaması</span><span class="sxs-lookup"><span data-stu-id="45c34-129">Required journal name identification</span></span>
<span data-ttu-id="45c34-130">**Üretim günlüğü adları** – hareketleri deftere nakletmek ve kaydetmek için kullanılan üretim günlük adlarını belirtin.</span><span class="sxs-lookup"><span data-stu-id="45c34-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="45c34-131">Operasyonları kullanmanız durumunda geçerli kurulum</span><span class="sxs-lookup"><span data-stu-id="45c34-131">Setup if you use operations</span></span>
<span data-ttu-id="45c34-132">Operasyonlar tamamlanmış ürünü imal etmek üzere gerçekleştirilen belirli faaliyetleri göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="45c34-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="45c34-133">**Not:** Maddeyi üretmek için gerekli eylemlerin türlerini ve bu eylemlerin sıralamasını ve önceliklerini biliyor olmanız gereklidir</span><span class="sxs-lookup"><span data-stu-id="45c34-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="45c34-134">Ayrıca hangi kaynakların, ne miktarda gerekli olduğunu bilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="45c34-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="45c34-135">**Operasyonlar** – Tamamlanan maddeyi üretmek için tamamlanması gereken görevleri temsil eden operasyonları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="45c34-136">**İlişkiler** – ayrıntılı özellikler oluşturmak için operasyon ilişkileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="45c34-137">Operasyon ilişkilerini tanımlamak için **İlişkiler** üzerinde **İşlemler** sayfasını tıklayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="45c34-138">Rotaları kullanmanız durumunda geçerli kurulum</span><span class="sxs-lookup"><span data-stu-id="45c34-138">Setup if you use routes</span></span>
<span data-ttu-id="45c34-139">Rotalarla çalışıyorsanız, ayarladığınız tüm üretim rotaları için operasyonların ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="45c34-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="45c34-140">Rota, üretim sürecinin başlangıcından sonuna kadar maddenin operasyondan operasyona aldığı yolu gösterir.</span><span class="sxs-lookup"><span data-stu-id="45c34-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="45c34-141">**Maliyet kategorileri** - belirtilen süreçlerin ve kurulum sürelerinin saat başına maliyetlerini tanımlamak üzere maliyet kategorileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="45c34-142">**Maliyet grupları** – farklı türde maliyetlendirmeleri oluşturmak ve sürdürmek için maliyet grupları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="45c34-143">**Rota grupları** – rota gruplarıyla ilişkili parametreleri tanımlamak için rota grupları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="45c34-144">Üretim rotaları oluşturabilmek için önce rota gruplarını ayarlamanız gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="45c34-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="45c34-145">**Rotalar** - Üretim rotaları ayarlayın ve rota operasyonlarının planlamasını, maliyetlendirmesini, fiyatlandırmasını ve ilerleme raporlamasını kontrol etmek üzere varsayılan ayarlar tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="45c34-146">**Rota sürümü** - Üretimdeki madde varyasyonlarına olanak vermek üzere rota versiyonları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-146">**Route version** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="45c34-147">İsteğe bağlı, gelişmiş ayarlar</span><span class="sxs-lookup"><span data-stu-id="45c34-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="45c34-148">**Üretim grupları** – üretim emri ve genel muhasebe hesapları arasında ilişki kurmak için üretim grupları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="45c34-149">Genel muhasebe hesapları, siparişleri raporlama için gruplandırmak veya nakletmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="45c34-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="45c34-150">**Üretim havuzları** – acil üretim emirlerini işlemek veya sipariş gruplarını silmek ve deftere nakletmek için üretim havuzları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="45c34-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="45c34-151">**Özellikler** – üretimlerin sırasını denetlemek için kaynaklarınıza atadığınız özel öznitelikleri oluşturmak için özellikleri tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="45c34-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="45c34-152">Bu öznitelikler çalışma süresi şablonuna bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="45c34-152">These attributes are connected to the working time template.</span></span>




