---
title: Madde konsolidasyonu - yerleşim kullanımı
description: Bu konu, ambar yöneticilerinin ambar içindeki yerleşimlerin hacimsel kullanımını görüntülemesini ve filtrelemesini kolaylaştıran işlev hakkında bilgi sağlar. Yöneticiler yerleşimleri seçip maddeleri konsolide etmek ve böylece ambar alanını daha iyi kullanabilmek için Madde Konsolidasyonu sayfasından doğrudan stok hareketi işi oluşturabilirler.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3b20b41d27e5faeac7ea88940c086ae33390dc29
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217017"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="4e65e-104">Madde konsolidasyonu - yerleşim kullanımı</span><span class="sxs-lookup"><span data-stu-id="4e65e-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e65e-105">Bu konu, ambar yöneticilerinin ambar içindeki yerleşimlerin hacimsel kullanımını görüntülemesini ve filtrelemesini kolaylaştıran işlev hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="4e65e-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="4e65e-106">Yöneticiler yerleşimleri seçip maddeleri konsolide etmek ve böylece ambar alanını daha iyi kullanabilmek için **Madde Konsolidasyonu** sayfasından doğrudan stok hareketi işi oluşturabilirler.</span><span class="sxs-lookup"><span data-stu-id="4e65e-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="4e65e-107">Özellikleri etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="4e65e-107">Turn on the features</span></span>

<span data-ttu-id="4e65e-108">Bu konuda açıklanan özellikleri kullanabilmeniz için, önce bunları sisteminizde açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="4e65e-109">Yöneticiler bu özelliklerin durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="4e65e-110">Aşağıdaki özelliklerin her ikisini de listelendikleri sırayla açın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="4e65e-111">(Her iki özellik de **Ambar Yönetimi** modülünde yer alır.)</span><span class="sxs-lookup"><span data-stu-id="4e65e-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="4e65e-112">Ambar yerleşimi durumu</span><span class="sxs-lookup"><span data-stu-id="4e65e-112">Warehouse location status</span></span>
2. <span data-ttu-id="4e65e-113">Madde konsolidasyon yerleşimi kullanımı</span><span class="sxs-lookup"><span data-stu-id="4e65e-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="4e65e-114">Ambar yerleşimi durumu</span><span class="sxs-lookup"><span data-stu-id="4e65e-114">Warehouse location status</span></span>

