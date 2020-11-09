---
title: Giden sıralama
description: Bu konuda giden tasnifi hakkında bilgiler verilmiştir. Bu işlev küçük konteynerleri kullanmayı kolaylaştırır ve ambar çalışanlarının kamyondaki palet kapasitesini daha iyi planlamasına ve organize etmesine yardımcı olur.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017702"
---
# <a name="outbound-sorting"></a><span data-ttu-id="12f10-104">Giden sıralama</span><span class="sxs-lookup"><span data-stu-id="12f10-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12f10-105">Bu işlev küçük konteynerleri kullanmayı kolaylaştırır ve ambar çalışanlarının kamyondaki palet kapasitesini daha iyi planlamasına ve organize etmesine yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="12f10-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="12f10-106">Giden tasnif işlevini kullandığınızda, paketleme istasyonuna geldikten sonra paketlenen konteynerlerin doğru palete tasnif edilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12f10-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="12f10-107">Ayrıca bir paketleme hiyerarşisi de oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12f10-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="12f10-108">Bu işlev, paketleme işleviyle paketlenmiş konteynerlerden palet oluşturmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="12f10-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="12f10-109">Konteyner, orijinal sevk akışında olduğundan son sevkiyat yerleşimine gönderilmez.</span><span class="sxs-lookup"><span data-stu-id="12f10-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="12f10-110">Bunun yerine, çalışanlar konteyneri kapatabilir ve bunu bir tasnif türündeki yerleşime taşıyabilir.</span><span class="sxs-lookup"><span data-stu-id="12f10-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="12f10-111">Böylece konteynerleri her birinin plakası bulunan (LP) konumlara göre tasnif edebilirler.</span><span class="sxs-lookup"><span data-stu-id="12f10-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="12f10-112">Konteynerler tasnif edildikten sonra, tüm plakayı konum yönergelerine veya kendi gereksinimlerinize göre nihai sevkiyat noktasına veya hazırlama yerleşimlerine göndermek için iş oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="12f10-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="12f10-113">Ayrıca, tasnif konumunu kapatma eylemi stoğu anında son sevkiyat yerleşimine taşıyabilir ve siparişe çekebilir.</span><span class="sxs-lookup"><span data-stu-id="12f10-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="12f10-114">Giden tasnif özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="12f10-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="12f10-115">Özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="12f10-116">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="12f10-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="12f10-117">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="12f10-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="12f10-118">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="12f10-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="12f10-119">**Özellik adı:** *Giden tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="12f10-120">Ayar</span><span class="sxs-lookup"><span data-stu-id="12f10-120">Setup</span></span>

<span data-ttu-id="12f10-121">Bu senaryo için standart **USMF** demo verilerini ve ambar *62* 'yi kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="12f10-122">Ayrıca, aşağıdaki alt bölümlerde açıklanan kurulumu da tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="12f10-123">Dalga şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-123">Set up a wave template</span></span>

<span data-ttu-id="12f10-124">Bu kurulum satır ambara serbest bırakıldığında dalgayı otomatik olarak işler ve işi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="12f10-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="12f10-125">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="12f10-126">Şablon listesinde **Ambar 62** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="12f10-127">**Genel** hızlı sekmesinde, **Ambara serbest bırakıldığında dalgayı işle** seçeneğinin *Evet* olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="12f10-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="12f10-128">Çalışan ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-128">Set up a worker</span></span>

<span data-ttu-id="12f10-129">Paketleme istasyonu bir yerleşim olarak kabul edilir.</span><span class="sxs-lookup"><span data-stu-id="12f10-129">The packing station is considered a location.</span></span> <span data-ttu-id="12f10-130">Ambalaj istasyonunda oturum açan ambar çalışanları, yalnızca söz konusu belirli paketleme yerleşiminde planlanan sevkiyatlar ve konteynerleri görebilir ve bunlar üzerinde çalışabilirler.</span><span class="sxs-lookup"><span data-stu-id="12f10-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="12f10-131">Microsoft Dynamics 365'te oturum açan bir kullanıcının Ambar yönetiminde çalışan olarak ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="12f10-132">Kullanıcının adı iş kullanıcıları listesinde görünmüyorsa, bunu eklemek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="12f10-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="12f10-133">Bu adımlarda, kullanıcının sistemde zaten var olduğu ve **İnsan Kaynakları** modülünde personel veya çalışan olarak ilişkilendirilmiş olduğu varsayılır.</span><span class="sxs-lookup"><span data-stu-id="12f10-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="12f10-134">**Ambar yönetimi \> Kurulum \> Çalışan** 'a gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="12f10-135">**Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-135">Select **New**.</span></span>
1. <span data-ttu-id="12f10-136">**Çalışan** alanında, personel listesinden hedef kullanıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="12f10-137">**Seç** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-137">Select **Select**.</span></span>
1. <span data-ttu-id="12f10-138">Eylem bölmesinde, **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="12f10-139">**Kullanıcılar** hızlı sekmesinde, mobil cihaz hesabı oluşturmak için **Yeni** 'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="12f10-140">**Kullanıcı Kimliği:** Benzersiz bir kimlik girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="12f10-141">**Kullanıcı adı:** Kimlik için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="12f10-142">**Varsayılan ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="12f10-143">**Menü adı:** *Ana*</span><span class="sxs-lookup"><span data-stu-id="12f10-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="12f10-144">Eylem bölmesinde, **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="12f10-145">**Parola ayarla** iletişim kutusu görüntülenir; bu iletişim kutusunda kullanıcının mobil uygulamada oturum açmak için kullanabileceği basit bir parola oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12f10-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="12f10-146">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-146">Set the following values:</span></span>

    - <span data-ttu-id="12f10-147">**Parola:** Basit bir parola girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="12f10-148">**Parolayı onayla:** Aynı parolayı yeniden girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="12f10-149">**Parola ayarlama** 'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-149">Select **Set password**.</span></span>

    <span data-ttu-id="12f10-150">İşlem Merkezindeki bir bildirim, oluşturduğunuz kullanıcı için parolanın ayarlanmış olduğunu bildirir.</span><span class="sxs-lookup"><span data-stu-id="12f10-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="12f10-151">Yerleşim türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="12f10-151">Create a location type</span></span>

1. <span data-ttu-id="12f10-152">**Ambar yönetimi \> Kurulum \> Ambar \> Yerleşim türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="12f10-153">Eylem Bölmesinde, bir yerleşim türü oluşturmak için **Yeni** 'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="12f10-154">**Yerleşim türü:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="12f10-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="12f10-155">**Açıklama:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="12f10-156">Eylem bölmesinde, **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="12f10-157">Ambar yönetimi parametreleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="12f10-158">**Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="12f10-159">**Genel** sekmesinde **Yerleşim türleri** hızlı sekmesinde **Tasnif yerleşimi türü** alanını *TASNİF* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="12f10-160">Eylem bölmesinde, **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="12f10-161">Yerleşim profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-161">Set up a location profile</span></span>

