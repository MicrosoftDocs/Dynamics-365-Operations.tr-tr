---
title: Toplu iş öznitelikleri
description: Bu konuda toplu iş öznitelikleri hakkında bilgiler verilmiştir. Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir. Bu konuda ayrıca toplu iş özniteliklerinin nasıl atanacağı ve toplu işleri rezerve ettiğinizde bunları nasıl arayacağınız açıklanmaktadır.
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 325e647185e3eb4c0eacdfd00c320804e31ddb48
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "347641"
---
# <a name="batch-attributes"></a><span data-ttu-id="c158c-105">Toplu iş öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="c158c-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c158c-106">Bu konuda toplu iş öznitelikleri hakkında bilgiler verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="c158c-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="c158c-107">Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="c158c-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="c158c-108">Bu konuda ayrıca toplu iş özniteliklerinin nasıl atanacağı ve toplu işleri rezerve ettiğinizde bunları nasıl arayacağınız açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="c158c-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="c158c-109">Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="c158c-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="c158c-110">Toplu iş öznitelikleri, ortam koşulları veya toplu işi oluşturmak için kullanılan hammaddelerin kalitesi ya da bitmiş ürünün sonucu gibi çeşitli etkenlere bağlı olarak değişiklik gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="c158c-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="c158c-111">Kullanılan toplu iş özniteliklerinin sayısı ve tipleri, endüstriler arasında büyük değişiklikler gösterebilir.</span><span class="sxs-lookup"><span data-stu-id="c158c-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="c158c-112">Toplu iş özniteliklerinin nasıl kullanıldığını gösteren iki örnek aşağıda verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c158c-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="c158c-113">Peynir endüstrisinde, peynir üretmekte kullanılan hammaddelerden biri olan süt, yağ içeriği ve yüzde ağırlık gibi özniteliklere sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="c158c-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="c158c-114">Sütten üretilen peynirin nem ve yaş gibi başka öznitelikleri olabilir.</span><span class="sxs-lookup"><span data-stu-id="c158c-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="c158c-115">Çelik endüstrisinde, ürettiğiniz demir magnezyum, gümüş ve çinko içeriği yüzdeleri gibi özniteliklere sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="c158c-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="c158c-116">Öznitelik sayısını ve türünü daha iyi yönetmek için, toplu iş öznitelik grupları kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c158c-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="c158c-117">Bu şekilde, her bir özniteliği tek tek eklemeniz gerekmez.</span><span class="sxs-lookup"><span data-stu-id="c158c-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="c158c-118">Toplu iş öznitelikleri atama</span><span class="sxs-lookup"><span data-stu-id="c158c-118">Assign batch attributes</span></span>
<span data-ttu-id="c158c-119">Toplu iş özniteliklerini, stok toplu işlerinde tutulan ürünlere tek tek atayabilir veya bunları belirli müşterilerle ilişkili ürünlere atarsınız.</span><span class="sxs-lookup"><span data-stu-id="c158c-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="c158c-120">Müşteri düzeyinde bir toplu iş özniteliği atamadan önce, ürün düzeyinde atamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c158c-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="c158c-121">Ürünün toplu iş boyutu izleme boyut grubunda **Etkin** olarak ayarlanmış olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c158c-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="c158c-122">Ayrı bir ürüne bir toplu iş özniteliği atamak için, ürüne özel sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="c158c-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="c158c-123">Öznitelik, bir müşteriye yönelik bir ürüne özelse, müşteriye özel sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="c158c-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="c158c-124">Bir ürüne öznitelik eklediğinizde, diğer parametreleri de tanımlarsınız.</span><span class="sxs-lookup"><span data-stu-id="c158c-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="c158c-125">Burada bazı örnekler verilmiştir:</span><span class="sxs-lookup"><span data-stu-id="c158c-125">Here are some examples:</span></span>

-   <span data-ttu-id="c158c-126">**Tamsayı** veya **Kesir** türünün özniteliği için minimum veya maksimum aralıklar.</span><span class="sxs-lookup"><span data-stu-id="c158c-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="c158c-127">**Tamsayı** veya **Kesir** türündeki bir öznitelik için tolerans eylemleri.</span><span class="sxs-lookup"><span data-stu-id="c158c-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="c158c-128">Özniteliğin değeri minimum ve maksimum aralığı dışında kalıyorsa, eylem bir uyarı mesajı veya hata mesajı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c158c-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="c158c-129">Öznitelik için hedef değer.</span><span class="sxs-lookup"><span data-stu-id="c158c-129">The target value for the attribute.</span></span> <span data-ttu-id="c158c-130">Bu değer, özniteliğin optimum değeridir ve tüm öznitelik türleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="c158c-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="c158c-131">**Serbest bırakılan ürünler** sayfasında seçtiğiniz ürünlere yönelik sayfalara Ürün bilgileri yönetiminde erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c158c-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="c158c-132">Bir ürüne toplu iş öznitelikleri atadıktan sonra, **Stok toplu iş öznitelikleri** sayfasında özniteliklere belirli değerler ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c158c-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="c158c-133">Toplu iş rezerve etme</span><span class="sxs-lookup"><span data-stu-id="c158c-133">Reserve batches</span></span>
<span data-ttu-id="c158c-134">Bir müşterinin siparişini yerine getirmek üzere bir satış emrine yönelik toplu iş rezervasyonları yaparken veya bir üretim emri için toplu işler çekip rezerve ederken toplu iş özniteliklerinde arama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c158c-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="c158c-135">Arama istediğiniz toplu iş özniteliğine sahip ürünü içeren bir stok toplu işini bulmaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="c158c-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="c158c-136">Toplu işi veya toplu işleri bulduktan sonra, ürünü kaynak stok hareket satırı için rezerve edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c158c-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>



