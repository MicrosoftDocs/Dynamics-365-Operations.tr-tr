---
title: Tercih edilen bakım görevlilerini ayarla
description: Bu konuda Varlık Yönetimi'nde tercih edilen bakım görevlisi ayarlama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887423"
---
# <a name="preferred-maintenance-workers"></a><span data-ttu-id="3f83d-103">Tercih edilen bakım görevlileri</span><span class="sxs-lookup"><span data-stu-id="3f83d-103">Preferred maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3f83d-104">İş emri planlama sırasında hangi bakım görevlilerinin iş emirlerini tamamlamak üzere tahsis edileceğini belirten bir tercih yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f83d-104">You can make a preference regarding which maintenance workers are allocated to complete work orders during work order scheduling.</span></span> <span data-ttu-id="3f83d-105">Bu işlevin kullanımı isteğe bağlıdır, ancak çalışanın yeteneklerine ve yetkinliklerine dayalı olarak işin tamamlanması için en nitelikli bakım görevlisini seçmenize yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="3f83d-105">The use of this functionality is optional, but it can help you make a choice for the most qualified maintenance worker to complete a job, based on worker skills and competencies.</span></span> <span data-ttu-id="3f83d-106">Bu nedenle, iş siparişi planlama sırasında, **Tercih edilen bakım görevlileri** kurulumu, bir iş emri için belirli bir bakım görevlisinin veya çalışan grubunun planlanıp planlanmayacağını belirlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3f83d-106">Therefore, during work order scheduling, the setup in **Preferred maintenance workers** is used to determine if a specific maintenance worker or worker group should be scheduled for a work order.</span></span> <span data-ttu-id="3f83d-107">Yalnızca, planlama zamanında uygun olan bakım görevlileri planlanır.</span><span class="sxs-lookup"><span data-stu-id="3f83d-107">Only maintenance workers that are available at scheduling time will be scheduled.</span></span> <span data-ttu-id="3f83d-108">Tercih edilen bakım görevlisi ayarı planlama sırasında bir iş emriyle eşleşirse ancak bakım görevlisi diğer işlere tahsis edilmişse, iş emri uygun durumdaki başka bir bakım görevlisi için planlanır.</span><span class="sxs-lookup"><span data-stu-id="3f83d-108">If a preferred maintenance worker setup matches a work order during scheduling, but the maintenance worker is allocated to other jobs, the work order will be scheduled to another, available, maintenance worker.</span></span>

<span data-ttu-id="3f83d-109">Tercih edilen bakım görevlilerini ayarlamadan önce, ilk olarak seçilmek için uygun olması gereken bakım görevlilerini ve çalışan gruplarını ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3f83d-109">Before you can set up preferred maintenance workers, you must first set up the maintenance workers and worker groups that should be available for selection.</span></span> <span data-ttu-id="3f83d-110">Bakım görevlileri ve çalışan gruplarını nasıl ayarlayacağınızla ilgili açıklama için bkz. [Bakım görevlileri ve çalışan grupları](../setup-for-objects/workers-and-worker-groups.md).</span><span class="sxs-lookup"><span data-stu-id="3f83d-110">Refer to [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md) for a description on how to set up maintenance workers and worker groups.</span></span>

## <a name="set-up-preferred-workers"></a><span data-ttu-id="3f83d-111">Tercih edilen bakım görevlilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="3f83d-111">Set up preferred workers</span></span>

<span data-ttu-id="3f83d-112">Tercih edilen bakım görevlisi veya çalışan grubu belirli bir</span><span class="sxs-lookup"><span data-stu-id="3f83d-112">A preferred maintenance worker or worker group can be related to a specific</span></span>

