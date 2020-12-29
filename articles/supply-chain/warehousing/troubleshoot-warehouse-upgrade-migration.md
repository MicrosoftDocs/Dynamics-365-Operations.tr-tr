---
title: Gelişmiş ambar yönetimine yükseltme ve geçiş ile ilgili sorunları giderme
description: Bu konuda, gelişmiş ambar yönetimine yükseltme ve geçiş sırasında karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmaktadır.
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
ms.openlocfilehash: d50c6d75ec7cc98109cf81c38ff42b4d2b105b0c
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645829"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="a239f-103">Gelişmiş ambar yönetimine yükseltme ve geçiş ile ilgili sorunları giderme</span><span class="sxs-lookup"><span data-stu-id="a239f-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a239f-104">Bu konuda, gelişmiş ambar yönetimine yükseltme ve geçiş sırasında karşılaşabileceğiniz genel sorunları nasıl giderebileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="a239f-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="a239f-105">Şu hata iletisini alıyorum: "java.security.cert.certPathValidatorException: Sertifika yolu için güven çıpası bulunamadı."</span><span class="sxs-lookup"><span data-stu-id="a239f-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a239f-106">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="a239f-106">Issue description</span></span>

<span data-ttu-id="a239f-107">Bu hata iletisini ambar uygulamasında alırsınız çünkü otomatik olarak imzalanan sertifikalara şirket içi ortamlarda Android 8+ sistemlerde güvenilmez.</span><span class="sxs-lookup"><span data-stu-id="a239f-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a239f-108">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="a239f-108">Issue resolution</span></span>

<span data-ttu-id="a239f-109">Harici (ortak) bir sertifika yetkilisi (CA) kullanın.</span><span class="sxs-lookup"><span data-stu-id="a239f-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="a239f-110">Bu sorunla ilgili düzeltme, ambar uygulamasının 1.9.0.0 sürümünde kullanıma sunulmuştur.</span><span class="sxs-lookup"><span data-stu-id="a239f-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="a239f-111">Bu sorun ve nasıl düzeltileceği hakkında daha fazla bilgi için bkz. [Ambar uygulaması bağlantı sorunlarını giderme](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a239f-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="a239f-112">Temel ambar işlemlerinden gelişmiş ambar işlemlerine geçiş için onaylı işlem nedir?</span><span class="sxs-lookup"><span data-stu-id="a239f-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="a239f-113">Sorun açıklaması</span><span class="sxs-lookup"><span data-stu-id="a239f-113">Issue description</span></span>

<span data-ttu-id="a239f-114">Şu anda envanter/stok yönetimi altında çalıştırıyor ve temel stok işlevlerini kullanıyorsunuz ve mobil cihazlardan, dalgalardan ve işlerden yararlanmak için Gelişmiş ambar işlemlerine geçmek istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="a239f-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="a239f-115">Ancak, bu taşımayı yapmaya çalıştığınızda sorunlarla karşılaşabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a239f-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="a239f-116">Örneğin, ürünleri depolama boyutları (tesis, ambar ve konum) kullanacak şekilde değiştiremezsiniz çünkü ürünlerin kendilerine karşı hareketler vardır.</span><span class="sxs-lookup"><span data-stu-id="a239f-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="a239f-117">Bu nedenle, temel ambar işlemlerinden gelişmiş ambar işlemlerine geçiş için onaylı işlemi öğrenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a239f-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a239f-118">Sorunun çözümü</span><span class="sxs-lookup"><span data-stu-id="a239f-118">Issue resolution</span></span>

<span data-ttu-id="a239f-119">Temel ambar işlemlerinden gelişmiş ambar işlemlerine geçiş hakkında daha fazla bilgi için aşağıdaki blog gönderilerine ve belgelere bakın:</span><span class="sxs-lookup"><span data-stu-id="a239f-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="a239f-120">Mevcut maddeler ve ambarlar için ambar yönetimi işlemini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="a239f-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="a239f-121">Microsoft Dynamics AX WMS'den yeni R3 ambar ve taşımacılık işlevine geçiş</span><span class="sxs-lookup"><span data-stu-id="a239f-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="a239f-122">WMSI/WMS2 madde geçişi</span><span class="sxs-lookup"><span data-stu-id="a239f-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="a239f-123">Ambar yönetimini Microsoft Dynamics AX 2012'den Supply Chain Management'a yükseltme</span><span class="sxs-lookup"><span data-stu-id="a239f-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
