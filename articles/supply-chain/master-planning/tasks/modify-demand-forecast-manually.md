---
title: Talep tahminini el ile değiştirme
description: Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.
author: ShylaThompson
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 518a49441a9d73d9da5ab90400e0b7482692d374
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829678"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="5ed8f-103">Talep tahminini el ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="5ed8f-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ed8f-104">Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="5ed8f-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5ed8f-106">Bu kayıt için üretim planlayıcısı içindir.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="5ed8f-107">Bir madde için tahmin değiştirme</span><span class="sxs-lookup"><span data-stu-id="5ed8f-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="5ed8f-108">**Gezinti panosunda** **Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="5ed8f-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="5ed8f-110">Tahminini değiştirmek istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="5ed8f-111">Örneğin, madde D0001'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="5ed8f-112">**Eylem Bölmesi**'nde **Plan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="5ed8f-113">**Talep tahmini** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="5ed8f-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-114">In the list, mark the selected row.</span></span> <span data-ttu-id="5ed8f-115">Eğer hiçbir tahmin satırı yoksa, uygulama çubuğunda Yeni'yi tıklatarak yeni bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="5ed8f-116">**Satış miktarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="5ed8f-117">Bu sayı, madde için tahmin edilmiş miktarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="5ed8f-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="5ed8f-119">Tahmini Excel'de değiştirin</span><span class="sxs-lookup"><span data-stu-id="5ed8f-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="5ed8f-120">Microsoft Office içinde **Aç** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="5ed8f-121">**Tahmin talebini düzenle**'yi Excel'de tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="5ed8f-122">Excel'de talep tahmin satırlarını ekleyebilir, silebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="5ed8f-123">Excel'deki verileri göremiyorsanız "Oturumumu açık tut" seçeneği etkin olarak oturum açmanız ve veri bağlantısı uygulamasına güvenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]