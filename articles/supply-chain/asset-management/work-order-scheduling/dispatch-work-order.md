---
title: İş emri gönderme
description: Bu konuda Varlık Yönetimi'nde iş emri gönderme işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetScheduledExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d46beb04923d06aa8ccec05355731aa1b3f27c5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439122"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="372a2-103">İş emri gönderme</span><span class="sxs-lookup"><span data-stu-id="372a2-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="372a2-104">**Gönder** işlevini kullanarak bir iş emri veya iş emri işlerini bir çalışana zamanlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="372a2-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="372a2-105">**Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="372a2-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="372a2-106">Listeden iş emrini seçin. </span><span class="sxs-lookup"><span data-stu-id="372a2-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="372a2-107">**Genel** sekmesinde, **Gönder** seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="372a2-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="372a2-108">**İş emrini zamanla** iletişim kutusunda **Çalışan** alanından çalışanı seçin.</span><span class="sxs-lookup"><span data-stu-id="372a2-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="372a2-109">**Saatleri zamanla** alanında, beklenen çalışma saatlerinin tahmin saatlerinden farklı olması durumunda beklenen çalışma saatleri ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="372a2-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="372a2-110">**Planlanan başlangıç** alanında, gerekirse başlangıç tarihi ve saatini düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="372a2-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="372a2-111">Planlama işlemi başka işlerde zaten zamanlanmış olan kaynaklarla ilgili kapasite sınırlamalarını gözlemlemek zorundaysa **Varlık**, **Araç** ve **Çalışan** düğmelerinin **Evet** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="372a2-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="372a2-112">Planlama işlemiyle ilgili ayrıntılı bilgi görmek istiyorsanız, **Ayrıntılı** düğmesinde **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="372a2-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="372a2-113">Bu, iş emrindeki hesaplanan puanlar hakkında ayrıntılı bilginin Bilgi günlüğünde gösterildiği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="372a2-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="372a2-114">Takvimdeki kapatılmış günleri yok saymak için **Zamanlamayı yoksay** düğmesini **Evet** olarak ayarlayın (varlık, çalışan ve araçlara uygulanır).</span><span class="sxs-lookup"><span data-stu-id="372a2-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="372a2-115">Planlamayla ilgili iş emrinde seçilmiş olabilecek sınırlamaları yok saymak için **Planlı yürütmeyi yoksay** düğmesini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="372a2-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="372a2-116">Zamanlanmış yürütme kurulumu hakkında bilgi için bkz. [Zamanlanmış yürütme](../setup-for-work-orders/scheduled-execution.md) bölümü.</span><span class="sxs-lookup"><span data-stu-id="372a2-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="372a2-117">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="372a2-117">Click **OK**.</span></span> <span data-ttu-id="372a2-118">İş emri yaşam döngüsü durumu otomatik olarak belirtilen **Zamanlandı** yaşam döngüsü durumuna güncelleştirilir **Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Yaşam döngüsü modelleri**.</span><span class="sxs-lookup"><span data-stu-id="372a2-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="372a2-119">Aşağıdaki şekilde, **İş emrini zamanla** iletişim kutusundaki gönderme seçimlerinin bir örneği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="372a2-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Şekil 1](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="372a2-121">Bir iş emrindeki zamanlamayı silmek istiyorsanız, **Genel** sekmesinde **Tüm iş emirleri**'nden iş emrini seçip **Zamanlamayı sil**'e tıklayın. Zamanlamayı silerseniz iş emri yaşam döngüsü durumunu el ile güncelleştirmeyi unutmayın.</span><span class="sxs-lookup"><span data-stu-id="372a2-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

