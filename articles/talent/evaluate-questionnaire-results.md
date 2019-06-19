---
title: Soru formlarının sonuçlarını görüntüleme ve değerlendirme
description: Bu konu yanıtlayanların tamamladığı anketlerin sonuçlarını nasıl görüntüleyeceğinizi ve değerlendireceğinizi açıklar.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 38b694b6dd4b1b9a198452e409bd64d7934b4685
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1519342"
---
# <a name="view-and-evaluate-the-results-of-questionnaires"></a><span data-ttu-id="929e0-103">Soru formlarının sonuçlarını görüntüleme ve değerlendirme</span><span class="sxs-lookup"><span data-stu-id="929e0-103">View and evaluate the results of questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="929e0-104">Bu konu yanıtlayanların tamamladığı anketlerin sonuçlarını nasıl görüntüleyeceğinizi ve değerlendireceğinizi açıklar.</span><span class="sxs-lookup"><span data-stu-id="929e0-104">This topic explains how you can view and evaluate the results of questionnaires that respondents complete.</span></span> 

<span data-ttu-id="929e0-105">Yanıtlayanlar bir anketi tamamladıktan sonra, anket sonuçlarını aşağıdaki yollardan görüntüleyebilir ve değerlendirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="929e0-105">After respondents complete a questionnaire, you can view and evaluate the questionnaire results in the following ways:</span></span>

-   <span data-ttu-id="929e0-106">**Tamamlanan yanıt oturumları** – Yanıtlayanların tamamladığı anketler hakkındaki ayrıntıları görüntüleyin ve yanıtları ve kazanılan puanları özetleyen raporlar üretin.</span><span class="sxs-lookup"><span data-stu-id="929e0-106">**Completed answer sessions** – View details about the questionnaires that respondents have completed, and generate reports to summarize answers and any points that were earned.</span></span>
-   <span data-ttu-id="929e0-107">**Sonuç grupları** – Anketler için sonuç grubu detayları ve istatistiklerini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="929e0-107">**Result groups** – View result group details and statistics for questionnaires.</span></span> <span data-ttu-id="929e0-108">Sonuç grubu istatistikleri ya bir anketin tek bir yanıt oturumu veya tüm yanıt oturumları için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="929e0-108">Result group statistics can be generated for either a single answer session  of a questionnaire or all answer sessions.</span></span>
-   <span data-ttu-id="929e0-109">**Anket istatistikleri** – Belirli bir yanıtlayan grubu için istatistik hesaplamak için ölçütleri belirleyin.</span><span class="sxs-lookup"><span data-stu-id="929e0-109">**Questionnaire statistics** – Specify criteria to calculate statistics for a specific group of respondents.</span></span>

<span data-ttu-id="929e0-110">Ayrıca kişi, yanıt oturumu veya sonuç grubuna göre sıralanmış sonuçları görüntülemek için çeşitli raporlar oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-110">You can also generate various reports to view results that are sorted by person, answer session, or result group.</span></span> <span data-ttu-id="929e0-111">Tamamlanmış anketlerle ilgili aşağıdaki raporlar kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="929e0-111">The following reports that are related to completed questionnaires are available:</span></span>

-   <span data-ttu-id="929e0-112">Yanıtlar</span><span class="sxs-lookup"><span data-stu-id="929e0-112">Answers</span></span>
-   <span data-ttu-id="929e0-113">Soru formu başına yanıt sayısı</span><span class="sxs-lookup"><span data-stu-id="929e0-113">Answers per questionnaire</span></span>
-   <span data-ttu-id="929e0-114">Kişi başına yanıt sayısı</span><span class="sxs-lookup"><span data-stu-id="929e0-114">Answers per person</span></span>
-   <span data-ttu-id="929e0-115">Geribildirim analizi</span><span class="sxs-lookup"><span data-stu-id="929e0-115">Feedback analysis</span></span>

