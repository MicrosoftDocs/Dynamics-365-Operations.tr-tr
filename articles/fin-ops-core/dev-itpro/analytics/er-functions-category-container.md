---
title: Konteyner kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen konteyner işlevleri hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561770"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="45836-103">Konteyner kategorisindeki ER işlevlerinin listesi</span><span class="sxs-lookup"><span data-stu-id="45836-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45836-104">*Konteyner* veri türünün veri kaynaklarını içeren işlemler gerçekleştirmek için [Elektronik raporlama (ER)](general-electronic-reporting.md) konteyner [işlevleri](er-formula-language.md#functions) kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="45836-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="45836-105">Bu işlemler, işleme verileri ikili büyük nesne (BLOB) biçimindeki bir ikili veri koleksiyonunu temsil ettiğinde gerçekleşir.</span><span class="sxs-lookup"><span data-stu-id="45836-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="45836-106">Bu konu, bu işlevlerin özetini sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="45836-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="45836-107">Desteklenen işlevler listesi</span><span class="sxs-lookup"><span data-stu-id="45836-107">List of supported functions</span></span>

| <span data-ttu-id="45836-108">İşlev</span><span class="sxs-lookup"><span data-stu-id="45836-108">Function</span></span> | <span data-ttu-id="45836-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="45836-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="45836-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="45836-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="45836-111">Bu işlev, ikiliden metne kodlama şemalarının Base64 grubunu temsil eden belirtilmiş ASCII dizesinden çözümlenen ikili içerikten oluşan *Konteyner* değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="45836-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="45836-112">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="45836-112">Additional resources</span></span>

[<span data-ttu-id="45836-113">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="45836-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="45836-114">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="45836-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="45836-115">Elektronik raporlamada formül dili</span><span class="sxs-lookup"><span data-stu-id="45836-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]