---
title: Supply Chain Management fiyatlandırma altyapısıyla istek üzerine eşitleme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta Dynamics 365 Sales'ın fiyatlandırma motorunun nasıl kullanılacağı açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: bf4154816f01040a236dde77b92ee69396158614
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750776"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="54ee6-103">Supply Chain Management fiyatlandırma altyapısıyla istek üzerine eşitleme</span><span class="sxs-lookup"><span data-stu-id="54ee6-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="54ee6-104">Microsoft Dynamics 365 Supply Chain Management, ticari sözleşmeleri, Fiyat listelerini, müşteri bağlılık programı programlarını, yükseltmeleri ve iskontoları işleyen bir fiyatlandırma altyapısı içerir.</span><span class="sxs-lookup"><span data-stu-id="54ee6-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="54ee6-105">Fiyatlandırma motoru, belirli bir teklif veya sipariş için en iyi fiyatı belirlemek amacıyla karmaşık kurallar kullanır.</span><span class="sxs-lookup"><span data-stu-id="54ee6-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="54ee6-106">Çift yazmayı kullandığınızda, Dynamics 365 Sales içindeki teklif ve sipariş sayfalarındaki Dynamics 365 Supply Chain Management'tan fiyatlandırma motorunu kullanırsınız.</span><span class="sxs-lookup"><span data-stu-id="54ee6-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="54ee6-107">Sales'da Supply Chain Management fiyatlandırma altyapısını kullan</span><span class="sxs-lookup"><span data-stu-id="54ee6-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="54ee6-108">Sales'da **satışlar \>siparişlere** gidin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="54ee6-109">Yeni sipariş oluşturmak için **Yeni**'yi seçin veya **Siparişlerim** listesinde mevcut siparişi seçin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="54ee6-110">Yeni siparişi satırı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-110">Add a new order line.</span></span>
4. <span data-ttu-id="54ee6-111">Yeni bir sipariş oluşturuyorsanız, eylem bölmesinde **fiyat siparişi** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="54ee6-112">Mevcut bir siparişi güncelliyorsanız eylem bölmesinde **Yeniden hesapla** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="54ee6-113">Aşağıdaki sütunlar otomatik olarak doldurulur:</span><span class="sxs-lookup"><span data-stu-id="54ee6-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="54ee6-114">Ayrıntı Tutarı</span><span class="sxs-lookup"><span data-stu-id="54ee6-114">Detail Amount</span></span>
    + <span data-ttu-id="54ee6-115">İskonto yüzdesi</span><span class="sxs-lookup"><span data-stu-id="54ee6-115">Discount %</span></span>
    + <span data-ttu-id="54ee6-116">İskonto</span><span class="sxs-lookup"><span data-stu-id="54ee6-116">Discount</span></span>
    + <span data-ttu-id="54ee6-117">Ön Navlun Tutarı</span><span class="sxs-lookup"><span data-stu-id="54ee6-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="54ee6-118">Navlun Tutarı</span><span class="sxs-lookup"><span data-stu-id="54ee6-118">Freight Amount</span></span>
    + <span data-ttu-id="54ee6-119">Toplam Vergi</span><span class="sxs-lookup"><span data-stu-id="54ee6-119">Total Tax</span></span>
    + <span data-ttu-id="54ee6-120">Toplam Tutar</span><span class="sxs-lookup"><span data-stu-id="54ee6-120">Total Amount</span></span>
    
5. <span data-ttu-id="54ee6-121">Sistemin fiyatı hesaplamak amacıyla ticaret ve satış anlaşmalarını dikkate aldığından emin olmak için:</span><span class="sxs-lookup"><span data-stu-id="54ee6-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="54ee6-122">Supply Chain Management ortamınıza gidin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="54ee6-123">**Alacak hesapları \> Kurulum \> Alacak hesapları parametreleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="54ee6-124">Yan gezinti çubuğunda **Fiyatlar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="54ee6-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="54ee6-125">**Ticaret anlaşması değerlendirme** hızlı sekmesi altında, **El ile giriş** seçeneğindeki işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="54ee6-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="54ee6-126">Nasıl çalışır</span><span class="sxs-lookup"><span data-stu-id="54ee6-126">How it works</span></span>

<span data-ttu-id="54ee6-127">Sales'ta **fiyat siparişi** seçeneğini belirlediğinizde, ilgili satış siparişi için Supply Chain Management'te **Satış Siprişi \> Görüntüle** sekmesindeki **Toplamlar** işlevi çağrılır.</span><span class="sxs-lookup"><span data-stu-id="54ee6-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="54ee6-128">Sales içindeki sipariş toplamlarında bulunan değerler, Supply Chain Management'ta karşılık gelen sütunları doldurmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54ee6-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="54ee6-129">Supply Chain Management'ta satış siparişi toplamı hesaplandığında, hesaplama müşteri ve satış siparişinde listelenen ürünler için varolan ticari sözleşmeleri ve satış anlaşmalarını değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="54ee6-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="54ee6-130">Toplamları hesaplamak için bu bilgiler kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54ee6-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="54ee6-131">**Fiyat siparişi** seçildiğinde, Sales, Supply Chain Management'de yapılan tüm kurulumu otomatik olarak yansıtır.</span><span class="sxs-lookup"><span data-stu-id="54ee6-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="54ee6-132">Sınırlamalar</span><span class="sxs-lookup"><span data-stu-id="54ee6-132">Limitations</span></span>

<span data-ttu-id="54ee6-133">Sales içindeki sütunlar doldurulduğunda, aşağıdaki sınırlamalar geçerlidir:</span><span class="sxs-lookup"><span data-stu-id="54ee6-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="54ee6-134">Supply Chain Management'ta bulunan masraf ve gider tahsisatının kurulumu Sales içinde çoğaltılmaz.</span><span class="sxs-lookup"><span data-stu-id="54ee6-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="54ee6-135">Fiyatlandırma, Supply Chain Management'ta satış siparişi satırı sayfasındaki **Perakende Kanalı** sütununda belirtilen özel perakende fiyatlandırmasını dikkate almıyor.</span><span class="sxs-lookup"><span data-stu-id="54ee6-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="54ee6-136">Supply Chain Management'ın **ticari kesinti Yönetimi** bölümünde tanımlanan iskontolar dikkate alınmazlar.</span><span class="sxs-lookup"><span data-stu-id="54ee6-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]