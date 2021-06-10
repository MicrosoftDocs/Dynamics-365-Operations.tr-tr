---
title: Dalga etiketi yazdırma
description: Bu konu, dalga etiketi yazdırma özelliğini ve bunu nasıl ayarlayabileceğinizi açıklamaktadır.
author: perlynne
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSDocumentRouting, WHSWaveTableListPage, WHSPostMethod, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelType, WHSWaveLabelTemplateGroup, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: yyyy-mm-dd
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 14a32f7fc4608ef8910646f80786a188c46dc89d
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102626"
---
# <a name="wave-label-printing"></a><span data-ttu-id="e4e75-103">Dalga etiketi yazdırma</span><span class="sxs-lookup"><span data-stu-id="e4e75-103">Wave label printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4e75-104">Dalga etiketi yazdırma özelliği, dalga yürütme sırasında doğrudan dalga şablonundan etiket oluşturup yazdırmanıza olanak sağlayan yeni bir dalga adımı yöntemi sunarak, etiket yazdırmaya alternatif bir yaklaşım sunar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-104">Wave label printing offers an alternative approach to label printing by introducing a new wave step method that lets you create and print labels directly from the wave template during wave execution.</span></span> <span data-ttu-id="e4e75-105">Böylece, çalışanlar bir mobil cihazda iş emrini çalıştırmadan önce etiketler kullanılabilir durumda olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-105">Therefore, the labels will already be available before workers run the work order on a mobile device.</span></span> <span data-ttu-id="e4e75-106">Çalışanlar, gerekli etiketleri malzeme çekme sonrasında değil malzeme çekme sırasında ekleyebilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-106">Workers can then attach the required labels during picking instead of after picking.</span></span>

<span data-ttu-id="e4e75-107">Dalga etiketi yazdırma etiket düzenleri oluşturmak için Zebra Programlama Dili (ZPL) kullanır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-107">Wave label printing uses Zebra Programming Language (ZPL) to create label layouts.</span></span> <span data-ttu-id="e4e75-108">Etiket düzeni, yinelenen yapıya sahip etiketlere izin vermek üzere üç bölüme (üstbilgi, gövde ve altbilgi) bölünmüştür.</span><span class="sxs-lookup"><span data-stu-id="e4e75-108">A label layout is divided into three sections (header, body, and footer) to allow for labels that have repeating structure.</span></span> <span data-ttu-id="e4e75-109">Dalga etiketi şablonları sisteme hangi etiket düzeninin kullanılacağını söyler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-109">Wave label templates tell the system which label layout to use.</span></span> <span data-ttu-id="e4e75-110">Kullanıcılar hangi yazıcının kullanılacağını belirtebilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-110">Users can specify which printer is used.</span></span> <span data-ttu-id="e4e75-111">Ayrıca, gerekirse etiketleri aynı anda birçok yazıcıda da yazdırabilirler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-111">They can also print labels on several printers at the same time, as they require.</span></span> <span data-ttu-id="e4e75-112">**Dalga etiketi geçmişi** sayfası, bu kurulum kullanılarak oluşturulmuş tüm etiketlerin kayıtlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-112">The **Wave label history** page shows a record of all labels that have been created by using this setup.</span></span>

<span data-ttu-id="e4e75-113">Etiketleri iş başlıklarına göre yazdırabilir ve harmanlayabilir, her iş başlığı için kesme etiketleri yazdırabilir ve konteyner içerik etiketlerini, kutu etiketlerini ve diğer benzer etiketleri yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-113">You can print and collate labels based on work headers, you can print break labels per work header, and you can print container content labels, case labels, and other similar labels.</span></span>

> [!NOTE]
> <span data-ttu-id="e4e75-114">Bu işlev, belge yönlendirmeyi temel alan mevcut etiket yazdırma işlevinin yerini almaz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-114">This functionality doesn't replace existing label printing functionality that is based on document routing.</span></span>

<span data-ttu-id="e4e75-115">Dalga etiketi yazdırma özelliği aşağıdaki geliştirmeleri sunar:</span><span class="sxs-lookup"><span data-stu-id="e4e75-115">Wave label printing offers the following enhancements:</span></span>

- <span data-ttu-id="e4e75-116">Etiketleri, tek bir iş satırındaki koli sayısına göre konteyner kullanımı olmadanyazdırın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-116">Print labels according to the number of cartons on a single work line, without using containerization.</span></span> <span data-ttu-id="e4e75-117">(Bir "koli", birim sıra grubu satırlarında belirlenmiş bir birimdir.)</span><span class="sxs-lookup"><span data-stu-id="e4e75-117">(A "carton" is a unit that is designated on unit sequence group lines.)</span></span>
- <span data-ttu-id="e4e75-118">Birkaç farklı etiket sırasını (örneğin, karton ve palet etiketleri) yazdırın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-118">Print several different label sequences (for example, carton and pallet labels).</span></span>
- <span data-ttu-id="e4e75-119">Etiket numaralandırmasını (örneğin, 1/124, 2/124,... 124/124) dahil edin ve numaralandırma aralığını tanımlayın (örneğin iş satırı, yük satırı veya sevkiyat).</span><span class="sxs-lookup"><span data-stu-id="e4e75-119">Include label enumeration (for example, 1/124, 2/124, ... 124/124), and define the range of enumeration (for example, work line, load line, or shipment).</span></span>
- <span data-ttu-id="e4e75-120">Konşimento oluşturulmadan önce, bir konşimento kodu oluşturun ve etiketlere yazdırın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-120">Create and print a bill of lading ID on labels before the bill of lading is generated.</span></span>
- <span data-ttu-id="e4e75-121">Her koli için benzersiz bir seri sevkiyat konteyner kodu (SSCC) oluşturun ve her etikete ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-121">Create a unique serial shipping container code (SSCC) for each carton, and include it on each label.</span></span>
- <span data-ttu-id="e4e75-122">Konşimento kodları ve SSCC'ler için GS1-uyumlu numara serileri oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e4e75-122">Create GS1-compliant number sequences for bill of lading IDs and SSCCs.</span></span>
- <span data-ttu-id="e4e75-123">Etiketleri hem mobil uygulamadan hem de zengin istemciden yeniden yazdırın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-123">Reprint labels from both mobile devices and the rich client.</span></span>
- <span data-ttu-id="e4e75-124">Etiketleri hükümsüz kılın (örneğin, eksik çekme senaryolarında) ve yeniden yazdırın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-124">Void labels (for example, in short pick scenarios), and reprint them.</span></span>
- <span data-ttu-id="e4e75-125">Dalga etiketi geçmişini temizleme.</span><span class="sxs-lookup"><span data-stu-id="e4e75-125">Clean up the wave label history.</span></span>
- <span data-ttu-id="e4e75-126">Belge yönlendirme düzenlerinde yapılan geliştirmeler, belge yönlendirme düzenleri ile dalga etiketi düzenleri arasında paylaşılır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-126">Improvements to document routing layouts are shared between document routing layouts and wave label layouts.</span></span> <span data-ttu-id="e4e75-127">(Daha fazla bilgi için bkz. [Plakalar için belge yönlendirme düzeni](../warehousing/document-routing-layout-for-license-plates.md).)</span><span class="sxs-lookup"><span data-stu-id="e4e75-127">(For more information, see [Document routing layout for license plates](../warehousing/document-routing-layout-for-license-plates.md).)</span></span>

<span data-ttu-id="e4e75-128">Bu geliştirmeler, paletlemeden önce kolileri etiketlemeyi daha etkili hale getirir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-128">These enhancements make it more efficient to label cartons before palletization.</span></span> <span data-ttu-id="e4e75-129">Bunlar özellikle, her koliyi ayrı olarak tarayıp sipariş girişlerini otomatik olarak onaylayan büyük perakendecilere sevkiyat yapan şirketler için yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-129">They especially benefit companies that ship to large retailers that automatically confirm order receipts by scanning each carton separately.</span></span>

> [!NOTE]
> <span data-ttu-id="e4e75-130">İş gereksinimlerinize bağlı olarak, bu konuda açıklanan yapılandırma senaryolarını ayrı olarak veya birlikte uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-130">You can implement the configuration scenarios that are described in this topic either separately or in combination, depending on your business requirements.</span></span> <span data-ttu-id="e4e75-131">Sırayla çalışan birkaç dalga etiketi şablonu (senaryo 3'te gösterildiği gibi) tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-131">You can design several wave label templates that work in sequence (as illustrated in scenario 3).</span></span> <span data-ttu-id="e4e75-132">Örneğin, koli etiketlerini yazdırmak için senaryo 1'i, palet etiketleri yazdırmak için de senaryo 2'yi kullanabilirsiniz (stoktaki paletler boyut ve kompozisyon olarak farklılık gösteriyorsa).</span><span class="sxs-lookup"><span data-stu-id="e4e75-132">For example, you can use scenario 1 to print carton labels and scenario 2 to print pallet labels (if pallets in stock vary in size and composition).</span></span>

## <a name="turn-on-the-wave-label-printing-feature"></a><span data-ttu-id="e4e75-133">Dalga etiketi yazdırma özelliğini açma</span><span class="sxs-lookup"><span data-stu-id="e4e75-133">Turn on the Wave label printing feature</span></span>

<span data-ttu-id="e4e75-134">*Dalga etiketi yazdırma* özelliğini kullanabilmeniz için sisteminizde etkinleştirilmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-134">Before you can use the *Wave label printing* feature, it must be turned on in your system.</span></span> <span data-ttu-id="e4e75-135">Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanını kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-135">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e4e75-136">Burada, özellik aşağıdaki şekilde listelenmiştir:</span><span class="sxs-lookup"><span data-stu-id="e4e75-136">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e4e75-137">**Modül:** *Ambar yönetimi*</span><span class="sxs-lookup"><span data-stu-id="e4e75-137">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e4e75-138">**Özellik adı:** *Dalga etiketi yazdırma*</span><span class="sxs-lookup"><span data-stu-id="e4e75-138">**Feature name:** *Wave label printing*</span></span>

## <a name="scenario-1-wave-label-printing-where-a-single-wave-label-is-generated"></a><span data-ttu-id="e4e75-139">Senaryo 1: Tek bir dalga etiketinin oluşturulduğu dalga etiketi yazdırma</span><span class="sxs-lookup"><span data-stu-id="e4e75-139">Scenario 1: Wave label printing where a single wave label is generated</span></span>

<span data-ttu-id="e4e75-140">Bu senaryoda, bir şirketin sipariş girişlerini her koliyi ayrı olarak tarayarak otomatik onaylayan büyük bir perakendeci için sevkiyat etiketlerini nasıl yazdırabileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-140">This scenario shows how a company can print shipping labels for a large retailer that automatically confirms order receipts by scanning each carton separately.</span></span>

<span data-ttu-id="e4e75-141">Bu senaryo uçtan uca akışı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-141">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e4e75-142">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="e4e75-142">Make demo data available</span></span>

<span data-ttu-id="e4e75-143">Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-143">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="e4e75-144">Dalga etiketi yönteminin kullanılabilir olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="e4e75-144">Make sure that the wave label method is available</span></span>

