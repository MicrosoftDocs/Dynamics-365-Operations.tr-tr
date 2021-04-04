---
title: SPLITLISTBYLIMIT ER işlevi
description: Bu konu, SPLITLISTBYLIMIT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 119ad3c363913ddaf3d6b890e36989d03e91b3c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565116"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="e2ab2-103">SPLITLISTBYLIMIT ER işlevi</span><span class="sxs-lookup"><span data-stu-id="e2ab2-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2ab2-104">`SPLITLISTBYLIMIT` işlev belirtilen listeyi yeni bir alt listeler listesine (toplu işlemler) böler.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="e2ab2-105">Her toplu işteki kayıt sayısı dinamik olarak hesaplanır.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="e2ab2-106">Bu işlev, Sonra sonucu, toplu işlemlerden oluşan yeni *bir kayıt listesi* değeri olarak döndürür.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ab2-107">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="e2ab2-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="e2ab2-108">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="e2ab2-108">Arguments</span></span>

<span data-ttu-id="e2ab2-109">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="e2ab2-109">`list`: *Record list*</span></span>

<span data-ttu-id="e2ab2-110">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e2ab2-111">`limit value`: *Tamsayı* veya *Gerçek*</span><span class="sxs-lookup"><span data-stu-id="e2ab2-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="e2ab2-112">Orijinal listeyi toplu işlemlere Bölmek için kullanılan maksimum sınır değeri.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="e2ab2-113">`limit source`: *Alan*</span><span class="sxs-lookup"><span data-stu-id="e2ab2-113">`limit source`: *Field*</span></span>

<span data-ttu-id="e2ab2-114">*Tamsayı* veya *Gerçek* veri alanının geçerli yolu belirtilen listeyi yazın.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="e2ab2-115">Bu alanın değeri, toplam toplamın artmakta olduğu adımı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="e2ab2-116">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="e2ab2-116">Return values</span></span>

<span data-ttu-id="e2ab2-117">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="e2ab2-117">*Record list*</span></span>

<span data-ttu-id="e2ab2-118">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e2ab2-119">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="e2ab2-119">Usage notes</span></span>

<span data-ttu-id="e2ab2-120">Aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:</span><span class="sxs-lookup"><span data-stu-id="e2ab2-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="e2ab2-121">**Değer**: *liste*</span><span class="sxs-lookup"><span data-stu-id="e2ab2-121">**Value**: *List*</span></span>

    <span data-ttu-id="e2ab2-122">Geçerli toplu işe ait kayıtların listesi.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="e2ab2-123">**Batchnumber**: *tam sayı*</span><span class="sxs-lookup"><span data-stu-id="e2ab2-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="e2ab2-124">Döndürülen listedeki geçerli toplu iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="e2ab2-125">Sınır kaynağı tanımlanan sınırı aştığında sınır, kaynak listedeki tek bir öğeye uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="e2ab2-126">Örnek</span><span class="sxs-lookup"><span data-stu-id="e2ab2-126">Example</span></span>

<span data-ttu-id="e2ab2-127">Aşağıdaki şekil, elektronik raporlama (ER) biçimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="e2ab2-128">Aşağıdaki şekilde, biçim için kullanılan veri kaynakları gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="e2ab2-129">Aşağıdaki örnekte biçim çalıştırıldığında elde edilen sonuç gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="e2ab2-130">Bu durumda, çıktı emtia maddelerinin düz listesi olur.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="e2ab2-131">Aşağıdaki örneklerde, tek bir toplu iş 9 limitini geçmemesi gereken toplam ağırlığa sahip emtiaları içerdiğinde, emtia maddelerinin listesini toplu işlerde ayarlananla aynı biçimde gösterir.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="e2ab2-132">Aşağıdaki örnekte düzeltilen biçim çalıştırıldığında elde edilen sonuç gösterilir.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="e2ab2-133">Sınırının kaynak (**ağırlık**) değeri (**11**) tanımlanan sınırı (**9**) geçtiğinden sınır, kaynak listedeki son maddeye uygulanmaz.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="e2ab2-134">Rapor oluşturma sırasında alt listeleri yok saymak için, gerekirse `WHERE` işlevini veya ilgili biçim öğesinin **Etkinleştirildi** ifadesini kullanın.</span><span class="sxs-lookup"><span data-stu-id="e2ab2-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2ab2-135">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="e2ab2-135">Additional resources</span></span>

[<span data-ttu-id="e2ab2-136">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="e2ab2-136">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]