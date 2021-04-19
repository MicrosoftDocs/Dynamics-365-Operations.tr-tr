---
title: Madde tahminini hesapla
description: Bu konuda Varlık Yönetiminde madde tahmininin nasıl hesaplandığını açıklanmaktadır.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9392245abe5858b03b8324dcb471f5652aed7cd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813905"
---
# <a name="calculate-item-forecast"></a><span data-ttu-id="5dacc-103">Madde tahminini hesapla</span><span class="sxs-lookup"><span data-stu-id="5dacc-103">Calculate item forecast</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5dacc-104">Önceki bölümde anlatılan Kapasite yükü hesaplamaları yapabileceğiniz gibi, madde tahmini hesaplamaları da yapabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="5dacc-104">Just as you can make capacity load calculations, which are described in the previous section, you can also make item forecast calculations on:</span></span>

- <span data-ttu-id="5dacc-105">bakım zamanlaması satırları</span><span class="sxs-lookup"><span data-stu-id="5dacc-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="5dacc-106">henüz zamanlanmamış olan iş emirleri</span><span class="sxs-lookup"><span data-stu-id="5dacc-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="5dacc-107">planlanmış iş emirleri</span><span class="sxs-lookup"><span data-stu-id="5dacc-107">scheduled work orders</span></span>

<span data-ttu-id="5dacc-108">Bu, belirli bir döneme ait beklenen madde tüketiminin (iş emirlerini tamamlamak için gerekli diğer maddelerin yanı sıra yedek parçaların) genel görünümünü almak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="5dacc-108">This is useful if you want to get an overview of expected item consumption (spare parts as well as other items required for completing work orders) for a specific period.</span></span> <span data-ttu-id="5dacc-109">Madde tahmini hesaplaması tüm varlıklar veya seçilen varlıklar üzerinde yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="5dacc-109">Calculation of item forecast can be done on all assets or selected assets.</span></span> <span data-ttu-id="5dacc-110">Ayrıca bir bakım kesinti süresi faaliyetinde (**Tüm bakım kesinti süresi faaliyetleri** veya **Etkin bakım kesinti süresi faaliyetleri**) veya iş emri havuzunda (**Tüm iş emri havuzları** veya **Etkin iş emri havuzları**) da hesaplama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5dacc-110">You can also make a calculation on a maintenance downtime activity (**All maintenance downtime activities** or **Active maintenance downtime activities**), or on a work order pool (**All work order pools** or **Active work order pools**).</span></span>

1. <span data-ttu-id="5dacc-111">**Varlık yönetimi** > **Sorgular** > **Madde tahmini** veya **Varlık yönetimi** > **Genel** > **İş emri havuzları** > **Tüm iş emri havuzları** / **Etkin iş emri havuzları** > listeden iş emri havuzu seçin > **Madde tahmini** düğmesine veya **Varlık yönetimi** > **Genel** > **Bakım kesinti süresi faaliyetleri** > **Tüm bakım kesinti süresi faaliyetleri** / **Etkin bakım kesinti süresi faaliyetleri** > listeden bakım kesinti süresi faaliyeti seçin > **Madde tahmini** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dacc-111">Click **Asset management** > **Inquiries** > **Item forecast**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Item forecast** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance downtime activity in the list > **Item forecast** button.</span></span>

2. <span data-ttu-id="5dacc-112">**Madde tahminini hesapla** iletişim kutusunda, **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarında hesaplama için bir dönem seçin.</span><span class="sxs-lookup"><span data-stu-id="5dacc-112">In the **Calculate item forecast** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="5dacc-113">Bakım zamanlaması satırlarını tahmin hesaplamasına dahil etmek istiyorsanız **Bakım zamanlamasını dahil et** düğmesini "Evet" seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="5dacc-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the forecast calculation.</span></span>

4. <span data-ttu-id="5dacc-114">İş emri işlerini tahmin hesaplamasına dahil etmek istiyorsanız **İş emrini dahil et** düğmesini "Evet" seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="5dacc-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the forecast calculation.</span></span>

5. <span data-ttu-id="5dacc-115">İşlem yapılacak yerleşimlerle ilişkilendirmek istediğiniz madde tahmini satırlarının ayrıntılarını göstermek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5dacc-115">You can use the **Level** field to indicate how detailed you want the item forecast lines to be regarding functional locations.</span></span> 

      <span data-ttu-id="5dacc-116">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım zamanlaması satırlarıve iş emirleri üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="5dacc-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
  
      <span data-ttu-id="5dacc-117">**Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm bakım zamanlaması satırlarını ve tüm iş emirlerini gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="5dacc-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="5dacc-118">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dacc-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="5dacc-119">**Gruplandırma ölçütü...** gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dacc-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5dacc-120">Aşağıdaki ekran görüntüsünde, seçilen **Gruplama ölçütü** düğmeleri mavi renkle vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="5dacc-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="5dacc-121">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dacc-121">Click on a button to activate or deactivate it.</span></span>

8. <span data-ttu-id="5dacc-122">Maddelerle ilgili ürün, depolama alanı veya izleme boyutlarını görmek istiyorsanız, **Boyutları görüntüle** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dacc-122">Click the **Display dimensions** button if you want to see the product, storage, or tracking dimensions related to the items.</span></span> <span data-ttu-id="5dacc-123">İlgili onay kutularını seçin ve **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5dacc-123">Select the relevant check boxes, and click **OK**.</span></span>

![Şekil 1](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]