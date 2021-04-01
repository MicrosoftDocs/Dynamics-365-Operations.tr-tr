---
title: Üretim akışı sürümüne mevcut bir faaliyeti ekleme
description: Üretim akışlarının yeni sürümlerini oluştururken, daha eski sürümler için oluşturulmuş faaliyetleri yeni sürüme eklemeyi seçebilirsiniz.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityAddExisting, PlanActivityAddExistingLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 04ffbd87dfed3e5764e24c4e4599bd458b5fb767
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255505"
---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="29289-103">Üretim akışı sürümüne mevcut bir faaliyeti ekleme</span><span class="sxs-lookup"><span data-stu-id="29289-103">Add an existing activity to a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29289-104">Üretim akışlarının yeni sürümlerini oluştururken, daha eski sürümler için oluşturulmuş faaliyetleri yeni sürüme eklemeyi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="29289-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="29289-105">Bu yordam, faaliyetleri kopyalamadan mevcut bir üretim akışı için yeni bir sürüm oluşturmayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="29289-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="29289-106">Sonraki adımda, mevcut faaliyet yeni sürüme eklenir.</span><span class="sxs-lookup"><span data-stu-id="29289-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="29289-107">Bu görev, önceden oluşturulmuş sürüme ve faaliyetlere sahip üretim akışı gerektirir.</span><span class="sxs-lookup"><span data-stu-id="29289-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="29289-108">Yeni bir üretim akışı sürümü oluştur</span><span class="sxs-lookup"><span data-stu-id="29289-108">Create a new production flow version</span></span>
1. <span data-ttu-id="29289-109">Üretim kontrolü > Kurulum > Yalın üretim akışı > Üretim akışları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="29289-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="29289-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="29289-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="29289-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29289-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="29289-112">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="29289-112">Click Edit.</span></span>
5. <span data-ttu-id="29289-113">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="29289-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="29289-114">Bitiş tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="29289-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="29289-115">Yeni bir üretim akışı sürümü oluşturmadan önce, etkin sürümün bitiş tarihini ve saatini denetlediğinizden emin olun.</span><span class="sxs-lookup"><span data-stu-id="29289-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="29289-116">Yeni sürüm seçili sürümün bitiş tarihine bağlanan yürürlükteki başlangıç tarihi ile oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="29289-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="29289-117">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="29289-117">Click Add.</span></span>
8. <span data-ttu-id="29289-118">Sürümden kopyala alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="29289-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="29289-119">Kopyalanan sürüme ait faaliyetlerin çoğu yeni faaliyetlerle değiştirilecekse boş bir sürümle başlamak için Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="29289-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="29289-120">Değiştirilmeyen faaliyetleri faaliyet formundaki Mevcut işlev ekle seçeneğine el ile ekleyin.</span><span class="sxs-lookup"><span data-stu-id="29289-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="29289-121">Kanban kurallarını çoğalt alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="29289-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="29289-122">Faaliyetler yeni sürüme kopyalanmadığında, yeni sürümü oluşturma sırasında kanban kurallarını kopyalamak mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="29289-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="29289-123">Bunun yerine, eski üretim akışı sürümünün kanban kurallarını yeni sürümün faaliyetlerini kullanan kanban kuralları ile değiştirmek için, daha sonra kanban kuralı formunda Yeni kanban oluşturma işlevini kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="29289-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="29289-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29289-124">Click OK.</span></span>
11. <span data-ttu-id="29289-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="29289-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="29289-126">Var olan faaliyeti ekleme</span><span class="sxs-lookup"><span data-stu-id="29289-126">Add an existing activity</span></span>
1. <span data-ttu-id="29289-127">Faaliyetler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="29289-127">Click Activities.</span></span>
2. <span data-ttu-id="29289-128">İletişim kutusunu açmak için Varolanı ekle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29289-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="29289-129">Yeni üretim akışı sürümüne eklenecek mevcut faaliyeti bulun ve ekleyin.</span><span class="sxs-lookup"><span data-stu-id="29289-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="29289-130">Listede akışın önceki tüm sürümlerinde bu üretim akışı için oluşturulan tüm faaliyetlerin gösterildiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="29289-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="29289-131">Faaliyet alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="29289-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="29289-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="29289-132">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]