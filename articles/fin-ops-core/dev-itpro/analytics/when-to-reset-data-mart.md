---
title: Veri reyonunu sıfırlama zamanı
description: Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumlar ile veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093224"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="b2780-103">Veri reyonunu sıfırlama zamanı</span><span class="sxs-lookup"><span data-stu-id="b2780-103">When to reset a data mart</span></span>

<span data-ttu-id="b2780-104">Veri reyonu sıfırlamak zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="b2780-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="b2780-105">Koşullara bağlı olarak, bu eylem gerekli çözüm olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="b2780-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="b2780-106">Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumların yanı sıra veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="b2780-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="b2780-107">Veri reyonu sıfırlama işlemini ne zaman yapmanız gerekir?</span><span class="sxs-lookup"><span data-stu-id="b2780-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="b2780-108">Veri reyonunu sıfırlamadan önce aşağıdaki soruları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="b2780-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="b2780-109">Bir veya daha fazla sorunun yanıtı evet ise veri reyonu sıfırlamak kuruluşunuz için faydalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b2780-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="b2780-110">Uygulama veri tabanı geri yüklendi ancak veri reyonu veri tabanı geri yüklenmedi.</span><span class="sxs-lookup"><span data-stu-id="b2780-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="b2780-111">Bir muhasebe dönemi için rapor tasarımıyla ilgili bir sorundan kaynaklanmayan hatalı veriler görüyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="b2780-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="b2780-112">Bir hesap dönemiyle ilgili hatalı veriler görüyorsunuz ve Rapor Tasarımcısındaki **Tümleştirme durumu** sayfasında yer alan Tümleştirme denemeleri bölümünde kayıtlar listeleniyor (Rapor Tasarımcısını başlatın ve  **Araçlar > Tümleştirme durumu**'nu seçin).</span><span class="sxs-lookup"><span data-stu-id="b2780-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="b2780-113">Bir destek olayı açtınız ve destek mühendisi sorun giderme adımının bir parçası olarak veri reyonunu sıfırlamanızı istedi.</span><span class="sxs-lookup"><span data-stu-id="b2780-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="b2780-114">Veri reyonu sıfırlamak hangi durumlarda uygun değildir?</span><span class="sxs-lookup"><span data-stu-id="b2780-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="b2780-115">Veri reyonunu sıfırlamayı önermediğimiz durumlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="b2780-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="b2780-116">Bunlara aşağıdakiler dahildir.</span><span class="sxs-lookup"><span data-stu-id="b2780-116">These include the following.</span></span> 

- <span data-ttu-id="b2780-117">Nedenin bu konuda listelenmediği durumlar.</span><span class="sxs-lookup"><span data-stu-id="b2780-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="b2780-118">Veri eşitlemeyle ilişkili performans sorunları yaşıyorsunuz. Bu durumda, veri reyonunu sıfırlamak faydalı olmaz.</span><span class="sxs-lookup"><span data-stu-id="b2780-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="b2780-119">Aşağıdakilerden herhangi biri nedeniyle yinelenen bir sıfırlama modeliniz varsa:</span><span class="sxs-lookup"><span data-stu-id="b2780-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="b2780-120">**Eksik veriler**: Önce, rapor tasarım sorunlarını ve veri eşitleme zamanlaması sorunlarını (ör. eksik verilerin deftere nakledilmesinden itibaren olgu eşlemesinin çalıştırılmadığını görüyorsanız) ortadan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="b2780-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="b2780-121">**Takılı kalan tümleştirme durumu**: Tümleştirme yavaşsa veya takılı kalmışsa veri reyonunu sıfırlamak büyük ihtimalle sorunu çözmeyecektir.</span><span class="sxs-lookup"><span data-stu-id="b2780-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="b2780-122">**Sıfırlama denemelerinin başarısız olması**: Sıfırlama işlemini tamamlamak için birkaç deneme yapılmışsa ve eksik veriler nedeniyle başarısız olunmuşsa, bir destek olayı açmanızı ve veri reyonunu yeniden sıfırlamaya çalışmadan önce durumunuzu analiz etmek için bir destek mühendisinden yardım almanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="b2780-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="b2780-123">**Eski kayıtlar**: Yalnızca eski kayıtlar olması tek başına veri reyonunun sıfırlanması için geçerli bir gerekçe değildir.</span><span class="sxs-lookup"><span data-stu-id="b2780-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="b2780-124">Büyük bir veri kümeniz varsa sıfırlama işleminin çalışması biraz zaman alır ancak bu işlemin iyileştirme sağlama olasılığı düşüktür.</span><span class="sxs-lookup"><span data-stu-id="b2780-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="b2780-125">Veri reyonu sıfırlamasının gerçekleştiremeyeceği işlemler</span><span class="sxs-lookup"><span data-stu-id="b2780-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="b2780-126">Sıfırlama, yalnızca mevcut görevler tamamlandığında başlar.</span><span class="sxs-lookup"><span data-stu-id="b2780-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="b2780-127">Bu, eski verilerin eklenmemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="b2780-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="b2780-128">Bu aşamada, "Veri reyonu sıfırlama işlemi, etkin bir görev nedeniyle işlenemedi.</span><span class="sxs-lookup"><span data-stu-id="b2780-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="b2780-129">Lütfen daha sonra yeniden deneyin."</span><span class="sxs-lookup"><span data-stu-id="b2780-129">Please try again later.”</span></span>
- <span data-ttu-id="b2780-130">Sıfırlama, tümleştirme görevlerini devre dışı bırakır ve tüm veri reyonu verilerini siler.</span><span class="sxs-lookup"><span data-stu-id="b2780-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="b2780-131">Tümleştirme yeniden etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="b2780-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="b2780-132">Aşağıdaki noktalar, veri reyonu sıfırlamanın *gerçekleştirmeyeceği* iki işlemi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b2780-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="b2780-133">Sıfırlama işlemleri rapor tasarımlarını temizlemez.</span><span class="sxs-lookup"><span data-stu-id="b2780-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="b2780-134">Sıfırlama işlemleri, seçili olmadıkça şirket verilerini veya kullanıcı verilerini temizlemez.</span><span class="sxs-lookup"><span data-stu-id="b2780-134">Resets do not clear company data or user data unless selected.</span></span>
