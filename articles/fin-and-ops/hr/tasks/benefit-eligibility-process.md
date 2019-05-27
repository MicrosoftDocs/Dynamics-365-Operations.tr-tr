---
title: Kazanç uygunluğu işlemi
description: Bu yordam, kazanç uygunluk işleminin nasıl çalıştığını gösterir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b842d76d2c02b7f5daa45c5a34c8f61029f6c035
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507947"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="261b9-103">Kazanç uygunluğu işlemi</span><span class="sxs-lookup"><span data-stu-id="261b9-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="261b9-104">Bu yordam, kazanç uygunluk işleminin nasıl çalıştığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="261b9-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="261b9-105">İşlem tamamlandığında sonuçları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="261b9-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="261b9-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="261b9-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="261b9-107">İnsan kaynakları > Kazançlar > Kazançlar seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="261b9-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="261b9-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="261b9-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="261b9-109">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="261b9-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="261b9-110">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="261b9-110">Click Edit.</span></span>
5. <span data-ttu-id="261b9-111">Uygunluk alanında 'Kural tabanlı'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="261b9-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="261b9-112">Kural Türü alanında, kazanca uygulanmasını istediğiniz kazanç ilke kuralını seçin.</span><span class="sxs-lookup"><span data-stu-id="261b9-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="261b9-113">Eylem Bölmesinde, Kazanç öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="261b9-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="261b9-114">İletişim kutusunu açmak için Uygunluk olayı oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="261b9-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="261b9-115">Olay alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="261b9-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="261b9-116">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="261b9-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="261b9-117">Olay türü alanında, 'Kaydı aç' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="261b9-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="261b9-118">Karşılama başlangıç tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="261b9-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="261b9-119">Kayıt dönemi başlangıç tarihi alanında bir tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="261b9-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="261b9-120">Kaydolmak için kalan gün sayısı alanında bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="261b9-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="261b9-121">Olay oluştur'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="261b9-121">Click Create event.</span></span>
16. <span data-ttu-id="261b9-122">Çalışanlar FastTab'inde Ekle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="261b9-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="261b9-123">Türe göre göster alanında 'Çalışanlar' öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="261b9-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="261b9-124">Tüzel kişiliğe göre göster alanında Geçerli tüzel kişilik' öğesini seçin</span><span class="sxs-lookup"><span data-stu-id="261b9-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="261b9-125">Listede, tüm satırları işaretleyin veya tüm satırların işaretlerini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="261b9-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="261b9-126">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="261b9-126">Click OK.</span></span>
21. <span data-ttu-id="261b9-127">İşlemi'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="261b9-127">Click Process.</span></span>
22. <span data-ttu-id="261b9-128">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="261b9-128">Click OK.</span></span>
23. <span data-ttu-id="261b9-129">Sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="261b9-129">Refresh the page.</span></span>
24. <span data-ttu-id="261b9-130">Sonuçları göster'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="261b9-130">Click Show results.</span></span>
25. <span data-ttu-id="261b9-131">Durum sütunu filtresini açın.</span><span class="sxs-lookup"><span data-stu-id="261b9-131">Open Status column filter.</span></span>
26. <span data-ttu-id="261b9-132">A'dan Z'ye sırala</span><span class="sxs-lookup"><span data-stu-id="261b9-132">Sort A to Z</span></span>

