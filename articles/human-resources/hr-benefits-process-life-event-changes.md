---
title: Ömür olayı değişikliklerini işle
description: Ömür olayı değişiklikleri için Microsoft Dynamics 365 Human Resources'ta ömür olayı değişikliklerini işleyin.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 39d1e94347809a1756fc4f66e5edc345c70eaf39
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741448"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="ede69-103">Ömür olayı değişikliklerini işle</span><span class="sxs-lookup"><span data-stu-id="ede69-103">Process life event changes</span></span>

<span data-ttu-id="ede69-104">Ömür olayı değişiklikleri için Microsoft Dynamics 365 Human Resources'ta iki ömür olayı değişikliklerini işleyin.</span><span class="sxs-lookup"><span data-stu-id="ede69-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="ede69-105">Doğum günü değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="ede69-105">Birthday changes</span></span>
- <span data-ttu-id="ede69-106">Uygunluk kuralı geçersiz kılma süresi değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="ede69-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="ede69-107">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Ömür olayı değişimi işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="ede69-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="ede69-108">**Ömür olayı değişimi işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="ede69-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="ede69-109">Alan</span><span class="sxs-lookup"><span data-stu-id="ede69-109">Field</span></span> | <span data-ttu-id="ede69-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="ede69-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ede69-111">Kayıt dönemi</span><span class="sxs-lookup"><span data-stu-id="ede69-111">Enrollment period</span></span> | <span data-ttu-id="ede69-112">Ömür olayı değişiklikleri işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="ede69-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="ede69-113">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="ede69-113">Legal entity</span></span> | <span data-ttu-id="ede69-114">Ömür olayı değişiklikleri işleyecek yasal varlık.</span><span class="sxs-lookup"><span data-stu-id="ede69-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="ede69-115">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="ede69-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="ede69-116">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="ede69-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="ede69-117">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ede69-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="ede69-118">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ede69-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="ede69-119">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ede69-119">Select **OK**.</span></span> <span data-ttu-id="ede69-120">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="ede69-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="ede69-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="ede69-121">Select **OK**.</span></span>
