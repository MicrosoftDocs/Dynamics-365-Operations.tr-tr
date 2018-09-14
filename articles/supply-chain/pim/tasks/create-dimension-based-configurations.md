--- 
title: "Boyut tabanlı yapılandırmalar oluşturma"
description: "Bu prosedürde bir boyut tabanlı ürün için bir yapılandırmanın nasıl tanımlanacağı açıklanmıştır."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9190d6dfd4b3f6cf0634e86845e7de028631bdd4
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="225fb-103">Boyut tabanlı yapılandırmalar oluşturma</span><span class="sxs-lookup"><span data-stu-id="225fb-103">Create dimension-based configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="225fb-104">Bu prosedürde bir boyut tabanlı ürün için bir yapılandırmanın nasıl tanımlanacağı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="225fb-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="225fb-105">Bu prosedür, boyut tabanlı yapılandırma kombinasyonlarının nasıl oluşturacağını açıklayan serinin son prosedürüdür.</span><span class="sxs-lookup"><span data-stu-id="225fb-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="225fb-106">Bu prosedürün uygulanması önceki yedi kayıtta oluşturulan verilere bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="225fb-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="225fb-107">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="225fb-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="225fb-108">Boyut tabanlı ürün mastarını bulma</span><span class="sxs-lookup"><span data-stu-id="225fb-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="225fb-109">Serbest bırakılan ürün bakımı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="225fb-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="225fb-110">Sevk edilen ürünler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="225fb-110">Click Released products.</span></span>
3. <span data-ttu-id="225fb-111">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="225fb-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="225fb-112">Bu 8 kayıtlı dizinde ilk kayıtta oluşturduğunuz boyut tabanlı ürün mastarını seçin.</span><span class="sxs-lookup"><span data-stu-id="225fb-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="225fb-113">Yapılandırmalar oluşturma</span><span class="sxs-lookup"><span data-stu-id="225fb-113">Create configurations</span></span>
1. <span data-ttu-id="225fb-114">Mühendislik Eylem Bölmesinde, Yapılandırmaları yönet düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="225fb-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="225fb-115">Yapılandır düğmesini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="225fb-115">Click Configure.</span></span>
3. <span data-ttu-id="225fb-116">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="225fb-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="225fb-117">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="225fb-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="225fb-118">İlk yapılandırma grubundaki maddelerden herhangi birini seçin.</span><span class="sxs-lookup"><span data-stu-id="225fb-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="225fb-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="225fb-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="225fb-120">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="225fb-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="225fb-121">İkinci yapılandırma grubundan herhangi bir maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="225fb-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="225fb-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="225fb-122">Click OK.</span></span>
8. <span data-ttu-id="225fb-123">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="225fb-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="225fb-124">Yapılandırma alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="225fb-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="225fb-125">Yapılandırmayı kolayca tanımlamanıza yardımcı olacak bir yapılandırma adı girin.</span><span class="sxs-lookup"><span data-stu-id="225fb-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="225fb-126">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="225fb-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="225fb-127">İçeriğini açıklamak için bir yapılandırma açıklaması girin.</span><span class="sxs-lookup"><span data-stu-id="225fb-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="225fb-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="225fb-128">Click OK.</span></span>


