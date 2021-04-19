---
title: Bakım durumu
description: Bu konuda Kıymet Yönetimi'nde bakım durumu hesaplama işlemi açıklanmaktadır.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f3d6f86c5052c845c9c8aad1e4437f4196f78b50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808628"
---
# <a name="maintenance-status"></a><span data-ttu-id="5de8d-103">Bakım durumu</span><span class="sxs-lookup"><span data-stu-id="5de8d-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5de8d-104">Varlık Yönetiminde belirli bir döneme ait yeni, etkin ve tamamlanmış bakım isteklerinin, iş emirlerinin ve bakım kesinti süresi faaliyetlerinin genel görünümünü hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5de8d-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="5de8d-105">Aynı dönem için tamamlanan koşul değerlendirmelerinin sayısını da görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5de8d-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="5de8d-106">Gelen ve tamamlanan bakım istekleriyle ve iş siparişleriyle ilgili iş yükünün özetini almak için bu hesaplamayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="5de8d-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="5de8d-107">Bakım durumu hesaplaması yap</span><span class="sxs-lookup"><span data-stu-id="5de8d-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="5de8d-108">**Varlık Yönetimi** > **Sorgular** > **Bakım durumu**' nu tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5de8d-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="5de8d-109">**Durumu hesapla** iletişim kutusunda, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına hesaplamayı yapmak istediğiniz zaman aralığını girin.</span><span class="sxs-lookup"><span data-stu-id="5de8d-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="5de8d-110">İşlem yapılacak yerleşimlerle ilgili olarak bakım satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5de8d-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="5de8d-111">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki durum, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="5de8d-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="5de8d-112">**Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="5de8d-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="5de8d-113">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5de8d-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="5de8d-114">**Gruplandırma ölçütü** düğmelerine tıklayarak hesaplamanın gerekli ayrıntı düzeyini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="5de8d-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5de8d-115">Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="5de8d-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="5de8d-116">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="5de8d-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="5de8d-117">**Gruplandırma ölçütü** düğmelerini etkinleştirerek veya devre dışı bırakarak her değişiklik yaptığınızda hesaplamayı güncelleştirmek için **Güncelleştir** düğmesine basmayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="5de8d-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="5de8d-118">Yeni bir bakım durumu hesaplaması oluşturmak istiyorsanız **durum**'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="5de8d-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="5de8d-119">**Bakım durumunda** gösterilen sonuçlar yalnızca gerçek başlangıç tarihi ve saatine sahip bakım isteklerini ve çalışma emirlerini içerir.</span><span class="sxs-lookup"><span data-stu-id="5de8d-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="5de8d-120">Bitiş tarihi ve saati boş olabilir.</span><span class="sxs-lookup"><span data-stu-id="5de8d-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="5de8d-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5de8d-121">Example 1</span></span>

<span data-ttu-id="5de8d-122">Aşağıdaki ekran görüntüsünde, **Yıl** ve **Ay** düğmeleri etkinleştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="5de8d-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="5de8d-123">Bu **Gruplandırma ölçütü** seçenekleri seçili olduğunda, bakım istekleriyle ve iş emirleriyle ilgili iş yükü ve iş emirleri hakkında genel bakış elde edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5de8d-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Aylık iş yükü örneği](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="5de8d-125">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="5de8d-125">Example 2</span></span>

<span data-ttu-id="5de8d-126">Aşağıdaki ekran görüntüsünde, işlem yapılacak yerleşim bilgileri eklendi.</span><span class="sxs-lookup"><span data-stu-id="5de8d-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="5de8d-127">Şimdi, coğrafi konumları, fabrikaları veya çalışma alanlarını temsil eden işlem yapılacak konumlar arasında iş yükü ve iş yükünü karşılaştırmak mümkündür.</span><span class="sxs-lookup"><span data-stu-id="5de8d-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![İşlem yapılacak yerleşimlere sahip aylık iş yükü örneği](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]