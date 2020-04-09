---
title: Maliyet muhasebesi genel muhasebesi için veri kaynağını yönetme
description: Bir maliyet muhasebesi defteri için genel muhasebe defteri veri kaynağını yönetmek için bu yordamı kullanın.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cf53e905cf32557f4671477b173b1c5072d186e
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137833"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="bf732-103">Maliyet muhasebesi genel muhasebesi için veri kaynağını yönetme</span><span class="sxs-lookup"><span data-stu-id="bf732-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bf732-104">Bir maliyet muhasebesi defteri için genel muhasebe defteri veri kaynağını yönetmek için bu yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="bf732-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="bf732-105">Bu görevi tamamlamadan önce, "Bir maliyet muhasebesi defteri oluştur" ve "Maliyet kontrol birimleri tanımla" görev kılavuzlarını çalıştırdığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="bf732-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="bf732-106">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bf732-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="bf732-107">Maliyet muhasebesi > Genel muhasebe kurulumu > Maliyet muhasebesi defterleri öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="bf732-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="bf732-108">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bf732-109">Güncel sürümler üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf732-109">Click Actual versions.</span></span>
4. <span data-ttu-id="bf732-110">Eylem Bölmesinde, Yönet'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="bf732-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="bf732-111">Genel muhasebe üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf732-111">Click General ledger.</span></span>
6. <span data-ttu-id="bf732-112">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf732-112">Click New.</span></span>
7. <span data-ttu-id="bf732-113">İsim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="bf732-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="bf732-114">Veri sağlayıcı alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="bf732-115">Bu örnek için, Dynamics 365 Finance - Genel muhasebe defter girişleri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="bf732-116">Maliyet öğesi boyutu alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="bf732-117">Bu örnek için Maliyet öğeleri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="bf732-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf732-118">Click Save.</span></span>
11. <span data-ttu-id="bf732-119">Veri sağlayıcısını yapılandır üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf732-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="bf732-120">Yasal varlık alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="bf732-121">Bu örnek için, USP2 seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="bf732-122">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf732-122">Click New.</span></span>
14. <span data-ttu-id="bf732-123">Deftere nakil katmanı alanında, Geçerli öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bf732-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="bf732-124">Tamam'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="bf732-124">Click OK.</span></span>

