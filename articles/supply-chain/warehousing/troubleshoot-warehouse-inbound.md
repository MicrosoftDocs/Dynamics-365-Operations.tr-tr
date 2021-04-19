---
title: Gelen ambar operasyonlarında sorun giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta gelen ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828238"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="6a240-103">Gelen ambar operasyonlarında sorun giderme</span><span class="sxs-lookup"><span data-stu-id="6a240-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a240-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta gelen ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="6a240-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="6a240-105">Şu hata iletisini alıyorum: "%1 kalite emri oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="6a240-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="6a240-106">Küme profili bulunamadı. Lütfen yapılandırmanızı denetleyin."</span><span class="sxs-lookup"><span data-stu-id="6a240-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6a240-107">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6a240-107">Issue description</span></span>

<span data-ttu-id="6a240-108">Bu hata iletisi, kalite yönetiminin (QMS) açık olduğu bir alma işlemiyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="6a240-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="6a240-109">Ortamınızdaki yapılandırmalara bağlı olarak, hata iletisini üreten hareketle ilgili ek ayrıntılar sorunu gidermeye yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="6a240-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6a240-110">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6a240-110">Issue resolution</span></span>

<span data-ttu-id="6a240-111">Önce, [küme malzeme çekme](set-up-cluster-picking.md) kurulumunu gözden geçirin ve küme profillerinizin doğru ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="6a240-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="6a240-112">Küme profilleri ayarlanmadıkça, küme malzeme çekme için bir mobil cihaz menü öğesi kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6a240-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="6a240-113">Ortamınıza bağlı olarak, diğer ilgili yapılandırmaları da gözden geçirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="6a240-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="6a240-114">Karma plaka alma işlemi, Alacak dışındaki herhangi bir değerlendirme kodu için çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6a240-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6a240-115">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6a240-115">Issue description</span></span>

<span data-ttu-id="6a240-116">Değerlendirme kodunun **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlandığında , iade edilen maddeleri işlemek için yalnızca [Karma plaka alma işlemi](mixed-license-plate-receiving.md) menü öğesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a240-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6a240-117">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6a240-117">Issue resolution</span></span>

<span data-ttu-id="6a240-118">Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="6a240-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="6a240-119">Şu anda, karma plaka alma işlemi için yalnızca **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlanan [değerlendirme kodları](../service-management/set-up-disposition-codes.md) desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="6a240-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="6a240-120">Ürün girişlerini güncelleştir periyodik görevini çalıştırdığımda, onaylanmamış satın alma siparişleri onaylanıyor.</span><span class="sxs-lookup"><span data-stu-id="6a240-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="6a240-121">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6a240-121">Issue description</span></span>

<span data-ttu-id="6a240-122">*Ürün girişlerini güncelleştir* periyodik görevini çalıştırdıktan sonra, sistem, stok hareket durumu *Kayıtlı* olan onaylanmamış satın alma siparişlerini otomatik olarak onaylar.</span><span class="sxs-lookup"><span data-stu-id="6a240-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6a240-123">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6a240-123">Issue resolution</span></span>

<span data-ttu-id="6a240-124">*Yük miktarlarını aşırı alma* adlı yeni bir özellikle bu sorunu düzeltilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6a240-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="6a240-125">Bu özelliği açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve aşağıdaki özellikleri (listelendikleri sırada) açın:</span><span class="sxs-lookup"><span data-stu-id="6a240-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="6a240-126">Satınalma siparişi stok hareketlerini yükle ilişkilendir</span><span class="sxs-lookup"><span data-stu-id="6a240-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="6a240-127">Yük miktarlarının fazlasını alma</span><span class="sxs-lookup"><span data-stu-id="6a240-127">Over receipt of load quantities</span></span>

<span data-ttu-id="6a240-128">Daha fazla bilgi için bkz. [Kayıtlı ürün miktarlarını satınalma siparişlerine göre deftere nakletme](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="6a240-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="6a240-129">Gelen siparişleri kaydettiğimde, şu hata iletisini alıyorum: "miktar geçerli değil."</span><span class="sxs-lookup"><span data-stu-id="6a240-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="6a240-130">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="6a240-130">Issue description</span></span>

<span data-ttu-id="6a240-131">**Plaka gruplandırma ilkesi** alanı gelen siparişleri kaydetmek için kullanılan bir mobil aygıt menü öğesi için *Kullanıcı tanımlı* olarak ayarlanmışsa, bir hata iletisi alırsınız ("miktar geçerli değil") ve kaydı tamamlayamazsınız.</span><span class="sxs-lookup"><span data-stu-id="6a240-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="6a240-132">Sorun nedeni</span><span class="sxs-lookup"><span data-stu-id="6a240-132">Issue cause</span></span>

<span data-ttu-id="6a240-133">*Kullanıcı tanımlı*, Plaka gruplama ilkesi olarak kullanıldığında sistem, gelen stoku birim sıra grubunda belirtildiği gibi ayrı plakalara böler.</span><span class="sxs-lookup"><span data-stu-id="6a240-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="6a240-134">Alınmakta olan maddeyi izlemek için toplu iş veya seri numaraları kullanılıyorsa, her toplu iş veya seri miktarı kaydedilen her plaka için belirtilmelidir.</span><span class="sxs-lookup"><span data-stu-id="6a240-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="6a240-135">Bir plaka için belirtilen miktar, geçerli boyutlar için hâlâ teslim alınması gereken miktarı aşarsa, hata iletisini alırsınız.</span><span class="sxs-lookup"><span data-stu-id="6a240-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="6a240-136">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="6a240-136">Issue resolution</span></span>

<span data-ttu-id="6a240-137">**Plaka gruplandırma ilkesi** alanının *Kullanıcı tanımlı* olarak ayarlandığı bir mobil aygıt menü öğesini kullanarak bir öğeyi kaydettiğinizde, sistem plaka numaralarını, toplu iş numaralarını veya seri numaralarını onaylamanızı veya girmenizi gerektirebilir.</span><span class="sxs-lookup"><span data-stu-id="6a240-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="6a240-138">Plaka onayı sayfasında, sistem, geçerli plakaya ayrılan miktarı gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a240-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="6a240-139">Toplu iş veya seri onay sayfalarında, sistem geçerli plakanın üzerinde hâlâ alınması gereken miktarı gösterir.</span><span class="sxs-lookup"><span data-stu-id="6a240-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="6a240-140">Ayrıca, bu plaka ve seri numarası birleşimi için kaydedilecek miktarı girebileceğiniz bir alan da içerir.</span><span class="sxs-lookup"><span data-stu-id="6a240-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="6a240-141">Bu durumda, plaka için kaydedilen miktarın hâlâ teslim alınması gereken miktardan fazla olmadığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="6a240-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="6a240-142">Alternatif olarak, gelen sipariş kaydında çok fazla plaka oluşturulursa, **Plaka gruplandırma ilkesi** alanının değeri *Plaka gruplandırma* ile değiştirilebilir, maddeye yeni bir birim dizi grubu atanabilir veya birim sıra grubu için **plaka gruplandırma** seçeneği devre dışı bırakılabilir.</span><span class="sxs-lookup"><span data-stu-id="6a240-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