<span data-ttu-id="4e65e-115">*Ambar yerleşimi durumu* özelliği, **Yerleşimler** sayfasına yerleşimin geçerli durumuyla ilgili ek bilgileri izlemek için dört yeni alan ekler:</span><span class="sxs-lookup"><span data-stu-id="4e65e-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="4e65e-116">**Madde numarası** – Yerleşimdeki mevcut madde.</span><span class="sxs-lookup"><span data-stu-id="4e65e-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="4e65e-117">Yerleşimde birden çok madde varsa bu alan boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="4e65e-118">**Son faaliyet tarih ve saati** – Yerleşime göre gerçekleştirilen son ambar hareketinin zaman damgası.</span><span class="sxs-lookup"><span data-stu-id="4e65e-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="4e65e-119">**Yaşlandırma tarihi** – Yerleşimdeki stokun ambara alındığı tarih.</span><span class="sxs-lookup"><span data-stu-id="4e65e-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="4e65e-120">Bu tarih, yaşlandırma tarihi temel alınarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="4e65e-121">Bu tarih, plaka izlemeli yerleşimler için doğru olsa da ancak plaka izlenmeyen yerleşimler için doğru olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="4e65e-122">**Yerleşim durumu** – Yerleşimin durumu.</span><span class="sxs-lookup"><span data-stu-id="4e65e-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="4e65e-123">Kullanılabilir dört değer bulunur:</span><span class="sxs-lookup"><span data-stu-id="4e65e-123">Four values are available:</span></span>

    - <span data-ttu-id="4e65e-124">**Belirlenmemiş** – Yerleşim profili durumu izlemez.</span><span class="sxs-lookup"><span data-stu-id="4e65e-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="4e65e-125">Bu nedenle, geçerli durum bilinmiyor demektir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="4e65e-126">**Boş** – Şu anda yerleşimde stok yok.</span><span class="sxs-lookup"><span data-stu-id="4e65e-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="4e65e-127">**Malzeme çekme** – Son boş olduğu zamandan sonra yerleşime karşı giden hareketler gerçekleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="4e65e-128">**Depolama** – Son boş olduğu zamandan sonra gelen hareketler gerçekleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="4e65e-129">Bu alanlar ambar yöneticilerinin ambar yerleşimlerinin durumu hakkında daha iyi genel fikir edinmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="4e65e-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="4e65e-130">Ayrıca, daha gelişmiş raporlama ve filtreleme işlemlerine de izin verir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="4e65e-131">Madde konsolidasyonu ve yerleşim kullanımını ayarlama</span><span class="sxs-lookup"><span data-stu-id="4e65e-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="4e65e-132">Bu bölümde, sistemin madde konsolidasyonu ve yerleşim kullanımını kullanmak için nasıl hazırlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="4e65e-133">Bu yordamlar, standart demo verilerinden örnek değerleri kullanır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="4e65e-134">Bu konunun ilerleyen kısımlarında sağlanan örnek senaryo aracılığıyla çalışmayı planlıyorsanız, **USMF** tüzel kişiliğini (standart demo verilerini içeren) seçin ve bu bölümde açıklanan her kaydı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4e65e-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="4e65e-135">Örnek senaryo aracılığıyla çalışmayı planlamıyorsanız, burada sağlanan değerler, özellikleri kullanmak için tamamlamanız gereken kurulum türleriyle ilgili örnekler olarak kabul edilebilir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="4e65e-136">Serbest bırakılan ürün</span><span class="sxs-lookup"><span data-stu-id="4e65e-136">Released product</span></span>

1. <span data-ttu-id="4e65e-137">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4e65e-138">**Madde numarası** alanında, *M9201* seçeneğini belirleyin ve ayrıntılar sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="4e65e-139">Eylem Bölmesinde, **Stoğu yönet** sekmesindeki **Ambar** grubunda, **Fiziksel boyutlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="4e65e-140">**Fiziksel boyut** sayfasında, eylem bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="4e65e-141">Kılavuza yeni bir satır eklenir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-141">A new line is added to the grid.</span></span> <span data-ttu-id="4e65e-142">**Madde numarası** alanı önceden ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="4e65e-143">**Birim** alanında *ea*'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="4e65e-144">Satırdaki kalan alanlar otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="4e65e-145">**Kaydet**'i seçip sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="4e65e-146">Yerleşim profili</span><span class="sxs-lookup"><span data-stu-id="4e65e-146">Location profile</span></span>

1. <span data-ttu-id="4e65e-147">**Ambar yönetimi \> Kurulum \> Ambar \> Konum profilleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="4e65e-148">Yerleşim profilleri listesinde **FLOOR-05**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="4e65e-149">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4e65e-150">**Genel** hızlı sekmesinde, aşağıdaki seçeneklerin her ikisinin de *Evet* olarak ayarlandığından emin olun:</span><span class="sxs-lookup"><span data-stu-id="4e65e-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="4e65e-151">Maddeyi yerleşimde etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4e65e-151">Enable item in location</span></span>
    - <span data-ttu-id="4e65e-152">Yerleşim durumunu etkinleştir</span><span class="sxs-lookup"><span data-stu-id="4e65e-152">Enable location status</span></span>

