--- 
title: " Kuruluş birimleri arasındaki ilişkileri tasarlama"
description: "Bu yordam kuruluş birimleri arasında ilişkiler tasarlamayı adım adım gösterir."
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e35915d2300755249ecd54bf2e4939d3a8df4f61
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="design-the-relationships-between-organizational-units"></a><span data-ttu-id="f8e96-103"> Kuruluş birimleri arasındaki ilişkileri tasarlama</span><span class="sxs-lookup"><span data-stu-id="f8e96-103">Design the relationships between organizational units</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="f8e96-104">Bu yordam kuruluş birimleri arasında ilişkiler tasarlamayı adım adım gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8e96-104">This procedure walks through how to design the relationship between organizational units.</span></span> <span data-ttu-id="f8e96-105">İlişkiyi tanımlamadan önce yeni bir kuruluş amacı oluşturmalısınız veya mevcut kuruluş amacını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8e96-105">You must create a new organization purpose before defining the relationship, or you can use the existing organization purpose.</span></span> <span data-ttu-id="f8e96-106">Bu prosedürün tamamlanması için veri şirketi USRT demo kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f8e96-106">The demo data company used to complete this procedure is USRT.</span></span> <span data-ttu-id="f8e96-107">Bu görev, yöneticiler rolünü hedefler.</span><span class="sxs-lookup"><span data-stu-id="f8e96-107">This task is intended for the administrator role.</span></span>

1. <span data-ttu-id="f8e96-108">Organizasyon yönetimi > Kuruluşlar > Kuruluş hiyerarşileri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-108">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="f8e96-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-109">Click New.</span></span>
3. <span data-ttu-id="f8e96-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f8e96-111">Amaç ata'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-111">Click Assign purpose.</span></span>
5. <span data-ttu-id="f8e96-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f8e96-113">Ekle öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-113">Click Add.</span></span>
7. <span data-ttu-id="f8e96-114">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-114">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="f8e96-115">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-115">Click OK.</span></span>
    * <span data-ttu-id="f8e96-116">Kuruluşunuz için gerektiği kadar kuruluş amacı seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8e96-116">You can select as many organization purposes as required for your organization.</span></span>  
9. <span data-ttu-id="f8e96-117">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-117">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f8e96-118">Varsayılan olarak ayarla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-118">Click Set as default.</span></span>
11. <span data-ttu-id="f8e96-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-119">Close the page.</span></span>
12. <span data-ttu-id="f8e96-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-120">Click Save.</span></span>
13. <span data-ttu-id="f8e96-121">Görüntüle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-121">Click View.</span></span>
14. <span data-ttu-id="f8e96-122">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-122">Click Edit.</span></span>
15. <span data-ttu-id="f8e96-123">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-123">Click Insert.</span></span>
16. <span data-ttu-id="f8e96-124">İş birimi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-124">Click Business unit.</span></span>
17. <span data-ttu-id="f8e96-125">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-125">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="f8e96-126">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-126">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="f8e96-127">Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-127">Click Insert.</span></span>
20. <span data-ttu-id="f8e96-128">Perakende kanalı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-128">Click Retail channel.</span></span>
21. <span data-ttu-id="f8e96-129">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-129">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="f8e96-130">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f8e96-131">Gerektiği kadar kuruluş birimi ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8e96-131">You can add as many organization units as is required.</span></span>  
23. <span data-ttu-id="f8e96-132">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-132">Click Save.</span></span>
24. <span data-ttu-id="f8e96-133">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-133">Click Close.</span></span>
25. <span data-ttu-id="f8e96-134">İletişim kutusunu açmak için Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-134">Click Publish to open the drop dialog.</span></span>
26. <span data-ttu-id="f8e96-135">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-135">In the Effective date field, enter a date and time.</span></span>
27. <span data-ttu-id="f8e96-136">Yürürlük tarihi alanına bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-136">In the Effective date field, enter a date and time.</span></span>
28. <span data-ttu-id="f8e96-137">Değişiklikleri tanımla alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f8e96-137">In the Describe changes field, type a value.</span></span>
29. <span data-ttu-id="f8e96-138">Yayımla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-138">Click Publish.</span></span>
30. <span data-ttu-id="f8e96-139">Kapat’a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f8e96-139">Click Close.</span></span>