1. <span data-ttu-id="12f10-162">**Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="12f10-163">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-164">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="12f10-165">**Yerleşim profili kimliği:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="12f10-166">**Ad:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="12f10-167">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-168">**Yerleşim biçimi:** *ASRB* (Koridor-Dolap-Raf-Bölme)</span><span class="sxs-lookup"><span data-stu-id="12f10-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="12f10-169">**Yerleşim türü:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="12f10-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="12f10-170">**Plaka izleme kullan:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="12f10-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="12f10-171">**Karışık maddelere izin ver:** *Evet* (Bu seçeneği *Evet* olarak ayarladığınızda **Karışık stok toplu işlemlerine izin ver** seçeneği otomatik olarak *Evet* 'e ayarlanır ve bağımsız olarak değiştirilemez.)</span><span class="sxs-lookup"><span data-stu-id="12f10-171">**Allow mixed items:** *Yes* (When you set this option to *Yes* , the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="12f10-172">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="12f10-173">Yerleşim ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-173">Set up a location</span></span>

1. <span data-ttu-id="12f10-174">**Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="12f10-175">Başlıkta, **Yerleşim için denetleme basamakları oluştur** onay kutusunu temizleyin.</span><span class="sxs-lookup"><span data-stu-id="12f10-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="12f10-176">Eylem Bölmesinde, bir yerleşim oluşturmak için **Yeni** 'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="12f10-177">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="12f10-178">**Yerleşim:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="12f10-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="12f10-179">**Yerleşim profili kimliği:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="12f10-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="12f10-180">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="12f10-181">Giden tasnif şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="12f10-182">Giden tasnif şablonu, işin tasnif yerleşiminin dışında oluşturulup oluşturulmayacağını ve tasnifin el ile mi yoksa otomatik olarak mı yapılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="12f10-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="12f10-183">Bu senaryo için, paketleme istasyonundan sonra palet oluşturmak üzere bir tasnif şablonu oluşturacaksınız.</span><span class="sxs-lookup"><span data-stu-id="12f10-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="12f10-184">**Ambar Yönetimi \> Kurulum \> Paketleme \> Giden tasnif şablonu** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="12f10-185">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-186">Yeni şablonun üst bilgisinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="12f10-187">**Giden tasnif şablonu kodu:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="12f10-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="12f10-188">**Açıklama:** *Otomatik İş Oluşturma*</span><span class="sxs-lookup"><span data-stu-id="12f10-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="12f10-189">**Giden tasnif şablon türü:** *Konteyner*</span><span class="sxs-lookup"><span data-stu-id="12f10-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="12f10-190">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="12f10-191">**Yerleşim:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="12f10-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="12f10-192">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-193">**Tasnif doğrulaması:** *Konum tarama*</span><span class="sxs-lookup"><span data-stu-id="12f10-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="12f10-194">**Pozisyon kapanışında iş oluştur:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="12f10-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="12f10-195">Bu seçenek *Evet* olarak ayarlandığında, konum kapatıldığı zaman stoğu nihai sevkiyat yerleşimine taşımak için iş oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="12f10-195">If this option is set to *Yes* , when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="12f10-196">*Hayır* olarak ayarlanırsa, konum kapatıldığında stok anında sipariş için çekilir.</span><span class="sxs-lookup"><span data-stu-id="12f10-196">If it's set to *No* , inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="12f10-197">**Pozisyon atama:** *Otomatik*</span><span class="sxs-lookup"><span data-stu-id="12f10-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="12f10-198">Bu alan *El ile* olarak ayarlandığında, kullanıcının her zaman stoğun hangi konumda sıralanacağını belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-198">If this field is set to *Manual* , the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="12f10-199">*Otomaik* olarak ayarlandığında sistem tasnif şablonu dökümlerini temel alarak mümkün olduğunda stoğu otomatik olarak bir konuma yönlendirir.</span><span class="sxs-lookup"><span data-stu-id="12f10-199">If it's set to *Automatic* , the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="12f10-200">Eylem bölmesinde **Sorguyu düzenle** seçeneğini kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="12f10-201">Eylem bölmesinde **Sorgu düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="12f10-202">Sorgu düzenleyicisinde, **Tasnif** sekmesinde, aşağıdaki değerlere sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="12f10-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="12f10-203">**Tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="12f10-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="12f10-204">**Türetilmiş tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="12f10-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="12f10-205">**Alan:** *Taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="12f10-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="12f10-206">Bu değeri seçtiğinizde sonra şu iletiyi alabilirsiniz: "Taşıyıcı hizmeti alanı bir dizin alanı değil.</span><span class="sxs-lookup"><span data-stu-id="12f10-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="12f10-207">Bunun üzerinde sıralama eklemek istiyor musunuz?"</span><span class="sxs-lookup"><span data-stu-id="12f10-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="12f10-208">**Evet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-208">Select **Yes**.</span></span>

    - <span data-ttu-id="12f10-209">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="12f10-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="12f10-210">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-210">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-211">Aşağıdaki iletiyi alabilirsiniz: "Gruplama sıfırlanacak, devam edilsin mi?"</span><span class="sxs-lookup"><span data-stu-id="12f10-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="12f10-212">**Evet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-212">Select **Yes**.</span></span>

    <span data-ttu-id="12f10-213">Eylem Bölmesindeki **Giden tasnif şablonu dökümleri** düğmesi kullanılabilir duruma gelir.</span><span class="sxs-lookup"><span data-stu-id="12f10-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="12f10-214">Eylem Bölmesinde, **Giden tasnif şablonu dökümleri** 'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="12f10-215">**Giden tasnif ölçüsü** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="12f10-216">**Referans tablosu adı:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="12f10-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="12f10-217">**Referans alanı adı:** *Taşıyıcı hizmeti*</span><span class="sxs-lookup"><span data-stu-id="12f10-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="12f10-218">**Alana göre gruplandır:** Sevkıyatları taşıyıcı hizmetine göre gruplandırmak için bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="12f10-219">Ayarlarınızı kaydedip iletişim kutusunu kapatmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="12f10-220">Konteyner paketleme ilkelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-220">Set up container packing policies</span></span>

