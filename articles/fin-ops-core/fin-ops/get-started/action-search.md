---
title: Eylem arama
description: Bu makale, eylem arama işlevini açıklar. Eylem arama, bir sayfadaki eylemleri bulmanıza ve çalıştırmanıza yardımcı olur.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 62303
ms.assetid: 62c70de0-fdde-4417-8e08-0583fb095a40
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b5d2e678b01f052db29d5a1c47eae27d27cd04f
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694200"
---
# <a name="action-search"></a><span data-ttu-id="6d6f6-104">Eylem arama</span><span class="sxs-lookup"><span data-stu-id="6d6f6-104">Action search</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d6f6-105">Bu makale, eylem arama işlevini açıklar.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-105">This article describes the action search functionality.</span></span> <span data-ttu-id="6d6f6-106">Eylem arama, bir sayfadaki eylemleri bulmanıza ve çalıştırmanıza yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-106">Action search will help you find and run actions on a page.</span></span>

## <a name="introduction"></a><span data-ttu-id="6d6f6-107">Giriş</span><span class="sxs-lookup"><span data-stu-id="6d6f6-107">Introduction</span></span>

<span data-ttu-id="6d6f6-108">Sayfalar, başlıca Eylem Panoları üzerindeki komutları ortaya çıkartır: sayfanın üzerinde görünen standart Eylem Panosu ve sayfanın çeşitli yerlerinde görünen araç çubukları.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-108">Pages primarily expose commands on Action Panes, both the standard Action Pane that appears at the top of a page and the toolbars that appear in various sections of the page.</span></span> <span data-ttu-id="6d6f6-109">Önceki sürümlerde, Anahtar İpuçları özelliği, Eylem Panosu üzerindeki herhangi bir düğmeye, Alt tuşu ve daha sonra bir dizi harfe basarak hızla erişmenize izin veriyordu.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-109">In previous versions, a Key Tips feature let you quickly access any button on an Action Pane by pressing the Alt key and then a series of letters.</span></span>

<span data-ttu-id="6d6f6-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-110">[![keyTipsAX6](./media/keytipsax6.png)](./media/keytipsax6.png)</span></span>

<span data-ttu-id="6d6f6-111">Anahtar İpuçları artık kullanılamaz, ancak yerine eylem arama özelliği getirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-111">Key Tips are no longer available but have been replaced by the action search feature.</span></span> <span data-ttu-id="6d6f6-112">Bu yeni özellik, görünen herhangi bir Eylem Bölmesinden bir düğmeyi hızla aramanıza ve düğmeyi çalıştırmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-112">This new feature lets you quickly search for and run a button from any visible Action Pane.</span></span>

## <a name="using-action-search"></a><span data-ttu-id="6d6f6-113">Eylem aramasını kullanma</span><span class="sxs-lookup"><span data-stu-id="6d6f6-113">Using action search</span></span>

<span data-ttu-id="6d6f6-114">Eylem arama özelliğini kullanmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-114">To use the action search feature, follow these steps.</span></span>

1. <span data-ttu-id="6d6f6-115">Eylem bölmesinde, **eylem arama** alanına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-115">On the Action Pane, click in the **action search** field.</span></span> <span data-ttu-id="6d6f6-116">(**Eylem arama** alanı bir büyüteç simgesi içerir.)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-116">(The **action search** field contains a magnifying glass icon.)</span></span>
2. <span data-ttu-id="6d6f6-117">Çalıştırmak istediğiniz düğmenin adının tamamını veya bir kısmını yazın.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-117">Type all or part of the name of the button that you want to run.</span></span> <span data-ttu-id="6d6f6-118">Düğmenin "yolu" üzerindeki kelimeleri de kullanarak arayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-118">You can also search by using words from the button's "path."</span></span> <span data-ttu-id="6d6f6-119">(Daha fazla bilgi için, bu makalenin sonraki bölümüne bakın.) Genellikle bir düğme, siz iki - dört karakter arasında yazdığınızda sonuç listesinin üstüne yakın bir yerde görünür.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-119">(For more information, see the next section of this article.) Typically, a button will appear near the top of the results list after you've typed two to four characters.</span></span>
3. <span data-ttu-id="6d6f6-120">Sonuçlar listesinde (fare ya da klavyenizi kullanarak) düğmeyi bulun ve çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-120">Find and run the button in the results list (by using your mouse or keyboard).</span></span>

