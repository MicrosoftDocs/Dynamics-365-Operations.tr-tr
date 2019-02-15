---
title: Perakende işlem tutarlılık denetleyicisi
description: Bu konuda Microsoft Dynamics 365 for Retail ürününde bulunan perakende işlem tutarlılık denetleyicisi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "303011"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="d79d2-103">Perakende işlem tutarlılık denetleyicisi</span><span class="sxs-lookup"><span data-stu-id="d79d2-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="d79d2-104">Bu konuda Microsoft Dynamics 365 for Finance and Operations sürüm 8.1.3'te sunulan perakende işlem tutarlılık denetleyicisi açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d79d2-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="d79d2-105">Tutarlılık denetleyicisi, tutarsız işlemleri ekstre deftere nakil işlemiyle seçilmeden önce tanımlayıp ayırır.</span><span class="sxs-lookup"><span data-stu-id="d79d2-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="d79d2-106">Bir ekstre Retail departmanında deftere nakledildiğinde deftere nakil işlemi, perakende işlem tablolarında tutarsız verilerin bulunması nedeniyle başarısız olabilir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="d79d2-107">Veri sorunu, satış noktası (POS) uygulamasında öngörülemeyen aksaklıklardan veya işlemlerin üçüncü taraf POS sistemleri tarafından yanlış aktarılmasından kaynaklanabilir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="d79d2-108">Bu tutarsızlıkların nasıl görünebileceğine ilişkin örnekler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d79d2-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="d79d2-109">Üstbilgi tablosundaki işlem toplamı, satırlardaki işlem toplamıyla eşleşmiyordur.</span><span class="sxs-lookup"><span data-stu-id="d79d2-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="d79d2-110">Üstbilgi tablosundaki satır sayısı, işlem tablosundaki satır sayısıyla eşleşmiyordur.</span><span class="sxs-lookup"><span data-stu-id="d79d2-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="d79d2-111">Üstbilgi tablosundaki vergiler, satırlardaki vergi tutarıyla eşleşmiyordur.</span><span class="sxs-lookup"><span data-stu-id="d79d2-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="d79d2-112">Ekstre deftere nakil işlemi tarafından tutarsız işlemler seçildiğinde tutarsız satış faturaları ve ödeme günlükleri oluşturulur ve bunun sonucunda tüm ekstre deftere nakil işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="d79d2-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="d79d2-113">Ekstrelerin bu durumdan kurtarılması, birden fazla işlem tablosu arasında karmaşık veri düzeltmelerini içerir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="d79d2-114">Perakende işlem tutarlılık denetleyicisi, bu tür sorunları önler.</span><span class="sxs-lookup"><span data-stu-id="d79d2-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="d79d2-115">Aşağıdaki çizelgede işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="d79d2-116">![Perakende işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi](./media/validchecker.png "Perakende işlem tutarlılık denetleyicisi ile gerçekleştirilen deftere nakil işlemi")</span><span class="sxs-lookup"><span data-stu-id="d79d2-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="d79d2-117">**Mağaza işlemlerini doğrulama** toplu işlemi, aşağıdaki senaryolar için perakende işlem tablolarının tutarlılığını denetler.</span><span class="sxs-lookup"><span data-stu-id="d79d2-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="d79d2-118">Müşteri hesabı: Perakende işlem tablolarındaki müşteri hesabının Genel Merkez müşteri yöneticisinde de bulunduğunu doğrular.</span><span class="sxs-lookup"><span data-stu-id="d79d2-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="d79d2-119">Satır sayısı: İşlem üstbilgi tablosundan alındığı şekilde satır sayısının satış işlem tablolarındaki satır sayısıyla eşleştiğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="d79d2-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="d79d2-120">Tutarlılık denetleyicisini ayarlama</span><span class="sxs-lookup"><span data-stu-id="d79d2-120">Set up the consistency checker</span></span>
<span data-ttu-id="d79d2-121">**Perakende \> Perakende BT \> POS deftere nakil** bölümünde "Mağaza işlemlerini doğrulama" toplu işlemini düzenli aralıklarla yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="d79d2-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="d79d2-122">Toplu iş, "Ekstreyi toplu olarak hesaplama" ve "Ekstreyi toplu olarak deftere nakletme" işlemlerinin ayarlanmasına benzer şekilde, mağaza organizasyon hiyerarşisine göre zamanlanabilir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="d79d2-123">Bu toplu işlemi günde birden fazla kez yürütülecek şekilde yapılandırmanızı ve her P işi uygulamasının sonunda çalıştırılacak şekilde zamanlamanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="d79d2-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="d79d2-124">Doğrulama işleminin sonuçları</span><span class="sxs-lookup"><span data-stu-id="d79d2-124">Results of validation process</span></span>
<span data-ttu-id="d79d2-125">Toplu işlem tarafından gerçekleştirilen doğrulama denetlemesinin sonuçları, uygun perakende işlemde işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="d79d2-126">Perakende işlem kaydındaki **Doğrulama durumu** alanı, ya **Başarılı** ya da **Hata** olarak ayarlanır ve son doğrulama çalıştırma tarihi, **Son doğrulama saati** alanında görünür.</span><span class="sxs-lookup"><span data-stu-id="d79d2-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="d79d2-127">Doğrulama hatası ile ilgili daha fazla hata açıklaması görmek için ilgili perakende mağaza işlem kaydını seçip **Doğrulama hataları** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d79d2-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="d79d2-128">Doğrulama denetlemesinden geçemeyen işlemler ve henüz doğrulanmamış olan işlemler ekstrelere eklenmez.</span><span class="sxs-lookup"><span data-stu-id="d79d2-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="d79d2-129">"Ekstre hesaplama" işlemi sırasında ekstreye eklenebilecek, ancak eklenmemiş olan işlemlerin olması durumunda kullanıcılar bilgilendirilir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="d79d2-130">Bir doğrulama hatası bulunursa hatayı düzeltmenin tek yolu, Microsoft Desteği ile iletişime geçmektir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="d79d2-131">Bir sonraki sürümde kullanıcıların kullanıcı arabiriminde başarısız olan kayıtları düzeltmelerine olanak tanıyan özellik eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="d79d2-132">Değişiklik geçmişini takip etmek için günlüğe kaydetme ve denetleme özellikleri de kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="d79d2-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="d79d2-133">Bir sonraki sürümde daha fazla senaryoyu desteklemek için ek doğrulama kuralları da eklenecektir.</span><span class="sxs-lookup"><span data-stu-id="d79d2-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
