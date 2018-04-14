--- 
title: "Sevk eden taşımacıları ayarlama"
description: "Bu yordam, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6e9ce934016139832b474d60d7dfc2e845434da2
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="af1a4-103">Sevk eden taşımacıları ayarlama</span><span class="sxs-lookup"><span data-stu-id="af1a4-103">Set up shipping carriers</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af1a4-104">Bu yordam, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="af1a4-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="af1a4-105">Ulaşım Koordinatörü, daha sonra, gelen veya giden bir yük için Sevkiyat taşıyıcısı atayabilir.</span><span class="sxs-lookup"><span data-stu-id="af1a4-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="af1a4-106">Yeni bir Sevkiyat taşıyıcısı oluşturun</span><span class="sxs-lookup"><span data-stu-id="af1a4-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="af1a4-107">Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="af1a4-108">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-108">Click New.</span></span>
3. <span data-ttu-id="af1a4-109">Sevkiyat taşıyıcıları alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="af1a4-110">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="af1a4-111">Mod alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="af1a4-112">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="af1a4-113">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="af1a4-114">Sevkiyat taşıyıcısı için genel bilgileri doldurun</span><span class="sxs-lookup"><span data-stu-id="af1a4-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="af1a4-115">Genel Bakış bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="af1a4-116">Sevkiyat taşıyıcısını etkinleştir onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="af1a4-117">Satıcı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="af1a4-118">Sevkiyat taşıyıcısının atanacağı satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="af1a4-119">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="af1a4-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="af1a4-121">Taşıma ödemesi tipi alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="af1a4-122">Taşıma ödemesi sayfasını kullanmak için El ile'yi seçin veya EDI'yi seçerek ödemeyi Elektronik Veri Değişimi (EDI) kullanarak güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="af1a4-123">Taşıyıcısını değerlendirmesini etkinleştir onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="af1a4-124">Sevkiyat taşıyıcısı için gerekli hizmetleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="af1a4-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="af1a4-125">Hizmetler bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="af1a4-126">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-126">Click New.</span></span>
3. <span data-ttu-id="af1a4-127">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="af1a4-128">Taşıyıcı hizmeti alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="af1a4-129">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="af1a4-130">Taşıma yöntemi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="af1a4-131">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="af1a4-132">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="af1a4-133">Taşıyıcı için adresi (isteğe bağlı) ayarlayın</span><span class="sxs-lookup"><span data-stu-id="af1a4-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="af1a4-134">Adres bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="af1a4-135">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-135">Click New.</span></span>
3. <span data-ttu-id="af1a4-136">Ad veya açıklama alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="af1a4-137">Ülke/bölge alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="af1a4-138">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="af1a4-139">Posta kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="af1a4-140">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="af1a4-141">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="af1a4-142">Cadde alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="af1a4-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="af1a4-144">Sevkiyat taşıyıcısı için derecelendirme profilini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="af1a4-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="af1a4-145">Değerlendirme profilleri bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="af1a4-146">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-146">Click New.</span></span>
3. <span data-ttu-id="af1a4-147">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="af1a4-148">Değerlendirme profili numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="af1a4-149">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="af1a4-150">Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="af1a4-151">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="af1a4-152">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="af1a4-153">Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="af1a4-154">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="af1a4-155">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="af1a4-156">Değerlendirme altyapısı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="af1a4-157">Taşıyıcı ile aranızdaki sözleşmeye uyugn olacak Değerlendirme altyapısını seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="af1a4-158">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="af1a4-159">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="af1a4-160">Ana oran alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="af1a4-161">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="af1a4-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="af1a4-162">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="af1a4-163">Taşıma süresi altyapıları alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="af1a4-164">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="af1a4-165">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="af1a4-165">Click Save.</span></span>


