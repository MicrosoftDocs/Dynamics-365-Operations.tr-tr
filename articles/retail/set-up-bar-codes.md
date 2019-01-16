---
title: "Barkodlar oluşturma"
description: "Bu makalede, Microsoft Dynamics 365 for Retail'de barkodların nasıl kullanılacağı açıklanmaktadır."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailBarcodeMaskCharacter, RetailBarcodeMaskSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15971
ms.assetid: 6b4b2ac2-0344-41aa-8818-62c30017d5ac
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 15d12abe32d3f5a47348016c67a4fb02d0a5d8e3
ms.contentlocale: tr-tr
ms.lasthandoff: 01/04/2019

---

# <a name="set-up-bar-codes"></a><span data-ttu-id="0f8c1-103">Barkodlar ayarlama</span><span class="sxs-lookup"><span data-stu-id="0f8c1-103">Set up bar codes</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f8c1-104">Bu makalede, Microsoft Dynamics 365 for Retail'de barkodların nasıl kullanılacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-104">This article describes how to use bar codes in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="0f8c1-105">Ürün satın almak ve satmak, ürün çeşitlerini takip etmek ve müşteri ve çalışan verileri oluşturmak için barkodları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-105">You can use bar codes to purchase and sell products, track product variants, and set up customers and employees.</span></span> <span data-ttu-id="0f8c1-106">Barkodları kuponlar, hediye kartları ve credit memo'lar oluşturmak ve bunları kullandırmak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-106">You can also use bar codes to issue and endorse coupons, gift cards, and credit memos.</span></span> <span data-ttu-id="0f8c1-107">Standart bankodları veya özel, şirkete has barkodları olacak şekilde perakende ürünleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-107">You can set up retail products so that they have standard bar codes or custom, in-house bar codes.</span></span> <span data-ttu-id="0f8c1-108">Ürünler birden fazla barkod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-108">Products can have more than one bar code.</span></span> <span data-ttu-id="0f8c1-109">Örneğin, bir ürün farklı üreticilerden geliyorsa veya boyutuna, tarzına veya rengine bağlı olarak çeşitlere sahipse birden fazla barkod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-109">For example, a product might have multiple bar codes if it comes from various manufacturers, or if it has variants that are based on size, style, or color.</span></span> <span data-ttu-id="0f8c1-110">Barkodlar, ürünün ağırlığını veya fiyatını içerebilir.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-110">Bar codes can include the weight or price of the product.</span></span> <span data-ttu-id="0f8c1-111">Barkod işaretleri, barkodlar oluşturmak için kullanılan şablonlarıdır.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-111">Bar code masks are templates that are used to create bar codes.</span></span>

> [!NOTE]
> <span data-ttu-id="0f8c1-112">Her çeşit birleşimine benzersiz bir barkod atayarak, kasada barkodu tarayabilir ve programın, ürünün hangi çeşidinin satıldığını bulmasını sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-112">If you assign a unique bar code to each variant combination, you can scan the bar code at the register and let the program determine which variant of the product is being sold.</span></span> <span data-ttu-id="0f8c1-113">Ayrıca ürüne göre satışlar hakkında istatistikler toplayabilir ve bunları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-113">You can also collect and view statistics about sales by variant.</span></span> <span data-ttu-id="0f8c1-114">Her boyut, renk ve stil grubuna barkodda bu grubu tanımlayan, benzersiz bir numara atanabilir.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-114">Each size, color, and style group can be assigned a unique number that identifies that group in the bar code.</span></span> <span data-ttu-id="0f8c1-115">Dynamics 365 for Retail her çeşit birleşimi için otomatik olarak barkodlar oluşturmak üzere barkod maskesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-115">Dynamics 365 for Retail uses the bar code mask to automatically generate bar codes for each variant combination.</span></span> <span data-ttu-id="0f8c1-116">Her bir çeşit koduyla bileşen sayısı önemli ölçüde arttığından pek çok boyut, renk ve stil söz konusu olduğunda bu işlev kullanışlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-116">This functionality can be useful if there are many sizes, colors, and styles, because the number of combinations increases significantly as each variant code is added.</span></span> <span data-ttu-id="0f8c1-117">Bu işlev kullanılmazsa, bir ürün çeşidini temsil eden her birleşime barkodların el ile atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-117">If this functionality isn't used, bar codes must be manually assigned to each combination that represents a product variant.</span></span>

<span data-ttu-id="0f8c1-118">Barkodları el ile veya otomatik olarak oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-118">You can create bar codes manually or automatically.</span></span> <span data-ttu-id="0f8c1-119">Barkodlar oluşturmak için, aşağıdaki görevleri listelendikleri sırayla tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-119">To create bar codes, complete the following tasks in the order in which they are listed.</span></span>

1. <span data-ttu-id="0f8c1-120">[Barkod maskesi karakterlerini ayarlama](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="0f8c1-120">[Set up bar code mask characters](set-up-bar-code-masks.md).</span></span>
2. <span data-ttu-id="0f8c1-121">[Barkod maskesi ayarlama](set-up-bar-code-masks.md).</span><span class="sxs-lookup"><span data-stu-id="0f8c1-121">[Set up bar code masks](set-up-bar-code-masks.md).</span></span>
3. <span data-ttu-id="0f8c1-122">Barkod kurulumlarını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-122">Configure bar code setups.</span></span>
4. <span data-ttu-id="0f8c1-123">Ürünler için barkodlar oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0f8c1-123">Create bar codes for products.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f8c1-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0f8c1-124">Additional resources</span></span>

[<span data-ttu-id="0f8c1-125">Barkod maskeleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="0f8c1-125">Set up bar code masks</span></span>](set-up-bar-code-masks.md)