<span data-ttu-id="e4e75-145">Dalga etiketi yazdırma yöntemini kullanılabilir hale getirmek için dalga işlemi yöntemlerini yeniden oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-145">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="e4e75-146">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-146">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="e4e75-147">**waveLabelPrinting** öğesinin listede olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-147">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="e4e75-148">Seçili değilse, eklemek Için eylem bölmesindeki **Yöntemleri yeniden üret**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-148">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="configure-a-wave-template"></a><span data-ttu-id="e4e75-149">Dalga şablonu yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e4e75-149">Configure a wave template</span></span>

<span data-ttu-id="e4e75-150">Dalga şablonları, belirli dalga yöntemi örneklerini ilgili dalga etiketi şablonuna bağlayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-150">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="e4e75-151">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="e4e75-152">**62 Sevkiyat Varsayılanı** gibi bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-152">Select a template, such as **62 Shipping Default**.</span></span>
1. <span data-ttu-id="e4e75-153">**Yöntemler** hızlı sekmesinde, **Dalga etiketi yazdırma** yöntemini **Seçili yöntemler** sütununa taşıyın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-153">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="e4e75-154">**Seçili Yöntemler** sütununda, **Dalga etiketi yazdırma** yöntemini seçin ve **Dalga adımı kodu** alanını *PrintLabel* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-154">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="e4e75-155">Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-155">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="e4e75-156">Dalga etiketi düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-156">Create a wave label layout</span></span>

<span data-ttu-id="e4e75-157">Etiket düzeni, etiket üzerine hangi bilgilerin basıldığını ve bunun nasıl yerleştirileceğini denetler. Buraya, yazıcıya gönderilen ZPL kodunu girersiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-157">The label layout controls what information is printed on the label and how it's laid out. Here, you enter the ZPL code that is sent to the printer.</span></span>

1. <span data-ttu-id="e4e75-158">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi düzenleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-158">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="e4e75-159">Aşağıdaki ayarlara sahip bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-159">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-160">**Etiket düzeni kodu:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-160">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-161">**Açıklama:** *Koli (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="e4e75-161">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="e4e75-162">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-162">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-163">Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-163">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4e75-164">**Dalga etiketi satır ayarları** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-164">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4e75-165">Burada, etiketin dinamik parçasını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-165">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4e75-166">Aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-166">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-167">**Satır kodu:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-167">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="e4e75-168">**Satır tablosu adı:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-168">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="e4e75-169">**Satır başlangıç konumu:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4e75-169">**Row start position:** *0*</span></span>

        <span data-ttu-id="e4e75-170">Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-170">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4e75-171">**Satır yüksekliği:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4e75-171">**Row height:** *0*</span></span>

        <span data-ttu-id="e4e75-172">Bu alan, ZPL standardına göre her satırın yüksekliğini (punto olarak) tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-172">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="e4e75-173">Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-173">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="e4e75-174">Bu örnekte tek bir satır olduğu için, değeri *0* (sıfır) olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-174">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="e4e75-175">**Sayfa başına satır:** *1*</span><span class="sxs-lookup"><span data-stu-id="e4e75-175">**Rows per page:** *1*</span></span>

        <span data-ttu-id="e4e75-176">Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-176">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4e75-177">Bu kurulum, dalga etiketleri tablosundaki her kayıt için ayrı bir ZPL etiketinin yazdırılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-177">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="e4e75-178">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-178">Close the page.</span></span>
1. <span data-ttu-id="e4e75-179">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-179">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4e75-180">Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-180">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-181">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-181">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-182">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-182">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-183">**Alan:** *İş türü*</span><span class="sxs-lookup"><span data-stu-id="e4e75-183">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4e75-184">**Ölçüt:** *Malzeme çekme*</span><span class="sxs-lookup"><span data-stu-id="e4e75-184">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="e4e75-185">Bu sorgu yalnızca çekme türü iş satırlarının etiket üzerine yazdırılmasını (yerine koyma türü iş satırları değil) sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-185">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="e4e75-186">Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-186">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="e4e75-187">Sorgu düzenleyicisi iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-187">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4e75-188">**Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**.</span><span class="sxs-lookup"><span data-stu-id="e4e75-188">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4e75-189">**Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-189">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4e75-190">Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-190">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="e4e75-191">**Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-191">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4e75-192">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-192">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="e4e75-193">**Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-193">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4e75-194">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-194">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4e75-195">Bu kurulum her etiketin bir kopyasını yazdırır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-195">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4e75-196">Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-196">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4e75-197">Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-197">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="e4e75-198">Etiketiniz şimdi kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-198">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-type"></a><span data-ttu-id="e4e75-199">Dalga etiketi türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-199">Create a wave label type</span></span>

<span data-ttu-id="e4e75-200">Dalga etiketi türleri, dalga etiketi şablonlarını birim dizi grubu satırlarındaki bir birime bağlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-200">Wave label types are used to link wave label templates to a unit on unit sequence group lines.</span></span>

1. <span data-ttu-id="e4e75-201">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-201">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="e4e75-202">Aşağıdaki ayarlara sahip bir dalga etiketi türü ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-202">Add a wave label type that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-203">**Etiket türü:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-203">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-204">**Açıklama:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-204">**Description:** *Carton*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="e4e75-205">Birim sıra gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="e4e75-205">Set up unit sequence groups</span></span>

<span data-ttu-id="e4e75-206">Sonra, dalga etiketi türü için birim sırası grubunu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-206">Next, set up the unit sequence group for the wave label type.</span></span>

1. <span data-ttu-id="e4e75-207">**Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri\> Birim sırası grubu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-207">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="e4e75-208">**Ea Kutu PL** grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-208">Select the **Ea Box PL** group.</span></span>
1. <span data-ttu-id="e4e75-209">**Kutu** satırı için **Dalga düzeyi türü** alanını *Koli* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-209">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="e4e75-210">Dalga etiketi şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-210">Create a wave label template</span></span>

<span data-ttu-id="e4e75-211">Sonra, dalga etiketi türü için dalga etiketi şablonunu oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e4e75-211">Next, create the wave label template for the wave label type.</span></span>

1. <span data-ttu-id="e4e75-212">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi şablonları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-212">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="e4e75-213">Dalga düzeyi şablonu ekleyin ve üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e4e75-213">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="e4e75-214">**Etiket şablonu adı:** *Koli etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-214">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="e4e75-215">**Açıklama:** *Koli etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-215">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="e4e75-216">**Dalga adımı kodu:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-216">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="e4e75-217">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4e75-217">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4e75-218">**Genel** hızlı sekmesinde, **Dalga etiketi türü** alanını *Koli* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-218">On the **General** FastTab, set the **Wave label type** field to *Carton*.</span></span>
1. <span data-ttu-id="e4e75-219">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip yeni bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-219">On the **Wave label template details** FastTab, add a new row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-220">**Etiket düzeni kodu:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-220">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-221">**Yazıcı adı:** Uygun bir ZPL yazıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-221">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4e75-222">**Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)</span><span class="sxs-lookup"><span data-stu-id="e4e75-222">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4e75-223">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-223">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-224">İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-224">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4e75-225">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-225">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4e75-226">Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-226">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-227">**Tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-227">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-228">**Türetilmiş tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-228">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-229">**Alan:** *Hesap numarası*</span><span class="sxs-lookup"><span data-stu-id="e4e75-229">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4e75-230">**Ölçüt:** İlgili müşteri hesap numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-230">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4e75-231">Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-231">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="e4e75-232">Eylem Bölmesinde, tam etiket şablonu için sorgu düzenleyicisi iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-232">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="e4e75-233">Sorgu düzenleyicisi iletişim kutusunda **Tasnif** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-233">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-234">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-234">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-235">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-235">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-236">**Alan:** *Referans yükleme satırı kodu (Kayıt kodu)*</span><span class="sxs-lookup"><span data-stu-id="e4e75-236">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="e4e75-237">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="e4e75-237">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4e75-238">Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-238">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4e75-239">Bir ileti kutusu, gruplandırma sıfırlama işlemini onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4e75-239">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="e4e75-240">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-240">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e4e75-241">Eylem bölmesinde, **Dalga etiketi şablon grubu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-241">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="e4e75-242">**Dalga etiketi şablon grubu** iletişim kutusunda, **Referans alan adı** alanının *Referans yük satırı kodu*'na ayarlandığı satırı seçin ve sonra bu satır için **Etiket derleme kodu** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-242">In the **Wave label template group** dialog box, select the row where the **Reference field name** field is set to *Reference load line id*, and then select the **Label build ID** check box for this row.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4e75-243">Bu kurulum, iş gruplandırma kurulumu ne olursa olsun, dalga boyunca her yükleme satırı için bir etiket sırası ("Koli 1/X") oluşturacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-243">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="e4e75-244">Bu etiket sırası etiket düzeninde yazdırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-244">This label sequence can be printed on the label layout.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="e4e75-245">Numara serisi uzantıları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e4e75-245">Configure number sequence extensions</span></span>

