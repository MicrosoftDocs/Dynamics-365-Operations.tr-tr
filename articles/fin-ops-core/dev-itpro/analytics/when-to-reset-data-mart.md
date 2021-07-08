---
title: Veri reyonunu sıfırlamayla ilgili SSS
description: Bu konu, veri reyonu sıfırlama hakkında sık sorulan bazı soruların yanıtlarını sağlar.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266621"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="f69ca-103">Veri reyonunu sıfırlamayla ilgili SSS</span><span class="sxs-lookup"><span data-stu-id="f69ca-103">Data mart resets FAQ</span></span>

<span data-ttu-id="f69ca-104">Bu konu, veri reyonu sıfırlama hakkında sık sorulan bazı soruların yanıtlarını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f69ca-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="f69ca-105">Veri reyonu sıfırlama işlemi zaman alan bir işlem olabilir ve koşullara bağlı olarak gerekli çözüm olmayabilir.</span><span class="sxs-lookup"><span data-stu-id="f69ca-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="f69ca-106">Bu nedenle, bu konu bir veri reyonu sıfırlamasının yardımcı olabileceği ve büyük olasılıkla size yardımcı olamayacağı koşullar hakkında bilgi içerir.</span><span class="sxs-lookup"><span data-stu-id="f69ca-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="f69ca-107">Veri reyonu sıfırlama nedir?</span><span class="sxs-lookup"><span data-stu-id="f69ca-107">What is a data mart reset?</span></span>

<span data-ttu-id="f69ca-108">Veri reyonu sıfırlama, tümleştirme görevlerini devre dışı bırakacak, tüm veri reyonu verilerini silecek ve tümleştirmeyi yeniden etkinleştirecektir.</span><span class="sxs-lookup"><span data-stu-id="f69ca-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="f69ca-109">Eski verilerin eklenmemesini sağlamak için veri reyonu sıfırlaması yalnızca mevcut görevler tamamlandıktan sonra başlatılabilir.</span><span class="sxs-lookup"><span data-stu-id="f69ca-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="f69ca-110">Tüm görevler tamamlanmadan önce veri reyonunu sıfırlamayı denerseniz şöyle bir ileti görebillirsiniz: "Veri reyonu sıfırlama etkin bir görev nedeniyle işlenemedi.</span><span class="sxs-lookup"><span data-stu-id="f69ca-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="f69ca-111">Lütfen daha sonra yeniden deneyin."</span><span class="sxs-lookup"><span data-stu-id="f69ca-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="f69ca-112">Veri reyonu sıfırlama işlemini ne zaman yapmam gerekir?</span><span class="sxs-lookup"><span data-stu-id="f69ca-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="f69ca-113">Aşağıdaki ifadelerden biri veya daha fazlası sizin durumunuza için geçerli ise kuruluşunuz bir veri reyonu sıfırlamadan yararlanabilir:</span><span class="sxs-lookup"><span data-stu-id="f69ca-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="f69ca-114">Uygulama veritabanı geri yüklendi.</span><span class="sxs-lookup"><span data-stu-id="f69ca-114">The application database was restored.</span></span>
- <span data-ttu-id="f69ca-115">Bir destek bileti açtınız ve Destek mühendisi sorun giderme adımının bir parçası olarak veri reyonunu sıfırlamanızı istedi.</span><span class="sxs-lookup"><span data-stu-id="f69ca-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="f69ca-116">Veri reyonu sıfırlama ne zaman uygun değildir?</span><span class="sxs-lookup"><span data-stu-id="f69ca-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="f69ca-117">Veri reyonunu sıfırlamayı önermediğimiz bazı durumları aşağıda bulabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="f69ca-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="f69ca-118">Veri eşitleme ile ilişkili performans sorunları yaşıyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="f69ca-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="f69ca-119">Aşağıdakilerden herhangi biri nedeniyle yinelenen bir sıfırlama modeliniz var:</span><span class="sxs-lookup"><span data-stu-id="f69ca-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="f69ca-120">**Eksik veri**: Verilerin eksik olduğunu görürseniz, rapor biçiminizi ve veri eşitleme sorunlarını gözden geçirmesi için Microsoft ile bir destek bileti açın.</span><span class="sxs-lookup"><span data-stu-id="f69ca-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="f69ca-121">**Tümleştirme durumu takılı kaldı**</span><span class="sxs-lookup"><span data-stu-id="f69ca-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="f69ca-122">**Eski kayıtlar**: Yalnızca eski kayıtlar olması tek başına veri reyonunun sıfırlanması için geçerli bir gerekçe değildir.</span><span class="sxs-lookup"><span data-stu-id="f69ca-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="f69ca-123">Büyük bir veri kümeniz varsa sıfırlama işleminin çalışması biraz zaman alır ancak bu işlemin iyileştirme sağlama olasılığı düşüktür.</span><span class="sxs-lookup"><span data-stu-id="f69ca-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="f69ca-124">Veri reyonunu sıfırladığımda, önceden tasarlamış olduğum raporları kaybedecek miyim?</span><span class="sxs-lookup"><span data-stu-id="f69ca-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="f69ca-125">Hayır.</span><span class="sxs-lookup"><span data-stu-id="f69ca-125">No.</span></span> <span data-ttu-id="f69ca-126">Raporlarınız veri reyonu sıfırlanmadan etkilenmeyen SQL tablolarında depolanır.</span><span class="sxs-lookup"><span data-stu-id="f69ca-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="f69ca-127">Tasarladığınız raporların kaybedilmesiyle ilgili endişeleriniz varsa, kaybetmek istemediğiniz tasarımları yedekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f69ca-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="f69ca-128">Tasarımları yedeklemek için, Rapor Tasarımcısı'nı açın ve **Şirket \> Şirketler \> Yapı Taşları \> Dışa aktar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="f69ca-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="f69ca-129">Veri reyonu sıfırlayabilmem için tüm kullanıcıların sistemden çıkması gerekiyor mu?</span><span class="sxs-lookup"><span data-stu-id="f69ca-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="f69ca-130">Hayır.</span><span class="sxs-lookup"><span data-stu-id="f69ca-130">No.</span></span> <span data-ttu-id="f69ca-131">Veri reyonu sıfırlama sırasında kullanıcılar sistemde çalışmaya devam edebilir.</span><span class="sxs-lookup"><span data-stu-id="f69ca-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="f69ca-132">Ancak, sıfırlama tamamlanana kadar Financial Reporter ile oluşturulan raporlara erişemezler.</span><span class="sxs-lookup"><span data-stu-id="f69ca-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
