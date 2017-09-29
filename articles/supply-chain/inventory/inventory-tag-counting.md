---
title: "Stok etiket sayımı"
description: "Bu makalede, ambardaki mevcut içeriği eldeki stokla karşılaştırmak için kullanabileceğiniz etiket sayımı hakkında bilgiler verilmektedir."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 9e129fda638cfd8cff0e40079747f7ca70fa7531
ms.contentlocale: tr-tr
ms.lasthandoff: 09/12/2017

---

# <a name="inventory-tag-counting"></a><span data-ttu-id="6524a-103">Stok etiket sayımı</span><span class="sxs-lookup"><span data-stu-id="6524a-103">Inventory tag counting</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="6524a-104">Bu makalede, ambardaki mevcut içeriği eldeki stokla karşılaştırmak için kullanabileceğiniz etiket sayımı hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6524a-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="6524a-105">**Etiket sayımı** sayfasında satırlar oluşturarak, her bir stok maddesine bir etiket numarası verirsiniz, örneğin 1-500 arasında.</span><span class="sxs-lookup"><span data-stu-id="6524a-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="6524a-106">Sayım sırasında, karşılık gelen bir etikette madde numarasını ve miktarı girersiniz.</span><span class="sxs-lookup"><span data-stu-id="6524a-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="6524a-107">Bunun üzerine, bu etiket, etiket sayım günlüğü girişi için temel olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6524a-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="6524a-108">Siz etiket sayımı günlüğünü naklettikten sonra, **Sayım** sayfasında yeni bir sayım günlüğü oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6524a-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="6524a-109">Yeni günlük, oluşturduğunuz etiket sayım günlüğü satırlarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="6524a-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="6524a-110">Maddeleri belirli bir stok boyutuna göre etiket sayımına tabi tutmak için, etiket sayım günlüğünü oluşturduğunuz zaman görüntülenen **Boyutu görüntüle** sayfasında boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="6524a-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="6524a-111">Örneğin, belirli bir ambardaki maddeleri saymak için **Ambar** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6524a-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="6524a-112">**Stok ve ambar yönetim parametreleri** sayfasındaki **Sayım sırasında madde kilitlemesi** sürgüsü seçilirse, sayım sırasında maddeler fiziksel olarak güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="6524a-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="6524a-113">Ancak, etiket sayım günlüklerindeki maddeler etiket sayımı sırasında kilitlenmez.</span><span class="sxs-lookup"><span data-stu-id="6524a-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="6524a-114">Etiket sayım satırları deftere nakil sırasında sayım günlüğüne aktarılana kadar stok hareketleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="6524a-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="6524a-115">Etiketler rastgele girilirse ve eksik etiketleri belirlemek isterseniz, satırları etikete göre sıralamak için **Etiket** sütun başlığına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6524a-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="see-also"></a><span data-ttu-id="6524a-116">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="6524a-116">See also</span></span>
--------

[<span data-ttu-id="6524a-117">Döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="6524a-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)

