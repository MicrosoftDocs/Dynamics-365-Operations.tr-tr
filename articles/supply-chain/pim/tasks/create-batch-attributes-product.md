---
title: Ürün için toplu iş öznitelikleri oluşturma
description: Bu yordam, toplu iş özniteliği oluşturmak, varsayılan değer aralıkları atamak ve özniteliği bir gruba dahil etmeyi gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8924eedfbb635ca04aa167d7f6c44872fef496fd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439305"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="9522e-103">Ürün için toplu iş öznitelikleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="9522e-103">Create batch attributes for a product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9522e-104">Bu yordam, toplu iş özniteliği oluşturmak, varsayılan değer aralıkları atamak ve özniteliği bir gruba dahil etmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="9522e-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="9522e-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2 Şirketi'dir.</span><span class="sxs-lookup"><span data-stu-id="9522e-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="9522e-106">Stok yönetimi > Kurulum > Toplu iş > Toplu iş öznitelikleri’ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9522e-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="9522e-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-107">Click New.</span></span>
3. <span data-ttu-id="9522e-108">Öznitelik alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9522e-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="9522e-109">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9522e-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9522e-110">Öznitelik türü alanında 'Kesir' seçin.</span><span class="sxs-lookup"><span data-stu-id="9522e-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="9522e-111">Bu yordam kesir türünü ondalık değerleri sağlamak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="9522e-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="9522e-112">Diğer bir öznitelik türlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9522e-112">You can select other attribute types.</span></span> <span data-ttu-id="9522e-113">Numaralandırma türünü seçerseniz, Hedef alanında bir değer girmek için önce numaralandırma listesinde değerler girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="9522e-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="9522e-114">Minimum alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9522e-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="9522e-115">Maksimum alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9522e-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="9522e-116">Artış alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="9522e-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="9522e-117">Hedef alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9522e-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="9522e-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-118">Click Save.</span></span>
11. <span data-ttu-id="9522e-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9522e-119">Close the page.</span></span>
12. <span data-ttu-id="9522e-120">Stok yönetimi > Kurulum > Toplu iş > Toplu iş öznitelikleri grupları'na tıklatın.</span><span class="sxs-lookup"><span data-stu-id="9522e-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="9522e-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-121">Click New.</span></span>
14. <span data-ttu-id="9522e-122">Öznitelik grubu numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="9522e-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="9522e-123">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="9522e-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="9522e-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-124">Click Save.</span></span>
17. <span data-ttu-id="9522e-125">Grup öznitelikleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-125">Click Group attributes.</span></span>
18. <span data-ttu-id="9522e-126">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-126">Click New.</span></span>
19. <span data-ttu-id="9522e-127">Öznitelik alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9522e-128">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="9522e-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="9522e-129">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9522e-130">Bir öznitelik, gruplardan herhangi birinin içine dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="9522e-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="9522e-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="9522e-131">Click Save.</span></span>
23. <span data-ttu-id="9522e-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="9522e-132">Close the page.</span></span>

