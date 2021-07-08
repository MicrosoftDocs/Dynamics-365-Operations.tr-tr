---
title: Teslim alınmadığı için sevkiyatı onaylayamazsınız
description: Teslim alınmadığı için sevkiyatı onaylayamazsınız
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301317"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="83346-103">Teslim alınmadığı için sevkiyatı onaylayamazsınız</span><span class="sxs-lookup"><span data-stu-id="83346-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="83346-104">Hata kodu: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="83346-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="83346-105">Belirtiler</span><span class="sxs-lookup"><span data-stu-id="83346-105">Symptoms</span></span>

<span data-ttu-id="83346-106">Bir sevkiyatı onaylamaya çalıştığınızda, sistem aşağıdaki hata iletisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="83346-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="83346-107">%1 yükü için ihtiyaç duyulan maddelerin bazıları henüz çekilmedi ve son sevkiyat konumuna taşındı.</span><span class="sxs-lookup"><span data-stu-id="83346-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="83346-108">Bu nedenle, yükleme için sevkiyat işlemini onaylayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="83346-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="83346-109">Nedeni</span><span class="sxs-lookup"><span data-stu-id="83346-109">Cause</span></span>

<span data-ttu-id="83346-110">Aşağıdaki koşullardan biri mevcut olduğu için yük veya sevkiyat mevcut durumunda onaylanamıyor:</span><span class="sxs-lookup"><span data-stu-id="83346-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="83346-111">İlgili iş henüz teslim alınmadı ve son sevkiyat konumuna taşınmadı.</span><span class="sxs-lookup"><span data-stu-id="83346-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="83346-112">Teslim alınan iş miktarı, yükleme satırında oluşturulan iş miktarıyla eşleşmiyor.</span><span class="sxs-lookup"><span data-stu-id="83346-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="83346-113">Yerleşim yönergesi, paketleme yerleşimi son sevkiyat yerleşimi olarak ve Dalga şablonu konteynerlemesi kullanılarak yapılandırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="83346-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="83346-114">Çözüm</span><span class="sxs-lookup"><span data-stu-id="83346-114">Resolution</span></span>

<span data-ttu-id="83346-115">Yükleme veya sevkiyat işlemi şu anda sevkiyat onayının başarısız olduğu bir durumdadır.</span><span class="sxs-lookup"><span data-stu-id="83346-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="83346-116">Bu sorunu gidermek için aşağıdaki görevlerden birini tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="83346-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="83346-117">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="83346-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="83346-118">Paketleme yerleşimi son sevkiyat yerleşimi olarak oluşturulan iş kodlarını iptal edin, konum yönergesini yeniden yapılandırın ve yükü yeniden serbest bırakın.</span><span class="sxs-lookup"><span data-stu-id="83346-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="83346-119">Yük satırlarınızı gözden geçirin ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun</span><span class="sxs-lookup"><span data-stu-id="83346-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="83346-120">Yük satırlarınızı gözden geçirmek için aşağıdaki yordamı kullanın ve tüm ilgili işlerin son sevkiyat konumunda tamamlandığından ve miktarların aynı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="83346-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="83346-121">**Ambar yönetimi \> Yükler \> Tüm yükler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="83346-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="83346-122">Sevkiyatın onaylanamadığı ilgili yükü seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="83346-123">**Yük satırları** hızlı sekmesinde, yük satırını seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="83346-124">**Oluşturulan iş miktarı** alanının değerini not alın.</span><span class="sxs-lookup"><span data-stu-id="83346-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="83346-125">Eylem Bölmesinde **Yüklemeler** sekmesindeki **İlgili bilgiler** grubunda **Çalışma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="83346-126">İşin son sevkiyat konumunda tamamlandığını ve teslim alınan iş miktarının yükleme satırındaki oluşturulan iş miktarıyla eşleştiğini doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="83346-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="83346-127">Tüm ölçütlerin karşılandığından emin olmak için bu prosedürü tüm yükleme satırları için yineleyin.</span><span class="sxs-lookup"><span data-stu-id="83346-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="83346-128">Paketleme yerleşimi son sevkiyat yerleşimi olarak oluşturulan iş kodlarını iptal edin, konum yönergesini yeniden yapılandırın ve yükü yeniden serbest bırakın</span><span class="sxs-lookup"><span data-stu-id="83346-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="83346-129">Otomatik konteynerlemenin bulunduğu ile son koyma yerleşimi olarak paketleme yerleşimine sahip iş kodlarını iptal etmek için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="83346-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="83346-130">**Ambar yönetimi \> Periyodik görevler \> Temizleme \>Çalışmayı iptal et**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="83346-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="83346-131">**İşi iptal et** iletişim kutusu açılır.</span><span class="sxs-lookup"><span data-stu-id="83346-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="83346-132">**İş kimliği** alanında, iptal etmek istediğiniz iş kaydının kodunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="83346-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="83346-133">Seçili iş kodu için **İş durumu** değeri şunlardan biri olmalıdır: *Açık*, *Devam Ediyor*, *İptal Edildi*, *Birleştirildi* veya *Kapalı*.</span><span class="sxs-lookup"><span data-stu-id="83346-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="83346-134">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-134">Select **OK**.</span></span>
1. <span data-ttu-id="83346-135">Çalışmayı iptal etmek istediğinizi onaylamak için **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="83346-136">Gerektiğinde diğer iş kodları için bu yordamı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="83346-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="83346-137">Daha fazla bilgi için bkz. [Özel durum işleme için ambar işini iptal etme](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="83346-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="83346-138">Yerleşim yönergesini, dalga şablonu için otomatik konteynerleme ayarlandığında son sevkiyat yerleşimi olarak paketleme yerleşimini kullanmayacak şekilde yeniden yapılandırmak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="83346-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="83346-139">**Ambar Yönetimi \> Kurulum \> Konum yönergeleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="83346-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="83346-140">**İş siparişi türü** alanında *Satış siparişi*'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="83346-141">Otomatik konteynerleme için kullandığınız yerleşim yönergesini seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="83346-142">**Yerleşim Yönergesi Eylemleri** hızlı sekmesi araç çubuğunda **Sorguyu düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="83346-143">Sorgu düzenleyicisi iletişim kutusunda, **Aralık** sekmesinde, **Alan**'ın *Yerleşim profili* olarak ayarlandığı satırı bulun ve bu satırın **Ölçüt** alanının **Paketleme** *Yerleşim türüne* sahip olan bir yerleşim profiline ayarlanmadığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="83346-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="83346-144">Son koyma yerleşimini düzeltmek için **Ölçüt** alanını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="83346-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="83346-145">Yükü yeniden serbest bırakmak ve doğru son sevkiyat yerleşimine sahip iş kodları oluşturmak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="83346-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="83346-146">**Ambar yönetimi \> Yükler \> Yük planlama çalışma ekranı** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="83346-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="83346-147">**Yükler** bölümünde, serbest bırakılması gereken yükü bulun.</span><span class="sxs-lookup"><span data-stu-id="83346-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="83346-148">**Yükler** bölümü araç çubuğunda seçili yükü ambara serbest bırakmak için **Serbest bırak \> Ambara serbest bırak** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="83346-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="83346-149">Gerektiğinde diğer yükler için bu yordamı yineleyin.</span><span class="sxs-lookup"><span data-stu-id="83346-149">Repeat this procedure for the other loads as needed.</span></span>
