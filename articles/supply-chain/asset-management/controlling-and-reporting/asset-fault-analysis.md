---
title: Kıymet hata analizi
description: Bu konuda Varlık Yönetimi'ndeki varlık hata analizinde açıklanmaktadır.
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
ms.openlocfilehash: 7c9330cc7b3a8839d94c8945418548033254786b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918453"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="7145b-103">Kıymet hata analizi</span><span class="sxs-lookup"><span data-stu-id="7145b-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7145b-104">Belirli bir dönemde kaydedilen toplam hata sayısını genel olarak almak için, varlık yönetiminde varlık hata kayıtlarını analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7145b-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="7145b-105">Örneğin varlıklar, varlık türleri, işlevsel yerleşimler, hata belirtileri veya arıza tipleri üzerinde odak bulunan bir arıza kaydı farklı açılardan analiz edilebilir.</span><span class="sxs-lookup"><span data-stu-id="7145b-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="7145b-106">**Varlık Yönetimi** > **Sorgular** > **Varlık hatası** > **Varlık hata analizi**'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7145b-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="7145b-107">**Varlık arıza Analizi hesaplaması** iletişim kutusunda, kıymet arıza satırlarının işlevsel yerleşimleriyle ilgili olmasını istediğiniz ayrıntıları göstermek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7145b-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> <span data-ttu-id="7145b-108">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlık arızası satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="7145b-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="7145b-109">**Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm varlık arızası satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="7145b-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="7145b-110">Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli kıymetleri, arıza tarihlerini, arıza nedenlerini ve arıza düzeltme 'leri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7145b-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="7145b-111">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7145b-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="7145b-112">**Kıymet arıza Analizi** sekmesinde, **gruplama ölçütü...** öğesini kullanarak Grup tarafından bir veya daha fazla düğmeyi tıklatın, görmek istediğiniz ayrıntı düzeyini görüntülemek için eylem bölmesi grupları.</span><span class="sxs-lookup"><span data-stu-id="7145b-112">On the **Asset fault analysis** tab, click one or more buttons in the **Group by...** action pane groups to display the detail level you want to see.</span></span> <span data-ttu-id="7145b-113">Etkinleştirilen düğmeler vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="7145b-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="7145b-114">Düğmelere tıklayarak onları etkinleştirin veya devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="7145b-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="7145b-115">Seçimlerinizi ekranda göstermek için **Hesaplamaları Güncelleştir**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="7145b-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="7145b-116">**Gruplandırma ölçütü...** öğesini kullanarak gruptaki düğmeleri her etkinleştirmenizde veya devre dışı bırakmanızda, eylem bölmesi grupları, seçimleri değiştirdikten sonra, **hesaplamaları Güncelleştir**düğmesini tıklatmayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="7145b-116">Every time you activate or deactivate buttons in the **Group by...** action pane groups, remember to click the **Update calculations** button after you changed the selections.</span></span> <span data-ttu-id="7145b-117">Hata olasılığını yeniden hesaplama sırasında büyük miktarda veri işlendiğinden, bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7145b-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

<span data-ttu-id="7145b-118">Arıza kayıtlarını çözümlemenin birçok yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="7145b-118">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="7145b-119">Aşağıda, farklı veri seçimlerinin farklı bilgi parçalarını nasıl sağlayacağınıza ilişkin beş ekran görüntüsü örnekleri görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7145b-119">Below you see examples in five screenshots of how different data selections provide different pieces of information.</span></span> <span data-ttu-id="7145b-120">Farklı seçimlerin, kıymet arıza kayıtları çözümlenirken nasıl daha ayrıntılı olduğunu göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="7145b-120">You will see how different selections provide more insight and detail when analyzing asset fault registrations.</span></span>

<span data-ttu-id="7145b-121">Aşağıdaki ekran görüntüsünde yalnızca **Belirti** düğmesi seçilidir.</span><span class="sxs-lookup"><span data-stu-id="7145b-121">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="7145b-122">Hata kayıtları üç hata belirtiyle yapılmaktadır: "hava sızıntısı", "sigorta yanması" ve "donanım sıkıştı".</span><span class="sxs-lookup"><span data-stu-id="7145b-122">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="7145b-123">**Olasılık %** sütununda, tüm yüzdeler %100 kadar toplanır.</span><span class="sxs-lookup"><span data-stu-id="7145b-123">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="7145b-124">Olasılık bu arıza Analizi içindeki tüm **belirti** kayıtlarını temel alan bir olasılıktır.</span><span class="sxs-lookup"><span data-stu-id="7145b-124">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Şekil 1](media/06-controlling-and-reporting.png)


