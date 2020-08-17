---
title: Toplu işlerden giden sevkiyatları onayla
description: Bu konuda, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 41dbfb90b7b19c964e725ee0a4c769402414fb17
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652274"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="942f0-103">Toplu işlerden giden sevkiyatları onayla</span><span class="sxs-lookup"><span data-stu-id="942f0-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="942f0-104">Bu konuda, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="942f0-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="942f0-105">Burada açıklanan toplu iş, satış siparişlerine değil, yalnızca transfer emri sevkıyatları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="942f0-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="942f0-106">Toplu işlerden giden sevkiyatları onaylama özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="942f0-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="942f0-107">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="942f0-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="942f0-108">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="942f0-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="942f0-109">Özellik şu şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="942f0-109">The feature is listed as:</span></span>

- <span data-ttu-id="942f0-110">**Modül**  - *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="942f0-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="942f0-111">**Özellik adı** - *Toplu işlerden giden sevkiyatları onaylama*</span><span class="sxs-lookup"><span data-stu-id="942f0-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="942f0-112">Giden sevkiyatları işle</span><span class="sxs-lookup"><span data-stu-id="942f0-112">Process outbound shipments</span></span>

<span data-ttu-id="942f0-113">Sevk edilmeye hazır olan yüklemeler için giden sevkiyat onayını çalıştırmak üzere planlanan bir toplu iş ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="942f0-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="942f0-114">**Ambar yönetimi \> Periyodik görevler\> Giden sevkiyatları işle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="942f0-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="942f0-115">**Sevkiyatı Onayla** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="942f0-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="942f0-116">**Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="942f0-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="942f0-117">Sorgu düzenleyicisi iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="942f0-117">The query editor dialog box opens.</span></span> <span data-ttu-id="942f0-118">**Aralık** sekmesinde, aşağıdaki değerlere sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="942f0-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="942f0-119">**Tablo** - *Yükler*</span><span class="sxs-lookup"><span data-stu-id="942f0-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="942f0-120">**Türetilmiş tablo** - *Yükler*</span><span class="sxs-lookup"><span data-stu-id="942f0-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="942f0-121">**Alan** - *Yük durumu*</span><span class="sxs-lookup"><span data-stu-id="942f0-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="942f0-122">**Kriter** - *Yüklü*</span><span class="sxs-lookup"><span data-stu-id="942f0-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="942f0-123">**Sevkiyatı Onayla** iletişim kutusuna dönmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="942f0-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="942f0-124">**Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** öğesini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="942f0-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="942f0-125">**Arka planda çalıştır** sekmesinde **Tekrar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="942f0-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="942f0-126">**Yinelemeyi tanımlayın** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="942f0-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="942f0-127">İşletmeniz için gereken çalışma zamanlamasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="942f0-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="942f0-128">**Sevkiyatı Onayla** iletişim kutusuna dönmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="942f0-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="942f0-129">Toplu işi toplu iş kuyruğuna eklemek için **Sevkiyatı onayla** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="942f0-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="942f0-130">Daha fazla bilgi için bkz. [Toplu işlemeye genel bakış](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="942f0-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>
