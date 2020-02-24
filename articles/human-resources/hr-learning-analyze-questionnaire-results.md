---
title: Soru formu sonuçlarını analiz etme
description: Soru formu istatistikleri, ortalamalar, toplamlar ve demografik veri kümesine göre yüzdeler hesaplamak için kullanılabilir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3b13ef7eda9943af35bbb37e3059dd81aa6365
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010908"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="cb83c-103">Soru formu sonuçlarını analiz etme</span><span class="sxs-lookup"><span data-stu-id="cb83c-103">Analyzing questionnaire results</span></span>



<span data-ttu-id="cb83c-104">Soru formu istatistikleri, ortalamalar, toplamlar ve demografik veri kümesine göre yüzdeler hesaplamak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cb83c-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="cb83c-105">Bu yordamı başlatmak için Soru formu > Sonuçları görüntüle ve analiz et > Soru formu istatistikleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="cb83c-106">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="cb83c-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="cb83c-107">Soru formu istatistik kaydı yaratın</span><span class="sxs-lookup"><span data-stu-id="cb83c-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="cb83c-108">Soru formu istatistikleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="cb83c-109">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-109">Click New.</span></span>
3. <span data-ttu-id="cb83c-110">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="cb83c-111">İstatistikler alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="cb83c-112">Tanım alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="cb83c-113">Soru formu alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cb83c-114">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cb83c-115">Genel sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-115">Click the General tab.</span></span>
    * <span data-ttu-id="cb83c-116">Anonim sonuçlar veya çalışanların, tüm kişilerden veya başvuranların sonuçlarını dahil etmek isteyip istemediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="cb83c-117">Çalışan onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="cb83c-118">Sonuçları kıdem veya yaşa göre görüntüleyecekseniz, bu gruplama sonuçları için kullanacağınız aralıkları belirleyin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="cb83c-119">Bir yaş aralığı grubuna 5 girmek, sonuçları beş yıllık aralıklarda gruplayacaktır.</span><span class="sxs-lookup"><span data-stu-id="cb83c-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="cb83c-120">Yaş alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="cb83c-121">Hesaplamayı tüm soru formuna karşı mı yoksa her bir sonuç grubuna, her bir soruya ya da her bir soru satırına karşı mı yapmak istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="cb83c-122">Sonuçları nasıl gruplandırmak istediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="cb83c-123">Örneğin, soru başına ortalama puanı hesaplarsanız, sonuç grubuna göre gruplandırılmış soruları görmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb83c-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="cb83c-124">Hesaplamayı dayandırmak istediğiniz temel veriyi seçin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="cb83c-125">Örneğin, çalışanlarınız arasında soru formunda kaznaılan ortalama yüzdeyi, çalışanlarınız arasında kazanılan ortalama puana göre görmek istiyorsanız.</span><span class="sxs-lookup"><span data-stu-id="cb83c-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="cb83c-126">Aralık sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-126">Click the Range tab.</span></span>
    * <span data-ttu-id="cb83c-127">Sonuç kümesini yalnızca aralık ölçütlerine uyanlarla kısıtlamak için aralıkları kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="cb83c-128">Gruplandırma tarafından sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="cb83c-129">Sonuçlarının nasıl görüntüleneceğini belirlemek için gruplandırmaları kullanın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="cb83c-130">Örneğin sonuçları önce cinsiyet sonra da yaşa göre gruplayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="cb83c-131">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cb83c-132">Gruplandırmaları seçili tarafa taşıyın ve istediğiniz sırada yerleştirin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="cb83c-133">İstatistik hesaplamalarını çalıştırma</span><span class="sxs-lookup"><span data-stu-id="cb83c-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="cb83c-134">Yürüt'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-134">Click Execute.</span></span>
    * <span data-ttu-id="cb83c-135">Sonuçların üzerinde gerçekleştirmek istediğiniz hesaplama işlevini seçin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="cb83c-136">Örneğin seçili gruplamalar için soru formları arasında ortalama yüzdeyi hesaplamak veya seçili gruplamalar arasında toplam puanları hesaplamak için.</span><span class="sxs-lookup"><span data-stu-id="cb83c-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="cb83c-137">Önceki aramaları sil onay kutusunu işaretleyin veya işareti kaldırın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="cb83c-138">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="cb83c-139">Soru formu istatistiklerinin çalıştırma sonucunu görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="cb83c-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="cb83c-140">Sonuçlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-140">Click Result.</span></span>
2. <span data-ttu-id="cb83c-141">Sonuçlar'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-141">Click Result.</span></span>
3. <span data-ttu-id="cb83c-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="cb83c-142">Close the page.</span></span>

