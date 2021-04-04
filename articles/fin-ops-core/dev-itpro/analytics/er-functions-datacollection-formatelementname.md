---
title: FORMATELEMENTNAME ER işlevi
description: Bu konu, FORMATELEMENTNAME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561314"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="b299f-103">FORMATELEMENTNAME ER işlevi</span><span class="sxs-lookup"><span data-stu-id="b299f-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b299f-104">`FORMATELEMENTNAME` işlev, geçerli ER biçim öğesinin adını gösteren bir *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="b299f-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="b299f-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="b299f-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="b299f-106">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="b299f-106">Return values</span></span>

<span data-ttu-id="b299f-107">*Dize*</span><span class="sxs-lookup"><span data-stu-id="b299f-107">*String*</span></span>

<span data-ttu-id="b299f-108">Sonuç metin değeri.</span><span class="sxs-lookup"><span data-stu-id="b299f-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b299f-109">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="b299f-109">Usage notes</span></span>

<span data-ttu-id="b299f-110">Bu işlev, ER biçimi bileşeninin **toplanan veri anahtarı adı** ve **Toplanan veri anahtarı değeri** özelliği için yapılandırılmış ER ifadelerinde, **Çıktı ayrıntılarını topla** seçeneğinin açık olduğu **ortak\\dosya** bileşeni altında bulunan **metin** grubundan çağrılabilir.</span><span class="sxs-lookup"><span data-stu-id="b299f-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="b299f-111">Örnek</span><span class="sxs-lookup"><span data-stu-id="b299f-111">Example</span></span>

<span data-ttu-id="b299f-112">Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için [ER Sayma ve toplama için çıktı biçiminde verileri kullanma](tasks/er-format-counting-summing-1.md) görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun.</span><span class="sxs-lookup"><span data-stu-id="b299f-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b299f-113">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b299f-113">Additional resources</span></span>

[<span data-ttu-id="b299f-114">Veri toplama işlevleri</span><span class="sxs-lookup"><span data-stu-id="b299f-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]