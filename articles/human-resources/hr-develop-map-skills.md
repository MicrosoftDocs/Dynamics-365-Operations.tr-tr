---
title: Becerileri eşleştirme
description: Dynamics 365 Human Resources'de nitelikli bir kişi bulmak için yetenek eşleme araması oluşturabilirsiniz.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076619"
---
# <a name="map-skills"></a><span data-ttu-id="42593-103">Becerileri eşleştirme</span><span class="sxs-lookup"><span data-stu-id="42593-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="42593-104">Dynamics 365 Human Resources'de nitelikli bir kişi bulmak için yetenek eşleme araması oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42593-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="42593-105">Yetenek eşleme aramaları aşağıdaki bilgileri arayarak girdiğiniz ölçütlere göre sonuçları döndürür:</span><span class="sxs-lookup"><span data-stu-id="42593-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="42593-106">Yetenekler</span><span class="sxs-lookup"><span data-stu-id="42593-106">Skills</span></span>
- <span data-ttu-id="42593-107">Eğitim</span><span class="sxs-lookup"><span data-stu-id="42593-107">Education</span></span>
- <span data-ttu-id="42593-108">Sertifikalar</span><span class="sxs-lookup"><span data-stu-id="42593-108">Certificates</span></span>
- <span data-ttu-id="42593-109">Pozisyonlar</span><span class="sxs-lookup"><span data-stu-id="42593-109">Positions</span></span>
- <span data-ttu-id="42593-110">Proje deneyimi</span><span class="sxs-lookup"><span data-stu-id="42593-110">Project experience</span></span>

<span data-ttu-id="42593-111">Örneğin, CPA kazandıkları kişileri kuruluşunuzda bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42593-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="42593-112">Yetenek eşleştirme profilleri, iş gereksinimlerine doğrudan karşılık gelen nitelikleri taşıyan mevcut çalışanları veya adayları bulmanıza olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="42593-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="42593-113">Yalnızca yetenek eşleme aramalarına eklenmek üzere seçilen çalışanlar, başvuranlar ve ilgili kişiler bir yetenek eşleme sonuçları listesinde görüntülenebilir ya da yetenek profiline eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="42593-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="42593-114">Yetenek eşleme aramalarına bir kişi eklemek için **Yetenek eşlemeye dahil et** seçimini aşağıdaki sayfalarda **Evet** olarak ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="42593-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="42593-115">Çalışan</span><span class="sxs-lookup"><span data-stu-id="42593-115">Worker</span></span><br>
> - <span data-ttu-id="42593-116">Personel</span><span class="sxs-lookup"><span data-stu-id="42593-116">Employee</span></span><br>
> - <span data-ttu-id="42593-117">Başvuran</span><span class="sxs-lookup"><span data-stu-id="42593-117">Applicant</span></span><br>
> - <span data-ttu-id="42593-118">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="42593-118">Contacts</span></span><br>

<span data-ttu-id="42593-119">Yetenek eşleme oluşturmak için **çalışan geliştirme > bağlantılar > Bceri eşleme** gidin.</span><span class="sxs-lookup"><span data-stu-id="42593-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="42593-120">Yetenek eşleme profili oluşturmak için **çalışan geliştirme > bağlantılar > Bceri eşleme profilleri** gidin.</span><span class="sxs-lookup"><span data-stu-id="42593-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="42593-121"> Yetenek eksikliği analizi ve yetenek profili analizi</span><span class="sxs-lookup"><span data-stu-id="42593-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="42593-122">Bir kişinin yetki listesini görüntülemek için yetenek profili Analizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42593-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="42593-123">Bir kişinin yeteneklerini ve bir iş için gereken yetenekleri karşılaştırmak için bir yetenek eksikliği analizi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="42593-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="42593-124">Bir boşluk Analizi oluşturmak için, **çalışan geliştirme > bağlantılar > yetenek boşluk Analizi - kişi** gidin.</span><span class="sxs-lookup"><span data-stu-id="42593-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="42593-125">Yetenek profili analizi oluşturmak için **çalışan geliştirme > bağlantılar > Bceri profili analizi** gidin.</span><span class="sxs-lookup"><span data-stu-id="42593-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="42593-126">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="42593-126">See also</span></span>

[<span data-ttu-id="42593-127">Yetenekleri konfigüre et</span><span class="sxs-lookup"><span data-stu-id="42593-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="42593-128">Yetenekleri girin</span><span class="sxs-lookup"><span data-stu-id="42593-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]