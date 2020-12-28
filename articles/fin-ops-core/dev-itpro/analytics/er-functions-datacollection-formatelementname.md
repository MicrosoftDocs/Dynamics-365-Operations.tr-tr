---
title: FORMATELEMENTNAME ER işlevi
description: Bu konu, FORMATELEMENTNAME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: ef59bb44a7096f4c095ce37a89558a717748f02e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685339"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="ec5d6-103">FORMATELEMENTNAME ER işlevi</span><span class="sxs-lookup"><span data-stu-id="ec5d6-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec5d6-104">`FORMATELEMENTNAME` işlev, geçerli ER biçim öğesinin adını gösteren bir *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec5d6-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="ec5d6-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="ec5d6-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="ec5d6-106">Return values</span></span>

<span data-ttu-id="ec5d6-107">*Dize*</span><span class="sxs-lookup"><span data-stu-id="ec5d6-107">*String*</span></span>

<span data-ttu-id="ec5d6-108">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec5d6-109">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="ec5d6-109">Usage notes</span></span>

<span data-ttu-id="ec5d6-110">Bu işlev, ER biçimi bileşeninin **toplanan veri anahtarı adı** ve **Toplanan veri anahtarı değeri** özelliği için yapılandırılmış ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan **metin** grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="ec5d6-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="ec5d6-111">Example</span></span>

<span data-ttu-id="ec5d6-112">Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.</span><span class="sxs-lookup"><span data-stu-id="ec5d6-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec5d6-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ec5d6-113">Additional resources</span></span>

[<span data-ttu-id="ec5d6-114">Veri toplama işlevleri</span><span class="sxs-lookup"><span data-stu-id="ec5d6-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
