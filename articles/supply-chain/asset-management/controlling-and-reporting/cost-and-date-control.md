---
title: Maliyet ve tarih kontrolü
description: Bu konuda Varlık Yönetimi'nde maliyeti ve tarih denetimini açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 18373ff16b63ea61a3a4bc38ee7fa0b5e33154b5
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889685"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="4f0df-103">Maliyet ve tarih kontrolü</span><span class="sxs-lookup"><span data-stu-id="4f0df-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4f0df-104">Kıymet yönetiminde, sabit kıymetler, işlevsel yerleşimler ve iş emirleriyle ilgili bütçe maliyetleriyle karşılaştırıldığında fiili maliyetlerin genel görünümünü elde etmek için maliyetleri hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f0df-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="4f0df-105">Fiili maliyetler deftere nakledilen hareketleri temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="4f0df-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="4f0df-106">Ayrıca, planlanan başlangıç ve bitiş tarihlerini çalışma emirlerindeki gerçek başlangıç ve bitiş tarihleriyle karşılaştırmak istiyorsanız, tarih hesaplaması da yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f0df-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="4f0df-107">Kıymetler, işlevsel yerleşimler ve iş emirleri için maliyet kontrolü</span><span class="sxs-lookup"><span data-stu-id="4f0df-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="4f0df-108">Varlıklar, işlevsel yerleşimler ve çalışma emirleri için oluşturulan hesaplamalar neredeyse aynıdır.</span><span class="sxs-lookup"><span data-stu-id="4f0df-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="4f0df-109">Tek fark, varlıklar ve işlem yapılacak konumlar için alt varlıkları ve alt konumları da hesaplamanıza dahil edebiliyor olmanızdır.</span><span class="sxs-lookup"><span data-stu-id="4f0df-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="4f0df-110">Tarih, kayıt kaydedildiği hareket tarihidir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="4f0df-111">**Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık maliyet denetimi** veya **İşlem yapılacak yerleşim maliyet denetimi** veya **Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri maliyet denetimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="4f0df-112">**Varlık maliyet denetimi** / **İşlem yapılacak yerleşim maliyet denetimi** / **İş emri maliyet denetimi** iletişim kutusunda, hesaplanacak bir zaman aralığı seçin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="4f0df-113">Gerekirse, hesaplamaya dahil edilecek bir mali boyut kümesi seçin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="4f0df-114">Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="4f0df-115">İşlem yapılacak yerleşimlerle ilgili olarak maliyet denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f0df-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="4f0df-116">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim hiyerarşiniz varsa, işlem yapılacak yerleşim için tüm maliyet denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="4f0df-117">**Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm maliyet denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="4f0df-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="4f0df-118">Bu sütunu hesaplamaya dahil etmek istiyorsanız **Açık taahhüt edilen maliyeti göster** değiştir düğmesini göster üzerinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="4f0df-119">Alt kıymetlerle ilgili maliyetleri ayrı satırlar olarak göstermek için **alt kıymetleri dahil et** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="4f0df-120">Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli varlıkları / işlem yapılacak yerleşimleri / iş emirlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4f0df-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="4f0df-121">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="4f0df-122">Aşağıdaki şekil, **Varlık maliyet denetimi** iletişim kutusunun bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Varlık Maliyet Denetimi iletişim kutusu](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="4f0df-124">**Varlık maliyet denetimi** sayfasında, hesaplamanın gerekli ayrıntı düzeyini göstermek için **Gruplama ölçütü** düğmelerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="4f0df-125">Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="4f0df-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="4f0df-126">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="4f0df-127">Örnek</span><span class="sxs-lookup"><span data-stu-id="4f0df-127">Example</span></span>

<span data-ttu-id="4f0df-128">Aşağıdaki ekran görüntüsü, **Varlık maliyet denetimi** içinde hesaplama sonuçlarının bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="4f0df-129">**Orijinal bütçe** alanı, bütçe maliyetlerini iş emri tahmininden gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="4f0df-130">**Taahhüt edilen maliyet** alanı, tüzel kişiliğin kendisi ödemek üzere taahhüt ettiği giderlerin tutarın toplamını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="4f0df-131">**Açık taahhüt edilen maliyet** alanı, sipariş ettiğiniz veya aldığınız, ancak henüz ödenmemiş olan maddeler, saatler ve servisler için ödeme taahhütlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="4f0df-132">Tüm tüketim kayıtları deftere nakledildikten sonra, ilgili maliyetler **Fiili maliyet** alanında gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Varlık maliyet denetiminde örnek hesaplama sonuçları](media/02-controlling-and-reporting.png)

