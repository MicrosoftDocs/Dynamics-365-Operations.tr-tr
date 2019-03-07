---
title: Stok etiket sayımı
description: Bu makalede, ambardaki mevcut içeriği eldeki stokla karşılaştırmak için kullanabileceğiniz etiket sayımı hakkında bilgiler verilmektedir.
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dff899d0e6d94287c0f1924fe1787189d79c09f4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "328965"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="fbb03-103">Stok etiket sayımı</span><span class="sxs-lookup"><span data-stu-id="fbb03-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="fbb03-104">Bu makalede, ambardaki mevcut içeriği eldeki stokla karşılaştırmak için kullanabileceğiniz etiket sayımı hakkında bilgiler verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="fbb03-104">This article provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="fbb03-105">**Etiket sayımı** sayfasında satırlar oluşturarak, her bir stok maddesine bir etiket numarası verirsiniz, örneğin 1-500 arasında.</span><span class="sxs-lookup"><span data-stu-id="fbb03-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="fbb03-106">Sayım sırasında, karşılık gelen bir etikette madde numarasını ve miktarı girersiniz.</span><span class="sxs-lookup"><span data-stu-id="fbb03-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="fbb03-107">Bunun üzerine, bu etiket, etiket sayım günlüğü girişi için temel olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="fbb03-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="fbb03-108">Siz etiket sayımı günlüğünü naklettikten sonra, **Sayım** sayfasında yeni bir sayım günlüğü oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="fbb03-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="fbb03-109">Yeni günlük, oluşturduğunuz etiket sayım günlüğü satırlarını temel alır.</span><span class="sxs-lookup"><span data-stu-id="fbb03-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="fbb03-110">Maddeleri belirli bir stok boyutuna göre etiket sayımına tabi tutmak için, etiket sayım günlüğünü oluşturduğunuz zaman görüntülenen **Boyutu görüntüle** sayfasında boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="fbb03-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="fbb03-111">Örneğin, belirli bir ambardaki maddeleri saymak için **Ambar** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="fbb03-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="fbb03-112">**Stok ve ambar yönetim parametreleri** sayfasındaki **Sayım sırasında madde kilitlemesi** sürgüsü seçilirse, sayım sırasında maddeler fiziksel olarak güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="fbb03-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="fbb03-113">Ancak, etiket sayım günlüklerindeki maddeler etiket sayımı sırasında kilitlenmez.</span><span class="sxs-lookup"><span data-stu-id="fbb03-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="fbb03-114">Etiket sayım satırları deftere nakil sırasında sayım günlüğüne aktarılana kadar stok hareketleri oluşturulmaz.</span><span class="sxs-lookup"><span data-stu-id="fbb03-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="fbb03-115">Etiketler rastgele girilirse ve eksik etiketleri belirlemek isterseniz, satırları etikete göre sıralamak için **Etiket** sütun başlığına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fbb03-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

<a name="additional-resources"></a><span data-ttu-id="fbb03-116">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="fbb03-116">Additional resources</span></span>
--------

[<span data-ttu-id="fbb03-117">Döngü sayımı</span><span class="sxs-lookup"><span data-stu-id="fbb03-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