1. <span data-ttu-id="12f10-221">**Ambar yönetimi\> Kurulum \> Konteynerler \> Konteyner paketleme ilkeleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="12f10-222">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-223">Yeni ilkenin üst bilgisinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="12f10-224">**Konteyner paketleme ilkesi:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="12f10-225">**Açıklama:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="12f10-226">**Genel bakış** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-227">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="12f10-228">**Tasnif için varsayılan yerleşim:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="12f10-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="12f10-229">**Ağırlık birimi:** *kg*</span><span class="sxs-lookup"><span data-stu-id="12f10-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="12f10-230">**Konteyner kapatma ilkesi:** *Otomatik serbest bırakma*</span><span class="sxs-lookup"><span data-stu-id="12f10-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="12f10-231">**Konteyner serbest bırakma ilkesi:** *Giden tasnif konumuna konteyner ata*</span><span class="sxs-lookup"><span data-stu-id="12f10-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="12f10-232">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="12f10-233">Paketleme profilleri ayarla</span><span class="sxs-lookup"><span data-stu-id="12f10-233">Set up packing profiles</span></span>

<span data-ttu-id="12f10-234">Tasnif işleviyle birlikte kullanılacak yeni bir paketleme profili oluşturun.</span><span class="sxs-lookup"><span data-stu-id="12f10-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="12f10-235">**Ambar yönetimi \> Kurulum \> Paketleme \> Paketleme profilleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="12f10-236">Eylem Bölmesinde, bir satır oluşturmak için **Yeni** 'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="12f10-237">**Paketleme profili kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="12f10-238">**Açıklama:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="12f10-239">**Konteyner paketleme ilkesi:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="12f10-240">**Konteyner kimliği modu:** *Otomatik*</span><span class="sxs-lookup"><span data-stu-id="12f10-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="12f10-241">**Konteyner türü:** *Kutu-Büyük*</span><span class="sxs-lookup"><span data-stu-id="12f10-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="12f10-242">**Konteyner kapatıldığında otomatik konteyner oluştur:** İşareti kaldırıldı (= *Hayır* )</span><span class="sxs-lookup"><span data-stu-id="12f10-242">**Auto create container at container close:** Cleared (= *No* )</span></span>

1. <span data-ttu-id="12f10-243">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="12f10-244">İş sınıflarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-244">Set up work classes</span></span>

<span data-ttu-id="12f10-245">Tasnif ile birlikte kullanılacak bir iş sınıfı ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="12f10-246">**Ambar yönetimi \> Kurulum \> İş \> İş sınıfları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="12f10-247">Eylem Bölmesinde, tasnif için iş sınıfı oluşturmak için **Yeni** 'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="12f10-248">**İş sınıfı kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="12f10-249">**Açıklama:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="12f10-250">**İş emri türü:** *Tasnif edilmiş stok çekme*</span><span class="sxs-lookup"><span data-stu-id="12f10-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="12f10-251">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="12f10-252">Mobil cihaz menü öğeleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="12f10-253">Yeni palet menü öğesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="12f10-254">Tasnif sırasında paletleri oluşturmak için mobil cihaz menü öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="12f10-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="12f10-255">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="12f10-256">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-257">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="12f10-258">**Menü öğesi adı:** *Palet oluşturma*</span><span class="sxs-lookup"><span data-stu-id="12f10-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="12f10-259">**Başlık:** *Palet oluşturma*</span><span class="sxs-lookup"><span data-stu-id="12f10-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="12f10-260">**Mod:** *Dolaylı*</span><span class="sxs-lookup"><span data-stu-id="12f10-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="12f10-261">**Varolan çalışmayı kullan:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="12f10-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="12f10-262">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-263">**Faaliyet kodu:** *Giden tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="12f10-264">Bu alan *Giden tasnif* olarak ayarlandığında, **Giden tasnif şablonu kimliği** alanı görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="12f10-264">When this field is set to *Outbound sorting* , the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="12f10-265">**İşlem kılavuzu kullan:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="12f10-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="12f10-266">**Faaliyet kodu** alanı *Giden tasnif* olarak ayarlandığında, bu seçenek otomatik olarak *Evet* 'e ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="12f10-266">When the **Activity code** field is set to *Outbound sorting* , this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="12f10-267">**Giden tasnif şablonu kodu:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="12f10-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="12f10-268">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="12f10-269">Yeni yükleme menü öğesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-269">Set up a new loading menu item</span></span>

<span data-ttu-id="12f10-270">Daha sonra kullanıcıların tasnif edilen stok maddelerini sevkiyat yerleşimine taşımasına olanak tanıyan bir menü öğesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="12f10-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="12f10-271">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="12f10-272">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-273">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="12f10-274">**Menü öğesi adı:** *Tasniften yükle*</span><span class="sxs-lookup"><span data-stu-id="12f10-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="12f10-275">**Başlık:** *Tasniften yükle*</span><span class="sxs-lookup"><span data-stu-id="12f10-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="12f10-276">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="12f10-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="12f10-277">**Mevcut işi kullan:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="12f10-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="12f10-278">**Genel** hızlı sekmesinde **Yöneten** alanı *Kullanıcı tarafından yönetilen* olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="12f10-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="12f10-279">**İş sınıfları** hızlı sekmesinde, **Yeni** 'yi seçin ve sonra aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-279">On the **Work classes** FastTab, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="12f10-280">**İş sınıfı kodu:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="12f10-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="12f10-281">**İş emri türü:** *Tasnif edilmiş stok çekme*</span><span class="sxs-lookup"><span data-stu-id="12f10-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="12f10-282">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="12f10-283">Mobil cihaz menüsünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-283">Set up the mobile device menu</span></span>

<span data-ttu-id="12f10-284">Şimdi yeni menü öğelerini mobil cihaz menüsüne eklemelisiniz.</span><span class="sxs-lookup"><span data-stu-id="12f10-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="12f10-285">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="12f10-286">**Giden** menüsünü seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="12f10-287">Eylem Bölmesi'nde, **Düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="12f10-288">**Mevcut menüler ve menü öğeleri** sütununda **Palet oluşturma** 'yı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="12f10-289">**Palet oluşturma** 'yı **Menü yapısı** sütununa taşımak için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="12f10-290">**Palet oluşturma** menü öğesini mobil cihaz menüsünde istenen konuma taşımak için yukarı ok ve aşağı ok düğmelerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12f10-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="12f10-291">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-291">Select **Save**.</span></span>
1. <span data-ttu-id="12f10-292">**Tasniften yükleme** menü öğesini **Tasnif** menüsüne eklemek için bu prosedürü tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="12f10-293">Yerleşim yönergelerini kur</span><span class="sxs-lookup"><span data-stu-id="12f10-293">Set up location directives</span></span>

