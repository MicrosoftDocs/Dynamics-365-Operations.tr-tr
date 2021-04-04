---
title: COLLECTEDLIST ER işlevi
description: Bu konu, COLLECTEDLIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: ff48170247130a03b10dc8fe2973f8d774046944
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561410"
---
# <a name="collectedlist-er-function"></a><span data-ttu-id="f069b-103">COLLECTEDLIST ER işlevi</span><span class="sxs-lookup"><span data-stu-id="f069b-103">COLLECTEDLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f069b-104">`COLLECTEDLIST` işlevi, bir biçim öğesi için toplanan veri anahtarı değeri özelliği tarafından döndürülen ve Format ögeleri çalıştırma biçimi sırasında ve belirtilen koşullara uyan bir giden belge oluşturmak için kullanıldığında **toplanan değerlerin listesini** içeren bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="f069b-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="f069b-105">Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="f069b-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="f069b-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="f069b-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="f069b-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="f069b-107">Arguments</span></span>

<span data-ttu-id="f069b-108">`condition 1 range`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="f069b-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="f069b-109">Bir elektronik raporlama (ER) biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="f069b-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="f069b-110">Bu bağımsız değişken zorunlu.</span><span class="sxs-lookup"><span data-stu-id="f069b-110">This argument is mandatory.</span></span>

<span data-ttu-id="f069b-111">`condition 1 value`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="f069b-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="f069b-112">Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="f069b-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="f069b-113">Bu bağımsız değişken zorunlu.</span><span class="sxs-lookup"><span data-stu-id="f069b-113">This argument is mandatory.</span></span>

<span data-ttu-id="f069b-114">`condition N range`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="f069b-114">`condition N range`: *String*</span></span>

<span data-ttu-id="f069b-115">Bir ER biçim bileşeninin **toplanan veri anahtarı adı** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="f069b-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="f069b-116">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f069b-116">These additional arguments are optional.</span></span>

<span data-ttu-id="f069b-117">`condition N value`: *Dize*</span><span class="sxs-lookup"><span data-stu-id="f069b-117">`condition N value`: *String*</span></span>

<span data-ttu-id="f069b-118">Bir ER biçim bileşeninin **toplanan veri anahtarı değeri** özelliğinde yapılandırılmış olan ifade tarafından döndürülen değer.</span><span class="sxs-lookup"><span data-stu-id="f069b-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="f069b-119">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="f069b-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f069b-120">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="f069b-120">Return values</span></span>

<span data-ttu-id="f069b-121">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="f069b-121">*Record list*</span></span>

<span data-ttu-id="f069b-122">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="f069b-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f069b-123">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="f069b-123">Usage notes</span></span>

<span data-ttu-id="f069b-124">Bu işlev, **toplanan veri anahtarı adı** ve **Toplanan veri anahtarı değeri** özelliği, ER biçimi bileşeninin **Sıra** bileşeni veya **XML Öğesi** bileşeni için yapılandırılabilir; ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan metin grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="f069b-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="f069b-125">Bu işlev, Geçerli **Ortak\\Dosya** bileşeninin **Çıkış ayrıntılarını topla** seçeneği bayrağı kapatıldığında boş listeye döner.</span><span class="sxs-lookup"><span data-stu-id="f069b-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="f069b-126">`condition range` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f069b-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="f069b-127">`condition value` bağımsız değişkenlerde, " **"\*"** joker karakteri, herhangi bir çoklu karakteri temsil etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f069b-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="f069b-128">Örnek</span><span class="sxs-lookup"><span data-stu-id="f069b-128">Example</span></span>

<span data-ttu-id="f069b-129">Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.</span><span class="sxs-lookup"><span data-stu-id="f069b-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f069b-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="f069b-130">Additional resources</span></span>

[<span data-ttu-id="f069b-131">Veri toplama işlevleri</span><span class="sxs-lookup"><span data-stu-id="f069b-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]