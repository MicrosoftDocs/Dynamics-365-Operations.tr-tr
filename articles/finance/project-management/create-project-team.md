---
title: Proje ekibi oluşturma
description: Bu konuda bir proje ekibi oluşturma ve yönetme hakkında bilgiler yer alır.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760684"
---
# <a name="create-a-project-team"></a><span data-ttu-id="0cbf8-103">Proje ekibi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0cbf8-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cbf8-104">Bir projedeki önceden ayarlanmış olan rolleri kullanmak için bir proje yöneticisinin rolleri projeyle ilişkilendirmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="0cbf8-105">Bir proje için birden fazla rol atanabilir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="0cbf8-106">Karışıklığı önlemek için bu roller, rezervasyon sırasında otomatik etiketlenir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="0cbf8-107">Örneğin, proje yöneticisi üç yazılım mühendisi istiyorsa, **yazılım mühendisi 1**, **yazılım mühendisi 2** ve **yazılım mühendisi 3** etiketlerine sahip üç Yazılım mühendisi rolü otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="0cbf8-108">Rol için rol özellikleri önceden ayarlanmışsa, kaynak arama sırasında filtre olarak uygulanır.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="0cbf8-109">Aramayı daha detaylı hale getirmek için ek özellikler eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="0cbf8-110">Kaynak kullanılabilirliğinin daha iyi görüntülenebilmesi için görüntüleme ayarları özelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="0cbf8-111">Saatlik, günlük, haftalık, aylık, üç aylık ve yıllık kullanılabilirliği gösterme seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="0cbf8-112">Ayrıca, kullanılabilir ve kalan kaynak kapasitesini görüntüleme seçeneği de bulunur.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="0cbf8-113">Bu seçenek, faaliyetler veya kaynak kullanılabilirliği için kullanılabilir zamanı tahmin etmeniz gerektiğinde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="0cbf8-114">Proje yöneticisi sayfadan bir rol seçebilir ve gereksinimi karşılayan kullanılabilir bir kaynak varsa, rolü doldurmak için bir kaynak rezerve etmeyi seçebilir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="0cbf8-115">Kaynakların, planlama aşamasının bu noktasında rezerve edilmemesi gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="0cbf8-116">Bir WBS oluşturduğunuzda, rolleri projedeki personelli kaynaklarla değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="0cbf8-117">Roller, WBS'deki personelli kaynaklarla değiştirilirse, kaynak ayarı proje ekibi listesini ve planlamasını otomatik olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="0cbf8-118">[![Hem rolleri hem de gerçek kaynakları içeren proje ekibi listesi](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="0cbf8-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="0cbf8-119">Proje yöneticisinin bir proje için bir kaynağı rezerve etmek için kullanabileceği **Kalan kapasite**, **Tam kapasite**, **Kapasite yüzdesi** ve **Saatleri belirtme** gibi çeşitli seçenekleri vardır.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="0cbf8-120">Kaynak atamalarını değiştirirseniz, bu rezerve etme seçenekleri herhangi bir zamanda iptal edilebilir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="0cbf8-121">İki tür rezervasyon desteklenir:</span><span class="sxs-lookup"><span data-stu-id="0cbf8-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="0cbf8-122">**Kesin Rezervasyon** – Kaynak rezervasyonu onaylanmış ve belirtilen süre için görevde çalışmak üzere doğrulanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="0cbf8-123">**Geçici Rezervasyon** – Kaynak rezervasyonları geçici olarak belirtilen süre için görevde çalışmak üzere ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="0cbf8-124">Aşağıdaki yordamda bir proje ekibinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="0cbf8-125">Proje ekibi oluşturma</span><span class="sxs-lookup"><span data-stu-id="0cbf8-125">Create a project team</span></span>

1. <span data-ttu-id="0cbf8-126">**Tüm projeler** liste sayfasında bir proje seçin ve ardından **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="0cbf8-127">**Proje ekibi ve planlama** sekmesindeki **Bitiş tarihini planla** alanına, planlanan başlama tarihi artı bir ay girin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="0cbf8-128">Örneğin, planlama başlangıç tarihi 24 Haziran 2017 ise (24/06/2017), **24/07/2017** girin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="0cbf8-129">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-129">Select **Add**.</span></span>
4. <span data-ttu-id="0cbf8-130">**Projeye roller ekle** bölmesindeki **Rol** alanında **Kıdemli Proje Yöneticisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="0cbf8-131">**Gerekli yetkinlikler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="0cbf8-132">**Özelliklerini seçin** sayfasında, Kıdemli proje yöneticisi rolü için önceden ayarlamış olduğunuz özellikler varsayılan olarak seçilir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="0cbf8-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-133">Select **OK**.</span></span>
7. <span data-ttu-id="0cbf8-134">**Projeye roller ekle** sayfasındaki **Kaynak sayısı** alanına **1** girin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="0cbf8-135">**Kaynak** alanında, arama gerekli yetkinliklere sahip tüm kaynakları gösterir.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="0cbf8-136">**Daniel Goldschmidt**'i seçin ve **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="0cbf8-137">**Proje** sayfasında **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="0cbf8-138">**Projeye roller ekle** bölmesindeki **Rol** alanında **Ekip üyesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="0cbf8-139">**Kaynak sayısı** alanına **5** girin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="0cbf8-140">**Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-140">Select **Create**.</span></span>
12. <span data-ttu-id="0cbf8-141">**Projeler** sayfasında **Kaynağı karşıla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="0cbf8-142">Proje ekiplerini izleme</span><span class="sxs-lookup"><span data-stu-id="0cbf8-142">Monitor project teams</span></span>
1. <span data-ttu-id="0cbf8-143">**Tüm projeler** sayfasında **XYZ Yükseltme Aşama 2** projesi için **Proje kimliği** bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="0cbf8-144">**Proje ekibi ve planlama** hızlı sekmesinde, listelenen proje kaynaklarının doğru olduğunu kontrol edin.</span><span class="sxs-lookup"><span data-stu-id="0cbf8-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
