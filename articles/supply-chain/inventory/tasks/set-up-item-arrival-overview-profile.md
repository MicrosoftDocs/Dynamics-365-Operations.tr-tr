---
title: Madde varışı genel bakış profili ayarlama
description: Bu görev bir varış genel bakış profili kurulumu üzerinde odaklanır.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b61d77072358083a35de28003176cb88e53453e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "338027"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="1c437-103">Madde varışı genel bakış profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="1c437-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c437-104">Bu görev bir varış genel bakış profili kurulumu üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="1c437-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="1c437-105">Varış genel bakış profili, varış genel bakışı kullanıcı tarafından açıldığında uygulanacak kurallar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="1c437-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="1c437-106">Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1c437-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="1c437-107">Bu yordam genel olarak bir teslim alma memuru tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="1c437-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="1c437-108">Stok yönetimi > Kurulum > Dağıtım > Varış genel bakış profilleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="1c437-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="1c437-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c437-109">Click New.</span></span>
    * <span data-ttu-id="1c437-110">Neredeyse her zaman aynı ambarda tam kamyon yükleri boşaltmakla uğraşacağınız için, alınan maddelerin kayıt işlemini basitleştirmek için bir varış genel bakış profilini oluşturmalısınız</span><span class="sxs-lookup"><span data-stu-id="1c437-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="1c437-111">Varış genel bakış profili alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1c437-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="1c437-112">Satırları göster alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="1c437-113">Makbuzlar için hangi satırların gösterileceğini seçin:   Tümü – durumu ne olursa olsun tüm satırları göster.</span><span class="sxs-lookup"><span data-stu-id="1c437-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="1c437-114">İşlemde - İlerlemenin Tamamlandı veya Kısmen olduğu girişlerin satırlarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="1c437-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="1c437-115">Bu, her satır için miktarın tamamının ya da miktarın bir kısmının bir varış günlüğüne kaydedildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1c437-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="1c437-116">Tamamlanmış değil - İlerlemenin Hiçbiri veya Kısmen olduğu girişlerin satırlarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="1c437-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="1c437-117">Bu, her satır için bir varış günlüğüne miktarın hiçbir kısmının kaydedilmediği ya da yalnızca bir kısmının kaydedildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="1c437-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="1c437-118">Varış seçenekleri bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="1c437-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="1c437-119">İleriye doğru gün alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1c437-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="1c437-120">Bu, sonraki birkaç gün içinde (ayarladığınız sayıya bağlı olarak) alınması beklenen alış irsaliyesi satırlarını göstermek için bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c437-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="1c437-121">Geriye doğru gün alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1c437-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="1c437-122">Bu, bugünden belir bir sayıdaki gün önce alınmış olması beklenen ürün girişi satırlarını gösteren bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c437-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="1c437-123">Ambarlar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="1c437-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="1c437-124">Bir ya da birden fazla fazla ambarı filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="1c437-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="1c437-125">Teslimat şekli alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="1c437-126">Bu, yalnızca bu teslimat şekli ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c437-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="1c437-127">Ad alanında WHS'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="1c437-128">Ambar alanında ambar 24'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="1c437-129">Bu, bu profili kullan kayıtlı alış irsaliyesi satırları için kullanılacak varsayılan ambardır.</span><span class="sxs-lookup"><span data-stu-id="1c437-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="1c437-130">Konum alanında Baydoor'u seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="1c437-131">Bu, bu profildeki kayıtlı giriş irsaliyesi satırları için kullanılacak varsayılan konumdur.</span><span class="sxs-lookup"><span data-stu-id="1c437-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="1c437-132">Varış sorgusu ayrıntıları bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="1c437-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="1c437-133">Tesisle kısıtla alanında konum 2'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="1c437-134">Bu, yalnızca bu tesis ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c437-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="1c437-135">Satın alma siparişleri seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1c437-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="1c437-136">Satınalma siparişlerinden alış irsaliyesi satırlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="1c437-137">Transfer emirleri seçeneğini Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1c437-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="1c437-138">Transfer emirlerinden alış irsaliyesi satırlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="1c437-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="1c437-139">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1c437-139">Click Save.</span></span>
18. <span data-ttu-id="1c437-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="1c437-140">Close the page.</span></span>

