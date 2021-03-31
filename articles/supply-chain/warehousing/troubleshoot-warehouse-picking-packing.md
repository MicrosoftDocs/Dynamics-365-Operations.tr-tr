---
title: Malzeme çekme ve paketleme ile ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta malzeme çekme ve paketleme işlemlerinde karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223254"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="93bfc-103">Malzeme çekme ve paketleme ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="93bfc-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93bfc-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta malzeme çekme ve paketleme işlemlerinde karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="93bfc-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="93bfc-105">Şu hata iletisini alıyorum: "Boyut seri numarası ayarlandığında boyut konumu boş bırakılamaz."</span><span class="sxs-lookup"><span data-stu-id="93bfc-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-106">Issue description</span></span>

<span data-ttu-id="93bfc-107">Bu hata iletisini, gelişmiş ambar yönetimi (WMS) için etkinleştirilen bir ambarı kullanarak bir seri madde için transfer emri oluşturup ardından iş tamamlandıktan sonra sevkiyatı onaylamaya çalışırsanız alırsınız.</span><span class="sxs-lookup"><span data-stu-id="93bfc-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-108">Issue resolution</span></span>

<span data-ttu-id="93bfc-109">**Varsayılan giriş konumu** alanı, "çıkış" ambarına ait bir transit ambar için boştur.</span><span class="sxs-lookup"><span data-stu-id="93bfc-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="93bfc-110">Bu sorunu gidermek için transit ambarında varsayılan bir giriş konumu belirtin.</span><span class="sxs-lookup"><span data-stu-id="93bfc-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="93bfc-111">Bu konumun plaka denetimli olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="93bfc-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="93bfc-112">Şu hata iletisini alıyorum: "Geçersiz plaka."</span><span class="sxs-lookup"><span data-stu-id="93bfc-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-113">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-113">Issue description</span></span>

<span data-ttu-id="93bfc-114">Bu hata iletisini, bir plaka kimliğini taradığınızda ambar uygulamasında alırsınız.</span><span class="sxs-lookup"><span data-stu-id="93bfc-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-115">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-115">Issue resolution</span></span>

<span data-ttu-id="93bfc-116">Plaka kimliğinin plaka tablosunda bulunduğundan ve plakadaki maddelerin ve miktarların kullanılabildiğinden (başka bir deyişle, engellenmemiş olduğundan) emin olun.</span><span class="sxs-lookup"><span data-stu-id="93bfc-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="93bfc-117">Şu hata iletisini alıyorum: "'Yük ağırlığı' alanı (=-%1) yalnızca pozitif sayılar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="93bfc-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="93bfc-118">Güncelleştirme iptal edildi."</span><span class="sxs-lookup"><span data-stu-id="93bfc-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-119">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-119">Issue description</span></span>

<span data-ttu-id="93bfc-120">Bu hata iletisini, ambalaj konumlarından hazırlama konumlarına veya yerleştirme konumlarına iş işlenirken açık çalışma olduğunda alırsınız.</span><span class="sxs-lookup"><span data-stu-id="93bfc-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-121">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-121">Issue resolution</span></span>

<span data-ttu-id="93bfc-122">Bu sorunu gidermek için **Sistem yönetimi \> Periyodik görevler \> Veritabanı \> Tutarlılık denetimi** bölümüne gidin ve **Ambar yükü ağırlık tutarlılık denetimi** için işlemi çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="93bfc-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="93bfc-123">Şu hata iletisini alıyorum: "Miktar %1 birimi için geçerli değil."</span><span class="sxs-lookup"><span data-stu-id="93bfc-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-124">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-124">Issue description</span></span>

<span data-ttu-id="93bfc-125">Bu hata iletisini, çoklu toplu işler arasında bir *bölmeli malzeme çekme* işlemi gerçekleştirmeye çalıştığınızda alırsınız.</span><span class="sxs-lookup"><span data-stu-id="93bfc-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-126">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-126">Issue resolution</span></span>

<span data-ttu-id="93bfc-127">Ambar çalışanının ambar uygulamasındaki *Kısa malzeme çekme* işlemini kullanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="93bfc-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="93bfc-128">Aynı konumdan birden fazla toplu iş çekmeyi deniyorsanız ambar uygulamasındaki **Tamamı** seçeneğini de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93bfc-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="93bfc-129">Stoğu, plaka denetimli bir konuma taşıyamıyorum.</span><span class="sxs-lookup"><span data-stu-id="93bfc-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-130">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-130">Issue description</span></span>

