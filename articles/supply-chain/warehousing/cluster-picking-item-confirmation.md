---
title: Küme çekme için ürün onayı
description: Bu konu, madde onaylamayı küme çekmeyle birlikte nasıl kuracağınızı açıklar.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d2ce787e6a7d677bc997bff363f34850ff9899b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568228"
---
[!include [banner](../includes/banner.md)]

# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="95761-103">Küme çekme için ürün onayı</span><span class="sxs-lookup"><span data-stu-id="95761-103">Product confirmation for cluster picking</span></span>
<span data-ttu-id="95761-104">Küme malzeme çekme, çok sayıda sipariş için tek seferde malzeme çekmenize olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="95761-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="95761-105">Küme malzeme çekme uygulandığında, öğe yapılandırması maddelerin kümelere eklendiğinden emin olmak için önemlidir.</span><span class="sxs-lookup"><span data-stu-id="95761-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="95761-106">Küme malzeme çekme işlemi sırasında küme malzeme çekme içerisindeki öğeleri doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="95761-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="95761-107">Uygulandığı yerler</span><span class="sxs-lookup"><span data-stu-id="95761-107">Where it applies</span></span>
<span data-ttu-id="95761-108">Küme malzeme çekme için madde doğrulaması, kümeli olmayan malzeme çekme işlemindeki doğrulamayla aynı şekilde çalışır.</span><span class="sxs-lookup"><span data-stu-id="95761-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="95761-109">Kurulum ürün barkod kurulumuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="95761-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="95761-110">Küme malzeme çekme ile madde doğrulamayı ayarlamak</span><span class="sxs-lookup"><span data-stu-id="95761-110">Set up item verification with cluster picking</span></span>
1.  <span data-ttu-id="95761-111">Mobil cihaz menü öğesinden iş onayı için kurulum formunu açın: **Ambar yönetimi** > **Ambar yönetimi** > **Kurulum** > **Mobil cihaz** > **Mobil cihaz menü öğeleri**.</span><span class="sxs-lookup"><span data-stu-id="95761-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
2.  <span data-ttu-id="95761-112">Mobil cihaz menü öğesinden **İş onayı ayarını** açın.</span><span class="sxs-lookup"><span data-stu-id="95761-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="95761-113">Seçenek</span><span class="sxs-lookup"><span data-stu-id="95761-113">Option</span></span>        |                                    <span data-ttu-id="95761-114">Açıklama</span><span class="sxs-lookup"><span data-stu-id="95761-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="95761-115">Ürün onayı</span><span class="sxs-lookup"><span data-stu-id="95761-115">Product confirmation</span></span> | <span data-ttu-id="95761-116">Tarandığında, her stok parçasını mobil cihazınızdan doğrulamanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="95761-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |

