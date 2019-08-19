---
title: Bir madde geliş günlüğü kullanılarak temel ambarlama için etkinleştirilen madde için maddeleri kaydetme
description: Bu prosedürde, Stok yönetimi modülündeki "temel depolama" işlevini kullanırken madde varış günlüğüyle maddelerin nasıl kaydedileceğini göreceksiniz.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e64a6df41e43c1b97243a6f7291393982575636
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847243"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="73359-103">Bir madde geliş günlüğü kullanılarak temel ambarlama için etkinleştirilen madde için maddeleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="73359-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73359-104">Bu prosedürde, Stok yönetimi modülündeki "temel depolama" işlevini kullanırken madde varış günlüğüyle maddelerin nasıl kaydedileceğini göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="73359-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="73359-105">Bu genellikle bir teslim alma memuru tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="73359-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="73359-106">Bu prosedürü demo veri şirketi USMF'de, gösterilen örnek değerlerle çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73359-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="73359-107">USMF kullanmıyorsanız, bu kılavuzu başlatmadan önce, elinizde açık bir satınalma siparişi satırı içeren onaylı bir satınalma siparişi bulunması gerekir.</span><span class="sxs-lookup"><span data-stu-id="73359-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="73359-108">Satırdaki öğenin stoğunun tutulması gerekir</span><span class="sxs-lookup"><span data-stu-id="73359-108">The item on the line must be stocked.</span></span> <span data-ttu-id="73359-109">Ayrıca, maddenin tesis ve ambarın etkin olduğu bir depolama boyutu grubuyla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="73359-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="73359-110">Bir madde varış günlüğü üst bilgisi oluşturun</span><span class="sxs-lookup"><span data-stu-id="73359-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="73359-111">Stok yönetimi > Yevmiye defteri girişleri > Madde varışı > Madde varışı öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="73359-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="73359-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-112">Click New.</span></span>
3. <span data-ttu-id="73359-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="73359-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="73359-114">USMF kullanıyorsanız, WHS yazabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73359-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="73359-115">Başka veriler kullanıyorsanız, adını seçtiğiniz günlükte iki özelliğin olması gerekir: Malzeme çekme yerleşimini denetle ayarı Hayır, Karantina yönetimi ayarı Hayır olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="73359-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="73359-116">Sevk irsaliyesi alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="73359-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="73359-117">Bu, satıcının çıkardığı sevk irsaliyesindeki sevk irsaliyesi kodudur.</span><span class="sxs-lookup"><span data-stu-id="73359-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="73359-118">Benzersiz bir numara ekleyin.</span><span class="sxs-lookup"><span data-stu-id="73359-118">Add a unique number.</span></span>  
5. <span data-ttu-id="73359-119">Numara alanında, satınalma siparişini seçin.</span><span class="sxs-lookup"><span data-stu-id="73359-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="73359-120">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="73359-121">Madde varış günlüğüne satırlar ekleyin</span><span class="sxs-lookup"><span data-stu-id="73359-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="73359-122">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73359-122">Click Functions.</span></span>
2. <span data-ttu-id="73359-123">Satır oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-123">Click Create lines.</span></span>
    * <span data-ttu-id="73359-124">Satırlar bu günlüğe el ile girilebilir veya otomatik olarak oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="73359-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="73359-125">Burada size bunun otomatik olarak nasıl oluşturulduğu gösterilecek.</span><span class="sxs-lookup"><span data-stu-id="73359-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="73359-126">Miktarı başlat onay kutusunu işaretleyin veya kutunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="73359-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="73359-127">Bu, satın alma siparişi satırında kaydedilmemiş miktarı olan günlük satırlarında miktarı başlatır.</span><span class="sxs-lookup"><span data-stu-id="73359-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="73359-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="73359-129">Günlüğü deftere naklet</span><span class="sxs-lookup"><span data-stu-id="73359-129">Post the journal</span></span>
1. <span data-ttu-id="73359-130">Deftere Naklet öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-130">Click Post.</span></span>
2. <span data-ttu-id="73359-131">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="73359-132">Ürün girişini oluşturun</span><span class="sxs-lookup"><span data-stu-id="73359-132">Generate the product receipt</span></span>
1. <span data-ttu-id="73359-133">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73359-133">Click Functions.</span></span>
2. <span data-ttu-id="73359-134">Ürün girişi seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-134">Click Product receipt.</span></span>
3. <span data-ttu-id="73359-135">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73359-135">Click OK.</span></span>