1. <span data-ttu-id="4e65e-153">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="4e65e-154">**Yerleşimde madde etkinleştir** ve **Yerleşim durumunu etkinleştir** seçenekleri zaten *Evet* olarak ayarlandıysa , 10. adımda **Boyutlar** hızlı sekmesini ayarlama yönergelerine atlayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="4e65e-155">Seçenekler önceden *Evet* olarak ayarlanmamışsa , bunları el ile ayarladıktan sonra **Ambar yönetimi** modülü için bir tutarlılık denetimi çalıştırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="4e65e-156">Bu durumda, sonraki adımla devam edin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="4e65e-157">Tutarlılık denetimini çalıştırmak için, **Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Tutarlılık denetimi** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="4e65e-158">**Tutarlılık denetimi** iletişim kutusunda aşağıdaki değerleri ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="4e65e-159">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="4e65e-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="4e65e-160">**Denetle/Onar:** *Denetle*</span><span class="sxs-lookup"><span data-stu-id="4e65e-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="4e65e-161">**Başlangıç tarihi:** Bu alanı boş bırakın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="4e65e-162">**Ambar yerleşim durumu tutarlılık denetimi:** Bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="4e65e-163">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="4e65e-164">Tutarlılık denetimi tamamlandığında bir bildirim alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4e65e-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="4e65e-165">İletiyi görüntülemek için [İşlem Merkezi](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications)'ni açın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="4e65e-166">Ayrıntıları görüntülemek için **İleti ayrıntıları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="4e65e-167">Tutarlılık denetimi iletisinde "Ambar XX'deki XXXX yerleşimi için yanlış yerleşim durumu bilgileri bulundu" ifadesi varsa tutarlılık denetimini tekrar çalıştırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="4e65e-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="4e65e-168">Bu kez, **Denetle/Onar** alanını *Hatayı düzelt* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="4e65e-169">Herhangi bir hata bulunmadığından emin olmak için iletileri görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="4e65e-170">Şimdi yerleşim profili kurulumunu tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="4e65e-171">**Ambar Yönetimi \> Kurulum \> Ambar \> Yerleşim profilleri**'ne dönün, yerleşim profili **FLOOR-05**'i seçin ve eylem bölmesinde **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4e65e-172">**Boyutlar** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4e65e-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4e65e-173">**Hacim kullanım yüzdesi:** *100*</span><span class="sxs-lookup"><span data-stu-id="4e65e-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="4e65e-174">**Stok yerleşimi için kullanılan hacimsel yöntem:** *Yerleşim hacmi kullan*</span><span class="sxs-lookup"><span data-stu-id="4e65e-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="4e65e-175">**Gerçek yerleşim yüksekliği:** *10*</span><span class="sxs-lookup"><span data-stu-id="4e65e-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="4e65e-176">**Gerçek yerleşim genişliği:** *10*</span><span class="sxs-lookup"><span data-stu-id="4e65e-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="4e65e-177">**Gerçek yerleşim derinliği:** *10*</span><span class="sxs-lookup"><span data-stu-id="4e65e-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="4e65e-178">**Maksimum ağırlık:** *100*</span><span class="sxs-lookup"><span data-stu-id="4e65e-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="4e65e-179">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="4e65e-180">Mobil cihaz menü öğeleri</span><span class="sxs-lookup"><span data-stu-id="4e65e-180">Mobile device menu items</span></span>

1. <span data-ttu-id="4e65e-181">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü öğeleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="4e65e-182">Eylem bölmesinde, sıralama amacıyla kullanılacak menü öğesini oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="4e65e-183">Üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4e65e-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="4e65e-184">**Menü öğesi adı:** *Ayarla*</span><span class="sxs-lookup"><span data-stu-id="4e65e-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="4e65e-185">**Başlık:** *Ayarla*</span><span class="sxs-lookup"><span data-stu-id="4e65e-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="4e65e-186">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="4e65e-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="4e65e-187">**Varolan çalışmayı kullan:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="4e65e-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="4e65e-188">**Genel** hızlı sekmesinde, aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4e65e-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="4e65e-189">**İş oluşturma işlemi:** *Ayarlama*</span><span class="sxs-lookup"><span data-stu-id="4e65e-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="4e65e-190">**Stok ayarlama türleri:** *Ayarlama*</span><span class="sxs-lookup"><span data-stu-id="4e65e-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="4e65e-191">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="4e65e-192">Mobil cihaz menüsü</span><span class="sxs-lookup"><span data-stu-id="4e65e-192">Mobile device menu</span></span>

