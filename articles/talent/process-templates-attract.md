---
title: Attract'ta süreç şablonu oluşturun
description: Bu konu, Attract'ta bir süreç şablonu oluşturma hakkında bilgi sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: 694835d20e3401aaeb22aa19082a2cd0e3a0163a
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010718"
---
# <a name="create-a-process-template"></a><span data-ttu-id="e4f12-103">Süreç şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4f12-103">Create a process template</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4f12-104">*İşe alma işlem şablonu*, bir işin işe alma işleminin parçası olarak dahil edilmesi gereken tüm faaliyetleri içerir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="e4f12-105">Bu konuda Microsoft Dynamics 365 Talent: Attract'teki bir işlem şablonunun öğeleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e4f12-105">This topic describes the elements of a process template in Microsoft Dynamics 365 Talent: Attract.</span></span> <span data-ttu-id="e4f12-106">Bu aynı zamanda bir şablon oluşturmayı açıklar.</span><span class="sxs-lookup"><span data-stu-id="e4f12-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="e4f12-107">Şablon oluşturma Attract için Kapsamlı İşe Alım eklentisinin parçasıdır.</span><span class="sxs-lookup"><span data-stu-id="e4f12-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="e4f12-108">Şablon yönetimi</span><span class="sxs-lookup"><span data-stu-id="e4f12-108">Template management</span></span>

<span data-ttu-id="e4f12-109">Kurumlar, Attract'ta ekip üyelerinin veya yalnızca yöneticilerin süreç şablonları oluşturmasını belirler.</span><span class="sxs-lookup"><span data-stu-id="e4f12-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="e4f12-110">Şablon yönetimi yapılandırmak için **Yönetici Merkezi**\>**Şablon yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="e4f12-111">Ekip üyelerinin kendi şablonlarını oluşturmasına izin vermek için şablon yönetimini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="e4f12-112">Şablon yönetimini etkinleştirmiyorsanız, yalnızca yöneticiler şablonları oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="e4f12-113">Varsayılan şablon</span><span class="sxs-lookup"><span data-stu-id="e4f12-113">Default template</span></span>

<span data-ttu-id="e4f12-114">Yalnızca yöneticiler varsayılan şablonu ayarlayabilir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-114">Only admins can set the default template.</span></span> <span data-ttu-id="e4f12-115">Bir iş oluşturulduğunda şablon işaretli değilse varsayılan şablon kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e4f12-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="e4f12-116">Varsayılan şablonu ayarlamak için **Yönetici Merkezi** \> **Şablon yönetimi**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="e4f12-117">Varsayılan şablon olması gereken şablonla ilgili karttaki üç nokta düğmesini (**...**) seçin ve daha sonra **Varsayılan olarak ayarla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="e4f12-118">Süreç şablonu oluştur</span><span class="sxs-lookup"><span data-stu-id="e4f12-118">Create a process template</span></span>

<span data-ttu-id="e4f12-119">Yöneticiler, işe alanlar ve işe alma müdürleri süreç şablonları oluşturabilir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="e4f12-120">Süreç şablonu, *aşamalar* ve *faaliyetlerden* oluşur.</span><span class="sxs-lookup"><span data-stu-id="e4f12-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="e4f12-121">Aşamalar, bir veya birkaç faaliyeti gruplandırır.</span><span class="sxs-lookup"><span data-stu-id="e4f12-121">Stages group together one or more activities.</span></span> <span data-ttu-id="e4f12-122">Varsayılan olarak, her işlem şablonu Aday müşteri, Başvuru ve Teklif faaliyetlerine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="e4f12-123">Bu etkinlikleri içeren aşamalar yeniden adlandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="e4f12-124">**+ Yeni Aşama**'yı seçerek daha fazla aşama ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4f12-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="e4f12-125">Faaliyetleri uygun aşaamaya sürükleyerek veya faaliyet listesinde çift tıklayarak bir aşamaya ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4f12-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="e4f12-126">Aşama adları **Başvuru durumu** sayfasında adaylara görünür.</span><span class="sxs-lookup"><span data-stu-id="e4f12-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="e4f12-127">Bu özelliği, aşamaları için adları seçtiğinizde dikkate almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="e4f12-128">Faaliyetler hakkında daha fazla bilgi için bkz: [Attract İşe alım süreci faaliyetleri](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="e4f12-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="e4f12-129">İşe alma süreç şablonu oluşturmak için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="e4f12-130">**Şablonlar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="e4f12-131">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-131">Select **New**.</span></span>
3. <span data-ttu-id="e4f12-132">**Şablon adı** alanında, şablon için bir ad girin ve sonra **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="e4f12-133">**Onay sürecini seç** listesinde bir iş için onay gerektirmek üzere **Varsayılan**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="e4f12-134">Aday müşterileri etkinleştirme veya devre dışı bırakmak için seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="e4f12-135">İsteğe bağlı: Aşama ekleyin veya kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e4f12-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="e4f12-136">Aşama eklemek için **+ Yeni aşama**yı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="e4f12-137">Aşama kaldırmak için aşama üzerine imleci getirin ve görünen çöp kutusu düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4f12-138">Aday, Başvuru ve Teklif aşamaları kaldırılamaz ancak yeniden adlandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4f12-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="e4f12-139">İsteğe bağlı: Faaliyet ekleyin veya kaldırın.</span><span class="sxs-lookup"><span data-stu-id="e4f12-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="e4f12-140">Faaliyet eklemek için sağdaki faaliyet listesinden uygun aşamaya sürükleyin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="e4f12-141">Alternatif olarak, faaliyete çift tıklatın ve eklemek için aşamayı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="e4f12-142">Faaliyeti kaldırmak için, genişletin ve faaliyet üst bilgisindeki çöp kutusu düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="e4f12-143">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4f12-143">Select **Save**.</span></span>