- <span data-ttu-id="3f83d-113">görevle</span><span class="sxs-lookup"><span data-stu-id="3f83d-113">trade</span></span>  
- <span data-ttu-id="3f83d-114">bakım işi türü çeşidiyle</span><span class="sxs-lookup"><span data-stu-id="3f83d-114">maintenance job type variant</span></span>  
- <span data-ttu-id="3f83d-115">bakım işi türüyle</span><span class="sxs-lookup"><span data-stu-id="3f83d-115">maintenance job type</span></span>  
- <span data-ttu-id="3f83d-116">bakım işi türü kategorisiyle</span><span class="sxs-lookup"><span data-stu-id="3f83d-116">maintenance job type category</span></span>  
- <span data-ttu-id="3f83d-117">varlıkla</span><span class="sxs-lookup"><span data-stu-id="3f83d-117">asset</span></span>  
- <span data-ttu-id="3f83d-118">varlık türüyle</span><span class="sxs-lookup"><span data-stu-id="3f83d-118">asset type</span></span>  

<span data-ttu-id="3f83d-119">veya bu seçimlerin bir bileşiyle ilgili olabilir.</span><span class="sxs-lookup"><span data-stu-id="3f83d-119">or a combination of those selections.</span></span> <span data-ttu-id="3f83d-120">Aynı kayıt için ne kadar çok seçim yaparsanız, kurulumunuz o kadar belirgin olacaktır.</span><span class="sxs-lookup"><span data-stu-id="3f83d-120">The more selections you make for the same record, the more specific your setup will be.</span></span>

1. <span data-ttu-id="3f83d-121">**Varlık Yönetimi** > **Kurulum** > **Çalışanlar** > **Tercih edilen bakım görevlileri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3f83d-121">Click **Asset management** > **Setup** > **Workers** > **Preferred maintenance workers**.</span></span>

2. <span data-ttu-id="3f83d-122">Yeni bir kayıt oluşturmak için **Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3f83d-122">Click **New** to create a new record.</span></span>

3. <span data-ttu-id="3f83d-123">Yukarıdaki madde işareti listesde gösterilen alanlarda seçim yapılmamış bir "varsayılan" bakım görevlisi veya çalışan grubu kurulumu oluşturarak başlayın.</span><span class="sxs-lookup"><span data-stu-id="3f83d-123">Start by creating a "default" maintenance worker or worker group setup that has no selections in the fields shown in the bullet list above.</span></span> <span data-ttu-id="3f83d-124">Bu, yalnızca **Tercih edilen bakım görevlisi grubu** alanında veya **Tercih edilen bakım görevlisi** alanında seçim yapacağınız anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3f83d-124">This means that you only make a selection in the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field.</span></span> <span data-ttu-id="3f83d-125">Aşağıdaki şekilde, tercih edilen bakım görevlisi grubu olarak "Talepler" in seçildiği bir ilk kayıt örneği görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="3f83d-125">In the figure below, you see an example in the first record in which "Requests" is selected as preferred maintenance worker group.</span></span>

>[!NOTE]
><span data-ttu-id="3f83d-126">Varsayılan kurulum, iş emri planlaması sırasında başka, daha özel kombinasyon iş emrinin içeriğiyle eşleşirse kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="3f83d-126">The default setup will be used during work order scheduling in case no other, more specific, combination matches the contents of the work order during work order scheduling.</span></span>

4. <span data-ttu-id="3f83d-127">Yeni bir kayıt oluşturmak için adım 2'yi tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="3f83d-127">Repeat step 2 to create a new record.</span></span> <span data-ttu-id="3f83d-128">Tercih edilen çalışan veya çalışan grubunun ayrıntı düzeyine bağlı olarak gerekli seçimleri yapın.</span><span class="sxs-lookup"><span data-stu-id="3f83d-128">Make the required selections, depending on the detail level for the preferred worker or worker group.</span></span> <span data-ttu-id="3f83d-129">*Örnek:* Aşağıdaki şekilde, altıncı kayıtta, tercih edilen çalışan olarak bakım görevlisi Shawn Richardson seçilidir.</span><span class="sxs-lookup"><span data-stu-id="3f83d-129">*Example:* In the figure below, in the sixth record, the maintenance worker Shawn Richardson is selected as preferred worker.</span></span> <span data-ttu-id="3f83d-130">Planlanan saatte uygun olması durumunda, "CH-BP1-03-02" varlığı ve "tesis değerlendirmesi " bakım işi türünü içeren bir iş emri planlamasında otomatik olarak seçilecektir.</span><span class="sxs-lookup"><span data-stu-id="3f83d-130">He will automatically be selected during scheduling of a work order that includes the asset "CH-BP1-03-02 and the maintennace job type "Facility assessment", if he is available at the scheduled time.</span></span>

