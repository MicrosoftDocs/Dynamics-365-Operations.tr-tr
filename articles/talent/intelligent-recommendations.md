---
title: Akıllı öneriler
description: Bu konu, makine öğreniminin işler ve iş adayları konusunda öneriler sağlamak için nasıl kullanılabileceğini açıklar.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "306587"
---
# <a name="intelligent-recommendations"></a><span data-ttu-id="a53d4-103">Akıllı öneriler</span><span class="sxs-lookup"><span data-stu-id="a53d4-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a53d4-104">Makine öğrenimi, işe alanlar ve işe alım yöneticilerinin bir pozisyon için üst adayları hızlı bir şekilde tanımlamasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a53d4-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="a53d4-105">Adayların ilgi alanları ve profiline en uygun pozisyonu bulmakta da yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a53d4-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="a53d4-106">Bu özellikler kullanılır ve geribildirim sağlanırsa öneriler artar.</span><span class="sxs-lookup"><span data-stu-id="a53d4-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="a53d4-107">Akıllı öneri özellikleri, yalnızca Kapsamlı işe alım eklentisinde kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a53d4-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="a53d4-108">Aday ve iş önerisi özelliklerini etkinleştirmek için yöneticinin bunlar için önizleme seçeneklerini açması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a53d4-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="a53d4-109">Yönetim merkezi içinde **Özellik yönetimi** sekmesinde, **Önizleme özellikleri** seçeneğinin **Açık** olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a53d4-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="a53d4-110">Ardından tek tek **Aday önerisi** ve **İş önerisi** seçeneklerinin **Açık** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="a53d4-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="a53d4-111">Aday önerileri</span><span class="sxs-lookup"><span data-stu-id="a53d4-111">Candidate recommendations</span></span>

<span data-ttu-id="a53d4-112">İş gönderileri yüzlerce başvuran çekebileceği için, yetenekleri ve özgeçmişi pozisyona uyan adayları bulmak işverenler ve işe alma müdürleri için zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="a53d4-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="a53d4-113">İş açıklaması ve gereksinimleri arasındaki ilişkiyi, adayların özgeçmiş ve profillerindeki verileri analiz ederek makine öğrenimi aday önerileri üretmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="a53d4-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="a53d4-114">Aday önerileri, iş verenlerin ve işe alma müdürlerinin üst becerileri tanımlayıp daha hızlı görüşme aşamasına taşımaya yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a53d4-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="a53d4-115">Özgeçmiş veya tam profili olan ondan fazla aday veya müşteri adayı olan her iş için, işin gerekliliklerine en yakın adaylar veya müşteri adayları **İş** sayfasının **Dikkate alınacak başvuranlar** bölüm üzerinde görünür.</span><span class="sxs-lookup"><span data-stu-id="a53d4-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="a53d4-116">Her türlü önerilen aday için aday kartındaki **Adayı görüntüle**'yi seçip adayın profilini gözden geçirebilir ve başvurusu üzerinde işlem gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a53d4-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="a53d4-117">Üç nokta düğmesini (**...**) kullanarak adayın profilini yeni bir sekmede açın. Öneri hakkında geribildirim sağlamak için de üç nokta düğmesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a53d4-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="a53d4-118">Bu şekilde, öneri altyapısının ince ayarlarını yapın ve gelecekteki önerileri geliştirin.</span><span class="sxs-lookup"><span data-stu-id="a53d4-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="a53d4-119">Sevmediğiniz öneriler **İş sayfasını** yenileyicne **Dikkate alınacak başvuranlar** bölümünden kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="a53d4-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="a53d4-120">Geribildirim kartını neden öneriyi faydalı bulmadığınızı belirtmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a53d4-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="a53d4-121">İş önerileri</span><span class="sxs-lookup"><span data-stu-id="a53d4-121">Job recommendations</span></span> 

<span data-ttu-id="a53d4-122">Aday personel, işe başvurmak için kariyer sitesi kullandığında kurumdaki diğer açık pozisyonlar tavsiye edilir.</span><span class="sxs-lookup"><span data-stu-id="a53d4-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="a53d4-123">Bu öneriler adayın eski başvurularına ve özgeçmiş veya aday profilini temel alır.</span><span class="sxs-lookup"><span data-stu-id="a53d4-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="a53d4-124">Bu nedenle, iş önerileri aday müşterilerin en iyi uyan işleri hızlı bir şekilde tanımasına yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="a53d4-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="a53d4-125">İş önerileri, kariyer sitesine ondan fazla iş yayınlanırsa sağlanır.</span><span class="sxs-lookup"><span data-stu-id="a53d4-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="a53d4-126">Aday müşteriler öneri kartından iş gönderisinin ayrıntılarını açabilir.</span><span class="sxs-lookup"><span data-stu-id="a53d4-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="a53d4-127">Gelecekteki öneriler, geliştirmek için bir öneri hakkında geribildirim de sağlayabilir.</span><span class="sxs-lookup"><span data-stu-id="a53d4-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>
