--- 
title: "Kazanç uygunluğu işlemi"
description: "Bu yordam, kazanç uygunluk işleminin nasıl çalıştığını gösterir."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: abc52192848649672cbcb8c770d74ba2aef139be
ms.openlocfilehash: fe773bd2375b2dea8e13a57918ad584f83f61073
ms.contentlocale: tr-tr
ms.lasthandoff: 02/15/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="83765-103">Kazanç uygunluğu işlemi</span><span class="sxs-lookup"><span data-stu-id="83765-103">Benefit eligibility process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83765-104">Bu yordam, kazanç uygunluk işleminin nasıl çalıştığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="83765-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="83765-105">İşlem tamamlandığında sonuçları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="83765-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="83765-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="83765-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="83765-107">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="83765-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="83765-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="83765-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="83765-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="83765-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="83765-110">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="83765-110">Click Edit.</span></span>
5. <span data-ttu-id="83765-111">Uygunluk alanında 'Kural tabanlı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="83765-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="83765-112">Kural Türü alanında, kazanca uygulanmasını istediğiniz kazanç ilke kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="83765-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="83765-113">Eylem Bölmesinde, Kazanç öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="83765-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="83765-114">İletişim kutusunu açmak için Uygunluk olayı oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="83765-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="83765-115">Olay alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="83765-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="83765-116">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="83765-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="83765-117">Olay türü alanında, 'Kaydı aç' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="83765-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="83765-118">Karşılama başlangıç tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="83765-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="83765-119">Kayıt dönemi başlangıç tarihi alanında bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="83765-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="83765-120">Kaydolmak için kalan gün sayısı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="83765-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="83765-121">Olay oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="83765-121">Click Create event.</span></span>
16. <span data-ttu-id="83765-122">Çalışanlar FastTab'inde Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="83765-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="83765-123">Türe göre göster alanında 'Çalışanlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="83765-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="83765-124">Tüzel kişiliğe göre göster alanında Geçerli tüzel kişilik' öğesini seçin</span><span class="sxs-lookup"><span data-stu-id="83765-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="83765-125">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="83765-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="83765-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="83765-126">Click OK.</span></span>
21. <span data-ttu-id="83765-127">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="83765-127">Click Process.</span></span>
22. <span data-ttu-id="83765-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="83765-128">Click OK.</span></span>
23. <span data-ttu-id="83765-129">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="83765-129">Refresh the page.</span></span>
24. <span data-ttu-id="83765-130">Sonuçları göster'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="83765-130">Click Show results.</span></span>
25. <span data-ttu-id="83765-131">Durum sütunu filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="83765-131">Open Status column filter.</span></span>
26. <span data-ttu-id="83765-132">A'dan Z'ye sırala</span><span class="sxs-lookup"><span data-stu-id="83765-132">Sort A to Z</span></span>


