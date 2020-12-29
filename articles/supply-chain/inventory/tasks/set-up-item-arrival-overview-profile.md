---
title: Madde varışı genel bakış profili ayarlama
description: Bu konu bir varış genel bakış profili kurulumu üzerinde odaklanır.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69389dd3a53ffec11116e16512bd038b45eda4d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439556"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="d02e4-103">Madde varışı genel bakış profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="d02e4-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="d02e4-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="d02e4-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="d02e4-105">Bu konu bir varış genel bakış profili kurulumu üzerinde odaklanır.</span><span class="sxs-lookup"><span data-stu-id="d02e4-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="d02e4-106">Varış genel bakış profili, varış genel bakışı kullanıcı tarafından açıldığında uygulanacak kurallar topluluğudur.</span><span class="sxs-lookup"><span data-stu-id="d02e4-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="d02e4-107">Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d02e4-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="d02e4-108">Bu yordam genel olarak bir teslim alma memuru tarafından yerine getirilir.</span><span class="sxs-lookup"><span data-stu-id="d02e4-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="d02e4-109">Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Dağıtım > Varış genel bakış profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="d02e4-110">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-110">Select **New**.</span></span> <span data-ttu-id="d02e4-111">Neredeyse her zaman aynı ambarda tam kamyon yükleri boşaltmakla uğraşacağınız için, alınan maddelerin kayıt işlemini basitleştirmek için bir varış genel bakış profilini oluşturmalısınız</span><span class="sxs-lookup"><span data-stu-id="d02e4-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="d02e4-112">**Varış genel bakış profili** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="d02e4-113">**Satırları göster** alanında, bir seçenek seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="d02e4-114">Girişler için gösterilecek satırları seçin:</span><span class="sxs-lookup"><span data-stu-id="d02e4-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="d02e4-115">**Tümü** – Durumuna bakmaksızın tüm satırları gösterin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="d02e4-116">**İşlemde** - İlerlemenin Tamamlandı veya Kısmen olduğu girişlerin satırlarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="d02e4-117">Bu, her satır için miktarın tamamının ya da miktarın bir kısmının bir varış günlüğüne kaydedildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d02e4-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="d02e4-118">**Tamamlanmış değil** - İlerlemenin Hiçbiri veya Kısmen olduğu girişlerin satırlarını gösterin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="d02e4-119">Bu, her satır için bir varış günlüğüne miktarın hiçbir kısmının kaydedilmediği ya da yalnızca bir kısmının kaydedildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="d02e4-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="d02e4-120">**Varış seçenekleri** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="d02e4-121">**İleriye doğru gün** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="d02e4-122">Bu, sonraki birkaç gün içinde (ayarladığınız sayıya bağlı olarak) alınması beklenen alış irsaliyesi satırlarını göstermek için bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d02e4-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="d02e4-123">**Geriye doğru gün** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="d02e4-124">Bu, bugünden belir bir sayıdaki gün önce alınmış olması beklenen ürün girişi satırlarını gösteren bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d02e4-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="d02e4-125">**Ambarlar** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="d02e4-126">Bir ya da birden fazla fazla ambarı filtreleyin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="d02e4-127">**Teslimat şekli** alanında bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="d02e4-128">Bu, yalnızca bu teslimat şekli ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d02e4-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="d02e4-129">**Ad** alanında WHS'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="d02e4-130">**Ambar** alanında ambar 24'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="d02e4-131">Bu, bu profili kullan kayıtlı alış irsaliyesi satırları için kullanılacak varsayılan ambardır.</span><span class="sxs-lookup"><span data-stu-id="d02e4-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="d02e4-132">**Konum** alanında **Baydoor**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="d02e4-133">Bu, bu profildeki kayıtlı giriş irsaliyesi satırları için kullanılacak varsayılan konumdur.</span><span class="sxs-lookup"><span data-stu-id="d02e4-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="d02e4-134">**Varış sorgusu ayrıntıları** bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="d02e4-135">**Tesisle kısıtla** alanında konum 2'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="d02e4-136">Bu, yalnızca bu tesis ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d02e4-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="d02e4-137">**Satın alma siparişleri** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="d02e4-138">Satınalma siparişlerinden alış irsaliyesi satırlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="d02e4-139">**Transfer** emirleri seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="d02e4-140">Transfer emirlerinden alış irsaliyesi satırlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="d02e4-141">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d02e4-141">Select **Save**.</span></span>
18. <span data-ttu-id="d02e4-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d02e4-142">Close the page.</span></span>

