---
title: "Bilgi bulmak için aramaları kullanma"
description: "Microsoft Dynamics 365 for Finance and Operations'taki birçok alanda, doğru veya istediğiniz değeri bulmanıza yardımcı olabilecek aramalar vardır. Bu denetimleri daha kullanışlı hale getiren ve kullanıcıları daha üretken hale getiren aramalara çeşitli geliştirmeler eklendi. Bu konuda, bu yeni arama özellikleri hakkında bilgi edineceksiniz ve sistemdeki aramalardan en iyi sonucu almak için bazı yararlı ipuçları edineceksiniz."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 269934
ms.assetid: f20cbd2c-14e0-47e7-b351-8e60d3537f96
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6c3499e483331eeef88e65f5f3bf1288dd71b268
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="use-lookups-to-find-information"></a><span data-ttu-id="850be-105">Bilgi bulmak için aramaları kullanma</span><span class="sxs-lookup"><span data-stu-id="850be-105">Use lookups to find information</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="850be-106">Microsoft Dynamics 365 for Finance and Operations'taki birçok alanda, doğru veya istediğiniz değeri bulmanıza yardımcı olabilecek aramalar vardır.</span><span class="sxs-lookup"><span data-stu-id="850be-106">In Microsoft Dynamics 365 for Finance and Operations, many fields have lookups that can help you easily find the correct or desired value.</span></span> <span data-ttu-id="850be-107">Bu denetimleri daha kullanışlı hale getiren ve kullanıcıları daha üretken hale getiren aramalara çeşitli geliştirmeler eklendi.</span><span class="sxs-lookup"><span data-stu-id="850be-107">Several enhancements have been added to lookups that make these controls more usable and make users more productive.</span></span> <span data-ttu-id="850be-108">Bu konuda, bu yeni arama özellikleri hakkında bilgi edineceksiniz ve sistemdeki aramalardan en iyi sonucu almak için bazı yararlı ipuçları edineceksiniz.</span><span class="sxs-lookup"><span data-stu-id="850be-108">In this topic, you will learn about these new lookup features and will receive some helpful tips to get the optimal use out of lookups in the system.</span></span>  

<a name="responsive-lookups"></a><span data-ttu-id="850be-109">Duyarlı aramalar</span><span class="sxs-lookup"><span data-stu-id="850be-109">Responsive lookups</span></span>
------------------

<span data-ttu-id="850be-110">Finance and Operations'ın önceki sürümlerinde, bir arama denetimiyle etkileşim kurarken, kullanıcının açılır menüyü açmak için açık bir eylem yapması gerekir.</span><span class="sxs-lookup"><span data-stu-id="850be-110">In previous versions of Finance and Operations, when interacting with a lookup control, a user would have to take an explicit action to open the drop-down menu.</span></span> <span data-ttu-id="850be-111">Bu, denetimin geçerli değerine göre aramayı filtrelemek için denetimde bir yıldız (\*) yazarak, açılır menü düğmesine tıklayarak veya **Alt**+**Aşağı ok** klavye kısayollarını kullanarak yapılmış olabilir</span><span class="sxs-lookup"><span data-stu-id="850be-111">This may have been by typing an asterisk (\*) in the control to filter the lookup based on the current value of the control, clicking the drop-down button, or by using the **Alt**+**Down arrow** keyboard shortcut.</span></span> <span data-ttu-id="850be-112">Arama denetimleri, geçerli web uygulamalarıyla daha uyumlu olması için aşağıdaki şekilde değiştirildi:</span><span class="sxs-lookup"><span data-stu-id="850be-112">Lookup controls have been modified in the following ways to better align with current web practices:</span></span>

-   <span data-ttu-id="850be-113">Arama açılır menüleri artık yazarken hafif bir duraklamadan sonra otomatik olarak açılır ve içerikleri arama denetiminin değerine göre filtrelenmiş haldedir.</span><span class="sxs-lookup"><span data-stu-id="850be-113">Lookup drop-down menus will now open automatically after a slight pause in typing, with the drop-down menu contents filtered based on the lookup control's value.</span></span>
    -   <span data-ttu-id="850be-114">Yıldız işareti (\*) yazdıktan sonra açılır menünün otomatik açıldığı eski davranışın kullanımdan kaldırıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="850be-114">Note that the old behavior of automatic opening of the dropdown after typing an asterisk (\*) has been deprecated.</span></span>
