--- 
title: "Ürün için barkod oluşturma"
description: "Bu yordam, örnek olarak M0001 madde numarasını kullanarak el ile nasıl bir barkod oluşturulacağını gösterir."
author: YuyuScheller
manager: AnnBe
ms.date: 09/26/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6a55e25205bc7e996b6ab8c6915e2e86b758ee7a
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="dd4fb-103">Ürün için barkod oluşturma</span><span class="sxs-lookup"><span data-stu-id="dd4fb-103">Create a bar code for a product</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd4fb-104">Bu yordam, örnek olarak M0001 madde numarasını kullanarak el ile nasıl bir barkod oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="dd4fb-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="dd4fb-106">Serbest bırakılan ürün bakımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="dd4fb-107">Sevk edilen ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-107">Click Released products.</span></span>
3. <span data-ttu-id="dd4fb-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="dd4fb-109">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="dd4fb-110">Barkodlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-110">Click Bar codes.</span></span>
6. <span data-ttu-id="dd4fb-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-111">Click New.</span></span>
7. <span data-ttu-id="dd4fb-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="dd4fb-113">Barkod ayarı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="dd4fb-114">Barkod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="dd4fb-115">Barkod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="dd4fb-116">Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="dd4fb-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-117">Close the page.</span></span>
12. <span data-ttu-id="dd4fb-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="dd4fb-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-119">Click Save.</span></span>
    * <span data-ttu-id="dd4fb-120">Kaydet'e tıkladığınızda barkod denetimi çalıştırılır ve bu örnekte beklenen denetleme basamağının 8 olduğunu ancak denetleme basamağında 3 sayısının olduğunu bildiren bir hata görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="dd4fb-121">Barkod numarasını son basamakta 8 sayısı olacak şekilde el ile güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="dd4fb-122">Barkod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="dd4fb-123">Barkod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="dd4fb-124">Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="dd4fb-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-125">Close the page.</span></span>
17. <span data-ttu-id="dd4fb-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-126">Click Save.</span></span>
18. <span data-ttu-id="dd4fb-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="dd4fb-127">Close the page.</span></span>


