---
title: Hata yönetimi
description: Bu konuda Varlık Yönetimi'ndeki varlık yönetiminde açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6665e80342af1baa7176aee92693b77e83b368f0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205932"
---
# <a name="fault-management"></a><span data-ttu-id="8644d-103">Hata yönetimi</span><span class="sxs-lookup"><span data-stu-id="8644d-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="8644d-104">Kıymet yönetiminde, arıza belirtileri, arıza alanları ve kıymet türlerinde arıza türleri ayarlamak için hata tasarımcısını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8644d-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="8644d-105">Bu şekilde, kıymetler üzerinde algılanan hataları yönetebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8644d-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="8644d-106">Ayrıca, hataları düzeltmek için hata nedenleri ve öneriler bir iş siparişine kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="8644d-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="8644d-107">Hata kayıt ve yönetim işlemi aşağıdaki adımlardan oluşur.</span><span class="sxs-lookup"><span data-stu-id="8644d-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="8644d-108">Kıymet türleriniz üzerinde oluşabilecek hata belirtileri, arıza alanları ve arıza türleri listesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8644d-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="8644d-109">Arıza Tasarımcısında, belirtiler, arıza alanları ve arıza türlerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="8644d-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="8644d-110">Hata belirtileri, arıza alanları ve arıza türleri arasındaki farkı anlamanıza yardımcı olacak bazı örnekler aşağıda verilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8644d-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="8644d-111">**Hata belirtileri:**</span><span class="sxs-lookup"><span data-stu-id="8644d-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="8644d-112">Dengesiz voltajlar</span><span class="sxs-lookup"><span data-stu-id="8644d-112">Unbalanced voltages</span></span>
- <span data-ttu-id="8644d-113">Kısa devre</span><span class="sxs-lookup"><span data-stu-id="8644d-113">Short circuit</span></span>
- <span data-ttu-id="8644d-114">Gürültü</span><span class="sxs-lookup"><span data-stu-id="8644d-114">Noise</span></span>
- <span data-ttu-id="8644d-115">Sızıntı</span><span class="sxs-lookup"><span data-stu-id="8644d-115">Leak</span></span>
- <span data-ttu-id="8644d-116">Titreşimler</span><span class="sxs-lookup"><span data-stu-id="8644d-116">Vibrations</span></span>

<span data-ttu-id="8644d-117">**Hata alanları:**</span><span class="sxs-lookup"><span data-stu-id="8644d-117">**Fault areas:**</span></span>

- <span data-ttu-id="8644d-118">Elektrik</span><span class="sxs-lookup"><span data-stu-id="8644d-118">Electrical</span></span>
- <span data-ttu-id="8644d-119">Mekanik</span><span class="sxs-lookup"><span data-stu-id="8644d-119">Mechanical</span></span>
- <span data-ttu-id="8644d-120">Hidrolik</span><span class="sxs-lookup"><span data-stu-id="8644d-120">Hydraulic</span></span>
- <span data-ttu-id="8644d-121">Pnömatik</span><span class="sxs-lookup"><span data-stu-id="8644d-121">Pneumatic</span></span>

<span data-ttu-id="8644d-122">**Hata türleri:**</span><span class="sxs-lookup"><span data-stu-id="8644d-122">**Fault types:**</span></span>

- <span data-ttu-id="8644d-123">Arızalı ana stator sargısı</span><span class="sxs-lookup"><span data-stu-id="8644d-123">Faulty main stator winding</span></span>
- <span data-ttu-id="8644d-124">Hatalı diyot</span><span class="sxs-lookup"><span data-stu-id="8644d-124">Faulty diode</span></span>
- <span data-ttu-id="8644d-125">Kirli sargılar</span><span class="sxs-lookup"><span data-stu-id="8644d-125">Dirty windings</span></span>
- <span data-ttu-id="8644d-126">Kusurlu oluşturucu</span><span class="sxs-lookup"><span data-stu-id="8644d-126">Defective generator</span></span>
- <span data-ttu-id="8644d-127">Kusurlu algılayıcı</span><span class="sxs-lookup"><span data-stu-id="8644d-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="8644d-128">Hata belirtileri oluştur</span><span class="sxs-lookup"><span data-stu-id="8644d-128">Create fault symptoms</span></span>

