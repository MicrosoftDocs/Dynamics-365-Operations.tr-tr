---
title: WMS özellikli bir ambarda yerleşimleri yapılandırma
description: Bu kılavuz, yeni bir WMS etkin ambarın (gelişmiş ambar yönetimi süreçleri kullanan bir ambarın) konum kurulumunun nasıl yapılandırılacağını gösterir.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2be3c7cb33225041872e8b747ba28063f897dae9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "337337"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="ba6da-103">WMS özellikli bir ambarda yerleşimleri yapılandırma</span><span class="sxs-lookup"><span data-stu-id="ba6da-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ba6da-104">Bu kılavuz, yeni bir WMS etkin ambarın (gelişmiş ambar yönetimi süreçleri kullanan bir ambarın) konum kurulumunun nasıl yapılandırılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="ba6da-105">Bu işlem genellikle ambar yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="ba6da-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="ba6da-106">Bu kılavuzu, demo verileri şirketi USMF'yi veya kendi verilerinizi kullanarak yerine getirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba6da-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="ba6da-107">Bir önkoşul, yapılandırılmış en az bir tesis olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="ba6da-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="ba6da-108">Yeni bir ambar oluşturun</span><span class="sxs-lookup"><span data-stu-id="ba6da-108">Create a new warehouse</span></span>
1. <span data-ttu-id="ba6da-109">Ambarlara git.</span><span class="sxs-lookup"><span data-stu-id="ba6da-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="ba6da-110">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-110">Click New.</span></span>
3. <span data-ttu-id="ba6da-111">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="ba6da-112">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ba6da-113">Tesis alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="ba6da-114">Ambar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="ba6da-115">Ambar yönetimi süreçleri kullanımını Evet olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="ba6da-116">Bu ayar, ambar çalışma ve mobil aygıtları kullanarak gelişmiş ambar işlemleri çalıştırmanızı sağlar.</span><span class="sxs-lookup"><span data-stu-id="ba6da-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="ba6da-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="ba6da-118">Konum biçimi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-118">Define a location format</span></span>
1. <span data-ttu-id="ba6da-119">Konum biçimlerine git.</span><span class="sxs-lookup"><span data-stu-id="ba6da-119">Go to Location formats.</span></span>
    * <span data-ttu-id="ba6da-120">Konum biçimleri, bir ambar içinde kullanılan farklı konum bölme pozisyonları için tutarlı ve benzersiz adlar oluşturmak için kullanılan isim sistemi biçimlerdir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="ba6da-121">Ayırıcıları, yerleşimin koridor numarası gibi bileşenlerini tanımlamayı kolaylaştırmak için bir konum biçimi parçası olarak kullanmak için yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="ba6da-122">Bu örnekte, dört bileşenli bir isim oluşturacağız.</span><span class="sxs-lookup"><span data-stu-id="ba6da-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="ba6da-123">Örneğin, bu koridor, dolap, raf ve bölme olabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="ba6da-124">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-124">Click New.</span></span>
3. <span data-ttu-id="ba6da-125">Konum biçimi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="ba6da-126">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ba6da-127">Segment tanımı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="ba6da-128">Bu konum adının ilk bölmesinin neyi temsil ettiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="ba6da-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="ba6da-129">Örneğin bu, koridor olabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="ba6da-130">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="ba6da-131">Bu, bu yerleşim adı bölümünün kaç karakter olması gerektiğini belirler.</span><span class="sxs-lookup"><span data-stu-id="ba6da-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="ba6da-132">Unutmayın, ayırıcılar da dahil olmak üzere, adın tüm bileşenlerinin toplam 10 karakterden uzun olamaz.</span><span class="sxs-lookup"><span data-stu-id="ba6da-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="ba6da-133">Ayırıcı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="ba6da-134">Bu, adın birinci ve ikinci bileşeni arasında hangi karakter veya simgenin kullanıldığını belirler.</span><span class="sxs-lookup"><span data-stu-id="ba6da-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="ba6da-135">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-135">Click New.</span></span>
9. <span data-ttu-id="ba6da-136">Segment tanımı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="ba6da-137">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="ba6da-138">Ayırıcı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="ba6da-139">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-139">Click New.</span></span>
13. <span data-ttu-id="ba6da-140">Segment tanımı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="ba6da-141">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="ba6da-142">Ayırıcı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="ba6da-143">Yeni'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-143">Click New.</span></span>
17. <span data-ttu-id="ba6da-144">Segment tanımı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="ba6da-145">Uzunluk alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="ba6da-146">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-146">Click Save.</span></span>
20. <span data-ttu-id="ba6da-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="ba6da-148">Konum türlerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="ba6da-148">Define location types</span></span>
1. <span data-ttu-id="ba6da-149">Konum türlerine git.</span><span class="sxs-lookup"><span data-stu-id="ba6da-149">Go to Location types.</span></span>
    * <span data-ttu-id="ba6da-150">Yerleşim tipleri farklı ambar yönetimi işlemlerini denetlemek için filtreleme seçenekleri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="ba6da-151">En düşük gereksinim olarak giden ambar yönetimi işlemi tanımlamak için hazırlama ve son sevkiyat yerleşim tiplerini oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="ba6da-152">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-152">Click New.</span></span>
