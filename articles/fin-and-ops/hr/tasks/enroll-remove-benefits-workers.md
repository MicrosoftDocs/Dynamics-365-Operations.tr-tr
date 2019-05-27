---
title: Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma
description: Bu yordam, tek bir çalışanın bir veya daha fazla kazançta veya birden çok çalışanın tek bir kazançta nasıl kaydedileceğini göstermektedir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmWorkerEnrollment, HcmBenefitByEligibilityLookup, HcmMassBenefitEnrollment, HcmBenefitLookup, HcmMassBenefitEnrollmentResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92da6d24f3fc4282de5673a8155b6ab6316e55aa
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510440"
---
# <a name="enroll-and-remove-benefits-from-workers"></a><span data-ttu-id="7e7ea-103">Çalışanlara kazanç kaydetme ve çalışanlardan kazanç kaldırma</span><span class="sxs-lookup"><span data-stu-id="7e7ea-103">Enroll and remove benefits from workers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e7ea-104">Bu yordam, tek bir çalışanın bir veya daha fazla kazançta veya birden çok çalışanın tek bir kazançta nasıl kaydedileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-104">This procedure demonstrates how a single worker can be enrolled in one or more benefits, as well as multiple workers can be enrolled in a benefit.</span></span> <span data-ttu-id="7e7ea-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="enroll-a-single-worker-in-benefits"></a><span data-ttu-id="7e7ea-106">Tek bir çalışanı kazançlar için kaydetme</span><span class="sxs-lookup"><span data-stu-id="7e7ea-106">Enroll a single worker in benefits</span></span>
1. <span data-ttu-id="7e7ea-107">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin</span><span class="sxs-lookup"><span data-stu-id="7e7ea-107">Go to Human resources > Workers > Employees</span></span>
2. <span data-ttu-id="7e7ea-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7e7ea-109">Kazançlar'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-109">Click Benefits.</span></span>
4. <span data-ttu-id="7e7ea-110">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-110">Click New.</span></span>
5. <span data-ttu-id="7e7ea-111">Kazanç alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-111">In the Benefit field, enter or select a value.</span></span>
6. <span data-ttu-id="7e7ea-112">Karşılama başlangıç tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-112">In the Coverage start date field, enter a date and time.</span></span>
7. <span data-ttu-id="7e7ea-113">Karşılama bitiş tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-113">In the Coverage end date field, enter a date and time.</span></span>
8. <span data-ttu-id="7e7ea-114">Kazanç için lehdarlar eklenmesi gerekiyorsa, Lehdarlar bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-114">Expand the Beneficiaries section if beneficiaries need to be added to the benefit.</span></span> <span data-ttu-id="7e7ea-115">Kazanç için uygunsa bu sayfadan bağımlılık da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-115">You can also add dependents from this page if applicable to the benefit.</span></span>
9. <span data-ttu-id="7e7ea-116">Kazançların kayıt ayrıntılarını düzenleyebilir veya kaydı bu sayfada silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-116">You can also edit the details of a benefit enrollment or delete an enrollment on this page.</span></span> <span data-ttu-id="7e7ea-117">Kazanç kaydında değişiklikleri yapmayı bitirdiğinizde sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-117">When you have finished making changes to the benefit enrollment, close the page.</span></span>

## <a name="enroll-multiple-workers-in-a-benefit"></a><span data-ttu-id="7e7ea-118">Birden çok çalışanı bir kazanca kaydetme</span><span class="sxs-lookup"><span data-stu-id="7e7ea-118">Enroll multiple workers in a benefit</span></span>
1. <span data-ttu-id="7e7ea-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-119">Close the page.</span></span>
2. <span data-ttu-id="7e7ea-120">İnsan kaynakları > Çalışanlar > Çalışanlar'a gidin</span><span class="sxs-lookup"><span data-stu-id="7e7ea-120">Go to Human resources > Workers > Employees</span></span>
3. <span data-ttu-id="7e7ea-121">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7e7ea-122">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-122">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7e7ea-123">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-123">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7e7ea-124">Kazançlara kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-124">Click Enroll in benefits.</span></span>
7. <span data-ttu-id="7e7ea-125">Kazanç alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-125">In the Benefit field, enter or select a value.</span></span>
8. <span data-ttu-id="7e7ea-126">Karşılama başlangıç tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-126">In the Coverage start date field, enter a date and time.</span></span>
9. <span data-ttu-id="7e7ea-127">Karşılama bitiş tarihi alanında tarih ve saat girin.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-127">In the Coverage end date field, enter a date and time.</span></span>
10. <span data-ttu-id="7e7ea-128">Kaydet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-128">Click Enroll.</span></span>
11. <span data-ttu-id="7e7ea-129">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-129">Close the page.</span></span>
12. <span data-ttu-id="7e7ea-130">İnsan Kaynakları > Kazançlar > Kayıt > Kazanç kayıt sonuçları'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-130">Go to Human Resources > Benefits > Enrollment > Benefit enrollment results</span></span>
13. <span data-ttu-id="7e7ea-131">Aradığınız kazanç sonuçları kaydını bulun.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-131">Find the benefit results record that you are looking for.</span></span>
14. <span data-ttu-id="7e7ea-132">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-132">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="7e7ea-133">Bu sayfa, hangi çalışanların kazanç için kaydedildiğini hangilerinin kaydedilmediğini görüntülemenize olanak verir.</span><span class="sxs-lookup"><span data-stu-id="7e7ea-133">This page allows you to view which employees have been enrolled in the benefit, as well as any employees who were not enrolled.</span></span>

