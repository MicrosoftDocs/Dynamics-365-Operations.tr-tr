---
title: Maliyet ve tarih kontrolü
description: Bu konuda Varlık Yönetimi'nde maliyeti ve tarih denetimini açıklanmaktadır.
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
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918407"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="7cdfd-103">Maliyet ve tarih kontrolü</span><span class="sxs-lookup"><span data-stu-id="7cdfd-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="7cdfd-104">Kıymet yönetiminde, sabit kıymetler, işlevsel yerleşimler ve iş emirleriyle ilgili bütçe maliyetleriyle karşılaştırıldığında fiili maliyetlerin genel görünümünü elde etmek için maliyetleri hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="7cdfd-105">Fiili maliyetler deftere nakledilen hareketleri temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="7cdfd-106">Ayrıca, planlanan başlangıç ve bitiş tarihlerini çalışma emirlerindeki gerçek başlangıç ve bitiş tarihleriyle karşılaştırmak istiyorsanız, tarih hesaplaması da yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="7cdfd-107">Kıymetler, işlevsel yerleşimler ve iş emirleri için maliyet kontrolü</span><span class="sxs-lookup"><span data-stu-id="7cdfd-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="7cdfd-108">Varlıklar, işlevsel yerleşimler ve çalışma emirleri için oluşturulan hesaplamalar neredeyse aynıdır.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="7cdfd-109">Tek fark, varlıklar ve işlem yapılacak konumlar için alt varlıkları ve alt konumları da hesaplamanıza dahil edebiliyor olmanızdır.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="7cdfd-110">Tarih, kayıt kaydedildiği hareket tarihidir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="7cdfd-111">**Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık maliyet denetimi** veya **İşlem yapılacak yerleşim maliyet denetimi** veya **Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri maliyet denetimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="7cdfd-112">**Varlık maliyet denetimi** / **İşlem yapılacak yerleşim maliyet denetimi** / **İş emri maliyet denetimi** iletişim kutusunda, hesaplanacak bir dönemi seçin.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="7cdfd-113">Gerekirse, hesaplamaya dahil edilecek bir mali boyut kümesi seçin.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="7cdfd-114">Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="7cdfd-115">İşlem yapılacak yerleşimlerle ilgili olarak maliyet denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="7cdfd-116">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim hiyerarşiniz varsa, işlem yapılacak yerleşim için tüm maliyet denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="7cdfd-117">**Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm maliyet denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="7cdfd-118">Bu sütunu hesaplamaya dahil etmek istiyorsanız **Açık taahhüt edilen maliyeti göster** değiştir düğmesini göster üzerinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="7cdfd-119">Alt kıymetlerle ilgili maliyetleri ayrı satırlar olarak göstermek için **alt kıymetleri dahil et** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="7cdfd-120">Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli varlıkları / işlem yapılacak yerleşimleri / iş emirlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="7cdfd-121">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="7cdfd-122">Aşağıdaki şekil, **Varlık maliyet denetimi** iletişim kutusunun bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![Şekil 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="7cdfd-124">**Varlık maliyet denetimi** sayfasındaki **Şuna göre grupla...** eylem panosu gruplarında, hesaplamanın gerekli ayrıntı düzeyini gösteren ilgili düğmelere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="7cdfd-125">Seçilen eylem bölmesi düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="7cdfd-126">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="7cdfd-127">Aşağıdaki şekil, **Varlık maliyet denetimi** içinde hesaplama sonuçlarının bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![Şekil 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="7cdfd-129">Maliyet hesaplaması yapmanın bir başka yolu **Tüm varlıklar** veya **Etkin varlıklar** içinde çoklu varlıkları seçmektir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="7cdfd-130">Daha sonra, **genel** sekmesindeki **maliyet denetimi** düğmesini tıklatın. **Varlık maliyet denetimi** iletişim kutusunda, seçilen kıymetler hızlı sekme **dahil edilecek kayıtlar** içindeki **Varlık** alanına otomatik eklenir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="7cdfd-131">**Tamam**'ı tıklattın ve seçilen varlıklar için bir maliyet hesaplaması gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="7cdfd-132">Aynı işlem **Tüm işlem yapılacak yerleşimler** veya **Etkin işlem yapılacak yerleşimler** içindeki işlem yapılacak yerleşimler ve **Tüm iş emirleri** veya **Etkin iş emirleri** içindeki tüm iş emirleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="7cdfd-133">**Orijinal bütçe** alanı, bütçe maliyetlerini iş emri tahmininden gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="7cdfd-134">**Taahhüt edilen maliyet** alanı, tüzel kişiliğin kendisi ödemek üzere taahhüt ettiği giderlerin tutarın toplamını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="7cdfd-135">**Açık taahhüt edilen maliyet** alanı, sipariş ettiğiniz veya aldığınız, ancak henüz ödenmemiş olan maddeler, saatler ve servisler için ödeme taahhütlerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="7cdfd-136">Tüm tüketim kayıtları gönderildikten sonra, ilgili maliyetler **Fiili maliyet** alanına eklenir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="7cdfd-137">İş emri tarih denetimi</span><span class="sxs-lookup"><span data-stu-id="7cdfd-137">Work order date control</span></span>

<span data-ttu-id="7cdfd-138">İş emirlerindeki gerçek başlangıç ve bitiş tarihleriyle karşılaştırıldığında, beklenen başlangıç ve bitiş tarihlerinin özetini almak için bu sayfayı kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="7cdfd-139">**Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri tarih denetimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="7cdfd-140">**Hesapla** üzerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="7cdfd-141">**İşlem yapılacak yerleşim** alanında bir işlem yapılacak yerleşim seçin.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="7cdfd-142">**Başlangıç tarihi** ve **Bitiş tarihi** alanlarında hesaplamayı yapmak istediğiniz dönemi girin.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="7cdfd-143">Dönem içinde başlaması beklenen tüm iş emirleri dahil edilir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="7cdfd-144">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-144">Click **OK**.</span></span>

6. <span data-ttu-id="7cdfd-145">**Gruplandırma ölçütü...** eylem bölmesi gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="7cdfd-146">Seçilen eylem bölmesi düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="7cdfd-147">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="7cdfd-148">Aşağıdaki şekil, **İş emri tarih denetimi** içinde hesaplama sonuçlarının bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![Şekil 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="7cdfd-150">**Ortalama başlangıç gecikmesi** alanı, fiili başlangıç tarihiyle karşılaştırıldığında bir iş emri için planlanan başlangıç tarihi arasındaki farkı gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="7cdfd-151">Örneğin, gerçek başlangıç tarihi planlanan başlangıç tarihinden iki gün önce ise, bu alanda "-2" görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="7cdfd-152">**Ortalama bitiş gecikmesi** alanı, fiili bitiş tarihiyle karşılaştırıldığında bir iş emri için planlanan bitiş tarihi arasındaki farkı gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="7cdfd-153">Örneğin, gerçek bitiş tarihi planlanan bitiş tarihinden üç gün sonra ise, bu alanda "3" görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="7cdfd-154">**Oluşum** alanları, planlanan ve fiili başlangıç tarihiyle ilişkili olarak sapmalarının kaç kere yinelendiğini ve iş emrindeki zamanlanan ve gerçek bitiş tarihini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cdfd-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

