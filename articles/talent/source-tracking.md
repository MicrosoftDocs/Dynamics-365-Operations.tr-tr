---
title: Aday profilleri ve başvurular için kaynakları izleme
description: Bu konu, aday profilleri ve uygulamaları için kaynağı izleme hakkında bilgi sağlar.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 5b368e97a716cd1ce4f668c2a97326877a2d3dff
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551899"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a><span data-ttu-id="cc4a3-103">Aday profilleri ve başvurular için kaynakları izleme</span><span class="sxs-lookup"><span data-stu-id="cc4a3-103">Track sources for candidate profiles and applications</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="cc4a3-104">Bu konuda belirtilen işlev önizleme sürümünün bir parçası kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="cc4a3-105">İçerik ve işlevde değişiklik yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="cc4a3-106">Bu özelliği kullanmak için bir yöneticinin Attract içinde **Yönetim ayarları**'nı kullanarak etkinleştirmesini isteyin.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="cc4a3-107">Gelecekteki bir sürüm kaynak izleme raporları sağlayacaktır.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="cc4a3-108">Daha fazla bilgi için bkz [Talent içinde önizleme özelliklerine erişin](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="cc4a3-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="cc4a3-109">Adaylar bir işe başvurduğunda, Attract, otomatik olarak başvurunun kaynağını izler, size işe alma çabanızda yardımcı olacak değerli bilgiler sağlar.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="cc4a3-110">İşe alımcılar ve işe alma yöneticileri de bir adayı el ile bir işe veya yetenek havuzuna eklerken bir başvuru kaynağı seçebilirler.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="cc4a3-111">**Etkinlik** sekmesi altında, başvuru etkinliği ayrıntılarında başvuru kaynağını görüntüleyebilirsiniz ve ayrıca, başvuru geçmişinde yetenek havuzları altında bulunan **Profil** içinde.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="cc4a3-112">Bir adayın profil kaynağını aday ayrıntıları altında **Profil** sekmesinde, her iki başvuru ve yetenek havuzunda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="cc4a3-113">İşlem şablonlarını [Kapsamlı işe alma eklentisinde](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="cc4a3-114">Önceden yapılandırılmış kaynaklar</span><span class="sxs-lookup"><span data-stu-id="cc4a3-114">Pre-configured sources</span></span>

<span data-ttu-id="cc4a3-115">Varsayılan kaynak listesi, genel başvuru kaynaklarını içerir.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-115">The default source list contains common application sources.</span></span> <span data-ttu-id="cc4a3-116">Bazı kaynak türleri, örneğin **İş panosu** veya **Sosyal Ağ** gibi, ek kaynak ayrıntılarına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="cc4a3-117">Örneğin, **Sosyal Ağ**, Facebook ve Twitter'ı içerir.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="cc4a3-118">**Referans** kaynak türü, dahili bir çalışanı referans olarak belirtmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="cc4a3-119">Varsayılan kaynak listesi, aşağıdaki önceden yapılandırılmış kaynakları içerir:</span><span class="sxs-lookup"><span data-stu-id="cc4a3-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="cc4a3-120">Attract kariyer sitesi</span><span class="sxs-lookup"><span data-stu-id="cc4a3-120">Attract career site</span></span>

-   <span data-ttu-id="cc4a3-121">Acente</span><span class="sxs-lookup"><span data-stu-id="cc4a3-121">Agency</span></span>

-   <span data-ttu-id="cc4a3-122">Kariyer Fuarı</span><span class="sxs-lookup"><span data-stu-id="cc4a3-122">Career Fair</span></span>

-   <span data-ttu-id="cc4a3-123">Şirket Pazarlaması</span><span class="sxs-lookup"><span data-stu-id="cc4a3-123">Company Marketing</span></span>

-   <span data-ttu-id="cc4a3-124">Konferanslar ve Fuarlar</span><span class="sxs-lookup"><span data-stu-id="cc4a3-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="cc4a3-125">Profesyonel İlişkilendirme</span><span class="sxs-lookup"><span data-stu-id="cc4a3-125">Professional Association</span></span>

-   <span data-ttu-id="cc4a3-126">İş panosu</span><span class="sxs-lookup"><span data-stu-id="cc4a3-126">Job board</span></span>

    -   <span data-ttu-id="cc4a3-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="cc4a3-127">Indeed</span></span>

    -   <span data-ttu-id="cc4a3-128">Seek</span><span class="sxs-lookup"><span data-stu-id="cc4a3-128">Seek</span></span>

    -   <span data-ttu-id="cc4a3-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="cc4a3-129">CareerBuilder</span></span>

    -   <span data-ttu-id="cc4a3-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="cc4a3-130">Google Jobs</span></span>

    -   <span data-ttu-id="cc4a3-131">Xing</span><span class="sxs-lookup"><span data-stu-id="cc4a3-131">Xing</span></span>

    -   <span data-ttu-id="cc4a3-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="cc4a3-132">Glassdoor</span></span>

    -   <span data-ttu-id="cc4a3-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="cc4a3-133">Monster Jobs</span></span>

-   <span data-ttu-id="cc4a3-134">Dergiler ve Yayınlar</span><span class="sxs-lookup"><span data-stu-id="cc4a3-134">Magazines & Publications</span></span>

-   <span data-ttu-id="cc4a3-135">Sosyal Ağ</span><span class="sxs-lookup"><span data-stu-id="cc4a3-135">Social Network</span></span>

    -   <span data-ttu-id="cc4a3-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="cc4a3-136">Facebook</span></span>

    -   <span data-ttu-id="cc4a3-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="cc4a3-137">Twitter</span></span>

-   <span data-ttu-id="cc4a3-138">Üniversiteden İşe Alma</span><span class="sxs-lookup"><span data-stu-id="cc4a3-138">University Recruiting</span></span>

-   <span data-ttu-id="cc4a3-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="cc4a3-139">LinkedIn</span></span>

-   <span data-ttu-id="cc4a3-140">Seri İlanlar</span><span class="sxs-lookup"><span data-stu-id="cc4a3-140">Classifieds</span></span>

-   <span data-ttu-id="cc4a3-141">Başvuru</span><span class="sxs-lookup"><span data-stu-id="cc4a3-141">Referral</span></span>

-   <span data-ttu-id="cc4a3-142">İşe alımcı tarafından eklendi</span><span class="sxs-lookup"><span data-stu-id="cc4a3-142">Added by Recruiter</span></span>

-   <span data-ttu-id="cc4a3-143">Diğer</span><span class="sxs-lookup"><span data-stu-id="cc4a3-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="cc4a3-144">Kaynak listesini özelleştir</span><span class="sxs-lookup"><span data-stu-id="cc4a3-144">Customize the source list</span></span> 

<span data-ttu-id="cc4a3-145">Kaynak listesini, ek başvuru kaynakları içermek üzere genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="cc4a3-146">Bu listeyi özelleştirmek için, [Attract içinde Seçenek Kümelerini Genişletmek](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract) içindeki talimatları izleyin.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="cc4a3-147">**TalentSource** varlığını, ek kaynakları dahil etmek için düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="cc4a3-148">Kullanıcı arabirimini (UI) olumsuz etkilemekten kaçınmak için aşağıdakilerin **TalentCategory** enum değerlerini (isimleri değil) düzenlemeyi veya silmeyin:</span><span class="sxs-lookup"><span data-stu-id="cc4a3-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="cc4a3-149">**Başvuru**</span><span class="sxs-lookup"><span data-stu-id="cc4a3-149">**Referral**</span></span>
- <span data-ttu-id="cc4a3-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="cc4a3-150">**LinkedIn**</span></span>
- <span data-ttu-id="cc4a3-151">**Diğer**</span><span class="sxs-lookup"><span data-stu-id="cc4a3-151">**Other**</span></span>

<span data-ttu-id="cc4a3-152">Bunun yerine, **TalentSource** enum'u diğer türde kaynaklar eklemek için genişletebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc4a3-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
