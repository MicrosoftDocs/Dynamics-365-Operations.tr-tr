---
title: Ürün yapılandırma modeli hesaplamaları
description: Bu konuda, bir ürün yapılandırma modelinde öznitelikler için hesaplamaların nasıl oluşturulacağı açıklanmaktadır
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829630"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="61398-103">Ürün yapılandırma modeli hesaplamaları</span><span class="sxs-lookup"><span data-stu-id="61398-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61398-104">Bu konuda, bir ürün yapılandırma modelinde öznitelikler için hesaplamaların nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="61398-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="61398-105">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="61398-105">Prerequisites</span></span>

<span data-ttu-id="61398-106">Ürün konfigürasyon modelinde, bir ürünün konfigürasyon değerlerini hesaplamak için hesaplamalar kullanılır.</span><span class="sxs-lookup"><span data-stu-id="61398-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="61398-107">Hesaplamaları ayarlamaya başlamadan önce ilgili ürün konfigürasyon modeli mevcut olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="61398-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="61398-108">Konfigürasyon modellerinin kurulum işlemine ve ilgili görevlere genel bakış için, bkz. [ürün konfigürasyon modeli ayarlama](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="61398-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="61398-109">Hesaplama oluşturma</span><span class="sxs-lookup"><span data-stu-id="61398-109">Create a calculation</span></span>

<span data-ttu-id="61398-110">Bir hesaplama bir ifade ve bir hedef özniteliğinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="61398-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="61398-111">Daha fazla bilgi için, bkz. [Ürün konfigürasyon modellerini hesaplama SSS](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="61398-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="61398-112">Varolan bir ürün modeli için hesaplama oluşturmak üzere, aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="61398-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="61398-113">**Ürün bilgileri yönetimi \> Ortak \> Ürün yapılandırma modelleri** öğelerini tıklayın.</span><span class="sxs-lookup"><span data-stu-id="61398-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="61398-114">Bir ürün konfigürasyon modeli açın ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="61398-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="61398-115">**Hesaplamalar** hızlı sekmesinde, hesaplama eklemek için **Ekle**'yi seçin ve ardından aşağıdaki alanları ayarlayın:</span><span class="sxs-lookup"><span data-stu-id="61398-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="61398-116">**Ad**: Hesaplama için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="61398-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="61398-117">**Açıklama**: Hesaplamanın açıklamasını girin.</span><span class="sxs-lookup"><span data-stu-id="61398-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="61398-118">**Hedef özniteliği**: Hesaplamasını yapmakta olduğunuz özniteliği seçin.</span><span class="sxs-lookup"><span data-stu-id="61398-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="61398-119">**İfadeyi Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="61398-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="61398-120">**Bir hesaplama girin** iletişim kutusunda, ifadeye gerekli öznitelikleri, işleçleri ve değerleri ekleyin.</span><span class="sxs-lookup"><span data-stu-id="61398-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="61398-121">Bu unsurlarla çalışma hakkında daha fazla bilgi için bkz. [Ürün yapılandırma modellerinde ifade kısıtlamaları ve tablo kısıtlamaları](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="61398-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="61398-122">İfadeniz hazır olduğunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="61398-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="61398-123">Hesaplama örnekleri</span><span class="sxs-lookup"><span data-stu-id="61398-123">Calculation examples</span></span>

<span data-ttu-id="61398-124">Bu bölümde, hesaplamaların nasıl çalıştığını gösteren birkaç örnek sağlanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="61398-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="61398-125">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="61398-125">Example 1</span></span>

<span data-ttu-id="61398-126">Hedef özniteliği Boole'dir, hesaplama aşağıdaki koşullu ifadeyi kullanır:</span><span class="sxs-lookup"><span data-stu-id="61398-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="61398-127">`decimalAttribute2` değeri, `decimalAttribute1` değerine eşitse veya daha yüksekse bu ifade, hedef özniteliğe *True* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="61398-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="61398-128">Aksi takdirde, *False* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="61398-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="61398-129">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="61398-129">Example 2</span></span>

<span data-ttu-id="61398-130">Bu örnek, hedef özniteliği olarak `textFixedList` metin özniteliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="61398-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="61398-131">Bu öznitelik aşağıdaki sabit listeyi içerir.</span><span class="sxs-lookup"><span data-stu-id="61398-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="61398-132">Değer</span><span class="sxs-lookup"><span data-stu-id="61398-132">Value</span></span> | <span data-ttu-id="61398-133">Çözücü değeri</span><span class="sxs-lookup"><span data-stu-id="61398-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="61398-134">A</span><span class="sxs-lookup"><span data-stu-id="61398-134">A</span></span> | <span data-ttu-id="61398-135">1a</span><span class="sxs-lookup"><span data-stu-id="61398-135">1a</span></span> |
| <span data-ttu-id="61398-136">B:</span><span class="sxs-lookup"><span data-stu-id="61398-136">B</span></span> | <span data-ttu-id="61398-137">2b</span><span class="sxs-lookup"><span data-stu-id="61398-137">2b</span></span> |
| <span data-ttu-id="61398-138">A</span><span class="sxs-lookup"><span data-stu-id="61398-138">C</span></span> | <span data-ttu-id="61398-139">2c</span><span class="sxs-lookup"><span data-stu-id="61398-139">2c</span></span> |

<span data-ttu-id="61398-140">Aşağıdaki ekran görüntüsü, bu öznitelik için ayarların sisteminizde nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61398-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="61398-141">![Öznitelik türü ayarları Örnek 2](media/model-calculations-example2.png "Öznitelik türü ayarları Örnek 2")</span><span class="sxs-lookup"><span data-stu-id="61398-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="61398-142">Öznitelik aşağıdaki koşul deyiminde kullanılır:</span><span class="sxs-lookup"><span data-stu-id="61398-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="61398-143">`integerAttribute` 150'den küçükse, bu ifade sabit listesindeki ilk kaydın metin değerini *A* döndürür. Aksi durumda, sabit listedeki üçüncü kaydın metin değerini *C* döndürür.</span><span class="sxs-lookup"><span data-stu-id="61398-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="61398-144">Sabit liste sıfır tabanlı bir numaralandırmaya (enum) eşdeğerdir ve değerlerine uygun tamsayı değeri tarafından erişilir.</span><span class="sxs-lookup"><span data-stu-id="61398-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="61398-145">Bu nedenle, ilk sabit liste değeri (*A*) *0* ile eşleşirse, ikinci değer (*B*) *1* ile eşleşir ve üçüncü değer (*C*) *2* ile eşleşir.</span><span class="sxs-lookup"><span data-stu-id="61398-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="61398-146">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="61398-146">Example 3</span></span>

<span data-ttu-id="61398-147">Bu örnek, önceki örnekten `textFixedList` hedef özniteliğini kullanır.</span><span class="sxs-lookup"><span data-stu-id="61398-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="61398-148">Ayrıca, aşağıdaki sabit listeyi içeren başka bir metin özniteliği (`textAttribute`) de kullanır.</span><span class="sxs-lookup"><span data-stu-id="61398-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="61398-149">Değer</span><span class="sxs-lookup"><span data-stu-id="61398-149">Value</span></span> | <span data-ttu-id="61398-150">Çözücü değeri</span><span class="sxs-lookup"><span data-stu-id="61398-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="61398-151">AA</span><span class="sxs-lookup"><span data-stu-id="61398-151">AA</span></span> | <span data-ttu-id="61398-152">1aa</span><span class="sxs-lookup"><span data-stu-id="61398-152">1aa</span></span> |
| <span data-ttu-id="61398-153">BB</span><span class="sxs-lookup"><span data-stu-id="61398-153">BB</span></span> | <span data-ttu-id="61398-154">2bb</span><span class="sxs-lookup"><span data-stu-id="61398-154">2bb</span></span> |

<span data-ttu-id="61398-155">Aşağıdaki ekran görüntüsü, bu öznitelik için ayarların sisteminizde nasıl görünebileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61398-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="61398-156">![Öznitelik türü ayarları Örnek 3](media/model-calculations-example3.png "Öznitelik türü ayarları Örnek 3")</span><span class="sxs-lookup"><span data-stu-id="61398-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="61398-157">`textFixedList` Özniteliğinin değeri aşağıdaki koşul deyimi kullanılarak hesaplanır:</span><span class="sxs-lookup"><span data-stu-id="61398-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="61398-158">`textAttribute` değeri *1aa* ile eş değer bir çözücü değerine sahipse bu ifade `textFixedList` sabit listesindeki ilk kaydın metin değerini *A* döndürür. Aksi durumda, `textFixedList` sabit listesindeki üçüncü kaydın metin değerini *C* döndürür.</span><span class="sxs-lookup"><span data-stu-id="61398-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="61398-159">Koşullu deyim özniteliğin çözücü değerini kullanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="61398-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="61398-160">Hesaplamalarda yalnızca sabit liste metin öznitelikleri kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="61398-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="61398-161">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="61398-161">See also</span></span>

- [<span data-ttu-id="61398-162">Ürün yapılandırma modeli için hesaplamalar SSS</span><span class="sxs-lookup"><span data-stu-id="61398-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="61398-163">Ürün yapılandırma modeline bir ifade kısıtlaması ekleme</span><span class="sxs-lookup"><span data-stu-id="61398-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="61398-164">Ürün yapılandırma modellerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="61398-164">Product configuration models overview</span></span>](product-configuration-models.md)