<span data-ttu-id="12f10-294">*Yerleşim yönergeleri* stok hareketi için çekme ve indirme konumlarını belirlemeye yardımcı olan kurallardır.</span><span class="sxs-lookup"><span data-stu-id="12f10-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="12f10-295">Tasnif işini yönetmek için şimdi bir kural oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="12f10-296">Tek SKU yönergesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="12f10-297">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="12f10-298">Sol bölmede, **İş emri türü** alanının değerini *Tasnif edilen stoktan malzeme çekme* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="12f10-299">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-300">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="12f10-301">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="12f10-302">**Ad:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="12f10-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="12f10-303">**Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-304">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="12f10-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="12f10-305">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="12f10-305">**Site:** *6*</span></span>
    - <span data-ttu-id="12f10-306">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="12f10-307">**Birden çok SKU:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="12f10-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="12f10-308">Araç çubuğunu **Satırlar** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="12f10-309">**Satırlar** hızlı sekmesinde, **Yeni** 'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-309">On the **Lines** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="12f10-310">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="12f10-311">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="12f10-312">**Başlangıç:** *0*</span><span class="sxs-lookup"><span data-stu-id="12f10-312">**From:** *0*</span></span>
    - <span data-ttu-id="12f10-313">**Bitiş:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="12f10-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="12f10-314">Araç çubuğunu **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="12f10-315">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Yeni** 'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-315">On the **Location Directive Actions** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="12f10-316">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="12f10-317">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="12f10-318">**Ad:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="12f10-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="12f10-319">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-319">Select **Save**.</span></span>
1. <span data-ttu-id="12f10-320">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="12f10-321">Sorgu düzenleyicisinde, **Aralık** sekmesinde, **Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun.</span><span class="sxs-lookup"><span data-stu-id="12f10-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="12f10-322">Bu satır için **Ölçüt** alanını *Baydoor* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="12f10-323">Ayarlarınızı kaydedip sorgu düzenleyicisini kapatmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="12f10-324">Birden çok SKU yönergesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="12f10-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="12f10-325">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="12f10-326">Sol bölmede, **İş emri türü** alanının değerini *Tasnif edilen stoktan malzeme çekme* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="12f10-327">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-328">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="12f10-329">**Sıra:** *2*</span><span class="sxs-lookup"><span data-stu-id="12f10-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="12f10-330">**Ad:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="12f10-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="12f10-331">**Yerleşim yönergeleri** hızlı sekmesinde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-332">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="12f10-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="12f10-333">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="12f10-333">**Site:** *6*</span></span>
    - <span data-ttu-id="12f10-334">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="12f10-335">**Birden çok SKU:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="12f10-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="12f10-336">Araç çubuğunu **Satırlar** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="12f10-337">**Satırlar** hızlı sekmesinde, **Yeni** 'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-337">On the **Lines** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="12f10-338">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="12f10-339">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="12f10-340">**Başlangıç:** *0*</span><span class="sxs-lookup"><span data-stu-id="12f10-340">**From:** *0*</span></span>
    - <span data-ttu-id="12f10-341">**Bitiş:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="12f10-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="12f10-342">Araç çubuğunu **Yerleşim Yönergesi Eylemleri** hızlı sekmesinde kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="12f10-343">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde, **Yeni** 'yi seçin ve sonra yeni satırda aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-343">On the **Location Directive Actions** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="12f10-344">Tüm diğer alanlar için varsayılan değerleri kabul edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="12f10-345">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="12f10-346">**Ad:** *Baydoor Multi*</span><span class="sxs-lookup"><span data-stu-id="12f10-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="12f10-347">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-347">Select **Save**.</span></span>
1. <span data-ttu-id="12f10-348">**Yerleşim Yönergesi Eylemleri** hızlı sekmesinde **Sorguyu düzenle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="12f10-349">Sorgu düzenleyicisinde, **Aralık** sekmesinde, **Alan** alanının *Yerleşim* olarak ayarlandığı satırı bulun.</span><span class="sxs-lookup"><span data-stu-id="12f10-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="12f10-350">Bu satır için **Ölçüt** alanını *Baydoor* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="12f10-351">Ayarlarınızı kaydedip sorgu düzenleyicisini kapatmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="12f10-352">İş şablonlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="12f10-352">Set up work templates</span></span>

1. <span data-ttu-id="12f10-353">**Ambar yönetimi \> Kurulum \> İş \> İş şablonları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="12f10-354">**İş emri türü** alanının değerini *Tasnif edilen stoktan malzeme çekme* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="12f10-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="12f10-355">Eylem bölmesinde, bir iş şablonu oluşturmak için **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="12f10-356">**Genel bakış** sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="12f10-357">**Sıra:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="12f10-358">**İş şablonu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="12f10-359">**İş şablonu açıklaması:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="12f10-360">**İş Şablonu Ayrıntıları** hızlı sekmesini kullanılabilir hale getirmek için **Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="12f10-361">**İş Şablonu Ayrıntıları** hızlı sekmesinde, satır eklemek için **Yeni** 'yi seçin ve bunun için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="12f10-362">**İş türü:** *Çekme*</span><span class="sxs-lookup"><span data-stu-id="12f10-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="12f10-363">**İş sınıfı kodu:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="12f10-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="12f10-364">**Satır ekle** 'yi seçerek ikinci bir satır ekleyin ve aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="12f10-365">**İş türü:** *Yerine koyma*</span><span class="sxs-lookup"><span data-stu-id="12f10-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="12f10-366">**İş sınıfı kodu:** *TASNİF*</span><span class="sxs-lookup"><span data-stu-id="12f10-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="12f10-367">**Kaydet** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="12f10-368">Senaryo</span><span class="sxs-lookup"><span data-stu-id="12f10-368">Scenario</span></span>

<span data-ttu-id="12f10-369">Bu senaryo, sevkiyat taşıma hizmetine bağlı olarak, paketlenen konteynerlerin paket istasyonu ardından otomatik olarak farklı konumlara (paletlere) tasnif edilmesi gereken bir durumun benzetimini yapar.</span><span class="sxs-lookup"><span data-stu-id="12f10-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="12f10-370">Yükten gelen tüm maddeler paketlendikten ve adrese göre tasnif edildikten sonra, paletler bölme kapısına taşınacaktır.</span><span class="sxs-lookup"><span data-stu-id="12f10-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="12f10-371">Satış siparişi ve çekme işi oluşturma</span><span class="sxs-lookup"><span data-stu-id="12f10-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="12f10-372">Satış siparişi oluşturma 1</span><span class="sxs-lookup"><span data-stu-id="12f10-372">Create sales order 1</span></span>

