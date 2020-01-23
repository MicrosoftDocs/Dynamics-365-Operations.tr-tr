---
title: LIST ER işlevi
description: Bu konu, LIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917293"
---
# <span data-ttu-id="2bbc9-103"><a name="LIST">LIST ER işlevi</a></span><span class="sxs-lookup"><span data-stu-id="2bbc9-103"><a name="LIST">LIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bbc9-104">`LIST` işlevi, belirtilen bağımsız değişkenlerden oluşturulmuş yeni listeden oluşan yeni bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bbc9-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="2bbc9-105">Syntax</span></span>

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="2bbc9-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="2bbc9-106">Arguments</span></span>

<span data-ttu-id="2bbc9-107">`record 1`: *Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="2bbc9-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="2bbc9-108">*Kayıt* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="2bbc9-109">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-109">This argument is required.</span></span>

<span data-ttu-id="2bbc9-110">`record N`: *Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="2bbc9-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="2bbc9-111">*Kayıt* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="2bbc9-112">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="2bbc9-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="2bbc9-113">Return values</span></span>

<span data-ttu-id="2bbc9-114">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="2bbc9-114">*Record list*</span></span>

<span data-ttu-id="2bbc9-115">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2bbc9-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="2bbc9-116">Usage notes</span></span>

<span data-ttu-id="2bbc9-117">Oluşturulan listenin yapısı, yalnızca bağımsız değişkenlerde belirtilen her kaydın yapısında sunulan alanları içerir.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="2bbc9-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="2bbc9-118">Example</span></span>

<span data-ttu-id="2bbc9-119">**Konteyner** türünün veri kaynağı *kayıt 1*'i girersiniz.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="2bbc9-120">Bu veri kaynağı, *hesaplanan alan* türünün Aşağıdaki iç içe alanlarını içerir:</span><span class="sxs-lookup"><span data-stu-id="2bbc9-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="2bbc9-121">**Kod:** Bu alan, *dize* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="2bbc9-122">**Tutar:** Bu alan, *Gerçek* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="2bbc9-123">**Konteyner** türünün veri kaynağı *kayıt 2*'i girersiniz.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="2bbc9-124">Bu veri kaynağı, *hesaplanan alan* türünün Aşağıdaki iç içe alanlarını içerir:</span><span class="sxs-lookup"><span data-stu-id="2bbc9-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="2bbc9-125">**Tutar:** Bu alan, *Gerçek* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="2bbc9-126">**IsValid:** Bu alan, *Boole* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="2bbc9-127">Bu durumda, `LIST('Record 1', 'Record 2')` ifade iki kayıt içeren yeni bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="2bbc9-128">Bu listenin yapısı, bu alan, çağrılan işlevin her bir bağımsız değişkeninde sunulan tek alan olduğundan, *gerçek* türün tek bir **tutar** alanından oluşur.</span><span class="sxs-lookup"><span data-stu-id="2bbc9-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2bbc9-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="2bbc9-129">Additional resources</span></span>

[<span data-ttu-id="2bbc9-130">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="2bbc9-130">List functions</span></span>](er-functions-category-list.md)