1. <span data-ttu-id="4e65e-193">**Ambar yönetimi \> Kurulum \> Mobil cihaz \> Mobil cihaz menüsü**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="4e65e-194">Menüler listesinde **Stok** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="4e65e-195">Eylem Bölmesi'nde, **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="4e65e-196">**Mevcut menüler ve menü öğeleri** listesinde, **Ayarla** menüsü öğesini bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="4e65e-197">**Ayarla**'yı **Menü Yapısı** listesine taşımak için sağ ok düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="4e65e-198">Böylece, yeni menü öğesini seçili menüye eklersiniz.</span><span class="sxs-lookup"><span data-stu-id="4e65e-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="4e65e-199">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="4e65e-200">Hareket türleri</span><span class="sxs-lookup"><span data-stu-id="4e65e-200">Movement types</span></span>

1. <span data-ttu-id="4e65e-201">**Ambar yönetimi \> Kurulum \> Stok \> Hareket türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="4e65e-202">Eylem bölmesinde **Yeni**'yi seçin ve ardından aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4e65e-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="4e65e-203">**Hareket türü kodu:** *KONSOLİDE ETME*</span><span class="sxs-lookup"><span data-stu-id="4e65e-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="4e65e-204">**Açıklama:** *Yerleşimleri konsolide et*</span><span class="sxs-lookup"><span data-stu-id="4e65e-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="4e65e-205">**İş sınıfı kodu:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="4e65e-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="4e65e-206">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="4e65e-207">Örnek senaryo</span><span class="sxs-lookup"><span data-stu-id="4e65e-207">Example scenario</span></span>

<span data-ttu-id="4e65e-208">Aşağıdaki senaryo, ambarda iki yerleşimde stok *ayarlaması* yapmak için mobil cihazda ambar uygulamasını kullanır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="4e65e-209">Yerleşimlere stok ekleme</span><span class="sxs-lookup"><span data-stu-id="4e65e-209">Add inventory to locations</span></span>

1. <span data-ttu-id="4e65e-210">Ambar *51* için ayarlanmış olan bir kullanıcı olarak mobil cihazda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="4e65e-211">**Stok \> Ayarla**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="4e65e-212">Şimdi ilk yerleşim ayarlamasını gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="4e65e-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="4e65e-213">**Ayarlama** görevinde stok ayarlamasının yapılacağı yerleşimi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="4e65e-214">**YERLEŞİM** alanında, *Lp-001*'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="4e65e-215">Yerleşimi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-215">Confirm the location.</span></span>
1. <span data-ttu-id="4e65e-216">Yerleşime eklenecek madde için bir plaka kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4e65e-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="4e65e-217">**LP** alanına *LP00101* girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="4e65e-218">Plakayı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="4e65e-219">Plakaya eklenecek maddeyi girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="4e65e-220">**ITEM** alanına *M9201* girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="4e65e-221">Maddeyi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-221">Confirm the item.</span></span>
1. <span data-ttu-id="4e65e-222">Eklenecek madde miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="4e65e-223">**MİKTAR** alanına, *10* girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="4e65e-224">Onaylanan miktar.</span><span class="sxs-lookup"><span data-stu-id="4e65e-224">Confirm the quantity.</span></span>

    <span data-ttu-id="4e65e-225">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4e65e-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="4e65e-226">Şimdi ikinci yerleşim ayarlamasını gireceksiniz.</span><span class="sxs-lookup"><span data-stu-id="4e65e-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="4e65e-227">**Ayarlama** görevinde stok ayarlamasının yapılacağı yerleşimi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="4e65e-228">**YERLEŞİM** alanında, *Lp-002*'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="4e65e-229">Yerleşimi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-229">Confirm the location.</span></span>
