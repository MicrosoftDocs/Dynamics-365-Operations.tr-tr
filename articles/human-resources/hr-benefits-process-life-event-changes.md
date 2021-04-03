---
title: Ömür olayı değişikliklerini işle
description: Ömür olayı değişiklikleri için Microsoft Dynamics 365 Human Resources'ta ömür olayı değişikliklerini işleyin.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2726dcb3c847c9af2a431358de04a27341b9e66c
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464262"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="7aad4-103">Ömür olayı değişikliklerini işle</span><span class="sxs-lookup"><span data-stu-id="7aad4-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7aad4-104">Ömür olayı değişiklikleri için Microsoft Dynamics 365 Human Resources'ta iki ömür olayı değişikliklerini işleyin.</span><span class="sxs-lookup"><span data-stu-id="7aad4-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="7aad4-105">Doğum günü değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="7aad4-105">Birthday changes</span></span>
- <span data-ttu-id="7aad4-106">Uygunluk kuralı geçersiz kılma süresi değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="7aad4-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="7aad4-107">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Ömür olayı değişimi işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="7aad4-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="7aad4-108">**Ömür olayı değişimi işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="7aad4-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="7aad4-109">Alan</span><span class="sxs-lookup"><span data-stu-id="7aad4-109">Field</span></span> | <span data-ttu-id="7aad4-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="7aad4-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7aad4-111">Kayıt dönemi</span><span class="sxs-lookup"><span data-stu-id="7aad4-111">Enrollment period</span></span> | <span data-ttu-id="7aad4-112">Ömür olayı değişiklikleri işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="7aad4-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="7aad4-113">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="7aad4-113">Legal entity</span></span> | <span data-ttu-id="7aad4-114">Ömür olayı değişiklikleri işleyecek yasal varlık.</span><span class="sxs-lookup"><span data-stu-id="7aad4-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="7aad4-115">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="7aad4-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="7aad4-116">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="7aad4-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="7aad4-117">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7aad4-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="7aad4-118">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7aad4-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="7aad4-119">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7aad4-119">Select **OK**.</span></span> <span data-ttu-id="7aad4-120">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="7aad4-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="7aad4-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="7aad4-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]