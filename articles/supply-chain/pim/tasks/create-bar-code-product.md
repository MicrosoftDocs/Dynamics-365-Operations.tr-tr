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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "329402"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="0f746-103">Ürün için barkod oluşturma</span><span class="sxs-lookup"><span data-stu-id="0f746-103">Create a bar code for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f746-104">Bu yordam, örnek olarak M0001 madde numarasını kullanarak el ile nasıl bir barkod oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f746-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="0f746-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="0f746-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="0f746-106">Serbest bırakılan ürün bakımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f746-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="0f746-107">Sevk edilen ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f746-107">Click Released products.</span></span>
3. <span data-ttu-id="0f746-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="0f746-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0f746-109">Eylem Bölmesinde, Stok yönetimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f746-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="0f746-110">Barkodlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f746-110">Click Bar codes.</span></span>
6. <span data-ttu-id="0f746-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f746-111">Click New.</span></span>
7. <span data-ttu-id="0f746-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="0f746-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="0f746-113">Barkod ayarı alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="0f746-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="0f746-114">Barkod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0f746-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="0f746-115">Barkod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0f746-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="0f746-116">Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="0f746-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="0f746-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0f746-117">Close the page.</span></span>
12. <span data-ttu-id="0f746-118">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="0f746-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="0f746-119">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f746-119">Click Save.</span></span>
    * <span data-ttu-id="0f746-120">Kaydet'e tıkladığınızda barkod denetimi çalıştırılır ve bu örnekte beklenen denetleme basamağının 8 olduğunu ancak denetleme basamağında 3 sayısının olduğunu bildiren bir hata görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0f746-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="0f746-121">Barkod numarasını son basamakta 8 sayısı olacak şekilde el ile güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="0f746-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="0f746-122">Barkod alanına bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="0f746-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="0f746-123">Barkod alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="0f746-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="0f746-124">Sekme tuşuna basın.</span><span class="sxs-lookup"><span data-stu-id="0f746-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="0f746-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0f746-125">Close the page.</span></span>
17. <span data-ttu-id="0f746-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0f746-126">Click Save.</span></span>
18. <span data-ttu-id="0f746-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0f746-127">Close the page.</span></span>

