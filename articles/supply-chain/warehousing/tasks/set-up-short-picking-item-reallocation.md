---
title: Kısa alım maddesi yeniden tahsisini ayarlama
description: Bu yordam yönlendirildikleri konumda yeterli stok olmadığında alternatif konumları hızlı bir şekilde bulmak üzere ambar çalışanlarını etkinleştirmeyi gösterir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a3c635c32a53226da6ce72db86ee7d9d0c17bdb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847099"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="01c41-103">Kısa alım maddesi yeniden tahsisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="01c41-103">Set up short picking item reallocation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01c41-104">Bu yordam yönlendirildikleri konumda yeterli stok olmadığında alternatif konumları hızlı bir şekilde bulmak üzere ambar çalışanlarını etkinleştirmeyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="01c41-104">This procedure shows you how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> <span data-ttu-id="01c41-105">Başka bir konumda kullanılabilen malları almak için konum yönergeleri kullanan otomatik yeniden tahsis işlemi kullanmak da mümkündür.</span><span class="sxs-lookup"><span data-stu-id="01c41-105">It’s possible to use an automatic re-allocation process, which uses location directives to retrieve the goods if they’re available at another location.</span></span> <span data-ttu-id="01c41-106">Alternatif olarak, el ile yeniden tahsis kullanıldığında, kullanılabilir miktara sahip konumların listesi mobil cihazda görüntülenir ve ambar çalışanı stoğun kullanılacağı konumu seçebilir.</span><span class="sxs-lookup"><span data-stu-id="01c41-106">Alternatively, when manual re-allocation is used, a list of the locations with the available quantity is shown on the mobile device, allowing the warehouse worker to choose which location to use inventory from.</span></span> <span data-ttu-id="01c41-107">Bu yordamı USMF demo veri şirketinde kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01c41-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="01c41-108">Bu yordam, Dynamics 365 for Operations sürüm 1611'e eklenen bir özellik içindir.</span><span class="sxs-lookup"><span data-stu-id="01c41-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-work-exceptions"></a><span data-ttu-id="01c41-109">İş özel durumlarını ayarla</span><span class="sxs-lookup"><span data-stu-id="01c41-109">Set up work exceptions</span></span>
1. <span data-ttu-id="01c41-110">Ambar yönetimi > Kurulum > İş > İş özel durumları'na gidin.</span><span class="sxs-lookup"><span data-stu-id="01c41-110">Go to Warehouse management > Setup > Work > Work exceptions.</span></span>
2. <span data-ttu-id="01c41-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01c41-111">Click New.</span></span>
    * <span data-ttu-id="01c41-112">Ambar çalışanının işledikleri sevkiyatın ihtiyaçlarına göre bir seçim yapabilmesi için, farklı madde yeniden tahsis ilkelerine sahip birden çok iş özel durumu tanımlamak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="01c41-112">It’s possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>  
3. <span data-ttu-id="01c41-113">İş özel durumu kodu alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="01c41-113">In the Work exception code field, type a value.</span></span>
    * <span data-ttu-id="01c41-114">İş özel durumuna ne için kullanıldığını belirten bir başlık verin.</span><span class="sxs-lookup"><span data-stu-id="01c41-114">Give the work exception a title to indicate what it’s used for.</span></span> <span data-ttu-id="01c41-115">Örneğin, Kısa malzeme çekme kılavuzu.</span><span class="sxs-lookup"><span data-stu-id="01c41-115">For example, Short picking manual.</span></span>  
4. <span data-ttu-id="01c41-116">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="01c41-116">In the Description field, type a value.</span></span>
5. <span data-ttu-id="01c41-117">Özel durum türü alanında, 'Kısa çekme'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="01c41-117">In the Exception type field, select 'Short pick'.</span></span>
6. <span data-ttu-id="01c41-118">Stoğu ayarla onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="01c41-118">Select the Adjust inventory check box.</span></span>
    * <span data-ttu-id="01c41-119">Bu seçenek stoğun kısa malzeme çekme konumunda 0'a otomatik olarak ayarlanacağı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="01c41-119">This option means that inventory will automatically be adjusted to 0 at the short picked location.</span></span>  
7. <span data-ttu-id="01c41-120">Varsayılan ayarlama türü kodu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="01c41-120">In the Default adjustment type code field, enter or select a value.</span></span>
    * <span data-ttu-id="01c41-121">Örneğin, USMF'de 'Kaynak Res Adj Out' seçeneğini belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01c41-121">For example, in USMF you can select 'Remove Res Adj Out'.</span></span>  
8. <span data-ttu-id="01c41-122">Madde yeniden tahsisi alanında 'El ile'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="01c41-122">In the Item reallocation field, select 'Manual'.</span></span>
    * <span data-ttu-id="01c41-123">El ile veya Otomatik ve El ile seçeneklerini belirlerseniz, ambar çalışanının el ile yeniden tahsisi kullanmak için etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="01c41-123">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="01c41-124">Çalışanı el ile madde yeniden tahsisini kullanmak üzere ayarlama</span><span class="sxs-lookup"><span data-stu-id="01c41-124">Set up a worker to use manual item reallocation</span></span>
1. <span data-ttu-id="01c41-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="01c41-125">Close the page.</span></span>
2. <span data-ttu-id="01c41-126">Ambar yönetimi > Kurulum > Çalışan'a gidin.</span><span class="sxs-lookup"><span data-stu-id="01c41-126">Go to Warehouse management > Setup > Worker.</span></span>
3. <span data-ttu-id="01c41-127">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="01c41-127">Click Edit.</span></span>
4. <span data-ttu-id="01c41-128">Listede, çalışan 24'ü seçin.</span><span class="sxs-lookup"><span data-stu-id="01c41-128">In the list, select worker 24.</span></span>
5. <span data-ttu-id="01c41-129">İş bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="01c41-129">Expand the Work section.</span></span>
6. <span data-ttu-id="01c41-130">El ile madde yeniden tahsisine izin ver alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="01c41-130">Select Yes in the Allow manual item reallocation field.</span></span>

