---
title: Eksik çekilen madde yeniden tahsisini ayarlama
description: Bu konuda, size, ambar çalışanlarının yönlendirildikleri yerleşimde yeterli stok olmadığında alternatif yerleşimleri hızlı bir şekilde bulmalarının nasıl sağlanacağı gösterilmektedir.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e14a4fc72d256bea31296bff80d5b5818b95ea9d
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527431"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="e3e95-103">Eksik çekilen madde yeniden tahsisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="e3e95-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3e95-104">Bu yordam, size, ambar çalışanlarının yönlendirildikleri yerleşimde yeterli stok olmadığında alternatif yerleşimleri hızlı bir şekilde bulmalarının nasıl sağlanacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="e3e95-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="e3e95-105">Yeniden tahsisat işlemi bir **İş özel durumu** ile denetlenir ve ambar **çalışanı** tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="e3e95-106">Otomatik, El ile veya her iki yeniden tahsisat işlemi kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="e3e95-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="e3e95-107">Otomatik yeniden tahsisat - Malların başka bir yerleşimde olup olmadığını belirlemek için yerleşim yönergeleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="e3e95-108">Mümkünse, iş güncelleştirilecek ve ambar kullanıcısı alternatif yerleşime yönlendirilecektir.</span><span class="sxs-lookup"><span data-stu-id="e3e95-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="e3e95-109">El ile yeniden tahsisat - Ambar kullanıcısının rezerve edilmemiş mal miktarları olan bir veya daha fazla yerleşimden seçim yapmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="e3e95-110">Otomatik ve el ile - Sistem otomatik yeniden tahsisat gerçekleştiremezse ve rezerve edilmemiş miktarlar bulunan yerleşimler varsa, kullanıcıdan bir yerleşim seçmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="e3e95-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="e3e95-111">İş özel durumlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="e3e95-111">Set up work exceptions</span></span>
<span data-ttu-id="e3e95-112">Ambar çalışanının işledikleri sevkiyatın ihtiyaçlarına göre bir seçim yapabilmesi için, farklı madde yeniden tahsis ilkelerine sahip birden çok iş özel durumu tanımlamak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="e3e95-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="e3e95-113">Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="e3e95-114">**Gezinti panosu**'nda, **Ambar yönetimi > Kurulum > İş > İş istisnaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="e3e95-115">**Yeni**'ye tıklayın</span><span class="sxs-lookup"><span data-stu-id="e3e95-115">Click **New**</span></span> 
3. <span data-ttu-id="e3e95-116">**İş özel durumu kodu** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="e3e95-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="e3e95-117">Bu, bu özel durumun başlığı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-117">This will be the title of this exception .</span></span> <span data-ttu-id="e3e95-118">Örneğin, Kısa malzeme çekme kılavuzu.</span><span class="sxs-lookup"><span data-stu-id="e3e95-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="e3e95-119">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="e3e95-120">Bu, bu özel durumun kullanımıyla ilgili kısa bir açıklama olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="e3e95-121">Örneğin, Kısa malzeme çekme - madde mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="e3e95-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="e3e95-122">**Özel durum** türü alanında, **Kısa çekme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="e3e95-123">**Stoğu ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="e3e95-124">Seçilirse, stok kısa malzeme çekme yerleşiminde 0'a otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="e3e95-125">**Varsayılan ayarlama türü kodu** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="e3e95-126">Örneğin, USMF'de **Kaynak Kaldırma Ayarlama Devre Dışı**'nı seçebilirsiniz. Her ayarlama türü kodu dört temel özellik içerir: ad, açıklama, stok günlüğü adı ve **Rezervasyonları kaldır**.</span><span class="sxs-lookup"><span data-stu-id="e3e95-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="e3e95-127">**Rezervasyonları kaldır** etkinse, kısa çekilen sipariş satırının rezervasyonları kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="e3e95-128">**Madde yeniden tahsisi** alanında bir değer seçin (örneğin El ile).</span><span class="sxs-lookup"><span data-stu-id="e3e95-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="e3e95-129">El ile veya Otomatik ve El ile seçeneklerini belirlerseniz, ambar çalışanının el ile yeniden tahsisi kullanmak için etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e3e95-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="e3e95-130">Çalışanı el ile madde yeniden tahsisini kullanmak üzere ayarlama</span><span class="sxs-lookup"><span data-stu-id="e3e95-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="e3e95-131">Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="e3e95-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="e3e95-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e3e95-132">Close the page.</span></span>
2. <span data-ttu-id="e3e95-133">**Gezinti panosu**'nda, **Ambar yönetimi > Kurulum > Çalışan**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="e3e95-134">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="e3e95-134">Click **Edit**.</span></span>
4. <span data-ttu-id="e3e95-135">Listede çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-135">In the list, select worker.</span></span> <span data-ttu-id="e3e95-136">Örneğin Julia Finanderburk.</span><span class="sxs-lookup"><span data-stu-id="e3e95-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="e3e95-137">**Kullanıcılar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="e3e95-138">Listede bir **Kullanıcı kodu** seçin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="e3e95-139">Örneğin, 24.</span><span class="sxs-lookup"><span data-stu-id="e3e95-139">For example, 24.</span></span>
7. <span data-ttu-id="e3e95-140">**İş** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="e3e95-141">**El ile madde yeniden tahsisine izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e3e95-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
