---
title: Toplu işlerden giden sevkiyatları onayla
description: Bu konuda, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838454"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a><span data-ttu-id="12f50-103">Toplu işlerden giden sevkiyatları onayla</span><span class="sxs-lookup"><span data-stu-id="12f50-103">Confirm outbound shipments from batch jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12f50-104">Bu konuda, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="12f50-104">This topic describes how to set up a batch job that automatically confirms outbound transfer-order shipments for ready-to-ship loads.</span></span> <span data-ttu-id="12f50-105">Burada açıklanan toplu iş, satış siparişlerine değil, yalnızca transfer emri sevkıyatları için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="12f50-105">The batch job described here only applies to transfer order shipments, not to sales orders.</span></span>

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a><span data-ttu-id="12f50-106">Toplu işlerden giden sevkiyatları onaylama özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="12f50-106">Enable the Confirm outbound shipments from batch jobs feature</span></span>

<span data-ttu-id="12f50-107">Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="12f50-107">Before you can use this feature, it must be enabled on your system.</span></span> <span data-ttu-id="12f50-108">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="12f50-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to check the feature status and enable it if needed.</span></span> <span data-ttu-id="12f50-109">Özellik şu şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="12f50-109">The feature is listed as:</span></span>

- <span data-ttu-id="12f50-110">**Modül**  - *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="12f50-110">**Module** - *Warehouse management*</span></span>
- <span data-ttu-id="12f50-111">**Özellik adı** - *Toplu işlerden giden sevkiyatları onaylama*</span><span class="sxs-lookup"><span data-stu-id="12f50-111">**Feature name** - *Confirm outbound shipments from batch jobs*</span></span>

## <a name="process-outbound-shipments"></a><span data-ttu-id="12f50-112">Giden sevkiyatları işle</span><span class="sxs-lookup"><span data-stu-id="12f50-112">Process outbound shipments</span></span>

<span data-ttu-id="12f50-113">Sevk edilmeye hazır olan yüklemeler için giden sevkiyat onayını çalıştırmak üzere planlanan bir toplu iş ayarlamak için:</span><span class="sxs-lookup"><span data-stu-id="12f50-113">To set up a scheduled batch job to run the outbound shipment confirmation for loads that are ready to ship:</span></span>

1. <span data-ttu-id="12f50-114">**Ambar yönetimi \> Periyodik görevler\> Giden sevkiyatları işle**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="12f50-114">Go to **Warehouse management \> Periodic tasks \> Process outbound shipments**.</span></span>
1. <span data-ttu-id="12f50-115">**Sevkiyatı Onayla** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="12f50-115">The **Confirm shipment** dialog box opens.</span></span> <span data-ttu-id="12f50-116">**Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="12f50-116">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="12f50-117">Sorgu düzenleyicisi iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="12f50-117">The query editor dialog box opens.</span></span> <span data-ttu-id="12f50-118">**Aralık** sekmesinde, aşağıdaki değerlere sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="12f50-118">On the **Range** tab, add a row with the following values:</span></span>
    - <span data-ttu-id="12f50-119">**Tablo** - *Yükler*</span><span class="sxs-lookup"><span data-stu-id="12f50-119">**Table** - *Loads*</span></span>
    - <span data-ttu-id="12f50-120">**Türetilmiş tablo** - *Yükler*</span><span class="sxs-lookup"><span data-stu-id="12f50-120">**Derived table** - *Loads*</span></span>
    - <span data-ttu-id="12f50-121">**Alan** - *Yük durumu*</span><span class="sxs-lookup"><span data-stu-id="12f50-121">**Field** - *Load status*</span></span>
    - <span data-ttu-id="12f50-122">**Kriter** - *Yüklü*</span><span class="sxs-lookup"><span data-stu-id="12f50-122">**Criteria** - *Loaded*</span></span>
1. <span data-ttu-id="12f50-123">**Sevkiyatı Onayla** iletişim kutusuna dönmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f50-123">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="12f50-124">**Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** öğesini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f50-124">On the **Run in the background** FastTab, set **Batch processing** to **Yes**.</span></span>
1. <span data-ttu-id="12f50-125">**Arka planda çalıştır** sekmesinde **Tekrar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f50-125">On the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="12f50-126">**Yinelemeyi tanımlayın** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="12f50-126">The **Define recurrence** dialog box opens.</span></span> <span data-ttu-id="12f50-127">İşletmeniz için gereken çalışma zamanlamasını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="12f50-127">Set the run schedule as needed for your business.</span></span>
1. <span data-ttu-id="12f50-128">**Sevkiyatı Onayla** iletişim kutusuna dönmek için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f50-128">Select **OK** to return to the **Confirm shipment** dialog box.</span></span>
1. <span data-ttu-id="12f50-129">Toplu işi toplu iş kuyruğuna eklemek için **Sevkiyatı onayla** iletişim kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="12f50-129">Select **OK** on the **Confirm shipment** dialog box to add the batch job to the batch queue.</span></span>

<span data-ttu-id="12f50-130">Daha fazla bilgi için bkz. [Toplu işlemeye genel bakış](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span><span class="sxs-lookup"><span data-stu-id="12f50-130">For more information, see [Batch processing overview](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]