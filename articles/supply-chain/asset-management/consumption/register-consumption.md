---
title: Tüketimi kaydetme
description: Bu konuda Varlık Yönetimi'nde tüketimi kaydetme işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea1522f8a8e4867d8d70fea59b493d139a1b01ef
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020793"
---
# <a name="register-consumption"></a><span data-ttu-id="73b13-103">Tüketimi kaydetme</span><span class="sxs-lookup"><span data-stu-id="73b13-103">Register consumption</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="73b13-104">Bir iş emrinde bakım işi tamamlandığında, bir sonraki adım tüketim kayıtları yapmak ve günlükleri deftere nakletmektir.</span><span class="sxs-lookup"><span data-stu-id="73b13-104">When a maintenance job has been completed on a work order, the next step is to make consumption registrations and post the journals.</span></span> <span data-ttu-id="73b13-105">Aşağıdaki tüketim türlerinde kayıt yapabilirsiniz: Saatler, maddeler ve giderler.</span><span class="sxs-lookup"><span data-stu-id="73b13-105">You can make registrations on the following consumption types: Hours, items, and expenses.</span></span> <span data-ttu-id="73b13-106">Farklı tüketim türleri **İş emri günlükleri** sayfasında kaydedilir ve deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="73b13-106">The different consumption types are registered and posted on the **Work order journals** page.</span></span> <span data-ttu-id="73b13-107">**Varlık Yönetimindeki** günlük kurulumu **Proje yönetimi ve muhasebe** modülündeki saatler, maddeler ve giderlere ilişkin ayrı günlükler oluşturmak ve deftere nakletmek amacıyla kullanılır.</span><span class="sxs-lookup"><span data-stu-id="73b13-107">The journal setup in **Asset Management** is used for creating and posting separate journals for hours, items, and expenses in the **Project management and accounting** module.</span></span>

<span data-ttu-id="73b13-108">Bazı durumlarda, bir iş emrine tahmin satırları ekleyebilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-108">In some cases, you may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="73b13-109">Bir iş emri yaşam döngüsü durumu, ilgili proje türü ve proje tipiyle ilgili aşama kuralları kurulumu, günlük satırları ekleyip ekleyemeyeceğinizi veya düzenleyip düzenleyemeyeceğinizi belirler.</span><span class="sxs-lookup"><span data-stu-id="73b13-109">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determine if you are able to add or edit journal lines.</span></span> <span data-ttu-id="73b13-110">İş emri yaşam döngüsü durumları ve ilgili proje aşamaları hakkında [Tahminler, iş emirleri ve projeler](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md) bölümünde daha fazla bilgi edinin.</span><span class="sxs-lookup"><span data-stu-id="73b13-110">Read more about work order lifecycle states and related project stages in [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

>[!NOTE]
><span data-ttu-id="73b13-111">Bir iş emri yaşam döngüsü durumunda günlüklerin otomatik olarak deftere nakledilmesini ayarlamak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="73b13-111">It is possible to set up automatic posting of journals on a work order lifecycle state.</span></span> <span data-ttu-id="73b13-112">Daha fazla bilgi için bkz. [İş emri yaşam döngüsü durumları](../setup-for-work-orders/work-order-lifecycle-states.md).</span><span class="sxs-lookup"><span data-stu-id="73b13-112">Refer to [Work order lifecycle states](../setup-for-work-orders/work-order-lifecycle-states.md) for more information.</span></span>

1. <span data-ttu-id="73b13-113">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73b13-113">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="73b13-114">İş emrini seçin ve **Günlükler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73b13-114">Select the work order, and click **Journals**.</span></span>

3. <span data-ttu-id="73b13-115">İş emrine bağlı olabilecek tahmin satırlarını transfer etmek için **Tahminden kopyala**'ya tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73b13-115">Click **Copy from forecast** to transfer any forecast lines that may be connected to the work order.</span></span> <span data-ttu-id="73b13-116">Transfer etmek istediğiniz tüketim tiplerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-116">You can select which consumption types you want to transfer.</span></span>

