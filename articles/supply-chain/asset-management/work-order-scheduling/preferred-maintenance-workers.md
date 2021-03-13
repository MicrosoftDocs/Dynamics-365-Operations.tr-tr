---
title: Tercih edilen bakım görevlilerini ayarla
description: Bu konuda Varlık Yönetimi'nde tercih edilen bakım görevlisi ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ab36d9fde0cc6e864f21f9ebd09834f5098c1913
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021416"
---
# <a name="set-up-preferred-maintenance-workers"></a><span data-ttu-id="09b13-103">Tercih edilen bakım görevlilerini ayarla</span><span class="sxs-lookup"><span data-stu-id="09b13-103">Set up preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="09b13-104">İş emri planlama sırasında hangi bakım görevlisinin veya görevli grubunun iş emrini tamamlamak üzere tahsis edileceğini belirten bir tercih yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09b13-104">During work order scheduling, you can make a preference regarding which maintenance worker or worker group is allocated to complete the work order.</span></span> <span data-ttu-id="09b13-105">Bu işlevin kullanımı isteğe bağlıdır, ancak çalışanın yeteneklerine ve yetkinliklerine dayalı olarak işin tamamlanması için en nitelikli bakım görevlisini seçmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="09b13-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="09b13-106">Yalnızca, planlama zamanında uygun olan bakım görevlileri planlanır.</span><span class="sxs-lookup"><span data-stu-id="09b13-106">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="09b13-107">Tercih edilen bakım görevlisi ayarı planlama sırasında bir iş emriyle eşleşirse ancak bakım görevlisi diğer işlere tahsis edilmişse, iş emri uygun durumdaki başka bir bakım görevlisi için planlanır.</span><span class="sxs-lookup"><span data-stu-id="09b13-107">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another available maintenance worker.</span></span>