3. <span data-ttu-id="ba6da-153">Konum türü alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="ba6da-154">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ba6da-155">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="ba6da-156">Konum profilleri tanımlayın</span><span class="sxs-lookup"><span data-stu-id="ba6da-156">Define location profile</span></span>
1. <span data-ttu-id="ba6da-157">Konum profillerine gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="ba6da-158">Konum profillerinin tanımı çok önemlidir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="ba6da-159">Gruplandırılmış konum kapasitelerinin yanı sıra, hangi stokun depolanacağı ve nasıl depolandığına dair ilgili ilkeler buradan kontrol edilebilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="ba6da-160">Yerleşim profilleri farklı ambar yönetimi işlemlerini denetlemek için filtreleme seçenekleri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="ba6da-161">En düşük gereksinim olarak ambar yönetimi işlemlerini etkinleştirmek için bir kullanıcı konumu profili oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="ba6da-162">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-162">Click New.</span></span>
3. <span data-ttu-id="ba6da-163">Konum profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="ba6da-164">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ba6da-165">Konum formatı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ba6da-166">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ba6da-167">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ba6da-168">Konum türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ba6da-169">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ba6da-170">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ba6da-171">Karışık stok durumlarına izin ver onay kutusunu işaretleyin veya bu onay kutusunun işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="ba6da-172">Bu konum profiline göre gruplandırılacak konumlarda karışık stok durum değerlerine izin vermek istiyorsanız bu seçeneği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="ba6da-173">Toplu günler için atlatma kuralları onay kutusunu işaretleyin veya onay kutusundaki işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="ba6da-174">Bu kurala uymayan stok toplu işlerinin karıştırılmasına izin vermek istiyorsanız, stok toplu sona erme tarihlerinin kaç gün farklılık gösterebileceğine dair kuralı geçersiz kılmak için bu seçeneği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="ba6da-175">Döngü sayımına izin ver onay kutusunu işaretleyin veya onay kutusundaki işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="ba6da-176">Bu konum profiline göre gruplandırılacak tüm konumlarda döngü sayımı işlemesine izin vermek istiyorsanız bu seçeneği etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="ba6da-177">Boyutlar bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="ba6da-178">Boyutlar sekmesi, konumlardan her birinin içindeki yük kapasitesini hassas şekilde hesaplamak için parametreler ve yöntemler tanımlamanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="ba6da-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="ba6da-179">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="ba6da-180">Ambar yönetim parametrelerini etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="ba6da-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="ba6da-181">Ambar yönetim parametrelerine gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="ba6da-182">Ambar işlerini işlemeye hazırlayabilmek için, kullanıcı konum profili, hazırlama konum türü ve son sevkiyat konum türü için parametreler ayarlamanız gerekir. Giden işlemler, tanımladığınız son sevkiyat konum türünde biter bitmez, ilgili giden hareketleri 'Çekildi' olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="ba6da-183">Konum profilleri bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="ba6da-184">Kullanıcı konumu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ba6da-185">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ba6da-186">Konum türleri bölümünü genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="ba6da-187">Depolama konum türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ba6da-188">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ba6da-189">Son yükleme konumu türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ba6da-190">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ba6da-191">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="ba6da-192">Ambar bölge gruplarını tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="ba6da-193">Ambar bölge gruplarına gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="ba6da-194">Ambar bölgeleri, farklı ambar yönetimi işlemlerini denetleme seçenekleri için filtre olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="ba6da-195">Bir bölge tanımlamadan önce bölge grubu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="ba6da-196">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-196">Click New.</span></span>
3. <span data-ttu-id="ba6da-197">Bölge grubu numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="ba6da-198">Bölge grubu adı alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="ba6da-199">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="ba6da-200">Ambar bölgelerini tanımlayın</span><span class="sxs-lookup"><span data-stu-id="ba6da-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="ba6da-201">Gidilecek bölgeler.</span><span class="sxs-lookup"><span data-stu-id="ba6da-201">Go to Zones.</span></span>
2. <span data-ttu-id="ba6da-202">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-202">Click New.</span></span>
3. <span data-ttu-id="ba6da-203">Bölge numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="ba6da-204">Bölge adı alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="ba6da-205">Bölge grubu numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ba6da-206">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ba6da-207">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ba6da-208">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="ba6da-209">Konum Kurulum Sihirbazı'nı kullanarak konumlar oluşturun</span><span class="sxs-lookup"><span data-stu-id="ba6da-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="ba6da-210">Konum kurulum sihirbazına gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="ba6da-211">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="ba6da-212">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ba6da-213">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ba6da-214">Bölge numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ba6da-215">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ba6da-216">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ba6da-217">Konum profil numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ba6da-218">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ba6da-219">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="ba6da-220">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="ba6da-221">Gönderen numarası alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="ba6da-222">Gönderen numarası ve Alıcı numarası alanları kaç adet konum oluşturulacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="ba6da-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="ba6da-223">Örneğin, gönderen numarası olarak 1 ve Alıcı numarası olarak 3 girerseniz, konum biçiminde tüm dört satır için 81 konum (3x3x3x3) oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ba6da-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="ba6da-224">Alıcı numarası alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="ba6da-225">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ba6da-226">Gönderen numarası alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="ba6da-227">Alıcı numarası alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="ba6da-228">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="ba6da-229">Gönderen numarası alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="ba6da-230">Alıcı numarası alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="ba6da-231">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="ba6da-232">Gönderen numarası alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="ba6da-233">Alıcı numarası alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="ba6da-234">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="ba6da-235">Konumları el ile oluştur</span><span class="sxs-lookup"><span data-stu-id="ba6da-235">Create locations manually</span></span>
1. <span data-ttu-id="ba6da-236">Konumlara gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-236">Go to Locations.</span></span>
    * <span data-ttu-id="ba6da-237">Ambar içinde konumların el ile oluşturulması kolaylıkla yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="ba6da-238">Konum adı ve konum profil kimliği zorunlu değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="ba6da-239">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-239">Click New.</span></span>
