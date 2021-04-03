---
title: GETENUMVALUEBYNAME işlevi
description: Bu konu, GETENUMVALUEBYNAME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570602"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="68a7c-103">GETENUMVALUEBYNAME işlevi</span><span class="sxs-lookup"><span data-stu-id="68a7c-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68a7c-104">`GETENUMVALUEBYNAME` işlevi, belirtilen numaralandırma veri kaynağındaki belirli bir *Enum* değerini *dize* değeri olarak belirtilen numaralandırma adını kullanarak arar.</span><span class="sxs-lookup"><span data-stu-id="68a7c-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="68a7c-105">*Numaralama* değeri bulunursa, işlev bunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="68a7c-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="68a7c-106">Aksi durumda, işlev **boş** numaralandırma değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="68a7c-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a7c-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="68a7c-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="68a7c-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="68a7c-108">Arguments</span></span>

<span data-ttu-id="68a7c-109">`enumeration data source path`: *numaralandırması*</span><span class="sxs-lookup"><span data-stu-id="68a7c-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="68a7c-110">Aşağıdaki sabit listesi tiplerinden birinin veri kaynağının geçerli yolu:</span><span class="sxs-lookup"><span data-stu-id="68a7c-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="68a7c-111">Elektronik raporlama (ER) model numaralandırması</span><span class="sxs-lookup"><span data-stu-id="68a7c-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="68a7c-112">ER biçim numaralandırma</span><span class="sxs-lookup"><span data-stu-id="68a7c-112">ER format enumeration</span></span>
- <span data-ttu-id="68a7c-113">Microsoft Dynamics 365 Finance numaralandırması</span><span class="sxs-lookup"><span data-stu-id="68a7c-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="68a7c-114">`enumeration value text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="68a7c-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="68a7c-115">Tek bir numaralandırma değerinin adını gösteren bir dize değeri.</span><span class="sxs-lookup"><span data-stu-id="68a7c-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="68a7c-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="68a7c-116">Return values</span></span>

<span data-ttu-id="68a7c-117">Boş giriş yapılabilir *Enum*</span><span class="sxs-lookup"><span data-stu-id="68a7c-117">Nullable *Enum*</span></span>

<span data-ttu-id="68a7c-118">Sonuç numaralandırma değeri.</span><span class="sxs-lookup"><span data-stu-id="68a7c-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="68a7c-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="68a7c-119">Usage notes</span></span>

<span data-ttu-id="68a7c-120">Bir *dize* değeri olarak belirtilen numaralandırma değerinin adı kullanılarak bir *Enum* değeri bulunamazsa, hiçbir özel durum atılır.</span><span class="sxs-lookup"><span data-stu-id="68a7c-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="68a7c-121">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="68a7c-121">Example 1</span></span>

<span data-ttu-id="68a7c-122">Aşağıdaki örnekte, bir veri modelinde oluşturulan **ReportDirection** numaralandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="68a7c-123">Etiketlerin numaralandırma değerleri ile tanımlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="68a7c-123">Notice that labels are defined for the enumeration values.</span></span>

![Veri modeli numaralandırması için kullanılabilir değerler](./media/ER-data-model-enumeration-values.PNG)

<span data-ttu-id="68a7c-125">Aşağıdaki örnek ayrıntıları göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="68a7c-125">The following illustration shows these details:</span></span>

- <span data-ttu-id="68a7c-126">**$Direction** veri kaynağı bir er raporu içinde konfigüre edilmiş.</span><span class="sxs-lookup"><span data-stu-id="68a7c-126">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="68a7c-127">Bu veri kaynağı **RaporYönü** modeli sabit listesi temel alınarak yapılandırıldı.</span><span class="sxs-lookup"><span data-stu-id="68a7c-127">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="68a7c-128">Bu işlevin parametresi olarak model numaralandırmaya dayalı **$Direction** veri kaynağı kullanmak için tasarlanan `$IsArrivals` ifadesi.</span><span class="sxs-lookup"><span data-stu-id="68a7c-128">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="68a7c-129">Bu karşılaştırma ifadenin değeri **DOĞRU**'dur.</span><span class="sxs-lookup"><span data-stu-id="68a7c-129">The value of this comparison expression is **TRUE**.</span></span>