<span data-ttu-id="6d6f6-121">Düğmeyi çalıştırdıktan sonra, çalışmaya devam edebilmeniz için sayfadaki son konumunuz yeniden ön plana geçer.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-121">After the button is run, the focus is returned to your last position on the page, so that you can continue to work.</span></span>

<span data-ttu-id="6d6f6-122">[![eylem-arama-alanı](./media/action-search-field.png)](./media/action-search-field.png)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-122">[![action-search-field](./media/action-search-field.png)](./media/action-search-field.png)</span></span>

<span data-ttu-id="6d6f6-123">Eylem aramasını Ctrl+/ veya Alt+Q tuşuna basarak da başlatabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-123">You can also start action search by pressing Ctrl+/ or Alt+Q.</span></span> <span data-ttu-id="6d6f6-124">Sayfadaki son konumunuzu yeniden ön plana almak için klavye kısayoluna tekrar basın.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-124">Press the keyboard shortcut again to return the focus to your last position on the page.</span></span>

## <a name="understanding-the-results-list"></a><span data-ttu-id="6d6f6-125">Sonuç listesini anlama</span><span class="sxs-lookup"><span data-stu-id="6d6f6-125">Understanding the results list</span></span>

<span data-ttu-id="6d6f6-126">Bir düğmenin amacını tamamen anlamak için çoğu zaman bu düğmenin hem konumunu hem de bağlamını bilmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-126">Often, you must know both the location and the context of a button to fully understand the purpose of that button.</span></span> <span data-ttu-id="6d6f6-127">Bu nedenle, size tam olarak hangi düğmenin listede göründüğünü anlamanıza yardımcı olmak için her bir öğe için ek bilgiler sonuç sayfasında görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-127">Therefore, additional information is shown for each item in the results list, to help you understand exactly which buttons appear in the list.</span></span> <span data-ttu-id="6d6f6-128">Özellikle, düğmenin "yol"u gösterilir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-128">In particular, the "path" of the button is shown.</span></span> <span data-ttu-id="6d6f6-129">Bu yol, ilgili olarak, aşağıdaki Kullanıcı Arabirimi öğelerini içerebilir:</span><span class="sxs-lookup"><span data-stu-id="6d6f6-129">This path might include the labels of the following UI elements, as relevant:</span></span>

- <span data-ttu-id="6d6f6-130">Eylem Bölmesi öğesi</span><span class="sxs-lookup"><span data-stu-id="6d6f6-130">Action Pane tab</span></span>
- <span data-ttu-id="6d6f6-131">Düğme grubu</span><span class="sxs-lookup"><span data-stu-id="6d6f6-131">Button group</span></span>
- <span data-ttu-id="6d6f6-132">Menü düğmesi (düğme bir menü düğmesi içinde ise)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-132">Menu button (if the button is inside a menu button)</span></span>
- <span data-ttu-id="6d6f6-133">Menü ayırıcı (düğme bir menü düğmesi içindeki adlandırılmış bir grup içinde ise)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-133">Menu separator (if the button is inside a named group inside a menu button)</span></span>
- <span data-ttu-id="6d6f6-134">Sayfadaki grup veya öğe (örneğin, bir Hızlı Sekmenin adı)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-134">Group or tab on the page (for example, the name of a FastTab)</span></span>

