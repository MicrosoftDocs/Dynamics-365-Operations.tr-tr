--- 
title: "Ürün için toplu iş öznitelikleri oluşturma"
description: "Bu yordam, toplu iş özniteliği oluşturmak, varsayılan değer aralıkları atamak ve özniteliği bir gruba dahil etmeyi gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: fcd0afb8005f1712b08f0854613573ef04c0cad6
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="86a42-103">Ürün için toplu iş öznitelikleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="86a42-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86a42-104">Bu yordam, toplu iş özniteliği oluşturmak, varsayılan değer aralıkları atamak ve özniteliği bir gruba dahil etmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="86a42-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="86a42-105">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi USP2 Şirketi'dir.</span><span class="sxs-lookup"><span data-stu-id="86a42-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="86a42-106">Stok yönetimi > Kurulum > Toplu iş > Toplu iş öznitelikleri’ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86a42-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="86a42-107">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-107">Click New.</span></span>
3. <span data-ttu-id="86a42-108">Öznitelik alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="86a42-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="86a42-109">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="86a42-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="86a42-110">Öznitelik türü alanında 'Kesir' seçin.</span><span class="sxs-lookup"><span data-stu-id="86a42-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="86a42-111">Bu yordam kesir türünü ondalık değerleri sağlamak için kullanır.</span><span class="sxs-lookup"><span data-stu-id="86a42-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="86a42-112">Diğer bir öznitelik türlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86a42-112">You can select other attribute types.</span></span> <span data-ttu-id="86a42-113">Numaralandırma türünü seçerseniz, Hedef alanında bir değer girmek için önce numaralandırma listesinde değerler girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="86a42-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="86a42-114">Minimum alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="86a42-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="86a42-115">Maksimum alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="86a42-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="86a42-116">Artış alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="86a42-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="86a42-117">Hedef alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="86a42-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="86a42-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-118">Click Save.</span></span>
11. <span data-ttu-id="86a42-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86a42-119">Close the page.</span></span>
12. <span data-ttu-id="86a42-120">Stok yönetimi > Kurulum > Toplu iş > Toplu iş öznitelikleri grupları'na tıklatın.</span><span class="sxs-lookup"><span data-stu-id="86a42-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="86a42-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-121">Click New.</span></span>
14. <span data-ttu-id="86a42-122">Öznitelik grubu numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="86a42-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="86a42-123">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="86a42-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="86a42-124">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-124">Click Save.</span></span>
17. <span data-ttu-id="86a42-125">Grup öznitelikleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-125">Click Group attributes.</span></span>
18. <span data-ttu-id="86a42-126">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-126">Click New.</span></span>
19. <span data-ttu-id="86a42-127">Öznitelik alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="86a42-128">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="86a42-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="86a42-129">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="86a42-130">Bir öznitelik, gruplardan herhangi birinin içine dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="86a42-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="86a42-131">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="86a42-131">Click Save.</span></span>
23. <span data-ttu-id="86a42-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="86a42-132">Close the page.</span></span>


