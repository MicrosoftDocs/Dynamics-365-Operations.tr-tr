---
title: Kıymet hata analizi
description: Bu konuda Varlık Yönetimi'ndeki varlık hata analizinde açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectFaultCalculate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f4d7b4a92486287027cba79c43ca5933cce42a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253866"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="4ebd4-103">Kıymet hata analizi</span><span class="sxs-lookup"><span data-stu-id="4ebd4-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4ebd4-104">Belirli bir dönemde kaydedilen toplam hata sayısını genel olarak almak için, varlık yönetiminde varlık hata kayıtlarını analiz edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="4ebd4-105">Örneğin varlıklar, varlık türleri, işlevsel yerleşimler, hata belirtileri veya arıza tipleri üzerinde odak bulunan bir arıza kaydı farklı açılardan analiz edilebilir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="4ebd4-106">**Varlık Yönetimi** > **Sorgular** > **Varlık hatası** > **Varlık hata analizi**'ni tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="4ebd4-107">**Varlık arıza Analizi hesaplaması** iletişim kutusunda, kıymet arıza satırlarının işlevsel yerleşimleriyle ilgili olmasını istediğiniz ayrıntıları göstermek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="4ebd4-108">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm varlık arızası satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="4ebd4-109">**Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm varlık arızası satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="4ebd4-110">Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli kıymetleri, arıza tarihlerini, arıza nedenlerini ve arıza düzeltme 'leri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="4ebd4-111">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="4ebd4-112">**Varlık arıza analizi** sekmesinde, bir veya daha fazla **Gruplama ölçütü** düğmesine tıklayarak istediğiniz ayrıntı düzeyini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="4ebd4-113">Etkinleştirilen düğmeler vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="4ebd4-114">Düğmelere tıklayarak onları etkinleştirin veya devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="4ebd4-115">Seçimlerinizi ekranda göstermek için **Hesaplamaları Güncelleştir**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="4ebd4-116">**Gruplama ölçütü** düğmesini her etkinleştirdiğinizde veya devre dışı bıraktığınızda, **Hesaplamaları güncelleştir** düğmesine tıklamayı unutmayın.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="4ebd4-117">Hata olasılığını yeniden hesaplama sırasında büyük miktarda veri işlendiğinden, bu gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="4ebd4-118">Örnekler</span><span class="sxs-lookup"><span data-stu-id="4ebd4-118">Examples</span></span>

<span data-ttu-id="4ebd4-119">Arıza kayıtlarını çözümlemenin birçok yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="4ebd4-120">Bu bölümde, farklı veri seçimlerinin varlık arıza kayıtları analiz edilirken nasıl daha fazla öngörü sağlayabildiğini gösteren beş örnek bulunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="4ebd4-121">Belirtilere göre grupla</span><span class="sxs-lookup"><span data-stu-id="4ebd4-121">Group by symptoms</span></span>

<span data-ttu-id="4ebd4-122">Aşağıdaki ekran görüntüsünde yalnızca **Belirti** düğmesi seçilidir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="4ebd4-123">Hata kayıtları üç hata belirtiyle yapılmaktadır: "hava sızıntısı", "sigorta yanması" ve "donanım sıkıştı".</span><span class="sxs-lookup"><span data-stu-id="4ebd4-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="4ebd4-124">**Olasılık %** sütununda, tüm yüzdeler %100 kadar toplanır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="4ebd4-125">Olasılık bu arıza Analizi içindeki tüm **belirti** kayıtlarını temel alan bir olasılıktır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Şekil 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="4ebd4-127">Belirtilere ve döneme göre grupla</span><span class="sxs-lookup"><span data-stu-id="4ebd4-127">Group by symptoms and time period</span></span>

