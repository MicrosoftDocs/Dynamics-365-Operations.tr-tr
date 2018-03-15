--- 
title: "Makine öğrenimi destekli ürün önerilerini yapılandırma"
description: "Bu yordam, ürün önerilerini destekleyen makine öğrenimi sistemi tarafından kullanılan Varlık deposundaki verileri yeniler ve POS istemcileri üzerinde ürün önerilerini etkinleştirir."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 277ffb879b80fe57deeaa2b52c1543baaf820274
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="4c31d-103">Makine öğrenimi destekli ürün önerilerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4c31d-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4c31d-104">Bu yordam, ürün önerilerini destekleyen makine öğrenimi sistemi tarafından kullanılan Varlık deposundaki verileri yeniler ve POS istemcileri üzerinde ürün önerilerini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="4c31d-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="4c31d-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="4c31d-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4c31d-106">Sistem yönetimi > Kurulum > Varlık Deposu öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="4c31d-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="4c31d-107">Listede, 'RetailSales' kaydını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="4c31d-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="4c31d-108">Yenile'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4c31d-108">Click Refresh.</span></span>
4. <span data-ttu-id="4c31d-109">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c31d-109">Click OK.</span></span>
5. <span data-ttu-id="4c31d-110">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4c31d-110">Close the page.</span></span>
6. <span data-ttu-id="4c31d-111">Perakende ve ticaret > Genel merkez kurulumu > Parametreler > Perakende parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="4c31d-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="4c31d-112">Makine öğrenimi sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c31d-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="4c31d-113">Ürün önerilerini etkinleştir alanında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4c31d-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="4c31d-114">"Öneri modelleri alınamadı" iletisini alırsanız, bunun nedeni yakın zamanda Varlık Deposu'nu yenilemiş olmanız ve sistemin yeni verileri benzeştirmeyi tamamlamamış olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="4c31d-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="4c31d-115">2-3 saat bekleyin ve yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="4c31d-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="4c31d-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4c31d-116">Click Save.</span></span>
10. <span data-ttu-id="4c31d-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="4c31d-117">Close the page.</span></span>


