--- 
title: "Gelişmiş kural yapıları oluşturma ve atama"
description: "Bu görev kılavuzu, gelişmiş kural yapısı oluşturmayı ve bir hesap yapısına atamayı adım adım açıklar."
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8cb138da8c1625d814214c239dad9a9d66609293
ms.contentlocale: tr-tr
ms.lasthandoff: 08/07/2018

---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="03d8e-103">Gelişmiş kural yapıları oluşturma ve atama</span><span class="sxs-lookup"><span data-stu-id="03d8e-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03d8e-104">Bu görev kılavuzu, gelişmiş kural yapısı oluşturmayı ve bir hesap yapısına atamayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="03d8e-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="03d8e-105">Bu kılavuz, USMF demo şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="03d8e-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="03d8e-106">Gelişmiş kural yapısı oluştur</span><span class="sxs-lookup"><span data-stu-id="03d8e-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="03d8e-107">Genel muhasebe > Hesap planı > Yapılar > Gelişmiş kural yapıları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="03d8e-108">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="03d8e-109">Gelişmiş kural yapısı alanında, kural yapısını açıklamak için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-109">In the Advanced rule structure field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="03d8e-110">Açıklama alanında, yapıyı açıklayan bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="03d8e-111">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-111">Click OK.</span></span>
6. <span data-ttu-id="03d8e-112">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-112">Click Add segment.</span></span>
7. <span data-ttu-id="03d8e-113">Segmentler listesinde, bir mali boyut seçin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="03d8e-114">Örneğin, Mağaza.</span><span class="sxs-lookup"><span data-stu-id="03d8e-114">For example, Store.</span></span>  
8. <span data-ttu-id="03d8e-115">Segment ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-115">Click Add segment.</span></span>
9. <span data-ttu-id="03d8e-116">Listede, gelişmiş kural yapısını görüntülemek için bağlantısını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="03d8e-117">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-117">Click Activate.</span></span>
11. <span data-ttu-id="03d8e-118">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="03d8e-119">Gelişmiş bir kural yapısını bir hesap yapısına uygula</span><span class="sxs-lookup"><span data-stu-id="03d8e-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="03d8e-120">Formu kapatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-120">Close the form.</span></span>
2. <span data-ttu-id="03d8e-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-121">Close the page.</span></span>
3. <span data-ttu-id="03d8e-122">Genel muhasebe > Hesap planı > Yapılar > Hesap yapılarını yapılandır'a gidin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="03d8e-123">Listede, gelişmiş kural uygulamak istediğiniz hesap yapısını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="03d8e-124">Hesap yapısını açmak için adını tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="03d8e-125">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-125">Click Edit.</span></span>
    * <span data-ttu-id="03d8e-126">Gelişmiş kuralları da tıklatabilirsiniz, ardından hesap yapısını Taslak moduna yerleştirmeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="03d8e-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="03d8e-127">Gelişmiş kurallar öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="03d8e-128">Açılır iletişim kutusunu açmak için Yeni öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="03d8e-129">Gelişmiş kural alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="03d8e-130">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="03d8e-131">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-131">Click Create.</span></span>
12. <span data-ttu-id="03d8e-132">Yeni ölçüt ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="03d8e-133">Nereye alanında, ana hesabı veya bir mali boyutu seçin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="03d8e-134">İşleç alanında, arasında ve içerir gibi bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="03d8e-135">Değer alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="03d8e-136">Aracılığıyla alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="03d8e-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="03d8e-137">Açılır iletişim kutusunu açmak için Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="03d8e-138">Listede, girdiğiniz ölçüt gerçekleştiğinde kullanmak istediğiniz gelişmiş kural yapısını bulun.</span><span class="sxs-lookup"><span data-stu-id="03d8e-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="03d8e-139">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-139">Click Add.</span></span>
20. <span data-ttu-id="03d8e-140">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-140">Close the page.</span></span>
21. <span data-ttu-id="03d8e-141">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-141">Click Activate.</span></span>
22. <span data-ttu-id="03d8e-142">Etkinleştir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="03d8e-142">Click Activate.</span></span>