1. <span data-ttu-id="12f10-373">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="12f10-374">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-375">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="12f10-376">**Müşteri hesabı:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="12f10-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="12f10-377">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="12f10-378">İletişim kutusunu kapatmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="12f10-379">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="12f10-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="12f10-380">**Üst bilgi** görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="12f10-381">**Teslimat** hızlı sekmesinde, **Taşıma** bölümünde aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="12f10-382">**Sevkiyat taşıyıcısı:** *Hava nakliyesi*</span><span class="sxs-lookup"><span data-stu-id="12f10-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="12f10-383">**Taşıyıcı hizmeti:** *Hava*</span><span class="sxs-lookup"><span data-stu-id="12f10-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="12f10-384">**Satırlar** görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="12f10-385">**Satış siparişi satırları** hızlı sekmesinde, kılavuza yeni bir satır otomatik olarak eklenmemişse **Satır ekle** 'yi seçin seçerek ekleyin:</span><span class="sxs-lookup"><span data-stu-id="12f10-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="12f10-386">Yeni sipariş satırında aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="12f10-387">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="12f10-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="12f10-388">**Miktar:** *2*</span><span class="sxs-lookup"><span data-stu-id="12f10-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="12f10-389">Yeni sipariş satırı **Satış siparişi satırları** hızlı sekmesinde seçiliyken, kılavuzun üzerindeki **Stok** menüsünden **Rezervasyon** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="12f10-390">**Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="12f10-391">Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="12f10-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="12f10-392">Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="12f10-393">Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12f10-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="12f10-394">Dalga kodu ve sevkiyat kodu numaralarını not edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="12f10-395">Satış siparişi 2</span><span class="sxs-lookup"><span data-stu-id="12f10-395">Sales order 2</span></span>

1. <span data-ttu-id="12f10-396">**Satış ve pazarlama \> Satış siparişleri \> Tüm satış siparişleri** 'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="12f10-397">Eylem Bölmesinde, **Yeni** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="12f10-398">**Satış siparişi oluştur** iletişim kutusunda, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="12f10-399">**Müşteri hesabı:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="12f10-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="12f10-400">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="12f10-401">İletişim kutusunu kapatmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="12f10-402">Yeni satış siparişi açılır.</span><span class="sxs-lookup"><span data-stu-id="12f10-402">The new sales order is opened.</span></span> <span data-ttu-id="12f10-403">**Satış siparişi satırları** hızlı sekmesi 'ndeki kılavuza yeni, boş bir satır dahil etmelidir.</span><span class="sxs-lookup"><span data-stu-id="12f10-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="12f10-404">Bu sipariş satırında aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="12f10-405">**Madde:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="12f10-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="12f10-406">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="12f10-407">**Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesinde, **Teslimat yöntemi** alanını *Flowe-STD* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="12f10-408">**Satış siparişi satırları** hızlı sekmesinde, **Satır ekle** 'yi seçin ve sonra ikinci sipariş satırında aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-408">On the **Sales order lines** FastTab, select **Add line** , and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="12f10-409">**Madde:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="12f10-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="12f10-410">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="12f10-411">**Satır ayrıntıları** hızlı sekmesinde **Teslimat** sekmesinde, **Teslimat yöntemi** alanının değerini *Air C-Air* olarak değiştirin.</span><span class="sxs-lookup"><span data-stu-id="12f10-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="12f10-412">**Satış siparişi satırları** hızlı sekmesinde ilk sipariş satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="12f10-413">Ardından, kılavuzun üzerindeki **stok** menüsünde **rezervasyon** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="12f10-414">**Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="12f10-415">Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="12f10-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="12f10-416">**Satış siparişi satırları** hızlı sekmesinde ikinci sipariş satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="12f10-417">Ardından, kılavuzun üzerindeki **stok** menüsünde **rezervasyon** 'u seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="12f10-418">**Rezervasyon** sayfasında, ambardaki seçili satırın tüm miktarını rezerve etmek için **Lot ayır** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="12f10-419">Satış siparişine dönmek için **Rezervasyon** sayfasını kapatın.</span><span class="sxs-lookup"><span data-stu-id="12f10-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="12f10-420">Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="12f10-421">Bu sipariş için sevkiyatı ve dalgayı gösteren bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12f10-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="12f10-422">Satış siparişi satırlarındaki her teslimat yöntemi için bir tane olmak üzere iki dalga kodu numarası ve iki sevkiyat kodu numarasının oluşturulmuş olduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="12f10-423">İş ayrıntılardan iş kodlarını alma</span><span class="sxs-lookup"><span data-stu-id="12f10-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="12f10-424">**Ambar yönetimi \> İş \> İş ayrıntıları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="12f10-425">Sayfa, satış siparişlerinden oluşturulan iş kodlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="12f10-426">Her bir dalga ve sevkiyatla ilgili iş kodunu bulmak için oluşturduğunuz satış siparişlerindeki dalga kodlarını ve sevkiyat kimliklerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="12f10-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="12f10-427">Bir sonraki adımda gereksinim duyacağınız tüm iş kodlarını not alın.</span><span class="sxs-lookup"><span data-stu-id="12f10-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="12f10-428">İkinci satış siparişi için iki iş kodu oluşturulduğuna dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="12f10-429">Farklı konumlardan farklı maddeler çekildiğinde, ayrı iş kodları oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="12f10-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="12f10-430">Satış siparişleri için maddeleri çekme</span><span class="sxs-lookup"><span data-stu-id="12f10-430">Pick items for the sales orders</span></span>

<span data-ttu-id="12f10-431">Maddeleri paket istasyonuna taşımak için mobil cihaz kullanarak oluşturulan işi tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="12f10-432">Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62* 'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="12f10-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="12f10-433">Ana menüde **Giden** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="12f10-434">**Giden** menüsünden **Satış Çekme** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="12f10-435">**Kod** alanına, satış siparişi 1 için oluşturulan iş kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="12f10-436">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-436">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-437">**Satış siparişleri - Çekme** sayfasında, satış siparişi 1 için oluşturulmuş olan hedef bir LP girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="12f10-438">Çekme yerleşimi ( *toplu-001* ), madde ( *A0001* ) ve miktar ( *2 adet* ) gösterildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-438">Notice that the picking location ( *bulk-001* ), item ( *A0001* ), and quantity ( *2 pcs* ) are shown.</span></span>
1. <span data-ttu-id="12f10-439">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-439">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-440">**Satış siparişleri: Yerine koyma** sayfası hakkındaki bilgileri inceleyin.</span><span class="sxs-lookup"><span data-stu-id="12f10-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="12f10-441">**Yerleşim** alanı, çekilen maddelerin *Paket* yerleşimine gittiğini göstermelidir.</span><span class="sxs-lookup"><span data-stu-id="12f10-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="12f10-442">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-442">Select **OK**.</span></span>

    <span data-ttu-id="12f10-443">**İş kodu/plaka kodu tara** sayfasında, satış sipariş i1'deki iş kodunun tamamlandığını belirten "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12f10-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="12f10-444">Şimdi satış siparişi 2'yi çekeceksiniz.</span><span class="sxs-lookup"><span data-stu-id="12f10-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="12f10-445">**Kod** alanına, satış siparişi 2 için oluşturulan iş kodunu girin; burada satır 1'de *A0001* maddesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="12f10-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="12f10-446">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-446">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-447">**Satış siparişleri - Çekme** sayfasında bir hedef LP girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="12f10-448">Çekme yerleşimi ( *toplu-001* ), madde ( *A0001* ) ve miktar ( *1 adet* ) gösterildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-448">Notice that the picking location ( *bulk-001* ), item ( *A0001* ), and quantity ( *1 pcs* ) are shown.</span></span>
