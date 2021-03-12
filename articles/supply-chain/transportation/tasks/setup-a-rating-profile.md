---
title: Değerlendirme profilleri
description: Bu konuda, değerlendirme profilleri için veri ayarlama yöntemi açıklanmaktadır.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973972"
---
# <a name="rating-profiles"></a><span data-ttu-id="b7042-103">Değerlendirme profilleri</span><span class="sxs-lookup"><span data-stu-id="b7042-103">Rating profiles</span></span>

<span data-ttu-id="b7042-104">Değerlendirme profili, lojistik sözleşmesine (ancak yasal sözleşmeye değil) benzer.</span><span class="sxs-lookup"><span data-stu-id="b7042-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="b7042-105">Bunlar, yükler için taşıma tarifelerini belirlemek amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b7042-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="b7042-106">Her değerlendirme profili bir sevkiyat taşıyıcısı için benzersizdir.</span><span class="sxs-lookup"><span data-stu-id="b7042-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="b7042-107">Profilde, sevkiyat taşıyıcısını bir ana oranla ilişkilendirirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7042-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="b7042-108">Ana oran, oran tabanı atamasını ve oran tabanını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="b7042-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="b7042-109">Oran tabanı, taşıyıcının oranını belirler.</span><span class="sxs-lookup"><span data-stu-id="b7042-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="b7042-110">Var olan tüm değerlendirme profillerinin özetini gösteren bir genel sayfa kullanarak bir değerlendirme profili ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7042-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="b7042-111">Alternatif olarak, doğrudan sevkiyat taşıyıcısından bir değerlendirme profili ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7042-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="b7042-112">Her iki durumda da, değerlendirme profili için ayarladığınız bilgiler aynıdır.</span><span class="sxs-lookup"><span data-stu-id="b7042-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="b7042-113">Değerlendirme profilleri sayfasında bir değerlendirme profili oluşturun veya düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="b7042-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="b7042-114">**Değerlendirme profilleri** sayfasında, kullanılabilir tüm değerlendirme profillerini gözden geçirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7042-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="b7042-115">Ayrıca, var olan profilleri düzenleyebilir ve yeni profiller oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7042-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="b7042-116">**Taşıma Yönetimi \> Kurulum \> Değerlendirme \> Değerlendirme profili**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="b7042-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="b7042-117">Eylem bölmesinde, kılavuza yeni değerlendirme profili eklemek için **Yeni**'yi veya var olan bir profili düzenlemek için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="b7042-118">Yeni veya var olan değerlendirme profili satırında, aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="b7042-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="b7042-119">**Değerlendirme profili**: Değerlendirme profili için benzersiz bir tanımlayıcı (kod) girin.</span><span class="sxs-lookup"><span data-stu-id="b7042-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="b7042-120">**Ad**: Değerlendirme profili için tanımlayıcı bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="b7042-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="b7042-121">**Sevkiyat taşıyıcısı**: Sevkiyat taşıyıcısı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="b7042-122">Ayarlamakta olduğunuz değerlendirme profili, seçilen taşıyıcı için **Sevkiyat taşıyıcıları** sayfasında da gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b7042-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="b7042-123">**Tesis** ve **Ambar**: Tesis ve ambar seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="b7042-124">**Değerlendirme Altyapısı** Değerlendirme profili için değerlendirme altyapısını seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="b7042-125">**Ana değerlendirme** Değerlendirme profili için ana değerlendirmeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="b7042-126">Ana oranı oran tabanı türü ve oran tabanı tanımlamak için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7042-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="b7042-127">Daha fazla bilgi için bkz. [Ana oranları ayarlama](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="b7042-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="b7042-128">**Yoldaki süre altyapısı**: Değerlendirme profili için yoldaki süresi altyapısını seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="b7042-129">**Taşıyıcı yakıt dizini**: Değerlendirme profili için taşıyıcı yakıt dizinini seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="b7042-130">**Geçerlilik başlangıç tarihi ve saati** ve **Geçerlilik bitiş tarihi ve saati**: Değerlendirme profilinin etkin olması gereken dönemi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="b7042-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="b7042-131">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="b7042-132">Sevkiyat taşıyıcıları sayfasında değerlendirme profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="b7042-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="b7042-133">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Sevkiyat taşıyıcıları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="b7042-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="b7042-134">Listeden sevkiyat taşıyıcısı seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="b7042-135">Değerlendirme profili oluşturmak için **Değerlendirme profilleri** hızlı sekmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="b7042-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="b7042-136">Yeni değerlendirme profili için alanları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b7042-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="b7042-137">Bu alanlar, bu konunun önceki bölümünde açıklandığı gibi, **Değerlendirme profilleri** sayfasındaki alanlara karşılık gelir.</span><span class="sxs-lookup"><span data-stu-id="b7042-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="b7042-138">**Sevkiyat taşıyıcıları** sayfasında oluşturulan profiller, **Değerlendirme profilleri** sayfasında da gösterilir.</span><span class="sxs-lookup"><span data-stu-id="b7042-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>
