---
title: Gelen ambar operasyonlarında sorun giderme
description: Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta gelen ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.
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
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250894"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="b1252-103">Gelen ambar operasyonlarında sorun giderme</span><span class="sxs-lookup"><span data-stu-id="b1252-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1252-104">Bu konuda, Microsoft Dynamics 365 Supply Chain Management'ta gelen ambar işlemleriyle çalışırken karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmıştır.</span><span class="sxs-lookup"><span data-stu-id="b1252-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="b1252-105">Şu hata iletisini alıyorum: "%1 kalite emri oluşturuldu.</span><span class="sxs-lookup"><span data-stu-id="b1252-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="b1252-106">Küme profili bulunamadı. Lütfen yapılandırmanızı denetleyin."</span><span class="sxs-lookup"><span data-stu-id="b1252-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1252-107">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b1252-107">Issue description</span></span>

<span data-ttu-id="b1252-108">Bu hata iletisi, kalite yönetiminin (QMS) açık olduğu bir alma işlemiyle ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="b1252-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="b1252-109">Ortamınızdaki yapılandırmalara bağlı olarak, hata iletisini üreten hareketle ilgili ek ayrıntılar sorunu gidermeye yardımcı olabilir.</span><span class="sxs-lookup"><span data-stu-id="b1252-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1252-110">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b1252-110">Issue resolution</span></span>

<span data-ttu-id="b1252-111">Önce, [küme malzeme çekme](set-up-cluster-picking.md) kurulumunu gözden geçirin ve küme profillerinizin doğru ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="b1252-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="b1252-112">Küme profilleri ayarlanmadıkça, küme malzeme çekme için bir mobil cihaz menü öğesi kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="b1252-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="b1252-113">Ortamınıza bağlı olarak, diğer ilgili yapılandırmaları da gözden geçirmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="b1252-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="b1252-114">Karma plaka alma işlemi, Alacak dışındaki herhangi bir değerlendirme kodu için çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b1252-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1252-115">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b1252-115">Issue description</span></span>

<span data-ttu-id="b1252-116">Değerlendirme kodunun **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlandığında , iade edilen maddeleri işlemek için yalnızca [Karma plaka alma işlemi](mixed-license-plate-receiving.md) menü öğesini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b1252-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1252-117">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b1252-117">Issue resolution</span></span>

<span data-ttu-id="b1252-118">Microsoft bu sorunu değerlendirmiş ve bir özellik sınırlaması olduğunu tespit etmiştir.</span><span class="sxs-lookup"><span data-stu-id="b1252-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="b1252-119">Şu anda, karma plaka alma işlemi için yalnızca **Eylem** alanı *Alacak* veya *Hurda* olarak ayarlanan [değerlendirme kodları](../service-management/set-up-disposition-codes.md) desteklenmektedir.</span><span class="sxs-lookup"><span data-stu-id="b1252-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="b1252-120">Ürün girişlerini güncelleştir periyodik görevini çalıştırdığımda, onaylanmamış satın alma siparişleri onaylanıyor.</span><span class="sxs-lookup"><span data-stu-id="b1252-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="b1252-121">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="b1252-121">Issue description</span></span>

<span data-ttu-id="b1252-122">*Ürün girişlerini güncelleştir* periyodik görevini çalıştırdıktan sonra, sistem, stok hareket durumu *Kayıtlı* olan onaylanmamış satın alma siparişlerini otomatik olarak onaylar.</span><span class="sxs-lookup"><span data-stu-id="b1252-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b1252-123">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="b1252-123">Issue resolution</span></span>

<span data-ttu-id="b1252-124">*Yük miktarlarını aşırı alma* adlı yeni bir özellikle bu sorunu düzeltilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b1252-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="b1252-125">Bu özelliği açmak için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ne gidin ve aşağıdaki özellikleri (listelendikleri sırada) açın:</span><span class="sxs-lookup"><span data-stu-id="b1252-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="b1252-126">Satınalma siparişi stok hareketlerini yükle ilişkilendir</span><span class="sxs-lookup"><span data-stu-id="b1252-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="b1252-127">Yük miktarlarının fazlasını alma</span><span class="sxs-lookup"><span data-stu-id="b1252-127">Over receipt of load quantities</span></span>

<span data-ttu-id="b1252-128">Daha fazla bilgi için bkz. [Kayıtlı ürün miktarlarını satınalma siparişlerine göre deftere nakletme](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="b1252-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]