>[!NOTE]
><span data-ttu-id="3f83d-131">Genellikle, iş emri planlama sırasında tercih edilen bir bakım çalışanı seçildiğinde, Varlık Yönetimi olası bir eşleşmeyi denetlemek için tüm **Tercih edilen bakım görevlileri** kayıtlarına bakar ve her zaman en belirgin birleşimi denetler.</span><span class="sxs-lookup"><span data-stu-id="3f83d-131">Generally, when a preferred maintenance worker is selected during work order scheduling, Asset Management goes through all **Preferred maintenance workers** records to check for a possible match, always checking the most specific combination first.</span></span> <span data-ttu-id="3f83d-132">Eşleşme bulunmazsa, **Tercih edilen bakım çalışanı grubu** alanında veya **Tercih edilen bakım çalışanı** alanında bulunan "varsayılan" kayıt kullanılır.</span><span class="sxs-lookup"><span data-stu-id="3f83d-132">If no match is found, the "default" record with a selection in either the **Preferred maintenance worker group** field or the **Preferred maintenance worker** field is used.</span></span>


![Şekil 1](media/02-work-order-scheduling.png)

<span data-ttu-id="3f83d-134">Ayrıca, bakım talebi veya iş emri oluşturulurken seçilebilecek sorumlu bakım çalışanları da ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f83d-134">You can also set up responsible maintenance workers who can be selected when a maintenance request or a work order is created.</span></span> <span data-ttu-id="3f83d-135">**Tüm iş emirleri** ve **Tüm bakım istekleri** alanında gerekirse seçimi düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3f83d-135">In **All work orders** and **All maintenance requests**, you can edit the selection, if required.</span></span> <span data-ttu-id="3f83d-136">Daha fazla bilgi için [Sorumlu bakım çalışanları](../setup-for-maintenance-requests/responsible-workers.md) bölümüne başvurun.</span><span class="sxs-lookup"><span data-stu-id="3f83d-136">Refer to [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md) for more information.</span></span>

<span data-ttu-id="3f83d-137">İş emri planlama sırasında, hangi çalışanların bir iş emriyle ilgili işleri tamamlaması gerektiğini belirlemek için farklı puanlar hesaplanır (bu puanlar,**Varlık yönetimi parametreleri** > **İş emri planlama** bağlantısında ayarlanır).</span><span class="sxs-lookup"><span data-stu-id="3f83d-137">During work order scheduling, different scores are calculated to determine which workers should complete the jobs related to a work order (those scores are set up in **Asset management parameters** > **Work order scheduling** link).</span></span> <span data-ttu-id="3f83d-138">İş emri planlama sırasında iki veya daha fazla tercih edilen bakım çalışanı veya sorumlu bakım çalışanı aynı puanı elde ederse, bir çalışan rasgele seçilir.</span><span class="sxs-lookup"><span data-stu-id="3f83d-138">If two or more preferred maintenance workers or responsible maintenance workers get the same score during work order scheduling, one worker is randomly selected.</span></span> <span data-ttu-id="3f83d-139">Aksi takdirde, iş emrini tamamlamak için tahsis edilen daima en yüksek puanlı çalışan olur.</span><span class="sxs-lookup"><span data-stu-id="3f83d-139">Otherwise, it is always the worker with the highest score who is allocated to complete a work order.</span></span>