<span data-ttu-id="7145b-126">Aşağıdaki ekran görüntüsünde , seçili bir dönem içinde hata kayıtlarını nasıl kullanabileceğinizi göstermek için **yıl** ve **ay** eklenir.</span><span class="sxs-lookup"><span data-stu-id="7145b-126">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="7145b-127">Hata belirtileri şimdi her yıl/ay kaydı olarak gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="7145b-127">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="7145b-128">**Olasılık %** sütununda, her ay için tüm yüzdeleri eklerseniz, bu değerler %100'e kadar toplanır.</span><span class="sxs-lookup"><span data-stu-id="7145b-128">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="7145b-129">Olasılık bu arıza Analizi içindeki **belirti** kayıtlarını temel alan bir olasılıktır.</span><span class="sxs-lookup"><span data-stu-id="7145b-129">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="7145b-130">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata belirtisiyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata belirtinin göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7145b-130">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Şekil 2](media/07-controlling-and-reporting.png)


- <span data-ttu-id="7145b-132">Aşağıdaki üç ekran görüntüsünde gösterilen hesaplamalarda temel olarak kıymet ve kıymet türü birleşimi ayrıntı düzeyinde kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="7145b-132">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  
- <span data-ttu-id="7145b-133">Genel olarak, **tarihegöre grupla**, **kıymete göre grupla**, **işlevsel konum eylem bölmesi gruplarına göre gruplandırma** ve **arıza** düğmesi (hata kodu), dönem veya sabit kıymet ilişkileri içerir.</span><span class="sxs-lookup"><span data-stu-id="7145b-133">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="7145b-134">**Belirti**, **Alan**, **Tür**, **Sebep** ve **Çözüm** düğmeleri, arıza yönetiminde kullanılan kategorizasyonlardır ve varlık arıza kayıtlarını analizde ve sorunlu alanları tespitte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7145b-134">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="7145b-135">Aşağıdaki ekran görüntüsünde, arıza kayıtları ile ilgili daha ayrıntılı bilgi sağlamak amacıyla **varlık** ve **kıymet türü** eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="7145b-135">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="7145b-136">Hata belirtileri şimdi **Varlı** / **Varlık Türü** / **Belirti** kombinasyonlarına ayrılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7145b-136">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="7145b-137">**Olasılık %** sütununda, **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır.</span><span class="sxs-lookup"><span data-stu-id="7145b-137">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="7145b-138">Olasılık bu arıza Analizi içindeki **belirti** kayıtlarını temel alan bir olasılıktır.</span><span class="sxs-lookup"><span data-stu-id="7145b-138">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="7145b-139">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata belirtisiyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata belirtinin göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7145b-139">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Şekil 3](media/08-controlling-and-reporting.png)


<span data-ttu-id="7145b-141">Aşağıdaki ekran görüntüsünde **Alan**, **Belirti**, **Varlık** ve **Varlık türü**'ne eklenerek hata kayıtları için daha fazla ayrıntı sağlar.</span><span class="sxs-lookup"><span data-stu-id="7145b-141">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="7145b-142">**Olasılık %** sütununda, bir varlıktaki **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır.</span><span class="sxs-lookup"><span data-stu-id="7145b-142">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="7145b-143">Olasılık, bu hata analizindeki **Belirti** ve **Alan** kombinasyonuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="7145b-143">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="7145b-144">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata alanıyla ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata alanının göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7145b-144">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Şekil 4](media/09-controlling-and-reporting.png)


<span data-ttu-id="7145b-146">Aşağıdaki ekran görüntüsünde **Tür** eklenmiştir ve bu örnekteki en ayrıntılı hesaplama gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7145b-146">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="7145b-147">**Olasılık %** sütununda, bir varlıktaki **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır.</span><span class="sxs-lookup"><span data-stu-id="7145b-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="7145b-148">Olasılık, bu hata analizindeki **Belirti** ve **Alan** ve **Tür** kombinasyonuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="7145b-148">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="7145b-149">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata türüyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata türünün göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7145b-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Şekil 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="7145b-151">İş emirlerinde ve bakım taleplerinde oluşturulan tüm arıza kayıtlarının genel bakışı için **Varlık yönetimi** > **Sorgular** > **Varlık arızası** > **Varlık arızaları** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7145b-151">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="7145b-152">**Varlık arızaları** sayfasında, bir varlık arızası kaydını seçin ve **İlgili bilgi** panosunu genişleterek ilgili iş emri veya bakım talebiyle ilgili bilgiyi görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="7145b-152">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

