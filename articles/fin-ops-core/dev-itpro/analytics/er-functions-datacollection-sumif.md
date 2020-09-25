---
title: SUMIF ER işlevi
description: Bu konu, SUMIF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 174ac28ee2b726ec7fb2ff6d3dda45906c56af65
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745621"
---
# <a name="sumif-er-function"></a><span data-ttu-id="183c4-103">SUMIF ER işlevi</span><span class="sxs-lookup"><span data-stu-id="183c4-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="183c4-104">`SUMIF` işlevi, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşullara uyuyan Biçim öğelerinin sayısını temsil eden bir *Gerçek* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="183c4-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="183c4-105">Koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="183c4-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="183c4-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="183c4-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="183c4-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="183c4-107">Arguments</span></span>

<span data-ttu-id="183c4-108">`key name for summing`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="183c4-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="183c4-109">Toplama değerinin toplayıcı amacıyla kullanılması gereken elektronik raporlama (ER) biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="183c4-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="183c4-110">Bu işlev, **Toplanan veri anahtarı değeri** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="183c4-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="183c4-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="183c4-111">Return values</span></span>

<span data-ttu-id="183c4-112">*Gerçek*</span><span class="sxs-lookup"><span data-stu-id="183c4-112">*Real*</span></span>

<span data-ttu-id="183c4-113">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="183c4-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="183c4-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="183c4-114">Usage notes</span></span>

<span data-ttu-id="183c4-115">Bu işlev, Geçerli **Ortak\\Dosya** bileşeninin **Çıkış ayrıntılarını topla** seçeneği bayrağı kapatıldığında **0** (sıfır) değeri döner.</span><span class="sxs-lookup"><span data-stu-id="183c4-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="183c4-116">`condition range` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="183c4-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="183c4-117">`condition value` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="183c4-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="183c4-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="183c4-118">Example</span></span>

<span data-ttu-id="183c4-119">Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.</span><span class="sxs-lookup"><span data-stu-id="183c4-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="183c4-120">Bu işlevi kullanma hakkında daha fazla bilgi ve örnekler için bkz. [ER biçimindeki sıra öğelerinin yürütülmesini erteleme](er-defer-sequence-element.md#Example) ve [ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="183c4-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="183c4-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="183c4-121">Additional resources</span></span>

[<span data-ttu-id="183c4-122">Veri toplama işlevleri</span><span class="sxs-lookup"><span data-stu-id="183c4-122">Data collection functions</span></span>](er-functions-category-data-collection.md)
