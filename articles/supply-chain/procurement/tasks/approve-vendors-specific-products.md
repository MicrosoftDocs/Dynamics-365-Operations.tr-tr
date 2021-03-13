---
title: Belirli ürünler için satıcıları onaylama
description: Bu yordam, belirli ürünler için satıcıları onaylamayı gösterir.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cc7d8a93bdbdb5a1446fc34beff4b74aa9d11a0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016665"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="8b8b8-103">Belirli ürünler için satıcıları onaylama</span><span class="sxs-lookup"><span data-stu-id="8b8b8-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b8b8-104">Bu yordam, belirli ürünler için satıcıları onaylamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="8b8b8-105">Bu, bir ürün satınalma siparişine eklendiğinde hangi satıcıların kullanılabileceğini denetlemenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="8b8b8-106">Bu yordamı, demo veri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="8b8b8-107">Genellikle bu görev bir Satınalma yöneticisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="8b8b8-108">Gezinti bölmesi'nde **Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="8b8b8-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8b8b8-110">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8b8b8-111">**Satınalma** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="8b8b8-112">**Satıcı** alanında gösterilen birincil bir satıcı var ise bu satıcıyı aşağıdaki adımlarla onaylı bir satıcı olarak eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="8b8b8-113">Eğer gösterilen varsa, satıcı numarasını not alın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="8b8b8-114">Eylem Bölmesinde, **Satınalma** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="8b8b8-115">**Kurulum**’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-115">Click **Setup**.</span></span>
7. <span data-ttu-id="8b8b8-116">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-116">Click **Add**.</span></span>
8. <span data-ttu-id="8b8b8-117">Satıcı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="8b8b8-118">Onaylanan satıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-118">Select the approved vendor.</span></span> <span data-ttu-id="8b8b8-119">En az bir satırın birincil satıcı olması gerekir, eğer ürün kaydında bir tane varsa.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="8b8b8-120">Daha önce satıcı numarasını not ettiyseniz, burada seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="8b8b8-121">**Bitiş** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="8b8b8-122">Bir kaç ay sonraki bir tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="8b8b8-123">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-123">Click **Add**.</span></span>
11. <span data-ttu-id="8b8b8-124">**Satıcı** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="8b8b8-125">**Bitiş** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="8b8b8-126">Önceki sona erme tarihinden farklı bir tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="8b8b8-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-127">Close the page.</span></span>
14. <span data-ttu-id="8b8b8-128">Eylem Bölmesi'nde, **Onaylanan satıcılar** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="8b8b8-129">**Bitiş** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="8b8b8-130">Bu tarih, belirli bir tarihe kadar olan onaylanan satıcıları görebilmeniz için bir filtre görevi görür.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="8b8b8-131">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-131">Close the page.</span></span>
17. <span data-ttu-id="8b8b8-132">Eylem Bölmesi'nde, **Yürürlük dönemi** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="8b8b8-133">**Satıcılar tarafından alan süresi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="8b8b8-134">Belirli bir tarihten sonra onay durumunu sona erecek satıcıları tanımlamak için bu sayfayı kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="8b8b8-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-135">Close the page.</span></span>
20. <span data-ttu-id="8b8b8-136">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-136">Click **Edit**.</span></span>
21. <span data-ttu-id="8b8b8-137">**Onaylanmış satıcı çeki yöntemi** alanında, bir seçeneği işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="8b8b8-138">Bu alan, bir satınalma siparişi satırına eklenen bir ürünün, satıcı onaylanmış bir satıcı olmadığında ne olacağını belirleyecek ilkeyi seçmenize olanak verir.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="8b8b8-139">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-139">Click **Save**.</span></span>
23. <span data-ttu-id="8b8b8-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-140">Close the page.</span></span>
24. <span data-ttu-id="8b8b8-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-141">Close the page.</span></span>
25. <span data-ttu-id="8b8b8-142">Gezinti Bölmesi'nde **Modüller > Tedarik ve kaynak atama > Satıcılar > Satıcı/madde ilişkileri > Maddeye göre onaylı satıcı listesi öğesi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="8b8b8-143">Bu sayfa, tüm ürünler ve onaylı satıcılara genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="8b8b8-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-144">Close the page.</span></span>
27. <span data-ttu-id="8b8b8-145">Gezinti Bölmesi'nde **Modüller > Tedarik ve kaynak atama > Satıcılar > Tüm satıcılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="8b8b8-146">Ayrıca bir satıcıdan başlatabilir ve o satıcı hesabı için onaylanan ürünler listesine gidebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="8b8b8-147">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="8b8b8-148">Eylem Bölmesi'nde, **Tedarik** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="8b8b8-149">**Satıcıya göre onaylı satıcı listesi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="8b8b8-150">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-150">Close the page.</span></span>
32. <span data-ttu-id="8b8b8-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="8b8b8-151">Close the page.</span></span>

