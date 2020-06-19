---
title: İş kartı cihazından tamamlandı olarak bildirme
description: Bu konuda, bir iş kartı kullanıcıları bir üretim emrinden stoka bitmiş ürünleri raporlenebilecek şekilde sistemi konfigüre etme yöntemi açıklanmıştır.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403274"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="c1c39-103">İş kartı cihazından tamamlandı olarak bildirme</span><span class="sxs-lookup"><span data-stu-id="c1c39-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1c39-104">Çalışanlar, bir üretim işi için tamamlanan miktarları bildirmek üzere, iş kartı aygıtındaki **rapor ilerleme** sayfasını kullanır.</span><span class="sxs-lookup"><span data-stu-id="c1c39-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="c1c39-105">Tamamlandı olarak rapor edilen miktarların stoğa eklenip eklenmeyeceğini denetleme</span><span class="sxs-lookup"><span data-stu-id="c1c39-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="c1c39-106">Son operasyonda tamamlandı olarak rapor edilen miktarların stoğa eklenmesi gerekip alınıp alınmayacağını denetlemek için, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="c1c39-107">**Üretim denetimi \> Kurulum \> Üretim yürütme \> Üretim emri varsayılanları** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="c1c39-108">**Tamamlandı bildirimi** sekmesinde, **güncelleştirme tamamlandı raporu çevrimiçi** alanını aşağıdaki değerlerden birine ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="c1c39-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="c1c39-109">**Hayır** – Son operasyonda miktar raporlandığında stoğa hiçbir miktar eklenmez.</span><span class="sxs-lookup"><span data-stu-id="c1c39-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="c1c39-110">Üretim emrinin durumu hiçbir zaman değişmeyecek.</span><span class="sxs-lookup"><span data-stu-id="c1c39-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="c1c39-111">**Durum + Miktar** - Üretim emrinin durumu *tamamlandı bildirimi* olarak değişecektir ve miktar stoka tamamlandı olarak bildirilir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="c1c39-112">**Miktar** - Miktar, envantere durumu tamamlandı bildirimi olarak değişecektir ancak üretim emri asla değişmez.</span><span class="sxs-lookup"><span data-stu-id="c1c39-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="c1c39-113">**Durum** - Yalnızca Üretim emrinin durumu değişir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="c1c39-114">Son operasyonda miktar raporlandığında stoğa hiçbir miktar eklenmez.</span><span class="sxs-lookup"><span data-stu-id="c1c39-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="c1c39-115">Tamamlandı olarak raporlandığı operasyonlar son operasyon olarak tanımlanmazsa, miktarlar stokta izlenmiyor.</span><span class="sxs-lookup"><span data-stu-id="c1c39-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="c1c39-116">Ancak, ilerlemeyi görüntülemek için bu miktarlar kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="c1c39-117">Bunlar aynı zamanda, önceki operasyonda bildirilen rapor edilen bir eşiğe ulaşılmadan önce çalışanların sonraki operasyonu başlatıp başlatmayacağını denetleyen kurallara dahil edilebilir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="c1c39-118">Bu kuralları , **üretim emri Varsayılanları** sayfasının **miktar doğrulama** sekmesinde tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c1c39-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="c1c39-119">**Üretim emri Varsayılanları** sayfasıyla nasıl çalışılacağı hakkında daha fazla bilgi için [üretim yürütmesindeki üretim parametrelerine](production-parameters-manufacturing-execution.md) bakın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="c1c39-120">Toplu denetimli maddeleri tamamlandı olarak raporla</span><span class="sxs-lookup"><span data-stu-id="c1c39-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="c1c39-121">İş kartı aygıtı toplu iş maddelerini raporlamak için üç senaryoyu destekler.</span><span class="sxs-lookup"><span data-stu-id="c1c39-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="c1c39-122">Bu senaryolar, hem Gelişmiş ambar süreçleri için etkinleştirilen maddelere hem de Gelişmiş ambar işlemleri için etkinleştirilmemiş maddelere uygulanır.</span><span class="sxs-lookup"><span data-stu-id="c1c39-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="c1c39-123">**El ile atanan toplu iş numaraları:** Çalışanlar özel bir toplu iş numarası girin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="c1c39-124">Bu toplu iş numarası, sistemde bilinmeyen bir harici kaynaktan gelebilir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="c1c39-125">**Önceden tanımlı toplu iş numaraları:** Çalışanlar, üretim emri iş kartı aygıtında serbest bırakılmadan önce sistemin otomatik olarak oluşturduğu toplu iş numaraları listesinde bir toplu iş numarası seçer.</span><span class="sxs-lookup"><span data-stu-id="c1c39-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="c1c39-126">**Sabit toplu iş numaraları:** Çalışanlar toplu iş numarası girmez veya seçmez.</span><span class="sxs-lookup"><span data-stu-id="c1c39-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="c1c39-127">Bunun yerine, sistem üretim emrine serbest bırakılmadan önce bir toplu iş numarası atar.</span><span class="sxs-lookup"><span data-stu-id="c1c39-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="c1c39-128">Her Senaryoyu etkinleştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="c1c39-129">**Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c1c39-130">Yapılandırmak istediğiniz ürünü seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-130">Select the product to configure.</span></span>
1. <span data-ttu-id="c1c39-131">**Stoğu Yönet** hızlı sekmesinde, **toplu iş numarası grubu** alanında, senaryonuzu destekleyecek izleme numara grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="c1c39-132">Varsayılan olarak, toplu denetlenen bir ürüne toplu iş numarası grubu atanmamışsa, iş kartı aygıtı tamamlandı bildirimi sırasında toplu iş numarası için el ile giriş sağlar.</span><span class="sxs-lookup"><span data-stu-id="c1c39-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="c1c39-133">Aşağıdaki alt kısımlar, toplu iş öğelerinde raporlama için üç senaryonun her birini desteklemek üzere izleme numarası gruplarının nasıl ayarlanacağını açıklar.</span><span class="sxs-lookup"><span data-stu-id="c1c39-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="c1c39-134">İş kartı aygıtında toplu iş numarası raporlamayı etkinleştir</span><span class="sxs-lookup"><span data-stu-id="c1c39-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="c1c39-135">İş kartı aygıtlarınızın tamamlandı bildirimi sırasında bir toplu iş numarası kabul etmesini sağlamak için, [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanarak aşağıdaki özellikleri (Bu sırada) açmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="c1c39-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="c1c39-136">İş Kartı Cihazındaki Rapor ilerlemesi iletişim kutusu için geliştirilmiş kullanıcı deneyimi.</span><span class="sxs-lookup"><span data-stu-id="c1c39-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="c1c39-137">İş Kartı Cihazında (Önizleme) bitmiş olarak raporlarken toplu iş ve seri numaralarını girmek için etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="c1c39-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="c1c39-138">Çalışanlarınızın el ile bir toplu iş numarası atayabilmesine olanak veren bir izleme numarası grubu ayarla</span><span class="sxs-lookup"><span data-stu-id="c1c39-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="c1c39-139">El ile atanan toplu iş numaralarına izin vermek için, bir izleme numarası grubu ayarlamak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="c1c39-140">**Stok Yönetimi \> Kurulum \> Boyut \> zleme numara gruplarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="c1c39-141">Ayarlanacak izleme grubu grubunu oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="c1c39-142">**Genel** hızlı sekmesinde, **Manuel** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="c1c39-143">![Numara gruplarını izleme sayfası](media/tracking-number-group-manual.png "Numara gruplarını izleme sayfası")</span><span class="sxs-lookup"><span data-stu-id="c1c39-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="c1c39-144">İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan Ürünler için toplu iş numarası grubu olarak bu izleme numara grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="c1c39-145">Bu senaryoyu kullandığınızda, iş kartı aygıtında **durumu raporla** sayfasının sağladığı **toplu iş numarası** alanı çalışanların herhangi bir değer girebildiği bir metin kutusudur.</span><span class="sxs-lookup"><span data-stu-id="c1c39-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="c1c39-146">![El ile toplu iş numarası için alan bulunan ilerleme durumu sayfasını raporla](media/job-card-device-batch-manual.png "El ile toplu iş numarası için alan bulunan ilerleme durumu sayfasını raporla")</span><span class="sxs-lookup"><span data-stu-id="c1c39-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="c1c39-147">Önceden tanımlanmış toplu iş numaralarının listesini sağlayan bir izleme numarası grubu ayarla</span><span class="sxs-lookup"><span data-stu-id="c1c39-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="c1c39-148">Önceden tanımlanmış toplu iş numaraları listesi sağlamak için bir izleme numarası grubu ayarlamak üzere aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="c1c39-149">**Stok Yönetimi \> Kurulum > Boyut \> İzleme numara gruplarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="c1c39-150">Ayarlanacak izleme grubu grubunu oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="c1c39-151">**Genel** hızlı sekmesinde, **Yalnızca envanter işlemleri için** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="c1c39-152">Miktar bazında toplu iş numaralarını, girdiğiniz değere göre, **her miktarda** ayırmak için kullanın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="c1c39-153">Örneğin, on parça için bir üretim emri, **Her miktar** alanı *2* olarak ayarlanmış.</span><span class="sxs-lookup"><span data-stu-id="c1c39-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="c1c39-154">Bu durumda üretim emrine oluşturulurken beş toplu iş numarası atanacaktır.</span><span class="sxs-lookup"><span data-stu-id="c1c39-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="c1c39-155">![Numara gruplarını izleme sayfası](media/tracking-number-group-predefined.png "Numara gruplarını izleme sayfası")</span><span class="sxs-lookup"><span data-stu-id="c1c39-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="c1c39-156">İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan Ürünler için toplu iş numarası grubu olarak bu izleme numara grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="c1c39-157">Bu senaryoyu kullandığınızda, iş kartı aygıtında **durumu raporla** sayfasının sağladığı **toplu iş numarası** alanı çalışanların önceden tanımlanan değer girebildiği bir açılır listedir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="c1c39-158">![Önceden tanımlanan toplu iş numaraları listesi için alan bulunan ilerleme durumu sayfasını raporla](media/job-card-device-batch-predefined.png "Önceden tanımlanan toplu iş numaraları listesi için alan bulunan ilerleme durumu sayfasını raporla")</span><span class="sxs-lookup"><span data-stu-id="c1c39-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="c1c39-159">Otomatik olarak toplu iş numarası atayabilmesine olanak veren bir izleme numarası grubu ayarla</span><span class="sxs-lookup"><span data-stu-id="c1c39-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="c1c39-160">Toplu iş numaralarının çalışan girişi olmadan otomatik olarak atanması gerekiyorsa, bir izleme numarası grubu ayarlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="c1c39-161">**Stok Yönetimi \> Kurulum \> Boyut \> zleme numara gruplarına** gidin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="c1c39-162">Ayarlanacak izleme grubu grubunu oluşturun veya seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="c1c39-163">**Genel** hızlı sekmesinde, **Yalnızca envanter işlemleri için** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="c1c39-164">**Manuel**seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="c1c39-165">![Numara gruplarını izleme sayfası](media/tracking-number-group-fixed.png "Numara gruplarını izleme sayfası")</span><span class="sxs-lookup"><span data-stu-id="c1c39-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="c1c39-166">İstediğiniz şekilde diğer değerleri ayarlayın, sonra da bu senaryoyu kullanmak istediğiniz serbest bırakılan Ürünler için toplu iş numarası grubu olarak bu izleme numara grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="c1c39-167">Bu senaryoyu kullandığınızda, iş kartı aygıtında **durumu raporla** sayfasının sağladığı **toplu iş numarası** alanı bir değer gösterir ancak çalışanlar düzenleymez.</span><span class="sxs-lookup"><span data-stu-id="c1c39-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="c1c39-168">![Sabit toplu iş numarası ile ilerleme durumu sayfasını raporla](media/job-card-device-batch-fixed.png "Sabit toplu iş numarası ile ilerleme durumu sayfasını raporla")</span><span class="sxs-lookup"><span data-stu-id="c1c39-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="c1c39-169">Lisans plakasına tamamlandı olarak raporlama</span><span class="sxs-lookup"><span data-stu-id="c1c39-169">Report as finished to a license plate</span></span>

