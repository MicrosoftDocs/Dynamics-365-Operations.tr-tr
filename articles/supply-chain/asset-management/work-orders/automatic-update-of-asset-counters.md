---
title: Kıymet sayaçlarını otomatik olarak güncelleştirme
description: Bu konuda, Varlık Yönetiminde varlık sayaçlarının otomatik olarak güncelleştirilmesi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875952"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="53557-103">Kıymet sayaçlarını otomatik olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="53557-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="53557-104">Önceki bölümde, varlık sayaçlarının el ile kaydı açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="53557-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="53557-105">Varlık sayaçları kurulumu [Sayaçlar](../setup-for-objects/counters.md) bölümünde açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="53557-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="53557-106">Sayaç değerleri, üretim saetleri veya üretim miktarına göre üretim kayıtlarından da otomatik olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="53557-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="53557-107">Bu işlem, **Varlık sayaçlarını güncelleştir**'de gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="53557-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="53557-108">Bir veya daha fazla varlığı **Başlangıç tarihi** parametresi ekleyerek güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53557-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="53557-109">Bu parametre, üretim kayıtları (saat veya üretilen miktar) için başlangıç tarihini belirtir; bu, sayaç değerlerinin güncelleştirilmesi gereken başlangıç tarihidir.</span><span class="sxs-lookup"><span data-stu-id="53557-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="53557-110">Bir kaynakla ilişkili olan *ve* üretilen miktara veya üretim saatlerine göre güncelleştirilmek üzere ayarlanan varlık sayaçları bulunan tüm varlıklar otomatik güncelleştirmeye dahil edilir ve yeni sayaç değerleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="53557-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="53557-111">Üretim miktarına dayalı sayaçlarla ilgili olarak, ürün miktarının yanı sıra kaydedilen hata miktarı da sayımına dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="53557-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="53557-112">Üretilen miktar kaydı için kullanılan birim sayaçta kullanılan birimden farklıysa miktar, sayaç birimine karşılık gelecek şekilde dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="53557-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="53557-113">Yukarıda belirtildiği gibi, otomatik sayaçlar üretim kayıtlarından güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="53557-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="53557-114">Bu nedenle, sayaçlarını otomatik olarak güncelleştirmek istediğiniz varlık bir kaynakla (makine) ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="53557-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="53557-115">Aşağıdaki açıklamalar, **Varlık yönetimi** modülündeki bir varlıkla ilgili sayaçların otomatik güncelleştirilmesi için temel olarak kullanılan üretim emirlerinin kurulumu ve işlenmesi (**Üretim denetimi** modülünde) ile ilgili genel bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="53557-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="53557-116">Üretilen miktarlar veya üretim saatleri kaynağa kaydedildiğinde, ilgili varlık sayaçlarını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53557-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="53557-117">**Varlık yönetimi** > **Periyodik** > **Varlıklar** > **Varlık sayaçlarını güncelleştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53557-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="53557-118">**Başlangıç tarihi** alanında otomatik güncelleştirmenin başlangıç tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="53557-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="53557-119">Bu alandaki tarih, **Rota hareketlerinden** gelen "süren iş" tarihidir (**Üretim denetimi** > **Sorgular ve raporlar** > **Üretim** > **Rota hareketleri** > **Fiziksel tarih** alanı).</span><span class="sxs-lookup"><span data-stu-id="53557-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="53557-120">Otomatik güncelleştirme için belirli varlıkları, varlık türlerini veya kaynakları seçmek isterseniz **Eklenecek kayıtlar** hızlı sekmesinde **Filtre**'ye tıklayın ve ilgili seçimleri yapın.</span><span class="sxs-lookup"><span data-stu-id="53557-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="53557-121">Gerekirse, **Arka planda çalıştır** hızlı sekmesinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53557-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Şekil 1](media/12-work-orders.png)

5. <span data-ttu-id="53557-123">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53557-123">Click **OK**.</span></span> <span data-ttu-id="53557-124">Otomatik varlık sayacı tamamlandığında, varlıkla ilgili sayaç kayıtlarını **Varlık sayaçları**'nda görebilirsiniz (**Varlık yönetimi** > **Genel** > **Varlılklar** > **Tüm varlıklar** > varlık seçin > **Sayaçlar** düğmesi).</span><span class="sxs-lookup"><span data-stu-id="53557-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="53557-125">**Varlık sayacı toplamları**'nda tüm varlıklardaki tüm sayaç türlerinde yapılmış en son kaydın genel görünümünü alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53557-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="53557-126">**Varlık Yönetimi** > **Sorgular** > **Varlıklar** > **Varlık toplam değeri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="53557-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="53557-127">Bu, **Varlık sayaçları**'na çok benzer ancak **Varlık toplam değeri**'nde kayıtları ekleyemez veya düzenleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="53557-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="53557-128">Yalnızca genel bakış içindir.</span><span class="sxs-lookup"><span data-stu-id="53557-128">It is for overview only.</span></span>

![Şekil 2](media/13-work-orders.png)


- <span data-ttu-id="53557-130">Otomatik olarak güncelleştirilen sayaç türleri için el ile sayaç değeri kayıtları oluşturmak da mümkündür.</span><span class="sxs-lookup"><span data-stu-id="53557-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="53557-131">Daha fazla bilgi için "Varlık sayaçlarını el ile güncelleştirme" bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="53557-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="53557-132">Başka bir sayaçla ilişkili sayaçlar ayarlayabilirsiniz. Bu, bir sayaç güncelleştirildiğinde ilgili sayaçların da aynı anda otomatik olarak güncelleştirileceği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="53557-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="53557-133">İlgili sayaçların kurulumuyla ilgili olarak [Sayaçlar](../setup-for-objects/counters.md) bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="53557-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
