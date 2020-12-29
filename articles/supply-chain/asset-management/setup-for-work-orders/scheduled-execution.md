---
title: Planlı yürütme
description: Bu konuda Varlık Yönetimi'nde zamanlanmış yürütmeyi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439328"
---
# <a name="scheduled-execution"></a><span data-ttu-id="630e0-103">Planlı yürütme</span><span class="sxs-lookup"><span data-stu-id="630e0-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="630e0-104">Zamanlanmış yürütmeyi ayarlamak için iş emri servis düzeylerini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="630e0-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="630e0-105">(İş emri hizmet düzeyleri hakkında daha fazla bilgi için bkz [Hizmet düzeyi ve açıklaması](service-level-and-description.md).) İş emrinin tamamlanması gereken aralık için daha ayrıntılı veya daha az ayrıntılı gereksinimleri ayarlayabileceğiniz için, zamanlanan yürütme, bakım görevlileri için iş planlamasında esneklik sağlar.</span><span class="sxs-lookup"><span data-stu-id="630e0-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="630e0-106">Örneğin, bir üretim aracında beklenenden daha hızlı bir iş tamamlayan bir bakım görevlisi, geçerli hafta için planlanan, ancak geçerli gün için gerekli olan başka bir yakındaki işe geçebilir.</span><span class="sxs-lookup"><span data-stu-id="630e0-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="630e0-107">Bu yaklaşım, çalışan planlama ve iş tamamlama işleminin en iyi duruma getirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="630e0-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="630e0-108">İş emirleriyle ilgili olan zamanlanmış yürütme kurulumu genel veya özel olabilir.</span><span class="sxs-lookup"><span data-stu-id="630e0-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="630e0-109">Belirli iş emri türleri, kıymet türleri, vb. ile sınırlı olmayan genel satırları ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="630e0-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="630e0-110">Alternatif olarak, belirli bir iş emri türü, kıymet türü, bakım iş türü vb. için geçerli olan planlı yürütme satırları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="630e0-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="630e0-111">**Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Planlanmış yürütme**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="630e0-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="630e0-112">Planlanmış yürütme satırı oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="630e0-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="630e0-113">**İşlem yapılacak yerleşim**, **İş emri türü**, **Kıymet türü**, **Üretici**, **Model**, **Bakım iş türü kategorisi**, **Bakım iş türü**, **Bakım iş türü varyantı** ve **Ticari** alanlarında, gereksinim duyduğunuz şekilde değerleri seçin.</span><span class="sxs-lookup"><span data-stu-id="630e0-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="630e0-114">**Servis düzeyi** alanında, bir iş emri servis düzeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="630e0-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="630e0-115">Bu alanı boş bırakırsanız, en genel zamanlanmış yürütme satırı türünü yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="630e0-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="630e0-116">Genel bir satır örneği için, aşağıdaki çizimdeki ilk kayda bakın.</span><span class="sxs-lookup"><span data-stu-id="630e0-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="630e0-117">Bu satır, iş emri servisi düzeyi olmayan tüm iş emirlerinin belirli bir tarih ve saat için zamanlanmasına olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="630e0-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="630e0-118">**Zamanlanmış yürütme** alanında zaman aralığını seçin.</span><span class="sxs-lookup"><span data-stu-id="630e0-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="630e0-119">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="630e0-119">Select **Save**.</span></span>

![Planlı yürütme](media/20-setup-for-work-orders.png)