<span data-ttu-id="4f0df-134">Maliyet hesaplaması yapmanın bir başka yolu **Tüm varlıklar** veya **Etkin varlıklar** içinde çoklu varlıkları seçmektir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="4f0df-135">Daha sonra, **genel** sekmesindeki **maliyet denetimi** düğmesini tıklatın. **Varlık maliyet denetimi** iletişim kutusunda, seçilen kıymetler hızlı sekme **dahil edilecek kayıtlar** içindeki **Varlık** alanına otomatik eklenir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="4f0df-136">**Tamam**'ı tıklattın ve seçilen varlıklar için bir maliyet hesaplaması gösterilir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="4f0df-137">Aynı işlem **Tüm işlem yapılacak yerleşimler** veya **Etkin işlem yapılacak yerleşimler** içindeki işlem yapılacak yerleşimler ve **Tüm iş emirleri** veya **Etkin iş emirleri** içindeki tüm iş emirleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="4f0df-138">İş emri tarih denetimi</span><span class="sxs-lookup"><span data-stu-id="4f0df-138">Work order date control</span></span>

<span data-ttu-id="4f0df-139">İş emirlerindeki gerçek başlangıç ve bitiş tarihleriyle karşılaştırıldığında, beklenen başlangıç ve bitiş tarihlerinin özetini almak için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="4f0df-140">**Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri tarih denetimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="4f0df-141">**Hesapla** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="4f0df-142">**İşlem yapılacak yerleşim** alanında bir işlem yapılacak yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="4f0df-143">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarında hesaplamayı yapmak istediğiniz aralığı girin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="4f0df-144">Başlama tarihi aralık içinde olan tüm iş emirleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="4f0df-145">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-145">Click **OK**.</span></span>

6. <span data-ttu-id="4f0df-146">**Gruplandırma ölçütü** düğmelerine tıklayarak hesaplamanın gerekli ayrıntı düzeyini görüntüleyin.</span><span class="sxs-lookup"><span data-stu-id="4f0df-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="4f0df-147">Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="4f0df-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="4f0df-148">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="4f0df-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="4f0df-149">Örnek</span><span class="sxs-lookup"><span data-stu-id="4f0df-149">Example</span></span>

<span data-ttu-id="4f0df-150">Aşağıdaki ekran görüntüsü, **İş emri tarih denetimi** içinde hesaplama sonuçlarının bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="4f0df-151">**Ortalama başlangıç gecikmesi** alanı, fiili başlangıç tarihiyle karşılaştırıldığında bir iş emri için planlanan başlangıç tarihi arasındaki farkı gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="4f0df-152">Örneğin, gerçek başlangıç tarihi planlanan başlangıç tarihinden iki gün önce ise, bu alanda "-2" görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="4f0df-153">**Ortalama bitiş gecikmesi** alanı, fiili bitiş tarihiyle karşılaştırıldığında bir iş emri için planlanan bitiş tarihi arasındaki farkı gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="4f0df-154">Örneğin, gerçek bitiş tarihi planlanan bitiş tarihinden üç gün sonra ise, bu alanda "3" görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="4f0df-155">**Oluşum** alanları, planlanan ve fiili başlangıç tarihiyle ilişkili olarak sapmalarının kaç kere yinelendiğini ve iş emrindeki zamanlanan ve gerçek bitiş tarihini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4f0df-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![İş emri tarihi denetiminde örnek hesaplama sonuçları](media/03-controlling-and-reporting.png)


