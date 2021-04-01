---
title: Varlık kritiklik türleri
description: Bu konuda Varlık Yönetiminde varlık kritiklik türleri açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetCriticality, EntAssetObjectCriticality
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c771e7ebda94687ab5442347e74c82b01ad2fcc6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245431"
---
# <a name="asset-criticality-types"></a><span data-ttu-id="a6e9e-103">Varlık kritiklik türleri</span><span class="sxs-lookup"><span data-stu-id="a6e9e-103">Asset criticality types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a6e9e-104">Bu konuda Varlık Yönetiminde varlık kritiklik türleri açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-104">The topic explains asset criticality types in Asset Management.</span></span> <span data-ttu-id="a6e9e-105">Varlık kritikliği varlıklarla ilişkilidir ve iş emirlerine aktarılır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-105">Asset criticality is related to assets and is transferred to work orders.</span></span> <span data-ttu-id="a6e9e-106">İş emri üzerinde değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-106">It can't be changed on a work order.</span></span> <span data-ttu-id="a6e9e-107">Varlık kritikliği iş emri planlaması sırasında iş emri kritikliğini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-107">Asset criticality is used to calculate work order criticality during work order scheduling.</span></span> <span data-ttu-id="a6e9e-108">Başka bir deyişle, bir varlıktaki bakım işinin şirketinizin üretim zamanlamasını ve üretkenliğini nasıl etkilediğini hesaplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-108">In other words, it's used to calculate the extent to which a maintenance job on an asset affects the production schedule and productivity in your company.</span></span> <span data-ttu-id="a6e9e-109">İş emri planlaması için derecelendirme puanlarının hesaplanmasıyla ilgili kurulum hakkında daha fazla bilgi için bkz. [Varlık Yönetimi parametreleri](../setup-for-objects/enterprise-asset-management-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a6e9e-109">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span>

<span data-ttu-id="a6e9e-110">Kritikliği ayarlamak için önce varlık kurulumunda kullanılması gereken kritiklik türlerini oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-110">To set up criticality, you first create the criticality types that should be used in the asset setup.</span></span> <span data-ttu-id="a6e9e-111">Daha sonra varlık kritikliklerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-111">You then set up asset criticalities.</span></span>

## <a name="set-up-criticality-types"></a><span data-ttu-id="a6e9e-112">Kritiklik türlerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="a6e9e-112">Set up criticality types</span></span>

