---
title: Sevkiyat taşıyıcılarını ayarlama
description: Bu konu, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 124f7473cbdae8890f74115d461603f50cc58be8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004889"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="24ed6-103">Sevkiyat taşıyıcılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="24ed6-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24ed6-104">Bu konu, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="24ed6-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="24ed6-105">Ulaşım Koordinatörü, daha sonra, gelen veya giden bir yük için Sevkiyat taşıyıcısı atayabilir.</span><span class="sxs-lookup"><span data-stu-id="24ed6-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="24ed6-106">Yeni bir Sevkiyat taşıyıcısı oluşturun</span><span class="sxs-lookup"><span data-stu-id="24ed6-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="24ed6-107">**Gezinti bölmesi > Modüller > Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin**.</span><span class="sxs-lookup"><span data-stu-id="24ed6-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="24ed6-108">Eylem Bölmesi'nde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="24ed6-109">**Sevkiyat taşıyıcıları** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="24ed6-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="24ed6-111">**Mod** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="24ed6-112">Sevkiyat taşıyıcısı için genel bilgileri doldurun</span><span class="sxs-lookup"><span data-stu-id="24ed6-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="24ed6-113">**Genel Bakış** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="24ed6-114">**Sevkiyat taşıyıcısını etkinleştir** onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="24ed6-115">**Satıcı hesabı** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="24ed6-116">Sevkiyat taşıyıcısının atanacağı satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="24ed6-117">**Taşıma ödemesi türü** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="24ed6-118">Taşıma ödemesi sayfasını kullanmak için **El ile**'yi seçin veya **EDI**'yi seçerek ödemeyi Elektronik Veri Değişimi (EDI) kullanarak güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="24ed6-119">**Taşıyıcı değerlendirmesini etkinleştir** onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="24ed6-120">Sevkiyat taşıyıcısı için gerekli hizmetleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="24ed6-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="24ed6-121">**Hizmetler** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="24ed6-122">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-122">Select **New**.</span></span>
3. <span data-ttu-id="24ed6-123">**Taşıyıcı hizmeti** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="24ed6-124">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="24ed6-125">**Taşıma yöntemi** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="24ed6-126">Taşıyıcı için adresi (isteğe bağlı) ayarlayın</span><span class="sxs-lookup"><span data-stu-id="24ed6-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="24ed6-127">**Adresler** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="24ed6-128">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-128">Select **New**.</span></span>
3. <span data-ttu-id="24ed6-129">**Ad veya açıklama** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="24ed6-130">**Ülke / bölge** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="24ed6-131">**Bitiş posta kodu** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="24ed6-132">**Cadde** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="24ed6-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="24ed6-134">Sevkiyat taşıyıcısı için derecelendirme profilini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="24ed6-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="24ed6-135">**Değerlendirme profilleri** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="24ed6-136">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-136">Select **New**.</span></span>
3. <span data-ttu-id="24ed6-137">**Değerlendirme profili** numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="24ed6-138">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="24ed6-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="24ed6-139">**Tesis** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="24ed6-140">**Ambar** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="24ed6-141">**Değerlendirme altyapısı** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="24ed6-142">Taşıyıcı ile aranızdaki sözleşmeye uyugn olacak Değerlendirme altyapısını seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="24ed6-143">**Ara oran** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="24ed6-144">**Yoldaki süre altyapısı** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="24ed6-145">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="24ed6-145">Select **Save**.</span></span>

