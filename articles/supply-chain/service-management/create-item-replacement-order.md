---
title: Madde değiştirme emri oluşturma
description: Madde değiştirme siparişleri genellikle bir ürün iade edildikten ve incelendikten sonra oluşturulur.
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 784a2522c27e8131f211ffc52319552b3b928cc3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556841"
---
# <a name="create-an-item-replacement-order"></a><span data-ttu-id="27d46-103">Madde değiştirme emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="27d46-103">Create an item replacement order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="27d46-104">Madde değiştirme siparişleri genellikle bir ürün iade edildikten ve incelendikten sonra oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27d46-104">Item replacement orders are usually created after a product is returned and inspected.</span></span> <span data-ttu-id="27d46-105">Ancak bir maddenin iade edilmeden önce değiştirilmesi gerekiyorsa veya orijinal madde iade edilmeyecekse iade siparişini oluşturduktan hemen sonra bir madde değiştirme siparişi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27d46-105">However, when an item must be replaced before it has been returned, or when the original item will not be returned, you can create an item replacement order immediately after you create a return order.</span></span>

## <a name="create-a-replacement-order-after-you-receive-an-item-that-is-returned"></a><span data-ttu-id="27d46-106">İade edilen bir maddeyi aldığınızda değiştirme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="27d46-106">Create a replacement order after you receive an item that is returned</span></span>

1.  <span data-ttu-id="27d46-107">**Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27d46-107">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="27d46-108">Yeni bir iade siparişi oluşturun veya **İade emri - RMA numarası: %1, %2** formunu açmak için listeden bir iade siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="27d46-108">Create a new return order, or select a returned order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="27d46-109">**İade satırı**'na tıklayın ve **Yerine koyulacak madde**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27d46-109">Click **Return line**, and then select **Replacement item**.</span></span>

4.  <span data-ttu-id="27d46-110">İade edilen maddenin yerine konulacak maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="27d46-110">Select the item to replace the returned item with.</span></span> <span data-ttu-id="27d46-111">Madde belirtimlerini girin ve ardından **Uygula**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27d46-111">Enter the item specifications, and then click **Apply**.</span></span>

5.  <span data-ttu-id="27d46-112">İade sipariş için sevk irsaliyesi oluşturmak üzere **Sevk irsaliyesi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27d46-112">Click **Packing slip** to generate the packing slip for the return order.</span></span> <span data-ttu-id="27d46-113">Seçtiğiniz yerine konulan madde için bir satış siparişi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27d46-113">A sales order is generated for the replacement item that you selected.</span></span>
    
    <span data-ttu-id="27d46-114">Yerine konulan madde için için satış siparişi oluşturulduktan sonra otomatik olarak satış sözleşmeleri aranır ve uygulanan bir satış sözleşmesini varsa satış siparişine uygulanır.</span><span class="sxs-lookup"><span data-stu-id="27d46-114">After the sales order is created for the replacement item, sales agreements are automatically searched and if there is an applicable sales agreement, it is applied to the sales order.</span></span>

## <a name="create-a-replacement-order-before-you-receive-an-item-that-will-be-returned"></a><span data-ttu-id="27d46-115">İade edilecek bir maddeyi almadan önce değiştirme siparişi oluşturma</span><span class="sxs-lookup"><span data-stu-id="27d46-115">Create a replacement order before you receive an item that will be returned</span></span>

1.  <span data-ttu-id="27d46-116">**Satış ve pazarlama** \> **Genel** \> **İade siparişleri** \> **Tüm iade siparişleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27d46-116">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="27d46-117">Yeni bir iade siparişi oluşturun veya **İade emri - RMA numarası: %1, %2** formunu açmak için listeden bir iade siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="27d46-117">Create a new return order, or select a return order from the list to open the **Return order - RMA number: %1, %2** form.</span></span>

