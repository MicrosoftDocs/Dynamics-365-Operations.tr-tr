---
title: Talep tahminini el ile değiştirme
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889036"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="8e431-103">Talep tahminini el ile değiştirme</span><span class="sxs-lookup"><span data-stu-id="8e431-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e431-104">Bu yordamda, bir madde için tahminin nasıl değiştirileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8e431-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="8e431-105">Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.</span><span class="sxs-lookup"><span data-stu-id="8e431-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8e431-106">Bu yordam için üretim planlayıcısına yöneliktir.</span><span class="sxs-lookup"><span data-stu-id="8e431-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="8e431-107">Seçili bir madde için tahmin değiştirme</span><span class="sxs-lookup"><span data-stu-id="8e431-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="8e431-108">Seçili bir madde için tahmini değiştirmek üzere:</span><span class="sxs-lookup"><span data-stu-id="8e431-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="8e431-109">**Modüller \> Ürün bilgileri yönetimi \> Ürünler \> Serbest bırakılan ürünler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="8e431-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="8e431-110">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="8e431-111">Tahminini değiştirmek istediğiniz maddeyi seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="8e431-112">Eylem Bölmesi'nde **Plan** sekmesini açın ve **Talep tahmini**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="8e431-113">Listede bir satır seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-113">In the list, select a row.</span></span> <span data-ttu-id="8e431-114">Tahmin satırı yoksa, Eylem Bölmesinde **Yeni**'ye tıklayarak yeni bir satır oluşturun.</span><span class="sxs-lookup"><span data-stu-id="8e431-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="8e431-115">**Satış miktarı** alanına pozitif bir sayı girin.</span><span class="sxs-lookup"><span data-stu-id="8e431-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="8e431-116">Bu sayı, madde için tahmin edilmiş miktarı temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8e431-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="8e431-117">Negatif bir sayı girerseniz hata gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8e431-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="8e431-118">Diğer alanları gereken şekilde doldurun.</span><span class="sxs-lookup"><span data-stu-id="8e431-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="8e431-119">Eylem Bölmesinde **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="8e431-120">Bir veya daha fazla madde için tahmini değiştirme Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="8e431-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="8e431-121">Bir veya daha fazla madde için tahmini değiştirmek üzere Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="8e431-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="8e431-122">Aşağıdakilerden birini yapın:</span><span class="sxs-lookup"><span data-stu-id="8e431-122">Do one of the following:</span></span>
    - <span data-ttu-id="8e431-123">Önceki bölümde açıklandığı gibi herhangi bir madde için (hangisi olduğu önemli değildir) **Talep tahmini** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="8e431-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="8e431-124">**Master planlama \> Tahmin \> El ile tahmin girişi \> Talep tahmini satırları**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="8e431-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="8e431-125">Eylem Bölmesinde **Microsoft Office'te Aç \>Talep tahmini girişleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="8e431-126">Bir indirme konumu seçin, kaydedin ve indirilen dosyayı Excel'de açın.</span><span class="sxs-lookup"><span data-stu-id="8e431-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="8e431-127">Bir uyarı görürseniz **Düzenlemeyi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="8e431-128">Excel'de, Microsoft Dynamics görev bölmesini kullanarak Supply Chain Management'ta oturum açın.</span><span class="sxs-lookup"><span data-stu-id="8e431-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="8e431-129">**Oturumumu açık tut** seçeneğini etkinleştirerek oturum açmanız ve veri bağlantısı uygulamasına güvenmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8e431-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="8e431-130">Excel elektronik tablosu artık şirketiniz için geçerli tüm talep tahmini satırlarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e431-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="8e431-131">Talep tahmin satırlarını gereken şekilde ekleyin, silin ve düzenleyin.</span><span class="sxs-lookup"><span data-stu-id="8e431-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="8e431-132">Değişikliklerinizi Supply Chain Management'a geri yüklemek için Microsoft Dynamics görev bölmesinde **Yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="8e431-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
