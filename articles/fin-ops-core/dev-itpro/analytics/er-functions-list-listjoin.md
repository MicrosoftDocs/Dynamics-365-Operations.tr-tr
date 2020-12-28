---
title: LISTJOIN ER işlevi
description: Bu konu, LISTJOIN Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28f03e5e6af0f252a994f2e54b57a5ef654f4e67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682255"
---
# <a name="listjoin-er-function"></a><span data-ttu-id="08499-103">LISTJOIN ER işlevi</span><span class="sxs-lookup"><span data-stu-id="08499-103">LISTJOIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08499-104">`LISTJOIN` işlevi, belirtilen bağımsız değişkenlerden oluşturulmuş yeni birleştirilmiş kayıt listesini temsil eden yeni bir *Kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="08499-104">The `LISTJOIN` function returns a *Record list* value that represents a new joined list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="08499-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="08499-105">Syntax</span></span>

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a><span data-ttu-id="08499-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="08499-106">Arguments</span></span>

<span data-ttu-id="08499-107">`list 1`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="08499-107">`list 1`: *Record list*</span></span>

<span data-ttu-id="08499-108">*Kayıt listesi* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="08499-108">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="08499-109">Bu bağımsız değişken zorunlu.</span><span class="sxs-lookup"><span data-stu-id="08499-109">This argument is mandatory.</span></span>

<span data-ttu-id="08499-110">`list N`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="08499-110">`list N`: *Record list*</span></span>

<span data-ttu-id="08499-111">*Kayıt listesi* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="08499-111">A reference to a data source of the *Record list* data type.</span></span> <span data-ttu-id="08499-112">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="08499-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="08499-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="08499-113">Return values</span></span>

<span data-ttu-id="08499-114">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="08499-114">*Record list*</span></span>

<span data-ttu-id="08499-115">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="08499-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="08499-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="08499-116">Usage notes</span></span>

<span data-ttu-id="08499-117">Oluşturulan listenin yapısı, yalnızca bağımsız değişkenlerde başvurulan her kayıt listesinin yapısında sunulan alanları içerir.</span><span class="sxs-lookup"><span data-stu-id="08499-117">The structure of the list that is created contains only the fields that are present in the structure of every record list that is referenced in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="08499-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="08499-118">Example</span></span>

<span data-ttu-id="08499-119">`Container` türünün veri kaynağı **Kayıt 1**'i girersiniz.</span><span class="sxs-lookup"><span data-stu-id="08499-119">You enter data source **Record 1** of the `Container` type.</span></span> <span data-ttu-id="08499-120">Bu veri kaynağı, `Calculated field` türünün aşağıdaki iç içe geçmiş alanlarını içerir:</span><span class="sxs-lookup"><span data-stu-id="08499-120">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="08499-121">**Kod**: Bu alan, `String` türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="08499-121">**Code**: This field contains an expression that returns a value of the `String` type.</span></span>
- <span data-ttu-id="08499-122">**Tutar**: Bu alan, `Real` türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="08499-122">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>

<span data-ttu-id="08499-123">Sonra, `Container` türünün veri kaynağı **Kayıt 2**'yi girersiniz.</span><span class="sxs-lookup"><span data-stu-id="08499-123">You then enter data source **Record 2** of the `Container` type.</span></span> <span data-ttu-id="08499-124">Bu veri kaynağı, `Calculated field` türünün aşağıdaki iç içe geçmiş alanlarını içerir:</span><span class="sxs-lookup"><span data-stu-id="08499-124">This data source contains the following nested fields of the `Calculated field` type:</span></span>

- <span data-ttu-id="08499-125">**Tutar**: Bu alan, `Real` türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="08499-125">**Amount**: This field contains an expression that returns a value of the `Real` type.</span></span>
- <span data-ttu-id="08499-126">**IsValid**: Bu alan, `Boolean` türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="08499-126">**IsValid**: This field contains an expression that returns a value of the `Boolean` type.</span></span>

![ER model eşleme tasarımcısı sayfası](./media/er-functions-list-listjoin-image1.gif)

<span data-ttu-id="08499-128">Bu durumda, `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` ifade iki kayıt içeren yeni bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="08499-128">In this case, the expression `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` returns a new list that contains two records.</span></span>

![İki kayıt bulunan ER model eşleme tasarımcısı sayfası](./media/er-functions-list-listjoin-image2.gif)

<span data-ttu-id="08499-130">Bu listenin yapısı, bu alan çağrılan işlevin her bir bağımsız değişkeninde sunulan tek alan olduğundan, `Real` türününü tek bir **Tutar** alanından oluşur.</span><span class="sxs-lookup"><span data-stu-id="08499-130">The structure of this list consists of a single **Amount** field of the `Real` type, because this field is the only field that is presented in every argument of the called function.</span></span>

![ER model eşleme tasarımcısı sayfası miktar alanı](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a><span data-ttu-id="08499-132">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="08499-132">Additional resources</span></span>

[<span data-ttu-id="08499-133">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="08499-133">List functions</span></span>](er-functions-category-list.md)

[<span data-ttu-id="08499-134">Veri akışı ve dönüşümünü analiz etmek için yürütülen bir ER biçiminin veri kaynaklarında hata ayıklama</span><span class="sxs-lookup"><span data-stu-id="08499-134">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>](er-debug-data-sources.md)
