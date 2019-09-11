---
title: Planlı yürütme
description: Bu konuda Varlık Yönetimi'nde zamanlanmış yürütmeyi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8d9c8afc139c96e32efb3161d35fde685b8abcc5
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874682"
---
# <a name="scheduled-execution"></a><span data-ttu-id="df4d9-103">Planlı yürütme</span><span class="sxs-lookup"><span data-stu-id="df4d9-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="df4d9-104">Zamanlanmış yürütmeyi ayarlamak için iş emri servis düzeylerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="df4d9-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="df4d9-105">(İş emri hizmet düzeyleri hakkında daha fazla bilgi için bkz [Hizmet düzeyi ve açıklaması](service-level-and-description.md).) İş emrinin tamamlanması gereken aralık için daha ayrıntılı veya daha az ayrıntılı gereksinimleri ayarlayabileceğiniz için, zamanlanan yürütme, bakım görevlileri için iş planlamasında esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="df4d9-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="df4d9-106">Örneğin, bir üretim aracında beklenenden daha hızlı bir iş tamamlayan bir bakım görevlisi, geçerli hafta için planlanan, ancak geçerli gün için gerekli olan başka bir yakındaki işe geçebilir.</span><span class="sxs-lookup"><span data-stu-id="df4d9-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="df4d9-107">Bu yaklaşım, çalışan planlama ve iş tamamlama işleminin en iyi duruma getirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="df4d9-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="df4d9-108">İş emirleriyle ilgili olan zamanlanmış yürütme kurulumu genel veya özel olabilir.</span><span class="sxs-lookup"><span data-stu-id="df4d9-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="df4d9-109">Belirli iş emri türleri, kıymet türleri, vb. ile sınırlı olmayan genel satırları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="df4d9-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="df4d9-110">Alternatif olarak, belirli bir iş emri türü, kıymet türü, bakım iş türü vb. için geçerli olan planlı yürütme satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="df4d9-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="df4d9-111">**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Planlanmış yürütme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="df4d9-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="df4d9-112">Planlanmış yürütme satırı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="df4d9-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="df4d9-113">**İşlem yapılacak yerleşim**, **İş emri türü**, **Kıymet türü**, **Üretici**, **Model**, **Bakım iş türü kategorisi**, **Bakım iş türü**, **Bakım iş türü varyantı** ve **Ticari** alanlarında, gereksinim duyduğunuz şekilde değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="df4d9-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="df4d9-114">**Servis düzeyi** alanında, bir iş emri servis düzeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="df4d9-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="df4d9-115">Bu alanı boş bırakırsanız, en genel zamanlanmış yürütme satırı türünü yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="df4d9-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="df4d9-116">Genel bir satır örneği için, aşağıdaki çizimdeki ilk kayda bakın.</span><span class="sxs-lookup"><span data-stu-id="df4d9-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="df4d9-117">Bu satır, iş emri servisi düzeyi olmayan tüm iş emirlerinin belirli bir tarih ve saat için zamanlanmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="df4d9-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="df4d9-118">**Zamanlanmış yürütme** alanında zaman aralığını seçin.</span><span class="sxs-lookup"><span data-stu-id="df4d9-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="df4d9-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="df4d9-119">Select **Save**.</span></span>

![Şekil 1](media/20-setup-for-work-orders.png)
