--- 
title: "Günlükler için gelişmiş kurallar oluşturma"
description: "Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1bb1663b0f5d7e6a550e1ffd2ee2edf3771a13b3
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="3a3e7-103">Günlükler için gelişmiş kurallar oluşturma</span><span class="sxs-lookup"><span data-stu-id="3a3e7-103">Create advanced rules for journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a3e7-104">Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="3a3e7-105">Bu, günlük kontrolü ve kullanıcı deftere nakil kısıtlamalarını ayarlamayı içerir.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="3a3e7-106">Bu yordam, USMF demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="3a3e7-107">Günlük kontrolünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="3a3e7-107">Set up journal control</span></span>
1. <span data-ttu-id="3a3e7-108">Genel muhasebe > Günlük ayarı > Günlük adları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="3a3e7-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3a3e7-110">Günlük kontrolü'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-110">Click Journal control.</span></span>
4. <span data-ttu-id="3a3e7-111">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-111">Click Add.</span></span>
5. <span data-ttu-id="3a3e7-112">Şirket hesapları alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3a3e7-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3a3e7-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3a3e7-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-115">Click Add.</span></span>
9. <span data-ttu-id="3a3e7-116">Hesap yapısı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="3a3e7-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="3a3e7-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="3a3e7-119">Segment alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="3a3e7-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="3a3e7-121">Başlangıç değeri alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="3a3e7-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="3a3e7-123">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="3a3e7-124">Bitiş değeri alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="3a3e7-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="3a3e7-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="3a3e7-127">Nakil kısıtlamalarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="3a3e7-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="3a3e7-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-128">Close the page.</span></span>
2. <span data-ttu-id="3a3e7-129">Deftere nakil kısıtlamaları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="3a3e7-130">Deftere nakil sınırlamalarını nasıl ayarlamak istiyorsunuz? içinde Kullanıcı grubuna göre'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="3a3e7-131">Ağaçta, 'Bu günlük adı için deftere nakile izin vermek istediğiniz grup' öğesini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="3a3e7-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a3e7-132">Click OK.</span></span>


