---
title: Oluşturmadan başlangıca toplu iş emri yaşam döngüsü
description: Bu yordam, bir toplu iş emrinin yaşam döngüsünün ilk kısmını adım adım açıklar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3582791fa0564e17338593152e13644322cdb44
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147193"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="4e99c-103">Oluşturmadan başlangıca toplu iş emri yaşam döngüsü</span><span class="sxs-lookup"><span data-stu-id="4e99c-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e99c-104">Bu yordam, bir toplu iş emrinin yaşam döngüsünün ilk kısmını adım adım açıklar.</span><span class="sxs-lookup"><span data-stu-id="4e99c-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="4e99c-105">Oluşturma, maliyet tahmini işleminden ve üretim işi planlamasından toplu iş emrine kadar tüm adımları içerir.</span><span class="sxs-lookup"><span data-stu-id="4e99c-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="4e99c-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="4e99c-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="4e99c-107">Bu yordamı başka bir veri kümesiyle çalıştırmanın önkoşulları etkin bir formül ve rota sürümü ile sevk edilmiş bir ürün bulunmasıdır.</span><span class="sxs-lookup"><span data-stu-id="4e99c-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="4e99c-108">Toplu iş emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="4e99c-108">Create a batch order</span></span>
1. <span data-ttu-id="4e99c-109">Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4e99c-109">Go to All production orders.</span></span>
2. <span data-ttu-id="4e99c-110">Yeni toplu iş emri'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-110">Click New batch order.</span></span>
3. <span data-ttu-id="4e99c-111">Madde numarası alanında bir değer girin veya seçin.</span><span class="sxs-lookup"><span data-stu-id="4e99c-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="4e99c-112">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-112">Click Create.</span></span>
5. <span data-ttu-id="4e99c-113">Üretim alanına bir filtre uygulamak için 'b' değeriyle Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="4e99c-114">Üretim formülünü ve beklenen ortak ürünleri görüntüleme</span><span class="sxs-lookup"><span data-stu-id="4e99c-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="4e99c-115">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="4e99c-116">Formül’ü tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-116">Click Formula.</span></span>
3. <span data-ttu-id="4e99c-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-117">Close the page.</span></span>
4. <span data-ttu-id="4e99c-118">Ortak ürünler’i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-118">Click Co-products.</span></span>
5. <span data-ttu-id="4e99c-119">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="4e99c-120">Toplu iş emrini tahmin etme</span><span class="sxs-lookup"><span data-stu-id="4e99c-120">Estimate the batch order</span></span>
1. <span data-ttu-id="4e99c-121">Tahmin seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-121">Click Estimate.</span></span>
2. <span data-ttu-id="4e99c-122">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-122">Click OK.</span></span>
3. <span data-ttu-id="4e99c-123">Eylem Bölmesinde Yönet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="4e99c-124">Hesaplama ayrıntılarını görüntüle seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-124">Click View calculation details.</span></span>
5. <span data-ttu-id="4e99c-125">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="4e99c-126">Toplu iş emrini sevk etme</span><span class="sxs-lookup"><span data-stu-id="4e99c-126">Release the batch order</span></span>
1. <span data-ttu-id="4e99c-127">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="4e99c-128">Serbest bırak öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-128">Click Release.</span></span>
3. <span data-ttu-id="4e99c-129">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="4e99c-130">Üretim işlerini zamanlama</span><span class="sxs-lookup"><span data-stu-id="4e99c-130">Schedule production jobs</span></span>
1. <span data-ttu-id="4e99c-131">Eylem Bölmesinde, Planla öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="4e99c-132">İşleri planla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="4e99c-133">Sınırlı kapasite alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e99c-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="4e99c-134">Sınırlı malzeme alanında Hayır'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="4e99c-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="4e99c-135">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-135">Click OK.</span></span>
6. <span data-ttu-id="4e99c-136">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="4e99c-137">Tüm işleri çalıştır'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-137">Click All jobs.</span></span>
8. <span data-ttu-id="4e99c-138">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="4e99c-139">Toplu iş emrini başlatma</span><span class="sxs-lookup"><span data-stu-id="4e99c-139">Start the batch order</span></span>
1. <span data-ttu-id="4e99c-140">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-140">Click Start.</span></span>
2. <span data-ttu-id="4e99c-141">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-141">Click the General tab.</span></span>
3. <span data-ttu-id="4e99c-142">Malzeme çekme listesini şimdi naklet alanında Hayır seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4e99c-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="4e99c-143">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-143">Click OK.</span></span>
5. <span data-ttu-id="4e99c-144">Eylem Bölmesinde, Görüntüle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="4e99c-145">Malzeme çekme listesi'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-145">Click Picking list.</span></span>
7. <span data-ttu-id="4e99c-146">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4e99c-147">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-147">Close the page.</span></span>
9. <span data-ttu-id="4e99c-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-148">Close the page.</span></span>
10. <span data-ttu-id="4e99c-149">Rota kartı'nı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-149">Click Route card.</span></span>
11. <span data-ttu-id="4e99c-150">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="4e99c-151">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-151">Close the page.</span></span>
13. <span data-ttu-id="4e99c-152">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4e99c-152">Close the page.</span></span>

