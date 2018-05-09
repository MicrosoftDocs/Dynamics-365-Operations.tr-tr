---
title: "Üretim farklılıklarının ortak kaynakları"
description: "Bu makale, üretim farkı türlerinin çeşitli kaynaklarını açıklamaktadır."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e7410d799cf2d1b9c6f37ac3b65cb28788f530aa
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="common-sources-of-production-variances"></a><span data-ttu-id="2bb55-103">Üretim farklılıklarının ortak kaynakları</span><span class="sxs-lookup"><span data-stu-id="2bb55-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bb55-104">Bu makale, üretim farkı türlerinin çeşitli kaynaklarını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="2bb55-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="2bb55-105">Burada bazı tipik **lot boyutu** farkı kaynakları yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="2bb55-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="2bb55-106">Üretim emrindeki sağlam ürün miktarı, standart maliyet hesaplamasında kullanılan hesaplama miktarından farklıdır.</span><span class="sxs-lookup"><span data-stu-id="2bb55-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="2bb55-107">Miktar, sabit maliyetlerin itfası için temel oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2bb55-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="2bb55-108">Üretim emrindeki sabit maliyetlerin değeri standart maliyet hesaplamasında kullanılan sabit maliyetlerden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="2bb55-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="2bb55-109">Üretim emrindeki sabit maliyetler çeşitli nedenlerle farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="2bb55-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="2bb55-110">Örneğin, sabit maliyetler aşağıdaki etkenleri yansıtabilir:</span><span class="sxs-lookup"><span data-stu-id="2bb55-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="2bb55-111">Üretim ürün reçetesi (BOM) veya rota ile ilgili el ile yapılan değişiklikler</span><span class="sxs-lookup"><span data-stu-id="2bb55-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="2bb55-112">Üretim emrini oluştururken farklı ürün reçetesi sürümü veya rota sürümü seçmeniz</span><span class="sxs-lookup"><span data-stu-id="2bb55-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="2bb55-113">Maddeye atanmış ürün reçetesi sürümü veya rota sürümü ile ilgili planlanmış mühendislik değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="2bb55-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="2bb55-114">Burada bazı tipik **üretim fiyatı** farkı kaynakları yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="2bb55-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="2bb55-115">Rota belirleme operasyonu tarafından bildirilen tüketime yönelik maliyet kategorisi (ve maliyet kategorisi fiyatı) standart maliyet hesaplamasında kullanılan maliyet kategorisinden farklıdır.</span><span class="sxs-lookup"><span data-stu-id="2bb55-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="2bb55-116">Maliyet kategorisi fiyatının etkin maliyeti standart maliyet hesaplamasında kullanılan maliyet kategorisi fiyatından farklıdır.</span><span class="sxs-lookup"><span data-stu-id="2bb55-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="2bb55-117">Burada bazı tipik **üretim miktarı** farkı kaynakları yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="2bb55-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="2bb55-118">Bir bileşen malzemesi çıkışınız fazla veya az.</span><span class="sxs-lookup"><span data-stu-id="2bb55-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="2bb55-119">Rota işlemi için fazla veya az zaman raporladınız.</span><span class="sxs-lookup"><span data-stu-id="2bb55-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="2bb55-120">Siparişin miktarına göre ana madde için mal miktarını fazla veya az aldınız.</span><span class="sxs-lookup"><span data-stu-id="2bb55-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="2bb55-121">Ancak, üretim emri için sipariş miktarına göre bileşenleri ve rapor işlemlerini tam olarak çıkış yaptınız.</span><span class="sxs-lookup"><span data-stu-id="2bb55-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="2bb55-122">Burada bazı tipik **üretim yedekleme** farkı kaynakları yer almaktadır:</span><span class="sxs-lookup"><span data-stu-id="2bb55-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="2bb55-123">Üretim ürün reçetesinde bulunmayan bir malzeme bileşeni çıkışı yaptınız.</span><span class="sxs-lookup"><span data-stu-id="2bb55-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="2bb55-124">Üretim ürün reçetesine el ile bir bileşen eklediniz ve bu bileşeni tüketildi olarak raporladınız.</span><span class="sxs-lookup"><span data-stu-id="2bb55-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="2bb55-125">Bir maddeyi tüketildi olarak raporladınız ancak üretim ürün reçetesine el ile eklemediniz.</span><span class="sxs-lookup"><span data-stu-id="2bb55-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="2bb55-126">Bir işlemi üretim rotasına el il eklediniz ve işlemi tüketildi olarak raporladınız.</span><span class="sxs-lookup"><span data-stu-id="2bb55-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="2bb55-127">Üretim emrini oluşturduğunuzda, standart maliyet hesaplamasında kullanılan ürün reçetesi sürümünden farklı bir ürün reçetesi sürümü seçtiniz.</span><span class="sxs-lookup"><span data-stu-id="2bb55-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="2bb55-128">Üretim emrini oluşturduğunuzda, standart maliyet hesaplamasında kullanılan rota sürümünden farklı bir rota sürümü seçtiniz.</span><span class="sxs-lookup"><span data-stu-id="2bb55-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>





