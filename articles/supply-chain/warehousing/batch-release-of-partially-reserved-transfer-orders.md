---
title: "Kısmen rezerve edilen transfer emirleri için toplu iş serbest bırakma"
description: "Bu konu bir mobil cihazdan kısmi rezerve edilmiş transfer emirlerini toplu serbest bırakmanın nasıl ayarlanacağını ve uygulanacağını açıklamaktadır."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4569ba5d24f84166254cfce86d9fe2cc9b98ac09
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="batch-release-of-partially-reserved-transfer-orders"></a><span data-ttu-id="7c416-103">Kısmen rezerve edilen transfer emirleri için toplu iş serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="7c416-103">Batch release of partially reserved transfer orders</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7c416-104">Kısmi rezerve edilmiş transfer emirlerini toplu serbest bırakma işlevi, bir transfer emrini bir ambara, bir toplu iş kullanarak kısmi serbest bırakmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="7c416-104">The functionality for batch release of partially reserved transfer orders lets you partially release transfer orders to a warehouse by using a batch job.</span></span>
<span data-ttu-id="7c416-105">Kısmi bir miktarı serbest bırakma seçeneğine sahip olduğunuz için bir siparişi serbest bırakmadan önce tüm miktarın ambarda kullanılabilir olmasını beklemenize gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="7c416-105">Because you have the option to release a partial quantity, you don’t have to wait for the whole order quantity to be available in the warehouse before you release an order.</span></span>

<span data-ttu-id="7c416-106">Siparişlerin bir ambara serbest bırakılması, gelişmiş bir ambar yönetimi işlemidir.</span><span class="sxs-lookup"><span data-stu-id="7c416-106">The release of orders to a warehouse is an advanced warehouse management process.</span></span> <span data-ttu-id="7c416-107">Bu işlem çekme, paketleme, sevkiyat gibi bir ambar çalışanının bir mobil cihaz kullanarak gerçekleştirebileceği etkinlikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="7c416-107">This process involves activities, such as picking, packing, and shipping, that a warehouse worker can perform by using a mobile device.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="7c416-108">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="7c416-108">Where it applies</span></span>

<span data-ttu-id="7c416-109">Bu işlev için, transfer emirleri bir ambara bir toplu iş kullanarak serbest bırakılır.</span><span class="sxs-lookup"><span data-stu-id="7c416-109">For this functionality, transfer orders are released to a warehouse by using a batch job.</span></span> <span data-ttu-id="7c416-110">Bu işlev, ambarda yeterli stoka sahip değilseniz ancak maddeleri yine de bir ambardan diğerine transfer etmek istiyorsanız yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="7c416-110">This functionality is useful when you don’t have enough inventory in the warehouse, but you still want to transfer items from one warehouse to another.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="7c416-111">Nasıl ayarlanır</span><span class="sxs-lookup"><span data-stu-id="7c416-111">How it is set up</span></span>

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="7c416-112">Transfer emirleri ve satış siparişleri için yerine getirilme ölçütleri belirtin</span><span class="sxs-lookup"><span data-stu-id="7c416-112">Specify fulfillment criteria for transfer orders and sales orders</span></span>

<span data-ttu-id="7c416-113">Bir sipariş kısmen bir ambara toplu bir işte serbest bırakılmadan önce, yerine ölçütünün karşılanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7c416-113">Before an order can be partially released to a warehouse in a batch, the fulfillment criteria must be met.</span></span> <span data-ttu-id="7c416-114">Bu karşılanma kriterleri yerine getirme ilkesi tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="7c416-114">These fulfillment criteria are determined by the fulfillment policy.</span></span>

<span data-ttu-id="7c416-115">Transfer emirleri ve satış siparişleri için yerine getirme ilkeleri şirket düzeyinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="7c416-115">Fulfillment policies for transfer orders and sales orders are specified at the company level.</span></span> <span data-ttu-id="7c416-116">Yerine getirme ilkesinin kurulumuna bağlı olarak, bir toplu işteki siparişlerin serbest bırakılması kabul veya reddedilir.</span><span class="sxs-lookup"><span data-stu-id="7c416-116">Depending on the setup of the fulfillment policy, the release of orders in a batch will be accepted or rejected.</span></span> <span data-ttu-id="7c416-117">Siparişler daha sonra uygun şekilde işlenir.</span><span class="sxs-lookup"><span data-stu-id="7c416-117">The orders will then be processed accordingly.</span></span>

-   <span data-ttu-id="7c416-118">Transfer emirleri ve satış siparişleri için yerine getirme ilkeleri oluşturmak için **Ambar yönetim** \> **Kurulum** \> **Ambara serbest bırakma** \> **Yerine getire ilkesi** üzerine tıklayın ve bir ad ve açıklama girerek bir yerine getirme ilkesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="7c416-118">To create fulfillment policies for transfer orders and sales orders, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then create a fulfillment policy by entering a name and a description.</span></span>

