---
title: Kullanıldığı madde
description: Bu konu, bir öğenin Varlık Yönetimi içinde nerede kullanıldığını açıklar.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 476b01a4bae34a271203f34481ff18042783d4df
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811275"
---
# <a name="item-where-used"></a><span data-ttu-id="11013-103">Kullanıldığı madde</span><span class="sxs-lookup"><span data-stu-id="11013-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="11013-104">Maddenin kıymet yönetiminde nereye kullanıldığını genel olarak almak için belirli bir madde için hesaplama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11013-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="11013-105">Sonuçlar, ömrü boyunca öğenin kullanıldığı bağlamı gösterir.</span><span class="sxs-lookup"><span data-stu-id="11013-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="11013-106">**Maddenin kullanımı** sayfası ana Varlık Yönetimi menüsünden açılabildiği gibi, ayrıca aşağıdaki sayfalardan da erişilebilir:</span><span class="sxs-lookup"><span data-stu-id="11013-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="11013-107">Varlık Ürün Reçeteleri</span><span class="sxs-lookup"><span data-stu-id="11013-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="11013-108">Varlık türü varsayılanları üzerinde yedek parçalar</span><span class="sxs-lookup"><span data-stu-id="11013-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="11013-109">Bakım işi türü kategorileri ve bakım iş türleri, bakım iş türü çeşitleri, bakım işi işlemleri ve bakım denetim listeleri</span><span class="sxs-lookup"><span data-stu-id="11013-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="11013-110">Bakım tahmini</span><span class="sxs-lookup"><span data-stu-id="11013-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="11013-111">Tedarik</span><span class="sxs-lookup"><span data-stu-id="11013-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="11013-112">İş emri satınalma işlemi</span><span class="sxs-lookup"><span data-stu-id="11013-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="11013-113">Madde oluşturma-kullanım yeri hesaplaması</span><span class="sxs-lookup"><span data-stu-id="11013-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="11013-114">**Varlık yönetimi** > **Sorgular** > **Maddenin kullanıldığı** veya **Kullanıldığı yerde madde** düğmesini yukarıda bahsi geçen sayfaların birinde seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11013-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="11013-115">**Kullanılan madde** iletişim kutusunda, hesaplama yapmak istediğiniz maddeyi **Madde numarası** alanında seçin.</span><span class="sxs-lookup"><span data-stu-id="11013-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="11013-116">İşlem yapılacak yerleşimlerle ilgili olarak madde satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="11013-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="11013-117">Örneğin, alana "1" numarasını girerseniz ve çok düzeyli işlem yapılacak yerleşim yapısına sahipseniz, işlem yapılacak yerleşim için tüm madde satırları üst düzeyde gösterilir.</span><span class="sxs-lookup"><span data-stu-id="11013-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="11013-118">Bu nedenle, satırdaki ilişki/miktar, daha düşük bir düzeyde bulunan işlevsel konumlardan eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="11013-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="11013-119">**Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm madde satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="11013-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="11013-120">**Dahil et** bölümünde, hesaplamayı dahil etmek istediğiniz düğmelerde "Evet"i seçin.</span><span class="sxs-lookup"><span data-stu-id="11013-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="11013-121">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="11013-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="11013-122">**Madde kullanımı** sekmesinde gerekli hesaplama ayrıntı düzeyini göstermek için **Gruplama ölçütü** düğmelerini seçin.</span><span class="sxs-lookup"><span data-stu-id="11013-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="11013-123">Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="11013-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="11013-124">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="11013-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="11013-125">Maddeyle ilgili boyutları göstermek istiyorsanız, **boyutları görüntüle** üzerine tıklatın ve gösterilecek boyutları seçin.</span><span class="sxs-lookup"><span data-stu-id="11013-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="11013-126">Örnek</span><span class="sxs-lookup"><span data-stu-id="11013-126">Example</span></span>

<span data-ttu-id="11013-127">Aşağıdaki ekran görüntüsünde, "1000" numaralı madde için madde-kullanım yeri hesaplaması örneği görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="11013-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Madde kullanımı hesaplaması örneği](media/12-controlling-and-reporting.png)

