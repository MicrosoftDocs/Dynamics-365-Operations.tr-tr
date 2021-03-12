---
title: Maliyet öğesi boyutunu eşleştirme
description: Bir maliyet denetleyicisi bu yordamı bir maliyet öğesi boyutunu bir maliyet öğesi boyutuna MXMF tüzel kişiliğinde eşleştirmek için kullanabilir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5570d7cf2a8139d7959cb708d306e8b91065ed1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990679"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="d38ff-103">Maliyet öğesi boyutunu eşleştirme</span><span class="sxs-lookup"><span data-stu-id="d38ff-103">Map a cost element dimension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d38ff-104">Bir maliyet denetleyicisi bu yordamı bir maliyet öğesi boyutunu bir maliyet öğesi boyutuna MXMF tüzel kişiliğinde eşleştirmek için kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="d38ff-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="d38ff-105">Bu kayıt USP2 demo veri şirketini kullanır.</span><span class="sxs-lookup"><span data-stu-id="d38ff-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="d38ff-106">Maliyet muhasebesi > Boyutlar > Maliyet öğesi boyutları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="d38ff-107">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d38ff-108">Bu örnek için Maliyet öğeleri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="d38ff-109">Boyut eşlemeleri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d38ff-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="d38ff-110">Bu boyuttan yapılan eşlemeleri konfigüre et'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d38ff-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="d38ff-111">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d38ff-111">Click New.</span></span>
6. <span data-ttu-id="d38ff-112">Boyuta alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="d38ff-113">Bu örnek için MXMF Maliyet öğeleri'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="d38ff-114">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d38ff-114">Click New.</span></span>
8. <span data-ttu-id="d38ff-115">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d38ff-116">Gelen boyutu üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d38ff-117">Bu örnekte, 606400 Telefon ve Faks Gideri boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="d38ff-118">Boyuta üyesi alanına bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d38ff-119">Bu örnekte, 6001004 Telefono boyut üyesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d38ff-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="d38ff-120">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d38ff-120">Click Save.</span></span>

