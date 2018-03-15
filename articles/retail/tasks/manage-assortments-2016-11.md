--- 
title: " Ürün çeşitlerini yönetme "
description: "Bu yordam yeni bir ürün sınıfının nasıl oluşturulduğunu ve yayınlandığını gösterir ve tanıtım verisi şirketi USRT'yi kullanır."
author: jashanno
manager: AnnBe
ms.date: 10/31/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1c353a135559a1901f98ae6e7c9671254ab625c3
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="manage-assortments"></a><span data-ttu-id="08c78-103"> Ürün çeşitlerini yönetme </span><span class="sxs-lookup"><span data-stu-id="08c78-103">Manage assortments</span></span> 

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="08c78-104">Bu yordam yeni bir ürün sınıfının nasıl oluşturulduğunu ve yayınlandığını gösterir ve tanıtım verisi şirketi USRT'yi kullanır.</span><span class="sxs-lookup"><span data-stu-id="08c78-104">This procedure demonstrates how to create and publish a new product assortment and uses the demo data company USRT.</span></span> <span data-ttu-id="08c78-105">Bu yordam Dynamics AX uygulaması 7.0.1 veya sonraki bir sürümü ve Dynamics AX platformu 7.1'i gerektirir.</span><span class="sxs-lookup"><span data-stu-id="08c78-105">This procedure requires Dynamics AX application 7.0.1 or later, and Dynamics AX platform 7.1.</span></span>  

1. <span data-ttu-id="08c78-106">Kategori ve ürün yönetimine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-106">Click Category and product management.</span></span>

## <a name="create-an-assortment"></a><span data-ttu-id="08c78-107">Bir sınıflama seçin</span><span class="sxs-lookup"><span data-stu-id="08c78-107">Create an assortment</span></span>
1. <span data-ttu-id="08c78-108">Sınıflamalar sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-108">Click the Assortments tab.</span></span>
2. <span data-ttu-id="08c78-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-109">Click New.</span></span>
3. <span data-ttu-id="08c78-110">Ürün çeşidi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-110">Click Assortment.</span></span>
    * <span data-ttu-id="08c78-111">Ürün Çeşidi Kodu gerekir ve benzersiz bir değer olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="08c78-111">The Assortment ID is required and must be a unique value.</span></span>  
4. <span data-ttu-id="08c78-112">Sınıflama adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="08c78-112">In the Assortment name field, type a value.</span></span>
5. <span data-ttu-id="08c78-113">Yürürlük tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="08c78-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="08c78-114">Bitiş tarihi alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="08c78-114">In the Expiration date field, enter a date.</span></span>
7. <span data-ttu-id="08c78-115">Perakende kanalları bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="08c78-115">Expand the Retail channels section.</span></span>
8. <span data-ttu-id="08c78-116">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-116">Click Add line.</span></span>
9. <span data-ttu-id="08c78-117">Ağaçta 'Contoso Retail\Electronics\Boston' seçin.</span><span class="sxs-lookup"><span data-stu-id="08c78-117">In the tree, select 'Contoso Retail\Electronics\Boston'.</span></span>
10. <span data-ttu-id="08c78-118">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08c78-118">Click Add.</span></span>
11. <span data-ttu-id="08c78-119">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-119">Click OK.</span></span>
12. <span data-ttu-id="08c78-120">Ürünler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="08c78-120">Expand the Products section.</span></span>
13. <span data-ttu-id="08c78-121">Satır ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-121">Click Add line.</span></span>
14. <span data-ttu-id="08c78-122">Kategori alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="08c78-122">In the Category field, enter or select a value.</span></span>
15. <span data-ttu-id="08c78-123">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-123">Click Save.</span></span>

## <a name="publish-an-assortment"></a><span data-ttu-id="08c78-124">Bir sınıflama yayınlayın</span><span class="sxs-lookup"><span data-stu-id="08c78-124">Publish an assortment</span></span>
1. <span data-ttu-id="08c78-125">Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="08c78-125">Click Publish.</span></span>
2. <span data-ttu-id="08c78-126">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="08c78-126">Click Yes.</span></span>


