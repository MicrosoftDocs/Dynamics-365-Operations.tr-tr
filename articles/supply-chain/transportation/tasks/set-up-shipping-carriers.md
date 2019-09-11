---
title: Sevkiyat taşıyıcılarını ayarlama
description: Bu konu, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a43a99e10b915f1265be14f2442069dae3a22e5
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867039"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="8e67d-103">Sevkiyat taşıyıcılarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="8e67d-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e67d-104">Bu konu, bir Sevkiyat taşıyıcısı ayarlamayı ve hizmet, sevkiyat modu, taşıma ödemesi, taşıma kısıtlamaları ve sevkiyat oranı gibi ayrıntıları tanımlamayı gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e67d-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="8e67d-105">Ulaşım Koordinatörü, daha sonra, gelen veya giden bir yük için Sevkiyat taşıyıcısı atayabilir.</span><span class="sxs-lookup"><span data-stu-id="8e67d-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="8e67d-106">Yeni bir Sevkiyat taşıyıcısı oluşturun</span><span class="sxs-lookup"><span data-stu-id="8e67d-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="8e67d-107">**Gezinti bölmesi > Modüller > Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin**.</span><span class="sxs-lookup"><span data-stu-id="8e67d-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="8e67d-108">Eylem bölmesinde, **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="8e67d-109">**Sevkiyat taşıyıcıları** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="8e67d-110">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8e67d-111">**Mod** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="8e67d-112">Sevkiyat taşıyıcısı için genel bilgileri doldurun</span><span class="sxs-lookup"><span data-stu-id="8e67d-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="8e67d-113">**Genel Bakış** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="8e67d-114">**Sevkiyat taşıyıcısını etkinleştir** onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="8e67d-115">**Satıcı hesabı** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="8e67d-116">Sevkiyat taşıyıcısının atanacağı satıcı hesabını seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="8e67d-117">**Taşıma ödemesi türü** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="8e67d-118">Taşıma ödemesi sayfasını kullanmak için **El ile**'yi seçin veya **EDI**'yi seçerek ödemeyi Elektronik Veri Değişimi (EDI) kullanarak güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="8e67d-119">**Taşıyıcı değerlendirmesini etkinleştir** onay kutusunu işaretleyin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="8e67d-120">Sevkiyat taşıyıcısı için gerekli hizmetleri oluşturun</span><span class="sxs-lookup"><span data-stu-id="8e67d-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="8e67d-121">**Hizmetler** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="8e67d-122">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-122">Select **New**.</span></span>
3. <span data-ttu-id="8e67d-123">**Taşıyıcı hizmeti** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="8e67d-124">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8e67d-125">**Taşıma yöntemi** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="8e67d-126">Taşıyıcı için adresi (isteğe bağlı) ayarlayın</span><span class="sxs-lookup"><span data-stu-id="8e67d-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="8e67d-127">**Adresler** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="8e67d-128">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-128">Select **New**.</span></span>
3. <span data-ttu-id="8e67d-129">**Ad veya açıklama** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="8e67d-130">**Ülke / bölge** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="8e67d-131">**Bitiş posta kodu** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="8e67d-132">**Cadde** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="8e67d-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="8e67d-134">Sevkiyat taşıyıcısı için derecelendirme profilini ayarlayın</span><span class="sxs-lookup"><span data-stu-id="8e67d-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="8e67d-135">**Değerlendirme profilleri** bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="8e67d-136">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-136">Select **New**.</span></span>
3. <span data-ttu-id="8e67d-137">**Değerlendirme profili** numarası alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="8e67d-138">**Ad** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="8e67d-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="8e67d-139">**Tesis** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="8e67d-140">**Ambar** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="8e67d-141">**Değerlendirme altyapısı** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="8e67d-142">Taşıyıcı ile aranızdaki sözleşmeye uyugn olacak Değerlendirme altyapısını seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="8e67d-143">**Ara oran** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="8e67d-144">**Yoldaki süre altyapısı** alanında, açılır menüden bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="8e67d-145">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8e67d-145">Select **Save**.</span></span>

