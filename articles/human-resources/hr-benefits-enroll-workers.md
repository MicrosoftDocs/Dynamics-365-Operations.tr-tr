---
title: Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma
description: Bu yordam, tek bir çalışanın bir veya daha fazla kazançta veya birden çok çalışanın tek bir kazançta nasıl kaydedileceğini göstermektedir.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 13e32c9bc77470d6b8e157e7a7805d3d72850478
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114558"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="4906f-103">Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma</span><span class="sxs-lookup"><span data-stu-id="4906f-103">Enroll and remove benefits from workers</span></span>



<span data-ttu-id="4906f-104">Bu yordam, tek bir çalışanın bir veya daha fazla kazançta veya birden çok çalışanın tek bir kazançta nasıl kaydedileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="4906f-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="4906f-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="4906f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="4906f-106">Tek bir çalışanı kazançlar için kaydetme</span><span class="sxs-lookup"><span data-stu-id="4906f-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="4906f-107">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin</span><span class="sxs-lookup"><span data-stu-id="4906f-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="4906f-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4906f-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4906f-109">Kazançlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-109">Click Benefits.</span></span>
4. <span data-ttu-id="4906f-110">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-110">Click New.</span></span>
5. <span data-ttu-id="4906f-111">Kazanç alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="4906f-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="4906f-112">Karşılama başlangıç tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="4906f-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="4906f-113">Karşılama bitiş tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="4906f-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="4906f-114">Kazanç için lehdarlar eklenmesi gerekiyorsa, Lehdarlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="4906f-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="4906f-115">Kazanç için uygunsa bu sayfadan bağımlılık da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4906f-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="4906f-116">Kazançların kayıt ayrıntılarını düzenleyebilir veya kaydı bu sayfada silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4906f-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="4906f-117">Kazanç kaydında değişiklikleri yapmayı bitirdiğinizde sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="4906f-118">Birden çok çalışanı bir kazanca kaydetme</span><span class="sxs-lookup"><span data-stu-id="4906f-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="4906f-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-119">Close the page.</span></span>
2. <span data-ttu-id="4906f-120">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin</span><span class="sxs-lookup"><span data-stu-id="4906f-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="4906f-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="4906f-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4906f-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4906f-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4906f-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4906f-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="4906f-124">Kazançlara kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="4906f-125">Kazanç alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="4906f-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="4906f-126">Karşılama başlangıç tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="4906f-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="4906f-127">Karşılama bitiş tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="4906f-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="4906f-128">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-128">Click Enroll.</span></span>
11. <span data-ttu-id="4906f-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-129">Close the page.</span></span>
12. <span data-ttu-id="4906f-130">İnsan Kaynakları > Kazançlar > Kayıt > Kazanç kayıt sonuçları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4906f-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="4906f-131">Aradığınız kazanç sonuçları kaydını bulun.</span><span class="sxs-lookup"><span data-stu-id="4906f-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="4906f-132">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4906f-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="4906f-133">Bu sayfa, hangi çalışanların kazanç için kaydedildiğini hangilerinin kaydedilmediğini görüntülemenize olanak verir.</span><span class="sxs-lookup"><span data-stu-id="4906f-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

