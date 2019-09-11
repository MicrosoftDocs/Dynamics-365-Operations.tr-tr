---
title: Varlık sayaçlarını el ile güncelleştirme
description: Bu konuda, Varlık Yönetiminde varlık sayaçlarının el ile güncelleştirilmesi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875947"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="d0cc4-103">Varlık sayaçlarını el ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d0cc4-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="d0cc4-104">Sayaçlar, varlıkta örneğin operasyondaki saat sayısı veya üretilen miktar sayısı gibi kayıtları oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="d0cc4-105">Bir sayaç için seçilen sayaç türü sayaç değerlerini devralmak üzere ayarlanırsa (**Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar** > **Genel** hızlı sekmesi > **Varlık sayaç değerlerini devral** düğmesi "Evet" olarak ayarlanır) bu tür için yeni bir sayaç satırı oluşturduğunuzda, aynı sayaç türünü kullanan alt varlıklar otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="d0cc4-106">**Tüm varlıklar**'da, varlık üzerinde yaptığınız okumaları temel alarak, varlıkta saatler veya miktar sayacı kayıtları oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="d0cc4-107">**Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="d0cc4-108">Listeden varlığı seçin ve **Sayaçlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="d0cc4-109">**Varlık sayaçları** formunda, seçilen varlıktaki önceki tüm sayaç kayıtlarının listesini görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="d0cc4-110">Yeni bir kayıt oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="d0cc4-111">Varlık kodu otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="d0cc4-112">**Sayaç** alanında, ilgili sayacı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="d0cc4-113">Yalnızca, varlıkta seçilen varlık türüyle ilgili sayaçlar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="d0cc4-114">İlgili birim otomatik olarak **Birim** alanına eklenir.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="d0cc4-115">Sayaç kaydı için tarih ve saat seçin.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="d0cc4-116">**Değer** alanına, en son sayaç kaydından itibaren numarayı ekleyin veya **Toplam değer** alanına toplam sayı numarasını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="d0cc4-117">Bir varlığa fiziksel olarak yeni bir sayaç yüklerseniz, değişikliği **Varlık sayaçlarında** varlığa kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="d0cc4-118">Daha sonra, aynı zaman damgalarına sahip iki kayıt satırı oluşturmanız ve yeni sayaca ilişkin satırda, **Sayaç sıfırlama** onay kutusunu seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="d0cc4-119">İki kayıt satırını oluşturduğunuzda, ilk satır değiştirdiğiniz sayaca ait olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="d0cc4-120">**Toplamlar** alanında toplam sayı numarası, bu sayaç türündeki tüm kayıtlı değerlerin toplam sayaç toplamıdır.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="d0cc4-121">**Sayaç sıfırlama** onay kutusu "İtibaren bir kez..." veya "Ulaşıldığında..." aralık türüne sahip bir bakım planı kullanan bir varlıkta işaretlendiğinde, ayrı bir sayaç satırı oluşturduğunuz ve yeni bir sayaçla baştan başladığınızdan sayaç yeni sayaç satırında etkin olmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Şekil 1](media/11-work-orders.png)


<span data-ttu-id="d0cc4-123">Birden fazla varlıkta sayaç kayıtları yapmanız gerekiyorsa, bunu **Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık sayaçları** altından yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="d0cc4-124">El ile sayaç kayıtlarında sapmaları tanımlamak için bir aralık ve kayıtlar tanımlanan aralığın dışında olduğunda görüntülenecek olan ileti türü ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="d0cc4-125">Sayaçların kurulumuyla ilgili olarak [Sayaçlar](../setup-for-objects/counters.md) konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