4. <span data-ttu-id="73b13-117">Gerekirse, **Satır ekle**'ye tıklayıp ve satırda verileri doldurarak ilgili hızlı sekmeye başka tüketim satırları da ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-117">If necessary, you can add more consumption lines on the relevant FastTab by clicking **Add line** and filling out data on the line.</span></span>

5. <span data-ttu-id="73b13-118">Deftere nakletmeden önce günlük satırlarını doğrulamak için **Günlükleri doğrula**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73b13-118">Click **Validate journals** to validate the journal lines before posting.</span></span>

6. <span data-ttu-id="73b13-119">Günlük satırlarını deftere nakletmek için **Günlükleri deftere naklet** öğesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73b13-119">Click **Post journals** to post the journal lines.</span></span>

7. <span data-ttu-id="73b13-120">Tüketim günlüklerini deftere naklettikten sonra, iş emri yaşam döngüsü durumunu güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-120">After you've posted the consumption journals, you can update the work order lifecycle state.</span></span> <span data-ttu-id="73b13-121">Örneğin, iş emrinin tamamlandığını belirtmek için, yaşam döngüsü durumunu "Sona erdi" olarak güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-121">For example, to indicate that the work order has been completed, you can update the lifecycle state to "Ended".</span></span>

    - <span data-ttu-id="73b13-122">**İş emri günlükleri** sayfasının en üstündeki **Göster** alanında, hangi günlük satırlarını görmek istediğinizi seçin: **tümü**, **deftere nakledilmemiş** veya **deftere nakledilmiş**.</span><span class="sxs-lookup"><span data-stu-id="73b13-122">In the **Show** field at the top of the **Work order journals** page, select which journal lines you want to see: **All**, **Not posted**, or **Posted**.</span></span> <span data-ttu-id="73b13-123">Deftere nakledilen günlüklerin **Deftere nakledildi** onay kutusunda onay işareti vardır.</span><span class="sxs-lookup"><span data-stu-id="73b13-123">Posted journals have a check mark in the **Posted** check box.</span></span>  
    - <span data-ttu-id="73b13-124">İş emri günlüğünde madde satırları oluşturulduğunda, maddeyle ilgili ürün boyutları ve izleme boyutları otomatik olarak günlük satırına transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="73b13-124">When item lines are created in the work order journal, product dimensions and tracking dimensions related to the item are automatically transferred to the journal line.</span></span>  

<span data-ttu-id="73b13-125">Aşağıdaki ekran görüntüsü, **İş emri günlüklerindeki** bir iş emrindeki bir saat ve madde kaydı örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="73b13-125">The screenshot below shows an example of hour and item registrations on a work order in **Work order journals**.</span></span>

