---
title: COUNTIF ER işlevi
description: Bu konu, COUNTIF Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3f1429ad98f9d4fdab992c2011c6518734484a84
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681196"
---
# <a name="countif-er-function"></a><span data-ttu-id="6fa31-103">COUNTIF ER işlevi</span><span class="sxs-lookup"><span data-stu-id="6fa31-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fa31-104">`COUNTIF` işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşula uyuyan Biçim öğelerinin sayısını temsil eden bir *tamsayı* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="6fa31-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="6fa31-105">Koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="6fa31-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa31-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="6fa31-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="6fa31-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="6fa31-107">Arguments</span></span>

<span data-ttu-id="6fa31-108">`condition range`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="6fa31-108">`condition range`: *String*</span></span>

<span data-ttu-id="6fa31-109">Bir elektronik raporlama (ER) biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="6fa31-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="6fa31-110">`condition value`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="6fa31-110">`condition value`: *String*</span></span>

<span data-ttu-id="6fa31-111">Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="6fa31-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="6fa31-112">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="6fa31-112">Return values</span></span>

<span data-ttu-id="6fa31-113">*Tamsayı*</span><span class="sxs-lookup"><span data-stu-id="6fa31-113">*Integer*</span></span>

<span data-ttu-id="6fa31-114">Sonuç sayısal değeri.</span><span class="sxs-lookup"><span data-stu-id="6fa31-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6fa31-115">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="6fa31-115">Usage notes</span></span>

<span data-ttu-id="6fa31-116">Bu işlev, **toplanan veri anahtarı adı** ve **Toplanan veri anahtarı değeri** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="6fa31-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="6fa31-117">Bu işlev, Geçerli **Ortak\\Dosya** bileşeninin **Çıkış ayrıntılarını topla** seçeneği bayrağı kapatıldığında **0** (sıfır) değeri döner.</span><span class="sxs-lookup"><span data-stu-id="6fa31-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="6fa31-118">`condition range` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6fa31-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="6fa31-119">`condition value` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6fa31-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="6fa31-120">Örnek</span><span class="sxs-lookup"><span data-stu-id="6fa31-120">Example</span></span>

<span data-ttu-id="6fa31-121">Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.</span><span class="sxs-lookup"><span data-stu-id="6fa31-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fa31-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6fa31-122">Additional resources</span></span>

[<span data-ttu-id="6fa31-123">Veri toplama işlevleri</span><span class="sxs-lookup"><span data-stu-id="6fa31-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