1. <span data-ttu-id="4e65e-230">Yerleşime eklenecek madde için bir plaka kodu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="4e65e-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="4e65e-231">**LP** alanına *LP00201* girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="4e65e-232">Plakayı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="4e65e-233">Plakaya eklenecek maddeyi girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="4e65e-234">**ITEM** alanına *M9201* girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="4e65e-235">Maddeyi onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-235">Confirm the item.</span></span>
1. <span data-ttu-id="4e65e-236">Eklenecek madde miktarını girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="4e65e-237">**MİKTAR** alanına, *15* girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="4e65e-238">Miktarı onaylayın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-238">Confirm the quantity.</span></span>

    <span data-ttu-id="4e65e-239">Bir "İş Tamamlandı" iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4e65e-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="4e65e-240">Menü düğmesini seçin (bazen hamburger veya hamburger düğmesi olarak da adlandırılır) ve **Ayarlama** görevinden çıkmak için **İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="4e65e-241">Yerleşimleri konsolide etme</span><span class="sxs-lookup"><span data-stu-id="4e65e-241">Consolidate locations</span></span>

1. <span data-ttu-id="4e65e-242">**Ambar Yönetimi \> Periyodik görevler \> Madde konsolidasyonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="4e65e-243">Başlıkta, konsolidasyon yapılacak bir ambar seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="4e65e-244">**Ambar** alanına *51* girin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="4e65e-245">Madde *M9201*'in ayarlandığı her yerleşim için bir kayıt gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="4e65e-246">**Kullanım yüzdesi** sütunu her yerleşimin hacimsel kullanımını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4e65e-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="4e65e-247">Stok konsolide etmek için, konsolide edilmesi gereken tüm yerleşimleri seçin ve sonra Eylem Bölmesinde **Stoğu konsolide et**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="4e65e-248">**Stoğu konsolide et** iletişim kutusunda, stok hareketi için iş oluşturmak üzere kullanılması gereken konumu ve hareket türünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="4e65e-249">Aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="4e65e-249">Set the following values:</span></span>

    - <span data-ttu-id="4e65e-250">**Yerleşim:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="4e65e-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="4e65e-251">**Hareket türü kodu:** *KONSOLİDE ETME*</span><span class="sxs-lookup"><span data-stu-id="4e65e-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="4e65e-252">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-252">Select **OK**.</span></span>
1. <span data-ttu-id="4e65e-253">Ouşturulan hareket işini gösteren bir bilgi iletisi alırsınız.</span><span class="sxs-lookup"><span data-stu-id="4e65e-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="4e65e-254">Hareket işi kodunu not edin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="4e65e-255">Hareket işini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="4e65e-255">View movement work</span></span>

1. <span data-ttu-id="4e65e-256">**Ambar yönetimi \> İş \> İş ayrıntıları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="4e65e-257">Oluşturulan işi görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4e65e-257">View the work that was created.</span></span> <span data-ttu-id="4e65e-258">İş kılavuzuna filtre uygulamak veya arama yapmak için stok konsolidasyonundan hareket işi kodunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e65e-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="4e65e-259">Bu senaryoda, stok konsolidasyon yerleşimi olarak stok içeren mevcut bir yerleşim kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4e65e-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="4e65e-260">Bu nedenle, yalnızca bir iş kodu oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="4e65e-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="4e65e-261">Sistem, tamamlanması gereken her bir hareket için bir iş kodu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4e65e-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="4e65e-262">Önceden stok içeren bir yerleşim belirlerseniz, yalnızca bir iş kodu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4e65e-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="4e65e-263">Yeni bir yerleşim belirtirseniz, iki iş kodu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4e65e-263">If you specify a new location, two work IDs are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]