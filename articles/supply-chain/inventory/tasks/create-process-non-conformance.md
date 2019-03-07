---
title: Uyumluluk oluşturma ve işleme
description: Uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmek için bu yordamı kullanın.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16ed11bce92920fe8240fc85f706a2ac6ab0a04b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "336302"
---
# <a name="create-and-process-a-conformance"></a><span data-ttu-id="f63de-103">Uyumluluk oluşturma ve işleme</span><span class="sxs-lookup"><span data-stu-id="f63de-103">Create and process a conformance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f63de-104">Uygunsuzluk yönetimini var olan bir kalite emrine göre gerçekleştirmek için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="f63de-104">Use this procedure to perform nonconformance management, based on an existing quality order.</span></span> <span data-ttu-id="f63de-105">Bu kaydı USMF demo şirketinde çalıştırabilir ve önerilen değerleri kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f63de-105">You can run this recording in the USMF demo company and can use the suggested values.</span></span> <span data-ttu-id="f63de-106">Tipik olarak, bu yordam kalite görevlisi tarafından gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f63de-106">Typically, this procedure is performed by a quality clerk.</span></span>  <span data-ttu-id="f63de-107">Bir önkoşul olarak "Malların kalitesini incele" görev kaydını çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f63de-107">As a prerequisite, run the “Inspect the quality of goods” task recording.</span></span> <span data-ttu-id="f63de-108">Bir uygunsuzluk onayını işlemek için görev kaydını çalıştıran kullanıcının atanmış kullanıcılar sayfasında bir "Ad" değeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f63de-108">To process the approval of a nonconformance, the user who runs the task recording must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="f63de-109">Kullanıcının belge notları kullanabilmesi için belge işleme seçeneğinin kullanıcı ayarlarında etkinleştirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="f63de-109">To use the document notes, the user must also have Document handling activated in the user options.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="f63de-110">Bir kalite emri seçin</span><span class="sxs-lookup"><span data-stu-id="f63de-110">Select a quality order</span></span>
1. <span data-ttu-id="f63de-111">Kalite emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="f63de-111">Go to Quality orders.</span></span>
2. <span data-ttu-id="f63de-112">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f63de-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f63de-113">"Malların kalitesini denetleme" görev kaydından oluşturulmuş kalite emrini seçin.</span><span class="sxs-lookup"><span data-stu-id="f63de-113">Select the quality order that was created from the "Inspect the quality of goods" task recording.</span></span>  

## <a name="create-a-nonconformance"></a><span data-ttu-id="f63de-114">Uygunsuzluk oluşturma</span><span class="sxs-lookup"><span data-stu-id="f63de-114">Create a nonconformance</span></span>
1. <span data-ttu-id="f63de-115">Sorgulamalar’ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-115">Click Inquiries.</span></span>
2. <span data-ttu-id="f63de-116">Uyumsuzluklar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-116">Click Non conformances.</span></span>
3. <span data-ttu-id="f63de-117">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-117">Click New.</span></span>
4. <span data-ttu-id="f63de-118">Sorun türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-118">In the Problem type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f63de-119">İnceleme sürecinde bulunan sorunu seçin.</span><span class="sxs-lookup"><span data-stu-id="f63de-119">Select the problem that was found during the inspection process.</span></span>  
5. <span data-ttu-id="f63de-120">Sorun türü alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-120">In the Problem type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f63de-121">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="f63de-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f63de-122">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f63de-123">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-123">Click OK.</span></span>

## <a name="approvereject-a-nonconformance"></a><span data-ttu-id="f63de-124">Bir uygunsuzluğu onaylama/reddetme</span><span class="sxs-lookup"><span data-stu-id="f63de-124">Approve/reject a nonconformance</span></span>
1. <span data-ttu-id="f63de-125">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-125">Click Functions.</span></span>
2. <span data-ttu-id="f63de-126">Uyumsuzluğu onayla'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-126">Click Approve non conformance.</span></span>
    * <span data-ttu-id="f63de-127">Bu örnek için, uygunsuzluğu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-127">For this example, approve the nonconformance.</span></span> <span data-ttu-id="f63de-128">Onaylanan uygunsuzluklar, ilgili operasyonlar ile uygunsuzluk işleme sürecinin bir parçası olarak yerine getirilen işlerin kaydını tutmak ve, bu görev kaydında olduğu gibi, uygunsuzluk işlemesini işlemden geçirmek için ilişkilendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="f63de-128">Approved nonconformances can be associated with related operations to record work that is done as part of the nonconformance handling and, as in this task recording, the processing of correction handling.</span></span>  
3. <span data-ttu-id="f63de-129">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-129">Click Yes.</span></span>

## <a name="create-a-correction-action"></a><span data-ttu-id="f63de-130">Düzeltme eylemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f63de-130">Create a correction action</span></span>
1. <span data-ttu-id="f63de-131">Düzeltmeler'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-131">Click Corrections.</span></span>
2. <span data-ttu-id="f63de-132">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-132">Click New.</span></span>
3. <span data-ttu-id="f63de-133">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="f63de-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f63de-134">Personel numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-134">In the Personnel number field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f63de-135">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-135">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f63de-136">Seç'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-136">Click Select.</span></span>
7. <span data-ttu-id="f63de-137">İliştir'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-137">Click Attach.</span></span>
    * <span data-ttu-id="f63de-138">Düzeltme hakkında bir not oluşturun.</span><span class="sxs-lookup"><span data-stu-id="f63de-138">Create a note about the correction.</span></span> <span data-ttu-id="f63de-139">Bu örnek için eylem, uygunsuzluk durumunu tartışmak için satıcıya başvurmaktır.</span><span class="sxs-lookup"><span data-stu-id="f63de-139">For this example, the action is to contact the vendor to discuss the nonconformance case.</span></span>  
8. <span data-ttu-id="f63de-140">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-140">Click New.</span></span>
9. <span data-ttu-id="f63de-141">Not'a tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-141">Click Note.</span></span>
    * <span data-ttu-id="f63de-142">Rapor kurulumuna bağlı olarak, uygunsuzluk yönetimiyle ilgili raporların üzerine farklı belge türlerinin yazdırılabilir olduğunu unutmayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-142">Note that, depending on the report setup, different document types can be printed on the reports that are related to nonconformance management.</span></span>  
10. <span data-ttu-id="f63de-143">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="f63de-143">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f63de-144">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-144">Close the page.</span></span>

## <a name="maintain-a-correction"></a><span data-ttu-id="f63de-145">Bir düzeltmeyi yönet</span><span class="sxs-lookup"><span data-stu-id="f63de-145">Maintain a correction</span></span>
1. <span data-ttu-id="f63de-146">Tamamlandı olarak işaretle'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-146">Click Mark complete.</span></span>
2. <span data-ttu-id="f63de-147">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-147">Click OK.</span></span>
3. <span data-ttu-id="f63de-148">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-148">Close the page.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="f63de-149">Bir uygunsuzluğu kapat</span><span class="sxs-lookup"><span data-stu-id="f63de-149">Close a nonconformance</span></span>
1. <span data-ttu-id="f63de-150">İşlevler'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-150">Click Functions.</span></span>
2. <span data-ttu-id="f63de-151">Uygunsuzluğu kapat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="f63de-151">Click Close non conformance.</span></span>
3. <span data-ttu-id="f63de-152">Evet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-152">Click Yes.</span></span>
4. <span data-ttu-id="f63de-153">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-153">Close the page.</span></span>
5. <span data-ttu-id="f63de-154">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="f63de-154">Close the page.</span></span>
