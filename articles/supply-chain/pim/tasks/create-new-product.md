--- 
title: "Yeni bir ürün oluştur"
description: "Bu görevde yeni bir paylaşılan ürünün nasıl oluşturulacağı gösterilmiştir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/08/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 56ce5d965952d0cb41278915e4631ae9d920f5f9
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2017

---
# <a name="create-a-new-product"></a><span data-ttu-id="7940b-103">Yeni bir ürün oluştur</span><span class="sxs-lookup"><span data-stu-id="7940b-103">Create a new product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7940b-104">Bu görevde yeni bir paylaşılan ürünün nasıl oluşturulacağı gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7940b-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="7940b-105">Bu işlem genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7940b-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="7940b-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="7940b-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="7940b-107">Ürün bilgileri yönetimi > Ürünler > Ürünler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7940b-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="7940b-108">Ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="7940b-108">Create a product</span></span>
1. <span data-ttu-id="7940b-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7940b-109">Click New.</span></span>
2. <span data-ttu-id="7940b-110">Ürün numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7940b-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7940b-111">Ürün numarası için bir numara serisi ayarlanmış ise ürün numaraları mutlaka el ile girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7940b-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="7940b-112">Ürün adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7940b-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="7940b-113">Ürün adı varsayılan olarak arama adı olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="7940b-113">The product name defaults to the search name.</span></span> <span data-ttu-id="7940b-114">Gerekirse bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7940b-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="7940b-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7940b-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="7940b-116">Boyut gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7940b-116">Set up dimension groups</span></span>
1. <span data-ttu-id="7940b-117">İletişim kutusunu açmak için Boyut grupları'ına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7940b-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="7940b-118">Stok boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7940b-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7940b-119">Saklama boyutu grubu, saklama boyutlarının ürün için her bir harekete nasıl girilmesi gerektiğini ve bunun stokta nasıl takip edileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="7940b-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="7940b-120">İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7940b-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7940b-121">Takip boyutu grubu, her bir ürün hareketi için mutlaka girmeniz gereken takip boyutlarını ve bunların stokta nasıl işleneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="7940b-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="7940b-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7940b-122">Click OK.</span></span>


