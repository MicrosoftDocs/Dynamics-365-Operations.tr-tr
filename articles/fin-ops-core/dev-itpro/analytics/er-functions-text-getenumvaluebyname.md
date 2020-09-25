---
title: GETENUMVALUEBYNAME işlevi
description: Bu konu, GETENUMVALUEBYNAME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743867"
---
# <a name="getenumvaluebyname-er-function"></a><span data-ttu-id="8bbdc-103">GETENUMVALUEBYNAME işlevi</span><span class="sxs-lookup"><span data-stu-id="8bbdc-103">GETENUMVALUEBYNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bbdc-104">`GETENUMVALUEBYNAME` işlevi, belirtilen numaralandırma veri kaynağındaki belirli bir *Enum* değerini *dize* değeri olarak belirtilen numaralandırma adını kullanarak arar.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="8bbdc-105">*Numaralama* değeri bulunursa, işlev bunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="8bbdc-106">Aksi durumda, işlev **boş** numaralandırma değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bbdc-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8bbdc-107">Syntax</span></span>

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="8bbdc-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="8bbdc-108">Arguments</span></span>

<span data-ttu-id="8bbdc-109">`enumeration data source path`: *numaralandırması*</span><span class="sxs-lookup"><span data-stu-id="8bbdc-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="8bbdc-110">Aşağıdaki sabit listesi tiplerinden birinin veri kaynağının geçerli yolu:</span><span class="sxs-lookup"><span data-stu-id="8bbdc-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="8bbdc-111">Elektronik raporlama (ER) model numaralandırması</span><span class="sxs-lookup"><span data-stu-id="8bbdc-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="8bbdc-112">ER biçim numaralandırma</span><span class="sxs-lookup"><span data-stu-id="8bbdc-112">ER format enumeration</span></span>
- <span data-ttu-id="8bbdc-113">Microsoft Dynamics 365 Finance numaralandırması</span><span class="sxs-lookup"><span data-stu-id="8bbdc-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="8bbdc-114">`enumeration value text`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="8bbdc-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="8bbdc-115">Tek bir numaralandırma değerinin adını gösteren bir dize değeri.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="8bbdc-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="8bbdc-116">Return values</span></span>

<span data-ttu-id="8bbdc-117">Boş giriş yapılabilir *Enum*</span><span class="sxs-lookup"><span data-stu-id="8bbdc-117">Nullable *Enum*</span></span>

<span data-ttu-id="8bbdc-118">Sonuç numaralandırma değeri.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8bbdc-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="8bbdc-119">Usage notes</span></span>

<span data-ttu-id="8bbdc-120">Bir *dize* değeri olarak belirtilen numaralandırma değerinin adı kullanılarak bir *Enum* değeri bulunamazsa, hiçbir özel durum atılır.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="8bbdc-121">Örnek</span><span class="sxs-lookup"><span data-stu-id="8bbdc-121">Example</span></span>

<span data-ttu-id="8bbdc-122">Aşağıdaki örnekte, bir veri modelinde oluşturulan **ReportDirection** numaralandırması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="8bbdc-123">Etiketlerin numaralandırma değerleri ile tanımlandığını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="8bbdc-124">Aşağıdaki örnek ayrıntıları göstermektedir:</span><span class="sxs-lookup"><span data-stu-id="8bbdc-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="8bbdc-125">**$Direction** veri kaynağı bir er raporu içinde konfigüre edilmiş.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="8bbdc-126">Bu veri kaynağı **RaporYönü** modeli sabit listesi temel alınarak yapılandırıldı.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="8bbdc-127">Bu işlevin parametresi olarak model numaralandırmaya dayalı **$Direction** veri kaynağı kullanmak için tasarlanan `$IsArrivals` ifadesi.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="8bbdc-128">Bu karşılaştırma ifadenin değeri **DOĞRU**'dur.</span><span class="sxs-lookup"><span data-stu-id="8bbdc-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="8bbdc-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8bbdc-129">Additional resources</span></span>

[<span data-ttu-id="8bbdc-130">Metin işlevleri</span><span class="sxs-lookup"><span data-stu-id="8bbdc-130">Text functions</span></span>](er-functions-category-text.md)
