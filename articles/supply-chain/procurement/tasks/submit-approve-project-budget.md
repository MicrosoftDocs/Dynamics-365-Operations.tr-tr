--- 
title: "Proje bütçesi gönderme ve onaylama"
description: "Bu yordam, bir proje için bütçe oluşturmayı ve göndermeyi gösterir."
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.contentlocale: tr-tr
ms.lasthandoff: 09/14/2018

---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="f0d84-103">Proje bütçesi gönderme ve onaylama</span><span class="sxs-lookup"><span data-stu-id="f0d84-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0d84-104">Bu yordam, bir proje için bütçe oluşturmayı ve göndermeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0d84-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="f0d84-105">Proje bütçesi oluşturduğunuzda, projenin tahmini gelirlerini ve maliyetlerini girebilir ve daha sonra gerçek proje hareketlerini denetlemek için bu değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f0d84-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="f0d84-106">Proje bütçelemede, tüm özgün bütçeler ve düzeltmeler onay için bir proje iş akışına gönderilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f0d84-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="f0d84-107">İş akışı, size işlem üzerinde artırılmış denetim sağlar ve değişiklik geçmişi kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f0d84-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="f0d84-108">Bu görev, USSI veri kümesini kullanarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="f0d84-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="f0d84-109">Proje yönetimi ve muhasebe > Projeler > Tüm projeler'e gidin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="f0d84-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f0d84-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f0d84-112">Eylem Bölmesinde Plan'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="f0d84-113">Proje bütçesi'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-113">Click Project budget.</span></span>
6. <span data-ttu-id="f0d84-114">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="f0d84-115">Maliyet bölümünü genişletin</span><span class="sxs-lookup"><span data-stu-id="f0d84-115">Expand the Cost section</span></span>
8. <span data-ttu-id="f0d84-116">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-116">Click New.</span></span>
9. <span data-ttu-id="f0d84-117">Hareket türü alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="f0d84-118">Kategori alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="f0d84-119">Orijinal bütçe alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="f0d84-120">Gelirler bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="f0d84-121">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-121">Click New.</span></span>
14. <span data-ttu-id="f0d84-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="f0d84-123">Hareket türü alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="f0d84-124">Kategori alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="f0d84-125">Orijinal bütçe alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="f0d84-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-126">Click Save.</span></span>
19. <span data-ttu-id="f0d84-127">İş akışı'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-127">Click Workflow.</span></span>
20. <span data-ttu-id="f0d84-128">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-128">Click Submit.</span></span>
21. <span data-ttu-id="f0d84-129">Açıklama alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f0d84-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="f0d84-130">Gönder'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f0d84-130">Click Submit.</span></span>


