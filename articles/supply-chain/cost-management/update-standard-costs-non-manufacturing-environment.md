---
title: Standart maliyetleri imalat dışı bir ortamda güncelleme
description: Bu makalede, imalat dışı bir ortamda standart maliyetlerin güncellenmesine yönelik yönergeler sağlanmıştır.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dca3012952b739a75a6930908752fba73a4550
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214125"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="c1d16-103">Standart maliyetleri imalat dışı bir ortamda güncelleme</span><span class="sxs-lookup"><span data-stu-id="c1d16-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1d16-104">Bu makalede, imalat dışı bir ortamda standart maliyetlerin güncellenmesine yönelik yönergeler sağlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="c1d16-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="c1d16-105">Aşağıdaki yönergelerde, standart maliyeti iki sürümlü bir yaklaşım kullanarak güncellediğiniz varsayılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c1d16-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="c1d16-106">Bu yaklaşımda bir maliyet sürümü orijinal olarak donmuş dönem için tanımlanmış olan standart maliyetleri, ikinci maliyetlendirme sürümü ise artımlı güncellemeleri içerir.</span><span class="sxs-lookup"><span data-stu-id="c1d16-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="c1d16-107">Her güncelleme, ikinci maliyetlendirme sürümüne alınmış bir maliyet kaydı olarak girilir ve nihayetinden etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c1d16-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="c1d16-108">Bir alternatif, orijinal olarak tanımlanmış olan standart maliyetler kümesini kullanan tek sürümlü yaklaşımdır.</span><span class="sxs-lookup"><span data-stu-id="c1d16-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="c1d16-109">İki sürümlü yaklaşım ikinci bir maliyetlendirme sürümü tanımlamanızı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="c1d16-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="c1d16-110">Bu maliyetlendirme sürümünü tanımlamaya yönelik yönergeler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="c1d16-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="c1d16-111">Bir **Standart maliyetler** maliyetlendirme türü atayın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="c1d16-112">Maliyetlendirme sürümünün içeriklerini belirtmek için **2016-UPDATES** gibi anlamlı bir tanımlayıcı atayın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="c1d16-113">İçeriklerin maliyet kayıtlarını içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="c1d16-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="c1d16-114">Maliyet kayıtlarının tüm tesisler için girilmesine izin verin.</span><span class="sxs-lookup"><span data-stu-id="c1d16-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="c1d16-115">Bir tesis belirtirseniz, maliyet kayıtları yalnızca o tesis için girilebilir.</span><span class="sxs-lookup"><span data-stu-id="c1d16-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="c1d16-116">Geri dönüş ilkesini **Hiç** olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="c1d16-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="c1d16-117">Geri dönül ilkesi yalnızca mamul maddelere yönelik maliyet hesaplamaları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c1d16-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="c1d16-118">Yeni maddeler için standart maliyetleri düzeltmek, ayarlamak veya güncellemek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1d16-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="c1d16-119">Maliyet verilerinin ikinci maliyetlendirme sürümüne girilebilmesini sağlamak için **Maliyetlendirme sürümü** **ayarlar** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="c1d16-120">İsteğe bağlı olarak, bekleyen maliyetlerin etkinleştirilmesini önleyin, böylelikle etkinleştirme bekleyen maliyetler tamamen ve doğru şekilde tanımlandıktan sonra mümkün olacaktır.</span><span class="sxs-lookup"><span data-stu-id="c1d16-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="c1d16-121">Ayrıca isteğe bağlı olarak **Başlangıç tarihi** alanına bir tarih de girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d16-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="c1d16-122">Genel bir yönerge olarak, artımlı güncellemelere izin vermek istediğinizde tarih kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="c1d16-123">Alternatif olarak **Başlangıç tarihi** alanını maliyetlendirme sürümü için boş bırakın ve ardından her bir maliyet kaydı için **Başlangıç tarihi** alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="c1d16-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="c1d16-124">Güncellemeleri ikinci maliyetlendirme sürümüne alınmış madde maliyet kayıtları olarak girmek için **Madde fiyatı** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="c1d16-125">İkinci maliyetlendirme sürümüne alınmış madde maliyet kayıtlarının tam ve doğruluğunu doğrulamak için **Madde fiyatları** raporunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="c1d16-126">İkinci maliyetlendirme sürümüne alınmış bekleyen maliyet kayıtlarının etkinleştirilmesine izin vermek için engelleme bayrağını değiştirmek üzere **Maliyetlendirme sürüm bakımı** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="c1d16-127">İkinci maliyetlendirme sürümüne alınmış tüm bekleyen madde maliyet kayıtlarını etkinleştirmek için **Etkin fiyatlar** sayfasını (**Maliyetlendirme sürüm bakımı** sayfasından açabilirsiniz) kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1d16-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="c1d16-128">Tek tek maddelere yönelik bekleyen maliyet kayıtlarını **Madde fiyatı** sayfasında **Bekleyen fiyatı etkinleştir** düğmesine tıklayarak da etkinleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1d16-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="c1d16-129">Ek veri bakımını önlemek için, **Maliyetlendirme sürümü ayarları** sayfasını kullanarak ikinci maliyetlendirme sürümüne alınmış engelleme bayraklarını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="c1d16-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="c1d16-130">Durdurma ilkeleri yeni bekleyen maliyetler girilmesini ve bekleyen maliyetlerin etkinleştirilmesini önler.</span><span class="sxs-lookup"><span data-stu-id="c1d16-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>




