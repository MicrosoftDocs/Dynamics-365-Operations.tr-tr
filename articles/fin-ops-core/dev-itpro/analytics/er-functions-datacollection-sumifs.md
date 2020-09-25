---
title: SUMIFS ER işlevi
description: Bu konu, SUMIFS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: a6815a8c9f4141649532f9cd56ac3bc442b48686
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743339"
---
# <a name="sumifs-er-function"></a><span data-ttu-id="9e6df-103">SUMIFS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="9e6df-103">SUMIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9e6df-104">`SUMIFS` işlevi, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşullara uyuyan Biçim öğelerinin sayısını temsil eden bir *Gerçek* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="9e6df-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="9e6df-105">Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="9e6df-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e6df-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="9e6df-106">Syntax</span></span>

```vb
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="9e6df-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="9e6df-107">Arguments</span></span>

<span data-ttu-id="9e6df-108">`key name for summing`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="9e6df-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="9e6df-109">Toplama değerinin toplayıcı amacıyla kullanılması gereken elektronik raporlama (ER) biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="9e6df-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="9e6df-110">Bu işlev, **Toplanan veri anahtarı adı** özelliği, ER biçimi bileşeninin **Sayısal** bileşeni veya **Dize** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e6df-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="9e6df-111">`condition 1 range`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="9e6df-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="9e6df-112">Bir ER biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="9e6df-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="9e6df-113">Bu bağımsız değişken zorunlu.</span><span class="sxs-lookup"><span data-stu-id="9e6df-113">This argument is mandatory.</span></span>

<span data-ttu-id="9e6df-114">Bu işlev, **Toplanan veri anahtarı adı** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e6df-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="9e6df-115">`condition 1 value`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="9e6df-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="9e6df-116">Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="9e6df-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="9e6df-117">Bu bağımsız değişken zorunlu.</span><span class="sxs-lookup"><span data-stu-id="9e6df-117">This argument is mandatory.</span></span>

<span data-ttu-id="9e6df-118">Bu işlev, **Toplanan veri anahtarı değeri** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e6df-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="9e6df-119">`condition N range`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="9e6df-119">`condition N range`: *String*</span></span>

<span data-ttu-id="9e6df-120">Bir ER biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="9e6df-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="9e6df-121">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9e6df-121">These additional arguments are optional.</span></span>

<span data-ttu-id="9e6df-122">Bu işlev, **Toplanan veri anahtarı adı** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e6df-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="9e6df-123">`condition N value`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="9e6df-123">`condition N value`: *String*</span></span>

<span data-ttu-id="9e6df-124">Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="9e6df-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="9e6df-125">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="9e6df-125">These additional arguments are optional.</span></span>

<span data-ttu-id="9e6df-126">Bu işlev, **Toplanan veri anahtarı değeri** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e6df-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="9e6df-127">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="9e6df-127">Return values</span></span>

<span data-ttu-id="9e6df-128">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="9e6df-128">*Real*</span></span>

<span data-ttu-id="9e6df-129">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="9e6df-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9e6df-130">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="9e6df-130">Usage notes</span></span>

<span data-ttu-id="9e6df-131">Bu işlev, Geçerli **Ortak\\Dosya** bileşeninin **Çıkış ayrıntılarını topla** seçeneği bayrağı kapatıldığında **0** (sıfır) değeri döner.</span><span class="sxs-lookup"><span data-stu-id="9e6df-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="9e6df-132">`condition range` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e6df-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="9e6df-133">`condition value` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e6df-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="9e6df-134">Örnek</span><span class="sxs-lookup"><span data-stu-id="9e6df-134">Example</span></span>

<span data-ttu-id="9e6df-135">Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.</span><span class="sxs-lookup"><span data-stu-id="9e6df-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9e6df-136">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9e6df-136">Additional resources</span></span>

[<span data-ttu-id="9e6df-137">Veri toplama işlevleri</span><span class="sxs-lookup"><span data-stu-id="9e6df-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
