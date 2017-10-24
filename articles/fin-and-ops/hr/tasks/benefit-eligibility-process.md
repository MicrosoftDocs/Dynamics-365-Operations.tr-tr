--- 
title: "Kazanç uygunluğu işlemi"
description: "Bu yordam, kazanç uygunluk işleminin nasıl çalıştığını gösterir."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7c05c7613ee0d37d6bdfcb42f4e9611629d215bd
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="bb876-103">Kazanç uygunluğu işlemi</span><span class="sxs-lookup"><span data-stu-id="bb876-103">Benefit eligibility process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb876-104">Bu yordam, kazanç uygunluk işleminin nasıl çalıştığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb876-104">This procedure hows the benefit eligibility process works.</span></span> <span data-ttu-id="bb876-105">İşlem tamamlandığında sonuçları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb876-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="bb876-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="bb876-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="bb876-107">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="bb876-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="bb876-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bb876-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bb876-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb876-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bb876-110">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bb876-110">Click Edit.</span></span>
5. <span data-ttu-id="bb876-111">Uygunluk alanında 'Kural tabanlı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="bb876-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="bb876-112">Kural Türü alanında, kazanca uygulanmasını istediğiniz kazanç ilke kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="bb876-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="bb876-113">Eylem Bölmesinde, Kazanç öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb876-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="bb876-114">İletişim kutusunu açmak için Uygunluk olayı oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bb876-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="bb876-115">Olay alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bb876-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="bb876-116">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="bb876-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="bb876-117">Olay türü alanında, 'Kaydı aç' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb876-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="bb876-118">Karşılama başlangıç tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="bb876-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="bb876-119">Kayıt dönemi başlangıç tarihi alanında bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="bb876-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="bb876-120">Kaydolmak için kalan gün sayısı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="bb876-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="bb876-121">Olay oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bb876-121">Click Create event.</span></span>
16. <span data-ttu-id="bb876-122">Çalışanlar FastTab'inde Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bb876-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="bb876-123">Türe göre göster alanında 'Çalışanlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb876-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="bb876-124">Tüzel kişiliğe göre göster alanında Geçerli tüzel kişilik' öğesini seçin</span><span class="sxs-lookup"><span data-stu-id="bb876-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="bb876-125">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="bb876-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="bb876-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb876-126">Click OK.</span></span>
21. <span data-ttu-id="bb876-127">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bb876-127">Click Process.</span></span>
22. <span data-ttu-id="bb876-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bb876-128">Click OK.</span></span>
23. <span data-ttu-id="bb876-129">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="bb876-129">Refresh the page.</span></span>
24. <span data-ttu-id="bb876-130">Sonuçları göster'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bb876-130">Click Show results.</span></span>
25. <span data-ttu-id="bb876-131">Durum sütunu filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="bb876-131">Open Status column filter.</span></span>
26. <span data-ttu-id="bb876-132">A'dan Z'ye sırala</span><span class="sxs-lookup"><span data-stu-id="bb876-132">Sort A to Z</span></span>


