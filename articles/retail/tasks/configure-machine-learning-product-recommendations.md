--- 
title: " Makine öğrenimi destekli ürün önerilerini yapılandırma"
description: "Bu yordam, ürün önerilerini destekleyen makine öğrenimi sistemi tarafından kullanılan Varlık deposundaki verileri yeniler ve POS istemcileri üzerinde ürün önerilerini etkinleştirir."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: tr-tr
ms.lasthandoff: 08/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="c4ec7-103"> Makine öğrenimi destekli ürün önerilerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="c4ec7-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c4ec7-104">Bu yordam, ürün önerilerini destekleyen makine öğrenimi sistemi tarafından kullanılan Varlık deposundaki verileri yeniler ve POS istemcileri üzerinde ürün önerilerini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="c4ec7-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c4ec7-106">Sistem yönetimi > Kurulum > Varlık Deposu öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="c4ec7-107">Listede, 'RetailSales' kaydını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="c4ec7-108">Yenile'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-108">Click Refresh.</span></span>
4. <span data-ttu-id="c4ec7-109">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-109">Click OK.</span></span>
5. <span data-ttu-id="c4ec7-110">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-110">Close the page.</span></span>
6. <span data-ttu-id="c4ec7-111">Perakende ve ticaret > Genel merkez kurulumu > Parametreler > Perakende parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="c4ec7-112">Makine öğrenimi sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="c4ec7-113">Ürün önerilerini etkinleştir alanında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="c4ec7-114">"Öneri modelleri alınamadı" iletisini alırsanız, bunun nedeni yakın zamanda Varlık Deposu'nu yenilemiş olmanız ve sistemin yeni verileri benzeştirmeyi tamamlamamış olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="c4ec7-115">2-3 saat bekleyin ve yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="c4ec7-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-116">Click Save.</span></span>
10. <span data-ttu-id="c4ec7-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c4ec7-117">Close the page.</span></span>


