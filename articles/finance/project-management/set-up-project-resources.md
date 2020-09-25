---
title: Proje kaynaklarını ayarlama
description: Bu konu, proje kaynaklarını ayarlama veya isteme hakkında bilgi sağlar.
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
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760688"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="0db8a-103">Proje kaynaklarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="0db8a-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0db8a-104">Bir takvim ayarlamanız ve bunu bir personel veya çalışanla ilişkilendirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0db8a-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="0db8a-105">Takvim, projeyi ve projeye rezerve edilen kaynakların çalışma zamanını planlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0db8a-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="0db8a-106">Takvim ayarlama işlemi sırasında, proje yöneticileri kaynak eşitlemeyi kaynak optimizasyonunun bir parçası olarak yapabilir.</span><span class="sxs-lookup"><span data-stu-id="0db8a-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="0db8a-107">Takvim planına bağlı olarak, kaynaklara kısıtlamalar yerleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="0db8a-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="0db8a-108">**Takvimler** sayfasından bir takvim ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0db8a-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="0db8a-109">Bir proje kaynağı için bir çalışan ayarlarsanız, kaynağı ayarladığını şirkette çalışan çalışanlar arasından seçim yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0db8a-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="0db8a-110">Alternatif olarak, kuruluşunuzdaki diğer şirketlerden çalışanları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0db8a-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="0db8a-111">Bu çalışanlar şirketlerarası kaynak olarak bilinir.</span><span class="sxs-lookup"><span data-stu-id="0db8a-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="0db8a-112">Aşağıdaki yordamlar bir çalışanı şirketinizdeki bir proje kaynağı olarak nasıl ayarlayacağınızı ve nasıl bir şirketlerarası proje kaynağı ayarlayabileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="0db8a-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="0db8a-113">Bir çalışanı proje kaynağı olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="0db8a-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="0db8a-114">**Çalışanlar** sayfasındaki **Çalışanlar** listesinde proje kaynağı olarak eklediğiniz çalışanı seçin ve çalışan kaydını açın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="0db8a-115">Eylem Bölmesinde **Proje** &gt; **Ayar** &gt; **Proje ayarı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="0db8a-116">Bir takvim seçin ve sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="0db8a-117">Bir kaynak için ön atama türü olarak varsayılan projeleri de belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0db8a-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="0db8a-118">Ön atamalar, kaynak yöneticisi veya proje yöneticisi, kaynağın hangi projede çalışacağını önceden bildiğinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="0db8a-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="0db8a-119">Ön atamalar için bir proje sponsoru veya müşterinin talebi de temel alınabilir.</span><span class="sxs-lookup"><span data-stu-id="0db8a-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="0db8a-120">Bir projeyi önceden atamak için **Projeleri ata** sayfasındaki **Projeler** sekmesinde bulunan **Kalan projeler** listesinden ilgili projeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="0db8a-121">Şirketlerarası bir kaynak ayarlama</span><span class="sxs-lookup"><span data-stu-id="0db8a-121">Set up an intercompany resource</span></span>

<span data-ttu-id="0db8a-122">Bir çalışanı şirketlerarası kaynak olarak ayarladığınızda, hem ayarı ödünç veren hem de ödünç alan şirkette tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="0db8a-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="0db8a-123">Ödünç veren şirkette</span><span class="sxs-lookup"><span data-stu-id="0db8a-123">In the lending company</span></span>

1. <span data-ttu-id="0db8a-124">Finance'te, borç veren şirketin seçildiğini doğruladıktan sonra, önceki bölümdeki "Bir çalışanı proje kaynağı olarak ayarlama" yordamını tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="0db8a-125">**Şirketlerarası muhasebe** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="0db8a-126">**Tüzel kişilik kimliği** alanında, ödünç veren şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="0db8a-127">Kalan alanları uygun şekilde doldurun ve **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="0db8a-128">**Transfer fiyatı** sayfasında, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="0db8a-129">**Ödünç alan tüzel kişilik** alanında, uygun şirketi seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="0db8a-130">Ödünç alan şirkete bölümün başında oluşturulan kaynağı ödünç vermek için **Kaynak** alanında, oluşturduğunuz kaynak adını seçin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="0db8a-131">Şirketteki tüm kaynakları ödünç alan şirketin kullanımına sunmak için, **Kaynak** alanını boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="0db8a-132">**Proje yönetimi ve muhasebe parametreleri** sayfasında **Şirketlerarası** sekmesinde, **Şirketlerarası kaynak planlamayı ve zaman çizelgelerini etkinleştir** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="0db8a-133">Ödünç alan şirkette</span><span class="sxs-lookup"><span data-stu-id="0db8a-133">In the borrowing company</span></span>

- <span data-ttu-id="0db8a-134">**Kaynak listesi** sayfasında arama filtresi alanına, ödünç alan şirketin kaynak listesine adın eklendiğini doğrulamak için ödünç veren şirket için oluşturduğunuz kaynağın adını girin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="0db8a-135">Proje kaynaklarını isteme</span><span class="sxs-lookup"><span data-stu-id="0db8a-135">Request project resources</span></span>
<span data-ttu-id="0db8a-136">Proje kaynak planlama işlevselliği yalnızca kaynak yöneticilerinin personelleri kaynakları görevlere veya projelere dağıtmasını destekler.</span><span class="sxs-lookup"><span data-stu-id="0db8a-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="0db8a-137">Bu işlevi etkinleştirmek için aşağıdaki görevleri tamamlayın veya bu görevlerin tamamlandığını doğrulayın:</span><span class="sxs-lookup"><span data-stu-id="0db8a-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="0db8a-138">Numara serileri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-138">Set up number sequences.</span></span>
- <span data-ttu-id="0db8a-139">Proje yönetimi ve muhasebe iş akışları ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="0db8a-140">Kaynak isteği iş akışlarını etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="0db8a-140">Enable resource request workflows.</span></span>

<span data-ttu-id="0db8a-141">Önceki görevler tamamlandıktan sonra, aşağıdaki görevleri istediğiniz gibi tamamlayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="0db8a-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="0db8a-142">Geçici rezervasyon personelli kaynağından bir kaynak isteği oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0db8a-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="0db8a-143">Kaynak isteklerini izleyin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-143">Monitor resource requests.</span></span>
- <span data-ttu-id="0db8a-144">Kaynak isteklerini karşılayın.</span><span class="sxs-lookup"><span data-stu-id="0db8a-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="0db8a-145">WBS'den personelli bir kaynak isteyin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="0db8a-146">Personelli kaynak isteği olmayan bir projeye kaynaklar rezerve edin.</span><span class="sxs-lookup"><span data-stu-id="0db8a-146">Book resources to a project without having a request for a staffed resource.</span></span>