1. <span data-ttu-id="12f10-449">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-449">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-450">**Satış siparişleri: Yerine koyma** sayfası hakkındaki bilgileri inceleyin.</span><span class="sxs-lookup"><span data-stu-id="12f10-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="12f10-451">**Yerleşim** alanı, çekilen maddelerin *Paket* yerleşimine gittiğini göstermelidir.</span><span class="sxs-lookup"><span data-stu-id="12f10-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="12f10-452">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-452">Select **OK**.</span></span>

    <span data-ttu-id="12f10-453">**İş kodu/plaka kodu tara** sayfasında "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12f10-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="12f10-454">Bu ileti, satış siparişi 2'nin satır 1'indeki iş kodunun tamamlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="12f10-455">**Kod** alanına, satış siparişi 2 için oluşturulan iş kodunu girin; burada satır 2'de *A0002* maddesi bulunur.</span><span class="sxs-lookup"><span data-stu-id="12f10-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="12f10-456">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-456">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-457">**Satış siparişleri - Çekme** sayfasında bir hedef LP girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="12f10-458">Çekme yerleşimi ( *toplu-002* ), madde ( *A0001* ) ve miktar ( *1 adet* ) gösterildiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-458">Notice that the picking location ( *bulk-002* ), item ( *A0001* ), and quantity ( *1 pcs* ) are shown.</span></span>
1. <span data-ttu-id="12f10-459">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-459">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-460">**Satış siparişleri: Yerine koyma** sayfası hakkındaki bilgileri inceleyin.</span><span class="sxs-lookup"><span data-stu-id="12f10-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="12f10-461">**Yerleşim** alanı, çekilen maddelerin *Paket* yerleşimine gittiğini göstermelidir.</span><span class="sxs-lookup"><span data-stu-id="12f10-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="12f10-462">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-462">Select **OK**.</span></span>

    <span data-ttu-id="12f10-463">**İş kodu/plaka kodu tara** sayfasında "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12f10-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="12f10-464">Bu ileti, satış siparişi 2'nin satır 2'indeki iş kodunun tamamlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="12f10-465">Satış siparişlerini konteynerlerde paketleme</span><span class="sxs-lookup"><span data-stu-id="12f10-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="12f10-466">Satış siparişi 1'i konteynerlerde paketleme</span><span class="sxs-lookup"><span data-stu-id="12f10-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="12f10-467">**Ambar Yönetimi \> Paketleme ve Konteyner kullanımı \> Paket** 'e gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="12f10-468">**Paketleme istasyonu seç** iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="12f10-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="12f10-469">Varsayılan olarak, **Çalışan** alanı daha önce ayarladığınız çalışanın adı olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="12f10-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="12f10-470">Belirli bir paketleme yerleşiminde planlanan sevkiyatları ve konteynerleri görüntülemek ve bunlarla çalışmak için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="12f10-471">**Tesis:** *6*</span><span class="sxs-lookup"><span data-stu-id="12f10-471">**Site:** *6*</span></span>
    - <span data-ttu-id="12f10-472">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="12f10-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="12f10-473">**Yerleşim:** *Paket*</span><span class="sxs-lookup"><span data-stu-id="12f10-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="12f10-474">**Paketleme profili kodu:** *Tasnif*</span><span class="sxs-lookup"><span data-stu-id="12f10-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="12f10-475">İletişim kutusunu kapatmak için **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="12f10-476">**Paket** sayfasında, **Plaka veya sevkiyat** alanına, satış siparişi 1 için hedef LP girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="12f10-477">Ardından alanın dışına gitmek için klavyenizden **Sekme** veya **Enter** tuşunu seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="12f10-478">Eylem Bölmesinde **Yeni konteyner** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="12f10-479">Tüm varsayılan ayarları kabul edin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="12f10-480">Konteyner kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="12f10-481">**Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-482">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="12f10-483">**Tanımlayıcı:** Madde *A0001*</span><span class="sxs-lookup"><span data-stu-id="12f10-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="12f10-484">Eylem Bölmesinde **Konteyneri kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="12f10-485">**Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="12f10-486">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-486">Select **OK**.</span></span> <span data-ttu-id="12f10-487">Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="12f10-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="12f10-488">Satış siparişi 1 için LP'den ikinci maddeyi yeni bir konteynere eklemek üzere ikinci bir konteyner oluşturun.</span><span class="sxs-lookup"><span data-stu-id="12f10-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="12f10-489">Eylem Bölmesinde **Yeni konteyner** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="12f10-490">Tüm varsayılan ayarları kabul edin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="12f10-491">Konteyner kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="12f10-492">**Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-493">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="12f10-494">**Tanımlayıcı:** Madde *A0001*</span><span class="sxs-lookup"><span data-stu-id="12f10-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="12f10-495">Eylem Bölmesinde **Konteyneri kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="12f10-496">**Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="12f10-497">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-497">Select **OK**.</span></span> <span data-ttu-id="12f10-498">Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="12f10-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="12f10-499">Satış siparişi 2'yi konteynerlerde paketleme</span><span class="sxs-lookup"><span data-stu-id="12f10-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="12f10-500">**Paket** sayfasında, **Plaka veya sevkiyat** alanına, satış siparişi 2'nin satır 1'i için hedef LP girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="12f10-501">Ardından alanın dışına gitmek için klavyenizden **Sekme** veya **Enter** tuşunu seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="12f10-502">Eylem Bölmesinde **Yeni konteyner** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="12f10-503">Tüm varsayılan ayarları kabul edin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="12f10-504">Konteyner kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="12f10-505">**Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-506">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="12f10-507">**Tanımlayıcı:** Madde *A0001*</span><span class="sxs-lookup"><span data-stu-id="12f10-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="12f10-508">Eylem Bölmesinde **Konteyneri kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="12f10-509">**Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="12f10-510">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-510">Select **OK**.</span></span> <span data-ttu-id="12f10-511">Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="12f10-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="12f10-512">**Plaka veya sevkiyat** alanına, satış siparişi 2'nin satır 2'si için hedef LP girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="12f10-513">Ardından alanın dışına gitmek için klavyenizden **Sekme** veya **Enter** tuşunu seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="12f10-514">Eylem Bölmesinde **Yeni konteyner** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="12f10-515">Tüm varsayılan ayarları kabul edin ve **Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="12f10-516">Konteyner kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="12f10-517">**Madde paketleme** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="12f10-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="12f10-518">**Miktar:** *1*</span><span class="sxs-lookup"><span data-stu-id="12f10-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="12f10-519">**Tanımlayıcı alanı:** Madde *A0002*</span><span class="sxs-lookup"><span data-stu-id="12f10-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="12f10-520">Eylem Bölmesinde **Konteyneri kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="12f10-521">**Konteyneri kapat** iletişim kutusunda, sistemin **Brüt ağırlık** alanını güncelleştirmesi için **Sistem ağırlığını al** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="12f10-522">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-522">Select **OK**.</span></span> <span data-ttu-id="12f10-523">Konteyner, *TASNİF* yerleşimine taşınır ve tasnif için hazırdır.</span><span class="sxs-lookup"><span data-stu-id="12f10-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="12f10-524">Konteyner ayrıntılarını görüntülemek için **Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Konteynerler** 'e gidin ve paketleme sırasında oluşturulan konteyner kodlarını arayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers** , and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="12f10-525">Konteynerleri tasnif etme</span><span class="sxs-lookup"><span data-stu-id="12f10-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12f10-526">Giden tasnifi yapmak için mobil uygulamada **Palet derleme** menü öğesine eriştiğinizde, **Tam** olarak etiketlenmiş bir düğme görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="12f10-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="12f10-527">*Konumu tasnif etmek veya kapatmak için **Tam** düğmesini kullanmayın.*</span><span class="sxs-lookup"><span data-stu-id="12f10-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="12f10-528">**Tam** düğmesi varsayılan olarak sağlanır ve devre dışı bırakılamaz veya sayfadan kaldırılamaz.</span><span class="sxs-lookup"><span data-stu-id="12f10-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="12f10-529">*Giden tasnif* özelliği için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="12f10-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="12f10-530">İlk konteyneri tasnif etme</span><span class="sxs-lookup"><span data-stu-id="12f10-530">Sort the first container</span></span>