-   <span data-ttu-id="850be-115">Arama açılır menü açıldıktan sonra şunlar olur:</span><span class="sxs-lookup"><span data-stu-id="850be-115">After the lookup drop-down menu has opened, the following will occur:</span></span>
    -   <span data-ttu-id="850be-116">İmleç, denetimin değerinde değişiklik yapmaya devam edebilmeniz için (açılır menüye odaklama yerine) arama denetiminde kalır.</span><span class="sxs-lookup"><span data-stu-id="850be-116">The cursor will stay in the lookup control (instead of focus moving into the drop-down menu) so you can continue to make modifications to the control's value.</span></span> <span data-ttu-id="850be-117">Ancak, kullanıcı açılır menüdeki satırları değiştirmek ve açılır menüdeki geçerli satırı seçmek üzere giriş yapmak için **Yukarı ok**'u ve **Aşağı ok**'u kullanmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="850be-117">However, the user can still use the **Up arrow** and **Down arrow** to change rows in the drop-down menu, and enter to select the current row in the drop-down menu.</span></span>
    -   <span data-ttu-id="850be-118">Arama denetiminin değerinde değişiklik yapıldıktan sonra açılır menünün içeriği ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="850be-118">The contents of the drop-down menu will adjust after any modifications are made to the lookup control's value.</span></span>

<span data-ttu-id="850be-119">Örneğin **Şehir** adlı bir arama alanı düşünün.</span><span class="sxs-lookup"><span data-stu-id="850be-119">For example, consider a lookup field called **City**.</span></span> 

<span data-ttu-id="850be-120">Odak **Şehir** (City) alanındayken, "col" gibi birkaç harf yazarak istediğiniz şehir için arama başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="850be-120">When focus is in the **City** field, you can start looking for the city that you want by typing a few letters, like "col."</span></span>  <span data-ttu-id="850be-121">Siz yazmayı durdurduktan sonra arama "col" ile başlayan şehirler filtre edilerek gösterilmiş halde otomatik olarak açılır.</span><span class="sxs-lookup"><span data-stu-id="850be-121">After you stop typing, the lookup will open automatically, filtered to those cities that begin with "col".</span></span> 

<span data-ttu-id="850be-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span><span class="sxs-lookup"><span data-stu-id="850be-122">[![typeaheadLookupExample](./media/typeaheadlookupexample.png)](./media/typeaheadlookupexample.png)</span></span> 

<span data-ttu-id="850be-123">Bu noktada imleç hala arama alanındadır.</span><span class="sxs-lookup"><span data-stu-id="850be-123">At this point, the cursor is still in the lookup field.</span></span> <span data-ttu-id="850be-124">Değer "colum" olacak şekilde yazmaya devam ederseniz, arama içeriği denetimdeki son değeri yansıtacak şekilde otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="850be-124">If you continue typing so the value is "colum," the lookup contents adjust automatically to reflect the latest value in the control.</span></span> 

![updateFilterLookupExample](./media/updatefilterlookupexample.png) 

<span data-ttu-id="850be-126">Odak arama denetiminde olsa da, seçmek istediğiniz satırı vurgulamak için **Yukarı ok** veya **Aşağı ok** tuşlarını da kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="850be-126">Even though focus is still in the lookup control, you can also use the **Up arrow** or **Down arrow** keys to highlight the row that you want to select.</span></span> <span data-ttu-id="850be-127">**Enter** tuşuna basarsanız, vurgulanmış satır aramada seçilir ve denetimin değeri güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="850be-127">If you press **Enter** the highlighted row will be selected from the lookup and the control's value will be updated.</span></span> 

![changingSelectionLookup](./media/changingselectionlookup.png)

