---
title: "Sabit kıymet toplu olarak güncelleştirme"
description: "Defterleri kullanıyorsanız, aynı defterlerin parçası olan kıymet grupları için amortisman yöntemlerini değiştirebilirsiniz."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3521
ms.assetid: 50207ffb-6b89-4fb9-92e9-928bc0729489
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b3fb55f1a51652299db8a31274b07f239fbaf28f
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-mass-update"></a><span data-ttu-id="cd084-103">Sabit kıymet toplu olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="cd084-103">Fixed asset mass update</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cd084-104">Defterleri kullanıyorsanız, aynı defterlerin parçası olan kıymet grupları için amortisman yöntemlerini değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd084-104">If you use books, you can change the depreciation conventions for groups of assets that are part of the same book.</span></span>

<span data-ttu-id="cd084-105">Örneğin, ABD'deyseniz ve kıymetlerinizin yüzde 40'ından fazlasını yılın dördüncü çeyreği sırasında hizmete soktuysanız, çeyrek ortası amortisman yöntemini kullanmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="cd084-105">For example, if you are in the United States, and you put more than 40 percent of your assets in service during the fourth quarter of the year, you must use the mid-quarter depreciation convention.</span></span> <span data-ttu-id="cd084-106">Yeni amortisman yöntemi gerektiren tüm kıymetleri değiştirmek için toplu güncelleştirme süresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd084-106">You can use the process for a mass update to change all assets that require the new depreciation convention.</span></span> 

<span data-ttu-id="cd084-107">Kıymetler için amortisman dönüştürmeyi güncelleştirdiğinizde, bu kıymetler için mevcut olan tüm amortisman hareketleri silersiniz.</span><span class="sxs-lookup"><span data-stu-id="cd084-107">When you update the depreciation convention for assets, you delete all depreciation transactions that exist for those assets.</span></span> <span data-ttu-id="cd084-108">Ayrıca amortisman ayarları için tüm hareketleri, ek amortisman için hareketleri ve bu varlıklar için olağandışı amortisman hareketlerini de silersiniz.</span><span class="sxs-lookup"><span data-stu-id="cd084-108">You also delete all transactions for depreciation adjustments, transactions for bonus depreciation, and transactions for extraordinary depreciation for those assets.</span></span> 

<span data-ttu-id="cd084-109">Zaten elden çıkarılmış kıymetlerin amortisman yöntemini güncelleştirmek için, mevcut elde çıkarma hareketlerini silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cd084-109">To update the depreciation convention for assets that have already been disposed of, you must first delete the existing disposal transactions.</span></span> <span data-ttu-id="cd084-110">Ayrıca, elden çıkarma süreci nedeniyle oluşturulan tüm hareketlerini de silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="cd084-110">You must also delete all transactions that were generated because of the disposal process.</span></span> 

<span data-ttu-id="cd084-111">Kıymetler için amortisman dönüştürmeyi güncelleştirdiğinizde her kıymet için amortismanı ve olağandışı amortismanı işleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd084-111">After you update the depreciation convention for assets, you can process depreciation and extraordinary depreciation for each asset.</span></span> <span data-ttu-id="cd084-112">Ayrıca, gerekirse el ile amortisman düzeltmeleri de yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cd084-112">You can also make manual depreciation adjustments, if any adjustments are required.</span></span>






