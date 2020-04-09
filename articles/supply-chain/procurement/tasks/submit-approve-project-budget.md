---
title: Proje bütçesi gönderme ve onaylama
description: Bu yordam, bir proje için bütçe oluşturmayı ve göndermeyi gösterir.
author: mkirknel
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aa7c301946b92b956f4b1b0f92985451ffe917e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149447"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="7d3da-103">Proje bütçesi gönderme ve onaylama</span><span class="sxs-lookup"><span data-stu-id="7d3da-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d3da-104">Bu yordam, bir proje için bütçe oluşturmayı ve göndermeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d3da-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="7d3da-105">Proje bütçesi oluşturduğunuzda, projenin tahmini gelirlerini ve maliyetlerini girebilir ve daha sonra gerçek proje hareketlerini denetlemek için bu değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7d3da-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="7d3da-106">Proje bütçelemede, tüm özgün bütçeler ve düzeltmeler onay için bir proje iş akışına gönderilmelidir.</span><span class="sxs-lookup"><span data-stu-id="7d3da-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="7d3da-107">İş akışı, size işlem üzerinde artırılmış denetim sağlar ve değişiklik geçmişi kaydı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7d3da-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="7d3da-108">Bu görev, USSI veri kümesini kullanarak oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="7d3da-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="7d3da-109">**Gezinti bölmesinde** **Modüller > Proje yönetimi ve muhasebe > Projeler > Tüm projeler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="7d3da-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7d3da-111">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7d3da-112">**Eylem Bölmesi**'nde **Plan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="7d3da-113">**Proje bütçesi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="7d3da-114">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="7d3da-115">**Maliyet** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="7d3da-116">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-116">Click **New**.</span></span>
9. <span data-ttu-id="7d3da-117">**Hareket türü** alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="7d3da-118">**Kategori** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="7d3da-119">**Orijinal bütçe** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="7d3da-120">**Gelirler** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="7d3da-121">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-121">Click **New**.</span></span>
14. <span data-ttu-id="7d3da-122">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="7d3da-123">**Hareket türü** alanında, bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="7d3da-124">**Kategori** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="7d3da-125">**Orijinal bütçe** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="7d3da-126">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-126">Click **Save**.</span></span>
19. <span data-ttu-id="7d3da-127">**İş akışı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="7d3da-128">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-128">Click **Submit**.</span></span>
21. <span data-ttu-id="7d3da-129">**Açıklama** alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="7d3da-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="7d3da-130">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7d3da-130">Click **Submit**.</span></span>

