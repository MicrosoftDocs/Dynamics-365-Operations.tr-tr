---
title: Satış vergisi atama ve geçersiz kılma
description: Bu yordam ticaret kanallarına satış vergisi gruplarının nasıl atanacağını gösterir.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 469850d8ed9251a827e834a483653ea7926bd414
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244075"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="9cd14-103"> Satış vergisi atama ve geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="9cd14-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9cd14-104">Bu yordam ticaret kanallarına satış vergisi gruplarının nasıl atanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="9cd14-105">Ayrıca, yeni bir satış vergisi geçersiz kılma işlemi oluşturma ve mevcut bir satış vergisi geçersiz kılma grubuna atama işleminin üzerinden geçer.</span><span class="sxs-lookup"><span data-stu-id="9cd14-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="9cd14-106">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="9cd14-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9cd14-107">Perakende ve Ticaret > Kanallar > Mağazalar > Tüm mağazalar'a gidin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="9cd14-108">Listede, "Houston" için Kanalı Kodu bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="9cd14-109">Düzenle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-109">Click Edit.</span></span>
    * <span data-ttu-id="9cd14-110">"Satış vergisi grubu" alanı mevcut şirket için satış vergisi gruplarının listesini içerir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="9cd14-111">Mevcut atanan grup, genel bir "Teksas" satış vergisi grubudur.</span><span class="sxs-lookup"><span data-stu-id="9cd14-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="9cd14-112">"Washington" ve "Washington, King County" için satış vergi grupları vardır.</span><span class="sxs-lookup"><span data-stu-id="9cd14-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="9cd14-113">Satış vergisi grupları birden fazla belediye için vergileri içerebilir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="9cd14-114">"Satış vergisi geçersiz kılma" alanı satış vergisi geçersiz kılma gruplarının kanala eşlenebildiği yerdir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="9cd14-115">Satış vergisi geçersiz kılma grupları birden fazla mağaza için çalışan satış vergisi geçersiz kılma işlemlerini gruplamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="9cd14-116">Satış vergisi geçersiz kılma işlemlerini, el ile tek tek atamak yerine zaman kazanmak için grup oluşturulup doğrudan kanallara atanabilir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="9cd14-117">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-117">Click Save.</span></span>
5. <span data-ttu-id="9cd14-118">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-118">Close the page.</span></span>
6. <span data-ttu-id="9cd14-119">Perakende ve ticaret > Kanal kurulumu > Satış vergileri > Satış vergisi geçersiz kılma işlemlerine gidin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="9cd14-120">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-120">Click New.</span></span>
8. <span data-ttu-id="9cd14-121">Satış vergisi geçersiz kılma alanında yeni geçersiz kılma işleminize bir ad verin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="9cd14-122">Açıklama alanında geçersiz kılma işleminin bir açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="9cd14-123">Durumu "Etkinleştir" olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="9cd14-124">Geçersiz Kıl bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="9cd14-125">Tür alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="9cd14-126">Madde satış vergisi grubu, gruba ait olan belirli maddeler için vergileri geçersiz kılmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="9cd14-127">Örneğin, yiyecek maddeleri genellikle bozulmaz mallardan farklı olarak vergilendirilir ve büyük ihtimalle kendilerine ait satış vergisi grubu vardır.</span><span class="sxs-lookup"><span data-stu-id="9cd14-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="9cd14-128">Satış vergisi grupları, belirli bir kanala uygulanabilir vergilerin gruplarıdır.</span><span class="sxs-lookup"><span data-stu-id="9cd14-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="9cd14-129">Örneğin, bir kanal hem perakende hem de işletmeler arası satış yapıyorsa, farklı maddelerin satış vergisi grupları kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="9cd14-130">Uygulanabilir tüm vergiler satış vergisi grubuna eşlenebilir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="9cd14-131">Şimdi satış vergisi geçersiz kılma işleminizi oluşturmak için "Kimden" ve "Kime" vergilerini veya "İlk vergi grubu" ve "Son vergi grubu" öğesini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9cd14-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="9cd14-132">"Kimden" alanı, geçersiz kılınacak vergi veya vergi grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="9cd14-133">Madde satış vergisi grubunu geçersiz kılma işlemi, satış vergisi grubuna göre geçersiz kılma işleminden farklı seçenekler sunar.</span><span class="sxs-lookup"><span data-stu-id="9cd14-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="9cd14-134">Satış vergisi geçersiz kılma işlemleri, vergileri tüm işlemler veya işlemde belirli satırlar üzerinde geçersiz kılacak şekilde ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="9cd14-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="9cd14-135">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-135">Click Save.</span></span>
14. <span data-ttu-id="9cd14-136">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-136">Close the page.</span></span>
15. <span data-ttu-id="9cd14-137">Perakende ve ticaret > Kanal kurulumu > Satış vergileri > Satış vergisi geçersiz kılma grupları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="9cd14-138">Bu adımda, Houston kanalına atanmış satış vergisi geçersiz kılma grubuna yeni oluşturulan satış vergisi geçersiz kılma işlemi atayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="9cd14-139">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-139">Click Edit.</span></span>
17. <span data-ttu-id="9cd14-140">Kurulum bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="9cd14-141">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-141">Click Add.</span></span>
19. <span data-ttu-id="9cd14-142">Satış vergisi geçersiz kılma alanında, aramayı açmak için açılır düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9cd14-143">Listeden, önceden oluşturulan satış vergisi geçersiz kılma işlemini seçin.</span><span class="sxs-lookup"><span data-stu-id="9cd14-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="9cd14-144">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="9cd14-145">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9cd14-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]