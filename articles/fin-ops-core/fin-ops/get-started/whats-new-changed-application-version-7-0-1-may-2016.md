---
title: Dynamics AX uygulama sürümü 7.0.1'deki yenilikler ve değişiklikler (Mayıs 2016)
description: Bu makale Microsoft Dynamics AX uygulama sürümü 7.0.1'da yeni veya değişen özellikler açıklanmaktadır. Bu sürüm Mayıs 2016 tarihinde yayımlanmıştır ve 7.0.1265.23014 yapım numarasına sahiptir.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 715e0f8d08c6abbde35eb917cddc4ecf4b7b67ed
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811468"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="0b0ba-104">Dynamics AX uygulama sürümü 7.0.1'deki yenilikler ve değişiklikler (Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="0b0ba-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b0ba-105">Bu makale Microsoft Dynamics AX uygulama sürümü 7.0.1'da yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="0b0ba-106">Bu sürüm Mayıs 2016 tarihinde yayımlanmıştır ve 7.0.1265.23014 yapım numarasına sahiptir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="0b0ba-107">Elektronik raporlama (ER)</span><span class="sxs-lookup"><span data-stu-id="0b0ba-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="0b0ba-108">Ne yapabilirsiniz?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-108">What can you do?</span></span> | <span data-ttu-id="0b0ba-109">Bu neden önemlidir?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0b0ba-110">Kullanıcıların istedikleri finansal boyutları seçebilmeleri için Elektronik raporlama (ER) raporları tasarlarken bir çalışma zamanı iletişim kutusu yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="0b0ba-111">Çalışma zamanında, ER raporunu çalıştırma iletişim kutusunda kullanıcılar birden çok finansal boyut seçebilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="0b0ba-112">Seçili finansal boyutların ayrıntıları oluşturulan elektronik belgede görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="0b0ba-113">ER raporunun tasarımı sırasında istenen veri kaynağına tek bir eşleme aracılığıyla birden çok finansal boyuta erişimi yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="0b0ba-114">Aynı ER raporu yapılandırması kullanıcı tarafından seçilen veya geçerli tüzel kişiliği veya kurulumu için yapılandırılan mali boyutların sayısından bağımsız olarak, mali boyutların ayrıntılarıyla birlikte hareket verileri sunan elektronik belgeler oluşturmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="0b0ba-115">ER raporunu OPENXML çalışma sayfası biçiminde oluşturulan bir elektronik belgenin dinamik olarak oluşturulan sütunlarına veri girmek üzere yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="0b0ba-116">ER raporu oluşturulan bir OPENXML çalışma sayfasına yatay olarak yinelenen sütunlar aracılığıyla veri girebilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="0b0ba-117">Bu nedenle aynı ER raporu yapılandırması dinamik olarak oluşturulan sütun sayısı farklı olan elektronik belgeler oluşturmak için yeniden kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="0b0ba-118">ER hedeflerini Bir biçimin çıkış sonucunun dosya, e-posta veya arşiv (Microsoft SharePoint klasörü veya Microsoft Azure Depolama) gibi belirli bir hedefe yönlendirileceği şekilde yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="0b0ba-119">Önceden bir ER yapılandırması çalıştırdığınızda dosyayı kaydetmek veya açmak için kullanıcı eylemi gerektiren bir ileti kutusu görüntüleniyordu.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="0b0ba-120">Artık her bir biçim yapılandırması ve her bir çıkış bileşeni (bir klasör veya bir dosya) için ayrı bir hedefi önceden yapılandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="0b0ba-121">Uygun erişim haklarına sahip kullanıcılar çalışma zamanında hedef ayarlarını da değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="0b0ba-122">POS – Microsoft Dynamics AX Perakende</span><span class="sxs-lookup"><span data-stu-id="0b0ba-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="0b0ba-123">Ne yapabilirsiniz?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-123">What can you do?</span></span> | <span data-ttu-id="0b0ba-124">Bu neden önemlidir?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0b0ba-125">Google Chrome tarayıcısını kullanın.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="0b0ba-126">Perakendeciler artık Chrome tarayıcısından Bulut POS uygulamasını başlatabilir ve Bulut POS'un Microsoft Edge ve Internet Explorer sürümlerinde bulunan tüm işlevleri kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="0b0ba-127">Mali raporlama</span><span class="sxs-lookup"><span data-stu-id="0b0ba-127">Financial reporting</span></span>

