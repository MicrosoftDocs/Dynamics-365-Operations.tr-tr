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
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4439653"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="a6ea4-103">Eksik çekilen madde yeniden tahsisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="a6ea4-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a6ea4-104">Bu yordam, size, ambar çalışanlarının yönlendirildikleri yerleşimde yeterli stok olmadığında alternatif yerleşimleri hızlı bir şekilde bulmalarının nasıl sağlanacağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="a6ea4-105">Yeniden tahsisat işlemi bir **İş özel durumu** ile denetlenir ve ambar **çalışanı** tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="a6ea4-106">Otomatik, El ile veya her iki yeniden tahsisat işlemi kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="a6ea4-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="a6ea4-107">Otomatik yeniden tahsisat - Malların başka bir yerleşimde olup olmadığını belirlemek için yerleşim yönergeleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="a6ea4-108">Mümkünse, iş güncelleştirilecek ve ambar kullanıcısı alternatif yerleşime yönlendirilecektir.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="a6ea4-109">El ile yeniden tahsisat - Ambar kullanıcısının rezerve edilmemiş mal miktarları olan bir veya daha fazla yerleşimden seçim yapmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="a6ea4-110">Otomatik ve el ile - Sistem otomatik yeniden tahsisat gerçekleştiremezse ve rezerve edilmemiş miktarlar bulunan yerleşimler varsa, kullanıcıdan bir yerleşim seçmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="a6ea4-111">İş özel durumlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="a6ea4-111">Set up work exceptions</span></span>
<span data-ttu-id="a6ea4-112">Ambar çalışanının işledikleri sevkiyatın ihtiyaçlarına göre bir seçim yapabilmesi için, farklı madde yeniden tahsis ilkelerine sahip birden çok iş özel durumu tanımlamak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="a6ea4-113">Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="a6ea4-114">**Gezinti panosu**'nda, **Ambar yönetimi > Kurulum > İş > İş istisnaları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-114">In the **Navigation pane**, go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="a6ea4-115">**Yeni**'ye tıklayın</span><span class="sxs-lookup"><span data-stu-id="a6ea4-115">Click **New**</span></span> 
3. <span data-ttu-id="a6ea4-116">**İş özel durumu kodu** alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="a6ea4-117">Bu, bu özel durumun başlığı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-117">This will be the title of this exception .</span></span> <span data-ttu-id="a6ea4-118">Örneğin, Kısa malzeme çekme kılavuzu.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="a6ea4-119">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="a6ea4-120">Bu, bu özel durumun kullanımıyla ilgili kısa bir açıklama olacaktır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="a6ea4-121">Örneğin, Kısa malzeme çekme - madde mevcut değil.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="a6ea4-122">**Özel durum** türü alanında, **Kısa çekme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="a6ea4-123">**Stoğu ayarla** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="a6ea4-124">Seçilirse, stok kısa malzeme çekme yerleşiminde 0'a otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="a6ea4-125">**Varsayılan ayarlama türü kodu** alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="a6ea4-126">Örneğin, USMF'de **Kaynak Kaldırma Ayarlama Devre Dışı**'nı seçebilirsiniz. Her ayarlama türü kodu dört temel özellik içerir: ad, açıklama, stok günlüğü adı ve **Rezervasyonları kaldır**.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="a6ea4-127">**Rezervasyonları kaldır** etkinse, kısa çekilen sipariş satırının rezervasyonları kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="a6ea4-128">**Madde yeniden tahsisi** alanında bir değer seçin (örneğin El ile).</span><span class="sxs-lookup"><span data-stu-id="a6ea4-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="a6ea4-129">El ile veya Otomatik ve El ile seçeneklerini belirlerseniz, ambar çalışanının el ile yeniden tahsisi kullanmak için etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="a6ea4-130">Çalışanı el ile madde yeniden tahsisini kullanmak üzere ayarlama</span><span class="sxs-lookup"><span data-stu-id="a6ea4-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="a6ea4-131">Bu yordamı oluşturmak için USMF demo verileri şirketi kullanılmıştır.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="a6ea4-132">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-132">Close the page.</span></span>
2. <span data-ttu-id="a6ea4-133">**Gezinti panosu**'nda, **Ambar yönetimi > Kurulum > Çalışan**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-133">In the **Navigation pane**, go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="a6ea4-134">**Düzenle**'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-134">Click **Edit**.</span></span>
4. <span data-ttu-id="a6ea4-135">Listede çalışan seçin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-135">In the list, select worker.</span></span> <span data-ttu-id="a6ea4-136">Örneğin Julia Finanderburk.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="a6ea4-137">**Kullanıcılar** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="a6ea4-138">Listede bir **Kullanıcı kodu** seçin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="a6ea4-139">Örneğin, 24.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-139">For example, 24.</span></span>
7. <span data-ttu-id="a6ea4-140">**İş** hızlı sekmesini genişletin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="a6ea4-141">**El ile madde yeniden tahsisine izin ver** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a6ea4-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
