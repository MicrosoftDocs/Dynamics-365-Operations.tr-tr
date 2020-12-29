---
title: Çevrimiçi siparişler için satış vergisini yapılandırma
description: Bu konu, Dynamics 365 Commerce'de farklı çevrimiçi sipariş türleri için satış vergisi grubu seçimine genel bir bakış sağlar .
author: gvrmohanreddy
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 40c20bf13779f73289e43df21b763e1b864686a7
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530209"
---
# <a name="configure-sales-tax-for-online-orders"></a><span data-ttu-id="f395e-103">Çevrimiçi siparişler için satış vergisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="f395e-103">Configure sales tax for online orders</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f395e-104">Bu konu, farklı çevrimiçi sipariş türleri için satış vergisi grubu seçimine genel bir bakış sağlar.</span><span class="sxs-lookup"><span data-stu-id="f395e-104">This topic provides an overview of sales tax group selection for different online order types.</span></span> 

<span data-ttu-id="f395e-105">E-ticaret kanallarınız, çevrimiçi siparişler için teslimat ve malzeme çekme gibi seçenekleri desteklemek isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="f395e-105">Your e-commerce channel may want to support options like delivery or pickup for online orders.</span></span> <span data-ttu-id="f395e-106">Satış vergi uygulanabilirliğini, çevrimiçi kullanıcılarınızın seçtiği seçeneğe göre yapılır.</span><span class="sxs-lookup"><span data-stu-id="f395e-106">The sales tax applicability is based on the option selected by your online users.</span></span> <span data-ttu-id="f395e-107">Bir site müşterisi, bir maddeyi çevrimiçi olarak satın almayı ve onu bir adrese sevk edilmesini seçtiğinde, satış vergisi müşterinin sevkiyat adresi vergi grubu ayarına göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="f395e-107">When a site customer chooses to buy an item online and gets it shipped to an address, the sales tax is determined based on the customer's shipping address tax group setting.</span></span> <span data-ttu-id="f395e-108">Bir müşteri bir mağazada satın alınan bir maddeyi çekme işlemi yaparken, satış vergisi malzeme çekme deposunun vergi grubu ayarına göre belirlenir.</span><span class="sxs-lookup"><span data-stu-id="f395e-108">When a customer opts to pick up a purchased item at a store, the sales tax is determined based on the pickup store's tax group setting.</span></span> 

## <a name="orders-shipped-to-a-customer-address"></a><span data-ttu-id="f395e-109">Müşteri adresine sevk edilen siparişler</span><span class="sxs-lookup"><span data-stu-id="f395e-109">Orders shipped to a customer address</span></span> 

<span data-ttu-id="f395e-110">Genel olarak, Müşteri adresine sevkiyat amacıyla gönderilen çevrimiçi siparişler için vergiler hedef tarafından tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f395e-110">In general, taxes for online orders that ship to customer addresses are defined by the destination.</span></span> <span data-ttu-id="f395e-111">Her satış vergisi grubunun, işletmenizin İlçe/Bölge, eyalet, ilçe ve şehir gibi hedef ayrıntılarını hiyerarşik bir formda tanımlayabileceği, perakende hedefi tabanlı bir vergi konfigürasyonu vardır.</span><span class="sxs-lookup"><span data-stu-id="f395e-111">Every sales tax group has a retail destination-based tax configuration in which your business can define destination details such as county/region, state, county, and city in a hierarchical form.</span></span> <span data-ttu-id="f395e-112">Bir çevrimiçi sipariş verildiğinde, Commerce vergi altyapısı, siparişteki her bir satır maddesinin teslimat adresini kullanır ve hedef esaslı vergi ölçütlerine sahip satış vergisi gruplarını bulur.</span><span class="sxs-lookup"><span data-stu-id="f395e-112">When an online order is placed, the Commerce tax engine uses the delivery address of every line item in the order, and finds sales tax groups with matching destination-based tax criteria.</span></span> <span data-ttu-id="f395e-113">Örneğin, California Francisco'ya ait satır maddesi teslimat adresi olan bir çevrimiçi sipariş için vergi altyapısı, California için satış vergisi grubunu ve satış vergisi kodunu bulacak ve her satır maddesi için vergiyi hesaplayacaktır.</span><span class="sxs-lookup"><span data-stu-id="f395e-113">For example, for an online order with a line item delivery address to San Francisco, California, the tax engine will find the sales tax group and sales tax code for California and then calculate tax for each line item accordingly.</span></span>  

## <a name="customer-based-tax-groups"></a><span data-ttu-id="f395e-114">Müşteri tabanlı vergi grupları</span><span class="sxs-lookup"><span data-stu-id="f395e-114">Customer-based tax groups</span></span>

<span data-ttu-id="f395e-115">Commerce Headquarters'da, müşteri vergi gruplarının konfigüre edildiği iki yer vardır:</span><span class="sxs-lookup"><span data-stu-id="f395e-115">In Commerce headquarters, there are two places where customer tax groups are configured:</span></span>

- <span data-ttu-id="f395e-116">**Müşterinin profili**</span><span class="sxs-lookup"><span data-stu-id="f395e-116">**Customer's profile**</span></span>
- <span data-ttu-id="f395e-117">**Müşterinin sevkiyat adresi**</span><span class="sxs-lookup"><span data-stu-id="f395e-117">**Customer's shipping address**</span></span>

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a><span data-ttu-id="f395e-118">Bir müşterinin profilinde konfigüre edilmiş bir vergi grubu varsa</span><span class="sxs-lookup"><span data-stu-id="f395e-118">If a customer's profile has a tax group configured</span></span>

