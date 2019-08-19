---
title: Günlükler için gelişmiş kurallar oluşturma
description: Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ec0db1bc5018649acaca05c71a510880b415777
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846691"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="2c459-103">Günlükler için gelişmiş kurallar oluşturma</span><span class="sxs-lookup"><span data-stu-id="2c459-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c459-104">Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="2c459-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="2c459-105">Bu, günlük kontrolü ve kullanıcı deftere nakil kısıtlamalarını ayarlamayı içerir.</span><span class="sxs-lookup"><span data-stu-id="2c459-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="2c459-106">Bu yordam, USMF demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="2c459-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="2c459-107">Günlük kontrolünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="2c459-107">Set up journal control</span></span>
1. <span data-ttu-id="2c459-108">Genel muhasebe > Günlük ayarı > Günlük adları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="2c459-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="2c459-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2c459-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2c459-110">Günlük kontrolü'nü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-110">Click Journal control.</span></span>
4. <span data-ttu-id="2c459-111">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-111">Click Add.</span></span>
5. <span data-ttu-id="2c459-112">Şirket hesapları alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2c459-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2c459-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2c459-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2c459-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="2c459-115">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-115">Click Add.</span></span>
9. <span data-ttu-id="2c459-116">Hesap yapısı alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="2c459-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2c459-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="2c459-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2c459-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="2c459-119">Segment alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2c459-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2c459-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="2c459-121">Başlangıç değeri alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="2c459-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2c459-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="2c459-123">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2c459-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="2c459-124">Bitiş değeri alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="2c459-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="2c459-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="2c459-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2c459-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="2c459-127">Nakil kısıtlamalarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="2c459-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="2c459-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-128">Close the page.</span></span>
2. <span data-ttu-id="2c459-129">Deftere nakil kısıtlamaları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="2c459-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="2c459-130">Deftere nakil sınırlamalarını nasıl ayarlamak istiyorsunuz? içinde Kullanıcı grubuna göre'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2c459-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="2c459-131">Ağaçta, 'Bu günlük adı için deftere nakile izin vermek istediğiniz grup' öğesini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="2c459-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="2c459-132">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="2c459-132">Click OK.</span></span>

