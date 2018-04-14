--- 
title: "Taşıyıcılı bir yakıt dizinini ilave masraf olarak ilişkilendirme"
description: "Bu kılavuz ilave atama, taşıyıcı ek giderleri, yakıt ek giderleri için ana ilaveler şablonu oluşturmayı ve taşıyıcı yakıt dizinini bir taşıyıcı ile nasıl ilişkilendirileceğini gösterir."
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
ms.openlocfilehash: 101ebe4a2e177a5702a162297e1820598e56a6e5
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="c61fb-103">Taşıyıcılı bir yakıt dizinini ilave masraf olarak ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="c61fb-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c61fb-104">Bu kılavuz ilave atama, taşıyıcı ek giderleri, yakıt ek giderleri için ana ilaveler şablonu oluşturmayı ve taşıyıcı yakıt dizinini bir taşıyıcı ile nasıl ilişkilendirileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c61fb-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="c61fb-105">Bu kılavuzu çalıştırmadan önce bir taşıyıcı yakıt dizini ayarlamış olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c61fb-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="c61fb-106">Bunu yapmak için "Taşıyıcı yakıt dizini kurma" kılavuzunu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c61fb-106">You can use the “Set up a carrier fuel index” guide to do this.</span></span> <span data-ttu-id="c61fb-107">Bu kurulum görevleri genellikle Lojistik Yöneticisi tarafından yapılır.</span><span class="sxs-lookup"><span data-stu-id="c61fb-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="c61fb-108">Bu yöntemi oluşturmak için kullanılan demo verisi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="c61fb-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="c61fb-109">Bir ana ilave oluştur</span><span class="sxs-lookup"><span data-stu-id="c61fb-109">Create an accessorial master</span></span>
1. <span data-ttu-id="c61fb-110">Taşıma yönetimi > Kurulum > Derecelendirme > Ana ilaveler öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="c61fb-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-111">Click New.</span></span>
3. <span data-ttu-id="c61fb-112">Ana ilaveler alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="c61fb-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c61fb-114">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="c61fb-115">Taşıyıcı ilave masrafı oluşturun</span><span class="sxs-lookup"><span data-stu-id="c61fb-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="c61fb-116">Taşıma yönetimi > Kurulum > Derecelendirme > Taşıyıcı ilave masrafları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="c61fb-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-117">Click New.</span></span>
3. <span data-ttu-id="c61fb-118">Taşıyıcı ilave numarası alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="c61fb-119">Sevkiyat taşıyıcısı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c61fb-120">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c61fb-121">Bu örnekte, Kamyon Taşıyıcısı'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="c61fb-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c61fb-123">Taşıyıcı hizmeti alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c61fb-124">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c61fb-125">Ana ilaveler alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c61fb-126">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c61fb-127">Bu örnekte, yeni oluşturulan Ana ilaveler'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="c61fb-128">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="c61fb-129">Bir ilave atama oluşturun</span><span class="sxs-lookup"><span data-stu-id="c61fb-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="c61fb-130">İlave atamaları'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="c61fb-131">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-131">Click New.</span></span>
3. <span data-ttu-id="c61fb-132">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c61fb-133">Ölçütler bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="c61fb-134">Kriterde, her zaman yakıt ek giderlerini uygulamayı veya bu örnek için sadece belirli bir bölge içerisinde uygulanacağını seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c61fb-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="c61fb-135">Posta kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="c61fb-136">Giden posta kodu alanında bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="c61fb-137">Hesaplama bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="c61fb-138">Hesaplama bölümünde yakıt ek giderlerini hesaplama yöntemini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c61fb-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="c61fb-139">Bu hesaplama, hesaplamanız için temel olarak seçtiğiniz ek birime bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="c61fb-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="c61fb-140">İlave ücret türü alanında 'Yakıt gideri' seçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="c61fb-141">İlave birim alanında 'Mesafe' seçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="c61fb-142">Bölge alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="c61fb-143">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c61fb-144">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="c61fb-145">Taşıyıcısı değerlendirme profilini güncelleyin</span><span class="sxs-lookup"><span data-stu-id="c61fb-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="c61fb-146">Taşımacılık Yönetimi > Kurulum > Taşıyıcılar > Seviyat taşıyıcıları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="c61fb-147">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c61fb-148">Değerlendirme profilleri bölümünün genişletilmiş görünümüne geçin.</span><span class="sxs-lookup"><span data-stu-id="c61fb-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="c61fb-149">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-149">Click Edit.</span></span>
5. <span data-ttu-id="c61fb-150">Taşıyıcı yakıt dizini alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c61fb-151">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c61fb-152">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c61fb-152">Click Save.</span></span>


