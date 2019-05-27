---
title: Ürün için barkod oluşturma
description: Bu yordam, örnek olarak M0001 madde numarasını kullanarak el ile nasıl bir barkod oluşturulacağını gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae2765a125045d60566267d01e380069d5d527c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568616"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="d68c3-103">Ürün için barkod oluşturma</span><span class="sxs-lookup"><span data-stu-id="d68c3-103">Create a bar code for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d68c3-104">Bu yordam, örnek olarak M0001 madde numarasını kullanarak el ile nasıl bir barkod oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d68c3-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="d68c3-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="d68c3-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d68c3-106">Serbest bırakılan ürün bakımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="d68c3-107">Sevk edilen ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-107">Click Released products.</span></span>
3. <span data-ttu-id="d68c3-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d68c3-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d68c3-109">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="d68c3-110">Barkodlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-110">Click Bar codes.</span></span>
6. <span data-ttu-id="d68c3-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-111">Click New.</span></span>
7. <span data-ttu-id="d68c3-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d68c3-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d68c3-113">Barkod ayarı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d68c3-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="d68c3-114">Barkod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d68c3-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="d68c3-115">Barkod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="d68c3-116">Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="d68c3-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-117">Close the page.</span></span>
12. <span data-ttu-id="d68c3-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="d68c3-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="d68c3-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-119">Click Save.</span></span>
    * <span data-ttu-id="d68c3-120">Kaydet'e tıkladığınızda barkod denetimi çalıştırılır ve bu örnekte beklenen denetleme basamağının 8 olduğunu ancak denetleme basamağında 3 sayısının olduğunu bildiren bir hata görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="d68c3-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="d68c3-121">Barkod numarasını son basamakta 8 sayısı olacak şekilde el ile güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="d68c3-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="d68c3-122">Barkod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="d68c3-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="d68c3-123">Barkod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="d68c3-124">Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="d68c3-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-125">Close the page.</span></span>
17. <span data-ttu-id="d68c3-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-126">Click Save.</span></span>
18. <span data-ttu-id="d68c3-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="d68c3-127">Close the page.</span></span>