## <a name="answer-session-results"></a><span data-ttu-id="929e0-116">Yanıt oturumu sonuçları</span><span class="sxs-lookup"><span data-stu-id="929e0-116">Answer session results</span></span>
<span data-ttu-id="929e0-117">Yanıtlayanlar bir anketi tamamladıktan sonra, tamamlanan yanıt oturumlarının sonuçlarını görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-117">After respondents complete a questionnaire, you can view the results of the completed answer sessions.</span></span> <span data-ttu-id="929e0-118">Bir yanıt oturumu kullanıcının bir ankete yanıtıdır.</span><span class="sxs-lookup"><span data-stu-id="929e0-118">An answer session is one user’s response to a questionnaire.</span></span> <span data-ttu-id="929e0-119">Tamamlanmış yanıt oturumları hakkındaki ayrıntıları **Yanıtlar** sayfasında görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-119">You can view details about completed answer sessions on the **Answers** page.</span></span> <span data-ttu-id="929e0-120"> **Yanıtlar** sayfasına dahil edilen yanıt oturumları sayfayı nasıl açtığınıza bağlı olarak çeşitli yollarla filtrelenir:</span><span class="sxs-lookup"><span data-stu-id="929e0-120">The answer sessions that are included on the **Answers** page are filtered in various ways, depending on how you open the page:</span></span>

-   <span data-ttu-id="929e0-121">Tüm anketler</span><span class="sxs-lookup"><span data-stu-id="929e0-121">All questionnaires</span></span>
-   <span data-ttu-id="929e0-122">Belirli bir anket</span><span class="sxs-lookup"><span data-stu-id="929e0-122">A specific questionnaire</span></span>
-   <span data-ttu-id="929e0-123">Belirli bir kişi</span><span class="sxs-lookup"><span data-stu-id="929e0-123">A specific person</span></span>

<span data-ttu-id="929e0-124">**Yanıtlar** sayfasından, yanıtlar hakkındaki ayrıntıları, kazanılan puanları, bir yanıtlayanın her yanıt grubundaki yanıtlarını ve eğer bir soru hiyerarşisi kullanıldıysa, seçili ankette kullanılan soru hiyerarşisini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-124">From the **Answers** page, you can view details about answers, points that were earned, a respondent’s responses in each result group, and the question hierarchy that was used on the selected questionnaire, if a question hierarchy was used.</span></span> <span data-ttu-id="929e0-125">Ayrıca aşağıdaki raporları oluşturabilir ve yazdırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="929e0-125">You can also generate and print the following reports:</span></span>

-   <span data-ttu-id="929e0-126">**Sonuç raporu** – Bu rapor, seçili yanıt oturumu için sonuç grubu başına kazanılan puanların grafik gösterimini gösterir.</span><span class="sxs-lookup"><span data-stu-id="929e0-126">**Results report** – This report shows a graphical representation of the points that were earned per result group for the selected answer session.</span></span>
-   <span data-ttu-id="929e0-127">**Yanıt raporu** – Bu rapor, anketteki her soru için yanıtlayanın seçtiği cevapları gösterir.</span><span class="sxs-lookup"><span data-stu-id="929e0-127">**Answer report** – This report shows the answers that the respondent selected for each question on the questionnaire.</span></span>
-   <span data-ttu-id="929e0-128">**Yanlış yanıtlar** – Bu rapor yanıtlayanın seçtiği yanlış yanıtlarla ilgili bilgileri gösterir.</span><span class="sxs-lookup"><span data-stu-id="929e0-128">**Incorrect answers** – This report shows information that is related to the incorrect answers that the respondent selected.</span></span>

<span data-ttu-id="929e0-129">**Not:** **Sonuçlar** raporu, yalnızca anketteki sonuç gruplarını kullanıyorsanız ve **Anketler** sayfasındaki **Sonuçlar sayfasını** seçtiyseniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="929e0-129">**Note:** The **Results** report is available only if you use results groups on the questionnaire, and if you selected **Results page** on the **Questionnaires** page.</span></span> <span data-ttu-id="929e0-130">**Yanıt** raporu ve **Yanlış yanıtlar** raporu yalnızca **Anketler** sayfasındaki **Yanıt raporu** seçeneğini seçtiyseniz kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="929e0-130">The **Answer** report and the **Incorrect answers** report are available only if you selected **Answer report** on the **Questionnaires** page.</span></span>

