--- 
title: "Yeni bir ürün oluştur"
description: "Bu görevde yeni bir paylaşılan ürünün nasıl oluşturulacağı gösterilmiştir."
author: ShylaThompson
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 62cfb3a8e348f5083d5681548d57715da0454a17
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-new-product"></a><span data-ttu-id="d4d27-103">Yeni bir ürün oluştur</span><span class="sxs-lookup"><span data-stu-id="d4d27-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4d27-104">Bu görevde yeni bir paylaşılan ürünün nasıl oluşturulacağı gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d4d27-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="d4d27-105">Bu işlem genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="d4d27-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="d4d27-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="d4d27-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="d4d27-107">Ürün bilgileri yönetimi > Ürünler > Ürünler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d4d27-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="d4d27-108">Ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="d4d27-108">Create a product</span></span>
1. <span data-ttu-id="d4d27-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4d27-109">Click New.</span></span>
2. <span data-ttu-id="d4d27-110">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d4d27-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="d4d27-111">Ürün numarası için bir numara serisi ayarlanmış ise ürün numaraları mutlaka el ile girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="d4d27-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="d4d27-112">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d4d27-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="d4d27-113">Ürün adı varsayılan olarak arama adı olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="d4d27-113">The product name defaults to the search name.</span></span> <span data-ttu-id="d4d27-114">Gerekirse bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d4d27-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="d4d27-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4d27-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="d4d27-116">Boyut gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="d4d27-116">Set up dimension groups</span></span>
1. <span data-ttu-id="d4d27-117">İletişim kutusunu açmak için Boyut grupları'ına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4d27-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="d4d27-118">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4d27-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="d4d27-119">Saklama boyutu grubu, saklama boyutlarının ürün için her bir harekete nasıl girilmesi gerektiğini ve bunun stokta nasıl takip edileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="d4d27-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="d4d27-120">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d4d27-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="d4d27-121">Takip boyutu grubu, her bir ürün hareketi için mutlaka girmeniz gereken takip boyutlarını ve bunların stokta nasıl işleneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="d4d27-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="d4d27-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d4d27-122">Click OK.</span></span>


