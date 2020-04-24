---
title: Dynamics 365 Supply Chain Management 10.0.6'daki yenilikler veya değişiklikler (Kasım 2019)
description: Bu konuda, Dynamics 365 Supply Chain Management 10.0.6'daki yeni veya değişen özellikler açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac1
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 319ba09184c087a194b664ca87076d57c6ba0c66
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201560"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="4aa6f-103">Dynamics 365 Supply Chain Management 10.0.6'daki yenilikler veya değişiklikler (Kasım 2019)</span><span class="sxs-lookup"><span data-stu-id="4aa6f-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aa6f-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management 10.0.6'daki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="4aa6f-105">Bu sürümün derleme numarası 10.0.234'tür.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="4aa6f-106">Genel kullanılabilirlik tarihi Kasım ayında olmasına karşın Ekim ayındaki erken sürüm için yeni özellikler bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="4aa6f-107">10.0.6 sürümü hakkında daha fazla bilgi için bkz. [Ek kaynaklar](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="4aa6f-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="4aa6f-108">Ürün yapılandırma modelleri V2 veri varlığı</span><span class="sxs-lookup"><span data-stu-id="4aa6f-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="4aa6f-109">"Ürün yapılandırma modelleri" veri varlığının ikinci sürümü yayınlandı ("ürün yapılandırma modelleri V2" olarak adlandırılmıştır).</span><span class="sxs-lookup"><span data-stu-id="4aa6f-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="4aa6f-110">"418-ürün yapılandırma modelleri" varsayılan şablonunun da içe aktarma/dışa aktarma çerçevesi şablonlarında yeni "ürün yapılandırma modelleri V2" veri varlığını kullanması gerekmektedir.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="4aa6f-111">Şablon otomatik olarak güncelleştirilmez, bu nedenle şablonu varsayılan olarak el ile yüklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="4aa6f-112">V2 varlığı, V1 varlığının boyut sınırlamalarını çözmek amacıyla bir satırı satır içi yerine ekli ayrı bir dosya olarak dışa aktarır.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="4aa6f-113">Bu değişikliği yapmak için ne yapmanız gerekir?</span><span class="sxs-lookup"><span data-stu-id="4aa6f-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="4aa6f-114">V1 varlığı kullanım dışı bırakıldığından, V1'den V2'ye geçişi başlatmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="4aa6f-115">"418-ürün yapılandırma modelleri" şablonunu kullanıyorsanız, "varsayılan şablonları yükle" düğmesine tıklayabilir ve "418 – ürün yapıladırma modelleri" şablonunu yeniden yükleyebilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4aa6f-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="4aa6f-116">Varolan sistemlerle uyumluluğu korumak istiyorsanız, tümleştirmeleri yeni şablona taşııncaya kadar varolan şablonu ve (kullanım dışı) V1 varlığını kullanmaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="4aa6f-117">Özellik yönetimi geliştirmeleri</span><span class="sxs-lookup"><span data-stu-id="4aa6f-117">Feature management enhancements</span></span>
<span data-ttu-id="4aa6f-118">Özellik yönetimi şimdi tüm yeni özellikleri varsayılan olarak etkinleştirmenize, bir özelliği etkinleştirmek için onay gerektirmenize ve önceden etkinleştirilmemiş olan tüm özellikleri etkinleştirmenize olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="4aa6f-119">Satınalma sözleşmesi sorumlu taraf</span><span class="sxs-lookup"><span data-stu-id="4aa6f-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="4aa6f-120">Artık, Satınalma sözleşmesi sınıflandırma formunda ve sonuçta elde edilen Satınalma sözleşmelerinde birincil ve ikincil sorumlu tarafları tanımlama olanağınız vardır.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="4aa6f-121">Bu, kullanıcıya sözleşmeleri denetleyenlere erişim olanağı sağlar.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="4aa6f-122">Satınalma siparişi satırındaki RFQ bağlantısı</span><span class="sxs-lookup"><span data-stu-id="4aa6f-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="4aa6f-123">Satınalma siparişi satırlarından, oluşturuldukları karşılık gelen RFQ satırlarına bir referans bağlantısı ekleyebilirsiniz; bu, kullanıcıya destekleyen teklif talebi belgesinin kolaylıkla sunulmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4aa6f-124">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4aa6f-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4aa6f-125">Hata düzeltmeleri</span><span class="sxs-lookup"><span data-stu-id="4aa6f-125">Bug fixes</span></span>
<span data-ttu-id="4aa6f-126">10.0.6'nın parçası olan güncelleştirmelerin her birine dahil edilen hata düzeltmeleri hakkında bilgi için, Lifecycle Services'ta (LCS) oturum açın ve [BB makalesini](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="4aa6f-127">Platform update 30</span><span class="sxs-lookup"><span data-stu-id="4aa6f-127">Platform update 30</span></span>
<span data-ttu-id="4aa6f-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 Platform update 30 içerir.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="4aa6f-129">Platform update 30 hakkında daha fazla bilgi edinmek için bkz. [Platform update 30'daki yenilikler veya değişiklikler](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="4aa6f-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="4aa6f-130">Dynamics 365: 2019 sürüm dalgası 2 planı</span><span class="sxs-lookup"><span data-stu-id="4aa6f-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="4aa6f-131">İş uygulamalarımız veya platformumuz için gelecek olan ve en son yayımlanan özellikleri merak ediyor musunuz?</span><span class="sxs-lookup"><span data-stu-id="4aa6f-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="4aa6f-132">[Dynamics 365: 2019 sürüm dalgası 2 planını](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/) inceleyin.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="4aa6f-133">Baştan sona tüm ayrıntıları, planlama için kullanabileceğiniz tek bir belgede bir araya getirdik.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="4aa6f-134">Kaldırılan ve kullanım dışı bırakılan Supply Chain Management özellikleri</span><span class="sxs-lookup"><span data-stu-id="4aa6f-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="4aa6f-135">[Dynamics 365 Supply Chain Management'taki kaldırılmış veya kullanım dışı bırakılmış özellikler](removed-deprecated-features-scm-updates.md) konusu Supply Chain Management için kaldırılan veya kullanım dışı bırakılan veya kaldırılması ya da kullanım dışı bırakılması planlanan özellikleri açıklar.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="4aa6f-136">*Kaldırılan* özellik artık üründe bulunmaz.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="4aa6f-137">*Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="4aa6f-138">Herhangi bir özellik üründen kaldırılmadan önce, kullanım dışı bırakma bildirimi kaldırma işleminden 12 ay önce [Dynamics 365 Supply Chain Management'taki kaldırılan veya kullanım dışı bırakılan özelliker](removed-deprecated-features-scm-updates.md) konusunda duyurulacaktır.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="4aa6f-139">Yalnızca derleme zamanını etkileyen ancak korumalı alan ve üretim ortamlarıyla ikili uyumlu olan son dakika değişiklikleri için kullanım dışı bırakma süresi 12 aydan kısa olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="4aa6f-140">Genellikle, bunlar derleyiciye yapılması gereken işlevsel güncelleştirmelerdir.</span><span class="sxs-lookup"><span data-stu-id="4aa6f-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
