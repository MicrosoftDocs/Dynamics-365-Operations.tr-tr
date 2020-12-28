---
title: LISTDISTINCT ER işlevi
description: Bu konu, LISTDISTINCT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2333cfc21a16a5905acadd590982020fdf878330
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682279"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="7c34b-103">LISTDISTINCT ER İşlevi</span><span class="sxs-lookup"><span data-stu-id="7c34b-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="7c34b-104">`LISTDISTINCT` işlevi, belirtilen listedeki tüm kayıtlar için belirtilen ifadeyi seçici olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="7c34b-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="7c34b-105">Her benzersiz seçici değeri için tek bir kayıt içeren yeni bir *Kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c34b-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c34b-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="7c34b-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="7c34b-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="7c34b-107">Arguments</span></span>

<span data-ttu-id="7c34b-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7c34b-108">`list`: *Record list*</span></span>

<span data-ttu-id="7c34b-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="7c34b-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7c34b-110">`selector`: *Temel veri türü*</span><span class="sxs-lookup"><span data-stu-id="7c34b-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="7c34b-111">Belirtilen listedeki her kayıt için bir seçici değeri hesaplamada kullanılan geçerli bir ifade.</span><span class="sxs-lookup"><span data-stu-id="7c34b-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="7c34b-112">Bu parametre için aşağıdaki veri türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="7c34b-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="7c34b-113">Boole</span><span class="sxs-lookup"><span data-stu-id="7c34b-113">Boolean</span></span>
- <span data-ttu-id="7c34b-114">Date</span><span class="sxs-lookup"><span data-stu-id="7c34b-114">Date</span></span>
- <span data-ttu-id="7c34b-115">Tarih/Saat</span><span class="sxs-lookup"><span data-stu-id="7c34b-115">DateTime</span></span>
- <span data-ttu-id="7c34b-116">GUID</span><span class="sxs-lookup"><span data-stu-id="7c34b-116">GUID</span></span>
- <span data-ttu-id="7c34b-117">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="7c34b-117">Integer</span></span>
- <span data-ttu-id="7c34b-118">Int64</span><span class="sxs-lookup"><span data-stu-id="7c34b-118">Int64</span></span>
- <span data-ttu-id="7c34b-119">Gerçek</span><span class="sxs-lookup"><span data-stu-id="7c34b-119">Real</span></span>
- <span data-ttu-id="7c34b-120">Dize</span><span class="sxs-lookup"><span data-stu-id="7c34b-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="7c34b-121">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="7c34b-121">Return values</span></span>

<span data-ttu-id="7c34b-122">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="7c34b-122">*Record list*</span></span>

<span data-ttu-id="7c34b-123">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="7c34b-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7c34b-124">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="7c34b-124">Usage notes</span></span>

<span data-ttu-id="7c34b-125">Oluşturulan listenin yapısı belirtilen listenin yapısıyla eşleşir.</span><span class="sxs-lookup"><span data-stu-id="7c34b-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="7c34b-126">Belirtilen listedeki birden çok kayıt için aynı seçici değeri hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="7c34b-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="7c34b-127">Bu durumda, oluşturulan listedeki karşılık gelen kaydın alan değerleri, seçici değerinin hesaplandığı belirtilen listedeki ilk kaydın değerleriyle eşittir.</span><span class="sxs-lookup"><span data-stu-id="7c34b-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="7c34b-128">Bu işlevin yürütülmesi, bellekte bulunan *Kayıt listesi* türünün [Elektronik raporlama (ER)](general-electronic-reporting.md) veri kaynağı üzerinde gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="7c34b-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="7c34b-129">**GROUPBY** veri kaynağı, farklı değerleri olan seçicinin hesaplandığı kayıtların listesini oluşturmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7c34b-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="7c34b-130">Ancak, bir performans ve bellek tüketimi açısından, `LISTDISTINCT` işlevini kullanmak **GROUPBY** veri kaynağını kullanmaktan dah aiyidir çünkü işlevi yürütme işlemi bellekte gerçekleştirilie.</span><span class="sxs-lookup"><span data-stu-id="7c34b-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="7c34b-131">Örnek</span><span class="sxs-lookup"><span data-stu-id="7c34b-131">Example</span></span>

<span data-ttu-id="7c34b-132">Aşağıdaki örnekte, belirli bir dönemde en az bir satış faturasının veya proje faturasının düzenlendiği benzersiz müşteri hesabı numaralarının listesini nasıl elde edebileceğiniz gösterilir.</span><span class="sxs-lookup"><span data-stu-id="7c34b-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="7c34b-133">**CustInvoiceJour** uygulama tablosuna başvuran ve belirli bir döneme ait satış faturalarını filtreleyen `Record list` türünün **SalesInvoice** veri kaynağını girin.</span><span class="sxs-lookup"><span data-stu-id="7c34b-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="7c34b-134">Bu veri kaynağının `InvoiceAccount` alanı, faturalandırılmış bir müşterinin hesap numarasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c34b-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="7c34b-135">**ProjInvoiceJour** uygulama tablosuna başvuran ve belirli bir döneme ait proje faturalarını filtreleyen `Record list` türünün **ProjectInvoice** veri kaynağını girin.</span><span class="sxs-lookup"><span data-stu-id="7c34b-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="7c34b-136">Bu veri kaynağının `InvoiceAccount` alanı, faturalandırılmış bir müşterinin hesap numarasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c34b-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="7c34b-137">`LISTJOIN(SalesInvoice, ProjectInvoice)` ifadesini içeren `Calculated field` türünün **AllInvoices** veri kaynağını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7c34b-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="7c34b-138">Bu veri kaynağı, birleştirilmiş satış faturası ve proje faturası listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c34b-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="7c34b-139">`LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` ifadesini içeren `Record list` türünün **InvoicedCustomer** veri kaynağını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="7c34b-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="7c34b-140">Bu veri kaynağı, tanımlanan dönem boyunca faturalanan her benzersiz müşteri için tek bir kayıt içeren yeni bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="7c34b-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="7c34b-141">Bu listenin `InvoiceAccount` alanı bir müşteri hesap numarası içerir.</span><span class="sxs-lookup"><span data-stu-id="7c34b-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c34b-142">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7c34b-142">Additional resources</span></span>

[<span data-ttu-id="7c34b-143">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="7c34b-143">List functions</span></span>](er-functions-category-list.md)