<span data-ttu-id="4ebd4-128">Aşağıdaki ekran görüntüsünde , seçili bir dönem içinde hata kayıtlarını nasıl kullanabileceğinizi göstermek için **yıl** ve **ay** eklenir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="4ebd4-129">Hata belirtileri şimdi her yıl/ay kaydı olarak gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="4ebd4-130">**Olasılık %** sütununda, her ay için tüm yüzdeleri eklerseniz, bu değerler %100'e kadar toplanır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="4ebd4-131">Olasılık bu arıza Analizi içindeki **belirti** kayıtlarını temel alan bir olasılıktır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="4ebd4-132">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata belirtisiyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata belirtinin göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Şekil 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="4ebd4-134">Birden çok belirtiye ve varlığa göre grupla</span><span class="sxs-lookup"><span data-stu-id="4ebd4-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="4ebd4-135">Aşağıdaki üç ekran görüntüsünde gösterilen hesaplamalarda temel olarak kıymet ve kıymet türü birleşimi ayrıntı düzeyinde kullanılmaktadır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="4ebd4-136">Genel olarak, **Tarihe göre grupla**, **Varlığa göre grupla**, **İşlem yapılacak yerleşime göre grupla** Eylem Bölmesi gruplarındaki düğmeler ve **Arıza** düğmesi (Hata Kodu), dönem veya varlık ilişkileri içerir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** Action Pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="4ebd4-137">**Belirti**, **Alan**, **Tür**, **Sebep** ve **Çözüm** düğmeleri, arıza yönetiminde kullanılan kategorizasyonlardır ve varlık arıza kayıtlarını analizde ve sorunlu alanları tespitte kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="4ebd4-138">**Belirtiye, varlığa ve varlık türüne göre grupla**</span><span class="sxs-lookup"><span data-stu-id="4ebd4-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="4ebd4-139">Aşağıdaki ekran görüntüsünde, arıza kayıtları ile ilgili daha ayrıntılı bilgi sağlamak amacıyla **varlık** ve **kıymet türü** eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="4ebd4-140">Hata belirtileri şimdi **Varlı** / **Varlık Türü** / **Belirti** kombinasyonlarına ayrılmıştır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="4ebd4-141">**Olasılık %** sütununda, **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="4ebd4-142">Olasılık bu arıza Analizi içindeki **belirti** kayıtlarını temel alan bir olasılıktır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="4ebd4-143">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata belirtisiyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata belirtinin göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Şekil 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="4ebd4-145">**İki belirtiye, varlığa ve varlık türüne göre grupla**</span><span class="sxs-lookup"><span data-stu-id="4ebd4-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="4ebd4-146">Aşağıdaki ekran görüntüsünde **Alan**, **Belirti**, **Varlık** ve **Varlık türü**'ne eklenerek hata kayıtları için daha fazla ayrıntı sağlar.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="4ebd4-147">**Olasılık %** sütununda, bir varlıktaki **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="4ebd4-148">Olasılık, bu hata analizindeki **Belirti** ve **Alan** kombinasyonuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="4ebd4-149">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata alanıyla ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata alanının göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Şekil 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="4ebd4-151">**Üç belirtiye, varlığa ve varlık türüne göre grupla**</span><span class="sxs-lookup"><span data-stu-id="4ebd4-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="4ebd4-152">Aşağıdaki ekran görüntüsünde **Tür** eklenmiştir ve bu örnekteki en ayrıntılı hesaplama gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="4ebd4-153">**Olasılık %** sütununda, bir varlıktaki **Varlık** / **Varlık türü** / **Belirti** için tüm yüzdeleri toplanırsanız, her biri %100'e ulaşır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="4ebd4-154">Olasılık, bu hata analizindeki **Belirti** ve **Alan** ve **Tür** kombinasyonuna dayanır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="4ebd4-155">Bir kıymette çok sayıda satır varsa, ancak bir satırda büyük bir yüzde değeri varsa, bu hata türüyle ilgili kayıt sayısını sınırlamak için bir yöntem bulmayı daha yakından incelemek amacıyla hata türünün göstergesi olacaktır.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Şekil 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="4ebd4-157">İş emirlerinde ve bakım taleplerinde oluşturulan tüm arıza kayıtlarının genel bakışı için **Varlık yönetimi** > **Sorgular** > **Varlık arızası** > **Varlık arızaları** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="4ebd4-158">**Varlık arızaları** sayfasında, bir varlık arızası kaydını seçin ve **İlgili bilgi** panosunu genişleterek ilgili iş emri veya bakım talebiyle ilgili bilgiyi görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4ebd4-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]