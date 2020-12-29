---
title: Ambar yapılandırması ile ilgili sorunları giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ı yapılandırırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9bbe92627f53b3b4b04597be144d602b3cae7ed7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646119"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="6e613-103">Ambar yapılandırması ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="6e613-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e613-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ı yapılandırırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6e613-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="6e613-105">Şu hata iletisini alıyorum: "Plaka veya konum geçerli değil."</span><span class="sxs-lookup"><span data-stu-id="6e613-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e613-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6e613-106">Issue description</span></span>

<span data-ttu-id="6e613-107">Bu hata iletisini, bir plaka kimliğini veya konumu taradığınızda alırsınız.</span><span class="sxs-lookup"><span data-stu-id="6e613-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e613-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6e613-108">Issue resolution</span></span>

<span data-ttu-id="6e613-109">Plaka kimliğinin başka bir şey tarafından ayrılmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="6e613-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="6e613-110">Bu sorun, bir kullanıcının ambar uygulamasında taradığı değer, hem geçerli bir konum hem de geçerli bir plaka olduğunda oluşurdu.</span><span class="sxs-lookup"><span data-stu-id="6e613-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="6e613-111">Ancak, bu sorun 10.0.11 sürümünde giderilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6e613-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="6e613-112">Şu hata iletisini alıyorum: "Bu konum için plaka belirtilmelidir."</span><span class="sxs-lookup"><span data-stu-id="6e613-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e613-113">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6e613-113">Issue description</span></span>

<span data-ttu-id="6e613-114">Bu hata iletisini, gelişmiş ambar yönetimi (WMS) için etkinleştirilen bir ambarı kullanarak transfer emri oluşturup ardından iş tamamlandıktan sonra sevkiyatı onaylamaya çalışırsanız alırsınız.</span><span class="sxs-lookup"><span data-stu-id="6e613-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e613-115">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6e613-115">Issue resolution</span></span>

<span data-ttu-id="6e613-116">**Varsayılan giriş konumu** alanı, "çıkış" ambarına ait bir transit ambar için boştur.</span><span class="sxs-lookup"><span data-stu-id="6e613-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="6e613-117">Bu sorunu gidermek için transit ambarında varsayılan bir giriş konumu belirtin.</span><span class="sxs-lookup"><span data-stu-id="6e613-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="6e613-118">Bu konumun plaka denetimli olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="6e613-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="6e613-119">Şu hata iletisini alıyorum: "İş türü geçerli olmadığından, Stok durumu değişikliği için iş şablonu satırı oluşturamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6e613-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="6e613-120">Farklı bir iş türü seçin."</span><span class="sxs-lookup"><span data-stu-id="6e613-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e613-121">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6e613-121">Issue description</span></span>

<span data-ttu-id="6e613-122">Bir çalışma şablonu için, **Çalışma şablonu ayrıntıları** bölümünün **İş türü** sütunundan *Stok durumu değişikliği*'ni seçemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e613-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e613-123">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6e613-123">Issue resolution</span></span>

<span data-ttu-id="6e613-124">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="6e613-124">This behavior is by design.</span></span> <span data-ttu-id="6e613-125">*Stok durumu değişikliği* iş türü, yalnızca sistem süreçleri tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6e613-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="6e613-126">Bu değer yapılandırılamaz.</span><span class="sxs-lookup"><span data-stu-id="6e613-126">It can't be configured.</span></span> <span data-ttu-id="6e613-127">İş türleri listesi bir numaralandırma olarak düzeltildiğinden, ekstra girişler, **İş türü** açılan menüsünden filtre dışı bırakılamaz.</span><span class="sxs-lookup"><span data-stu-id="6e613-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="6e613-128">Şu hata iletisini alıyorum: "Miktar 1% birimi için geçerli değil."</span><span class="sxs-lookup"><span data-stu-id="6e613-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e613-129">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6e613-129">Issue description</span></span>

<span data-ttu-id="6e613-130">Tek bir konumda birden fazla plakası olan malzeme çekme işi varken miktar *ea* birimi için geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="6e613-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e613-131">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6e613-131">Issue resolution</span></span>