<span data-ttu-id="8644d-129">Hata tasarımcısında kullanılabilecek belirtilerin listesini oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8644d-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="8644d-130">**Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata semptomları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="8644d-131">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="8644d-132">**Hata semptomları** alanına hata semptomu adı girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="8644d-133">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8644d-134">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="8644d-135">Hata alanları oluştur</span><span class="sxs-lookup"><span data-stu-id="8644d-135">Create fault areas</span></span>

<span data-ttu-id="8644d-136">Hata tasarımcısında kullanılabilecek alanların veya konumların listesini oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8644d-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="8644d-137">**Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata alanları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="8644d-138">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="8644d-139">**Hata alanları** alanına hata alanı adı girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="8644d-140">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8644d-141">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="8644d-142">Hata türleri oluştur</span><span class="sxs-lookup"><span data-stu-id="8644d-142">Create fault types</span></span>

<span data-ttu-id="8644d-143">Hata tasarımcısında kullanılabilecek hata türlerinin listesini oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8644d-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="8644d-144">**Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="8644d-145">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="8644d-146">**Hata Türü** alanına hata türü için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="8644d-147">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8644d-148">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="8644d-149">Hata tasarımcısını ayarla</span><span class="sxs-lookup"><span data-stu-id="8644d-149">Set up the fault designer</span></span>

<span data-ttu-id="8644d-150">Hata tasarımcısında, kıymet türlerinde hata verileri ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="8644d-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="8644d-151">**Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata tasarımcısı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="8644d-152">Sol bölmede, bir hata kaydı kurmak üzere kullanılacak kıymetin türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="8644d-153">**Hata semptomu** hızlı sekmesinde **Satır ekle**'yi seçin ve **Hata semptomu** alanında bir hata semptomu seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="8644d-154">**Hata alanı** hızlı sekmesinde **Satır ekle**'yi seçin ve **Hata alanı** alanında bir hata alanı seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="8644d-155">**Hata türü** hızlı sekmesinde **Satır ekle**'yi seçin ve **Hata türü** alanında bir hata türü seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="8644d-156">Seçili varlık türü için varolan tüm hata semptomları, alanlar ve türlerin birleşimlerini hızlı bir şekilde oluşturmak için **Hata birleşimleri oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="8644d-157">Birçok hata semptomu, alanı ve türü eklediyseniz bu işlev yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="8644d-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="8644d-158">Kıymet türüyle alakalı olmayan herhangi bir kombinasyon için satırları silmek, el ile yeni satırlar oluşturmaktan daha kolaydır.</span><span class="sxs-lookup"><span data-stu-id="8644d-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8644d-159">Bir kıymet türündeki hata semptomları, alanlar ve türlerin kurulumunu seçili kıymet türüne kopyalamak için **Sabit kıymet türünden kopyala**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="8644d-160">Değişikliklerinizi kaydetmek için **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-160">Select **Save** to save your changes.</span></span>

![Arıza tasarımcısı sayfası](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="8644d-162">Hata nedenleri oluştur</span><span class="sxs-lookup"><span data-stu-id="8644d-162">Create fault causes</span></span>

<span data-ttu-id="8644d-163">Bir iş emrine veya bakım isteğine eklenebilen bilinen hata nedenlerinin bir listesini oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8644d-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="8644d-164">**Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata nedenleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="8644d-165">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="8644d-166">**Hata nedeni** alanına hata nedeni için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="8644d-167">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8644d-168">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="8644d-169">Hata düzeltici oluştur</span><span class="sxs-lookup"><span data-stu-id="8644d-169">Create fault remedies</span></span>

<span data-ttu-id="8644d-170">Bir iş emrine veya bakım isteğine eklenebilen düzeltici ve onarım önerilerinin bir listesini oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="8644d-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="8644d-171">**Kıymet yönetimi** \> **Kurulum** \> **Hata** \> **Hata düzelticisi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="8644d-172">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="8644d-173">**Hata düzeltici** alanına hata düzeltici adı girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="8644d-174">**Açıklama** alanına bir açıklama girin.</span><span class="sxs-lookup"><span data-stu-id="8644d-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="8644d-175">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8644d-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="8644d-176">Hata semptomlarınızın adlarını, alanlarını, türlerini, nedenlerini ve gereksinim duyduğunuz değişiklikleri değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8644d-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="8644d-177">Ad değişiklikleri otomatik olarak ilgili hata kayıtlarında yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="8644d-177">The name changes are automatically reflected in the related fault registrations.</span></span>
