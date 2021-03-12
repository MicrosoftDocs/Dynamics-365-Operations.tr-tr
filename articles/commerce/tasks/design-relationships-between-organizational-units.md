---
title: " Kuruluş birimleri arasındaki ilişkileri tasarlama"
description: Bu yordam kuruluş birimleri arasında ilişkiler tasarlamayı adım adım gösterir.
author: mugunthanm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner, OMNodeSelection,  HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b516d51210604a5813d637aa342dc7e269c60d89
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972263"
---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="a2e15-103"> Kuruluş birimleri arasındaki ilişkileri tasarlama</span><span class="sxs-lookup"><span data-stu-id="a2e15-103">Design the relationships between organizational units</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2e15-104">Bu yordam kuruluş birimleri arasında ilişkiler tasarlamayı adım adım gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2e15-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="a2e15-105">İlişkiyi tanımlamadan önce yeni bir kuruluş amacı oluşturmalısınız veya mevcut kuruluş amacını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2e15-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="a2e15-106">Bu prosedürün tamamlanması için veri şirketi USRT demo kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a2e15-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="a2e15-107">Bu görev, yöneticiler rolünü hedefler.</span><span class="sxs-lookup"><span data-stu-id="a2e15-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="a2e15-108">Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="a2e15-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-109">Click New.</span></span>
3. <span data-ttu-id="a2e15-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a2e15-111">Amaç ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="a2e15-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="a2e15-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-113">Click Add.</span></span>
7. <span data-ttu-id="a2e15-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="a2e15-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-115">Click OK.</span></span>
    * <span data-ttu-id="a2e15-116">Kuruluşunuz için gerektiği kadar kuruluş amacı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2e15-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="a2e15-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a2e15-118">Varsayılan olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-118">Click Set as default.</span></span>
11. <span data-ttu-id="a2e15-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-119">Close the page.</span></span>
12. <span data-ttu-id="a2e15-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-120">Click Save.</span></span>
13. <span data-ttu-id="a2e15-121">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-121">Click View.</span></span>
14. <span data-ttu-id="a2e15-122">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-122">Click Edit.</span></span>
15. <span data-ttu-id="a2e15-123">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-123">Click Insert.</span></span>
16. <span data-ttu-id="a2e15-124">İş birimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-124">Click Business unit.</span></span>
17. <span data-ttu-id="a2e15-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="a2e15-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="a2e15-127">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-127">Click Insert.</span></span>
20. <span data-ttu-id="a2e15-128">Commerce kanalına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-128">Click Commerce channel.</span></span>
21. <span data-ttu-id="a2e15-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="a2e15-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a2e15-131">Gerektiği kadar kuruluş birimi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a2e15-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="a2e15-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-132">Click Save.</span></span>
24. <span data-ttu-id="a2e15-133">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-133">Click Close.</span></span>
25. <span data-ttu-id="a2e15-134">İletişim kutusunu açmak için Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="a2e15-135">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="a2e15-136">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="a2e15-137">Değişiklikleri tanımla alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a2e15-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="a2e15-138">Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-138">Click Publish.</span></span>
30. <span data-ttu-id="a2e15-139">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a2e15-139">Click Close.</span></span>

