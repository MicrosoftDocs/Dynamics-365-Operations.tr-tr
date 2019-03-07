---
title: Plaka kontrollü olmayan bir konuma tamamlandı olarak rapor etme (Uygulama, Mayıs 2016)
description: Bu görev kılavuzunda, plaka kontrollü olmayan bir konumuna tamamlandı olarak raporlama yapılmasına ilişkin bir örnek gösterilmiştir.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "344559"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="ff984-103">Plaka kontrollü olmayan bir konuma tamamlandı olarak rapor etme (Uygulama, Mayıs 2016)</span><span class="sxs-lookup"><span data-stu-id="ff984-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff984-104">Bu görev kılavuzunda, plaka kontrollü olmayan bir konumuna tamamlandı olarak raporlama yapılmasına ilişkin bir örnek gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ff984-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="ff984-105">Geçerli bir iş politikasının olması bu görev için bir ön koşuldur.</span><span class="sxs-lookup"><span data-stu-id="ff984-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="ff984-106">Önceki görev kılavuzunda iş politikasının kurulumu gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ff984-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="ff984-107">Bu görev kılavuzu Dynamics AX uygulama 7.0.1 veya sonrasını gerektirir.</span><span class="sxs-lookup"><span data-stu-id="ff984-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="ff984-108">Bir çıkış konumu ayarlama</span><span class="sxs-lookup"><span data-stu-id="ff984-108">Set up an output location</span></span>
1. <span data-ttu-id="ff984-109">Organizasyon yönetimi > Kaynaklar > Kaynak grupları öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ff984-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="ff984-110">Listeden '5102' kaynak grubunu seçin.</span><span class="sxs-lookup"><span data-stu-id="ff984-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="ff984-111">Düzenle'yi tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-111">Click Edit.</span></span>
4. <span data-ttu-id="ff984-112">Çıkış ambarı alanına '51' girin.</span><span class="sxs-lookup"><span data-stu-id="ff984-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="ff984-113">Çıkış konumu alanına '001' girin.</span><span class="sxs-lookup"><span data-stu-id="ff984-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="ff984-114">Konum 001, plaka kontrollü bir konum değildir.</span><span class="sxs-lookup"><span data-stu-id="ff984-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="ff984-115">Konum için geçerli bir çalışma politikası bulunuyorsa sadece, plaka dışı bir çıkış konumu ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff984-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="ff984-116">Bir üretim emri oluşturun ve bunu tamamlandı olarak rapor edin</span><span class="sxs-lookup"><span data-stu-id="ff984-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="ff984-117">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-117">Close the page.</span></span>
2. <span data-ttu-id="ff984-118">Üretim denetimi > Üretim emirleri > Tüm üretim emirleri'ne gidin.</span><span class="sxs-lookup"><span data-stu-id="ff984-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="ff984-119">Yeni üretim emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff984-119">Click New production order.</span></span>
4. <span data-ttu-id="ff984-120">Madde numarası alanına 'L0101' girin.</span><span class="sxs-lookup"><span data-stu-id="ff984-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="ff984-121">Oluştur öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff984-121">Click Create.</span></span>
6. <span data-ttu-id="ff984-122">Eylem Bölmesinde Üretime emri'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff984-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="ff984-123">Tahmin seçeneğine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff984-123">Click Estimate.</span></span>
8. <span data-ttu-id="ff984-124">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-124">Click OK.</span></span>
9. <span data-ttu-id="ff984-125">Başlat'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff984-125">Click Start.</span></span>
10. <span data-ttu-id="ff984-126">Genel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-126">Click the General tab.</span></span>
11. <span data-ttu-id="ff984-127">Otomatik malzeme listesi tüketimi alanında, 'Hiçbir zaman' seçin.</span><span class="sxs-lookup"><span data-stu-id="ff984-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="ff984-128">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-128">Click OK.</span></span>
13. <span data-ttu-id="ff984-129">Tamamlandı olarak bildir'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-129">Click Report as finished.</span></span>
14. <span data-ttu-id="ff984-130">Genel sekmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-130">Click the General tab.</span></span>
15. <span data-ttu-id="ff984-131">Kabul hatası alanında Evet'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ff984-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="ff984-132">Tamam'ı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="ff984-132">Click OK.</span></span>
17. <span data-ttu-id="ff984-133">Eylem Bölmesinde, Ambar öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff984-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="ff984-134">İş ayrıntıları öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="ff984-134">Click Work details.</span></span>
    * <span data-ttu-id="ff984-135">Üretim emri, tamamlandı olarak rapor edilmişse, hiçbir iş üretilmez.</span><span class="sxs-lookup"><span data-stu-id="ff984-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="ff984-136">Bu durum, Ürün L0101, konum 001'e bitirildi olarak rapor edildiğinde işin oluşturulmasının engellenmesi için tanımlanan bir iş politikası bulunmasından kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="ff984-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