| <span data-ttu-id="0b0ba-128">Ne yapabilirsiniz?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-128">What can you do?</span></span> | <span data-ttu-id="0b0ba-129">Bu neden önemlidir?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0b0ba-130">Mali raporlama veri reyonunu yeniden oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="0b0ba-131">Dynamics AX veritabanları ortamlar arasında taşıdığınızda veya ortama başka aykırı değişiklikler yaptığınızda Finansal raporlama veritabanının yeniden oluşturulması gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="0b0ba-132">Veritabanını sizin için yeniden oluşturmak amacıyla bir Windows PowerShell komut dosyası sağlandı.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="0b0ba-133">Artık geçerli olmayan rapor tasarımcısı seçeneklerini belirleyemezsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="0b0ba-134">Management Reporter pazar içi sürümlerinde kullanılan pek çok rapor tasarımcısı seçeneği Dynamics AX'in bu sürümünde geçerli değildir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="0b0ba-135">Bu seçenekler, finansal rapor tasarımıyla, çıktıyla ve bağlama ile ilgiliydi.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="0b0ba-136">Bu seçenekler, kullanıcı hataları önlemek için mali rapor tasarımcısından kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="0b0ba-137">Mali yönetim</span><span class="sxs-lookup"><span data-stu-id="0b0ba-137">Financial management</span></span>

| <span data-ttu-id="0b0ba-138">Ne yapabilirsiniz?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-138">What can you do?</span></span> | <span data-ttu-id="0b0ba-139">Bu neden önemlidir?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="0b0ba-140">Borç hesapları ödemeleri için pozitif ödeme dosyaları oluşturun.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="0b0ba-141">Pozitif ödeme dosyaları çek sahteciliğini önlemeye yardımcı olmak için oluşturulabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="0b0ba-142">Ambar ve üretim</span><span class="sxs-lookup"><span data-stu-id="0b0ba-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0b0ba-143">Ne yapabilirsiniz?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-143">What can you do?</span></span></th>
<th><span data-ttu-id="0b0ba-144">Bu neden önemlidir?</span><span class="sxs-lookup"><span data-stu-id="0b0ba-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0b0ba-145">Belirli yerleşimlerde ürün kümeleri için iş oluşturma işlemini denetleyen bir ambar çalışma ilkesi tanımlayın.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="0b0ba-146">Ambar işlemler, her zaman iş içermez.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="0b0ba-147">Yeni ambar çalışma ilkesini kullanarak, hammadde çekme ve tamamlanmış malların yerine koyması işlerinin oluşturulmasını, çeşitli bir ürün dizisi veya belirtilen konumlar için engelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0b0ba-148">Ürün çıkış konumunun plaka denetimli olmadığını belirtin.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="0b0ba-149">Artık bir ürün çıkış konumunun plaka denetimli olmadığını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="0b0ba-150">Örneğin, bu özellik yukarı doğru bir üretim emri maddeleri aşağı doğru bir ürün emri için ürün giriş konumu görevi gören bir konuma doğrudan tamamlandı olarak bildirdiğinde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0b0ba-151">Aynı maddenin farklı üretim boyutlarına sahip maddeleri içeren ürün reçetelerini destekleyin.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="0b0ba-152">Üretimde bir veya daha fazla üretim boyutu kullanırken, maddeyi aynı maddenin farklı seçeneklerine göre üretmek istediğiniz durumlar olabilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="0b0ba-153">Daha fazla bilgi için bkz. <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">bu blog</a>.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0b0ba-154">Ürün reçetelerinin birinci düzeyinde döngüsel yapıya sahip üretim emirleri malzeme kaynak planlamasında ürün reçetesi düzeyi hesaplamanın dışında bırakılır.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="0b0ba-155">Ürün reçetesi hiyerarşisinde döngüselliğe neden olan üretim emirlerinde seçenek üretmek için doğru ürün reçetesi düzeyleri atamak mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0b0ba-156">Malzeme kaynak planlaması ve maliyet hesaplaması için ayrı ürün reçetesi düzeyleri hesaplayın:</span><span class="sxs-lookup"><span data-stu-id="0b0ba-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="0b0ba-157">Malzeme kaynak planlamasında, ürün reçetesi düzeyleri yeni <strong>ReqItemLevel</strong> tablosunda hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="0b0ba-158">Biten üretim emirleri hesaplamada dikkate alınmaz.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="0b0ba-159">Üretim maliyeti hesaplamasında, ürün reçetesi düzeyleri <strong>InventTable</strong> üzerinde hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="0b0ba-160">Biten üretim emirleri hesaplamaya dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="0b0ba-161">Malzeme kaynak planlaması çalıştırırken, örneğin master planlama plan planlama ve açılım, yalnızca malzeme kaynak planlamasında kullanılan ürün reçetesi düzeylerinin hesaplanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="0b0ba-162">Diğer bir deyişle, üretim maliyeti hesaplamasında kullanılan ürün reçetesi düzeylerini hesaplamaya gerek yoktur.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="0b0ba-163">Maliyet işlemleri çalıştırırken (örneğin stok kapatma), yalnızca üretim maliyeti hesaplamasında kullanılan ürün reçetesi düzeylerinin yeniden hesaplanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="0b0ba-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="0b0ba-164">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="0b0ba-164">Additional resources</span></span>

[<span data-ttu-id="0b0ba-165">Finance and Operations giriş sayfasındaki yenilikler veya değişiklikler</span><span class="sxs-lookup"><span data-stu-id="0b0ba-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="0b0ba-166">Yeni veya güncelleştirilmiş kılavuzlar (Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="0b0ba-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
