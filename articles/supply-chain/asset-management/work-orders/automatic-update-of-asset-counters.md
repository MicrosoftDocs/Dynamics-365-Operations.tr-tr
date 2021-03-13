---
title: Kıymet sayaçlarını otomatik olarak güncelleştirme
description: Bu konuda, Varlık Yönetiminde varlık sayaçlarının otomatik olarak güncelleştirilmesi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3e8619439545cf3ea42f84a6dd7ee6ffdf1026e
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021942"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="c53d1-103">Kıymet sayaçlarını otomatik olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c53d1-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c53d1-104">Varlık sayaçlarının el ile kaydı hakkında bilgi edinmek için bkz. [Varlık sayaçlarının el ile güncelleştirilmesi](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="c53d1-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="c53d1-105">Varlık sayaçlarının nasıl ayarlanacağı konusunda bilgi için bkz. [Sayaçlar](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="c53d1-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="c53d1-106">Sayaç değerleri, üretim saetleri veya üretim miktarına (bu üretilen miktardır) göre üretim kayıtlarından da otomatik olarak güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="c53d1-107">Bu güncelleştirme, **Varlık sayaçlarını güncelleştir** sayfasında gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="c53d1-108">Bir veya daha fazla varlığı bir **Başlangıç tarihi** parametresi ayarlayarak güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="c53d1-109">Bu parametre, üretim kayıtları (üretim saatleri veya üretim miktarları) için başlangıç tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="c53d1-110">Başka bir deyişle, sayaç değerlerinin güncelleştirilmesi gereken tarihi belirtir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="c53d1-111">Bir kaynakla ilişkili olan *ve* üretim saatlerine veya üretim miktarına göre güncelleştirilmek üzere ayarlanan varlık sayaçları bulunan tüm varlıklar otomatik güncelleştirmeye dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="c53d1-112">Yeni sayaç değerleri oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c53d1-112">New counter values will be created.</span></span>

<span data-ttu-id="c53d1-113">Üretim miktarına dayalı sayaçlar için sayım, hem sağlam miktarı hem de kaydedilen hata miktarını içerir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="c53d1-114">Üretim miktaır kaydı için kullanılan birim sayaçta kullanılan birimden farklıysa miktar sayaç birimine karşılık gelecek şekilde dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="c53d1-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="c53d1-115">Yukarıda belirtildiği gibi, otomatik sayaçlar üretim kayıtlarından güncelleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="c53d1-116">Bu nedenle, sayaçlarını otomatik olarak güncelleştirmek istediğiniz varlık bir kaynakla (makine) ilişkili olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c53d1-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="c53d1-117">Üretilen miktarlar veya üretim saatleri kaynağa kaydedildiğinde, ilgili varlık sayaçlarını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="c53d1-118">**Varlık yönetimi** > **Periyodik** > **Varlıklar** > **Varlık sayaçlarını güncelleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c53d1-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="c53d1-119">**Başlangıç tarihi** alanında otomatik güncelleştirmenin başlangıç tarihini seçin.</span><span class="sxs-lookup"><span data-stu-id="c53d1-119">In the **From date** field, select the start date of the automatic update.</span></span>

    >[!NOTE]
    ><span data-ttu-id="c53d1-120">Bu alandaki tarih, **Rota hareketlerinden** gelen "süren iş" tarihidir (**Üretim denetimi** > **Sorgular ve raporlar** > **Üretim** > **Rota hareketleri** > **Fiziksel tarih** alanı).</span><span class="sxs-lookup"><span data-stu-id="c53d1-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="c53d1-121">**Dahil edilecek kayıtlar** hızlı sekmesinde, otomatik güncelleştirme için belirli varlıkları, varlık türlerini veya kaynakları seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="c53d1-122">**Filtre**'yi seçin ve ilgili seçimleri yapın.</span><span class="sxs-lookup"><span data-stu-id="c53d1-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="c53d1-123">**Arka planda çalıştır** hızlı sekmesinde gerektiğinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

    <span data-ttu-id="c53d1-124">Aşağıdaki örnekte **Varlık sayaçlarını güncelleştir** iletişim kutusunun bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

    ![Şekil 1](media/12-work-orders.png)

5. <span data-ttu-id="c53d1-126">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c53d1-126">Select **OK**.</span></span> 

<span data-ttu-id="c53d1-127">Otomatik varlık sayacı güncelleştirmesi yapıldıktan sonra, **Varlık sayaçları** sayfasında bulunan varlıkla ilgili sayaç kayıtlarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="c53d1-128">**Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar**'ı seçin, varlığı seçin ve ardından Eylem Bölmesinde **Varlık** sekmesine gidip **Önleyici** grubundan **Sayaçlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c53d1-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="c53d1-129">**Varlık toplam değeri** sayfasında tüm varlıklardaki tüm sayaç türlerinde yapılmış en son kaydın genel görünümünü alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="c53d1-130">**Varlık Yönetimi** > **Sorgular** > **Varlıklar** > **Varlık toplam değeri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="c53d1-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="c53d1-131">Bu sayfa, **Varlık sayaçları** sayfasına benzer, ancak kayıt ekleyemez veya düzenleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="c53d1-132">Yalnızca genel bakış içindir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-132">It's for overview only.</span></span>

<span data-ttu-id="c53d1-133">Aşağıdaki örnekte **Varlık toplam değeri** sayfasının bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Şekil 2](media/13-work-orders.png)

<span data-ttu-id="c53d1-135">Aaşağıdaki noktaları unutmayın:</span><span class="sxs-lookup"><span data-stu-id="c53d1-135">Note the following points:</span></span>

- <span data-ttu-id="c53d1-136">Otomatik olarak güncelleştirilen sayaç türleri için el ile sayaç değeri kayıtları da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="c53d1-137">Daha fazla bilgi için bkz. [Varlık sayaçlarını el ile güncelleştirme](../work-orders/manual-update-of-asset-counters.md).</span><span class="sxs-lookup"><span data-stu-id="c53d1-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="c53d1-138">Başka bir sayaca ilişkin sayaçlar ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c53d1-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="c53d1-139">Bu durumda, bir sayaç güncelleştirildiğinde, ilgili sayaçlar aynı anda otomatik olarak güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c53d1-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="c53d1-140">İlgili sayaçların nasıl ayarlanacağı konusunda daha fazla bilgi için bkz. [Sayaçlar](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="c53d1-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

