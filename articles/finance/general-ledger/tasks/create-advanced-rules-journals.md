---
title: Günlükler için gelişmiş kurallar oluşturma
description: Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145229"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="96510-103">Günlükler için gelişmiş kurallar oluşturma</span><span class="sxs-lookup"><span data-stu-id="96510-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="96510-104">Bu yordam, günlükler için gelişmiş kurallar oluşturmayı adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="96510-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="96510-105">Bu, günlük kontrolü ve kullanıcı deftere nakil kısıtlamalarını ayarlamayı içerir.</span><span class="sxs-lookup"><span data-stu-id="96510-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="96510-106">Bu yordam, USMF demo verisi şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="96510-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="96510-107">Günlük kontrolünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="96510-107">Set up journal control</span></span>
1. <span data-ttu-id="96510-108">**Gezinti bölmesinde** **Modüller > Genel muhasebe > Günlük kurulumu > Günlük adları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="96510-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="96510-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="96510-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="96510-110">**Eylem bölmesinde** **Günlük denetimi** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="96510-111">**Deftere nakledilebilecek hesap türleri** hızlı sekmesinde **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="96510-112">**Şirket hesapları** alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="96510-113">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="96510-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="96510-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="96510-115">**Bu günlük için geçerli olan segment değerleri** hızlı sekmesinde **Ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="96510-116">**Hesap yapısı** alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96510-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="96510-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="96510-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="96510-118">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="96510-119">**Segment** alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96510-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="96510-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="96510-121">**Başlangıç değeri** alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96510-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="96510-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="96510-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="96510-123">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="96510-124">**Bitiş değeri** alanında, aramayı açmak için açılır menü düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96510-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="96510-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="96510-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="96510-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="96510-127">Nakil kısıtlamalarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="96510-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="96510-128">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="96510-128">Close the page.</span></span>
2. <span data-ttu-id="96510-129">**Deftere nakil kısıtlamaları**'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="96510-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="96510-130">**Deftere nakil sınırlamalarını nasıl ayarlamak istiyorsunuz?** alanında 'Kullanıcı grubuna göre'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="96510-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="96510-131">Ağaçta, 'Bu günlük adı için deftere nakile izin vermek istediğiniz grup' öğesini işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="96510-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="96510-132">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="96510-132">Click **OK**.</span></span>

