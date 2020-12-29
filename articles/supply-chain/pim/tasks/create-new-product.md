---
title: Yeni ürün oluşturma
description: Bu konuda, yeni bir paylaşılan ürün oluşturma yöntemi açıklanmıştır.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a4745fe4fc44f85bcfd388ee573f5a6d0cd8519
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439299"
---
# <a name="create-a-new-product"></a><span data-ttu-id="371b9-103">Yeni ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="371b9-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="371b9-104">Bu konuda, yeni bir paylaşılan ürün oluşturma yöntemi açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="371b9-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="371b9-105">Bu işlem genellikle bir ürün tasarımcısı tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="371b9-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="371b9-106">Bu görevi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="371b9-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="371b9-107">Ürün oluşturma</span><span class="sxs-lookup"><span data-stu-id="371b9-107">Create a product</span></span>
1. <span data-ttu-id="371b9-108">Gezinti bölmesinde **Modüller >Ürün bilgileri yönetimi > Ürünler > Ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="371b9-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="371b9-109">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="371b9-109">Select **New**.</span></span>
3. <span data-ttu-id="371b9-110">**Ürün numarası** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="371b9-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="371b9-111">Ürün numarası için bir numara serisi ayarlanmış ise ürün numaraları mutlaka el ile girilmelidir.</span><span class="sxs-lookup"><span data-stu-id="371b9-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="371b9-112">**Ürün adı** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="371b9-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="371b9-113">Ürün adı varsayılan olarak arama adı olarak atanır.</span><span class="sxs-lookup"><span data-stu-id="371b9-113">The product name defaults to the search name.</span></span> <span data-ttu-id="371b9-114">Gerekirse bunu değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="371b9-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="371b9-115">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="371b9-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="371b9-116">Boyut gruplarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="371b9-116">Set up dimension groups</span></span>
1. <span data-ttu-id="371b9-117">İletişim kutusunu açmak için **Boyut grupları**'ını seçin.</span><span class="sxs-lookup"><span data-stu-id="371b9-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="371b9-118">**Stok boyutu grubu alanı**'na bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="371b9-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="371b9-119">Saklama boyutu grubu, saklama boyutlarının ürün için her bir harekete nasıl girilmesi gerektiğini ve bunun stokta nasıl takip edileceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="371b9-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="371b9-120">**İzleme boyutu grubu** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="371b9-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="371b9-121">Takip boyutu grubu, her bir ürün hareketi için mutlaka girmeniz gereken takip boyutlarını ve bunların stokta nasıl işleneceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="371b9-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="371b9-122">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="371b9-122">Select **OK**.</span></span>

