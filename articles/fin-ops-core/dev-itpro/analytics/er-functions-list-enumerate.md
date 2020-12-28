---
title: ENUMERATE ER işlevi
description: Bu konu, ENUMERATE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 34ebbec94644276be4ef9beb1c77638606dd37a0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679474"
---
# <a name="enumerate-er-function"></a><span data-ttu-id="176a9-103">ENUMERATE ER işlevi</span><span class="sxs-lookup"><span data-stu-id="176a9-103">ENUMERATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="176a9-104">Bu `ENUMERATE` işlevi, belirtilen listenin numaralandırılmış kayıtlarından oluşan yeni bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="176a9-104">The `ENUMERATE` function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="176a9-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="176a9-105">Syntax</span></span>

```vb
ENUMERATE (list)
```

## <a name="arguments"></a><span data-ttu-id="176a9-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="176a9-106">Arguments</span></span>

<span data-ttu-id="176a9-107">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="176a9-107">`list`: *Record list*</span></span>

<span data-ttu-id="176a9-108">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="176a9-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="176a9-109">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="176a9-109">Return values</span></span>

<span data-ttu-id="176a9-110">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="176a9-110">*Record list*</span></span>

<span data-ttu-id="176a9-111">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="176a9-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="176a9-112">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="176a9-112">Usage notes</span></span>

<span data-ttu-id="176a9-113">Döndürülen numaralandırılmış kayıtların listesi aşağıdaki ek öğeleri sunar:</span><span class="sxs-lookup"><span data-stu-id="176a9-113">The list of enumerated records that is returned exposes the following additional elements:</span></span>

- <span data-ttu-id="176a9-114">Alanlar kaydı (**Değer** bileşeni)</span><span class="sxs-lookup"><span data-stu-id="176a9-114">The record of fields (**Value** component)</span></span>
- <span data-ttu-id="176a9-115">Geçerli kayıt dizini (**Numara** bileşeni)</span><span class="sxs-lookup"><span data-stu-id="176a9-115">The current record index (**Number** component)</span></span>

## <a name="example"></a><span data-ttu-id="176a9-116">Örnek</span><span class="sxs-lookup"><span data-stu-id="176a9-116">Example</span></span>

<span data-ttu-id="176a9-117">Aşağıdaki örnekte, **Numaralandırılan** veri kaynağı, VendTable tablosuna başvuran **Satıcılar** veri kaynağındaki satıcı kayıtlarının numaralandırılmış bir listesi olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="176a9-117">In the following illustration, an **Enumerated** data source is created as an enumerated list of vendor records from the **Vendors** data source that refers to the VendTable table.</span></span>

<a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>

<span data-ttu-id="176a9-118">Aşağıdaki şekil, elektronik raporlama (ER) biçimi gösterir.</span><span class="sxs-lookup"><span data-stu-id="176a9-118">The following illustration shows the Electronic reporting (ER) format.</span></span> <span data-ttu-id="176a9-119">Bu biçimde, veri bağlamaları XML biçiminde çıktı üretmek için oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="176a9-119">In this format, data bindings are created to generate output in XML format.</span></span> <span data-ttu-id="176a9-120">Bu çıktı ayrı ayrı satıcıları numaralandırılmış düğümler olarak gösterir.</span><span class="sxs-lookup"><span data-stu-id="176a9-120">This output presents individual vendors as enumerated nodes.</span></span>

<a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a>

<span data-ttu-id="176a9-121">Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.</span><span class="sxs-lookup"><span data-stu-id="176a9-121">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>

## <a name="additional-resources"></a><span data-ttu-id="176a9-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="176a9-122">Additional resources</span></span>

[<span data-ttu-id="176a9-123">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="176a9-123">List functions</span></span>](er-functions-category-list.md)