3. <span data-ttu-id="ba6da-240">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="ba6da-241">Yerleşim alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="ba6da-242">Burada yeni bir konum yarattığınızı ve bu yüzden mevcut bir tanesini kullanmak yerine, yeni ve benzersiz bir isim yazmanız gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="ba6da-243">Konum profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="ba6da-244">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="ba6da-245">Ambalaj boyutu kategorilerini tanımla</span><span class="sxs-lookup"><span data-stu-id="ba6da-245">Define Pack size categories</span></span>
1. <span data-ttu-id="ba6da-246">Paket boyutu kategorilerine gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="ba6da-247">Ambalaj boyutu kategorileri, fiziki olarak benzer ambalaj boyutlarına öğeleri gruplandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ba6da-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="ba6da-248">Bu örnekte, ambalaj boyutu kategorisi, ambarın belirli bir bölümündeki çekme konumlarının kapasitesini denetlemekte kullanılacak.</span><span class="sxs-lookup"><span data-stu-id="ba6da-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="ba6da-249">Lütfen ambalaj boyut kategori kimliğinin stoklamanın bir parçası olarak kullanılabilmesi için serbest bırakılan ürünün varlığının stoklama limitlerinin işlenmesi için atanması gerektiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="ba6da-250">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-250">Click New.</span></span>
3. <span data-ttu-id="ba6da-251">Paket boyutu kategori numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="ba6da-252">Paket boyutu kategori ismi alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="ba6da-253">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="ba6da-254">Konum stoklama sınırlarını tanımla</span><span class="sxs-lookup"><span data-stu-id="ba6da-254">Define location stocking limits</span></span>
1. <span data-ttu-id="ba6da-255">Konum stoklama sınırlarına gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="ba6da-256">Konum stoklama limitleri, stok miktarını taşıyacak fiziksel kapasitenin mevcut olmadığı konumlara yerleştirilmesini talep edecek işlerin oluşturulmasının önüne geçmeye yardımcı olmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ba6da-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="ba6da-257">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-257">Click New.</span></span>
3. <span data-ttu-id="ba6da-258">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="ba6da-259">Konum profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="ba6da-260">Paket boyutu kategori numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="ba6da-261">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="ba6da-262">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-262">Click Save.</span></span>
8. <span data-ttu-id="ba6da-263">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="ba6da-264">Sabit Malzeme çekme konumlarını tanımla</span><span class="sxs-lookup"><span data-stu-id="ba6da-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="ba6da-265">Sabit yerleşimlere gidin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="ba6da-266">Ürün veya ürün varyantı başına kullanılacak konumlarını tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ba6da-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="ba6da-267">Aynı ambar içinde aynı ürün için birden fazla sabit konum oluşturmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="ba6da-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="ba6da-268">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-268">Click New.</span></span>
3. <span data-ttu-id="ba6da-269">Madde numarası alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="ba6da-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="ba6da-270">Ambar alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="ba6da-271">Yerleşim alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ba6da-272">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ba6da-273">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ba6da-273">Close the page.</span></span>

