---
title: Stok durdurma oluştur ve sürdür
description: Bu konu, stok durdurmanın eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemek üzere nasıl kullanılacağını gösterir.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956170"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="899d8-103">Stok durdurma oluştur ve sürdür</span><span class="sxs-lookup"><span data-stu-id="899d8-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="899d8-104">Bu konu, stok durdurmanın eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemek üzere nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="899d8-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="899d8-105">Bu konudaki prosedürlere başlamadan önce, fiziksel eldeki stoğun kullanılabilir olduğu bir öğenizin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="899d8-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="899d8-106">Stoku engelle</span><span class="sxs-lookup"><span data-stu-id="899d8-106">Block inventory</span></span>

<span data-ttu-id="899d8-107">Stoğun durdurabilmesi için stok durdurma kaydı oluşturmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="899d8-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="899d8-108">**Stok yönetimi \> Periyodik görevler \> Stok durdurma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="899d8-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="899d8-109">Eylem Bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="899d8-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="899d8-110">Yeni durdurma kaydının başlığında, **Öğe numarası** alanını durdurmak istediğiniz öğeye ayarlayıp bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="899d8-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="899d8-111">**Genel** hızlı sekmesinde, **Miktar** alanına durdurulacak öğe sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="899d8-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="899d8-112">**Stok boyutları** hızlı sekmesinde, durdurmak istediğiniz öğelerin bulunduğu tesisi ve ambarı belirtin.</span><span class="sxs-lookup"><span data-stu-id="899d8-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="899d8-113">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="899d8-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="899d8-114">Stok durdurma koşullarını güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="899d8-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="899d8-115">Stok durdurma kaydını güncelleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="899d8-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="899d8-116">**Stok yönetimi \> Periyodik görevler \> Stok durdurma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="899d8-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="899d8-117">Liste bölmesinde, ilgili durdurma kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="899d8-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="899d8-118">Kaydı, gerektiği şekilde düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="899d8-118">Edit the record as required.</span></span> <span data-ttu-id="899d8-119">Örneğin, durdurulan stoğun rezervasyon için ne zaman kullanılabilir hale geleceğini belirtmek için **Beklenen tarih** alanının değerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="899d8-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="899d8-120">**Beklenen girişler** seçeneği seçilmişse tarih, beklenen harekette görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="899d8-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="899d8-121">(Manuel olarak bir durdurma kaydı oluşturduğunuzda, **Beklenen girişler** seçeneği varsayılan olarak seçilir.)</span><span class="sxs-lookup"><span data-stu-id="899d8-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="899d8-122">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="899d8-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="899d8-123">Stok durdurmayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="899d8-123">Unblock inventory</span></span>

<span data-ttu-id="899d8-124">Stoğun durdurmasını kaldırmak için stok durdurma kaydını kaldırmak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="899d8-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="899d8-125">**Stok yönetimi \> Periyodik görevler \> Stok durdurma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="899d8-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="899d8-126">Liste bölmesinde, ilgili durdurma kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="899d8-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="899d8-127">Eylem Bölmesi'nde **Sil**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="899d8-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="899d8-128">İşlemi onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="899d8-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="899d8-129">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="899d8-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="899d8-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="899d8-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