<span data-ttu-id="e4e75-246">Numara serisi uzantıları, belirli numara serilerinin GS1 uyumluluğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-246">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="e4e75-247">Bu yapılandırma, geçerli senaryo için isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-247">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="e4e75-248">Daha fazla bilgi ve yapılandırma yönergeleri için bkz. [Numara serisi uzantılarını yapılandırma](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-248">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="e4e75-249">Satış siparişi oluşturma ve ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="e4e75-249">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="e4e75-250">**Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-250">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="e4e75-251">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-251">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-252">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e4e75-252">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e4e75-253">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4e75-253">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4e75-254">Aşağıdaki ayarlara sahip iki satış siparişi satırı ekleyin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-254">Add two sales order lines that have the following settings:</span></span>

    - <span data-ttu-id="e4e75-255">Satış sipariş satırı 1:</span><span class="sxs-lookup"><span data-stu-id="e4e75-255">Sales order line 1:</span></span>

        - <span data-ttu-id="e4e75-256">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e4e75-256">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e4e75-257">**Miktar:** *9024*</span><span class="sxs-lookup"><span data-stu-id="e4e75-257">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="e4e75-258">**Birim:** *ea* (9024 ea = 376 Kutu = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="e4e75-258">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="e4e75-259">Satış sipariş satırı 2:</span><span class="sxs-lookup"><span data-stu-id="e4e75-259">Sales order line 2:</span></span>

        - <span data-ttu-id="e4e75-260">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4e75-260">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e4e75-261">**Miktar:** *9016*</span><span class="sxs-lookup"><span data-stu-id="e4e75-261">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="e4e75-262">**Birim:** *ea* (9016 ea = 322 Kutu = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="e4e75-262">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4e75-263">Burada sunulan maddeler ve miktarlar yalnızca örnektir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-263">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="e4e75-264">Bunlar için daha önce tanımladığınız birim sırası grubunu kullanmaları, bunlar için *ea*'dan *kutu*'ya *PL*'ye uygun birim dönüşümlerinin tanımlanması ambar *62*'de stokta bulunmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-264">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="e4e75-265">Daha fazla bilgi için, bkz. [Ölçü birimi ve stoklama ilkeleri](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-265">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="e4e75-266">Satış siparişi satırı 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-266">Select sales order line 1.</span></span> <span data-ttu-id="e4e75-267">Ardından, **Satış siparişi satırı** bölümünde **Stok** menüsünde **Rezervasyonlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-267">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="e4e75-268">**Rezervasyon** sayfasında, Eylem Bölmesi'nde **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-268">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="e4e75-269">Satış siparişi satırı 2 için 4 ve 5 numaralı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-269">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="e4e75-270">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-270">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e4e75-271">Aşağıdaki olaylar gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="e4e75-271">The following events occur:</span></span>

    - <span data-ttu-id="e4e75-272">Sistem, oluşturulan sevkiyatı etiket yazdırma adımını içeren şablonu kullanarak işler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-272">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="e4e75-273">Etiket düzeni, etiketin biçimini tanımlamak için kullanılır ve sonuç etiket şablonunda seçilen yazıcıda yazdırılan bir etiket olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-273">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="e4e75-274">Dalga etiketleri oluşturulur ve yazdırılır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-274">Wave labels are generated and printed.</span></span> <span data-ttu-id="e4e75-275">Etiket sayısı koli sayısına eşit olacaktır (bu örnekte, satır 1 için 376 Kutu etiketi ve satır 2 için 322 kutu etiketi).</span><span class="sxs-lookup"><span data-stu-id="e4e75-275">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1 and 322 Box labels for line 2).</span></span>
    - <span data-ttu-id="e4e75-276">Sevk irsaliyeleri için yeni bir konşimento kodu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-276">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="e4e75-277">Numara serisi uzantılarını yapılandırdıysanız, dalga etiketi kodları **SSCC-18** numara biçimini izler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-277">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="e4e75-278">Dalga etiketlerini aşağıdaki sayfalardan görüntüleyebilir ve yeniden yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-278">You can view and reprint wave labels from the following pages.</span></span> <span data-ttu-id="e4e75-279">Her sayfanın Eylem Bölmesinde **Sevkiyatlar** sekmesindeki **İlgili bilgiler** grubunda **Dalga etiketleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-279">On the Action Pane of each page, on the **Shipments** tab, in the **Related information** group, select **Wave labels**.</span></span>

- <span data-ttu-id="e4e75-280">Tüm sevkiyatlar \> Sevkiyat ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="e4e75-280">All shipments \> Shipment details</span></span>
- <span data-ttu-id="e4e75-281">Tüm yükler \> Yük ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="e4e75-281">All loads \> Load details</span></span>
- <span data-ttu-id="e4e75-282">Tüm dalgalar</span><span class="sxs-lookup"><span data-stu-id="e4e75-282">All waves</span></span>
- <span data-ttu-id="e4e75-283">Dalga etiketleri</span><span class="sxs-lookup"><span data-stu-id="e4e75-283">Wave labels</span></span>
- <span data-ttu-id="e4e75-284">Dalga etiketi geçmişi</span><span class="sxs-lookup"><span data-stu-id="e4e75-284">Wave label history</span></span>

## <a name="scenario-2-wave-label-printing-for-containerization-without-wave-label-records"></a><span data-ttu-id="e4e75-285">Senaryo 2: Konteyner kullanımı için dalga etiketi yazdırma (dalga etiketi kayıtları olmadan)</span><span class="sxs-lookup"><span data-stu-id="e4e75-285">Scenario 2: Wave label printing for containerization (without wave label records)</span></span>

<span data-ttu-id="e4e75-286">Bu senaryo, maddeleri otomatik olarak kolilere bölmek için konteyner kullanımı etiketleri kullanırken dalga etiketlerini yazdırmanıza olanak tanır ve bu nedenle bir dalga etiketi kaydı gerektirmez.</span><span class="sxs-lookup"><span data-stu-id="e4e75-286">This scenario lets you print wave labels when you use containerization to automatically split items into cartons and therefore don't require a wave label record.</span></span> <span data-ttu-id="e4e75-287">Bu durumda, konteyner kodu SSCC için bir yer tutucu olarak işlem gerçekleştirir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-287">In this case, the container ID acts as a placeholder for the SSCC.</span></span>

<span data-ttu-id="e4e75-288">Bu senaryo ve senaryo 1 arasındaki başlıca farklar aşağıdadır:</span><span class="sxs-lookup"><span data-stu-id="e4e75-288">Here are the main differences between this scenario and scenario 1:</span></span>

- <span data-ttu-id="e4e75-289">**Dalga etiketi şablonları:** Dalga etiketi şablonunda bir dalga etiketi türü seçemezsiniz ve etiket derleme gruplandırması gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-289">**Wave label templates:** You won't select a wave label type on the wave label template, and you won't require a label build grouping.</span></span> <span data-ttu-id="e4e75-290">Aksi durumda, dalga etiketi şablonunu yapılandırırsınız ve senaryo 1'de açıklanan şekilde dalga şablonuna bağlarsınız.</span><span class="sxs-lookup"><span data-stu-id="e4e75-290">Otherwise, you will configure the wave label template and link to the wave template in the same way that is described in scenario 1.</span></span> <span data-ttu-id="e4e75-291">Dalga etiketlerinin oluşturulmasını önlemek için dalga etiketi türünü boş bırakmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-291">You must leave the wave label type blank to prevent wave labels from being generated.</span></span>
- <span data-ttu-id="e4e75-292">**Dalga etiketi düzenleri:** Dalga etiketi kayıtları yerine iş satırları için dalga etiketi düzen satırı ayarlarını yapılandırırsınız.</span><span class="sxs-lookup"><span data-stu-id="e4e75-292">**Wave label layouts:** You will configure the wave label layout row settings for work lines instead of wave label records.</span></span> <span data-ttu-id="e4e75-293">Etiket düzeni için satır ayarını **WHSWaveLabel** tablosu yerine  **WHSWorkLine** tablosunu kullanarak yapılandırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-293">You must configure the row setting for the label layout by using the **WHSWorkLine** table instead of the **WHSWaveLabel** table.</span></span> <span data-ttu-id="e4e75-294">**Sayfa başına satır sayısı** ayarı, gövde bölümünde bulunacak satır sayısını denetler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-294">The **Rows per page** setting controls the number of rows that the body section will have.</span></span> 

<span data-ttu-id="e4e75-295">Bu yapılandırma ayrıca, birden fazla farklı maddenin tek etiketli bir kutu veya bir palette bulunduğu iş senaryolarında kullanılabilir ve bu paketleme süreci iş oluşturma ile (örneğin, sevkiyata göre gruplandırılan iş) tanımlanabilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-295">This configuration is also suitable for business scenarios where multiple different items are packed into one labeled box or into a pallet, and this packing process can be defined by work creation (for example, work that is grouped by shipment).</span></span>

<span data-ttu-id="e4e75-296">Bu senaryo uçtan uca akışı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-296">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e4e75-297">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="e4e75-297">Make demo data available</span></span>

<span data-ttu-id="e4e75-298">Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-298">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="make-sure-that-the-wave-label-method-is-available"></a><span data-ttu-id="e4e75-299">Dalga etiketi yönteminin kullanılabilir olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="e4e75-299">Make sure that the wave label method is available</span></span>

<span data-ttu-id="e4e75-300">Dalga etiketi yazdırma yöntemini kullanılabilir hale getirmek için dalga işlemi yöntemlerini yeniden oluşturmanız gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-300">You might have to regenerate the wave process methods to make the wave label printing method available.</span></span>

1. <span data-ttu-id="e4e75-301">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-301">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="e4e75-302">**waveLabelPrinting** öğesinin listede olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-302">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="e4e75-303">Seçili değilse, eklemek Için eylem bölmesindeki **Yöntemleri yeniden üret**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-303">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="e4e75-304">Dalga şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4e75-304">Set up a wave template</span></span>

<span data-ttu-id="e4e75-305">Dalga şablonları, belirli dalga yöntemi örneklerini ilgili dalga etiketi şablonuna bağlayabilmenizi sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-305">Wave templates let you link specific instances of wave methods to a corresponding wave label template.</span></span>

1. <span data-ttu-id="e4e75-306">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-306">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="e4e75-307">**63 Konteyner Kullanımı** gibi bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-307">Select a template, such as **63 Containerization**.</span></span>
1. <span data-ttu-id="e4e75-308">**Yöntemler** hızlı sekmesinde, **Dalga etiketi yazdırma** yöntemini **Seçili yöntemler** sütununa taşıyın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-308">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
1. <span data-ttu-id="e4e75-309">**Seçili Yöntemler** sütununda, **Dalga etiketi yazdırma** yöntemini seçin ve **Dalga adımı kodu** alanını *PrintLabel* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-309">In the **Selected methods** column, select the **Wave label printing** method, and set its **Wave step code** field to *PrintLabel*.</span></span> <span data-ttu-id="e4e75-310">Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-310">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-a-wave-label-layout"></a><span data-ttu-id="e4e75-311">Dalga etiketi düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-311">Create a wave label layout</span></span>

1. <span data-ttu-id="e4e75-312">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi düzenleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-312">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="e4e75-313">Aşağıdaki ayarlara sahip bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-313">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-314">**Etiket düzeni kodu:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-314">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-315">**Açıklama:** *Koli (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="e4e75-315">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="e4e75-316">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-316">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-317">Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-317">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4e75-318">**Dalga etiketi satır ayarları** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-318">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4e75-319">Burada, etiketin dinamik parçasını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-319">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4e75-320">Aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-320">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-321">**Satır kodu:** *WorkLine*</span><span class="sxs-lookup"><span data-stu-id="e4e75-321">**Row Id:** *WorkLine*</span></span>
    - <span data-ttu-id="e4e75-322">**Satır tablosu adı:** *WHSWaveLine*</span><span class="sxs-lookup"><span data-stu-id="e4e75-322">**Row table name:** *WHSWorkLine*</span></span>
    - <span data-ttu-id="e4e75-323">**Satır başlangıç konumu:** *500*</span><span class="sxs-lookup"><span data-stu-id="e4e75-323">**Row start position:** *500*</span></span>

        <span data-ttu-id="e4e75-324">Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-324">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4e75-325">**Satır yüksekliği:** *-50*</span><span class="sxs-lookup"><span data-stu-id="e4e75-325">**Row height:** *-50*</span></span>

        <span data-ttu-id="e4e75-326">Bu alan her satırın yüksekliğini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-326">This field defines the height of each row.</span></span> <span data-ttu-id="e4e75-327">Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-327">The row height is positive for horizontal labels and negative for vertical labels.</span></span>

    - <span data-ttu-id="e4e75-328">**Sayfa başına satır:** *5*</span><span class="sxs-lookup"><span data-stu-id="e4e75-328">**Rows per page:** *5*</span></span>

        <span data-ttu-id="e4e75-329">Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-329">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4e75-330">Bu ayar her iş için her bir sayfada en fazla beş iş satırı bulunan birkaç ZPL etiketi yazdırır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-330">This setup will print several ZPL labels per work, where each page can hold up to five work lines.</span></span> <span data-ttu-id="e4e75-331">Örneğin, 12 satırı bulunan bir konteyner için etiket yazdırılıyorsa, üç etiket yazdırılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-331">For example, if a label is printed for a container that has 12 lines, three labels will be printed.</span></span> <span data-ttu-id="e4e75-332">Her bir çekme satırı için ayrı bir etiket yazdırmak istiyorsanız, bu değeri *1* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-332">If you want to print a separate label for each pick line, set this value to *1*.</span></span>

1. <span data-ttu-id="e4e75-333">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-333">Close the page.</span></span>
1. <span data-ttu-id="e4e75-334">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-334">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4e75-335">Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-335">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-336">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-336">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-337">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-337">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-338">**Alan:** *İş türü*</span><span class="sxs-lookup"><span data-stu-id="e4e75-338">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4e75-339">**Ölçüt:** *Malzeme çekme*</span><span class="sxs-lookup"><span data-stu-id="e4e75-339">**Criteria:** *Pick*</span></span>

1. <span data-ttu-id="e4e75-340">Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-340">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="e4e75-341">Sorgu düzenleyicisi iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-341">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4e75-342">**Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**.</span><span class="sxs-lookup"><span data-stu-id="e4e75-342">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4e75-343">**Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-343">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4e75-344">Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-344">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkTable.ContainerId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="e4e75-345">**Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-345">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4e75-346">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-346">Here is an example.</span></span>

    ```plaintext
    <Row name="WorkLine">
    <Heading>
    //Optional heading for section of rows
    </Heading>
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWorkLine.ItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWorkLine.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="e4e75-347">**Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-347">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4e75-348">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-348">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4e75-349">Bu kurulum her etiketin bir kopyasını yazdırır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-349">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4e75-350">Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-350">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4e75-351">Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-351">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

<span data-ttu-id="e4e75-352">Etiketiniz şimdi kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-352">Your label is now ready to use.</span></span>

### <a name="create-a-wave-label-template"></a><span data-ttu-id="e4e75-353">Dalga etiketi şablonu oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-353">Create a wave label template</span></span>

1. <span data-ttu-id="e4e75-354">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi şablonları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-354">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="e4e75-355">Dalga düzeyi şablonu ekleyin ve üst bilgide aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e4e75-355">Add a wave level template, and set the following values in the header:</span></span>

    - <span data-ttu-id="e4e75-356">**Etiket şablonu adı:** *Konteyner etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-356">**Label template name:** *Container labels*</span></span>
    - <span data-ttu-id="e4e75-357">**Açıklama:** *Konteyner etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-357">**Description:** *Container labels*</span></span>
    - <span data-ttu-id="e4e75-358">**Dalga adımı kodu:** *PrintLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-358">**Wave step code:** *PrintLabel*</span></span>
    - <span data-ttu-id="e4e75-359">**Ambar:** *63*</span><span class="sxs-lookup"><span data-stu-id="e4e75-359">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="e4e75-360">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-360">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-361">**Etiket düzeni kodu:** *Konteyner*</span><span class="sxs-lookup"><span data-stu-id="e4e75-361">**Label layout ID:** *Container*</span></span>
    - <span data-ttu-id="e4e75-362">**Yazıcı adı:** Uygun bir ZPL yazıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-362">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4e75-363">**Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)</span><span class="sxs-lookup"><span data-stu-id="e4e75-363">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4e75-364">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-364">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-365">İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-365">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4e75-366">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-366">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4e75-367">Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-367">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-368">**Tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-368">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-369">**Türetilmiş tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-369">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-370">**Alan:** *Hesap numarası*</span><span class="sxs-lookup"><span data-stu-id="e4e75-370">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4e75-371">**Ölçüt:** İlgili müşteri hesap numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-371">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4e75-372">Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-372">When you've finished, select **OK** to close the query editor dialog box.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="e4e75-373">Numara serisi uzantıları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e4e75-373">Configure number sequence extensions</span></span>

<span data-ttu-id="e4e75-374">Numara serisi uzantıları, belirli numara serilerinin GS1 uyumluluğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-374">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="e4e75-375">Bu yapılandırma, geçerli senaryo için isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-375">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="e4e75-376">Daha fazla bilgi ve yapılandırma yönergeleri için bkz. [Numara serisi uzantılarını yapılandırma](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-376">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="e4e75-377">Satış siparişi oluşturma ve ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="e4e75-377">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="e4e75-378">**Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-378">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="e4e75-379">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-379">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-380">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e4e75-380">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e4e75-381">**Ambar:** *63*</span><span class="sxs-lookup"><span data-stu-id="e4e75-381">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="e4e75-382">Beş satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-382">Add five sales order lines:</span></span>

    - <span data-ttu-id="e4e75-383">Satış sipariş satırı 1:</span><span class="sxs-lookup"><span data-stu-id="e4e75-383">Sales order line 1:</span></span>

        - <span data-ttu-id="e4e75-384">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e4e75-384">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e4e75-385">**Miktar:** *10*</span><span class="sxs-lookup"><span data-stu-id="e4e75-385">**Quantity:** *10*</span></span>

    - <span data-ttu-id="e4e75-386">Satış sipariş satırı 2:</span><span class="sxs-lookup"><span data-stu-id="e4e75-386">Sales order line 2:</span></span>

        - <span data-ttu-id="e4e75-387">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4e75-387">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e4e75-388">**Miktar:** *20*</span><span class="sxs-lookup"><span data-stu-id="e4e75-388">**Quantity:** *20*</span></span>

    - <span data-ttu-id="e4e75-389">Satış sipariş satırı 3:</span><span class="sxs-lookup"><span data-stu-id="e4e75-389">Sales order line 3:</span></span>

        - <span data-ttu-id="e4e75-390">**Madde numarası:** *L0006*</span><span class="sxs-lookup"><span data-stu-id="e4e75-390">**Item number:** *L0006*</span></span>
        - <span data-ttu-id="e4e75-391">**Miktar:** *20*</span><span class="sxs-lookup"><span data-stu-id="e4e75-391">**Quantity:** *20*</span></span>

    - <span data-ttu-id="e4e75-392">Satış sipariş satırı 4:</span><span class="sxs-lookup"><span data-stu-id="e4e75-392">Sales order line 4:</span></span>

        - <span data-ttu-id="e4e75-393">**Madde numarası:** *L0100*</span><span class="sxs-lookup"><span data-stu-id="e4e75-393">**Item number:** *L0100*</span></span>
        - <span data-ttu-id="e4e75-394">**Miktar:** *40*</span><span class="sxs-lookup"><span data-stu-id="e4e75-394">**Quantity:** *40*</span></span>

    - <span data-ttu-id="e4e75-395">Satış sipariş satırı 5:</span><span class="sxs-lookup"><span data-stu-id="e4e75-395">Sales order line 5:</span></span>

        - <span data-ttu-id="e4e75-396">**Madde numarası:** *L0101*</span><span class="sxs-lookup"><span data-stu-id="e4e75-396">**Item number:** *L0101*</span></span>
        - <span data-ttu-id="e4e75-397">**Miktar:** *50*</span><span class="sxs-lookup"><span data-stu-id="e4e75-397">**Quantity:** *50*</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4e75-398">Burada sunulan maddeler ve miktarlar yalnızca örnektir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-398">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="e4e75-399">Bunlar belirtilen ambarda stokta bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-399">They must have stock in the specified warehouse.</span></span>

1. <span data-ttu-id="e4e75-400">Satış siparişi satırı 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-400">Select sales order line 1.</span></span> <span data-ttu-id="e4e75-401">Ardından, **Satış siparişi satırı** bölümünde **Stok** menüsünde **Rezervasyonlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-401">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="e4e75-402">**Rezervasyon** sayfasında, Eylem Bölmesi'nde **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-402">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="e4e75-403">Eklenen her satış siparişi satırı için 4 ve 5 numaralı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-403">Repeat steps 4 and 5 for each additional sales order line.</span></span>
1. <span data-ttu-id="e4e75-404">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-404">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e4e75-405">Aşağıdaki olaylar gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="e4e75-405">The following events occur:</span></span>

    - <span data-ttu-id="e4e75-406">Sistem, oluşturulan sevkiyatı etiket yazdırma adımını içeren şablonu kullanarak işler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-406">The system processes the created shipment using the template that includes the label printing step.</span></span> <span data-ttu-id="e4e75-407">Etiket düzeni, etiketin biçimini tanımlamak için kullanılır ve sonuç etiket şablonunda seçilen yazıcıda yazdırılan ve beş satırı bulunan bir etiket olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-407">The label layout will be used to define the format of the label, and the end result will be a label that has five lines and that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="e4e75-408">Sevk irsaliyeleri için yeni bir konşimento kodu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-408">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="e4e75-409">Numara serisi uzantılarını yapılandırdıysanız, dalga etiketi kodları **SSCC-18** numara biçimini izler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-409">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="e4e75-410">**Ambar Yönetimi \> Sorgular ve raporlar \> Dalga etiketi geçmişi**'ne giderek bu dalga etiketlerini yeniden yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-410">You can reprint these wave labels by going to **Warehouse management \> Inquiries and reports \> Wave label history**.</span></span>

## <a name="scenario-3-wave-label-printing-for-multi-tiered-labels"></a><span data-ttu-id="e4e75-411">Senaryo 3: Çok katmanlı etiketler için dalga etiketi yazdırma</span><span class="sxs-lookup"><span data-stu-id="e4e75-411">Scenario 3: Wave label printing for multi-tiered labels</span></span>

<span data-ttu-id="e4e75-412">Bu senaryo, ambar işlemleri birkaç sevkiyat etiketi katmanı gerektirdiğinde dalga etiketi yazdırma işlevinin nasıl kullanılacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-412">This scenario shows how to use the wave label printing functionality when the warehousing processes require several tiers of shipping labels.</span></span> <span data-ttu-id="e4e75-413">Örneğin, koliler ve paletler için ayrı etiketler yazdırılması gerekebilir ve tüm sevkiyat için bir kesme etiketi yazdırılması gerekli olabilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-413">For example, separate labels might have to be printed for cartons and pallets, and a break label might have to be printed for a whole shipment.</span></span> <span data-ttu-id="e4e75-414">Kesme etiketleri, sevkiyat kodu ve barkod için olan etiketler gibi, rulolar ve konteynerler arasında bir ayırıcı gibi kullanılabilen ayrı bir etiket türüdür; böylece etiketler yazdırıldıktan sonra kolaylıkla tasnif edilebilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-414">Break labels are a separate type of label that can be used as a divider between rolls and containers, such as labels for the shipment ID and a barcode, so that the labels can easily be sorted after they are printed.</span></span>

<span data-ttu-id="e4e75-415">Bu senaryonun yapılandırması ile senaryo 1'in yapılandırılması arasındaki temel fark, kesme etiketlerinin etkinleştirilmesi dışında, çok sayıda dalga etiketi türünün dalga etiketi şablonları ve birim sırası grup satırlarıyla ilişkilendirilmesinin gerekli olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-415">The main difference between the configuration of this scenario and the configuration of scenario 1, besides the fact that break labels are enabled, is that multiple wave label types must be associated with wave label templates and unit sequence group lines.</span></span> <span data-ttu-id="e4e75-416">Bu yapılandırmayı tamamlamak için, bu senaryo için aşağıdaki öğeleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e4e75-416">To accomplish this configuration, you set up the following elements for this scenario:</span></span>

- <span data-ttu-id="e4e75-417">**Dalga işleme yöntemleri:** Dalga etiketi yöntemini "yinelenebilir" olarak işaretler, dalga şablonuna iki (veya daha fazla) defa ekler ve farklı dalga adımı kodları ayarlarsınız.</span><span class="sxs-lookup"><span data-stu-id="e4e75-417">**Wave processing methods:** You will mark the wave label method as "repeatable," add it two (or more) times to the wave template, and set different wave step codes.</span></span>
- <span data-ttu-id="e4e75-418">**Dalga etiketi şablonları:** Dalga etiketi şablonlarını yapılandırır ve onları dalga şablonuna bağlarsınız.</span><span class="sxs-lookup"><span data-stu-id="e4e75-418">**Wave label templates:** You will configure the wave label templates and link them to the wave template.</span></span> <span data-ttu-id="e4e75-419">Her dalga etiketi şablonunun kendi dalga etiketi türü vardır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-419">Each wave label template has its own wave label type.</span></span>
- <span data-ttu-id="e4e75-420">**Dalga etiketi düzenleri:** Birden çok dalga etiketi düzeni oluşturursunuz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-420">**Wave label layouts:** You will create multiple wave label layouts.</span></span> <span data-ttu-id="e4e75-421">Etiketlerin her "katmanı" için ayrı bir etiket düzeni olur ve aynı zamanda bir kesme etiketi düzeni bulunur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-421">There will be a separate label layout for each "tier" of labels, and there will also be a break label layout.</span></span>

<span data-ttu-id="e4e75-422">Bu senaryo uçtan uca akışı gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-422">This scenario shows the end-to-end flow.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="e4e75-423">Tanıtım verilerini kullanılabilir hale getirme</span><span class="sxs-lookup"><span data-stu-id="e4e75-423">Make demo data available</span></span>

<span data-ttu-id="e4e75-424">Bu senaryoyu izlemek için, demo verilerinin yüklenmiş olması ve **USMF** tüzel kişiliğini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-424">To follow this scenario, you must have demo data installed, and you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-wave-process-method"></a><span data-ttu-id="e4e75-425">Dalga işlemi yöntemi ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4e75-425">Set up a wave process method</span></span>

1. <span data-ttu-id="e4e75-426">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga işleme yöntemleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-426">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="e4e75-427">**waveLabelPrinting** öğesinin listede olduğunu onaylayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-427">Confirm that **waveLabelPrinting** is in the list.</span></span> <span data-ttu-id="e4e75-428">Seçili değilse, eklemek Için eylem bölmesindeki **Yöntemleri yeniden üret**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-428">If it isn't, select **Regenerate methods** on the Action Pane to add it.</span></span>
1. <span data-ttu-id="e4e75-429">**waveLabelPrinting** yöntemi için **Yöntemi yinelenebilir yap** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-429">For the **waveLabelPrinting** method, select the **Make method repeatable** check box.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="e4e75-430">Dalga şablonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="e4e75-430">Set up a wave template</span></span>

1. <span data-ttu-id="e4e75-431">**Ambar yönetimi \> Kurulum \> Dalgalar \> Dalga şablonları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-431">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
2. <span data-ttu-id="e4e75-432">**62 Sevkiyat Varsayılanı** gibi bir şablon seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-432">Select a template, such as **62 Shipping Default**.</span></span>
3. <span data-ttu-id="e4e75-433">**Yöntemler** hızlı sekmesinde, **Dalga etiketi yazdırma** yöntemini **Seçili yöntemler** sütununa taşıyın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-433">On the **Methods** FastTab, move the **Wave label printing** method to the **Selected methods** column.</span></span>
4. <span data-ttu-id="e4e75-434">**Seçili yöntemler** sütununda, **Dalga etiketi yazdırma** yöntemine *Koli* gibi bir **Dalga adımı kodu** değeri atayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-434">In the **Selected methods** column, assign a **Wave step code** value, such as *Carton*, to the **Wave label printing** method.</span></span> <span data-ttu-id="e4e75-435">Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-435">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>
5. <span data-ttu-id="e4e75-436">**Dalga etiketi yazdırma** yöntemini ikinci kez **Seçili yöntemler** sütununa taşıyın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-436">Move the **Wave label printing** method to the **Selected methods** column a second time.</span></span>
6. <span data-ttu-id="e4e75-437">**Seçili yöntemler** sütununda, ikinci **Dalga etiketi yazdırma** yöntemine *Palet* gibi farklı bir **Dalga adımı kodu** değeri atayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-437">In the **Selected methods** column, assign a different **Wave step code** value, such as *Pallet*, to the second **Wave label printing** method.</span></span> <span data-ttu-id="e4e75-438">Dalga adım kodları hakkında daha fazla bilgi için bkz. [Dalga adımı kodları](wave-step-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-438">For more information about wave step codes, see [Wave step codes](wave-step-codes.md).</span></span>

### <a name="create-three-wave-label-layouts"></a><span data-ttu-id="e4e75-439">Üç dalga etiketi düzeni oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-439">Create three wave label layouts</span></span>

1. <span data-ttu-id="e4e75-440">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi düzenleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-440">Go to **Warehouse management \> Setup \> Document routing \> Wave label layouts**.</span></span>
1. <span data-ttu-id="e4e75-441">Aşağıdaki ayarlara sahip bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-441">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-442">**Etiket düzeni kodu:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-442">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-443">**Açıklama:** *Koli (SSCC)*</span><span class="sxs-lookup"><span data-stu-id="e4e75-443">**Description:** *Carton (SSCC)*</span></span>

1. <span data-ttu-id="e4e75-444">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-444">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-445">Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-445">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4e75-446">**Dalga etiketi satır ayarları** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-446">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4e75-447">Burada, etiketin dinamik parçasını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-447">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4e75-448">Aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-448">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-449">**Satır kodu:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-449">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="e4e75-450">**Satır tablosu adı:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-450">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="e4e75-451">**Satır başlangıç konumu:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4e75-451">**Row start position:** *0*</span></span>

        <span data-ttu-id="e4e75-452">Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-452">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4e75-453">**Satır yüksekliği:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4e75-453">**Row height:** *0*</span></span>

        <span data-ttu-id="e4e75-454">Bu alan, ZPL standardına göre her satırın yüksekliğini (punto olarak) tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-454">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="e4e75-455">Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-455">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="e4e75-456">Bu örnekte tek bir satır olduğu için, değeri *0* (sıfır) olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-456">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="e4e75-457">**Sayfa başına satır:** *1*</span><span class="sxs-lookup"><span data-stu-id="e4e75-457">**Rows per page:** *1*</span></span>

        <span data-ttu-id="e4e75-458">Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-458">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4e75-459">Bu kurulum, dalga etiketleri tablosundaki her kayıt için ayrı bir ZPL etiketinin yazdırılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-459">This setup will cause a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="e4e75-460">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-460">Close the page.</span></span>
1. <span data-ttu-id="e4e75-461">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-461">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4e75-462">Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-462">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-463">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-463">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-464">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-464">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-465">**Alan:** *İş türü*</span><span class="sxs-lookup"><span data-stu-id="e4e75-465">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4e75-466">**Ölçüt:** *Malzeme çekme*</span><span class="sxs-lookup"><span data-stu-id="e4e75-466">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="e4e75-467">Bu sorgu yalnızca çekme türü iş satırlarının etiket üzerine yazdırılmasını (yerine koyma türü iş satırları değil) sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-467">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="e4e75-468">Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-468">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span> 
1. <span data-ttu-id="e4e75-469">Sorgu düzenleyicisi iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-469">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4e75-470">**Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**.</span><span class="sxs-lookup"><span data-stu-id="e4e75-470">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4e75-471">**Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-471">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4e75-472">Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-472">For example, if you're using Zebra printers, you can use the following code.</span></span>


    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA~TA000~JSN^LT0^MNW^MTT^PON^PMN^LH0,0^JMA^PR8,8~SD15^JUS^LRN^CI0^XZ
    ^XA
    ^MMT
    ^PW812
    ^LL1218
    ^LS0
    ^FT85,505^A0N,28,28^FH\^FD$WHSShipmentTable.CustomerReq$^FS
    ^FO1,173^GB809,0,1^FS
    ^FO0,391^GB809,0,1^FS
    ^FO3,599^GB809,0,2^FS
    ^FO420,176^GB0,216,1^FS
    ^FO313,3^GB0,169,1^FS
    ^FO0,807^GB809,0,1^FS
    ^FT529,370^A0N,28,26^FH\^FD$WHSShipmentTable.BillOfLadingId$^FS
    ^BY2,3,132^FT25,344^BCN,,N,N
    ^FD>:(420)>38102>63^FS
    ^FT526,315^A0N,28,28^FH\^FD ^FS
    ^FT437,248^A0N,28,28^FH\^FDCARR: $WHSShipmentTable.SCAC$^FS
    ^FT425,201^A0N,23,24^FH\^FDCARRIER:^FS
    ^FT17,68^A0N,20,19^FH\^FDIntershipping, Inc.^FS
    ^FT15,99^A0N,20,19^FH\^FD1000 Shipping Lane^FS
    ^FT16,158^A0N,20,19^FH\^FD ^FS
    ^FT438,368^A0N,28,28^FH\^FDB/L#^FS
    ^FT15,128^A0N,20,19^FH\^FDShelbyville TN 38102^FS
    ^FT19,203^A0N,23,24^FH\^FD(420) SHIP TO POSTAL CODE^FS
    ^FT331,39^A0N,28,28^FH\^FDShip To:^FS
    ^FT14,39^A0N,28,28^FH\^FDShip From:^FS
    ^FT331,67^A0N,23,24^FH\^FDWAL-MART DC 1111A-ABC DIS^FS
    ^FT330,98^A0N,23,24^FH\^FDDEPT 10^FS
    ^FT329,166^A0N,23,24^FH\^FDSpringfield TN 39021^FS
    ^FT330,134^A0N,23,24^FH\^FD100 Main Street^FS
    ^FT19,504^A0N,28,28^FH\^FDPO#:^FS
    ^FT437,316^A0N,28,28^FH\^FDPRO#^FS
    ^FT105,371^A0N,28,28^FB130,1,0,C^FH\^FD(420)39021^FS
    ```

1. <span data-ttu-id="e4e75-473">**Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-473">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4e75-474">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-474">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FT127,439^A0N,28,28^FH\^FD$WHSWaveLabel.SeqNum$^FS
    ^FT256,439^A0N,28,28^FH\^FD$WHSWaveLabel.NumberOfLabels$^FS
    ^FT17,439^A0N,28,28^FH\^FDCARTON^FS
    ^FT522,422^A0N,23,24^FH\^FDVPN:^FS
    ^FT74,1156^A0N,28,28^FH\^FDSSCC-18^FS
    ^FT21,579^A0N,28,28^FH\^FDItem name:^FS
    ^FT107,580^A0N,28,28^FH\^FD$WHSWaveLabel.LabelItemName$^FS
    ^FT576,423^A0N,23,21^FH\^FD$WHSWaveLabel.LabelItemId$^FS
    ^FT252,1155^A0N,32,31^FH\^FD(00)$WHSWaveLabel.WaveLabelId$^FS
    ^BY4,3,283^FT66,1115^BCN,,N,N
    ^FD>;>800$WHSWaveLabel.WaveLabelId$^FS
    ^FT194,439^A0N,28,28^FH\^FDof^FS
    </Row>
    ```

1. <span data-ttu-id="e4e75-475">**Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-475">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4e75-476">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-476">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4e75-477">Bu kurulum her etiketin bir kopyasını yazdırır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-477">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4e75-478">Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-478">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4e75-479">Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-479">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="e4e75-480">İlk etiketiniz şimdi kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-480">The first label is now ready to use.</span></span>
1. <span data-ttu-id="e4e75-481">Aşağıdaki ayarlara sahip ikinci bir düzen kaydı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-481">Create a second layout record that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-482">**Etiket düzeni kodu:** *Palet*</span><span class="sxs-lookup"><span data-stu-id="e4e75-482">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="e4e75-483">**Açıklama:** *Palet*</span><span class="sxs-lookup"><span data-stu-id="e4e75-483">**Description:** *Pallet*</span></span>

1. <span data-ttu-id="e4e75-484">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-484">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-485">Eylem bölmesinde, **Dalga etiketi satır ayarları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-485">On the Action Pane, select **Wave label row settings**.</span></span>

    <span data-ttu-id="e4e75-486">**Dalga etiketi satır ayarları** sayfası görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-486">The **Wave label row settings** page appears.</span></span> <span data-ttu-id="e4e75-487">Burada, etiketin dinamik parçasını yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-487">Here, you can configure the dynamic part of the label.</span></span>

1. <span data-ttu-id="e4e75-488">Aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-488">Add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-489">**Satır kodu:** *WaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-489">**Row Id:** *WaveLabel*</span></span>
    - <span data-ttu-id="e4e75-490">**Satır tablosu adı:** *WHSWaveLabel*</span><span class="sxs-lookup"><span data-stu-id="e4e75-490">**Row table name:** *WHSWaveLabel*</span></span>
    - <span data-ttu-id="e4e75-491">**Satır başlangıç konumu:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4e75-491">**Row start position:** *0*</span></span>

        <span data-ttu-id="e4e75-492">Bu alan, satırın etikette başlayacağı dikey konumu tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-492">This field defines the vertical position where the row will begin on the label.</span></span>

    - <span data-ttu-id="e4e75-493">**Satır yüksekliği:** *0*</span><span class="sxs-lookup"><span data-stu-id="e4e75-493">**Row height:** *0*</span></span>

        <span data-ttu-id="e4e75-494">Bu alan, ZPL standardına göre her satırın yüksekliğini (punto olarak) tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-494">This field defines the height of each row (in points), according to the ZPL standard.</span></span> <span data-ttu-id="e4e75-495">Yatay etiketler için satır yüksekliği pozitif, dikey etiketler için negatif olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-495">The row height is positive for horizontal labels and negative for vertical labels.</span></span> <span data-ttu-id="e4e75-496">Bu örnekte tek bir satır olduğu için, değeri *0* (sıfır) olarak ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-496">Because there is just one row in this example, you can set the value to *0* (zero).</span></span>

    - <span data-ttu-id="e4e75-497">**Sayfa başına satır:** *1*</span><span class="sxs-lookup"><span data-stu-id="e4e75-497">**Rows per page:** *1*</span></span>

        <span data-ttu-id="e4e75-498">Bu alan, her bir etikete yazdırılabilen satır sayısını tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-498">This field defines the number of rows that can be printed on each label.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4e75-499">Bu kurulum, dalga etiketleri tablosundaki her kayıt için ayrı bir ZPL etiketinin yazdırılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-499">This setup causes a separate ZPL label to be printed for each record in the wave labels table.</span></span>

1. <span data-ttu-id="e4e75-500">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-500">Close the page.</span></span>
1. <span data-ttu-id="e4e75-501">Eylem Bölmesi'nde, **Sorgu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-501">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e4e75-502">Sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-502">In the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-503">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-503">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-504">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-504">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-505">**Alan:** *İş türü*</span><span class="sxs-lookup"><span data-stu-id="e4e75-505">**Field:** *Work type*</span></span>
    - <span data-ttu-id="e4e75-506">**Ölçüt:** *Malzeme çekme*</span><span class="sxs-lookup"><span data-stu-id="e4e75-506">**Criteria:** *Pick*</span></span>

    <span data-ttu-id="e4e75-507">Bu sorgu yalnızca çekme türü iş satırlarının etiket üzerine yazdırılmasını (yerine koyma türü iş satırları değil) sağlar.</span><span class="sxs-lookup"><span data-stu-id="e4e75-507">This query ensures that only pick-type work lines will be printed on the label, not put-type work lines.</span></span>

1. <span data-ttu-id="e4e75-508">Konşimento kodunu yazdırabilmek istiyorsanız, **Birleşimler** sekmesinde **İş satırları** tablosunu seçin ve **Sevkiyatlar** tablosunu bu tabloya birleştirin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-508">If you want to be able to print the bill of lading ID, on the **Joins** tab, select the **Work lines** table, and join the **Shipments** table to it.</span></span>
1. <span data-ttu-id="e4e75-509">Sorgu düzenleyicisi iletişim kutusunu kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-509">Close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4e75-510">**Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**.</span><span class="sxs-lookup"><span data-stu-id="e4e75-510">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4e75-511">**Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait kodu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-511">In the **Header section** section, in the **Label header** field, enter code for the required header.</span></span> <span data-ttu-id="e4e75-512">Örneğin, Zebra yazıcılar kullanıyorsanız, aşağıdaki kodu kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-512">For example, if you're using Zebra printers, you can use the following code.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWaveLabel.WaveLabelId$ ^FS
    ^FO0,75 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ^FO0,150 ^AT ^FD$WHSShipmentTable.BillOfLadingId$ ^FS
    ```

1. <span data-ttu-id="e4e75-513">**Gövde bölümü** bölümünde, **Etiket gövdesi** alanına gövde için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-513">In the **Body section** section, in the **Label body** field, enter ZPL code for the required body.</span></span> <span data-ttu-id="e4e75-514">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-514">Here is an example.</span></span>

    ```plaintext
    <Row name="WaveLabel">
    ^FO0,450 ^AT ^FDItem ^FS
    ^FO200,450 ^AT ^FDQuantity ^FS
    ^FO0,[[YPos]] ^AT ^FD$WHSWaveLabel.LabelItemId$ ^FS
    ^FO200,[[YPos]] ^AT ^FD$WHSWaveLabel.QtyWork$ ^FS
    </Row>
    ```

1. <span data-ttu-id="e4e75-515">**Gövde bölümü** bölümünde, **Etiket alt bilgisi** alanına alt bilgi için gereken ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-515">In the **Body section** section, in the **Label footer** field, enter ZPL code for the required footer.</span></span> <span data-ttu-id="e4e75-516">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-516">Here is an example.</span></span>

    ```plaintext
    ^PQ1^XZ
    ```

    > [!NOTE]
    > <span data-ttu-id="e4e75-517">Bu kurulum her etiketin bir kopyasını yazdırır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-517">This setup will print one copy of each label.</span></span> <span data-ttu-id="e4e75-518">Daha fazla kopyaya gereksinim duyarsanız (örneğin, paletin her iki tarafı için bir kopya), alt bilgideki **\^PQn** bölümü için **n** değerini gerekli kopya sayısı olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-518">If you require more copies (for example, one copy for each side of the pallet), set the **n** value for the **\^PQn** section in the footer to the required number of copies.</span></span> <span data-ttu-id="e4e75-519">Örneğin, her etiketin dört kopyasını yazdırmak için **\^PQ4** girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-519">For example, to print four copies of each label, specify **\^PQ4**.</span></span>

1. <span data-ttu-id="e4e75-520">İkinci etiketiniz şimdi kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-520">The second label is now ready to use.</span></span>
1. <span data-ttu-id="e4e75-521">Aşağıdaki ayarlara sahip üçüncü bir düzen kaydı oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-521">Create a third layout record that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-522">**Etiket düzeni kodu:** *Kesme*</span><span class="sxs-lookup"><span data-stu-id="e4e75-522">**Label layout ID:** *Break*</span></span>
    - <span data-ttu-id="e4e75-523">**Açıklama:** *Kesme etiketi*</span><span class="sxs-lookup"><span data-stu-id="e4e75-523">**Description:** *Break label*</span></span>

1. <span data-ttu-id="e4e75-524">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-524">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-525">**Yazıcı metin düzeni** hızlı sekmesinde, yazıcı kodunu yazabileceğiniz üç bölüm vardır: **Üstbilgi bölümü**, **Gövde bölümü** ve **Altbilgi bölümü**.</span><span class="sxs-lookup"><span data-stu-id="e4e75-525">The **Printer text Layout** FastTab has three sections where you can write printer code: **Header section**, **Body section**, and **Footer section**.</span></span> <span data-ttu-id="e4e75-526">**Üstbilgi bölümü** bölümünde, **Etiket başlığı** alanına gereken başlığa ait ZPL kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-526">In the **Header section** section, in the **Label header** field, enter ZPL code for the required header.</span></span> <span data-ttu-id="e4e75-527">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-527">Here is an example.</span></span>

    ```plaintext
    CT~~CD,~CC^~CT~
    ^XA
    ^LH10,10
    ^FO0,0 ^AT ^FD$WHSWorkLine.ShipmentId$ ^FS
    ```

1. <span data-ttu-id="e4e75-528">Bu kez, gövde gerekli değildir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-528">This time, no body is required.</span></span> <span data-ttu-id="e4e75-529">Bu nedenle, gerekli metni **Alt bilgi bölümü** bölümüne girmeniz yeterlidir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-529">Therefore, just enter the required text in the **Footer section** section.</span></span> <span data-ttu-id="e4e75-530">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-530">Here is an example.</span></span>

    ```plaintext
    ^XZ
    ```

    <span data-ttu-id="e4e75-531">Üçüncü etiketiniz şimdi kullanıma hazır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-531">The third label is now ready to use.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4e75-532">Bu üçüncü etiket, etiket ruloları arasında ayırıcı olarak kullanılacak bir kesme etiketidir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-532">This third label is a break label that will be used as a divider between label rolls.</span></span>

### <a name="create-two-wave-label-types"></a><span data-ttu-id="e4e75-533">İki dalga etiketi türü oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-533">Create two wave label types</span></span>

1. <span data-ttu-id="e4e75-534">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi türleri** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-534">Go to **Warehouse management \> Setup \> Document routing \> Wave label types**.</span></span>
1. <span data-ttu-id="e4e75-535">Aşağıdaki ayarlara sahip bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-535">Create a record that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-536">**Etiket türü:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-536">**Label type:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-537">**Açıklama:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-537">**Description:** *Carton*</span></span>

1. <span data-ttu-id="e4e75-538">Aşağıdaki ayarlara sahip ikinci bir kayıt oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-538">Create a second record that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-539">**Etiket türü:** *Palet*</span><span class="sxs-lookup"><span data-stu-id="e4e75-539">**Label type:** *Pallet*</span></span>
    - <span data-ttu-id="e4e75-540">**Açıklama:** *Palet*</span><span class="sxs-lookup"><span data-stu-id="e4e75-540">**Description:** *Pallet*</span></span>

### <a name="set-up-unit-sequence-groups"></a><span data-ttu-id="e4e75-541">Birim sıra gruplarını ayarla</span><span class="sxs-lookup"><span data-stu-id="e4e75-541">Set up unit sequence groups</span></span>

1. <span data-ttu-id="e4e75-542">**Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri\> Birim sırası grubu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-542">Go to **Warehouse management \> Setup \> Warehouse \> Unit sequence groups**.</span></span>
1. <span data-ttu-id="e4e75-543">**Ea Kutu PL** grubu seçin veya oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e4e75-543">Select or create an **Ea Box PL** group.</span></span>
1. <span data-ttu-id="e4e75-544">**Kutu** satırı için **Dalga düzeyi türü** alanını *Koli* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-544">For the **Box** line, set the **Wave level type** field to *Carton*.</span></span>
1. <span data-ttu-id="e4e75-545">**PL** satırı için **Dalga düzeyi türü** alanını *Palet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-545">For the **PL** line, set the **Wave level type** field to *Pallet*.</span></span>

### <a name="create-wave-label-templates"></a><span data-ttu-id="e4e75-546">Dalga etiketi şablonları oluşturma</span><span class="sxs-lookup"><span data-stu-id="e4e75-546">Create wave label templates</span></span>

1. <span data-ttu-id="e4e75-547">**Ambar yönetimi \> Kurulum \> Belge yönlendirme \> Dalga etiketi şablonları** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-547">Go to **Warehouse management \> Setup \> Document routing \> Wave label templates**.</span></span>
1. <span data-ttu-id="e4e75-548">Aşağıdaki ayarlara sahip bir etiket şablonu oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-548">Create a label template that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-549">**Etiket şablonu adı:** *Koli etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-549">**Label template name:** *Carton labels*</span></span>
    - <span data-ttu-id="e4e75-550">**Açıklama:** *Koli etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-550">**Description:** *Carton labels*</span></span>
    - <span data-ttu-id="e4e75-551">**Dalga adımı kodu:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-551">**Wave step code:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-552">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4e75-552">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4e75-553">**Genel** hızlı sekmesinde **Dalga etiketi türü** alanında *Koli* gibi bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-553">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Carton*.</span></span>
1. <span data-ttu-id="e4e75-554">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-554">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-555">**Etiket düzeni kodu:** *Koli*</span><span class="sxs-lookup"><span data-stu-id="e4e75-555">**Label layout ID:** *Carton*</span></span>
    - <span data-ttu-id="e4e75-556">**Yazıcı adı:** Uygun bir ZPL yazıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-556">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4e75-557">**Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)</span><span class="sxs-lookup"><span data-stu-id="e4e75-557">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4e75-558">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-558">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-559">İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-559">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4e75-560">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-560">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4e75-561">Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-561">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-562">**Tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-562">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-563">**Türetilmiş tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-563">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-564">**Alan:** *Hesap numarası*</span><span class="sxs-lookup"><span data-stu-id="e4e75-564">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4e75-565">**Ölçüt:** İlgili müşteri hesap numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-565">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4e75-566">Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-566">When you've finished, select **OK** to close the query editor dialog box.</span></span>

1. <span data-ttu-id="e4e75-567">Eylem Bölmesinde, tam etiket şablonu için sorgu düzenleyicisi iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-567">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="e4e75-568">Sorgu düzenleyicisi iletişim kutusunda **Tasnif** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-568">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-569">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-569">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-570">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-570">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-571">**Alan:** *Referans yükleme satırı kodu (Kayıt kodu)*</span><span class="sxs-lookup"><span data-stu-id="e4e75-571">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="e4e75-572">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="e4e75-572">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4e75-573">Aşağıdaki ayarlara sahip ikinci bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-573">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-574">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-574">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-575">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-575">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-576">**Alan:** *Sevkiyat kodu*</span><span class="sxs-lookup"><span data-stu-id="e4e75-576">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="e4e75-577">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="e4e75-577">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4e75-578">Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-578">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4e75-579">Bir ileti kutusu, gruplandırma sıfırlama işlemini onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4e75-579">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="e4e75-580">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-580">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e4e75-581">Eylem bölmesinde, **Dalga etiketi şablon grubu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-581">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="e4e75-582">**Dalga etiketi şablon grubu** iletişim kutusunda, **Referans alan adı** alanının *Sevkiyat kodu* olarak ayarlandığı satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e4e75-582">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="e4e75-583">**Kesme etiketi yazdır:** Bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-583">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="e4e75-584">**Etiket düzeni kodu:** Bir kesme etiketi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-584">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="e4e75-585">(Örneğin, bu senaryoda daha önce oluşturduğunuz *Kesme* etiketi düzenini seçin)</span><span class="sxs-lookup"><span data-stu-id="e4e75-585">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="e4e75-586">**Yazıcı adı:** Kesme etiketi için yazıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-586">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="e4e75-587">(Tipik olarak, etiket rulolarını ayırmak amacıyla, **Dalga etiketi şablon ayrıntıları** hızlı sekmesinde seçilenle aynı yazıcıyı seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-587">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="e4e75-588">Ancak, başka senaryolar da olabilir.)</span><span class="sxs-lookup"><span data-stu-id="e4e75-588">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="e4e75-589">**Referans alan adı** alanının *Referans yük satırı kodu* olarak ayarlandığı satır için , **Etiket derleme kodu** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-589">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4e75-590">Bu kurulum, iş gruplandırma kurulumu ne olursa olsun, dalga boyunca her yükleme satırı için bir etiket sırası ("Koli 1/X") oluşturacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-590">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="e4e75-591">Bu etiket sırası etiket düzeninde yazdırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-591">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="e4e75-592">Ek olarak, farklı sevkiyatların etiketleri seçili kesme etiketiyle ayrılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-592">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

1. <span data-ttu-id="e4e75-593">**Dlga etiketi şablon grubu** iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-593">Select **OK** to close the **Wave label template group** dialog box.</span></span>
1. <span data-ttu-id="e4e75-594">Aşağıdaki ayarlara sahip ikinci bir etiket şablonu oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-594">Create a second label template that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-595">**Etiket şablonu adı:** *Palet etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-595">**Label template name:** *Pallet labels*</span></span>
    - <span data-ttu-id="e4e75-596">**Açıklama:** *Palet etiketleri*</span><span class="sxs-lookup"><span data-stu-id="e4e75-596">**Description:** *Pallet labels*</span></span>
    - <span data-ttu-id="e4e75-597">**Dalga adımı kodu:** *Palet*</span><span class="sxs-lookup"><span data-stu-id="e4e75-597">**Wave step code:** *Pallet*</span></span>
    - <span data-ttu-id="e4e75-598">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4e75-598">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4e75-599">**Genel** hızlı sekmesinde **Dalga etiketi türü** alanında *Palet* gibi bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-599">On the **General** FastTab, in the **Wave label type** field, select a value, such as *Pallet*.</span></span>
1. <span data-ttu-id="e4e75-600">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-600">On the **Wave label template details** FastTab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-601">**Etiket düzeni kodu:** *Palet*</span><span class="sxs-lookup"><span data-stu-id="e4e75-601">**Label layout ID:** *Pallet*</span></span>
    - <span data-ttu-id="e4e75-602">**Yazıcı adı:** Uygun bir ZPL yazıcı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-602">**Printer name:** Select an appropriate ZPL printer.</span></span>
    - <span data-ttu-id="e4e75-603">**Sorguyu çalıştır:** *Evet* (Bu ayar isteğe bağlıdır, ancak en iyi performans için önerilir.)</span><span class="sxs-lookup"><span data-stu-id="e4e75-603">**Run query:** *Yes* (This setting is optional, but it's recommended for optimal performance.)</span></span>

1. <span data-ttu-id="e4e75-604">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-604">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4e75-605">İsteğe bağlı: Müşteriye özel etiket tasarımını ayarlıyorsanız, müşterinin hesabını bulmak için bir sorgu oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-605">Optional: If you're setting up a customer-specific label design, you must create a query to find the customer's account.</span></span> <span data-ttu-id="e4e75-606">**Dalga etiketi şablonu ayrıntıları** hızlı sekmesinde, **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-606">On the **Wave label template details** FastTab, select **Edit query**.</span></span> <span data-ttu-id="e4e75-607">Ardından, sorgu düzenleyicisi iletişim kutusunda **Aralık** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-607">Then, in the query editor dialog box, on the **Range** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-608">**Tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-608">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-609">**Türetilmiş tablo:** *Sevkiyatlar*</span><span class="sxs-lookup"><span data-stu-id="e4e75-609">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="e4e75-610">**Alan:** *Hesap numarası*</span><span class="sxs-lookup"><span data-stu-id="e4e75-610">**Field:** *Account number*</span></span>
    - <span data-ttu-id="e4e75-611">**Ölçüt:** İlgili müşteri hesap numarasını girin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-611">**Criteria:** Enter the relevant customer account number.</span></span>

    <span data-ttu-id="e4e75-612">Bitirdiğinizde sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-612">When you've finished, select **OK** to close the query editor dialog box.</span></span> 

1. <span data-ttu-id="e4e75-613">Eylem Bölmesinde, tam etiket şablonu için sorgu düzenleyicisi iletişim kutusunu açmak için **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-613">On the Action Pane, select **Edit query** to open the query editor dialog box for the whole label template.</span></span>
1. <span data-ttu-id="e4e75-614">Sorgu düzenleyicisi iletişim kutusunda **Tasnif** sekmesinde, aşağıdaki ayarlara sahip bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-614">In the query editor dialog box, on the **Sorting** tab, add a row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-615">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-615">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-616">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-616">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-617">**Alan:** *Referans yükleme satırı kodu (Kayıt kodu)*</span><span class="sxs-lookup"><span data-stu-id="e4e75-617">**Field:** *Reference load line id (Record-ID)*</span></span>
    - <span data-ttu-id="e4e75-618">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="e4e75-618">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4e75-619">Aşağıdaki ayarlara sahip ikinci bir satır ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-619">Add a second row that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-620">**Tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-620">**Table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-621">**Türetilen tablo:** *İş satırları*</span><span class="sxs-lookup"><span data-stu-id="e4e75-621">**Derived table:** *Work lines*</span></span>
    - <span data-ttu-id="e4e75-622">**Alan:** *Sevkiyat kodu*</span><span class="sxs-lookup"><span data-stu-id="e4e75-622">**Field:** *Shipment ID*</span></span>
    - <span data-ttu-id="e4e75-623">**Arama yönü:** *Artan*</span><span class="sxs-lookup"><span data-stu-id="e4e75-623">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e4e75-624">Sorgu düzenleyicisi iletişim kutusunu kapatmak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-624">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e4e75-625">Bir ileti kutusu, gruplandırma sıfırlama işlemini onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4e75-625">A message box prompts you to confirm the grouping reset operation.</span></span> <span data-ttu-id="e4e75-626">Devam etmek için **Eve**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-626">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e4e75-627">Eylem bölmesinde, **Dalga etiketi şablon grubu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-627">On the Action Pane, select **Wave label template group**.</span></span>
1. <span data-ttu-id="e4e75-628">**Dalga etiketi şablon grubu** iletişim kutusunda, **Referans alan adı** alanının *Sevkiyat kodu* olarak ayarlandığı satır için aşağıdaki değerleri ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="e4e75-628">In the **Wave label template group** dialog box, for the row where the **Reference field name** field is set to *Shipment ID*, set the following values:</span></span>

    - <span data-ttu-id="e4e75-629">**Kesme etiketi yazdır:** Bu onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-629">**Print break label:** Select this check box.</span></span>
    - <span data-ttu-id="e4e75-630">**Etiket düzeni kodu:** Bir kesme etiketi seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-630">**Label layout ID:** Select a break label.</span></span> <span data-ttu-id="e4e75-631">(Örneğin, bu senaryoda daha önce oluşturduğunuz *Kesme* etiketi düzenini seçin)</span><span class="sxs-lookup"><span data-stu-id="e4e75-631">(For example, select the *Break* label layout that you created earlier in this scenario.)</span></span>
    - <span data-ttu-id="e4e75-632">**Yazıcı adı:** Kesme etiketi için yazıcıyı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-632">**Printer name:** Select the printer for the break label.</span></span> <span data-ttu-id="e4e75-633">(Tipik olarak, etiket rulolarını ayırmak amacıyla, **Dalga etiketi şablon ayrıntıları** hızlı sekmesinde seçilenle aynı yazıcıyı seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-633">(Typically, for the purpose of splitting label rolls, you should select the same printer that is selected on the **Wave label template details** FastTab.</span></span> <span data-ttu-id="e4e75-634">Ancak, başka senaryolar da olabilir.)</span><span class="sxs-lookup"><span data-stu-id="e4e75-634">However, other scenarios are possible.)</span></span>

1. <span data-ttu-id="e4e75-635">**Referans alan adı** alanının *Referans yük satırı kodu* olarak ayarlandığı satır için , **Etiket derleme kodu** onay kutusunu seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-635">For the row where the **Reference field name** field is set to *Reference load line id*, select the **Label build ID** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4e75-636">Bu kurulum, iş gruplandırma kurulumu ne olursa olsun, dalga boyunca her yükleme satırı için bir etiket sırası ("Koli 1/X") oluşturacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-636">This setup will create one label sequence ("Carton 1 of X") per load line throughout the wave, regardless of the work grouping setup.</span></span> <span data-ttu-id="e4e75-637">Bu etiket sırası etiket düzeninde yazdırılabilir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-637">This label sequence can be printed on a label layout.</span></span> <span data-ttu-id="e4e75-638">Ek olarak, farklı sevkiyatların etiketleri seçili kesme etiketiyle ayrılacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-638">Additionally, labels for different shipments will be separated by the selected break label.</span></span>

### <a name="configure-number-sequence-extensions"></a><span data-ttu-id="e4e75-639">Numara serisi uzantıları yapılandırma</span><span class="sxs-lookup"><span data-stu-id="e4e75-639">Configure number sequence extensions</span></span>

<span data-ttu-id="e4e75-640">Numara serisi uzantıları, belirli numara serilerinin GS1 uyumluluğunu denetler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-640">Number sequence extensions control the GS1 compliance of specific number sequences.</span></span> <span data-ttu-id="e4e75-641">Bu yapılandırma, geçerli senaryo için isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-641">This configuration is optional for the current scenario.</span></span> <span data-ttu-id="e4e75-642">Daha fazla bilgi ve yapılandırma yönergeleri için bkz. [Numara serisi uzantılarını yapılandırma](../warehousing/configure-number-sequence-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-642">For more information and configuration instructions, see [Configure number sequence extensions](../warehousing/configure-number-sequence-extensions.md).</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="e4e75-643">Satış siparişi oluşturma ve ambara serbest bırakma</span><span class="sxs-lookup"><span data-stu-id="e4e75-643">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="e4e75-644">**Satış ve pazarlama \> Satış siparişi \> Tüm satış siparişleri**'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-644">Go to **Sales and marketing \> Sales order \> All sales orders**.</span></span>
1. <span data-ttu-id="e4e75-645">Aşağıdaki ayarlara sahip bir satış siparişi oluşturun:</span><span class="sxs-lookup"><span data-stu-id="e4e75-645">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="e4e75-646">**Müşteri hesabı:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e4e75-646">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e4e75-647">**Ambar:** *62*</span><span class="sxs-lookup"><span data-stu-id="e4e75-647">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="e4e75-648">İki satış siparişi satırı ekleyin:</span><span class="sxs-lookup"><span data-stu-id="e4e75-648">Add two sales order lines:</span></span>

    - <span data-ttu-id="e4e75-649">Satış sipariş satırı 1:</span><span class="sxs-lookup"><span data-stu-id="e4e75-649">Sales order line 1:</span></span>

        - <span data-ttu-id="e4e75-650">**Madde numarası:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e4e75-650">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e4e75-651">**Miktar:** *9024*</span><span class="sxs-lookup"><span data-stu-id="e4e75-651">**Quantity:** *9024*</span></span>
        - <span data-ttu-id="e4e75-652">**Birim:** *ea* (9024 ea = 376 Kutu = 47 PL)</span><span class="sxs-lookup"><span data-stu-id="e4e75-652">**Unit:** *ea* (9024 ea = 376 Box = 47 PL)</span></span>

    - <span data-ttu-id="e4e75-653">Satış sipariş satırı 2:</span><span class="sxs-lookup"><span data-stu-id="e4e75-653">Sales order line 2:</span></span>

        - <span data-ttu-id="e4e75-654">**Madde numarası:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4e75-654">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e4e75-655">**Miktar:** *9016*</span><span class="sxs-lookup"><span data-stu-id="e4e75-655">**Quantity:** *9016*</span></span>
        - <span data-ttu-id="e4e75-656">**Birim:** *ea* (9016 ea = 322 Kutu = 46 PL)</span><span class="sxs-lookup"><span data-stu-id="e4e75-656">**Unit:** *ea* (9016 ea = 322 Box = 46 PL)</span></span>

    > [!NOTE]
    > <span data-ttu-id="e4e75-657">Burada sunulan maddeler ve miktarlar yalnızca örnektir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-657">The items and quantities that are provided here are only examples.</span></span> <span data-ttu-id="e4e75-658">Bunlar için daha önce tanımladığınız birim sırası grubunu kullanmaları, bunlar için *ea*'dan *kutu*'ya *PL*'ye uygun birim dönüşümlerinin tanımlanması ambar *62*'de stokta bulunmaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="e4e75-658">They must use the unit sequence group that you defined earlier, appropriate unit conversions from *ea* to *Box* to *PL* must be defined for them, and they must have stock in warehouse *62*.</span></span> <span data-ttu-id="e4e75-659">Daha fazla bilgi için, bkz. [Ölçü birimi ve stoklama ilkeleri](unit-measure-stocking-policies.md).</span><span class="sxs-lookup"><span data-stu-id="e4e75-659">For more information, see [Unit of measure and stocking policies](unit-measure-stocking-policies.md).</span></span>

1. <span data-ttu-id="e4e75-660">Satış siparişi satırı 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-660">Select sales order line 1.</span></span> <span data-ttu-id="e4e75-661">Ardından, **Satış siparişi satırı** bölümünde **Stok** menüsünde **Rezervasyonlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-661">Then, in the **Sales order line** section, on the **Inventory** menu, select **Reservations**.</span></span>
1. <span data-ttu-id="e4e75-662">**Rezervasyon** sayfasında, Eylem Bölmesi'nde **Lotu rezerve et**'i seçin ve ardından sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="e4e75-662">On the **Reservation** page, on the Action Pane, select **Reserve lot**, and then close the page.</span></span>
1. <span data-ttu-id="e4e75-663">Satış siparişi satırı 2 için 4 ve 5 numaralı adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-663">Repeat steps 4 and 5 for sales order line 2.</span></span>
1. <span data-ttu-id="e4e75-664">Eylem bölmesinde, **Ambar** sekmesinde **Ambara serbest bırak**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="e4e75-664">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="e4e75-665">Aşağıdaki olaylar gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="e4e75-665">The following events occur:</span></span> 

    - <span data-ttu-id="e4e75-666">Sistem, oluşturulan sevkiyatı etiket yazdırma adımını içeren şablonu kullanarak işler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-666">The system processes the created shipment by using the template that includes the label printing step.</span></span> <span data-ttu-id="e4e75-667">Etiket düzeni, etiketin biçimini tanımlamak için kullanılır ve sonuç etiket şablonunda seçilen yazıcıda yazdırılan bir etiket olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-667">The label layout will be used to define the format of the label, and the result will be a label that is printed on the printer that is selected in the label template.</span></span>
    - <span data-ttu-id="e4e75-668">Dalga etiketleri oluşturulur ve yazdırılır.</span><span class="sxs-lookup"><span data-stu-id="e4e75-668">Wave labels are generated and printed.</span></span> <span data-ttu-id="e4e75-669">Etiket sayısı koli sayısına eşit olacaktır (bu örnekte, satır 1 için 376 Kutu etiketi, satır 2 için 322 Kutu etiketi, satır 1 için 47 PL etiketi, satır 2 için 47 PL etiketi ve sevkiyat koduna sahip iki kesme etiketi).</span><span class="sxs-lookup"><span data-stu-id="e4e75-669">The number of labels will equal the number of cartons (in this example, 376 Box labels for line 1, 322 Box labels for line 2, 47 PL labels for line 1, 47 PL labels for line 2, and two break labels that have the shipment ID).</span></span>
    - <span data-ttu-id="e4e75-670">Sevk irsaliyeleri için yeni bir konşimento kodu oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="e4e75-670">A new bill of lading ID is generated for the shipments.</span></span> <span data-ttu-id="e4e75-671">Numara serisi uzantılarını yapılandırdıysanız, dalga etiketi kodları **SSCC-18** numara biçimini izler.</span><span class="sxs-lookup"><span data-stu-id="e4e75-671">If you configured the number sequence extensions, the wave label IDs will follow the **SSCC-18** number format.</span></span> 

<span data-ttu-id="e4e75-672">Dalga etiketlerini aşağıdaki sayfalardan görüntüleyebilir ve yeniden yazdırabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="e4e75-672">You can view and reprint wave labels from the following pages:</span></span>

- <span data-ttu-id="e4e75-673">Tüm sevkiyatlar \> Sevkiyat ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="e4e75-673">All shipments \> Shipment details</span></span>
- <span data-ttu-id="e4e75-674">Tüm yükler \> Yük ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="e4e75-674">All loads \> Load details</span></span>
- <span data-ttu-id="e4e75-675">Tüm dalgalar</span><span class="sxs-lookup"><span data-stu-id="e4e75-675">All waves</span></span>
- <span data-ttu-id="e4e75-676">Dalga etiketleri</span><span class="sxs-lookup"><span data-stu-id="e4e75-676">Wave labels</span></span>
- <span data-ttu-id="e4e75-677">Dalga etiketi geçmişi</span><span class="sxs-lookup"><span data-stu-id="e4e75-677">Wave label history</span></span>

<span data-ttu-id="e4e75-678">Bu sayfaların çoğu için, Eylem bölmesindeki **Sevkiyatlar** sekmesinde yer alan **İlgili bilgi** grubunda **Dalga etiketleri**'ni seçerek ilgili işlevi bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e4e75-678">For most of these pages, you can find the relevant function by selecting **Wave labels** in the **Related information** group on the **Shipments** tab of the Action Pane.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4e75-679">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e4e75-679">Additional resources</span></span>

- [<span data-ttu-id="e4e75-680">Dalga etiketlerini yeniden yazdırma ve hükümsüz kılma</span><span class="sxs-lookup"><span data-stu-id="e4e75-680">Reprint and void wave labels</span></span>](reprint-and-void-wave-labels.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]