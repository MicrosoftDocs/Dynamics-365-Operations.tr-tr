---
title: Varsayılan ürün yaşam döngüsü durumu oluşturma
description: Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564190"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="fa075-103">Varsayılan ürün yaşam döngüsü durumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa075-103">Create a default product lifecycle state</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa075-104">Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="fa075-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="fa075-105">Varsayılan yaşam döngüsü durumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa075-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="fa075-106">Ürün bilgileri yönetimi > Kurulum > Ürün yaşam döngüsü durumu seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="fa075-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="fa075-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fa075-107">Click New.</span></span>
3. <span data-ttu-id="fa075-108">Durum alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fa075-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="fa075-109">Tüzel kişiliğe serbest bırakıldığında varsayılan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="fa075-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fa075-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="fa075-111">Planlama için etkin alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="fa075-112">Yeni serbest bırakılan ürünün Master planlama dışında tutulması gerekiyorsa Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="fa075-113">Master planlamaya dahil edilmesi gerekiyorsa denetimi varsayılan değer olan Evet'te bırakın.</span><span class="sxs-lookup"><span data-stu-id="fa075-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="fa075-114">Yeni bir serbest bırakılan ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="fa075-114">Create a new released product</span></span>
1. <span data-ttu-id="fa075-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="fa075-115">Close the page.</span></span>
2. <span data-ttu-id="fa075-116">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="fa075-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="fa075-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fa075-117">Click New.</span></span>
4. <span data-ttu-id="fa075-118">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fa075-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="fa075-119">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="fa075-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="fa075-120">Arama adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="fa075-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="fa075-121">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="fa075-122">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="fa075-123">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="fa075-124">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="fa075-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="fa075-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="fa075-126">Varsayılan ürün yaşam döngüsü durumu genel bir tanımdır.</span><span class="sxs-lookup"><span data-stu-id="fa075-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="fa075-127">Ürünü etkin duruma değiştirme</span><span class="sxs-lookup"><span data-stu-id="fa075-127">Change the product to an active state</span></span>
1. <span data-ttu-id="fa075-128">Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="fa075-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="fa075-129">Etkin bir durum ayarladığınızı varsayalım: şimdi etkin durumu ürününün Master planlama ve ürün reçetesi seviyesinde hesaplamada kullanılmasına izin vermek üzere seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fa075-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="fa075-130">Bu, yalnızca tutarlı planlama için gerekli tüm ürün ayrıntılarının belirtilmiş olması durumunda bir anlam ifade etmektedir.</span><span class="sxs-lookup"><span data-stu-id="fa075-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  