3.  <span data-ttu-id="27d46-118">İade edilen madde için satış siparişi tanımlamak isterseniz **Satış siparişini bul**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27d46-118">Click **Find sales order** if you want to identify the sales order for the returned item.</span></span> <span data-ttu-id="27d46-119">**Satış siparişi bul** formunu doldurun ve formu kapatmak için **Tamam**'a tıklayın, **İade siparişi - RMA numarası: %1, %2** formuna geri dönün.</span><span class="sxs-lookup"><span data-stu-id="27d46-119">Complete the **Find sales order** form and then click **OK** to close the form and return to the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="27d46-120">İade edilen maddeyle ilişkili satış siparişi satırı iade siparişine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="27d46-120">The sales order line for the returned item is copied to the return order.</span></span>

4.  <span data-ttu-id="27d46-121">**Satış siparişi oluştur** formunu açmak için **Değiştirme siparişi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="27d46-121">Click **Replacement order** to open the **Create sales order** form.</span></span>

5.  <span data-ttu-id="27d46-122">**İade siparişi - RMA numarası %1, %2** formunda seçtiğiniz iade siparişindeki ayrıntıları bu satış siparişine transfer etmek için **İade siparişi satırlarını kopyala** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="27d46-122">Select the **Copy return order lines** check box to transfer details from the return order you selected on the **Return order - RMA number: %1, %2** form to this sales order.</span></span>

6.  <span data-ttu-id="27d46-123">Ayrıntıları gerektiği gibi girin veya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="27d46-123">Enter or modify details, as required.</span></span>
    
    <span data-ttu-id="27d46-124">Satış siparişini adım 3'te tanımladıysanız ve iade edilen madde için satış sipariş satırı bir satış sözleşmesine bağlıysa, uygun satış sözleşmesinin madde değiştirme siparişi tanımlayıcısı otomatik olarak **Satış sözleşmesi kodu** alanında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="27d46-124">If you identified the sales order in step 3, and if the sales order line for the returned item is linked to a sales agreement, the identifier of the applicable sales agreement for the item replacement order will be automatically displayed in the **Sales agreement ID** field.</span></span>

7.  <span data-ttu-id="27d46-125">**Satış siparişi oluştur** formunu kapatmak için **Tamam**'a tıklayın, yeni satış siparişi için bilgileri girmeye devam edebileceğiniz **Satış siparişi** formunu açın.</span><span class="sxs-lookup"><span data-stu-id="27d46-125">Click **OK** to close the **Create sales order** form and open the **Sales order** form, where you can continue to enter information for the new sales order.</span></span> <span data-ttu-id="27d46-126">Geçerli iade sipariş satırları yeni satış siparişine kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="27d46-126">Any applicable return order lines will be copied to the new sales order.</span></span> 
    
    <span data-ttu-id="27d46-127">Satış sözleşmesi tanımlayıcısı otomatik olarak **Satış sözleşmesi kodu** alanında görüntülenirse, satış sözleşmesi madde değiştirme siparişiyle ilgili satış siparişi başlığına bağlanır.</span><span class="sxs-lookup"><span data-stu-id="27d46-127">If the identifier of the sales agreement is automatically displayed in the **Sales agreement ID** field, then the sales agreement has been linked to the sales order header for the item replacement order.</span></span> <span data-ttu-id="27d46-128">Satış sözleşmesinde henüz karşılanmamış geçerli bir taahhüt varsa ve satış siparişi satış sözleşmesi sona ermeden önce oluşturulursa, satış sözleşmesi ile satış siparişi satırı arasında bir bağlantı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="27d46-128">If there is an applicable commitment in the sales agreement that has not been fulfilled yet, and the sales order is created before the sales agreement expires, a link is established between the sales agreement line and the sales order line.</span></span> <span data-ttu-id="27d46-129">Bu nedenle, satış sözleşmesinden alınan madde fiyatı gibi bilgiler yeni satış sipariş satırına kopyalanır.</span><span class="sxs-lookup"><span data-stu-id="27d46-129">Therefore, information from the sales agreement, such as item price, is copied to the new sales order line.</span></span> 
  