1. <span data-ttu-id="a6e9e-113">**Varlık yönetimi** \> **Kurulum** \> **Varlıklar** \> **Kritiklik türleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-113">Select **Asset management** \> **Setup** \> **Assets** \> **Criticality types**.</span></span>
2. <span data-ttu-id="a6e9e-114">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-114">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a6e9e-115">**Kritiklik** alanında, kritikliği gösteren bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-115">In the **Criticality** field, enter a number that indicates the criticality.</span></span>
4. <span data-ttu-id="a6e9e-116">**Ad** alanına kritiklik türü için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-116">In the **Name** field, enter a name for the criticality type.</span></span>
5. <span data-ttu-id="a6e9e-117">**Faktör** alanına bir faktör girin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-117">In the **Factor** field, enter a factor.</span></span> <span data-ttu-id="a6e9e-118">Bu faktör, kullanılması gereken kritiklik kaydını belirlemek için iş emri planlaması hesaplaması sırasında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-118">This factor is used during the calculation of work order scheduling to determine the criticality record that should be used.</span></span> <span data-ttu-id="a6e9e-119">(En yüksek faktörüne sahip kayıt her zaman kullanılır.) Bu ayar, aşağıdaki örnekte gösterildiği gibi, aynı kritiklik değerine sahip olan kritiklik satırları oluşturulmuşsa geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-119">(The record that has the highest factor is always used.) This setting is relevant if, as shown in the following illustration, criticality lines are created that have the same criticality value.</span></span>

    ![Kritiklik türleri sayfası](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a><span data-ttu-id="a6e9e-121">Varlıkla kritiklikleri ayarlama</span><span class="sxs-lookup"><span data-stu-id="a6e9e-121">Set up asset criticalities</span></span>

1. <span data-ttu-id="a6e9e-122">**Varlık yönetimi** \> **Kurulum** \> **Varlık kritiklikleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-122">Select **Asset management** \> **Setup** \> **Asset criticalities**.</span></span>
2. <span data-ttu-id="a6e9e-123">Bir kayıt oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-123">Select **New** to create a record.</span></span>
3. <span data-ttu-id="a6e9e-124">Varlık kritikliği için gerekli olan ayrıntı düzeyine bağlı olarak **İşlem yapılacak yerleşim**, **Varlık türü**, **Üretici**, **Model**, **Varlık**, **İş türü kategorisi**, **İş türü**, **İş türü değişkeni** ve **İş gereksinimi** alanlarında ilgili seçimleri yapın.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-124">Depending on the required level of detail for asset criticality, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a6e9e-125">Bir varlık kritikliği seçildiğinde, Varlık Yönetimi olası bir eşleşme olup olmadığını kontrol etmek için tüm varlık kritiklik kayıtlarına bakar.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-125">When an asset criticality is selected, Asset Management goes through all asset criticality records to check for a possible match.</span></span> <span data-ttu-id="a6e9e-126">Her zaman ilk önce en belirgin birleşimi denetler.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-126">It always checks the most specific combination first.</span></span> <span data-ttu-id="a6e9e-127">Diğer bir deyişle, Varlık Yönetimi önce **İş gereksinimi**'ni kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-127">In other words, Asset Management first checks **Job requirement**.</span></span> <span data-ttu-id="a6e9e-128">Eşleşme bulunmazsa, **İş türü değişkeni**'ni kontrol eder.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-128">If no match is found, it checks **Job type variant**.</span></span> <span data-ttu-id="a6e9e-129">Eşleşme bulunmazsa, **İş türü**'nü kontrol eder ve bu şekilde devam eder.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-129">If no match is found, it checks **Job type**, and so on.</span></span> <span data-ttu-id="a6e9e-130">Sayfa düzeninde gördüğünüz gibi bu davranış en özel birleşimi bulmak için Varlık Yönetimi'nin eşleşme için sağdan sola her kaydı denetlediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-130">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="a6e9e-131">Eşleşme bulunmazsa, hiçbir seçimi olmayan "varsayılan" kayıt kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-131">If no match is found, the "default" record that has no selections is used.</span></span>

4. <span data-ttu-id="a6e9e-132">**Kritiklik** alanında, önceki yordamda oluşturduğunuz kritiklik değerlerinden birini seçin.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-132">In the **Criticality** field, select one of the criticality values that you created in the previous procedure.</span></span>

### <a name="notes-about-criticality-setup"></a><span data-ttu-id="a6e9e-133">Kritiklik kurulumu hakkında notlar</span><span class="sxs-lookup"><span data-stu-id="a6e9e-133">Notes about criticality setup</span></span>

- <span data-ttu-id="a6e9e-134">Bir iş emri üzerinde kullandıktan sonra bu kurulumdaki bir varlık kritikliğini değiştirirseniz, iş emrindeki kritiklik buna göre güncelleştirilmez.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-134">If you change an asset criticality in this setup after you've already used it on a work order, the criticality on the work order isn't updated accordingly.</span></span>
- <span data-ttu-id="a6e9e-135">İş emrindeki kritiklik, iş emrine bir iş emri satırı eklendiğinde veya silindiğinde yeniden hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-135">The criticality on a work order is recalculated every time that a work order line is added to or deleted from the work order.</span></span>
- <span data-ttu-id="a6e9e-136">İş emri birkaç iş emri işi içeriyorsa, daima **Kritiklik türleri** sayfasındaki **Faktör** alanına göre en yüksek kritiklik, iş emri üzerinde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-136">If a work order contains several work order jobs, the highest criticality, according to the **Factor** field on the **Criticality types** page, is always used on the work order.</span></span>
- <span data-ttu-id="a6e9e-137">Genellikle, varlık kritikliği zaman içinde değişebilir.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-137">Generally, asset criticality can change over a period.</span></span> <span data-ttu-id="a6e9e-138">Kritiklik yeni ekipman satın alma, yenilemeler gibi durumlardan etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-138">Criticality can be affected by the purchase of new equipment, refurbishments, and so on.</span></span> <span data-ttu-id="a6e9e-139">Kritiklik tanımlarınızın geçerli üretim kurulumunuz ile eşleştiğinden emin olmak için varlık kritikliklerini düzenli aralıklarla (örneğin, yılda bir veya her iki yılda bir) yeniden değerlendirmeyi düşünün.</span><span class="sxs-lookup"><span data-stu-id="a6e9e-139">Consider reevaluating your asset criticalities at regular intervals (for example, once per year or every other year) to make sure that your criticality definitions match your current production setup.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]