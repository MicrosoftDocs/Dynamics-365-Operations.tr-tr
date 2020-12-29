---
title: İadeler için fişsiz ödeme yöntemlerini kısıtlama
description: Bu konu, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: dfc49e3c3132fe2687ea71e5da75fe31753d57f9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416419"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="78f92-103">İadeler için fişsiz ödeme yöntemlerini kısıtlama</span><span class="sxs-lookup"><span data-stu-id="78f92-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="78f92-104">Perakendecinin kabul edeceği ödeme türlerinin her biri, sistem ayarlandığında mutlaka yapılandırılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="78f92-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="78f92-105">Bu konu, çeşitli ödeme türlerinin, iadeler bir giriş olmadan yapıldığında bir iade için nasıl kısıtlanabileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="78f92-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="78f92-106">Ödeme yöntemlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="78f92-106">Set up payment methods</span></span>

<span data-ttu-id="78f92-107">Ödeme yöntemleri ayarlamak için, aşağıdaki görevlerin tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="78f92-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="78f92-108">Tüm organizasyon tarafından kabul edilen ödeme yöntemleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="78f92-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="78f92-109">Organizasyon kapsamında kart tipleri ve kart numaraları oluşturma.</span><span class="sxs-lookup"><span data-stu-id="78f92-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="78f92-110">Kredi kartları veya ATM kartları kabul ediliyorsa, kartlar için bir ödeme yöntemi oluşturmanız ve sonra organizasyon kapsamındaki kart tiplerini ve kart numaralarını oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="78f92-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="78f92-111">Mağaza ödeme yöntemlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="78f92-111">Set up store payment methods.</span></span> <span data-ttu-id="78f92-112">Ödeme yöntemlerini her bir mağazayla ilişkilendirin ve ardından her bir ödeme yöntemi için mağazaya özel ayarları girin.</span><span class="sxs-lookup"><span data-stu-id="78f92-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="78f92-113">Mağazalar için kart ödeme yöntemleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="78f92-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="78f92-114">Mağazanın kabul ettiği tüm kart ödeme yöntemleri için kart kurulumunu tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="78f92-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="78f92-115">![Mağaza Kurulumu](media/NoReceiptReturns1.png "Mağazada Retail kurulumu")</span><span class="sxs-lookup"><span data-stu-id="78f92-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="78f92-116">İadeler için fişsiz ödeme yöntemlerini kısıtlama</span><span class="sxs-lookup"><span data-stu-id="78f92-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="78f92-117">Her bir mağaza ödeme yöntemi için **Mağaza yönetimi** sayfasında, **Giriş olmayan iadeler** altında, **Giriş olmadan iadeleri kısıtla**'yı **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="78f92-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="78f92-118">Varsayılan değer **Hayır**'dır, bu da ödeme yönteminin iadeler için izin verilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="78f92-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="78f92-119">**Giriş olmadan iadeleri kısıtla**, **Evet** olarak ayarlanmışsa, seçilen ödeme yöntemine iadelerde izin verilmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="78f92-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="78f92-120">![Mağaza ödeme yöntemi](media/NoReceiptReturns3.png "Perakende Mağaza Ödeme Yöntemi")</span><span class="sxs-lookup"><span data-stu-id="78f92-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="78f92-121">Bir kasiyer, giriş olmayan bir iade için kısıtlanmış bir ödem yöntemini seçerse, kabul edilebilir ödeme yöntemlerini gösteren bir mesaj görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="78f92-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="78f92-122">![Kabul edilebilir ödeme yöntemleri](media/NoReceiptReturns4.png "Kabul edilebilir ödeme yöntemleri")</span><span class="sxs-lookup"><span data-stu-id="78f92-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="78f92-123">Bir işlem hem girişli iade hem de giriş olmayan iade ise, kısıtlama koşulu zorlanmaz çünkü işlem, girişli bir iade iş akışı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="78f92-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

