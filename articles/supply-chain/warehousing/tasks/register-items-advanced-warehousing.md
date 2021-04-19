---
title: Gelişmiş ambar işlemleri etkinleştirilmiş madde için madde varış günlüğü kullanarak maddeleri kaydetme
description: Bu konu, gelişmiş ambar yönetimi işlemlerini kullanırken ürünlerin ürün varış günlüğü kullanılarak nasıl kaydedileceğini gösteren bir senaryo sunar.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830846"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="5c1d6-103">Gelişmiş ambar işlemleri etkinleştirilmiş madde için madde varış günlüğü kullanarak maddeleri kaydetme</span><span class="sxs-lookup"><span data-stu-id="5c1d6-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c1d6-104">Bu konu, gelişmiş ambar yönetimi işlemlerini kullanırken ürünlerin ürün varış günlüğü kullanılarak nasıl kaydedileceğini gösteren bir senaryo sunar.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="5c1d6-105">Bu genellikle bir teslim alma memuru tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="5c1d6-106">Örnek verileri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="5c1d6-106">Enable sample data</span></span>

<span data-ttu-id="5c1d6-107">Bu konuda belirtilen örnek kayıtları ve değerleri kullanarak bu senaryo aracılığıyla çalışmak için, standart gösteri verilerinin yüklendiği bir sistem kullanıyor olmanız ve başlamadan önce *USMF* hukuk varlığını seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="5c1d6-108">Bunun yerine, aşağıdaki veriler kullanılabilir olduğu takdirde değerleri kendi verilerinizde değiştirerek bu senaryoya göre çalışabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="5c1d6-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="5c1d6-109">Açık bir satın alma siparişi satırı ile onaylanmış bir satın alma siparişiniz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="5c1d6-110">Satırdaki öğenin stoğunun tutulması gerekir</span><span class="sxs-lookup"><span data-stu-id="5c1d6-110">The item on the line must be stocked.</span></span> <span data-ttu-id="5c1d6-111">Ürün varyantlarını kullanmamalı ve izleme boyutları olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="5c1d6-112">Ürün ambar yönetimi işlemi etkin bir depolama boyut grubuyla ilişkilendirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="5c1d6-113">Kullanılan ambar, ambar yönetimi işlemleri için etkinleştirilmelidir ve alım işlemi için kullanılan yerleşimin plakası kontrol edilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="5c1d6-114">Ambar yönetimini kullanan bir madde varış günlüğü başlığı oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c1d6-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="5c1d6-115">Aşağıdaki senaryo, ambar yönetimi kullanan bir madde varış günlüğü başlığının nasıl oluşturulacağını gösterir:</span><span class="sxs-lookup"><span data-stu-id="5c1d6-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="5c1d6-116">Sisteminizin, önceki bölümde özetlenen gereksinimleri karşılayan, onaylanmış bir satın alma siparişi içerdiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="5c1d6-117">Bu senaryoda, *USMF* şirketi, *1001* satıcı hesabı, *51* ambarı ve *M9200* madde numarası için *10 PL* (10 palet) ilgili sipariş satırı bulunan bir satın alma siparişi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="5c1d6-118">Kullanacağınız Satın alma siparişi numarasını not edin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="5c1d6-119">**Stok yönetimi \> Günlük girişleri \> Madde varışı \> Madde varışı** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="5c1d6-120">Eylem Bölmesi'nde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="5c1d6-121">**Ambar yönetimi günlüğü oluştur** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="5c1d6-122">**Ad** alanında bir günlük adı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="5c1d6-123">*USMF* örnek verilerini kullanıyorsanız, *WHS* öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="5c1d6-124">Kendi verilerinizi kullanıyorsanız, seçtiğiniz günlükte **çekme konumunu denetle**'nin *Hayır* olarak ayarlanmış ve **karantina yönetimi**'nın *Hayır* olarak ayarlanmış olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="5c1d6-125">**Referans**'ı *Satın alma emri* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="5c1d6-126">**Hesap numarasını** *1001* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="5c1d6-127">Bu alıştırma için tanımladığınız satın alma siparişinin numarasını **Numara** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="5c1d6-128">![Gelen maddeler günlüğü](../media/item-arrival-journal-header.png "Gelen maddeler günlüğü")</span><span class="sxs-lookup"><span data-stu-id="5c1d6-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="5c1d6-129">Günlük başlığını oluşturmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="5c1d6-130">**Günlük satırları** bölümünde **satır ekle**'yi seçin ve aşağıdaki verileri girin:</span><span class="sxs-lookup"><span data-stu-id="5c1d6-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="5c1d6-131">**Öğe numarası** *M9200* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="5c1d6-132">**Tesis**, **Ambar** ve **miktar** 10 palet (her biri 1000) için stok işlemi verilerine dayalı olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="5c1d6-133">**Konum**: *001* olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="5c1d6-134">Bu belirli konum plakaları izlemez.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="5c1d6-135">![Gelen maddeler günlüğü satırı](../media/item-arrival-journal-line.png "Gelen maddeler günlüğü satırı")</span><span class="sxs-lookup"><span data-stu-id="5c1d6-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c1d6-136">**Tarih** alanı, bu ürünün eldeki miktarın stokta kaydedileceği tarihi belirler.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="5c1d6-137">**Lot kodu** sağlanan bilgilerden hareketle benzersiz şekilde tanımlanabiliyorsa, sistem tarafından doldurulur.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="5c1d6-138">Aksi halde, bunu el ile girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="5c1d6-139">Bu, bu kaydı belirli bir kaynak belge satırına bağlayan gerekli bir alandır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="5c1d6-140">Eylem bölmesinde **Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="5c1d6-141">Bu günlüğün deftere nakile hazır olup olmadığını denetler.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="5c1d6-142">Doğrulama başarısız olursa, günlüğü deftere nakledebilmek için hataları düzeltmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="5c1d6-143">**Günlüğü denetle** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="5c1d6-144">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-144">Select **OK**.</span></span>
1. <span data-ttu-id="5c1d6-145">İleti çubuğunu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-145">Review the message bar.</span></span> <span data-ttu-id="5c1d6-146">İşlemin tamamlandığını belirten bir ileti görünmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="5c1d6-147">Eylem Bölmesinde **Deftere naklet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="5c1d6-148">**Günlüğü deftere naklet** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="5c1d6-149">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-149">Select **OK**.</span></span>
1. <span data-ttu-id="5c1d6-150">İleti çubuğunu inceleyin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-150">Review the message bar.</span></span> <span data-ttu-id="5c1d6-151">İşlemin tamamlandığını belirten bir ileti görünmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="5c1d6-152">Satın alma sipariş satırını güncelleştirmek ve bir ürün girişini deftere nakletmek için eylem bölmesinde **İşlevler > ürün girişi** işlevlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="5c1d6-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
