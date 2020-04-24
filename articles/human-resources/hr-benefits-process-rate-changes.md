---
title: Değişiklikleri işleyin
description: Yeni veya mevcut bir avantaj planının uygunluk kuralı ayarlarında bir değişikliği olduğunda, Microsoft Dynamics 365 Human Resources'ta kazanç oranı değişikliklerini işleyin.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 850709480326f6a0871f19ea1bb287631cd58b42
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229959"
---
# <a name="process-rate-changes"></a><span data-ttu-id="35480-103">Değişiklikleri işleyin</span><span class="sxs-lookup"><span data-stu-id="35480-103">Process rate changes</span></span>

<span data-ttu-id="35480-104">Yeni veya mevcut bir avantaj planının uygunluk kuralı ayarlarında bir değişikliği olduğunda, Microsoft Dynamics 365 Human Resources'ta kazanç oranı değişikliklerini işleyin.</span><span class="sxs-lookup"><span data-stu-id="35480-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="35480-105">Yeni bir uygunluk kuralı oluşturulup plana atanmışsa, bu durum sisteme, çalışanların şimdi yeni uygunluk seçeneklerine dayalı olarak planlama için uygun olup olmadığını denetlemek amacıyla, alt uygunluğu yeniden çalıştırması için uyarır.</span><span class="sxs-lookup"><span data-stu-id="35480-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="35480-106">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Oran değişimi güncelleme işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="35480-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="35480-107">**Kazanç kaydı oran güncelleme çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="35480-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="35480-108">Alan</span><span class="sxs-lookup"><span data-stu-id="35480-108">Field</span></span> | <span data-ttu-id="35480-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="35480-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="35480-110">**Kayıt dönemi**</span><span class="sxs-lookup"><span data-stu-id="35480-110">**Enrollment period**</span></span> | <span data-ttu-id="35480-111">Oran değişiklikleri işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="35480-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="35480-112">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="35480-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="35480-113">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="35480-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="35480-114">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="35480-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="35480-115">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="35480-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="35480-116">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="35480-116">Select **OK**.</span></span> <span data-ttu-id="35480-117">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="35480-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="35480-118">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="35480-118">Select **OK**.</span></span>
