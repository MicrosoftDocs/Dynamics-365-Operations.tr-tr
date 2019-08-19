---
title: Varlık ölçüleri
description: Bu konuda Kıymet Yönetimi'nde varlık ölçüsü oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783665"
---
# <a name="asset-measures"></a><span data-ttu-id="ac9c4-103">Varlık ölçüleri</span><span class="sxs-lookup"><span data-stu-id="ac9c4-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ac9c4-104">Bu konuda Kıymet Yönetimi'nde varlık ölçüsü oluşturma işlemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="ac9c4-105">Varlık ölçü birimi türleri, varlıklar üzerinde üretim saatleri sayısı veya varlık üzerinde üretilen miktar gibi ölçüm kayıtları yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="ac9c4-106">Varlık türleri varlık ölçü birimi türleriyle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="ac9c4-107">Bu, varlık ölçümünün bir varlık üzerinde yalnızca varlık üzerinde kullanılan kıymet türünde varlık ölçüsü ayarlanmış olması durumunda kullanılabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="ac9c4-108">Varlıklar üzerinde ölçüm kayıtları yapmadan önce, **Sayaçlar**'da kullanmak istediğiniz varlık ölçüsü türlerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="ac9c4-109">Ardından, **Varlık ölçüleri**'nden varlıklar üzerinde ölçüm kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="ac9c4-110">Varlık ölçüleri bakım planlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="ac9c4-111">Bir bakım planı satırı, örneğin üretim saatlerinin veya üretilen miktarın sayısıyla ilgili olarak "Sayaç" türünde olabilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="ac9c4-112">Bir varlık ölçüm kaydı el ile veya üretim saatlerine veya üretilen miktara göre otomatik olarak güncellenebilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="ac9c4-113">Varlık ölçüsü, üç güncelleştirme yönteminden birini kullanacak şekilde ayarlanabilir (**Sayaçlar**'ın **Güncelleştir** alanında seçilir):</span><span class="sxs-lookup"><span data-stu-id="ac9c4-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="ac9c4-114">El ile: Varlık ölçüm değerlerini el ile kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="ac9c4-115">Üretim saatleri: Sayaç, üretim saatlerinin sayısına göre otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="ac9c4-116">Üretim miktarı: Sayaç, üretilen miktarın sayısına göre otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="ac9c4-117">Üretilen miktar kullanılırsa, sağlam miktar ve hatalı miktar dahil *tüm* kayıtlı maddeler ölçüm kaydına eklenir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="ac9c4-118">Gerekirse, el ile varlık ölçüm kayıtları yapmak her zaman mümkündür.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="ac9c4-119">Varlık sayacı kayıtları için sayaç türleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="ac9c4-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="ac9c4-120">**Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="ac9c4-121">Yeni bir varlık ölçüsü türü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="ac9c4-122">**Sayaç** alanına bir kimlik ve **Ad** alanına bir sayaç adı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="ac9c4-123">**Genel** hızlı sekmesinde, **Birim** alanından bir ölçüm birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="ac9c4-124">**Güncelleştirme** alanında, varlık ölçüsü için kullanılacak güncelleştirme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="ac9c4-125">Bir varlık yapısındaki alt varlıkların otomatik olarak üst varlıkta yapılan varlık ölçüsü kayıtlarını devralması gerekiyorsa **Sayaç verilerini devral** düğmesini "Evet"e getirin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="ac9c4-126">**Toplama toplamı** alanında, bu varlık ölçü birimi türünü kullanan bir varlık ölçüsü için kullanılacak toplama yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="ac9c4-127">"Toplam", toplam değere kayıtlı değerleri sürekli olarak eklemek için kullanılan standart seçimdir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="ac9c4-128">Bir varlık ölçüsü, örneğin varlıktaki sıcaklık, titreşim veya aşınmayla ilgili olarak bir eşik izlemek için ayarlanmışsa, "Ortalama" kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="ac9c4-129">**Yukarı yönlü sapma** alanına, el ile yapılan varlık ölçü kayıtlarının beklenen aralıkta olduğunu doğrulamak için üst düzey yüzde değeri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="ac9c4-130">Doğrulama, varolan varlık ölçü birimi kayıtlarındaki doğrusal artışı temel alır.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="ac9c4-131">**Aşağı yönlü sapma** alanına, el ile yapılan varlık ölçü kayıtlarının beklenen aralıkta olduğunu doğrulamak için daha alt düzey yüzde değeri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="ac9c4-132">Doğrulama, varolan varlık ölçü birimi kayıtlarındaki doğrusal düşüşü temel alır.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="ac9c4-133">**Tür** alanında, el ile varlık ölçü kayıtları yaptığınızda tanımlanan aralığın dışındaki sapmalar oluşursa gösterilecek ileti türünü (bilgi, uyarı, hata) seçin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="ac9c4-134">**Varlık türleri** hızlı sekmesinden varlık ölçüsünü kullanabilmesi gereken varlık türlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="ac9c4-135">**İlgili varlık ölçüleri** hızlı sekmesinde, bu varlık ölçüsü güncelleştirildiğinde otomatik olarak güncelleştirilmesini istediğiniz varlık ölçülerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="ac9c4-136">İlgili varlık ölçüsü, yalnızca ilgili varlık ölçüsü, varlık ölçüsü kurulumunda ilişkili olduğu varlık türüne sahipse, ilgili varlık ölçüsü otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="ac9c4-137">Örneğin: "Üretim saatleri" için bir varlık ölçüsü ayarlayın ve "Kamyon Motoru" varlık türünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="ac9c4-138">Bu varlık ölçümü güncelleştirildiğinde, ilgili bir sayaç olan "Petrol" aynı varlık ölçüsü değerleri ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="ac9c4-139">**Sayaçlar**'daki kurulum "Saat" kurulumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="ac9c4-140">Ayrıca, "Petrol" varlık ölçüsünde, "Kamyon Motoru" varlık türü varlık ölçü ilişkisini sağlamak amacıyla **Varlık türleri** hızlı sekmesine eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="ac9c4-141">Saat ve Petrol varlık ölçüleri kurulumu örneği için aşağıdaki ekran görüntülerine bakın.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="ac9c4-142">Varlık türleri **Sayaçlar**'daki bir varlık ölçüsü türüne eklendiğinde bu varlık ölçüsü otomatik olarak  [Varlık türleri](../setup-for-objects/object-types.md)'ndeki **Sayaçlar** hızlı sekmesinde bulunan varlık türlerine eklenir.</span><span class="sxs-lookup"><span data-stu-id="ac9c4-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Şekil 1](media/071-setup-for-objects.png)


