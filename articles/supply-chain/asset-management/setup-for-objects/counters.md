---
title: Varlık ölçüleri
description: Bu konuda Kıymet Yönetimi'nde varlık ölçüsü oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889781"
---
# <a name="counters"></a><span data-ttu-id="acec9-103">Sayaçlar</span><span class="sxs-lookup"><span data-stu-id="acec9-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="acec9-104">Bu konuda Varlık Yönetimi'nde sayaç türleri oluşturma işlemi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="acec9-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="acec9-105">Sayaç türleri, varlıklar üzerinde üretim saatleri sayısı veya varlık üzerinde üretilen miktar gibi sayaç kayıtları yapmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="acec9-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="acec9-106">Sayaç türleri varlık ölçü birimi türleriyle ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="acec9-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="acec9-107">Bu, sayacın bir varlık üzerinde yalnızca varlık üzerinde kullanılan varlık türünde sayaç ayarlanmış olması durumunda kullanılabileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="acec9-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="acec9-108">Varlıklar üzerinde sayaç kayıtları yapmadan önce, **Sayaçlar**'da kullanmak istediğiniz sayaç türlerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="acec9-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="acec9-109">Ardından, **Sayaçlar**'dan varlıklar üzerinde sayaç kayıtları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="acec9-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="acec9-110">Sayaçlar bakım planlarında kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="acec9-111">Bir bakım planı satırı, örneğin üretim saatlerinin veya üretilen miktarın sayısıyla ilgili olarak "Sayaç" türünde olabilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="acec9-112">Bir sayaç kaydı el ile veya üretim saatlerine veya üretilen miktara göre otomatik olarak güncellenebilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="acec9-113">Sayaç, üç güncelleştirme yönteminden birini kullanacak şekilde ayarlanabilir (**Sayaçlar**'ın **Güncelleştir** alanında seçilir):</span><span class="sxs-lookup"><span data-stu-id="acec9-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="acec9-114">El ile: Sayaç değerlerini el ile kaydetmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="acec9-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="acec9-115">Üretim saatleri: Sayaç, üretim saatlerinin sayısına göre otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="acec9-116">Üretim miktarı: Sayaç, üretilen miktarın sayısına göre otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="acec9-117">Üretilen miktar kullanılırsa, sağlam miktar ve hatalı miktar dahil *tüm* kayıtlı maddeler sayaç kaydına eklenir.</span><span class="sxs-lookup"><span data-stu-id="acec9-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="acec9-118">Gerekirse, el ile varlık sayaç kayıtları yapmak her zaman mümkündür.</span><span class="sxs-lookup"><span data-stu-id="acec9-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="acec9-119">Varlık sayacı kayıtları için sayaç türleri oluşturma</span><span class="sxs-lookup"><span data-stu-id="acec9-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="acec9-120">**Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="acec9-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="acec9-121">Yeni bir sayaç türü oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="acec9-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="acec9-122">**Sayaç** alanına bir kimlik ve **Ad** alanına bir sayaç adı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="acec9-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="acec9-123">**Genel** hızlı sekmesinde, **Birim** alanından bir sayaç birimi seçin.</span><span class="sxs-lookup"><span data-stu-id="acec9-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="acec9-124">**Güncelleştirme** alanında, sayaç için kullanılacak güncelleştirme yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="acec9-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="acec9-125">Bir varlık yapısındaki alt varlıkların otomatik olarak üst varlıkta yapılan sayaç kayıtlarını devralması gerekiyorsa **Sayaç verilerini devral** düğmesini "Evet"e getirin.</span><span class="sxs-lookup"><span data-stu-id="acec9-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="acec9-126">**Toplama toplamı** alanında, bu sayaç türünü kullanan bir sayaç için kullanılacak toplama yöntemini seçin.</span><span class="sxs-lookup"><span data-stu-id="acec9-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="acec9-127">"Toplam", toplam değere kayıtlı değerleri sürekli olarak eklemek için kullanılan standart seçimdir.</span><span class="sxs-lookup"><span data-stu-id="acec9-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="acec9-128">Bir sayaç, örneğin varlıktaki sıcaklık, titreşim veya aşınmayla ilgili olarak bir eşik izlemek için ayarlanmışsa, "Ortalama" kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="acec9-129">**Yukarı yönlü sapma** alanına, el ile yapılan sayaç kayıtlarının beklenen aralıkta olduğunu doğrulamak için üst düzey yüzde değeri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="acec9-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="acec9-130">Doğrulama, varolan sayaç kayıtlarındaki doğrusal artışı temel alır.</span><span class="sxs-lookup"><span data-stu-id="acec9-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="acec9-131">**Aşağı yönlü sapma** alanına, el ile yapılan sayaç kayıtlarının beklenen aralıkta olduğunu doğrulamak için alt düzey yüzde değeri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="acec9-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="acec9-132">Doğrulama, varolan sayaç kayıtlarındaki doğrusal azalışı temel alır.</span><span class="sxs-lookup"><span data-stu-id="acec9-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="acec9-133">**Tür** alanında, el ile sayaç kayıtları yaptığınızda tanımlanan aralığın dışındaki sapmalar oluşursa gösterilecek ileti türünü (bilgi, uyarı, hata) seçin.</span><span class="sxs-lookup"><span data-stu-id="acec9-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="acec9-134">**Varlık türleri** hızlı sekmesinden sayacı kullanabilmesi gereken varlık türlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="acec9-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="acec9-135">**İlgili varlık sayaçları** hızlı sekmesinde, bu sayaç güncelleştirildiğinde otomatik olarak güncelleştirilmesini istediğiniz sayacı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="acec9-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="acec9-136">İlgili sayaç, yalnızca ilgili varlık ölçüsü, sayaç kurulumunda ilişkili olduğu varlık türüne sahipse, ilgili sayaç otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="acec9-137">Örneğin: "Üretim saatleri" için bir sayaç ayarlayın ve "Kamyon Motoru" varlık türünü ekleyin.</span><span class="sxs-lookup"><span data-stu-id="acec9-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="acec9-138">Bu sayaç güncelleştirildiğinde, ilgili bir sayaç olan "Petrol" aynı sayaç değerleri ile güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="acec9-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="acec9-139">**Sayaçlar**'daki kurulum "Saat" kurulumunu içerir.</span><span class="sxs-lookup"><span data-stu-id="acec9-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="acec9-140">Ayrıca, "Petrol" sayacında, "Kamyon Motoru" varlık türü sayaç ilişkisini sağlamak amacıyla **Varlık türleri** hızlı sekmesine eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="acec9-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="acec9-141">Saat ve Petrol sayaçları kurulumu örneği için aşağıdaki ekran görüntülerine bakın.</span><span class="sxs-lookup"><span data-stu-id="acec9-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="acec9-142">Varlık türleri **Sayaçlar**'daki bir sayaç türüne eklendiğinde bu sayaç otomatik olarak  [Varlık türleri](../setup-for-objects/object-types.md)'ndeki **Sayaçlar** hızlı sekmesinde bulunan varlık türlerine eklenir.</span><span class="sxs-lookup"><span data-stu-id="acec9-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Şekil 1](media/071-setup-for-objects.png)

