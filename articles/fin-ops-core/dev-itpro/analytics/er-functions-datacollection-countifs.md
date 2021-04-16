---
title: COUNTIFS ER işlevi
description: Bu konu, COUNTIFS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 667002aa01537f846c616d38bba436da18f6e05f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755288"
---
# <a name="countifs-er-function"></a><span data-ttu-id="312de-103">COUNTIFS ER işlevi</span><span class="sxs-lookup"><span data-stu-id="312de-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="312de-104">`COUNTIFS` işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşula uyuyan Biçim öğelerinin sayısını temsil eden bir *tamsayı* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="312de-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="312de-105">Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="312de-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="312de-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="312de-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="312de-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="312de-107">Arguments</span></span>

<span data-ttu-id="312de-108">`condition 1 range`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="312de-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="312de-109">Bir elektronik raporlama (ER) biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="312de-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="312de-110">Bu bağımsız değişken zorunlu.</span><span class="sxs-lookup"><span data-stu-id="312de-110">This argument is mandatory.</span></span>

<span data-ttu-id="312de-111">`condition 1 value`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="312de-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="312de-112">Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="312de-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="312de-113">Bu bağımsız değişken zorunlu.</span><span class="sxs-lookup"><span data-stu-id="312de-113">This argument is mandatory.</span></span>

<span data-ttu-id="312de-114">`condition N range`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="312de-114">`condition N range`: *String*</span></span>

<span data-ttu-id="312de-115">Bir ER biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="312de-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="312de-116">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="312de-116">These additional arguments are optional.</span></span>

<span data-ttu-id="312de-117">`condition N value`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="312de-117">`condition N value`: *String*</span></span>

<span data-ttu-id="312de-118">Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="312de-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="312de-119">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="312de-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="312de-120">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="312de-120">Return values</span></span>

<span data-ttu-id="312de-121">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="312de-121">*Integer*</span></span>

<span data-ttu-id="312de-122">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="312de-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="312de-123">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="312de-123">Usage notes</span></span>

<span data-ttu-id="312de-124">Bu işlev, **toplanan veri anahtarı adı** ve **Toplanan veri anahtarı değeri** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="312de-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="312de-125">Bu işlev, Geçerli **Ortak\\Dosya** bileşeninin **Çıkış ayrıntılarını topla** seçeneği bayrağı kapatıldığında **0** (sıfır) değeri döner.</span><span class="sxs-lookup"><span data-stu-id="312de-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="312de-126">`condition range` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="312de-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="312de-127">`condition value` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="312de-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="312de-128">Örnek</span><span class="sxs-lookup"><span data-stu-id="312de-128">Example</span></span>

<span data-ttu-id="312de-129">Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.</span><span class="sxs-lookup"><span data-stu-id="312de-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="312de-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="312de-130">Additional resources</span></span>

[<span data-ttu-id="312de-131">Veri toplama işlevleri</span><span class="sxs-lookup"><span data-stu-id="312de-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]