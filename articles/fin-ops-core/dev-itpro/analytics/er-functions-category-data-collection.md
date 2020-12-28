---
title: Veri toplama kategorisindeki ER işlevlerinin listesi
description: Bu konu, elektronik raporlama (ER) uygulamasında desteklenen veri toplama işlevleri hakkında bilgi sağlar.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686305"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="07548-103">Veri toplama kategorisindeki ER işlevlerinin listesi</span><span class="sxs-lookup"><span data-stu-id="07548-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07548-104">Elektronik raporlama (ER) veri toplama işlevleri, daha önce **metin** veya **XML** biçiminde oluşturulmuş çıktının verilerine dayalı olarak, çalıştırılmakta olan bir er biçimini saymak ve toplamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="07548-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="07548-105">Bu yaklaşım, çalıştırılan bir ER biçiminin performansını artırmaya yardımcı olmak, oluşturulan belgelerde çalışan toplam değerleri girmek ve başka amaçlar için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="07548-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="07548-106">Bu konu, bu işlevlerin özetini sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="07548-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="07548-107">Desteklenen işlevler listesi</span><span class="sxs-lookup"><span data-stu-id="07548-107">List of supported functions</span></span>

| <span data-ttu-id="07548-108">İşlev</span><span class="sxs-lookup"><span data-stu-id="07548-108">Function</span></span> | <span data-ttu-id="07548-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="07548-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="07548-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="07548-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="07548-111">Bu işlev, bir biçim öğesi için **toplanan veri anahtarı değeri** özelliği tarafından döndürülen ve Format ögeleri çalıştırma biçimi sırasında ve belirtilen koşullara uyan bir giden belge oluşturmak için kullanıldığında toplanan değerlerin listesini içeren bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="07548-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="07548-112">Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="07548-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="07548-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="07548-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="07548-114">Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşula uyuyan Biçim öğelerinin sayısını temsil eden bir *tamsayı* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="07548-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="07548-115">Koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="07548-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="07548-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="07548-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="07548-117">Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşullara uyuyan Biçim öğelerinin sayısını temsil eden bir *tamsayı* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="07548-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="07548-118">Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="07548-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="07548-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="07548-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="07548-120">Bu işlev, geçerli ER biçim öğesinin adını gösteren bir *Dize* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="07548-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="07548-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="07548-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="07548-122">Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşula uyuyan Biçim öğelerinin sayısını temsil eden bir *Gerçek* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="07548-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="07548-123">Koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="07548-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="07548-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="07548-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="07548-125">Bu işlev, biçim ögeleri çalışma biçimi sırasında bir giden belge oluşturmak için kullanıldığında ve belirtilen koşullara uyuyan Biçim öğelerinin sayısını temsil eden bir *Gerçek* değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="07548-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="07548-126">Her koşul bir anahtar aralığı ve bir anahtar değerinden oluşur.</span><span class="sxs-lookup"><span data-stu-id="07548-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="07548-127">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="07548-127">Additional resources</span></span>

[<span data-ttu-id="07548-128">Elektronik Raporlamaya genel bakış</span><span class="sxs-lookup"><span data-stu-id="07548-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="07548-129">Elektronik raporlamada formül tasarımcısı</span><span class="sxs-lookup"><span data-stu-id="07548-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="07548-130">Elektronik raporlamada formül dili</span><span class="sxs-lookup"><span data-stu-id="07548-130">Electronic reporting formula language</span></span>](er-formula-language.md)