<span data-ttu-id="f395e-119">Müşteri merkezindeki bir müşterinin profil kaydının konfigüre edilmiş bir satış vergisi grubu olabilir; ancak çevrimiçi siparişler için vergi altyapısı tarafından konfigüre edilen satış vergisi grubu kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="f395e-119">A customer's profile record in headquarters may have a sales tax group configured, however for online orders the sales tax group configured in a customer's profile will not be used by the tax engine.</span></span> 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a><span data-ttu-id="f395e-120">Bir müşterinin teslimat adresinde konfigüre edilmiş bir vergi grubu varsa</span><span class="sxs-lookup"><span data-stu-id="f395e-120">If a customer's shipping address has a tax group configured</span></span>

<span data-ttu-id="f395e-121">Müşterinin sevkiyat adresi kaydının konfigüre edilmiş bir vergi grubu varsa ve müşterinin sevkiyat adresine bir çevrimiçi sipariş (veya satır maddesi) sevk edilmişse, müşterinin adres kaydında konfigüre edilen vergi grubu vergi hesaplamaları için vergi alt yapısı tarafından kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="f395e-121">If a customer's shipping address record has a tax group configured and an online order (or line item) is shipped to the customer's shipping address, the tax group configured in the customer's address record will be used by the tax engine for tax calculations.</span></span>

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a><span data-ttu-id="f395e-122">Bir müşterinin teslimat adresi kaydı için vergi grubunu yapılandırın</span><span class="sxs-lookup"><span data-stu-id="f395e-122">Configure a tax group for a customer's shipping address record</span></span>

<span data-ttu-id="f395e-123">Commerce Headquarters'da müşterinin sevkiyat adresi kaydı için bir vergi grubu konfigüre etmek üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="f395e-123">To configure a tax group for a customer's shipping address record in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="f395e-124">**Tüm müşteriler**'e gidin ve istediğiniz müşteriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="f395e-124">Go to **All customers**, and then select the desired customer.</span></span> 
1. <span data-ttu-id="f395e-125">**Adresler** hızlı sekmesinde, istediğiniz adresi seçin ve **Daha fazla seçenek \> Gelişmiş**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f395e-125">On the **Addresses** FastTab, select the desired address, and then select **More options \> Advanced**.</span></span> 
1. <span data-ttu-id="f395e-126">**Adresleri Yönet** sayfasının **Genel** sekmesi altında satış vergisi değerini gerektiği gibi ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="f395e-126">Under the **General** tab on the **Manage addresses** page, set the sales tax value as needed.</span></span>

> [!NOTE]
> <span data-ttu-id="f395e-127">Vergi grubu sipariş satırının teslimat adresi ve hedef esaslı vergiler vergi grubunun kendisinde konfigüre edilmiş olarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="f395e-127">The tax group is defined using the delivery address of the order line and the destination-based taxes are configured at the tax group itself.</span></span> <span data-ttu-id="f395e-128">Daha fazla bilgi için, bkz [Hedefe bağlı olara çevrimiçi mağazalar için vergiler ayarlayın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span><span class="sxs-lookup"><span data-stu-id="f395e-128">For more information, see [Set up taxes for online stores based on destination](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).</span></span>

## <a name="order-pickup-in-store"></a><span data-ttu-id="f395e-129">Mağazadan sipariş teslim alma</span><span class="sxs-lookup"><span data-stu-id="f395e-129">Order pickup in store</span></span>

<span data-ttu-id="f395e-130">Mağazada malzeme çekme veya perde çekme belirtilmiş sipariş satırları için, seçili malzeme çekme deposundaki vergi grubu uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f395e-130">For order lines with pickup in store or curbside pickup specified, the tax group from the selected pickup store will be applied.</span></span> <span data-ttu-id="f395e-131">Belirli bir mağaza için vergi grubunun nasıl konfigüre nakledileceği hakkında ayrıntılı bilgi için bkz [Mağazalar için diğer vergi seçenekleri ayarlayın](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span><span class="sxs-lookup"><span data-stu-id="f395e-131">For details about how to configure the tax group for a given store, see [Set other tax options for stores](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).</span></span>

> [!NOTE]
> <span data-ttu-id="f395e-132">Bir mağazada sipariş satırı çekildiğinde, vergi altyapısı (ayarlanmış ise) için müşterinin adres vergi ayarları yoksayılacaktır ve malzeme çekme deposunun vergi konfigürasyonu uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f395e-132">When an order line is picked up at a store, a customer's address tax settings (if set up) will be ignored by the tax engine and the pickup store's tax configuration will be applied.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f395e-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f395e-133">Additional resources</span></span>

[<span data-ttu-id="f395e-134">Satış vergisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="f395e-134">Sales tax overview</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f395e-135">Kaynak alanında satış vergisi hesaplama yöntemleri</span><span class="sxs-lookup"><span data-stu-id="f395e-135">Sales tax calculation methods in the Origin field</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f395e-136"> Satış vergisi atama ve geçersiz kılma</span><span class="sxs-lookup"><span data-stu-id="f395e-136">Sales tax assignment and overrides</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f395e-137">Satış vergisi kodları için Tam tutar ve Aralık hesaplama seçenekleri</span><span class="sxs-lookup"><span data-stu-id="f395e-137">Whole amount and Interval calculation options for sales tax codes</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[<span data-ttu-id="f395e-138">Vergi muafiyeti hesaplaması</span><span class="sxs-lookup"><span data-stu-id="f395e-138">Calculation of tax exemption</span></span>](tax-exempt-price-inclusive.md) 

