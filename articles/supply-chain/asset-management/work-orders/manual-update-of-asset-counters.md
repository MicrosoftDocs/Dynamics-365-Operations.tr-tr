---
title: Varlık sayaçlarını el ile güncelleştirme
description: Bu konuda, Varlık Yönetiminde varlık sayaçlarının el ile güncelleştirilmesi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5318bac961682f88e192ac70c4993c62b69b399c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020897"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="94208-103">Kıymet sayaçlarını el ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="94208-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="94208-104">Sayaçlar, bir varlık üzerinde varlığın işlemde olduğu saat sayısı veya üretilmiş miktar gibi kayıtlar için kayıt oluşturmak amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="94208-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="94208-105">Bir sayaç için seçilen sayaç türü, sayaç değerlerini devralmak üzere ayarlanabilir.</span><span class="sxs-lookup"><span data-stu-id="94208-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="94208-106">Başka bir deyişle, **VArlık sayacı değerlerini devral** seçeneği **Sayaçlar** sayfasının **Genel** hızlı sekmesinde **Evet** olarak ayarlanır (**Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar**).</span><span class="sxs-lookup"><span data-stu-id="94208-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="94208-107">Bu durumda, bu türde yeni bir sayaç satırı oluşturduğunuzda, aynı sayaç türünü kullanan her alt varlık otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="94208-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="94208-108">**Tüm varlıklar** sayfasında, varlık üzerinde yaptığınız okumaları temel alarak, varlıkta saatler veya miktar sayacı kayıtları oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="94208-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="94208-109">**Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="94208-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="94208-110">Varlığı seçin ve ardından Eylem bölmesinde **Varlık** sekmesinde, **Önleyici** grubunda **Sayaçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="94208-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="94208-111">**Varlık sayaçları** sayfası, seçilen varlıkta yapılmış olan önceki tüm sayaç kayıtlarının listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="94208-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="94208-112">Kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="94208-112">Select **New** to create a registration.</span></span> <span data-ttu-id="94208-113">Varlık kodu **Varlık** alanına otomatik olarak girilir.</span><span class="sxs-lookup"><span data-stu-id="94208-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="94208-114">**Sayaç** alanında, ilgili sayacı seçin.</span><span class="sxs-lookup"><span data-stu-id="94208-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="94208-115">Yalnızca, varlıkta seçilen varlık türüyle ilgili sayaçlar seçilebilir.</span><span class="sxs-lookup"><span data-stu-id="94208-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="94208-116">İlgili birim otomatik olarak **Birim** alanına girilir.</span><span class="sxs-lookup"><span data-stu-id="94208-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="94208-117">**Kayıtlı** alanında, sayaç kaydının tarih ve saatini seçin.</span><span class="sxs-lookup"><span data-stu-id="94208-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="94208-118">**Değer** alanına, son sayac kaydından sonra gelen numarayı girin.</span><span class="sxs-lookup"><span data-stu-id="94208-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="94208-119">Alternatif olarak, **Toplu değer** alanına toplam sayım numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="94208-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="94208-120">Aaşağıdaki noktaları unutmayın:</span><span class="sxs-lookup"><span data-stu-id="94208-120">Note the following points:</span></span>

- <span data-ttu-id="94208-121">Bir varlığa fiziksel olarak yeni bir sayaç yüklerseniz, değişikliği **Varlık sayaçları** sayfasında varlığa kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="94208-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="94208-122">Daha sonra, aynı zaman damgalarına sahip iki kayıt satırı oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="94208-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="94208-123">İlk satırın değiştirdiğiniz sayaç için olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="94208-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="94208-124">Yeni sayaçla ilgili satırda, **Sayaç sıfırla** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="94208-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="94208-125">**Toplamlar** alanında toplam sayı numarası, bu sayaç türündeki tüm kayıtlı değerlerin toplam sayaç toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="94208-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="94208-126">**Sayaç sıfırlama** onay kutusu "İtibaren bir kez..." veya "Ulaşıldığında..." aralık türüne sahip bir bakım planı kullanan bir varlıkta işaretlendiğinde, ayrı bir sayaç satırı oluşturduğunuz ve yeni bir sayaçla baştan başladığınızdan sayaç yeni sayaç satırında etkin olmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="94208-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="94208-127">Aşağıdaki örnekte **Varlık sayaçları** sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="94208-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Şekil 1](media/11-work-orders.png)

<span data-ttu-id="94208-129">**Varlık sayaçları** sayfasında (**Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık sayaçları**), gereksinim duyduğunuz gibi, aynı anda birden fazla varlıkta sayaç kaydı yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94208-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="94208-130">El ile gerçekleştirilen sayaç kayıtlarında sapmaları tanımlamak için bir aralık ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94208-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="94208-131">Kayıtlar tanımlanan aralığın dışında olduğunda gösterilecek ileti türünü de belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="94208-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="94208-132">Sayaçların nasıl ayarlanacağı konusunda daha fazla bilgi için bkz. [Sayaçlar](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="94208-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

