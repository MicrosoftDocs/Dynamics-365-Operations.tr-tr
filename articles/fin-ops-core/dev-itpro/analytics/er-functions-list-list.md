---
title: LIST ER işlevi
description: Bu konu, LIST Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563860"
---
# <a name="list-er-function"></a><span data-ttu-id="d065d-103">LIST ER işlevi</span><span class="sxs-lookup"><span data-stu-id="d065d-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d065d-104">`LIST` işlevi, belirtilen bağımsız değişkenlerden oluşturulmuş yeni listeden oluşan yeni bir *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="d065d-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="d065d-105">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="d065d-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="d065d-106">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="d065d-106">Arguments</span></span>

<span data-ttu-id="d065d-107">`record 1`: *Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="d065d-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="d065d-108">*Kayıt* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="d065d-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="d065d-109">Bu bağımsız değişken gereklidir.</span><span class="sxs-lookup"><span data-stu-id="d065d-109">This argument is required.</span></span>

<span data-ttu-id="d065d-110">`record N`: *Konteyner (kayıt)*</span><span class="sxs-lookup"><span data-stu-id="d065d-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="d065d-111">*Kayıt* veri türünün veri kaynağına yönelik referans.</span><span class="sxs-lookup"><span data-stu-id="d065d-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="d065d-112">Bu ek bağımsız değişkenler isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="d065d-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="d065d-113">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="d065d-113">Return values</span></span>

<span data-ttu-id="d065d-114">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="d065d-114">*Record list*</span></span>

<span data-ttu-id="d065d-115">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="d065d-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d065d-116">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="d065d-116">Usage notes</span></span>

<span data-ttu-id="d065d-117">Oluşturulan listenin yapısı, yalnızca bağımsız değişkenlerde belirtilen her kaydın yapısında sunulan alanları içerir.</span><span class="sxs-lookup"><span data-stu-id="d065d-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="d065d-118">Örnek</span><span class="sxs-lookup"><span data-stu-id="d065d-118">Example</span></span>

<span data-ttu-id="d065d-119">**Konteyner** türünün veri kaynağı *kayıt 1*'i girersiniz.</span><span class="sxs-lookup"><span data-stu-id="d065d-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="d065d-120">Bu veri kaynağı, *hesaplanan alan* türünün Aşağıdaki iç içe alanlarını içerir:</span><span class="sxs-lookup"><span data-stu-id="d065d-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="d065d-121">**Kod:** Bu alan, *dize* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="d065d-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="d065d-122">**Tutar:** Bu alan, *Gerçek* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="d065d-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="d065d-123">**Konteyner** türünün veri kaynağı *kayıt 2*'i girersiniz.</span><span class="sxs-lookup"><span data-stu-id="d065d-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="d065d-124">Bu veri kaynağı, *hesaplanan alan* türünün Aşağıdaki iç içe alanlarını içerir:</span><span class="sxs-lookup"><span data-stu-id="d065d-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="d065d-125">**Tutar:** Bu alan, *Gerçek* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="d065d-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="d065d-126">**IsValid:** Bu alan, *Boole* türünde bir değer döndüren bir ifade içerir.</span><span class="sxs-lookup"><span data-stu-id="d065d-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="d065d-127">Bu durumda, `LIST('Record 1', 'Record 2')` ifade iki kayıt içeren yeni bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="d065d-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="d065d-128">Bu listenin yapısı, bu alan, çağrılan işlevin her bir bağımsız değişkeninde sunulan tek alan olduğundan, *gerçek* türün tek bir **tutar** alanından oluşur.</span><span class="sxs-lookup"><span data-stu-id="d065d-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d065d-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d065d-129">Additional resources</span></span>

[<span data-ttu-id="d065d-130">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="d065d-130">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]