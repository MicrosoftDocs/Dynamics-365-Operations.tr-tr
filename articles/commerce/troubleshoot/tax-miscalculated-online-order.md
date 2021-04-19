---
title: Çevrimiçi siparişlerdeki vergiler yanlış hesaplandı
description: Bu konu, çevrimiçi siparişlerdeki vergilerin yanlış hesaplandığı veya satış satırındaki vergi grubunun doğru ayarlanmadığı durumlarda yardımcı olabilecek hata giderme kılavuzu sağlar.
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
ms.openlocfilehash: 7f71add679e1d24f80db8ce3990058b591128ec1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801423"
---
# <a name="taxes-on-online-orders-are-incorrectly-calculated"></a><span data-ttu-id="7ef3b-103">Çevrimiçi siparişlerdeki vergiler yanlış hesaplandı</span><span class="sxs-lookup"><span data-stu-id="7ef3b-103">Taxes on online orders are incorrectly calculated</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ef3b-104">Bu konu, çevrimiçi siparişlerdeki vergilerin yanlış hesaplandığı veya satış satırındaki vergi grubunun doğru ayarlanmadığı durumlarda yardımcı olabilecek hata giderme kılavuzu sağlar.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-104">This topic provides troubleshooting guidance that can help when taxes on online orders are incorrectly calculated, or when the tax group on the sales line isn't correctly set.</span></span>

## <a name="description"></a><span data-ttu-id="7ef3b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ef3b-105">Description</span></span>

<span data-ttu-id="7ef3b-106">Bir e-ticaret siparişi verildiğinde vergiler yanlış hesaplanıyor veya satış satırındaki vergi grubu yanlış ayarlanıyor.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-106">When an e-commerce order is placed, the taxes are incorrectly calculated, or the tax group on the sales line is incorrectly set.</span></span>

## <a name="resolution"></a><span data-ttu-id="7ef3b-107">Çözünürlük</span><span class="sxs-lookup"><span data-stu-id="7ef3b-107">Resolution</span></span>

### <a name="configure-the-sales-tax-for-a-retail-store-in-commerce-headquarters"></a><span data-ttu-id="7ef3b-108">Commerce Headquarters'da bir perakende mağazası için satış vergisini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="7ef3b-108">Configure the sales tax for a retail store in Commerce headquarters</span></span>

<span data-ttu-id="7ef3b-109">Commerce Headquarters'da bir perakende mağazası için satış vergisini yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-109">To configure the sales tax for a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7ef3b-110">**Retail ve Commerce \> Kanallar \> Tüm mağazalar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-110">Go to **Retail and Commerce \> Channels \> All stores**.</span></span>
1. <span data-ttu-id="7ef3b-111">Satış vergisinin yapılandırılacağı mağazayı seçin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-111">Select the store to configure sales tax for.</span></span>
1. <span data-ttu-id="7ef3b-112">**Genel** hızlı sekmesinde, **Satış vergisi** bölümünde, mağazanın satış vergisi bilgilerini yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-112">On the **General** FastTab, in the **Sales tax** section, configure the sales tax information for the store.</span></span>

> [!NOTE]
> <span data-ttu-id="7ef3b-113">Bir mağazadan ürün çekme işlemi için vergi grubu malzeme çekme için seçilen mağazadan gelir.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-113">For product pickup from a store, the tax group comes from the store that is selected for pickup.</span></span> <span data-ttu-id="7ef3b-114">Daha fazla bilgi için bkz. [Mağazalar için diğer vergi seçeneklerini ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="7ef3b-114">For more information, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

### <a name="configure-the-sales-tax-for-a-customers-address-in-commerce-headquarters"></a><span data-ttu-id="7ef3b-115">Commerce Headquarters'da bir müşterinin adresi için satış vergisini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="7ef3b-115">Configure the sales tax for a customer's address in Commerce headquarters</span></span>

<span data-ttu-id="7ef3b-116">Commerce Headquarters'da bir müşterinin adresi için satış vergisini yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-116">To configure the sales tax for a customer's address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7ef3b-117">**Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-117">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="7ef3b-118">Satış vergisini yapılandıracağınız müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-118">Select the customer to configure sales taxes for.</span></span>
1. <span data-ttu-id="7ef3b-119">**Adresler** hızlı sekmesinde, satış vergilerini yapılandıracağınız adresi seçin, **diğer seçenekleri** ve sonra **Gelişmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-119">On the **Addresses** FastTab, select the address to configure sales taxes for, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="7ef3b-120">**Genel** hızlı sekmesinde, **Vergi grubu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-120">On the **General** FastTab, select the **Tax group**.</span></span>
1. <span data-ttu-id="7ef3b-121">**Satış vergisi** alanında uygun değeri seçin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-121">In the **Sales tax** field, select the appropriate value.</span></span>

> [!NOTE]
> <span data-ttu-id="7ef3b-122">Müşterinin adresinde satış vergisi içeren sevkiyat için satırın teslimat adresi satırın vergi grubunu belirler.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-122">For shipping that involves sales tax on the customer's address, the delivery address of the line determines the tax group for the line.</span></span> <span data-ttu-id="7ef3b-123">Müşteri zaten yapılandırılmış bir vergi grubuna sahip mevcut bir adrese ürün gönderiyorsa mevcut vergi grubu kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-123">If the customer is shipping to an existing address that has a tax group that is already configured, the existing tax group will be used.</span></span> <span data-ttu-id="7ef3b-124">Varsayılan olarak, adresler oluşturuldukları sırada bir vergi grubuna sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-124">By default, addresses don't have a tax group when they are created.</span></span>

### <a name="configure-general-sales-tax-groups-in-commerce-headquarters"></a><span data-ttu-id="7ef3b-125">Commerce Headquarters'da genel satış vergisi gruplarını yapılandırın</span><span class="sxs-lookup"><span data-stu-id="7ef3b-125">Configure general sales tax groups in Commerce headquarters</span></span>

<span data-ttu-id="7ef3b-126">Commerce Headquarters'da genel satış vergisi grupları yapılandırmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-126">To configure general sales tax groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="7ef3b-127">**Vergi \> Dolaylı vergiler \> Satış vergisi \> Satış vergisi grubu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-127">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="7ef3b-128">Sol gezinti bölmesinde yapılandırılacak vergi grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-128">In the left navigation, select the tax group to configure.</span></span>
1. <span data-ttu-id="7ef3b-129">**Mağaza hedefi tabanlı vergi** hızlı sekmesinde, satış vergi grubuyla ilgili vergileri yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-129">On the **Retail destination based tax** FastTab, configure the taxes for the sales tax group.</span></span>

> [!NOTE]
> <span data-ttu-id="7ef3b-130">Müşteri adresinde satış vergisi içermeyen sevkiyat için vergi grubu, vergi grubu için yapılandırılan satırın teslimat adresi ve hedef tabanlı vergiler tarafından belirlenir.</span><span class="sxs-lookup"><span data-stu-id="7ef3b-130">For shipping that doesn't involve sales tax on the customer's address, the delivery address of the line and the destination-based taxes that are configured for the tax group determine the tax group.</span></span> <span data-ttu-id="7ef3b-131">Daha fazla bilgi için, bkz [Hedefe bağlı olara çevrimiçi mağazalar için vergiler ayarlayın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="7ef3b-131">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ef3b-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7ef3b-132">Additional resources</span></span>

[<span data-ttu-id="7ef3b-133">Çevrimiçi siparişler için satış vergisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7ef3b-133">Configure sales tax for online orders</span></span>](../sales-tax-config.md)
