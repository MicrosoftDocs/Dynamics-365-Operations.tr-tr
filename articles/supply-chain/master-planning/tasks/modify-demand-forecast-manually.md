---
title: 'Kılavuz: Talep tahminini el ile değiştirme'
description: Bu konuda, bir madde için tahminin nasıl değiştirileceği açıklanmaktadır
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224022"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="32fbe-103">Kılavuz: Talep tahminini el ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="32fbe-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="32fbe-104">Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="32fbe-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="32fbe-105">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="32fbe-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="32fbe-106">Seçili bir madde için tahmin değiştirme</span><span class="sxs-lookup"><span data-stu-id="32fbe-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="32fbe-107">Seçili bir madde için tahmini değiştirmek üzere:</span><span class="sxs-lookup"><span data-stu-id="32fbe-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="32fbe-108">**Modüller \> Ürün bilgileri yönetimi \> Ürünler \> Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="32fbe-109">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="32fbe-110">Tahminini değiştirmek istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="32fbe-111">Eylem Bölmesi'nde **Plan** sekmesini açın ve **Talep tahmini**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="32fbe-112">Listede bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-112">In the list, select a row.</span></span> <span data-ttu-id="32fbe-113">Tahmin satırı yoksa, Eylem Bölmesinde **Yeni**'ye tıklayarak yeni bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="32fbe-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="32fbe-114">**Satış miktarı** alanına pozitif bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="32fbe-115">Bu sayı, madde için tahmin edilmiş miktarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="32fbe-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="32fbe-116">Negatif bir sayı girerseniz hata gösterilir.</span><span class="sxs-lookup"><span data-stu-id="32fbe-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="32fbe-117">Diğer alanları gereken şekilde doldurun.</span><span class="sxs-lookup"><span data-stu-id="32fbe-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="32fbe-118">Eylem Bölmesinde **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="32fbe-119">Microsoft Excel ile bir veya daha fazla madde için tahmini değiştirme</span><span class="sxs-lookup"><span data-stu-id="32fbe-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="32fbe-120">Microsoft Excel ile bir veya daha fazla madde için tahmini değiştirmek için:</span><span class="sxs-lookup"><span data-stu-id="32fbe-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="32fbe-121">Aşağıdakilerden birini yapın:</span><span class="sxs-lookup"><span data-stu-id="32fbe-121">Do one of the following:</span></span>
    - <span data-ttu-id="32fbe-122">Önceki bölümde açıklandığı gibi herhangi bir madde için (hangisi olduğu önemli değildir) **Talep tahmini** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="32fbe-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="32fbe-123">**Master planlama \> Tahmin \> El ile tahmin girişi \> Talep tahmini satırları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="32fbe-124">Eylem Bölmesinde **Microsoft Office'te Aç \>Talep tahmini girişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="32fbe-125">Bir indirme konumu seçin, kaydedin ve indirilen dosyayı Excel'de açın.</span><span class="sxs-lookup"><span data-stu-id="32fbe-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="32fbe-126">Bir uyarı görürseniz **Düzenlemeyi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="32fbe-127">Excel'de, Microsoft Dynamics görev bölmesini kullanarak Supply Chain Management'ta oturum açın.</span><span class="sxs-lookup"><span data-stu-id="32fbe-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="32fbe-128">**Oturumumu açık tut** seçeneğini etkinleştirerek oturum açmanız ve veri bağlantısı uygulamasına güvenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="32fbe-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="32fbe-129">Excel elektronik tablosu artık şirketiniz için geçerli tüm talep tahmini satırlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32fbe-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="32fbe-130">Talep tahmin satırlarını gereken şekilde ekleyin, silin ve düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="32fbe-131">Değişikliklerinizi Supply Chain Management'a geri yüklemek için Microsoft Dynamics görev bölmesinde **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="32fbe-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
