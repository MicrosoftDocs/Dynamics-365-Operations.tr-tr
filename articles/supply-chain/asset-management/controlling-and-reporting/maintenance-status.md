---
title: Bakım durumu
description: Bu konuda Kıymet Yönetimi'nde bakım durumu hesaplama işlemi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43389db93032ec29adb805f86ae04a686803176f
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889589"
---
# <a name="maintenance-status"></a><span data-ttu-id="a97f2-103">Bakım durumu</span><span class="sxs-lookup"><span data-stu-id="a97f2-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a97f2-104">Varlık Yönetiminde belirli bir döneme ait yeni, etkin ve tamamlanmış bakım isteklerinin, iş emirlerinin ve bakım kesinti süresi faaliyetlerinin genel görünümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a97f2-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="a97f2-105">Aynı dönem için tamamlanan koşul değerlendirmelerinin sayısını da görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a97f2-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="a97f2-106">Gelen ve tamamlanan bakım istekleriyle ve iş siparişleriyle ilgili iş yükünün özetini almak için bu hesaplamayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="a97f2-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="a97f2-107">Bakım durumu hesaplaması yap</span><span class="sxs-lookup"><span data-stu-id="a97f2-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="a97f2-108">**Varlık Yönetimi** > **Sorgular** > **Bakım durumu**' nu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a97f2-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="a97f2-109">**Durumu hesapla** iletişim kutusunda, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına hesaplamayı yapmak istediğiniz zaman aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="a97f2-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="a97f2-110">İşlem yapılacak yerleşimlerle ilgili olarak bakım satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a97f2-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="a97f2-111">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki durum, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="a97f2-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="a97f2-112">**Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="a97f2-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="a97f2-113">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a97f2-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="a97f2-114">**Gruplandırma ölçütü** düğmelerine tıklayarak hesaplamanın gerekli ayrıntı düzeyini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="a97f2-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="a97f2-115">Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="a97f2-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="a97f2-116">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a97f2-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="a97f2-117">**Gruplandırma ölçütü** düğmelerini etkinleştirerek veya devre dışı bırakarak her değişiklik yaptığınızda hesaplamayı güncelleştirmek için **Güncelleştir** düğmesine basmayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a97f2-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="a97f2-118">Yeni bir bakım durumu hesaplaması oluşturmak istiyorsanız **durum**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="a97f2-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="a97f2-119">**Bakım durumunda** gösterilen sonuçlar yalnızca gerçek başlangıç tarihi ve saatine sahip bakım isteklerini ve çalışma emirlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="a97f2-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="a97f2-120">Bitiş tarihi ve saati boş olabilir.</span><span class="sxs-lookup"><span data-stu-id="a97f2-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="a97f2-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a97f2-121">Example 1</span></span>

<span data-ttu-id="a97f2-122">Aşağıdaki ekran görüntüsünde, **Yıl** ve **Ay** düğmeleri etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a97f2-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="a97f2-123">Bu **Gruplandırma ölçütü** seçenekleri seçili olduğunda, bakım istekleriyle ve iş emirleriyle ilgili iş yükü ve iş emirleri hakkında genel bakış elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a97f2-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Aylık iş yükü örneği](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="a97f2-125">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a97f2-125">Example 2</span></span>

<span data-ttu-id="a97f2-126">Aşağıdaki ekran görüntüsünde, işlem yapılacak yerleşim bilgileri eklendi.</span><span class="sxs-lookup"><span data-stu-id="a97f2-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="a97f2-127">Şimdi, coğrafi konumları, fabrikaları veya çalışma alanlarını temsil eden işlem yapılacak konumlar arasında iş yükü ve iş yükünü karşılaştırmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="a97f2-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![İşlem yapılacak yerleşimlere sahip aylık iş yükü örneği](media/14-controlling-and-reporting.png)

