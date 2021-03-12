---
title: Üretim emri oluşturma
description: Bu prosedür, bir üretim emrinin nasıl oluşturulacağını gösterir.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute, ProdJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81caa6693d86c797d8565270094556ae4e103e6a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998690"
---
# <a name="create-a-production-order"></a><span data-ttu-id="ec6a8-103">Üretim emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="ec6a8-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec6a8-104">Bu prosedür, bir üretim emrinin nasıl oluşturulacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="ec6a8-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ec6a8-106">Bu, üretim emri ömrünü açıklayan yedi yordamın birincisidir.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="ec6a8-107">Üretim emri oluşturma</span><span class="sxs-lookup"><span data-stu-id="ec6a8-107">Create a production order</span></span>
1. <span data-ttu-id="ec6a8-108">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="ec6a8-109">Yeni üretim emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-109">Click New production order.</span></span>
3. <span data-ttu-id="ec6a8-110">Madde numarası alanına 'D0001' girin.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="ec6a8-111">Teslimat alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="ec6a8-112">Teslim tarihi, zamanında teslimat yapılabilmesi için bir üretim emrinin ne zaman bitmesi gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="ec6a8-113">Bu tarih planlama işleminde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="ec6a8-114">Örneğin, emri teslim tarihinden geriye doğru planlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="ec6a8-115">Miktarı '20' olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="ec6a8-116">Not: Ürün reçetesi numarası alanı, geçerli madde için etkin olan herhangi bir ürün reçetesi numarasını gösterir ancak onaylanan ürün reçetesi sürümlerinin listesinden etkin bir ürün reçetesi seçerek üretim emri için ürün reçetesini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="ec6a8-117">Not: Rota numarası alanı, geçerli madde için etkin olan herhangi bir Rota numarasını gösterir ancak onaylanan Rota sürümlerinin listesinden etkin bir Rota seçerek üretim emri için Rotayı değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="ec6a8-118">Oluştur'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="ec6a8-119">Üretim emrini doğrulama</span><span class="sxs-lookup"><span data-stu-id="ec6a8-119">Validate the production order</span></span>
1. <span data-ttu-id="ec6a8-120">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ec6a8-121">Yeni oluşturduğunuz üretim emri numarası bağlantısına tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="ec6a8-122">Bu, siparişle ilgili ayrıntılar sayfasını açar.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="ec6a8-123">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-123">Click Edit.</span></span>
3. <span data-ttu-id="ec6a8-124">Teslimat alanına bir tarih girin.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="ec6a8-125">Örneğin, üretim emrinin teslim tarihini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="ec6a8-126">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-126">Click Save.</span></span>
5. <span data-ttu-id="ec6a8-127">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="ec6a8-128">Ürün reçetesini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ec6a8-128">Update the BOM</span></span>
1. <span data-ttu-id="ec6a8-129">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="ec6a8-130">Ürün reçetesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-130">Click BOM.</span></span>
    * <span data-ttu-id="ec6a8-131">Üretim emri oluşturulurken varsayılan verilerden kopyalanan ürün reçetesi verilerini doğrulamak için ürün reçetesi sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="ec6a8-132">Bu yordamda, bir ürün reçetesi için miktarı güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="ec6a8-133">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-133">Click Edit.</span></span>
4. <span data-ttu-id="ec6a8-134">Miktar alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ec6a8-135">Ürün reçetesi satırındaki miktarı değiştirmek, üretim emrine ilişkin malzeme tüketiminin maliyet tahminini etkiler.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="ec6a8-136">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-136">Click Save.</span></span>
6. <span data-ttu-id="ec6a8-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="ec6a8-138">Üretim rotasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ec6a8-138">Update the production route</span></span>
1. <span data-ttu-id="ec6a8-139">Eylem Bölmesinde, Üretim emri öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="ec6a8-140">Rota'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-140">Click Route.</span></span>
    * <span data-ttu-id="ec6a8-141">Üretim emri oluşturulurken varsayılan verilerden kopyalanan ürün rotası verilerini doğrulamak için Rota sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="ec6a8-142">Bu yordamda, bir üretim rotasındaki operasyonlardan biri için miktarı güncelleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="ec6a8-143">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ec6a8-144">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-144">Click Edit.</span></span>
5. <span data-ttu-id="ec6a8-145">İşlem miktarı alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="ec6a8-146">İşlem süresini değiştirmek tahmini rota tüketimini ve üretim emri maliyetini etkiler.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="ec6a8-147">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-147">Click Save.</span></span>
7. <span data-ttu-id="ec6a8-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ec6a8-148">Close the page.</span></span>