## <a name="typing-in-more-than-ids"></a><span data-ttu-id="850be-129">Koddan daha fazlasını yazma</span><span class="sxs-lookup"><span data-stu-id="850be-129">Typing in more than IDs</span></span>
<span data-ttu-id="850be-130">Veri girerken kullanıcıların, bir varlığı temsil eden bir tanımlayıcı yerine, bir müşteri veya satıcı gibi bir varlığı tanımlamaya çalışması doğaldır.</span><span class="sxs-lookup"><span data-stu-id="850be-130">When entering data, it's natural for users to attempt to identify an entity, such as a customer or vendor, in terms of the name rather than an identifier representing the entity.</span></span> <span data-ttu-id="850be-131">Finance and Operations'ın geçerli sürümünde birçok aramada (tümünde değil) bağlamsal veri girişine artık izin veriliyor.</span><span class="sxs-lookup"><span data-stu-id="850be-131">In the current version of Finance and Operations, many (but not all) lookups now allow contextual data entry.</span></span> <span data-ttu-id="850be-132">Bu güçlü özellik kullanıcının arama denetiminde kodu veya karşılık gelen adı yazmasına izin veriyor.</span><span class="sxs-lookup"><span data-stu-id="850be-132">This powerful feature allows the user to type the ID or the corresponding name into the lookup control.</span></span> 

<span data-ttu-id="850be-133">Örneğin bir satış siparişi oluştururken **Müşteri hesabı** alanını düşünün.</span><span class="sxs-lookup"><span data-stu-id="850be-133">For example, consider the **Customer account** field when creating a sales order.</span></span> <span data-ttu-id="850be-134">Bu alanda müşteri için **Hesap kodu** gösterilir ancak bir kullanıcı satış siparişi oluştururken genellikle **Hesap kodu** yerine **Hesap adı** girmeyi tercih edecektir (örneğin "ABD-003" yerine "Forest Wholesales").</span><span class="sxs-lookup"><span data-stu-id="850be-134">This field shows the **Account ID** for the customer, but a user would typically prefer to enter an **Account name** instead of an **Account ID** for this field when creating a sales order, such as "Forest Wholesales" instead of "US-003."</span></span>

<span data-ttu-id="850be-135">Kullanıcı arama denetimine bir **Hesap kodu** girmeye başladığı zaman açılır menü önceki bölümde açıklandığı şekilde otomatik olarak açılır ve kullanıcı aramayı aşağıda gösterildiği gibi görür.</span><span class="sxs-lookup"><span data-stu-id="850be-135">If the user started to enter an **Account ID** into the lookup control, the drop-down menu would automatically open as described in the previous section and the user would see the lookup as shown below.</span></span>