## <a name="questionnaire-statistics"></a><span data-ttu-id="929e0-131">Soru formu istatistikleri</span><span class="sxs-lookup"><span data-stu-id="929e0-131">Questionnaire statistics</span></span>
<span data-ttu-id="929e0-132">Tamamlanmış bir anketin sonuçlarını tanımladığınız hesaplamalara göre analiz etmek için anket istatistiklerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-132">You can use questionnaire statistics to analyze the results of a completed questionnaire, based on calculations that you define.</span></span> <span data-ttu-id="929e0-133">Hesaplamaları tanımlamak için, aşağıdaki görevleri tamamlamalısınız:</span><span class="sxs-lookup"><span data-stu-id="929e0-133">To define calculations, you must complete the following tasks:</span></span>

-   <span data-ttu-id="929e0-134">İstatistikleri hesaplamak ve görüntülemek için ölçüt seçin.</span><span class="sxs-lookup"><span data-stu-id="929e0-134">Select criteria to calculate and display the statistics.</span></span>
    -   <span data-ttu-id="929e0-135">Anket, sorular, soru satırları veya sonuç gruplarına göre istatistikleri görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-135">You can show statistics by questionnaire, questions, question rows, or results groups.</span></span>
    -   <span data-ttu-id="929e0-136">Sonuçları görüntülerken kullanılacak grafik türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="929e0-136">Select the type of chart that will be used when you view results.</span></span>
    -   <span data-ttu-id="929e0-137">Yanıtları dahil etmek için ağdan, çalışanlar, iletişim kişileri veya başvuranlar gibi kişi türlerini seçin.</span><span class="sxs-lookup"><span data-stu-id="929e0-137">Select the types of people from the network, such as employees, contact persons, or applicants, to include answers for.</span></span> <span data-ttu-id="929e0-138">Aynı zamanda anonim olarak tamamlanmış anketlerden yanıtları dahil edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-138">You can also include answers from questionnaires that were completed anonymously.</span></span>
    -   <span data-ttu-id="929e0-139">Sonuçları analiz etmek için yaş veya kıdeme dayanan aralıklar ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="929e0-139">Set up intervals that are based on age or seniority to analyze results.</span></span>
-   <span data-ttu-id="929e0-140">İstatistiklerin konusunu yenileyen ayarları seçin veya doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="929e0-140">Select or verify settings that refine the subject of the statistics.</span></span> <span data-ttu-id="929e0-141">Örneğin, bir posta kodu seçerek belirli bir coğrafi bölge içindeki tüm yanıtlayanlar için sonuçları analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-141">For example, by selecting a ZIP Code or postal code, you can analyze results for all respondents within a specific geographic area.</span></span>
-   <span data-ttu-id="929e0-142">Yanıtlayan veya anket özelliklerine göre sonuçları analiz etmek için ölçütleri seçin veya doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="929e0-142">Select or verify criteria to analyze results by respondent or questionnaire characteristics.</span></span> <span data-ttu-id="929e0-143">Örneğin, **Posta kodu**, seçeneğini seçerek, yanıtlayanın konumu ve doğru yanıtlar arasındaki korelasyonu analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="929e0-143">For example, by selecting **ZIP/postal code**, you can analyze the correlation between a respondent’s location and correct answers.</span></span>

<span data-ttu-id="929e0-144">Tanımladığınız ayarlar kaydedilir ve sonuçları yeniden hesaplamak için periyodik olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="929e0-144">The settings that you define are saved and can be used to periodically recalculate results.</span></span>

<a name="additional-resources"></a><span data-ttu-id="929e0-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="929e0-145">Additional resources</span></span>
--------

[<span data-ttu-id="929e0-146">Soru formları tasarlama</span><span class="sxs-lookup"><span data-stu-id="929e0-146">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="929e0-147">Soru formlarını kullanma</span><span class="sxs-lookup"><span data-stu-id="929e0-147">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="929e0-148">Soru formlarını dağıtma ve tamamlama</span><span class="sxs-lookup"><span data-stu-id="929e0-148">Distributing and completing questionnaires</span></span>](distribute-questionnaires.md)

