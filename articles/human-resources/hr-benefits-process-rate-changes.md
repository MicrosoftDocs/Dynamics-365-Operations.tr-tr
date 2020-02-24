---
title: Değişiklikleri işleyin
description: Yeni veya mevcut bir avantaj planının uygunluk kuralı ayarlarında bir değişikliği olduğunda, Microsoft Dynamics 365 Human Resources'ta kazanç oranı değişikliklerini işleyin.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010821"
---
# <a name="process-rate-changes"></a><span data-ttu-id="a2c39-103">Değişiklikleri işleyin</span><span class="sxs-lookup"><span data-stu-id="a2c39-103">Process rate changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a2c39-104">Yeni veya mevcut bir avantaj planının uygunluk kuralı ayarlarında bir değişikliği olduğunda, Microsoft Dynamics 365 Human Resources'ta kazanç oranı değişikliklerini işleyin.</span><span class="sxs-lookup"><span data-stu-id="a2c39-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="a2c39-105">Yeni bir uygunluk kuralı oluşturulup plana atanmışsa, bu durum sisteme, çalışanların şimdi yeni uygunluk seçeneklerine dayalı olarak planlama için uygun olup olmadığını denetlemek amacıyla, alt uygunluğu yeniden çalıştırması için uyarır.</span><span class="sxs-lookup"><span data-stu-id="a2c39-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to re-run worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="a2c39-106">**Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Oran değişimi güncelleme işlemini** seçin.</span><span class="sxs-lookup"><span data-stu-id="a2c39-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="a2c39-107">**Kazanç kaydı oran güncelleme çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:</span><span class="sxs-lookup"><span data-stu-id="a2c39-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="a2c39-108">Alan</span><span class="sxs-lookup"><span data-stu-id="a2c39-108">Field</span></span> | <span data-ttu-id="a2c39-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2c39-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="a2c39-110">Kayıt dönemi</span><span class="sxs-lookup"><span data-stu-id="a2c39-110">Enrollment period</span></span> | <span data-ttu-id="a2c39-111">Oran değişiklikleri işleyecek kayıt dönemi.</span><span class="sxs-lookup"><span data-stu-id="a2c39-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="a2c39-112">İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="a2c39-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="a2c39-113">İşlem bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="a2c39-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="a2c39-114">Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2c39-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="a2c39-115">İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2c39-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="a2c39-116">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2c39-116">Select **OK**.</span></span> <span data-ttu-id="a2c39-117">İşlem, ayarladığınız parametrelerle çalışacaktır.</span><span class="sxs-lookup"><span data-stu-id="a2c39-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="a2c39-118">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a2c39-118">Select **OK**.</span></span>
