---
title: Varsayılan ürün yaşam döngüsü durumu oluşturma
description: Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b62d47f52da7f9e18bce401578a5e2a629ac5eb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818145"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="f3b83-103">Varsayılan ürün yaşam döngüsü durumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="f3b83-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3b83-104">Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="f3b83-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="f3b83-105">Varsayılan yaşam döngüsü durumu oluşturma</span><span class="sxs-lookup"><span data-stu-id="f3b83-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="f3b83-106">Ürün bilgileri yönetimi > Kurulum > Ürün yaşam döngüsü durumu seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="f3b83-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f3b83-107">Click New.</span></span>
3. <span data-ttu-id="f3b83-108">Durum alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f3b83-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="f3b83-109">Tüzel kişiliğe serbest bırakıldığında varsayılan alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="f3b83-110">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f3b83-111">Planlama için etkin alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="f3b83-112">Yeni serbest bırakılan ürünün Master planlama dışında tutulması gerekiyorsa Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="f3b83-113">Master planlamaya dahil edilmesi gerekiyorsa denetimi varsayılan değer olan Evet'te bırakın.</span><span class="sxs-lookup"><span data-stu-id="f3b83-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="f3b83-114">Yeni bir serbest bırakılan ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="f3b83-114">Create a new released product</span></span>
1. <span data-ttu-id="f3b83-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f3b83-115">Close the page.</span></span>
2. <span data-ttu-id="f3b83-116">Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="f3b83-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f3b83-117">Click New.</span></span>
4. <span data-ttu-id="f3b83-118">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="f3b83-119">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="f3b83-120">Arama adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f3b83-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="f3b83-121">Model grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="f3b83-122">Ürün grubu alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="f3b83-123">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="f3b83-124">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="f3b83-125">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f3b83-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="f3b83-126">Varsayılan ürün yaşam döngüsü durumu genel bir tanımdır.</span><span class="sxs-lookup"><span data-stu-id="f3b83-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="f3b83-127">Ürünü etkin duruma değiştirme</span><span class="sxs-lookup"><span data-stu-id="f3b83-127">Change the product to an active state</span></span>
1. <span data-ttu-id="f3b83-128">Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f3b83-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="f3b83-129">Etkin bir durum ayarladığınızı varsayalım: şimdi etkin durumu ürününün Master planlama ve ürün reçetesi seviyesinde hesaplamada kullanılmasına izin vermek üzere seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f3b83-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="f3b83-130">Bu, yalnızca tutarlı planlama için gerekli tüm ürün ayrıntılarının belirtilmiş olması durumunda bir anlam ifade etmektedir.</span><span class="sxs-lookup"><span data-stu-id="f3b83-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]