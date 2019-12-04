---
title: LinkedIn ile Microsoft Dynamics 365 Talent - Attract tümleştirmesinde sorun giderme
description: Bu konu, Microsoft Dynamics 365 Talent- Attract'ten işleri LinkedIn'de yayınlamaya çalıştığınızda oluşan sorunların nasıl giderileceğini açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 42065f3d6b7ae9e7ad99b26c7692e41f8c36934d
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832989"
---
# <a name="troubleshoot-integration-with-linkedin-and-microsoft-dynamics-365-talent---attract"></a><span data-ttu-id="9d6ac-103">LinkedIn ile Microsoft Dynamics 365 Talent - Attract tümleştirmesinde sorun giderme</span><span class="sxs-lookup"><span data-stu-id="9d6ac-103">Troubleshoot integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d6ac-104">Microsoft Dynamics 365 Talent: Attract'ten LinkedIn'e iş yayınlamaya çalıştığınızda karşılaşabileceğiniz sorunları gidermeye yardımcı olması için aşağıdaki bilgileri kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-104">Use the following information to help troubleshoot issues that you might have when you try to post jobs to LinkedIn from Microsoft Dynamics 365 Talent: Attract.</span></span>

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a><span data-ttu-id="9d6ac-105">Attract'ten LinkedIn'de oturum açamazsınız</span><span class="sxs-lookup"><span data-stu-id="9d6ac-105">You can't sign in to LinkedIn from Attract</span></span>

<span data-ttu-id="9d6ac-106">Attract'ten LinkedIn'de oturum açmada sorun yaşıyorsanız, şu adımları deneyin:</span><span class="sxs-lookup"><span data-stu-id="9d6ac-106">If you're having trouble signing in to LinkedIn from Attract, try these steps:</span></span>

1. <span data-ttu-id="9d6ac-107">Attract içine girmiş olduğunuz LinkedIn kimlik bilgilerinin doğru ve geçerli olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-107">Verify that the LinkedIn credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="9d6ac-108">Kimlik bilgileri geçerli ve doğruysa, [LinkedIn destek](https://www.linkedin.com/help/linkedin) ile iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-108">If the credentials are valid and correct, contact [LinkedIn support](https://www.linkedin.com/help/linkedin).</span></span>
3. <span data-ttu-id="9d6ac-109">Sorun devam ederse, [Microsoft destek](./talent-support.md) ile iletişime geçin.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-109">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a><span data-ttu-id="9d6ac-110">Attract'ten iş postaları LinkedIn'de görünmüyor</span><span class="sxs-lookup"><span data-stu-id="9d6ac-110">Job posts from Attract don't appear on LinkedIn</span></span>

<span data-ttu-id="9d6ac-111">İşiniz 24 saatten sonra LinkedIn'de görünmediyse, aşağıdaki adımları deneyin:</span><span class="sxs-lookup"><span data-stu-id="9d6ac-111">If your job hasn't appeared on LinkedIn after 24 hours, try these steps:</span></span>

1. <span data-ttu-id="9d6ac-112">LinkedIn Şirket kimliğinizin LinkedIn Şirket sayfanıza eşlendiğinden ve Attract yönetim merkezine doğru olarak girildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-112">Make sure that your LinkedIn Company ID maps to your LinkedIn company page and is correctly entered in the Attract Admin center.</span></span> <span data-ttu-id="9d6ac-113">Yönetim merkezinde LinkedIn ayarlarını değiştirme hakkında daha fazla bilgi için bkz. [Microsoft Dynamics 365 Talent - Attract için LinkedIn ile tümleştirmeyi ayarlama](attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="9d6ac-113">For more information about how to change LinkedIn settings in the Admin center, see [Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract](attract-admin-linkedin.md).</span></span> <span data-ttu-id="9d6ac-114">LinkedIn Şirket kimlikleri için daha fazla bilgi için bkz. [LinkedIn Şirket Kimliğinizle LinkedIn İş Panosunu İlişkilendirme - sık sorulan sorular](https://www.linkedin.com/help/linkedin/answer/98972).</span><span class="sxs-lookup"><span data-stu-id="9d6ac-114">For more information about LinkedIn Company IDs, see [Associating your LinkedIn Company ID with the LinkedIn Job Board - Frequently Asked Questions](https://www.linkedin.com/help/linkedin/answer/98972).</span></span>
2. <span data-ttu-id="9d6ac-115">Adresin eksiksiz olduğundan emin olmak için LinkedIn ile ilgili iş ayrıntılarını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-115">Check the job details on LinkedIn to make sure that the address is complete.</span></span> <span data-ttu-id="9d6ac-116">LinkedIn'in bir işi başarıyla deftere nakletmek için, en azından işin şehir ve ülkesine veya bölgesine ihtiyacı vardır.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-116">To post a job successfully, LinkedIn needs at least the city and country or region of the job.</span></span>
3. <span data-ttu-id="9d6ac-117">İşin LinkedIn'de deftere nakledilen başka bir işi çoğaltmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-117">Make sure that the job doesn't duplicate another job that has been posted on LinkedIn.</span></span> <span data-ttu-id="9d6ac-118">LinkedIn, LinkedIn Premium İş yuvalarının çoğaltmaları veya başka bir kaynaktan sınırlı listeleme olan işleri deftere nakletmez.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-118">LinkedIn won't post jobs that are duplicates of either LinkedIn Premium Job Slots or Limited Listings from another source.</span></span> <span data-ttu-id="9d6ac-119">Şirketinizdeki başka bir kişinin işi henüz el ile deftere nakletmemiş olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-119">Verify that another person at your company didn't already post the job manually.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d6ac-120">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="9d6ac-120">See also</span></span>

[<span data-ttu-id="9d6ac-121">LinkedIn SSS ile Attract tümleştirme</span><span class="sxs-lookup"><span data-stu-id="9d6ac-121">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="9d6ac-122">Microsoft Dynamics 365 Talent - Attract'ten LinkedIn'e iş yayınlama</span><span class="sxs-lookup"><span data-stu-id="9d6ac-122">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="9d6ac-123">Microsoft Dynamics 365 Talent - Attract'te LinkedIn Recruiter ile aday kaynağı bulma</span><span class="sxs-lookup"><span data-stu-id="9d6ac-123">Source candidates with LinkedIn Recruiter in Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-linkedin-recruiter.md)

[<span data-ttu-id="9d6ac-124">Attract'te iş oluşturma, onaylama ve yayımlama</span><span class="sxs-lookup"><span data-stu-id="9d6ac-124">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="9d6ac-125">LinkedIn ve Microsoft Dynamics 365 Talent - Attract ile tümleştirmede sorun giderme</span><span class="sxs-lookup"><span data-stu-id="9d6ac-125">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
