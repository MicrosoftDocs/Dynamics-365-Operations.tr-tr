---
title: Veri reyonunu sıfırlama zamanı
description: Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumlar ile veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2021
ms.locfileid: "5989004"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="8fd4b-103">Veri reyonunu sıfırlama zamanı</span><span class="sxs-lookup"><span data-stu-id="8fd4b-103">When to reset a data mart</span></span>

<span data-ttu-id="8fd4b-104">Veri reyonu sıfırlamak zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="8fd4b-105">Koşullara bağlı olarak, bu eylem gerekli çözüm olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="8fd4b-106">Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumların yanı sıra veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="8fd4b-107">Veri reyonu sıfırlama işlemini ne zaman yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="8fd4b-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="8fd4b-108">Veri reyonunu sıfırlamadan önce aşağıdaki soruları göz önünde bulundurun.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="8fd4b-109">Bir veya daha fazla sorunun yanıtı evet ise veri reyonu sıfırlamak kuruluşunuz için faydalı olabilir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="8fd4b-110">Uygulama veritabanı geri yüklendi mi?</span><span class="sxs-lookup"><span data-stu-id="8fd4b-110">Was the application database restored?</span></span>
- <span data-ttu-id="8fd4b-111">Bir destek olayı açtınız mı ve destek mühendisi sorun giderme adımının bir parçası olarak veri reyonunu sıfırlamanızı istedi mi?</span><span class="sxs-lookup"><span data-stu-id="8fd4b-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="8fd4b-112">Veri reyonu sıfırlamak hangi durumlarda uygun değildir?</span><span class="sxs-lookup"><span data-stu-id="8fd4b-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="8fd4b-113">Veri reyonunu sıfırlamayı önermediğimiz durumlar bulunur.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="8fd4b-114">Bunlara aşağıdakiler dahildir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-114">These include the following.</span></span> 

- <span data-ttu-id="8fd4b-115">Veri eşitleme ile ilişkili performans sorunları yaşıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="8fd4b-116">Aşağıdakilerden herhangi biri nedeniyle yinelenen bir sıfırlama modeliniz varsa:</span><span class="sxs-lookup"><span data-stu-id="8fd4b-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="8fd4b-117">**Eksik veri**</span><span class="sxs-lookup"><span data-stu-id="8fd4b-117">**Missing data**</span></span> 
  - <span data-ttu-id="8fd4b-118">**Tümleştirme durumu takılı kaldı**</span><span class="sxs-lookup"><span data-stu-id="8fd4b-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="8fd4b-119">**Eski kayıtlar**: Yalnızca eski kayıtlar olması tek başına veri reyonunun sıfırlanması için geçerli bir gerekçe değildir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="8fd4b-120">Büyük bir veri kümeniz varsa sıfırlama işleminin çalışması biraz zaman alır ancak bu işlemin iyileştirme sağlama olasılığı düşüktür.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="8fd4b-121">Veri reyonu sıfırlama nedir?</span><span class="sxs-lookup"><span data-stu-id="8fd4b-121">What is a data mart reset?</span></span>
- <span data-ttu-id="8fd4b-122">Sıfırlama, yalnızca mevcut görevler tamamlandığında başlar.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="8fd4b-123">Bu, eski verilerin eklenmemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="8fd4b-124">Bu aşamada, "Veri reyonu sıfırlama işlemi, etkin bir görev nedeniyle işlenemedi.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="8fd4b-125">Lütfen daha sonra yeniden deneyin."</span><span class="sxs-lookup"><span data-stu-id="8fd4b-125">Please try again later.”</span></span>
- <span data-ttu-id="8fd4b-126">Sıfırlama, tümleştirme görevlerini devre dışı bırakır ve tüm veri reyonu verilerini siler.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="8fd4b-127">Tümleştirme yeniden etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="8fd4b-128">Veri reyonunu sıfırladığımda, önceden tasarlamış olduğum raporları kaybedecek miyim?</span><span class="sxs-lookup"><span data-stu-id="8fd4b-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="8fd4b-129">Hayır, raporlarınız veri reyonu sıfırlanmadan etkilenmeyen SQL tablolarında depolanır.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="8fd4b-130">Tasarladığınız raporların kaybedilmesiyle ilgili endişeleriniz varsa, kaybetmek istemediğiniz tasarımları yedekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="8fd4b-131">Bunları yedeklemek için, Rapor Tasarımcısı'nı açın ve **Şirket > Şirketler > Yapı Taşları > Dışa aktar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="8fd4b-132">Tüm kullanıcıların veri reyonu sıfırlamak için sistemden çıkması gerekiyor mu?</span><span class="sxs-lookup"><span data-stu-id="8fd4b-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="8fd4b-133">Hayır, veri reyonu sıfırlama sırasında kullanıcılar sistemde çalışmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="8fd4b-134">Ancak, sıfırlama tamamlanana kadar Mali Raporlayıcı ile oluşturulan raporlara erişemezler.</span><span class="sxs-lookup"><span data-stu-id="8fd4b-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