-   <span data-ttu-id="7c416-119">Yerine getirme oranını, bir değer türünü ve yerine getirme ilkesi ihlal edilirse gösterilecek mesajı belirtmek için **Ambar yönetimi** \> **Kurulum** \> **Ambara serbest bırak** \> **Yerine getirme ilkesi** üzerine tıklayın ve sonra **Yerine getirme oranı**, **Değer türü** ve **Yerine getirme ihlal mesajı** alanlarını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7c416-119">To specify a fulfillment rate, a value type, and the message that is shown if the fulfillment policy is violated, click **Warehouse management** \> **Setup** \> **Release to warehouse** \> **Fulfillment policy**, and then set the **Fulfillment rate**, **Value type**, and **Fulfillment violation message** fields.</span></span>

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a><span data-ttu-id="7c416-120">Transfer emirleri ve satış siparişleri için yerine getirilme ilkelerini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="7c416-120">Set the fulfillment policies for transfer orders and sales orders</span></span>

-   <span data-ttu-id="7c416-121">Transfer emirler için yerine getirme ilkelerini ayarlamak için **Stok yönetimi** \> **Kurulum** \> **Stok ve ambar yönetimi parametreleri** \> **Transfer emirleri** \> **Ambar yönetimi** üzerine tıklayın ve sonra bir transfer emri yerine getirme ilkesi satın.</span><span class="sxs-lookup"><span data-stu-id="7c416-121">To set the fulfillment policies for transfer orders, click **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters** \> **Transfer orders** \> **Warehouse management**, and then select a transfer order fulfillment policy.</span></span>

-   <span data-ttu-id="7c416-122">Satış siparişleri için yerine getirme ilkesi ayarlamak için **Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri** \> **Ambar yönetimi** üzerine tıklayın ve bir satış siparişi yerine getirme ilkesi seçin.</span><span class="sxs-lookup"><span data-stu-id="7c416-122">To set the fulfillment policies for sales orders, click **Accounts receivable** \> **Setup** \> **Accounts receivable parameters** \> **Warehouse management**, and then select a sales order fulfillment policy.</span></span>

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-release-in-a-batch"></a><span data-ttu-id="7c416-123">Toplu iş içinde serbest bırakmaya izin verin ve bir toplu iş içinde serbest bırakılacak miktarı belirtin.</span><span class="sxs-lookup"><span data-stu-id="7c416-123">Allow release in a batch and specify the quantity that should be release in a batch</span></span>

<span data-ttu-id="7c416-124">Bir toplu iş, siparişleri bir ambara toplu olarak serbest bırakmakta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7c416-124">A batch job is used to release orders to a warehouse in a batch.</span></span> <span data-ttu-id="7c416-125">Bir toplu işte çalışacak siparişleri ayırt eden parametreler, toplu işin kendisinde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7c416-125">The parameters that distinguish the orders that should be run in a batch job are set on the batch job itself.</span></span>

<span data-ttu-id="7c416-126">**Miktar** parametresi, fiziksel olarak rezerve edilmiş miktarı veya toplam miktarın mı toplu işte serbest bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c416-126">The **Quantity** parameter specifies whether the whole quantity or the physically reserved quantity should be released in the batch.</span></span> <span data-ttu-id="7c416-127">**Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver** parametresi, toplu işteki hangi siparişlerin, daha önce kısmen serbest bırakılmışlarsa kabul edileceğini veya reddedileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="7c416-127">The **Allow release of partially released orders** parameter determines whether orders in the batch should be accepted or rejected if they were partially released earlier.</span></span>

-   <span data-ttu-id="7c416-128">Transfer siparişleri için **Miktar** ve **Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver** parametrelerini ayarlamak için **Ambar yönetimi** \> **Ambara serbest bırak** \> **Transfer siparişlerinin otomatik serbest bırakması** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c416-128">To set the **Quantity** and **Allow release of partially released orders** parameters for transfer orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of transfer orders**.</span></span>

-   <span data-ttu-id="7c416-129">Satış siparişleri için **Miktar** ve **Kısmi serbest bırakılmış siparişlerin serbest bırakılmasına izin ver** parametrelerini ayarlamak için **Ambar yönetimi** \> **Ambara serbest bırak** \> **Satış siparişlerinin otomatik serbest bırakması** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7c416-129">To set the **Quantity** and **Allow release of partially released orders** parameters for sales orders, click **Warehouse management** \> **Release to warehouse** \> **Automatic release of sales orders**.</span></span>

