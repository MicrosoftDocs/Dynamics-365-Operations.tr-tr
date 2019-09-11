---
title: Tüketim raporları oluşturma
description: Bu konuda Varlık Yönetimi'nde tüketim raporları oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
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
ms.openlocfilehash: 3d978f8b991211e477dd8f766fe67432d9d493d0
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913114"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="0a156-103">Tüketim raporları oluşturma</span><span class="sxs-lookup"><span data-stu-id="0a156-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="0a156-104">Varlık Yönetiminde iş emirleriyle ilgili tüketim kayıtları oluşturup deftere naklettiğinizde, tüketim ayrıntılarını görüntülemek için iki rapor kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="0a156-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="0a156-105">Varlık tüketim raporu</span><span class="sxs-lookup"><span data-stu-id="0a156-105">Asset consumption report</span></span>

<span data-ttu-id="0a156-106">İş emirleriyle ilgili tüketimi deftere naklettiğinizde, bir varlık tüketim raporu yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a156-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="0a156-107">Rapor saatleri, saat maliyetlerini, madde maliyetlerini ve varlıklarda nakledilen giderleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a156-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="0a156-108">**Varlık yönetimi** > **Raporlar** > **Varlıklar** > **Varlık tüketimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a156-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="0a156-109">**Varlık tüketimi** iletişim kutusunda, ilgili düğmelerde "Evet" seçeneğini belirleyerek **Göster** bölümünde bir işlem yapılacak yerleşim düzeyi ekleyerek görmek istediğiniz parametreleri ve ayrıntı düzeyini seçin.</span><span class="sxs-lookup"><span data-stu-id="0a156-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting "Yes" on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="0a156-110">İşlem yapılacak yerleşimlerle ilgili olarak varlık satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzeyler** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a156-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> <span data-ttu-id="0a156-111">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlıklar üst düzeyde gösterilir ve dolayısıyla bir satır alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="0a156-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="0a156-112">**Düzeyler** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm varlıkları gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="0a156-112">If you insert the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
    - <span data-ttu-id="0a156-113">Rapordaki her bir alt varlığın toplamlarını görmek için **Tüm alt kıymetlerin toplamı** düğmesinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="0a156-113">Select "Yes" on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="0a156-114">**Tarihler** bölümünde bir tarih aralığı seçin.</span><span class="sxs-lookup"><span data-stu-id="0a156-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="0a156-115">**Hedef** hızlı sekmesinde raporu ekranda görüntülemek, yazdırmak veya bir dosya veya e-posta olarak kaydetmek isteyip istemediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="0a156-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="0a156-116">Gerekirse, raporda görüntülenecek belirli varlıklar seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a156-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="0a156-117">**Dahil edilecek raporlar** hızlı sekmesinde, **Filtre**'ye tıklayıp rapora dahil etmek istediğiniz varlıkları ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0a156-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="0a156-118">Raporu oluşturmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a156-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="0a156-119">İş emri tüketim raporu</span><span class="sxs-lookup"><span data-stu-id="0a156-119">Work order consumption report</span></span>

<span data-ttu-id="0a156-120">İş emirleriyle ilgili tüketimi deftere naklettiğinizde, bir iş emri tüketim raporu yazdırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a156-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="0a156-121">Rapor saatleri, saat maliyetlerini, madde maliyetlerini ve iş emirlerinde nakledilen giderleri gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a156-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="0a156-122">**Varlık yönetimi** > **Raporlar** > **İş emirleri** > **İş emri tüketimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a156-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="0a156-123">**İş emri tüketimi** iletişim kutusunda, **Göster** bölümünde ilgili iki durumlu düğmelerde "Evet" seçeneğini belirleyerek rapora dahil etmek istediğiniz parametreleri seçin.</span><span class="sxs-lookup"><span data-stu-id="0a156-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting "Yes" on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="0a156-124">**Tarihler** bölümünde bir tarih aralığı seçin.</span><span class="sxs-lookup"><span data-stu-id="0a156-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="0a156-125">**Hedef** hızlı sekmesinde raporu ekranda görüntülemek, yazdırmak veya bir dosya veya e-posta olarak kaydetmek isteyip istemediğinizi seçin.</span><span class="sxs-lookup"><span data-stu-id="0a156-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="0a156-126">Gerekirse, raporda görüntülenecek belirli iş emirleri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a156-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="0a156-127">**Dahil edilecek raporlar** hızlı sekmesinde, **Filtre**'ye tıklayıp rapora dahil etmek istediğiniz iş emirlerini ekleyin.</span><span class="sxs-lookup"><span data-stu-id="0a156-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="0a156-128">Raporu oluşturmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="0a156-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="0a156-129">Ayrıca, daha fazla iş emri ayrıntısı içeren [iş emri raporu](../work-orders/work-order-report.md) da oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a156-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

