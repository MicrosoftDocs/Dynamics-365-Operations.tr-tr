--- 
title: "Mevcut bir formül sürümünden ortak ürünler kopyalama"
description: "Bu yordam, size ortak ürünleri bir formül sürümünden sevk edilen bir ürün için farklı bir formül sürümüne nasıl kopyalayacağınızı gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: adcfa7441c2beaa9e4f8602aa19d23a10fb7e6c5
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="7fe7b-103">Mevcut bir formül sürümünden ortak ürünler kopyalama</span><span class="sxs-lookup"><span data-stu-id="7fe7b-103">Copy co-products from an existing formula version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fe7b-104">Bu yordam, size ortak ürünleri bir formül sürümünden sevk edilen bir ürün için farklı bir formül sürümüne nasıl kopyalayacağınızı gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="7fe7b-105">Ortak ürünlerle ilişkili en az bir formül sürümü bulunması önkoşulu vardır.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="7fe7b-106">Bu yordamı oluşturmak için kullanılan demo verisi şirketi USP2'dir.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="7fe7b-107">Sevk edilen ürünleri bulma</span><span class="sxs-lookup"><span data-stu-id="7fe7b-107">Find a released product</span></span>
1. <span data-ttu-id="7fe7b-108">Serbest bırakılan ürünler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-108">Go to Released products.</span></span>
2. <span data-ttu-id="7fe7b-109">Filtreleri göster'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-109">Click Show filters.</span></span>
    * <span data-ttu-id="7fe7b-110">Filtre iletişim kutusunda alan Üretim türü eklemek üzeresiniz.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="7fe7b-111">Filtre ekle alanını, Üretim türüne alanı eklemek için tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="7fe7b-112">Sonraki adımda Uygula'yı seçmeden önce Üretim türü alanında Formülü el ile girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="7fe7b-113">Bu, filtre üzerinde yayınlanan ürünlerin listesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="7fe7b-114">Üretim türü alanına Formülü el ile girin.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="7fe7b-115">Uygula düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="7fe7b-116">Sevk edilen ürünleri seçme</span><span class="sxs-lookup"><span data-stu-id="7fe7b-116">Select a released product</span></span>
1. <span data-ttu-id="7fe7b-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="7fe7b-118">Formül sürümleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-118">Click Formula versions.</span></span>
    * <span data-ttu-id="7fe7b-119">Mühendislik İşlemi Bölmesinde Formül sürümleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="7fe7b-120">Ortak ürünleri kopyalama</span><span class="sxs-lookup"><span data-stu-id="7fe7b-120">Copy co-products</span></span>
1. <span data-ttu-id="7fe7b-121">Eylem Bölmesi'nde Formül sürümleri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="7fe7b-122">Ortak ürünler’i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-122">Click Co-products.</span></span>
3. <span data-ttu-id="7fe7b-123">Kopyala'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-123">Click Copy.</span></span>
4. <span data-ttu-id="7fe7b-124">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="7fe7b-125">Formül sürümü alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="7fe7b-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-126">Click OK.</span></span>
7. <span data-ttu-id="7fe7b-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7fe7b-127">Close the page.</span></span>


