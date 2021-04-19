---
title: Malzeme çekme bilgileri modülü
description: Bu konu teslim bilgileri modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün ödeme sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 063701d5cd5714febeb32907346d9f6e5c2a2ca1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804417"
---
# <a name="pickup-information-module"></a><span data-ttu-id="47169-103">Malzeme çekme bilgileri modülü</span><span class="sxs-lookup"><span data-stu-id="47169-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47169-104">Bu konu teslim bilgileri modülünü kapsamaktadır ve Microsoft Dynamics 365 Commerce'ün ödeme sayfalarına nasıl ekleneceğini açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="47169-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="47169-105">Malzeme çekme bilgileri modülü, sipariş alma bilgilerini göstermek amacıyla bir kullanıma alma modülünde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="47169-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="47169-106">Müşteriler, mevcut malzeme çekme tarihlerini ve zaman yuvalarını görüntüleyebilir ve sonra siparişini çekmek için uygun bir zaman seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47169-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="47169-107">Örneğin, bir müşteri San Francisco Store 'dan 21 Mart 'ta 15.00'da siparişi teslim alabilir.</span><span class="sxs-lookup"><span data-stu-id="47169-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="47169-108">İlgili Mağazalar için malzeme çekme zaman yuvaları Commerce Headquarters 'da konfigüre edilmelidir.</span><span class="sxs-lookup"><span data-stu-id="47169-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="47169-109">Daha fazla bilgi için bkz. [Müşteri malzeme çekme için zaman aralıkları oluşturma ve güncelleştirme](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="47169-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="47169-110">Malzeme çekme bilgileri modülü kullanıma alma sayfasında oluşturulursa, ancak malzeme çekme için seçilen mağaza için tanımlanmış zaman yuvaları yoksa modül bilgileri gösterir, ancak Kullanıcı herhangi bir zaman dilimini seçemeyecektir.</span><span class="sxs-lookup"><span data-stu-id="47169-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="47169-111">Zaman yuvaları isteğe bağlıdır ve sipariş vermek zorunda değildir.</span><span class="sxs-lookup"><span data-stu-id="47169-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="47169-112">Çoklu mağazalar arasında malzeme çekme için birden fazla madde seçilmişse, malzeme çekme bilgileri modülü kullanıcının her mağaza için zaman dilimini seçmesini sağlar; bunlar için zaman dilimi kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="47169-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="47169-113">Zaman yuvaları desteği ve kullanıma alma bilgileri modülü Dynamics 365 Commerce sürüm 10.0.15 ve sonrasında mevcuttur.</span><span class="sxs-lookup"><span data-stu-id="47169-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="47169-114">Aşağıdaki resimde, kullanıma alma sayfasındaki malzeme çekme bilgileri modülü aracılığıyla zaman dilimi seçimi örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47169-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Ödeme sayfasındaki teslimat bilgileri modülü örneği](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="47169-116">Modül özellikleri</span><span class="sxs-lookup"><span data-stu-id="47169-116">Module properties</span></span>

- <span data-ttu-id="47169-117">**Başlık** - Ödeme modülü için başlık.</span><span class="sxs-lookup"><span data-stu-id="47169-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="47169-118">Sipariş yerleştirildikten sonra zaman dilimi bilgilerini göster</span><span class="sxs-lookup"><span data-stu-id="47169-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="47169-119">Bir sipariş yerleştirildikten sonra, seçilen zaman dilimi hakkındaki bilgiler [sipariş onayı modülünde](order-confirmation-module.md) ve [sipariş ayrıntıları modülünde görüntülenebilir](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="47169-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="47169-120">Bu modüllerin her ikisi de bir **zaman lotu bilgilerini göster** özelliğine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="47169-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="47169-121">Sipariş işlemi sırasında seçilen zaman dilimini gösterebilmek için, bu özelliğin **doğru** olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="47169-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="47169-122">Bir sayfadaki ödeme teslimat bilgileri modülü örneği</span><span class="sxs-lookup"><span data-stu-id="47169-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="47169-123">Bir ödeme sayfasına teslim bilgileri modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="47169-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="47169-124">Aşağıdaki çizimde, malzeme çekme kalemindeki zaman yuvalarını içeren bir e-ticaret kullanıma alma sayfası örneği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="47169-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Malzeme çekme kalemindeki zaman yuvalarını içeren bir e-ticaret kullanıma alma sayfası örneği](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="47169-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="47169-126">Additional resources</span></span>

[<span data-ttu-id="47169-127">Müşteri malzeme çekme için zaman aralıkları oluşturma ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="47169-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="47169-128">Ödeme yapma modülü</span><span class="sxs-lookup"><span data-stu-id="47169-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="47169-129">Sipariş onayı modülü</span><span class="sxs-lookup"><span data-stu-id="47169-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="47169-130">Sipariş ayrıntıları modülü</span><span class="sxs-lookup"><span data-stu-id="47169-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]