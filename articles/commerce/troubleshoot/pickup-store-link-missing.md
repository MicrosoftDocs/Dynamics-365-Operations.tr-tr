---
title: Teslim al seçeneği sepette veya ürün ayrıntıları sayfalarında görünmüyor
description: Bu konu, sepet sayfasında veya ürün ayrıntıları sayfalarında mağazadan teslim alma seçeneği gözükmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 46eeed18bb547035603d7e9a01e8f131a2393f01
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801639"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="2302a-103">"Teslim al" seçeneği sepette veya ürün ayrıntıları sayfalarında görünmüyor</span><span class="sxs-lookup"><span data-stu-id="2302a-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2302a-104">Bu konu, sepet sayfasında veya ürün ayrıntıları sayfalarında mağazadan teslim alma seçeneği gözükmediğinde yardımcı olabilecek sorun giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="2302a-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="2302a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2302a-105">Description</span></span>

<span data-ttu-id="2302a-106">**Teslim al** düğmesi sepet sayfasında veya ürün ayrıntıları sayfalarında görünmüyor.</span><span class="sxs-lookup"><span data-stu-id="2302a-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="2302a-107">Aşağıdaki resimde **Teslim al** düğmesini içeren bir sayfa örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2302a-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Teslim al düğmesi](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="2302a-109">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="2302a-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="2302a-110">Commerce Site Builder'da BOPIS uzantısını etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2302a-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="2302a-111">Commerce Site Builder'da "çevrimiçi satın al, mağazadan teslim al" (BOPIS) uzantısını etkinleştirmek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2302a-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="2302a-112">Sitenizi seçin.</span><span class="sxs-lookup"><span data-stu-id="2302a-112">Select your site.</span></span>
1. <span data-ttu-id="2302a-113">**Site Ayarları**'nı ve daha sonra **Uzantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2302a-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="2302a-114">**BOPIS'ı devre dışı bırak** seçeneğinin temizlenmiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2302a-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="2302a-115">Commerce Headquarters'da teslimat şekillerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2302a-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="2302a-116">Commerce Headquarters'da teslimat şekillerdini yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2302a-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2302a-117">**Tedarik ve kaynak \> Kurulum \> Teslimat şekilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="2302a-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="2302a-118">**Müşteri teslim alma** teslimat şeklinin oluşturulduğundan ve ürün ve adreslerin buna atanmış olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="2302a-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="2302a-119">**Retail ve Commerce \> Headquarters kurulumu \> Parametreler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="2302a-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="2302a-120">Sol gezinti bölmesinde **Müşteri siparişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2302a-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="2302a-121">**Teslim alma teslimat şekli**'nin doğru yapılandırıldığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="2302a-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="2302a-122">Müşteri siparişleri ödemelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2302a-122">Configure customer orders payments</span></span>

<span data-ttu-id="2302a-123">Commerce Headquarters'da müşteri siparişleri ödemelerini yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2302a-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="2302a-124">**Retail ve Commerce \> Headquarters kurulumu \> Parametreler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="2302a-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="2302a-125">Sol gezinti bölmesinde **Müşteri siparişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2302a-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="2302a-126">**Ödemeler** hızlı sekmesinde, **Ödeme koşullarının** ve **ödeme yönteminin** doğru ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="2302a-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2302a-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2302a-127">Additional resources</span></span>

[<span data-ttu-id="2302a-128">BOPIS'i yapılandırma</span><span class="sxs-lookup"><span data-stu-id="2302a-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="2302a-129">Müşteri sipairşleri için Çoklu malzeme çekme teslimat şekillerini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2302a-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="2302a-130">Çok yönlü kanal Commerce siparişi ödemeleri</span><span class="sxs-lookup"><span data-stu-id="2302a-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="2302a-131">Mağaza seçicisi modülü</span><span class="sxs-lookup"><span data-stu-id="2302a-131">Store selector module</span></span>](../store-selector.md)
