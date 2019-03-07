---
title: Makine öğrenimi destekli ürün önerilerini yapılandırma
description: Bu yordam, ürün önerilerini destekleyen makine öğrenimi sistemi tarafından kullanılan Varlık deposundaki verileri yeniler ve POS istemcileri üzerinde ürün önerilerini etkinleştirir.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "348538"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="488a3-103">Makine öğrenimi destekli ürün önerilerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="488a3-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="488a3-104">Bu yordam, ürün önerilerini destekleyen makine öğrenimi sistemi tarafından kullanılan Varlık deposundaki verileri yeniler ve POS istemcileri üzerinde ürün önerilerini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="488a3-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="488a3-105">Bu yordam USRT demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="488a3-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="488a3-106">Sistem yönetimi > Kurulum > Varlık Deposu öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="488a3-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="488a3-107">Listede, 'RetailSales' kaydını bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="488a3-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="488a3-108">Yenile'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="488a3-108">Click Refresh.</span></span>
4. <span data-ttu-id="488a3-109">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="488a3-109">Click OK.</span></span>
5. <span data-ttu-id="488a3-110">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="488a3-110">Close the page.</span></span>
6. <span data-ttu-id="488a3-111">Perakende ve ticaret > Genel merkez kurulumu > Parametreler > Perakende parametreleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="488a3-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="488a3-112">Makine öğrenimi sekmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="488a3-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="488a3-113">Ürün önerilerini etkinleştir alanında 'Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="488a3-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="488a3-114">"Öneri modelleri alınamadı" iletisini alırsanız, bunun nedeni yakın zamanda Varlık Deposu'nu yenilemiş olmanız ve sistemin yeni verileri benzeştirmeyi tamamlamamış olmasıdır.</span><span class="sxs-lookup"><span data-stu-id="488a3-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="488a3-115">2-3 saat bekleyin ve yeniden deneyin.</span><span class="sxs-lookup"><span data-stu-id="488a3-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="488a3-116">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="488a3-116">Click Save.</span></span>
10. <span data-ttu-id="488a3-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="488a3-117">Close the page.</span></span>