1. <span data-ttu-id="12f10-531">Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62* 'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="12f10-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="12f10-532">Ana menüde **Giden** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="12f10-533">**Giden** menüsünden **Palet derleme** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="12f10-534">**LP/Kon** alanına, satış siparişi 1 ile ilişkilendirilen ilk konteyner kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="12f10-535">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-535">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-536">Şu anda tasnif konumu bulunmadığından, bir tane belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="12f10-537">**Tasnif konumu kodu** alanına *SP01* girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="12f10-538">Şu anda *SP01* sıralama konumuyla ilişkilendirilmiş bir LP olmadığından, bir tane belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-538">Because no LP is currently associated with sort position *SP01* , you must specify one.</span></span> <span data-ttu-id="12f10-539">**LP** alanına *PLP01* girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="12f10-540">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-540">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-541">Tasnif konumu doğrulaması açık olduğundan, tasnif konumu kodunu yeniden girmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="12f10-542">**Tasnif Konumu kodu** alanına *SP01* girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="12f10-543">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-543">Select **OK**.</span></span>

    <span data-ttu-id="12f10-544">Bir "İş tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="12f10-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="12f10-545">Tasnif konumunu ve içindeki LP'yi görüntülemek için **Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Giden tasnif konumu atamaları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="12f10-546">**Giden tasnif konumu atamaları** sayfası, etkin olan tüm tasnif konumlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="12f10-547">**Tasnif konumu hareketleri** alanı, her tasnif konumuyla ilişkilendirilmiş LP'yi ve tasnif konumundaki konteynerleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="12f10-548">Bir tasnif konumunun var olduğuna ve **Tasnif konumu ölçütleri** hızlı sekmesinin **Sevkiyat – Taşıyıcı hizmeti - Hava** ölçütünü gösterdiğine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="12f10-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="12f10-549">Kalan konteynerleri tasnif etme</span><span class="sxs-lookup"><span data-stu-id="12f10-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="12f10-550">Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62* 'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="12f10-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="12f10-551">Ana menüde **Giden** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="12f10-552">**Giden** menüsünden **Palet derleme** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="12f10-553">**LP/Kon** alanına, satış siparişi 1 ile ilişkilendirilen ikinci konteyner kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="12f10-554">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-554">Select **OK**.</span></span> <span data-ttu-id="12f10-555">Tasnif şablonu otomatik olarak tasnif edecek şekilde ayarlandığından ve eşleşen ölçütleri olan bir tasnif konumu zaten var olduğundan, otomatik olarak doğru tasnif konumuna yönlendirilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="12f10-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="12f10-556">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-556">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-557">Stoğun doğru yerde olduğunu belirtmek için tasnif konumu kodunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="12f10-558">**Tasnif Konumu kodu** alanına *SP01* girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="12f10-559">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-559">Select **OK**.</span></span>

    <span data-ttu-id="12f10-560">İş satış siparişi 1'deki ikinci konteynerden tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="12f10-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="12f10-561">Şimdi, satış siparişi 2'deki kalan konteynerleri tasnif etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="12f10-562">**LP/Kon** alanına, *A0001* maddesini içeren satış siparişi 2'deki konteynerin konteyner kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="12f10-563">Taşıyıcı hizmeti farklı olduğundan, yeni bir tasnif konumu girmeniz ve o konuma bir LP atamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="12f10-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="12f10-564">Tasnif konumu *SP02* 'yi ve LP *PLP02* 'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="12f10-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="12f10-565">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-565">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-566">*Tasnif konumu kodu* alanına **SP02** girerek tasnif konumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="12f10-567">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-567">Select **OK**.</span></span>

    <span data-ttu-id="12f10-568">İş konteynerde tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="12f10-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="12f10-569">**LP/Kon** alanına, *A0002* maddesini içeren satış siparişi 2'deki kalan konteynerin konteyner kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="12f10-570">Taşıyıcı hizmeti satış siparişi 1'in taşıyıcı hizmetiyle aynı olduğundan sistem eşleşen ölçütlere sahip mevcut tasnif konumunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="12f10-571">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-571">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-572">*Tasnif konumu kodu* alanına **SP01** girerek tasnif konumunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="12f10-573">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-573">Select **OK**.</span></span>

    <span data-ttu-id="12f10-574">İş konteynerde tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="12f10-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="12f10-575">Giden tasnif konumlarını kapatma</span><span class="sxs-lookup"><span data-stu-id="12f10-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="12f10-576">Tüm stoklar tasnif edildiğinde, işin oluşturulabilmesi için konumun kapatılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="12f10-577">Tasnif edilen stok çekme işi, stoğu bölme kapısına almak amacıyla oluşturulacaktır.</span><span class="sxs-lookup"><span data-stu-id="12f10-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="12f10-578">Konumu mobil cihazdan kapatma</span><span class="sxs-lookup"><span data-stu-id="12f10-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="12f10-579">Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62* 'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="12f10-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="12f10-580">Ana menüde **Giden** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="12f10-581">**Giden** menüsünden **Palet derleme** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="12f10-582">**LP/Kon** alanına, *SP01* tasnif konumuna tasnif edilmiş olan bir konteyner kodu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="12f10-583">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-583">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-584">Aşağıdaki iletiyi alırsınız: "Konteyner zaten SP01 konumuna tasnif edilmiş.</span><span class="sxs-lookup"><span data-stu-id="12f10-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="12f10-585">Konum kapatılsın mı?"</span><span class="sxs-lookup"><span data-stu-id="12f10-585">Close the position?"</span></span> <span data-ttu-id="12f10-586">**Kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-586">Select **Close**.</span></span>

    <span data-ttu-id="12f10-587">İş tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="12f10-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="12f10-588">Giden tasnif konumu atamalarından konum kapatma</span><span class="sxs-lookup"><span data-stu-id="12f10-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="12f10-589">**Ambar yönetimi \> Paketleme ve konteyner kullanımı \> Giden tasnif konumu atamaları** 'na gidin.</span><span class="sxs-lookup"><span data-stu-id="12f10-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="12f10-590">Sol sütunda **SP02 seçin**.</span><span class="sxs-lookup"><span data-stu-id="12f10-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="12f10-591">Bu giden tasnif konumu satırı kapatacağınız konum satırıdır.</span><span class="sxs-lookup"><span data-stu-id="12f10-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="12f10-592">Eylem Bölmesinde **Konumu kapat** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="12f10-593">Tasnif konumu kaydı kapatılır ve artık gösterilmez.</span><span class="sxs-lookup"><span data-stu-id="12f10-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="12f10-594">Tüm kapalı konum kayıtlarını göstermek için, **Kapalı olanı göster** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="12f10-595">Tasnif edilmiş stok çekme</span><span class="sxs-lookup"><span data-stu-id="12f10-595">Sorted inventory picking</span></span>