<span data-ttu-id="6d6f6-135">Örneğin, **eylem arama** alanına **top** yazdınız ve şimdi sonuçlar listesini inceliyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-135">For example, you typed **tot** in the **action search** field and are now examining the results list.</span></span> <span data-ttu-id="6d6f6-136">Bir düğme için ilk girişte **Toplamlar** adına sahiptir ve vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-136">The first entry, for a button that is named **Totals**, is highlighted.</span></span> <span data-ttu-id="6d6f6-137">**Satış siparişi** &gt; **Görünüm** düğme yolu da gösterilir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-137">A button path of **Sales order** &gt; **View** is also shown.</span></span> <span data-ttu-id="6d6f6-138">Yolun **Satış siparişi** parçasına karşılık gelen **Satış siparişi** sekmesi, Eylem bölmesinde ve yolun **Görüntüle** parçasına karşılık gelen o sekmede **Görüntüle** grubunda. Benzer şekilde **Toplam indirim** düğmesi (**Sat** &gt; **Hesapla**), bu düğmenin **Hesapla** grubunda, Eylem bölmesinin **Sat** sekmesinde olduğunu size belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-138">The **Sales order** part of the path corresponds to the **Sales order** tab on the Action Pane, and the **View** part of the path corresponds to the **View** group on that tab. Similarly, the path of the **Total discount** button (**Sell** &gt; **Calculate**) informs you that this button is located in the **Calculate** group on the **Sell** tab of the Action Pane.</span></span> <span data-ttu-id="6d6f6-139">Bu nedenle, bu bilgi size tam olarak hangi düğmenin hangi eylem arama tarafından tetiklendiğini anlamanıza yardımcı olur (düğmeyi sonuç listesinden seçerseniz).</span><span class="sxs-lookup"><span data-stu-id="6d6f6-139">Therefore, this information helps you understand exactly which button will be triggered by action search (if you select that button in the results list).</span></span>

<span data-ttu-id="6d6f6-140">[![eylem-arama-alan-ile-veri](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-140">[![action-search-field-with-data](./media/action-search-field-with-data.png)](./media/action-search-field-with-data.png)</span></span>

<span data-ttu-id="6d6f6-141">Önceki örnekte, eylem arama bir sayfanın en üstündeki standart Eylem Bölmesi'nden sonuçları göstermiştir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-141">In the previous example, action search showed results from the standard Action Pane at the top of a page.</span></span> <span data-ttu-id="6d6f6-142">Bununla birlikte, eylem arama sayfada başka yerlerde bulunan görünür araç çubuklarından sonuçları da gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-142">However, action search also shows results from visible toolbars that are located in other places on the page.</span></span> <span data-ttu-id="6d6f6-143">Örneğin **Satış siparişleri satırı** hızlı sekmesi üzerindeki **Eldeki stok** düğmesini arıyorsanız.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-143">For example, you're searching for the **On-hand inventory** button that is located on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="6d6f6-144">Bu durumda, sonuç sayfasındaki düğme yolu (**Satış siparişi satırları** &gt; **Stok** &gt; **Görünüm**), bu düğmenin **Satış siparişleri satırları** hızlı sekmesi üzerindeki **Stok** menü düğmesindeki **Görünüm** başlığı altında bulunduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-144">In this case, the button path in the results list (**Sales order lines** &gt; **Inventory** &gt; **View**) informs you that this button is located under the **View** heading on the **Inventory** menu button on the **Sales order lines** FastTab.</span></span>

<span data-ttu-id="6d6f6-145">[![eldeki-stok](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span><span class="sxs-lookup"><span data-stu-id="6d6f6-145">[![on-hand-inventory](./media/on-hand-inventory.png)](./media/on-hand-inventory.png)</span></span>

> [!NOTE]
> <span data-ttu-id="6d6f6-146">Eylem aramasında gösterilmeyen bazı düğmeler vardır.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-146">There are some buttons that do not show up in Action search.</span></span> <span data-ttu-id="6d6f6-147">Bunlar açılır iletişim kutusu düğmelerini ve alt formlardaki düğmeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-147">These include drop dialog buttons and buttons from subforms.</span></span> 

## <a name="action-search-vs-navigation-search"></a><span data-ttu-id="6d6f6-148">Eylem arama - Gezinti arama karşılaştırması</span><span class="sxs-lookup"><span data-stu-id="6d6f6-148">Action search vs. Navigation search</span></span>

<span data-ttu-id="6d6f6-149">Eylem arama ile bir sayfadaki eylemleri bulup çalıştırma amaçlanırken, sayfaları bulup gezinmek için ayrı bir arama mekanizması bulunur.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-149">Whereas action search is intended to find and run actions on a page, there is a separate search mechanism for finding and navigating to pages.</span></span> <span data-ttu-id="6d6f6-150">Bu özellik hakkında daha fazla bilgi için, bkz. [Gezinti arama](navigation-search.md) makalesi.</span><span class="sxs-lookup"><span data-stu-id="6d6f6-150">For more information about that feature, see the [Navigation search](navigation-search.md) article.</span></span>