![Veri modeli numaralandırması örneği](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a><span data-ttu-id="68a7c-131">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="68a7c-131">Example 2</span></span>

<span data-ttu-id="68a7c-132">`GETENUMVALUEBYNAME` ve [`LISTOFFIELDS`](er-functions-list-listoffields.md) işlevleri, desteklenen numaralandırmalar değerlerini ve etiketlerini metin değerleri olarak getirir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-132">The `GETENUMVALUEBYNAME` and [`LISTOFFIELDS`](er-functions-list-listoffields.md) functions let you fetch values and labels of supported enumerations as text values.</span></span> <span data-ttu-id="68a7c-133">(Desteklenen numaralandırmalar uygulama numaralandırmalar, veri modeli numaralandırmaları ve biçim numaralandırmalarıdır.)</span><span class="sxs-lookup"><span data-stu-id="68a7c-133">(The supported enumerations are application enumerations, data model enumerations, and format enumerations.)</span></span>

<span data-ttu-id="68a7c-134">Aşağıdaki örnekte, bir model eşlemesinde oluşturulan **TransType** veri kaynağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-134">In the following illustration, the **TransType** data source is introduced in a model mapping.</span></span> <span data-ttu-id="68a7c-135">Bu veri kaynağı **LedgerTransType** uygulama numaralandırması anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-135">This data source refers to the **LedgerTransType** application enumeration.</span></span>

![Uygulama numaralandırmasına başvuran model eşlemesinin veri kaynağı](./media/er-functions-text-getenumvaluebyname-example2-1.png)

<span data-ttu-id="68a7c-137">Aşağıdaki resim, bir model eşlemesinde yapılandırılan **TransTypeList** veri kaynağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-137">The following illustration shows the **TransTypeList** data source that is configured in a model mapping.</span></span> <span data-ttu-id="68a7c-138">Bu veri kaynağı **TransType** uygulama numaralandırması temel alınarak yapılandırıldı.</span><span class="sxs-lookup"><span data-stu-id="68a7c-138">This data source is configured based on the **TransType** application enumeration.</span></span> <span data-ttu-id="68a7c-139">`LISTOFFIELDS` işlevi, alan içeren kayıtların listesi olarak tüm numaralandırma değerlerini döndürmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="68a7c-139">The `LISTOFFIELDS` function is used to return all enumeration values as a list of records that contain fields.</span></span> <span data-ttu-id="68a7c-140">Bu şekilde, her numaralandırma değerinin ayrıntıları gösterilir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-140">In this way, the details of every enumeration value are exposed.</span></span>

> [!NOTE]
> <span data-ttu-id="68a7c-141">**EnumValue** alanı, `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` ifadesi kullanılarak **TranstTypeList** veri kaynağı için yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="68a7c-141">The **EnumValue** field is configured for the **TransTypeList** data source by using the `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` expression.</span></span> <span data-ttu-id="68a7c-142">Bu alan, bu listedeki her kayıt için bir numaralandırma değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="68a7c-142">This field returns an enumeration value for every record in this list.</span></span>

![Seçilen bir numaralandırmanın tüm numaralandırma değerlerini kayıt listesi olarak döndüren model eşleme veri kaynağı](./media/er-functions-text-getenumvaluebyname-example2-2.png)

<span data-ttu-id="68a7c-144">Aşağıdaki resim, bir model eşlemesinde yapılandırılan **VendTrans** veri kaynağını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-144">The following illustration shows the **VendTrans** data source that is configured in a model mapping.</span></span> <span data-ttu-id="68a7c-145">Bu veri kaynağı, **VendTrans** uygulama tablosundaki satıcı hareket kayıtlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="68a7c-145">This data source returns vendor transaction records from the **VendTrans** application table.</span></span> <span data-ttu-id="68a7c-146">Her hareketin genel muhasebe türü, **TransType** alanının değeriyle tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="68a7c-146">The ledger type of every transaction is defined by the value of the **TransType** field.</span></span>

> [!NOTE]
> <span data-ttu-id="68a7c-147">**TransTypeTitle** alanı, `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` ifadesi kullanılarak **VendTrans** veri kaynağı için yapılandırılır.</span><span class="sxs-lookup"><span data-stu-id="68a7c-147">The **TransTypeTitle** field is configured for the **VendTrans** data source by using the `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` expression.</span></span> <span data-ttu-id="68a7c-148">Bu numaralandırma değeri kullanılabilir ise, bu alan geçerli hareketin numaralandırma değerinin etiketini metin olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="68a7c-148">This field returns the label of an enumeration value of the current transaction as text, if this enumeration value is available.</span></span> <span data-ttu-id="68a7c-149">Aksi halde, boş bir dize değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="68a7c-149">Otherwise, it returns a blank string value.</span></span>
>
> <span data-ttu-id="68a7c-150">**TransTypeTitle** alanı, veri modelini veri kaynağı olarak kullanan her ER biçiminde bu bilginin kullanılmasına olanak sağlayan bir veri modelinin **LedgerType** alanına bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="68a7c-150">The **TransTypeTitle** field is bound to the **LedgerType** field of a data model that enables this information to be used in every ER format that uses the data model as a source of data.</span></span>

![Satıcı hareketlerini döndüren model eşlemesinin veri kaynağı](./media/er-functions-text-getenumvaluebyname-example2-3.png)

<span data-ttu-id="68a7c-152">Aşağıdaki şekil, yapılandırılmış model eşlemesini test etmek için [veri kaynağı hata ayıklayıcısını](er-debug-data-sources.md) nasıl kullanabileceğinizi gösterir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-152">The following illustration shows how you can use the [data source debugger](er-debug-data-sources.md) to test the configured model mapping.</span></span>

![Yapılandırılan model eşlemesini test etmek için veri kaynağı hata ayıklayıcısını kullanma](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

<span data-ttu-id="68a7c-154">Bir veri modelinin **LedgerType** alanı, hareket türlerinin etiketlerini beklendiği gibi gösterir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-154">The **LedgerType** field of a data model exposes labels of transaction types as expected.</span></span>

<span data-ttu-id="68a7c-155">Bu yaklaşımı büyük miktarda hareket verisi için kullanmayı planlıyorsanız, yürütme performansını dikkate almanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="68a7c-155">If you plan to use this approach for a large amount of transactional data, you must consider execution performance.</span></span> <span data-ttu-id="68a7c-156">Daha fazla bilgi için, bkz. [Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md).</span><span class="sxs-lookup"><span data-stu-id="68a7c-156">For more information, see [Trace the execution of ER formats to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="68a7c-157">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="68a7c-157">Additional resources</span></span>

[<span data-ttu-id="68a7c-158">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="68a7c-158">Text functions</span></span>](er-functions-category-text.md)

[<span data-ttu-id="68a7c-159">Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme</span><span class="sxs-lookup"><span data-stu-id="68a7c-159">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

[<span data-ttu-id="68a7c-160">LISTOFFIELDS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="68a7c-160">LISTOFFIELDS ER function</span></span>](er-functions-list-listoffields.md)

[<span data-ttu-id="68a7c-161">FIRSTORNULL ER işlevi</span><span class="sxs-lookup"><span data-stu-id="68a7c-161">FIRSTORNULL ER function</span></span>](er-functions-list-firstornull.md)

[<span data-ttu-id="68a7c-162">WHERE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="68a7c-162">WHERE ER function</span></span>](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]