![Şekil 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a><span data-ttu-id="73b13-127">Birkaç iş emri işine sahip iş emirlerindeki saatleri bölme</span><span class="sxs-lookup"><span data-stu-id="73b13-127">Split hours on work orders with several work order jobs</span></span>

<span data-ttu-id="73b13-128">Bir iş emri birkaç iş emri işi içeriyorsa, iş saatlerini **Saatleri böl** işlevini kullanarak kaydedebilirsiniz, böylece her bir saat kayıt satırı her iş emri işinde eşit şekilde dağıtılabilir.</span><span class="sxs-lookup"><span data-stu-id="73b13-128">If a work order contains several work order jobs, you can register work hours using the **Split hours** functionality, meaning one hour registration line can be distributed evenly on each work order job.</span></span>

1. <span data-ttu-id="73b13-129">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73b13-129">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="73b13-130">İş emrini seçin ve **Günlükler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73b13-130">Select the work order and click **Journals**.</span></span>

3. <span data-ttu-id="73b13-131">Bölmek istediğiniz saat kayıt satırını seçin ve **Saatleri böl**'e tıklatın.</span><span class="sxs-lookup"><span data-stu-id="73b13-131">Select the hour registration line you want to split, and click **Split hours**.</span></span>

4. <span data-ttu-id="73b13-132">**İş emri bakım işlerinde saatleri böl** iletişim kutusunda oturum açan çalışanın adı otomatik olarak **Çalışan** alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="73b13-132">In the **Split hours on work order maintenance jobs** dialog, the name of the worker who is logged in is automatically shown in the **Worker** field.</span></span> <span data-ttu-id="73b13-133">Gerekirse başka bir çalışan seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-133">If required, you can select another worker.</span></span>

5. <span data-ttu-id="73b13-134">**Kategori** alanında saat kaydı için bir kategori seçin.</span><span class="sxs-lookup"><span data-stu-id="73b13-134">Select a category for the hour registration in the **Category** field.</span></span>

6. <span data-ttu-id="73b13-135">**Saatler** alanına bölünecek çalışma saatleri sayısını ekleyin.</span><span class="sxs-lookup"><span data-stu-id="73b13-135">Insert number of work hours to be split in the **Hours** field.</span></span>

    ![Şekil 2](media/02-consumption.png)

7. <span data-ttu-id="73b13-137">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="73b13-137">Click **OK**.</span></span>

<span data-ttu-id="73b13-138">*Örnek:* Aşağıdaki ekran görüntüsünde, üç iş emri işi içeren bir iş emrine ait günlük satırları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="73b13-138">*Example:* In the screenshot below, journal lines for a work order containing three work order jobs are shown.</span></span> <span data-ttu-id="73b13-139">Üç iş saati içeren ilk satır bölünmüştür ve her bir iş emri işine bir saat kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="73b13-139">The first line, containing three work hours, has been split, and one work hour is registered on each work order job.</span></span> <span data-ttu-id="73b13-140">Üç saat kayıt satırı oluşturulduktan sonra, orijinal saat kayıt satırı (örnekteki ilk satır) ile ne yapılacağına karar verirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-140">After the three hour registration lines have been created, you decide what to do with the original hour registration line (the first line in the example).</span></span> <span data-ttu-id="73b13-141">Olduğu gibi tutabilir veya silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="73b13-141">You can keep it as is or delete it.</span></span> 

![Şekil 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a><span data-ttu-id="73b13-143">Tüketim kayıtlarında mali boyutlar</span><span class="sxs-lookup"><span data-stu-id="73b13-143">Financial dimensions on consumption registrations</span></span>

<span data-ttu-id="73b13-144">Tüketim kayıtları yaptığınızda, farklı kayıt türleriyle ilgili mali boyutlar belirli bir dizideki kayıtlara eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-144">When you make consumption registrations, financial dimensions related to the different registration types are added to the registrations in a specific sequence.</span></span> 

- <span data-ttu-id="73b13-145">*Saat ve Gider kayıtları:* Önce, varsa günlük başlığındaki mali boyutlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-145">*Hour and Expense registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="73b13-146">Sonra ilgili iş emri projesindeki mali boyutlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-146">Next, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="73b13-147">Son olarak, kaynaktaki (çalışan) mali boyutlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-147">Finally, financial dimensions from the resource (worker) are added.</span></span>

- <span data-ttu-id="73b13-148">*Madde kayıtları:* Önce, varsa günlük başlığındaki mali boyutlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-148">*Item registrations:* First, financial dimensions from the journal header are added, if any.</span></span> <span data-ttu-id="73b13-149">Ardından ilgili iş emri projesindeki mali boyutlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-149">Then, financial dimensions from the related work order project are added.</span></span> <span data-ttu-id="73b13-150">Bundan sonra, tesisteki mali boyutlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-150">Next, financial dimensions from the site are added.</span></span> <span data-ttu-id="73b13-151">Son olarak, maddedeki mali boyutlar eklenir.</span><span class="sxs-lookup"><span data-stu-id="73b13-151">Finally, financial dimensions from the item are added.</span></span>

>[!NOTE]
><span data-ttu-id="73b13-152">Üç kayıt türü için, mali boyut birleşimi doğrulanır ve geçersiz birleşimler boş bırakılır.</span><span class="sxs-lookup"><span data-stu-id="73b13-152">For all three registration types, the financial dimension combination is validated, and invalid combinations are blanked.</span></span> <span data-ttu-id="73b13-153">Bu, diğer Finance and Operations uygulamalarıyla birlikte standart kurulumdur.</span><span class="sxs-lookup"><span data-stu-id="73b13-153">This is standard setup with other Finance and Operations apps.</span></span>

