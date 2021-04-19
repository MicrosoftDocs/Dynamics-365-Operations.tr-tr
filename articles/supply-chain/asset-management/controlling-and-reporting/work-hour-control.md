---
title: Çalışma saati denetimi
description: Bu konuda Varlık Yönetimi'nde iş saati denetimini açıklanmaktadır.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9ac64b0e40662f30cc615dfbd3f05aba5b37d862
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838670"
---
# <a name="work-hour-control"></a><span data-ttu-id="6e2ab-103">Çalışma saati denetimi</span><span class="sxs-lookup"><span data-stu-id="6e2ab-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6e2ab-104">Kıymet yönetiminde, sabit kıymetler, işlevsel yerleşimler ve iş emirleriyle ilgili bütçe saatleriyle karşılaştırıldığında fiili saatlerin genel görünümünü elde etmek için saatleri hesaplayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="6e2ab-105">Gerçek saatler deftere nakledilen hareketleri temel alarak yapılır.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="6e2ab-106">Kıymetler, işlevsel yerleşimler ve iş emirleri için çalışma saatleri kontrolü</span><span class="sxs-lookup"><span data-stu-id="6e2ab-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="6e2ab-107">Varlıklar, işlevsel yerleşimler ve çalışma emirleri için oluşturulan hesaplamalar neredeyse aynıdır.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="6e2ab-108">Tek fark, varlıklar ve işlem yapılacak konumlar için alt varlıkları ve alt konumları da hesaplamanıza dahil edebiliyor olmanızdır.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="6e2ab-109">Tarih, kayıt kaydedildiği hareket tarihidir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="6e2ab-110">**Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık saat denetimi** veya **İşlem yapılacak yerleşim saat denetimi** veya **Varlık yönetimi** > **Sorgular** > **İş emirleri** > **İş emri saat denetimi**'ne tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="6e2ab-111">**Kıymet saati denetimi** iletişim kutusunda.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="6e2ab-112">**Varlık saat denetimi** / **İşlem yapılacak yerleşim saat denetimi** / **İş emri saat denetimi** iletişim kutusunda, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında hesaplanacak bir dönem seçin.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="6e2ab-113">Gerekirse, hesaplamaya dahil edilecek bir **Mali boyut kümesi** seçin.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="6e2ab-114">Sıfır saat içeren sonuçları göstermek istemiyorsanız, **sıfır atlama** düğmesi üzerinde "Evet" seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="6e2ab-115">İşlem yapılacak yerleşimlerle ilgili olarak saat denetimi satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="6e2ab-116">Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim hiyerarşiniz varsa, işlem yapılacak yerleşim için tüm saat denetimi satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="6e2ab-117">**Düzey** alanına "0" sayısını girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm saat denetimi satırlarını gösteren ayrıntılı bir sonuç görürsünüz.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="6e2ab-118">Alt kıymetlerle ilgili maliyetleri ayrı satırlar olarak göstermek için **alt kıymetleri dahil et** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="6e2ab-119">Aramayı sınırlandırmak istiyorsanız, Hızlı Sekme **dahil edilecek kayıtlar** üzerinde belirli varlıkları / işlem yapılacak yerleşimleri / iş emirlerini seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="6e2ab-120">Hesaplamayı başlatmak için **Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="6e2ab-121">**Varlık saat denetimi** sayfasında, hesaplamanın gerekli ayrıntı düzeyini göstermek için **Gruplama ölçütü** düğmelerine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="6e2ab-122">Seçilen **Gruplandırma ölçütü** düğmeleri vurgulanır.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="6e2ab-123">Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="6e2ab-124">Örnek</span><span class="sxs-lookup"><span data-stu-id="6e2ab-124">Example</span></span>

<span data-ttu-id="6e2ab-125">Aşağıdaki ekran görüntüsü, **Varlık saat denetimi** hesaplamasının birkaç örneğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="6e2ab-126">**Orijinal bütçe** alanı, bütçe saatlerini iş emri tahmininden gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="6e2ab-127">**Fiili saatler** alanı, iş emirlerinde deftere nakledilir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="6e2ab-128">**Taahhüt edilen saatler** alanı, şirketinizin iş siparişleri ile ilgili olarak taahhüt edildiği toplam saat miktarını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Varlık saat denetim hesaplaması örneği](media/04-controlling-and-reporting.png)

<span data-ttu-id="6e2ab-130">Bir saat hesaplaması yapmanın bir başka yolu **Tüm varlıklar** veya **Etkin varlıklar** içinde çoklu varlıkları seçmektir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="6e2ab-131">Daha sonra **Genel** Hızlı Sekmesi üzerinde **Saat denetimi** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="6e2ab-132">Seçilen varlıklar, hızlı sekme **dahil edilecek kayıtlar** alanındaki **varlık** alanına otomatik olarak eklenir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="6e2ab-133">**Varlık saati kontrol** iletişim kutusunda, **Tamam** üzerine tıklayın ve seçilen varlıklar için hesaplama gösterilir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="6e2ab-134">Aynı işlem **Tüm işlem yapılacak yerleşimler** veya **Etkin işlem yapılacak yerleşimler** içindeki işlem yapılacak yerleşimler ve **Tüm iş emirleri** veya **Etkin iş emirleri** içindeki tüm iş emirleri için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6e2ab-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]