<span data-ttu-id="850be-136">[![Müşteri hesap kodu girildiğinde bağlamsal arama](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span><span class="sxs-lookup"><span data-stu-id="850be-136">[![Contextual lookup when a customer account ID is entered](./media/howtocontextuallookups-1.png)](./media/howtocontextuallookups-1.png)</span></span>

<span data-ttu-id="850be-137">Ancak, kullanıcı artık bir **Hesap adının** baş kısmını da girebilir.</span><span class="sxs-lookup"><span data-stu-id="850be-137">However, the user can also now enter the beginning of an **Account name** as well.</span></span> <span data-ttu-id="850be-138">Bu algılandığı zaman kullanıcı aşağıdaki aramayı görecektir.</span><span class="sxs-lookup"><span data-stu-id="850be-138">If this is detected, then the user will see the following lookup.</span></span> <span data-ttu-id="850be-139">Aramada **Ad** (Name) sütununun ilk sütun olacak şekilde nasıl taşındığına ve aramanın **Ad** sütununa göre nasıl sıralanıp filtrelendiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="850be-139">Notice how the **Name** column is moved to be the first column in the lookup, and how the lookup is sorted and filtered based on the **Name** column.</span></span>

<span data-ttu-id="850be-140">[![Müşteri adı girildiğinde bağlamsal arama](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span><span class="sxs-lookup"><span data-stu-id="850be-140">[![Contextual lookup when a customer name is entered](./media/howtocontextuallookups-2.png)](./media/howtocontextuallookups-2.png)</span></span>

## <a name="using-grid-column-headers-for-more-advanced-filtering-and-sorting"></a><span data-ttu-id="850be-141">Daha gelişmiş filtreleme ve sıralama için kılavuz sütun başlıklarını kullanma</span><span class="sxs-lookup"><span data-stu-id="850be-141">Using grid column headers for more advanced filtering and sorting</span></span>
<span data-ttu-id="850be-142">Önceki iki bölümde ele alınan arama geliştirmeleri kullanıcının bir aramada **Kod** veya **Alan** alanının "ile başlar" şeklinde aranmasına göre satırlar arasında gezinme yeteneğini büyük ölçüde geliştiriyor.</span><span class="sxs-lookup"><span data-stu-id="850be-142">The lookup enhancements discussed in the previous two sections greatly improve a user's ability to navigate the rows in a lookup based on a "begins with" search of the **ID** or **Name** field in the lookup.</span></span> <span data-ttu-id="850be-143">Bununla birlikte, doğru satırı bulmak için daha gelişmiş filtrelemenin (veya sıralamanın) gerekli olduğu durumlar vardır.</span><span class="sxs-lookup"><span data-stu-id="850be-143">However, there are situations in which more advanced filtering (or sorting) is needed to find the correct row.</span></span> <span data-ttu-id="850be-144">Böyle durumlarda kullanıcının arama içinde kılavuz sütun başlıklarında filtreleme ve sıralama seçeneklerini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="850be-144">In these situations, the user needs to use the filtering and sorting options in the grid column headers inside the lookup.</span></span> <span data-ttu-id="850be-145">Örneğin, bir satış siparişi satırı girerken ürün olarak doğru "kabloyu" bulması gereken bir çalışan düşünün.</span><span class="sxs-lookup"><span data-stu-id="850be-145">For example, consider an employee entering a sales order line who needs to locate the right "cable" as the product.</span></span> <span data-ttu-id="850be-146">"Kablo" ile başlayan ürün adı olmadığı için, **Madde numarası** denetimine "kablo" yazmak yardımcı olmaz.</span><span class="sxs-lookup"><span data-stu-id="850be-146">Typing "cable" into the **Item number** control isn't helpful, as there are no product names that begin with "cable."</span></span> 

![emptyitemlookup](./media/emptyitemlookup.png) 

<span data-ttu-id="850be-148">Bunun yerine, kullanıcı arama denetiminin değerini temizlemeli, arama açılır menüsünü açmalı ve aşağıda gösterildiği gibi ızgara sütun başlığını kullanarak açılır menüyü filtrelemelidir.</span><span class="sxs-lookup"><span data-stu-id="850be-148">Instead, the user needs to clear the value of the lookup control, open the lookup drop-down menu, and filter the drop-down menu using the grid column header, as shown below.</span></span> <span data-ttu-id="850be-149">Bir kullanıcı sütun başlığına fareyle tıklayarak veya dokunarak o sütunun filtreleme ve sıralama seçeneklerine erişebilir.</span><span class="sxs-lookup"><span data-stu-id="850be-149">A mouse (or touch) user can simply click (or touch) any column header to access the filtering and sorting options for that column.</span></span> <span data-ttu-id="850be-150">Klavye kullananlar için, kullanıcının odağı açılır menüye getirmesi için, doğru sütuna gelmek üzere ikinci kez **Alt**+**Aşağı** **oka** basması, ardından **Ctrl**+**G** tuşlarına basarak ızgara sütunu başlığının açılır menüsünü açması gerekir.</span><span class="sxs-lookup"><span data-stu-id="850be-150">For a keyboard user, the user simply needs to press **Alt**+**Down** **arrow** a second time to move focus into the drop-down menu, after which the user can tab to the correct column, and then press **Ctrl**+**G** to open the grid column header drop-down menu.</span></span> 

<span data-ttu-id="850be-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span><span class="sxs-lookup"><span data-stu-id="850be-151">[![gridfilteritemlookup](./media/gridfilteritemlookup.png)](./media/gridfilteritemlookup.png)</span></span> 

<span data-ttu-id="850be-152">Filtre uygulandıktan sonra (aşağıdaki resme bakın) kullanıcı her zamanki gibi satırı bulup seçebilir.</span><span class="sxs-lookup"><span data-stu-id="850be-152">After the filter has been applied (see the image below), the user can find and select the row as usual.</span></span> 

![filtereditemlookup](./media/filtereditemlookup.png)




