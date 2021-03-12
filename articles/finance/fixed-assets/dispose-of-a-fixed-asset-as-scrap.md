---
title: Sabit kıymeti hurda olarak elden çıkarma
description: Bu konu, hurda olarak elden çıkarılan bir sabit kıymet için hareketleri eleme sürecini açıklar.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4dee4468079a9ad500f513900cec090acf6026ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969140"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="96bc9-103">Sabit kıymeti hurda olarak elden çıkarma</span><span class="sxs-lookup"><span data-stu-id="96bc9-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96bc9-104">Bu konu, hurda olarak elden çıkarılan bir sabit kıymet için hareketleri eleme sürecini açıklar.</span><span class="sxs-lookup"><span data-stu-id="96bc9-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="96bc9-105">Elenebilecek hareket tipleri bir kıymetin alımını ve birikmiş amortisman hareketlerini ve diğer sabit kıymet hareketlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="96bc9-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="96bc9-106">Bu hareketlerin elenmesi alım düzeltmesi, amortisman ayarlaması, yeniden değerleme, değer artırma ve değer azaltma hesapları gibi bilanço hesaplarını etkiler.</span><span class="sxs-lookup"><span data-stu-id="96bc9-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="96bc9-107">Hareket</span><span class="sxs-lookup"><span data-stu-id="96bc9-107">Transaction</span></span>                                         | <span data-ttu-id="96bc9-108">Borç (Br.)</span><span class="sxs-lookup"><span data-stu-id="96bc9-108">Debit (Dr.)</span></span> | <span data-ttu-id="96bc9-109">Alacak (Al.)</span><span class="sxs-lookup"><span data-stu-id="96bc9-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="96bc9-110">Br. Birikmiş amortisman</span><span class="sxs-lookup"><span data-stu-id="96bc9-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="96bc9-111">X</span><span class="sxs-lookup"><span data-stu-id="96bc9-111">X</span></span>           |              |
| <span data-ttu-id="96bc9-112">Al. sabit kıymet kazancı/zararı</span><span class="sxs-lookup"><span data-stu-id="96bc9-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="96bc9-113">X</span><span class="sxs-lookup"><span data-stu-id="96bc9-113">X</span></span>            |
| <span data-ttu-id="96bc9-114">Br. Sabit kıymet kazancı/zararı</span><span class="sxs-lookup"><span data-stu-id="96bc9-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="96bc9-115">X</span><span class="sxs-lookup"><span data-stu-id="96bc9-115">X</span></span>           |              |
| <span data-ttu-id="96bc9-116">Al. Sabit kıymet alımı hesabı</span><span class="sxs-lookup"><span data-stu-id="96bc9-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="96bc9-117">X</span><span class="sxs-lookup"><span data-stu-id="96bc9-117">X</span></span>            |
| <span data-ttu-id="96bc9-118">Br. Sabit kıymet kazanç/kayıp (net defter değeri \[NDD\])</span><span class="sxs-lookup"><span data-stu-id="96bc9-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="96bc9-119">X</span><span class="sxs-lookup"><span data-stu-id="96bc9-119">X</span></span>           |              |
| <span data-ttu-id="96bc9-120">Al. Sabit kıymet kazancı/zararı (NDD)</span><span class="sxs-lookup"><span data-stu-id="96bc9-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="96bc9-121">X</span><span class="sxs-lookup"><span data-stu-id="96bc9-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="96bc9-122">Her hareket türü için kullanılacak doğru hesapları tanımlamak ve ayrıca elden çıkarma işleminin ve oluşturduğu hareketlerin doğrulanması için şirketinizin mali müdürü (CFO) veya denetleyicinizle yakından çalışmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="96bc9-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="96bc9-123">Sabit bir kıymeti hurda olarak elden çıkarmadan önce kıymetin alım değeri, geçerli yıla ait amortisman, önceki yıla ait amortisman ve kıymetin NDD'si ile ilişkili genel muhasebe sehapları oluştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="96bc9-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="96bc9-124">Sabit kıymet hareket türleri **Sabit kıymetler deftere nakil profili** sayfasında listelenmiştir.</span><span class="sxs-lookup"><span data-stu-id="96bc9-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="96bc9-125">**Sabit kıymetler \> Kurulum \> Sabit kıymet deftere nakil profilleri**'ne gidin ve **Elden çıkarma** hızlı sekmesinde, kılavuzun üstündeki alanda bulunan **Hurda**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="96bc9-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="96bc9-126">Aşağıdaki şekil, **Sabit kıymet deftere nakil profilleri** sayfasındaki sabit kıymet hareket türlerinin listesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="96bc9-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="96bc9-127">[![Bir kıymetin hurda olarak elden çıkarılması, Şek. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="96bc9-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="96bc9-128">Aşağıdaki örnekte, sabit kıymet 1 Ocak 2018 tarihinde elde edildi ve 31 Mart 2019 tarihinde hurdaya çıkarılacak.</span><span class="sxs-lookup"><span data-stu-id="96bc9-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="96bc9-129">**Alım fiyatı:** 24.000,00 ABD Doları (USD)</span><span class="sxs-lookup"><span data-stu-id="96bc9-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="96bc9-130">**Servis ömrü:** İki yıl</span><span class="sxs-lookup"><span data-stu-id="96bc9-130">**Service life:** Two years</span></span>
- <span data-ttu-id="96bc9-131">**Amortisman yöntemi:** Sabit servis ömrü</span><span class="sxs-lookup"><span data-stu-id="96bc9-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="96bc9-132">**Amortisman tutarı:** ayda 1.000,00 USD</span><span class="sxs-lookup"><span data-stu-id="96bc9-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="96bc9-133">Sabit kıymetin NDD'si aşağıdaki formül kullanılarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="96bc9-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="96bc9-134">Net defter değeri = Alım fiyatı – Amortisman</span><span class="sxs-lookup"><span data-stu-id="96bc9-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="96bc9-135">Bu örnekte, sabit kıymet elde edildi ve Ocak 2018 ile Mart 2019 arasında 15 ay için amortisman uygulandı.</span><span class="sxs-lookup"><span data-stu-id="96bc9-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="96bc9-136">Bu nedenle kıymetin NDD'si 9.000,00 USD (24.000,00 USD – 15.000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="96bc9-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="96bc9-137">[![Sabit kıymet amortisman örneği](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="96bc9-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="96bc9-138">Elden çıkarma günlüğü oluşturmak için **Sabit kıymetler \> Günlük girişleri \> Sabit kıymetler günlüğü**'ne gidin ve Eylem bölmesinde **Satırlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="96bc9-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="96bc9-139">**Elden çıkarma – hurda**'yı ve ardından sabit kıymet kodunu seçin.</span><span class="sxs-lookup"><span data-stu-id="96bc9-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="96bc9-140">Kıymetin tamamen elden çıkarılması için **Borç** alanına veya **Alacak** alanına değer girmeyin.</span><span class="sxs-lookup"><span data-stu-id="96bc9-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="96bc9-141">[![Sabit kıymet günlüğü](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="96bc9-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="96bc9-142">Sabit kıymet elden çıkarma hurda hareketi, sabit kıymet defterinin alan değerlerini aşağıdaki yollarla değiştirir:</span><span class="sxs-lookup"><span data-stu-id="96bc9-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="96bc9-143">**Bakiye** bölümünde, **Durum** alanı **Hurdaya çıkarıldı** şeklinde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="96bc9-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="96bc9-144">**Çıkış** bölümünde, **Elden çıkarma tarihi** alanı kıymetin hurdaya çıkarıldığı tarihe ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="96bc9-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="96bc9-145">[![Sabit kıymetler günlüğü ayrıntısı](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="96bc9-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="96bc9-146">Aşağıdaki şekil sabit kıymet bakiyesini gösterir.</span><span class="sxs-lookup"><span data-stu-id="96bc9-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="96bc9-147">[![Sabit kıyme bakiyesi](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="96bc9-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="96bc9-148">Aşağıdaki şekil deftere nakledilen fişi gösterir.</span><span class="sxs-lookup"><span data-stu-id="96bc9-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="96bc9-149">[![Net defter değeri](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="96bc9-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>