<span data-ttu-id="93bfc-131">Bir yükte çekilen malzeme miktarlarını azaltamazsınız.</span><span class="sxs-lookup"><span data-stu-id="93bfc-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-132">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-132">Issue resolution</span></span>

<span data-ttu-id="93bfc-133">Önceki sürümlerde, bir yükte çekilen malzeme miktarlarını azaltamazsınız.</span><span class="sxs-lookup"><span data-stu-id="93bfc-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="93bfc-134">Ancak, artık plaka denetimli bir konumuna malzeme çekmeyi geri alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="93bfc-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="93bfc-135">**Çekilen malzeme miktarını azalt** sayfasındaki yük satırı için hem **Konum** değerini hem de **Plaka** değerini belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="93bfc-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="93bfc-136">Ambara göre bir teslimat notu veya ambalaj içeriği yazdırabilir miyim?</span><span class="sxs-lookup"><span data-stu-id="93bfc-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-137">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-137">Issue description</span></span>

<span data-ttu-id="93bfc-138">**İş denetim şablonu satırı güncelleştirmesi** sayfasında, teslim notu veya ambalaj içeriğini ambara veya siteye göre yazdırmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="93bfc-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-139">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-139">Issue resolution</span></span>

<span data-ttu-id="93bfc-140">Yazdırma yönetimi ayarlarını kullanarak bir belgeyi yazdırdığınızda, **İş denetim şablonu satırı güncelleştirme** sayfasında **Yazdırma ayarlarını düzenle**'yi seçmek yerine kapsamı (tesis/ambar) bunun Yazdırma yönetimi üzerinden sınırlandırın.</span><span class="sxs-lookup"><span data-stu-id="93bfc-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="93bfc-141">Bir satış siparişinden deftere nakledildikten sonra sevk irsaliyesini iptal edemiyorum.</span><span class="sxs-lookup"><span data-stu-id="93bfc-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-142">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-142">Issue description</span></span>

<span data-ttu-id="93bfc-143">Malzeme çekme ve sevkiyat işlemleri WMS için etkinleştirildiğinde, bir satış siparişinden deftere nakledildikten sonra sevk irsaliyesini iptal edemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="93bfc-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-144">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-144">Issue resolution</span></span>

<span data-ttu-id="93bfc-145">WMS için etkinleştirilen maddelere ait deftere nakledilen sevk irsaliyelerini düzeltmek için deftere nakletme işlemi siparişten değil, yükten oluşturulmalıdır.</span><span class="sxs-lookup"><span data-stu-id="93bfc-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="93bfc-146">Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="93bfc-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="93bfc-147">Genel olarak, ambar yönetimi işlemleri üzerinden malzemesi çekilen ve sevk edilen bir satış siparişi sevk irsaliyesi yük veya sevkiyattan ve satış siparişi belgesinden güncelleştirilen bir sevk irsaliyesi olabilir.</span><span class="sxs-lookup"><span data-stu-id="93bfc-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="93bfc-148">Ancak, satış siparişini satış siparişi belgesinden güncelleştiren sevk irsaliyesi durumunda, sevk irsaliyesi tersine çevirme işlemi yükten veya satış siparişinden yapılamaz.</span><span class="sxs-lookup"><span data-stu-id="93bfc-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="93bfc-149">Bu nedenle, sevk irsaliyesini yükten deftere nakletme işlemini kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="93bfc-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="93bfc-150">Bu durumda, yükten gerçekleştirilmesi gereken ters işlem etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="93bfc-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="93bfc-151">Şu hata iletisini alıyorum: "Küme için yeterli iş bulunamadı."</span><span class="sxs-lookup"><span data-stu-id="93bfc-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="93bfc-152">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="93bfc-152">Issue description</span></span>

<span data-ttu-id="93bfc-153">*Sistem tarafından yönlendirilen küme malzemesi çekme* sürecini kullandığınızda, örneğin 10 pozisyonun çekildiği bir küme profili yapılandırırsanız işlem, 10 pozisyona kadar malzeme çekme için yeterli iş olduğunda planlanan şekilde çalışır.</span><span class="sxs-lookup"><span data-stu-id="93bfc-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="93bfc-154">Bununla birlikte, seçebileceğiniz yalnızca sekiz konum varsa, bir küme için yeterli iş olmadığı için bu hata iletisini alırsınız.</span><span class="sxs-lookup"><span data-stu-id="93bfc-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="93bfc-155">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="93bfc-155">Issue resolution</span></span>

<span data-ttu-id="93bfc-156">Bu sorunu gidermek için küme profilini düzenleyin ve **Pozisyonları etkinleştir** seçeneğini *Hayır* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="93bfc-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]