---
title: Uyumluluk oluşturma ve işleme
description: Uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi bu konu açıklar.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4525e79cb388cc9bbcfe1d038a53cf53916a678c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008114"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="a7863-103">Uyumluluk oluşturma ve işleme</span><span class="sxs-lookup"><span data-stu-id="a7863-103">Create and process a conformance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a7863-104">Uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmeyi bu konu açıklar.</span><span class="sxs-lookup"><span data-stu-id="a7863-104">This topic explains how to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="a7863-105">Bu kaydı USMF demo şirketinde çalıştırabilir ve önerilen değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7863-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="a7863-106">Tipik olarak, bu yordam kalite görevlisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a7863-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="a7863-107">Önkoşul olarak, [Malların kalitesini incele](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) içindeki talimatlar bakın.</span><span class="sxs-lookup"><span data-stu-id="a7863-107">As a prerequisite, complete the instructions in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span> <span data-ttu-id="a7863-108">Bir uygunsuzluk onayını işlemek için görev kaydını çalıştıran kullanıcının atanmış kullanıcılar sayfasında bir "Ad" değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a7863-108">To process the approval of a nonconformance, the user who runs the task recording must have a "Name" value assigned on the Users page.</span></span> <span data-ttu-id="a7863-109">Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a7863-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="a7863-110">Bir kalite emri seçin</span><span class="sxs-lookup"><span data-stu-id="a7863-110">Select a quality order</span></span>
1. <span data-ttu-id="a7863-111">Gezinti panelinde **Modüller > Stok yönetimi > Periyodik görevler > Kalite yönetimi > Kalite emirleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="a7863-111">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="a7863-112">Listede, [Malların kalitesini incele](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) içinde oluşturulmuş kalite emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-112">In the list, select the quality order that was created in [Inspect the quality of goods](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="a7863-113">Uygunsuzluk oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7863-113">Create a nonconformance</span></span>
1. <span data-ttu-id="a7863-114">Eylem Bölmesi'nde, **Sorgular**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-114">On the Action Pane, select **Inquiries**.</span></span>
2. <span data-ttu-id="a7863-115">**Uyumsuzluklar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-115">Select **Non conformances**.</span></span>
3. <span data-ttu-id="a7863-116">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-116">Select **New**.</span></span>
4. <span data-ttu-id="a7863-117">**Problem türü** alanının açılı menüsünde, denetleme işlemi sırasında bulunan problemi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-117">In the drop-down menu of the **Problem type** field, select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="a7863-118">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-118">Select **OK**.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="a7863-119">Bir uygunsuzluğu onaylama/reddetme</span><span class="sxs-lookup"><span data-stu-id="a7863-119">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="a7863-120">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-120">Select **Functions**.</span></span>
2. <span data-ttu-id="a7863-121">**Uyumsuzluğu onayla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-121">Select **Approve non conformance**.</span></span> <span data-ttu-id="a7863-122">Bu örnek için, uygunsuzluğu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="a7863-122">For this example, approve the nonconformance.</span></span> <span data-ttu-id="a7863-123">Onaylanan uygunsuzluklar, ilgili operasyonlar ile uygunsuzluk işleme sürecinin bir parçası olarak yerine getirilen işlerin kaydını tutmak ve, bu konuda olduğu gibi, uygunsuzluk işlemesini işlemden geçirmek için ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a7863-123">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this topic, the processing of correction handling.</span></span>  
3. <span data-ttu-id="a7863-124">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-124">Select **Yes**.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="a7863-125">Düzeltme eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a7863-125">Create a correction action</span></span>
1. <span data-ttu-id="a7863-126">**Düzeltmeler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-126">Select **Corrections**.</span></span>
2. <span data-ttu-id="a7863-127">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-127">Select **New**.</span></span>
3. <span data-ttu-id="a7863-128">Yeni satırın **Personel numarası** alanında, açılır menüden istenilen kaydı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-128">In the **Personnel number** field of the new row, select the desired record from the drop down menu.</span></span>
4. <span data-ttu-id="a7863-129">**Seç**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a7863-129">Click **Select**.</span></span>
5. <span data-ttu-id="a7863-130">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-130">Select **Attach**.</span></span> <span data-ttu-id="a7863-131">Düzeltme hakkında bir not oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a7863-131">Create a note about the correction.</span></span> <span data-ttu-id="a7863-132">Bu örnek için eylem, uygunsuzluk durumunu tartışmak için satıcıya başvurmaktır.</span><span class="sxs-lookup"><span data-stu-id="a7863-132">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
6. <span data-ttu-id="a7863-133">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-133">Select **New**.</span></span>
7. <span data-ttu-id="a7863-134">**Not**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-134">Select **Note**.</span></span> <span data-ttu-id="a7863-135">Rapor kurulumuna bağlı olarak, uygunsuzluk yönetimiyle ilgili raporların üzerine farklı belge türlerinin yazdırılabilir.</span><span class="sxs-lookup"><span data-stu-id="a7863-135">Depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
8. <span data-ttu-id="a7863-136">**Tanım** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="a7863-136">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="a7863-137">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a7863-137">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="a7863-138">Bir düzeltmeyi yönet</span><span class="sxs-lookup"><span data-stu-id="a7863-138">Maintain a correction</span></span>
1. <span data-ttu-id="a7863-139">**Tamamladı işaretle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-139">Select **Mark complete**.</span></span>
2. <span data-ttu-id="a7863-140">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-140">Select **OK**.</span></span>
3. <span data-ttu-id="a7863-141">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a7863-141">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="a7863-142">Bir uygunsuzluğu kapat</span><span class="sxs-lookup"><span data-stu-id="a7863-142">Close a nonconformance</span></span>
1. <span data-ttu-id="a7863-143">**İşlevler**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-143">Select **Functions**.</span></span>
2. <span data-ttu-id="a7863-144">**Uyumsuzluğu kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-144">Select **Close non conformance**.</span></span>
3. <span data-ttu-id="a7863-145">**Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a7863-145">Select **Yes**.</span></span>
4. <span data-ttu-id="a7863-146">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="a7863-146">Close the pages.</span></span>