<span data-ttu-id="c1c39-170">Gelişmiş ambar işlemleri, bu amaçla ayarlanmış ambar yerleşimlerinde bulunan stoğu izlemek için, lisans levhası boyutunu kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="c1c39-171">Bu durumda, bir çalışanın tamamlandığı miktarları raporladığında, lisans levhası numarası gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c1c39-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="c1c39-172">Raporlama ve Plaka etiketi yazdırmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="c1c39-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="c1c39-173">Bu bölümde anlatılan özellikleri kullanmak için, [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanarak aşağıdaki özellikleri (Bu sırada) açmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="c1c39-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="c1c39-174">İş Kartı Cihazına eklenen tamamlandı olarak işaretleme plakası</span><span class="sxs-lookup"><span data-stu-id="c1c39-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="c1c39-175">İş kartı cihazında tamamlandı olarak bildirme sırasında otomatik plaka numarası oluşturmayı etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="c1c39-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="c1c39-176">İş Kartı Cihazından etiket yazdır</span><span class="sxs-lookup"><span data-stu-id="c1c39-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="c1c39-177">Lisans plakasına tamamlandı olarak raporlamayı ayarla</span><span class="sxs-lookup"><span data-stu-id="c1c39-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="c1c39-178">Çalışanların varolan bir lisans plağı 'nı yeniden kullanması veya miktarları tamamlandı olarak raporlarına yeni bir lisans plağı oluşturup oluşturmayacağını denetlemek için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="c1c39-179">**Üretim denetimi \> Ayarlar \> Üretim yürütme \> Cihazlar için iş kartını konfigüre et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="c1c39-180">Her aygıt için aşağıdaki seçenekleri belirleyin:</span><span class="sxs-lookup"><span data-stu-id="c1c39-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="c1c39-181">**Lisans levhasını oluştur** - Her tamamlandı bildirimi oluşturmak için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="c1c39-182">Her bir rapor tamamlandı bildirimi için mevcut bir lisans kalıbının kullanılması gerekiyorsa **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="c1c39-183">**Etiket Yazdır** - bir çalışan bir çalışma tamamlandı bildirimi yapmak için bu seçeneği **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="c1c39-184">Etiket gerekmiyorsa **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="c1c39-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="c1c39-185">![Cihazlar için iş kartını yapılandırma sayfası](media/config-job-card-raf.png "Cihazlar için iş kartını yapılandırma sayfası")</span><span class="sxs-lookup"><span data-stu-id="c1c39-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="c1c39-186">Etiekt yapılandırmak içni **Ambar Yönetimi \> Kurulum \> Belge yönlendirme \> Belge yönlendirme**'ye gidin.</span><span class="sxs-lookup"><span data-stu-id="c1c39-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="c1c39-187">Daha fazla bilgi için, bkz [Lisans plaka etiket yazdırmayı etkinleştir](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="c1c39-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
