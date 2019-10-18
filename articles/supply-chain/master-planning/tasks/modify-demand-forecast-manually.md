---
title: Talep tahminini el ile değiştirme
description: Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec51c1a500b5c9ff2c363cfb69cc1d404e939df9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250657"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="3e2f5-103">Talep tahminini el ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="3e2f5-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3e2f5-104">Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="3e2f5-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3e2f5-106">Bu kayıt için üretim planlayıcısı içindir.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="3e2f5-107">Bir madde için tahmin değiştirme</span><span class="sxs-lookup"><span data-stu-id="3e2f5-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="3e2f5-108">**Gezinti panosunda** **Modüller > Ürün bilgileri yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="3e2f5-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="3e2f5-110">Tahminini değiştirmek istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="3e2f5-111">Örneğin, madde D0001'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="3e2f5-112">**Eylem Bölmesi**'nde **Plan**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="3e2f5-113">**Talep tahmini** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="3e2f5-114">Listede, seçili satırı işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-114">In the list, mark the selected row.</span></span> <span data-ttu-id="3e2f5-115">Eğer hiçbir tahmin satırı yoksa, uygulama çubuğunda Yeni'yi tıklatarak yeni bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="3e2f5-116">**Satış miktarı** alanına bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="3e2f5-117">Bu sayı, madde için tahmin edilmiş miktarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="3e2f5-118">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="3e2f5-119">Tahmini Excel'de değiştirin</span><span class="sxs-lookup"><span data-stu-id="3e2f5-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="3e2f5-120">Microsoft Office içinde **Aç** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="3e2f5-121">**Tahmin talebini düzenle**'yi Excel'de tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="3e2f5-122">Excel'de talep tahmin satırlarını ekleyebilir, silebilir ve düzenleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="3e2f5-123">Excel'deki verileri göremiyorsanız "Oturumumu açık tut" seçeneği etkin olarak oturum açmanız ve veri bağlantısı uygulamasına güvenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="3e2f5-123">If you are not able to see the data in Excel, you need to sign in with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

