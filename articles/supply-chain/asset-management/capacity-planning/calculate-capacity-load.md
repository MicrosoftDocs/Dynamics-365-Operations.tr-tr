---
title: Kapasite yükünü hesapla
description: Bu konuda Varlık Yönetiminde kapasite yükünün nasıl hesaplandığını açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: da737cedfcd678a835e85a2b82a05394d771f8cc
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652276"
---
# <a name="calculate-capacity-load"></a><span data-ttu-id="1fb48-103">Kapasite yükünü hesaplama</span><span class="sxs-lookup"><span data-stu-id="1fb48-103">Calculate capacity load</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="1fb48-104">Varlık Yönetiminde, kapasite yükünü şunlar üzerinde hesaplayabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="1fb48-104">In Asset Management, you can calculate capacity load on:</span></span>

- <span data-ttu-id="1fb48-105">bakım zamanlaması satırları</span><span class="sxs-lookup"><span data-stu-id="1fb48-105">maintenance schedule lines</span></span>  
- <span data-ttu-id="1fb48-106">henüz zamanlanmamış olan iş emirleri</span><span class="sxs-lookup"><span data-stu-id="1fb48-106">work orders that have not yet been scheduled</span></span>  
- <span data-ttu-id="1fb48-107">planlanmış iş emirleri</span><span class="sxs-lookup"><span data-stu-id="1fb48-107">scheduled work orders</span></span>

<span data-ttu-id="1fb48-108">Bu, belirli bir döneme ait beklenen kapasite yükünün genel görünümünü almak istediğinizde yararlıdır.</span><span class="sxs-lookup"><span data-stu-id="1fb48-108">This is useful if you want to get an overview of expected capacity load for a specific period.</span></span> <span data-ttu-id="1fb48-109">Kapasite yükü hesaplanması tüm varlıklar veya seçilen varlıklar üzerinde yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="1fb48-109">Calculation of capacity load can be done on all assets or selected assets.</span></span> <span data-ttu-id="1fb48-110">Ayrıca, bakım kesinti süresi faaliyetleri veya iş emri havuzlarında da hesaplama yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fb48-110">You can also make a calculation on maintenance downtime activities or work order pools.</span></span>

1. <span data-ttu-id="1fb48-111">**Varlık yönetimi** > **Sorgular** > **Kapasite yükü** veya **Varlık yönetimi** > **Genel** > **İş emri havuzları** > **Tüm iş emri havuzları** / **Etkin iş emri havuzları** > listeden iş emri havuzu seçin > **Kapasite yükü** düğmesine veya **Varlık yönetimi** > **Genel** > **Bakım kesinti süresi faaliyetleri** > **Tüm bakım kesinti süresi faaliyetleri** / **Etkin bakımkesinti süresi faaliyetleri** > listeden bakım faaliyeti seçin > **Kapasite yükü** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1fb48-111">Click **Asset management** > **Inquiries** > **Capacity load**, or **Asset management** > **Common** > **Work order pools** > **All work order pools** / **Active work order pools** > select work order pool in the list > **Capacity load** button, or **Asset management** > **Common** > **Maintenance downtime activities** > **All maintenance downtime activities** / **Active maintenance downtime activities** > select maintenance activity in the list > **Capacity load** button.</span></span>

2. <span data-ttu-id="1fb48-112">**Kapasite yükünü hesapla** iletişim kutusunda, **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarında hesaplama için bir dönem seçin.</span><span class="sxs-lookup"><span data-stu-id="1fb48-112">In the **Calculate capacity load** dialog, select a period for the calculation in the **Start date/time** and **End date/time** fields.</span></span>

3. <span data-ttu-id="1fb48-113">Bakım zamanlaması satırlarını hesaplamaya dahil etmek istiyorsanız **Bakım zamanlamasını dahil et** düğmesini "Evet" seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="1fb48-113">Select "Yes" on the **Include maintenance schedule** toggle button if you want to include maintenance schedule lines in the calculation.</span></span>

4. <span data-ttu-id="1fb48-114">İş emri işlerini hesaplamaya dahil etmek istiyorsanız **İş emrini dahil et** düğmesini "Evet" seçeneğine getirin.</span><span class="sxs-lookup"><span data-stu-id="1fb48-114">Select "Yes" on the **Include work order** toggle button if you want to include work order jobs in the calculation.</span></span>

5. <span data-ttu-id="1fb48-115">İşlem yapılacak yerleşimlerle ilişkilendirmek istediğiniz kapasite yükü satırlarının ayrıntılarını göstermek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1fb48-115">You can use the **Level** field to indicate how detailed you want the capacity load lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="1fb48-116">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım zamanlaması satırlarıve iş emirleri üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="1fb48-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines and work orders for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="1fb48-117">**Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım zamanlaması satırlarını ve tüm iş emirlerini gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="1fb48-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines and all work orders on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="1fb48-118">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1fb48-118">Click **OK** to start the calculation.</span></span>

7. <span data-ttu-id="1fb48-119">**Gruplandırma ölçütü...** gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1fb48-119">In the **Group by...** groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="1fb48-120">Aşağıdaki ekran görüntüsünde, seçilen **Gruplama ölçütü** düğmeleri mavi renkle vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="1fb48-120">In the screenshot below, the selected **Group by** buttons are highlighted in blue color.</span></span> <span data-ttu-id="1fb48-121">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="1fb48-121">Click on a button to activate or deactivate it.</span></span>

    ![Şekil 1](media/01-capacity-planning.png)

>[!NOTE]
><span data-ttu-id="1fb48-123">Yalnızca planlanan iş emirleriyle ilgili kapasite planlamasına odaklanmak istiyorsanız bkz. [Planlanan iş emirlerinde kapasite yükünü hesaplama](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span><span class="sxs-lookup"><span data-stu-id="1fb48-123">If you want to focus only on capacity planning regarding scheduled work orders, see [Calculate capacity load on scheduled work orders](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).</span></span>

