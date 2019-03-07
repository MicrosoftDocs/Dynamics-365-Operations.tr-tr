---
title: İadeler için fişsiz ödeme yöntemlerini kısıtlama
description: Bu konu, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.
author: rapraj
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: 1f84a6382453c0ba7540e618ad90ae1d3c684a2b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "315924"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="d1c18-103">İadeler için fişsiz ödeme yöntemlerini kısıtlama</span><span class="sxs-lookup"><span data-stu-id="d1c18-103">Restrict payment methods for returns without a receipt</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d1c18-104">Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında mutlaka yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d1c18-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="d1c18-105">Bu konu, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="d1c18-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="d1c18-106">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d1c18-106">Set up payment methods</span></span>

<span data-ttu-id="d1c18-107">Ödeme yöntemleri ayarlamak için, aşağıdaki görevlerin tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d1c18-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="d1c18-108">Tüm organizasyon tarafından kabul edilen ödeme yöntemleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d1c18-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="d1c18-109">Organizasyon kapsamında kart tipleri ve kart numaraları oluşturma.</span><span class="sxs-lookup"><span data-stu-id="d1c18-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="d1c18-110">Kredi kartları veya ATM kartları kabul ediliyorsa, kartlar için bir ödeme yöntemi oluşturmanız ve sonra organizasyon kapsamındaki kart tiplerini ve kart numaralarını oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d1c18-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="d1c18-111">Mağaza ödeme yöntemlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d1c18-111">Set up store payment methods.</span></span> <span data-ttu-id="d1c18-112">Ödeme yöntemlerini her bir mağazayla ilişkilendirin ve ardından her bir ödeme yöntemi için mağazaya özel ayarları girin.</span><span class="sxs-lookup"><span data-stu-id="d1c18-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="d1c18-113">Mağazalar için kart ödeme yöntemleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d1c18-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="d1c18-114">Mağazanın kabul ettiği tüm kart ödeme yöntemleri için kart kurulumunu tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="d1c18-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="d1c18-115">![Perakende Mağaza Kurulumu](media/NoReceiptReturns1.png "Perakende Mağaza Kurulumu")</span><span class="sxs-lookup"><span data-stu-id="d1c18-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="d1c18-116">İadeler için fişsiz ödeme yöntemlerini kısıtlama</span><span class="sxs-lookup"><span data-stu-id="d1c18-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="d1c18-117">Her bir mağaza ödeme yöntemi için **Perakende mağaza yönetimi** sayfasında, **Giriş olmayan iadeler** altında, **Giriş olmadan iadeleri kısıtla**'yı **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d1c18-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="d1c18-118">Varsayılan değer **Hayır**'dır, bu da ödeme yönteminin iadeler için izin verilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="d1c18-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="d1c18-119">**Giriş olmadan iadeleri kısıtla**, **Evet** olarak ayarlanmışsa, seçilen ödeme yöntemine iadelerde izin verilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="d1c18-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="d1c18-120">![Perakende Mağazası ödeme yöntemi](media/NoReceiptReturns3.png "Perakende Mağazası ödeme yöntemi")</span><span class="sxs-lookup"><span data-stu-id="d1c18-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="d1c18-121">Bir kasiyer, giriş olmayan bir iade için kısıtlanmış bir ödem yöntemini seçerse, kabul edilebilir ödeme yöntemlerini gösteren bir mesaj görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d1c18-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="d1c18-122">![Kabul edilebilir ödeme yöntemleri](media/NoReceiptReturns4.png "Kabul edilebilir ödeme yöntemleri")</span><span class="sxs-lookup"><span data-stu-id="d1c18-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="d1c18-123">Bir işlem hem girişli iade hem de giriş olmayan iade ise, kısıtlama koşulu zorlanmaz çünkü işlem, girişli bir iade iş akışı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d1c18-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