<span data-ttu-id="12f10-596">Tasnif edilen stok çekme işini tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f10-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="12f10-597">Tamamlandığında, stok satış siparişine çekilir.</span><span class="sxs-lookup"><span data-stu-id="12f10-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="12f10-598">Bu noktada, diğer tüm ambar süreçleri geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="12f10-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="12f10-599">Mobil cihazda, bu senaryo için oluşturduğunuz Kullanıcı kimliğini (veya mevcut demo veri kullanıcısının kullanıcı kimliğini) kullanarak ambar *62* 'de oturum açın.</span><span class="sxs-lookup"><span data-stu-id="12f10-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="12f10-600">Ana menüde **Giden** 'i seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="12f10-601">**Giden** menüsünde, **Tasniften yükle** 'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="12f10-602">İlk tasnif konumu olan *SP01* 'den hedef LP kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="12f10-603">**Kod** alanını *PLP01* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="12f10-604">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-604">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-605">**Tasnif edilen stok çekme: Çekme** sayfası gerçekleştirilmesi gereken çekme işini gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="12f10-606">Birden fazla madde içeren ve *3* miktarına sahip olan *TASNİF* yerleşiminden ve hedef plaka *PLP01* 'den çekin.</span><span class="sxs-lookup"><span data-stu-id="12f10-606">Pick from the *SORT* location and target LP *PLP01* , which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="12f10-607">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-607">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-608">**Tasnif edilen stok çekme: Yerine koyma** sayfası gerçekleştirilmesi gereken yerine koyma işini gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="12f10-609">Birden fazla madde içeren ve *3* miktarına sahip olan *Bölme kapısı* yerleşimine ve hedef plaka *PLP01* 'e koyun.</span><span class="sxs-lookup"><span data-stu-id="12f10-609">Put to the *Baydoor* location and target LP *PLP01* , which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="12f10-610">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-610">Select **OK**.</span></span>

    <span data-ttu-id="12f10-611">İş tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="12f10-611">Work is completed.</span></span>

1. <span data-ttu-id="12f10-612">İkinci tasnif konumu olan *SP02* 'den hedef plaka kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="12f10-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="12f10-613">**Kod** alanını *PLP02* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f10-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="12f10-614">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-614">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-615">**Tasnif edilen stok çekme: Çekme** sayfası gerçekleştirilmesi gereken çekme işini gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="12f10-616">Birden fazla madde içeren ve *1* miktarına sahip olan *TASNİF* yerleşiminden ve hedef plaka *PLP02* 'den çekin.</span><span class="sxs-lookup"><span data-stu-id="12f10-616">Pick from the *SORT* location and target LP *PLP02* , which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="12f10-617">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-617">Select **OK**.</span></span>
1. <span data-ttu-id="12f10-618">**Tasnif edilen stok çekme: Yerine koyma** sayfası gerçekleştirilmesi gereken yerine koyma işini gösterir.</span><span class="sxs-lookup"><span data-stu-id="12f10-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="12f10-619">Birden fazla madde içeren ve *1* miktarına sahip olan *Bölme kapısı* yerleşimine ve hedef plaka *PLP02* 'e koyun.</span><span class="sxs-lookup"><span data-stu-id="12f10-619">Put to the *Baydoor* location and target LP *PLP02* , which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="12f10-620">**Tamam** 'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f10-620">Select **OK**.</span></span>

    <span data-ttu-id="12f10-621">İş tamamlanır.</span><span class="sxs-lookup"><span data-stu-id="12f10-621">Work is completed.</span></span>

<span data-ttu-id="12f10-622">Bu noktadan itibaren, diğer tüm ambar süreçleri geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="12f10-622">From this point forward, all other warehouse processes apply.</span></span>
