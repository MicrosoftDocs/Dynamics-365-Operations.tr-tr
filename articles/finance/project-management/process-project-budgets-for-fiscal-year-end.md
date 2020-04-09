---
title: Proje bütçelerini mali yıl bitişinde transfer etme
description: Bu makalede, kalan Bütçe tutarlarının gelecekteki yıllara nasıl aktarılacağı ve bütçe kayıt ayrıntılarının nasıl oluşturulacağı hakkında bir bilgi verilir.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172342"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="a4ac6-103">Proje bütçelerini mali yıl bitişinde transfer etme</span><span class="sxs-lookup"><span data-stu-id="a4ac6-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4ac6-104">Çok yıllık bir projede çalışırken, mali yılın sonunda bütçe kalan bütçesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="a4ac6-105">Kalan bütçe tutarlarını, gelecekteki bir yıla transfer edebilir ve ilgili genel muhasebe hesaplarındaki tutarlar için bütçe kaydı ayrıntılarını oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="a4ac6-106">Kalan tutarları ileriye almadan önce kalan bütçe tutarlarını gözden geçirip analiz edin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="a4ac6-107">Kalan bütçe tutarlarını İncele ve analiz et</span><span class="sxs-lookup"><span data-stu-id="a4ac6-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="a4ac6-108">Projelere ait yıl sonu bütçe tutarlarını gözden geçirmek için aşağıdaki adımları tamamlayın, ancak tutarları ileriye doğru taşımaz.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="a4ac6-109">**Proje Yönetimi ve muhasebe** > **periyodik** > **bütçeler** > **bütçeleriileri taşı**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="a4ac6-110">**Proje bütçesi taşıması ileriye doğru işlem** sayfasında, **yıl sonu seçenekleri** sekmesinde, **Kalan Proje Bütçe tutarlarını ilet** etkin olmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="a4ac6-111">**Parametreler** sekmesinde, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yılı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="a4ac6-112">**Mali yılı açma** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yılı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="a4ac6-113">**İlk tahmin modeli** alanında, **kalan bütçeyi** seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="a4ac6-114">Seçtiğiniz ölçütlere uyan ve kalan bütçeyi içermeyen projeleri dahil etmek için, **Kalan sıfır göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="a4ac6-115">**Bütçe Seç** sekmesinde, seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **tüm bütçeleri al**'ı seçin ve ardından **İşle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="a4ac6-116">Belirli bir bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçilen bütçeleri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="a4ac6-117">Bölmedeki belirli bir satırla ilgili daha fazla bilgi için, satırı seçin ve **Bütçe ayrıntılarını görüntüle** veya **Firmaları görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="a4ac6-118">Kalan bütçesi tutarlarını devret</span><span class="sxs-lookup"><span data-stu-id="a4ac6-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="a4ac6-119">Kalan bütçe tutarlarını işleseniz, genel muhasebede, ilettiğiniz tutarlar için hareketler oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="a4ac6-120">Genel muhasebe hareketleri oluşturmak için [bütçe tutarlarını ileriye taşı ve genel muhasebe hareketleri oluştur](#carry-forward) bölümdeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="a4ac6-121">İleriye doğru gerçekleştirilen bütçe tutarları **tahmin modelleri** sayfasında, ileri sarma tahmin modeli olarak seçilen tahmin modeline transfer edilir.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="a4ac6-122">Bütçe tutarlarını ileri sar ve genel muhasebe hareketleri oluştur</span><span class="sxs-lookup"><span data-stu-id="a4ac6-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="a4ac6-123">**Proje Yönetimi ve muhasebe** > **periyodik** > **bütçeler** > **bütçeleriileri taşı**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="a4ac6-124">**Proje bütçesi devam ediyor-ileri işlem** sayfasında **yıl sonu** seçeneğini belirleyin ve sonra da **genel muhasebede kalan proje bütçe tutarlarını ileri sar** ve **bütçe kayıt girişleri oluştur** seçeneğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="a4ac6-125">**Parametreler** sekmesinde, **proje parametreleri** alan grubunda aşağıdakileri seçin:</span><span class="sxs-lookup"><span data-stu-id="a4ac6-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="a4ac6-126">**Proje bütçe yılı**:Kalan bütçe tutarlarını görüntülemek istediğiniz mali yılı başını seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="a4ac6-127">**Kar ve zarar**: Genel muhasebede kar ve zarar hareketleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="a4ac6-128">**Süren iş**: Süren İş (WIP) hareketlerini genel muhasebede oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="a4ac6-129">**Bordro**: Genel muhasebede Bordro tahsisatı hareketleri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="a4ac6-130">**Genel muhasebe** alanı grubunda aşağıdaki bilgileri sağlayın:</span><span class="sxs-lookup"><span data-stu-id="a4ac6-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="a4ac6-131">**Mali yılı açma** alanında, kalan bütçe tutarlarını aktarmak istediğiniz projeler için mali yılı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="a4ac6-132">Varsayılan değer, **proje bütçe yılı** alanındaki değerden sonraki bir yılla yapılır.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="a4ac6-133">**Hareket-ileri dönemi** alanında, genel muhasebede bütçe kaydı ayrıntılarını oluşturmak istediğiniz dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="a4ac6-134">Bu, genellikle açılış mali yıldaki ilk dönemdir.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="a4ac6-135">**Şuradan/Şuraya kopyala** alanı grubunda aşağıdaki bilgileri sağlayın:</span><span class="sxs-lookup"><span data-stu-id="a4ac6-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="a4ac6-136">**İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarıyla ilişkili proje bütçe tahmin modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="a4ac6-137">**Muhasebe bütçe modeline** alanında, genel muhasebeye aktarmak istediğiniz bütçe tutarlarıyla ilişkili öuhasebe bütçe tahmin modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="a4ac6-138">Projelere ait bütçe tutarlarını transfer ettiğinizde oluşturulan genel muhasebe hareketleri için projenin satış para birimini kullanmak üzere **transfer satış para birimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="a4ac6-139">Bu seçenek işaretli değilse, hareketler muhasebe para birimini kullanır.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="a4ac6-140">Kalan bütçe tutarları olmayan projeleri dahil etmek için **Kalan sıfır göster**'i seçin, ancak alt bölmede görüntülenen projelerde seçtiğiniz diğer ölçütleri karşılayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="a4ac6-141">**Bütçe Seç** sekmesinde, seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **tüm bütçeleri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="a4ac6-142">Belirli bir proje bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak isterseniz, **Seçilen bütçeleri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="a4ac6-143">İşlemek istediğiniz her proje için, projenin satır başındaki seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="a4ac6-144">Projelerin tümünü veya bir çoğunu seçmek için, sol üst köşedeki onay işaretini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="a4ac6-145">Herhangi bir projenin işlenmesini hariç tutmak için projenin onay işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="a4ac6-146">Seçili projeler için kalan bütçe tutarlarını seçili mali yıla aktarmak ve genel muhasebede bütçe kayıt ayrıntıları oluşturmak için, **işlem** seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="a4ac6-147">Genel muhasebe hareketleri oluşturmadan bütçe tutarlarını ileri sar</span><span class="sxs-lookup"><span data-stu-id="a4ac6-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="a4ac6-148">**Proje Yönetimi ve muhasebe** > **periyodik** > **bütçeler** > **bütçeleriileri taşı**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="a4ac6-149">**Proje bütçesi taşıması ileriye doğru işlem** sayfasında, **yıl sonu seçenekleri** alanında, **Kalan Proje Bütçe tutarlarını ilet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="a4ac6-150">**Parametreler** grubunda, **proje bütçe yılı** alanında, kalan bütçe tutarını görüntülemek istediğiniz mali yılı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="a4ac6-151">**Şuradan/Şuraya kopyala** grubunda aşağıdaki bilgileri sağlayın:</span><span class="sxs-lookup"><span data-stu-id="a4ac6-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="a4ac6-152">**İlk tahmin modeli** alanında, projeler için transfer etmek istediğiniz kalan bütçe tutarlarıyla ilişkili proje bütçe tahmin modelini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="a4ac6-153">Seçtiğiniz ölçütlere uyan ve kalan bütçeyi içermeyen projeleri dahil etmek için, **Kalan sıfır göster**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="a4ac6-154">**Bütçe Seç** grubunda, seçilen ölçütünüze uyan tüm bütçeleri yüklemek için **tüm bütçeleri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="a4ac6-155">Belirli bir proje bütçe kümesini bölmeye yükleyen bir veritabanı sorgusu tasarlamak için, **Seçilen bütçeleri al**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="a4ac6-156">İşlemek istediğiniz her proje için, projenin satır başındaki seçeneği belirleyin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="a4ac6-157">Seçili **projeler** için kalan Bütçe tutarlarının seçili mali yıla aktarılması işlemini seçin.</span><span class="sxs-lookup"><span data-stu-id="a4ac6-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

