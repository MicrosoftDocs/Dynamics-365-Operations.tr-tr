---
title: Sipariş tutmaları yönetme
description: Bu yordam, müşteri satış siparişlerinin nasıl beklemeye alınacağını, sipariş bekletmeleri kullanıma almayla nasıl çalışılacağını ve sipariş bekletmelerinin nasıl kaldırılacağını gösterir.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16e11be633cdffbc8ee3e206eb42e7e1a2f72b9c
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146457"
---
# <a name="manage-order-holds"></a><span data-ttu-id="bea4b-103">Sipariş tutmaları yönetme</span><span class="sxs-lookup"><span data-stu-id="bea4b-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bea4b-104">Bu yordam, müşteri satış siparişlerinin nasıl beklemeye alınacağını, sipariş bekletmeleri kullanıma almayla nasıl çalışılacağını ve sipariş bekletmelerinin nasıl kaldırılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bea4b-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="bea4b-105">Sipariş, çeşitli nedenlerle beklemeye alınabilir.</span><span class="sxs-lookup"><span data-stu-id="bea4b-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="bea4b-106">Örneğin, müşteri adresi veya ödeme yöntemi doğrulanıncaya kadar veya yönetici, müşterinin kredi limitini gözden geçirene kadar siparişi beklemeye alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea4b-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="bea4b-107">Sipariş beklemedeyken sevkiyat için ambar tarafından işlenemez.</span><span class="sxs-lookup"><span data-stu-id="bea4b-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="bea4b-108">Bu prosedürü demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea4b-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="bea4b-109">Sipariş bekletmelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="bea4b-109">Set up order holds</span></span>
1. <span data-ttu-id="bea4b-110">**Gezinti bölmesi > Modüller > Satış ve pazarlama > Ayarla > Satış siparişleri > Sipariş bekletme kodları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="bea4b-111">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-111">Click **New**.</span></span>
3. <span data-ttu-id="bea4b-112">**Bekletme kodu** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="bea4b-113">Örneğin, "Geri çağırma" yazın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="bea4b-114">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="bea4b-115">Örneğin, Sipariş müşteri geri araması için bekletiliyor.</span><span class="sxs-lookup"><span data-stu-id="bea4b-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="bea4b-116">İsteğe bağlı olarak, bu sipariş bekletme kodu eklendiğinde tüm fiziksel rezervasyonları kaldırmak için **Rezervasyonları kaldır** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="bea4b-117">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="bea4b-118">Siparişi beklemeye alma</span><span class="sxs-lookup"><span data-stu-id="bea4b-118">Place order on hold</span></span>
1. <span data-ttu-id="bea4b-119">**Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="bea4b-120">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-120">Click **New**.</span></span>
3. <span data-ttu-id="bea4b-121">**Müşteri hesabı** alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="bea4b-122">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-122">Click **OK**.</span></span>
5. <span data-ttu-id="bea4b-123">**Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="bea4b-124">**Miktar** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="bea4b-125">**Eylem Bölmesinde** **Satış siparişi** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="bea4b-126">**Sipariş bekletmeleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="bea4b-127">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-127">Click **New**.</span></span>
10. <span data-ttu-id="bea4b-128">**Bekletme kodu** alanında, önceki alt görevde oluşturduğunuz kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="bea4b-129">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-129">Click **Save**.</span></span>
12. <span data-ttu-id="bea4b-130">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-130">Close the page.</span></span>
13. <span data-ttu-id="bea4b-131">**Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="bea4b-132">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-132">In the list, mark the selected row.</span></span> <span data-ttu-id="bea4b-133">Şu anda beklemede olan siparişlerde "İşleme" ve "Durduruldu" alanları işaretledir.</span><span class="sxs-lookup"><span data-stu-id="bea4b-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="bea4b-134">Eylem Bölmesi'nde **Çek ve paketle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="bea4b-135">Sipariş tutmaları yönetme</span><span class="sxs-lookup"><span data-stu-id="bea4b-135">Manage order holds</span></span>
1. <span data-ttu-id="bea4b-136">**Satış ve pazarlama > Satış siparişleri > Açık siparişler > Sipariş bekletmeleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="bea4b-137">**Sipariş bekletmeleri** sayfası, bir çalışma ekranı işlevi görür. Burada mevcut ve işlenmiş tüm bekletmelerin bir özetini görebilir, bunları ve ilişkilendirilmiş satış siparişlerini işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea4b-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="bea4b-138">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="bea4b-139">**Eylem Bölmesi**'nde **Ödemeyi beklet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="bea4b-140">**Öde**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-140">Click **Check out**.</span></span>
5. <span data-ttu-id="bea4b-141">Listede, seçili satırın işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="bea4b-142">**Ödemeyi yapan kişi** alanında artık sizin kullanıcı kimliğiniz gösterilir.</span><span class="sxs-lookup"><span data-stu-id="bea4b-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="bea4b-143">**Ödemeyi sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="bea4b-144">**Eylem Bölmesi**'nde **Bekletmeyi sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="bea4b-145">Bekletmeyi kaldırmaya ve siparişin sonraki tamamlanma adımına ilerlemesine izin vermeye hazır olduğunuzda bekletmeyi temizlemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bea4b-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="bea4b-146">Sipariş hiçbir değişiklik gerektirmiyorsa Tutmaları temizle eylemini çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea4b-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="bea4b-147">Ancak bir bekletmeyi temizlerken siparişin güncelleştirilmesi gerekirse Temizle ve değiştir eylemini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bea4b-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="bea4b-148">**Sil ve gönder** eylemi, yalnızca Çağrı merkezi işlevini kullandığınızda geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="bea4b-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="bea4b-149">**Bekletmeleri sil**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bea4b-149">Click **Clear holds**.</span></span> <span data-ttu-id="bea4b-150">Bekletme artık siparişten temizlenmiş ve Etkin bekletmeler listesinden kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="bea4b-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="bea4b-151">Tüm bekletmeleri veya bunların alt kümesini belirli bir duruma göre görmek için Göster alanındaki değeri değiştirin.</span><span class="sxs-lookup"><span data-stu-id="bea4b-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

