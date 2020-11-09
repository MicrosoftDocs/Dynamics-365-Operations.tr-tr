---
title: Taşıyıcılı bir yakıt dizinini ilave masraf olarak ilişkilendirme
description: Bu kılavuz ilave atama, taşıyıcı ek giderleri, yakıt ek giderleri için ana ilaveler şablonu oluşturmayı ve taşıyıcı yakıt dizinini bir taşıyıcı ile nasıl ilişkilendirileceğini gösterir.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c91d49c2ccdc274632e3acf94b836e19dc6cdaa8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017012"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="d04d7-103">Taşıyıcılı bir yakıt dizinini ilave masraf olarak ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="d04d7-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d04d7-104">Bu kılavuz ilave atama, taşıyıcı ek giderleri, yakıt ek giderleri için ana ilaveler şablonu oluşturmayı ve taşıyıcı yakıt dizinini bir taşıyıcı ile nasıl ilişkilendirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d04d7-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="d04d7-105">Bu kılavuzu çalıştırmadan önce bir taşıyıcı yakıt dizini ayarlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d04d7-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="d04d7-106">Bunu yapmak için "Taşıyıcı yakıt dizini kurma" kılavuzunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d04d7-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="d04d7-107">Bu kurulum görevleri genellikle Lojistik Yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="d04d7-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="d04d7-108">Bu yöntemi oluşturmak için kullanılan demo verisi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="d04d7-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="d04d7-109">Bir ana ilave oluştur</span><span class="sxs-lookup"><span data-stu-id="d04d7-109">Create an accessorial master</span></span>
1. <span data-ttu-id="d04d7-110">Taşıma yönetimi > Kurulum > Derecelendirme > Ana ilaveler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="d04d7-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-111">Click New.</span></span>
3. <span data-ttu-id="d04d7-112">Ana ilaveler alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="d04d7-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d04d7-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="d04d7-115">Taşıyıcı ilave masrafı oluşturun</span><span class="sxs-lookup"><span data-stu-id="d04d7-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="d04d7-116">Taşıma yönetimi > Kurulum > Derecelendirme > Taşıyıcı ilave masrafları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="d04d7-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-117">Click New.</span></span>
3. <span data-ttu-id="d04d7-118">Taşıyıcı ilave numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="d04d7-119">Sevkiyat taşıyıcısı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d04d7-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d04d7-121">Bu örnekte, Kamyon Taşıyıcısı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="d04d7-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d04d7-123">Taşıyıcı hizmeti alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d04d7-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d04d7-125">Ana ilaveler alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="d04d7-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d04d7-127">Bu örnekte, yeni oluşturulan Ana ilaveler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="d04d7-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="d04d7-129">Bir ilave atama oluşturun</span><span class="sxs-lookup"><span data-stu-id="d04d7-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="d04d7-130">İlave atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="d04d7-131">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-131">Click New.</span></span>
3. <span data-ttu-id="d04d7-132">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d04d7-133">Ölçütler bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="d04d7-134">Kriterde, her zaman yakıt ek giderlerini uygulamayı veya bu örnek için sadece belirli bir bölge içerisinde uygulanacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d04d7-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="d04d7-135">Posta kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="d04d7-136">Giden posta kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="d04d7-137">Hesaplama bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="d04d7-138">Hesaplama bölümünde yakıt ek giderlerini hesaplama yöntemini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d04d7-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="d04d7-139">Bu hesaplama, hesaplamanız için temel olarak seçtiğiniz ek birime bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d04d7-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="d04d7-140">İlave ücret türü alanında 'Yakıt gideri' seçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="d04d7-141">İlave birim alanında 'Mesafe' seçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="d04d7-142">Bölge alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d04d7-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d04d7-144">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="d04d7-145">Taşıyıcısı değerlendirme profilini güncelleyin</span><span class="sxs-lookup"><span data-stu-id="d04d7-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="d04d7-146">Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="d04d7-147">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="d04d7-148">Değerlendirme profilleri bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="d04d7-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="d04d7-149">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-149">Click Edit.</span></span>
5. <span data-ttu-id="d04d7-150">Taşıyıcı yakıt dizini alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d04d7-151">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d04d7-152">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d04d7-152">Click Save.</span></span>

