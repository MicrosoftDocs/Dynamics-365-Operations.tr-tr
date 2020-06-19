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
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 11809bcf631316a064a3c917926f486ff22cb35a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429140"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="2b866-103">Ömür olayı değişikliklerini işle</span><span class="sxs-lookup"><span data-stu-id="2b866-103">Process life event changes</span></span>

<span data-ttu-id="2b866-104">Ömür olayı değişiklikleri için Microsoft Dynamics 365 Human Resources'ta iki ömür olayı değişikliklerini işleyin.</span><span class="sxs-lookup"><span data-stu-id="2b866-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="2b866-105">Doğum günü değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="2b866-105">Birthday changes</span></span>
- <span data-ttu-id="2b866-106">Uygunluk kuralı geçersiz kılma süresi değişiklikleri</span><span class="sxs-lookup"><span data-stu-id="2b866-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="2b866-107">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Ömür olayı değişimi işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="2b866-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="2b866-108">**Ömür olayı değişimi işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="2b866-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="2b866-109">Alan</span><span class="sxs-lookup"><span data-stu-id="2b866-109">Field</span></span> | <span data-ttu-id="2b866-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b866-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2b866-111">Kayıt dönemi</span><span class="sxs-lookup"><span data-stu-id="2b866-111">Enrollment period</span></span> | <span data-ttu-id="2b866-112">Ömür olayı değişiklikleri işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="2b866-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="2b866-113">Tüzel kişilik</span><span class="sxs-lookup"><span data-stu-id="2b866-113">Legal entity</span></span> | <span data-ttu-id="2b866-114">Ömür olayı değişiklikleri işleyecek yasal varlık.</span><span class="sxs-lookup"><span data-stu-id="2b866-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="2b866-115">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="2b866-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2b866-116">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="2b866-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="2b866-117">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b866-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2b866-118">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b866-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2b866-119">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b866-119">Select **OK**.</span></span> <span data-ttu-id="2b866-120">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="2b866-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="2b866-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2b866-121">Select **OK**.</span></span>