<span data-ttu-id="6e613-132">Serbest bırakılan ürün veya ürün varyantındaki **Birim dizisi grup kodu** ve **Birim dönüştürmeleri** alanlarının doğru ayarlandığını doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="6e613-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="6e613-133">Hata iletisinin sürüm 10.0.15'te geliştirilmiş olduğunu (bkz. [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)) unutmayın.</span><span class="sxs-lookup"><span data-stu-id="6e613-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="6e613-134">Yeni hata iletisi şöyledir: "Miktar geçerli değil.</span><span class="sxs-lookup"><span data-stu-id="6e613-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="6e613-135">Beklenen %1 %2."</span><span class="sxs-lookup"><span data-stu-id="6e613-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="6e613-136">Satış siparişi yerine koyma işinin konum yönergelerinde, çoklu SKU seçeneği birden çok konum yönergesi eylemini değerlendirmez.</span><span class="sxs-lookup"><span data-stu-id="6e613-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e613-137">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6e613-137">Issue description</span></span>

<span data-ttu-id="6e613-138">*Satış siparişleri* iş emri türünün konum yönergeleri ve *Yerine koyma* iş türü, **Birden Fazla SKU** seçeneği seçiliyken, çoklu konum yönergesi eylemlerini değerlendirmez.</span><span class="sxs-lookup"><span data-stu-id="6e613-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="6e613-139">Yalnızca ilk konum yönergesi eylemi değerlendirilir.</span><span class="sxs-lookup"><span data-stu-id="6e613-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e613-140">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6e613-140">Issue resolution</span></span>

<span data-ttu-id="6e613-141">10.0.15 sürümüne *Çoklu SKU konum yönergeleri için tüm eylemleri değerlendir* adlı yeni bir özellik eklendi (bkz. [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="6e613-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="6e613-142">Bu özellik çoklu SKU konum yönergeleri için tüm eylemleri değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="6e613-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="6e613-143">Bu özelliğe gereksinim duyarsanız, etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e613-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="6e613-144">Kısmi malzeme çekme yapmak için ambar uygulamasını kullanamıyorum.</span><span class="sxs-lookup"><span data-stu-id="6e613-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e613-145">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6e613-145">Issue description</span></span>

<span data-ttu-id="6e613-146">Satış siparişleri ve transfer emirleri için maddeleri atlayamazsınız ve kısmi malzeme çekme yapamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6e613-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e613-147">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6e613-147">Issue resolution</span></span>

<span data-ttu-id="6e613-148">**Mobil cihaz menü öğeleri** sayfasında, satış siparişlerini veya transfer emirlerini işleyecek şekilde ayarlanan her menü öğesi için **Genel** hızlı sekmesindeki **İşin bölünmesine izin ver** seçeneğini *Evet* olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6e613-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="6e613-149">Kısmi miktarlı iş için stok durumu değişikliğini nasıl yapabilirim?</span><span class="sxs-lookup"><span data-stu-id="6e613-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="6e613-150">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6e613-150">Issue description</span></span>

<span data-ttu-id="6e613-151">Partinin kısmi bir miktarı için stok durumu değişikliği yapmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="6e613-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6e613-152">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6e613-152">Issue resolution</span></span>

<span data-ttu-id="6e613-153">Çalışanların bu değişikliği yapmasını sağlamak için ambar uygulamasında bir menü öğesi oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e613-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="6e613-154">**Mobil cihaz menü öğeleri** sayfasında, şu özelliklere sahip bir menü öğesi oluşturun (veya düzenleyin):</span><span class="sxs-lookup"><span data-stu-id="6e613-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="6e613-155">**Mod:** *İş*</span><span class="sxs-lookup"><span data-stu-id="6e613-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="6e613-156">**Varolan çalışmayı kullan:** *Hayır*</span><span class="sxs-lookup"><span data-stu-id="6e613-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="6e613-157">**İş oluşturma işlemi:** *Hareket*</span><span class="sxs-lookup"><span data-stu-id="6e613-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="6e613-158">**Stok durumunu görüntüle:** *Evet*</span><span class="sxs-lookup"><span data-stu-id="6e613-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="6e613-159">Sayfadaki diğer alanları gerektiği gibi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e613-159">You can set other fields on the page as you require.</span></span>