<span data-ttu-id="09b13-108">Tercih edilen bakım görevlilerini ayarlamak için önce bakım görevlileri ve görevli gruplarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="09b13-108">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups.</span></span> <span data-ttu-id="09b13-109">Bakım görevlileri ve görevli gruplarını nasıl ayarlayacağınızla ilgili açıklama için bkz. [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="09b13-109">For a description about how to set up maintenance workers and worker groups, see to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="09b13-110">Tercih edilen bakım görevlilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="09b13-110">Set up preferred workers</span></span>

<span data-ttu-id="09b13-111">Tercih edilen bakım görevlisi veya görevli grubu aşağıdakilerden biri veya daha fazlasıyla ilgili olabilir:</span><span class="sxs-lookup"><span data-stu-id="09b13-111">A preferred maintenance worker or worker group can be related to one or more of the following:</span></span>

- <span data-ttu-id="09b13-112">görevle</span><span class="sxs-lookup"><span data-stu-id="09b13-112">trade</span></span>  
- <span data-ttu-id="09b13-113">bakım işi türü çeşidiyle</span><span class="sxs-lookup"><span data-stu-id="09b13-113">maintenance job type variant</span></span>  
- <span data-ttu-id="09b13-114">bakım işi türüyle</span><span class="sxs-lookup"><span data-stu-id="09b13-114">maintenance job type</span></span>  
- <span data-ttu-id="09b13-115">bakım işi türü kategorisiyle</span><span class="sxs-lookup"><span data-stu-id="09b13-115">maintenance job type category</span></span>  
- <span data-ttu-id="09b13-116">varlıkla</span><span class="sxs-lookup"><span data-stu-id="09b13-116">asset</span></span>  
- <span data-ttu-id="09b13-117">varlık türüyle</span><span class="sxs-lookup"><span data-stu-id="09b13-117">asset type</span></span>  

<span data-ttu-id="09b13-118">Aynı kayıt için ne kadar çok seçim yaparsanız, kurulumunuz o kadar belirgin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="09b13-118">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="09b13-119">**Varlık Yönetimi** > **Kurulum** > **Çalışanlar** > **Tercih edilen bakım görevlileri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09b13-119">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="09b13-120">Yeni bir kayıt oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="09b13-120">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="09b13-121">Bir "varsayılan" bakım görevlisi veya görevli grubu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="09b13-121">Start by creating a "default" maintenance worker or worker group.</span></span> <span data-ttu-id="09b13-122">Bu, yalnızca **Tercih edilen bakım görevlisi grubu** alanında veya **Tercih edilen bakım görevlisi** alanında seçim yapacağınız anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="09b13-122">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="09b13-123">Aşağıdaki ekran görüntüsünde, **tercih edilen bakım görevlisi grubu** olarak "Talepler" in seçildiği bir ilk kayıt örneği görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="09b13-123">In the screenshot below, you see an example in the first record in which "Requests" is selected as **Preferred maintenance worker group**.</span></span>

    [!NOTE] <span data-ttu-id="09b13-124">Varsayılan kurulum, iş emri planlaması sırasında başka, daha özel kombinasyon iş emrinin içeriğiyle eşleşirse kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="09b13-124">The default setup will be used during work order scheduling if no other, more specific, combination matches the contents of the work order.</span></span>

4. <span data-ttu-id="09b13-125">Yeni bir kayıt oluşturmak için adım 2'yi tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="09b13-125">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="09b13-126">Tercih edilen çalışan veya çalışan grubunun ayrıntı düzeyine bağlı olarak gerekli seçimleri yapın.</span><span class="sxs-lookup"><span data-stu-id="09b13-126">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> 

    <span data-ttu-id="09b13-127">*Örnek:* Aşağıdaki ekran görüntüsünde, altıncı kayıtta, tercih edilen çalışan olarak bakım görevlisi Shawn Richardson seçilidir.</span><span class="sxs-lookup"><span data-stu-id="09b13-127">*Example:* In the screenshot below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="09b13-128">Planlanan saatte uygun olması durumunda, "CH-BP1-03-02" varlığı ve "tesis değerlendirmesi " bakım işi türünü içeren bir iş emri planlamasında otomatik olarak seçilecektir.</span><span class="sxs-lookup"><span data-stu-id="09b13-128">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintenance job type "Facility assessment", if he is available at the scheduled time.</span></span>

    [!NOTE] <span data-ttu-id="09b13-129">Genellikle, iş emri planlama sırasında tercih edilen bir bakım çalışanı seçildiğinde, Varlık Yönetimi olası bir eşleşmeyi denetlemek için tüm **Tercih edilen bakım görevlileri** kayıtlarına bakar ve her zaman en belirgin birleşimi denetler.</span><span class="sxs-lookup"><span data-stu-id="09b13-129">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="09b13-130">Eşleşme bulunmazsa, **Tercih edilen bakım çalışanı grubu** alanında veya **Tercih edilen bakım çalışanı** alanında bulunan "varsayılan" kayıt kullanılır.</span><span class="sxs-lookup"><span data-stu-id="09b13-130">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>

![Şekil 1](media/02-work-order-scheduling.png)

<span data-ttu-id="09b13-132">Ayrıca, bakım talebi veya iş emri oluşturulurken seçilebilecek *sorumlu* bakım görevlileri de ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09b13-132">You can also set up *responsible* maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="09b13-133">**Tüm iş emirleri** ve **Tüm bakım istekleri** alanında gerekirse seçimi düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="09b13-133">You can edit the selection in **All work orders** and **All maintenance requests**, if required.</span></span> <span data-ttu-id="09b13-134">Daha fazla bilgi için bkz. [Sorumlu bakım görevlileri](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="09b13-134">For more information, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

<span data-ttu-id="09b13-135">İş emri planlama sırasında, hangi çalışanların bir iş emriyle ilgili işleri tamamlaması gerektiğini belirlemek için farklı puanlar hesaplanır (bu puanlar,**Varlık yönetimi parametreleri** > **İş emri planlama** bağlantısında ayarlanır).</span><span class="sxs-lookup"><span data-stu-id="09b13-135">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="09b13-136">İş emri planlama sırasında iki veya daha fazla tercih edilen bakım çalışanı veya sorumlu bakım çalışanı aynı puanı elde ederse, bir çalışan rasgele seçilir.</span><span class="sxs-lookup"><span data-stu-id="09b13-136">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="09b13-137">Aksi takdirde, iş emrini tamamlamak için tahsis edilen daima en yüksek puanlı çalışan olur.</span><span class="sxs-lookup"><span data-stu-id="09b13-137">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

