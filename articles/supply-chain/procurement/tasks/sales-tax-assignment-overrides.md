--- 
title: "Satış vergisi atama ve geçersiz kılma"
description: "Bu yordam perakende kanallarına satış vergisi gruplarının nasıl atanacağını gösterir."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 2420dceeb321ed11dbf6d7d9c09e3a579d65134c
ms.contentlocale: tr-tr
ms.lasthandoff: 09/11/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="14d6d-103">Satış vergisi atama ve geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="14d6d-103">Sales tax assignment and overrides</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14d6d-104">Bu yordam perakende kanallarına satış vergisi gruplarının nasıl atanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="14d6d-105">Ayrıca, yeni bir satış vergisi geçersiz kılma işlemi oluşturma ve mevcut bir satış vergisi geçersiz kılma grubuna atama işleminin üzerinden geçer.</span><span class="sxs-lookup"><span data-stu-id="14d6d-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="14d6d-106">Bu yordam</span><span class="sxs-lookup"><span data-stu-id="14d6d-106">This procedure</span></span>

<span data-ttu-id="14d6d-107">demo verilerdeki USRT şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="14d6d-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="14d6d-108">Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="14d6d-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="14d6d-109">Listede, "Houston" için Perakende Kanalı Kodu bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="14d6d-110">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-110">Click Edit.</span></span>
    * <span data-ttu-id="14d6d-111">"Satış vergisi grubu" alanı mevcut şirket için satış vergisi gruplarının listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="14d6d-112">Mevcut atanan grup, genel bir "Teksas" satış vergisi grubudur.</span><span class="sxs-lookup"><span data-stu-id="14d6d-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="14d6d-113">"Washington" ve "Washington, King County" için satış vergi grupları vardır.</span><span class="sxs-lookup"><span data-stu-id="14d6d-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="14d6d-114">Satış vergisi grupları birden fazla belediye için vergileri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="14d6d-115">"Satış vergisi geçersiz kılma" alanı satış vergisi geçersiz kılma gruplarının kanala eşlenebildiği yerdir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="14d6d-116">Satış vergisi geçersiz kılma grupları birden fazla mağaza için çalışan satış vergisi geçersiz kılma işlemlerini gruplamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="14d6d-117">Satış vergisi geçersiz kılma işlemlerini, el ile tek tek atamak yerine zaman kazanmak için grup oluşturulup doğrudan kanallara atanabilir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="14d6d-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-118">Click Save.</span></span>
5. <span data-ttu-id="14d6d-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-119">Close the page.</span></span>
6. <span data-ttu-id="14d6d-120">Perakende ve ticaret > Kanal kurulumu > Satış vergileri > Satış vergisi geçersiz kılma işlemlerine gidin.</span><span class="sxs-lookup"><span data-stu-id="14d6d-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="14d6d-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-121">Click New.</span></span>
8. <span data-ttu-id="14d6d-122">Satış vergisi geçersiz kılma alanında yeni geçersiz kılma işleminize bir ad verin.</span><span class="sxs-lookup"><span data-stu-id="14d6d-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="14d6d-123">Açıklama alanında geçersiz kılma işleminin bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="14d6d-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="14d6d-124">Durumu "Etkinleştir" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="14d6d-125">Geçersiz Kıl bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="14d6d-126">Tür alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="14d6d-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="14d6d-127">Madde satış vergisi grubu, gruba ait olan belirli maddeler için vergileri geçersiz kılmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="14d6d-128">Örneğin, yiyecek maddeleri genellikle bozulmaz mallardan farklı olarak vergilendirilir ve büyük ihtimalle kendilerine ait satış vergisi grubu vardır.</span><span class="sxs-lookup"><span data-stu-id="14d6d-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="14d6d-129">Satış vergisi grupları, belirli bir kanala uygulanabilir vergilerin gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="14d6d-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="14d6d-130">Örneğin, bir kanal hem perakende hem de işletmeler arası satış yapıyorsa, farklı maddelerin satış vergisi grupları kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="14d6d-131">Uygulanabilir tüm vergiler satış vergisi grubuna eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="14d6d-132">Şimdi satış vergisi geçersiz kılma işleminizi oluşturmak için "Kimden" ve "Kime" vergilerini veya "İlk vergi grubu" ve "Son vergi grubu" öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14d6d-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="14d6d-133">"Kimden" alanı, geçersiz kılınacak vergi veya vergi grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="14d6d-134">Madde satış vergisi grubunu geçersiz kılma işlemi, satış vergisi grubuna göre geçersiz kılma işleminden farklı seçenekler sunar.</span><span class="sxs-lookup"><span data-stu-id="14d6d-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="14d6d-135">Satış vergisi geçersiz kılma işlemleri, vergileri tüm işlemler veya işlemde belirli satırlar üzerinde geçersiz kılacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="14d6d-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="14d6d-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-136">Click Save.</span></span>
14. <span data-ttu-id="14d6d-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-137">Close the page.</span></span>
15. <span data-ttu-id="14d6d-138">Perakende ve ticaret > Kanal kurulumu > Satış vergileri > Satış vergisi geçersiz kılma grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="14d6d-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="14d6d-139">Bu adımda, Houston kanalına atanmış satış vergisi geçersiz kılma grubuna yeni oluşturulan satış vergisi geçersiz kılma işlemi atayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="14d6d-140">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-140">Click Edit.</span></span>
17. <span data-ttu-id="14d6d-141">Kurulum bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="14d6d-142">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-142">Click Add.</span></span>
19. <span data-ttu-id="14d6d-143">Satış vergisi geçersiz kılma alanında, aramayı açmak için açılır düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="14d6d-144">Listeden, önceden oluşturulan satış vergisi geçersiz kılma işlemini seçin.</span><span class="sxs-lookup"><span data-stu-id="14d6d-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="14d6d-145">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="14d6d-146">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="14d6d-146">Click Save.</span></span>


