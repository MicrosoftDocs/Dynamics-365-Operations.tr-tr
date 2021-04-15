---
title: LISTDISTINCT ER işlevi
description: Bu konu, LISTDISTINCT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9ab9354b0fdb1c08c192b90e6bab303cb85ea41a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743835"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="8b87e-103">LISTDISTINCT ER İşlevi</span><span class="sxs-lookup"><span data-stu-id="8b87e-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="8b87e-104">`LISTDISTINCT` işlevi, belirtilen listedeki tüm kayıtlar için belirtilen ifadeyi seçici olarak hesaplar.</span><span class="sxs-lookup"><span data-stu-id="8b87e-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="8b87e-105">Her benzersiz seçici değeri için tek bir kayıt içeren yeni bir *Kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b87e-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b87e-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="8b87e-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="8b87e-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="8b87e-107">Arguments</span></span>

<span data-ttu-id="8b87e-108">`list`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="8b87e-108">`list`: *Record list*</span></span>

<span data-ttu-id="8b87e-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="8b87e-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="8b87e-110">`selector`: *Temel veri türü*</span><span class="sxs-lookup"><span data-stu-id="8b87e-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="8b87e-111">Belirtilen listedeki her kayıt için bir seçici değeri hesaplamada kullanılan geçerli bir ifade.</span><span class="sxs-lookup"><span data-stu-id="8b87e-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="8b87e-112">Bu parametre için aşağıdaki veri türleri desteklenir:</span><span class="sxs-lookup"><span data-stu-id="8b87e-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="8b87e-113">Boole</span><span class="sxs-lookup"><span data-stu-id="8b87e-113">Boolean</span></span>
- <span data-ttu-id="8b87e-114">Date</span><span class="sxs-lookup"><span data-stu-id="8b87e-114">Date</span></span>
- <span data-ttu-id="8b87e-115">Tarih/Saat</span><span class="sxs-lookup"><span data-stu-id="8b87e-115">DateTime</span></span>
- <span data-ttu-id="8b87e-116">GUID</span><span class="sxs-lookup"><span data-stu-id="8b87e-116">GUID</span></span>
- <span data-ttu-id="8b87e-117">Tamsayı</span><span class="sxs-lookup"><span data-stu-id="8b87e-117">Integer</span></span>
- <span data-ttu-id="8b87e-118">Int64</span><span class="sxs-lookup"><span data-stu-id="8b87e-118">Int64</span></span>
- <span data-ttu-id="8b87e-119">Gerçek</span><span class="sxs-lookup"><span data-stu-id="8b87e-119">Real</span></span>
- <span data-ttu-id="8b87e-120">Dize</span><span class="sxs-lookup"><span data-stu-id="8b87e-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="8b87e-121">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="8b87e-121">Return values</span></span>

<span data-ttu-id="8b87e-122">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="8b87e-122">*Record list*</span></span>

<span data-ttu-id="8b87e-123">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="8b87e-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8b87e-124">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="8b87e-124">Usage notes</span></span>

<span data-ttu-id="8b87e-125">Oluşturulan listenin yapısı belirtilen listenin yapısıyla eşleşir.</span><span class="sxs-lookup"><span data-stu-id="8b87e-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="8b87e-126">Belirtilen listedeki birden çok kayıt için aynı seçici değeri hesaplanabilir.</span><span class="sxs-lookup"><span data-stu-id="8b87e-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="8b87e-127">Bu durumda, oluşturulan listedeki karşılık gelen kaydın alan değerleri, seçici değerinin hesaplandığı belirtilen listedeki ilk kaydın değerleriyle eşittir.</span><span class="sxs-lookup"><span data-stu-id="8b87e-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="8b87e-128">Bu işlevin yürütülmesi, bellekte bulunan *Kayıt listesi* türünün [Elektronik raporlama (ER)](general-electronic-reporting.md) veri kaynağı üzerinde gerçekleştirilir.</span><span class="sxs-lookup"><span data-stu-id="8b87e-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="8b87e-129">**GROUPBY** veri kaynağı, farklı değerleri olan seçicinin hesaplandığı kayıtların listesini oluşturmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8b87e-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="8b87e-130">Ancak, bir performans ve bellek tüketimi açısından, `LISTDISTINCT` işlevini kullanmak **GROUPBY** veri kaynağını kullanmaktan dah aiyidir çünkü işlevi yürütme işlemi bellekte gerçekleştirilie.</span><span class="sxs-lookup"><span data-stu-id="8b87e-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="8b87e-131">Örnek</span><span class="sxs-lookup"><span data-stu-id="8b87e-131">Example</span></span>

<span data-ttu-id="8b87e-132">Aşağıdaki örnekte, belirli bir dönemde en az bir satış faturasının veya proje faturasının düzenlendiği benzersiz müşteri hesabı numaralarının listesini nasıl elde edebileceğiniz gösterilir.</span><span class="sxs-lookup"><span data-stu-id="8b87e-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="8b87e-133">**CustInvoiceJour** uygulama tablosuna başvuran ve belirli bir döneme ait satış faturalarını filtreleyen `Record list` türünün **SalesInvoice** veri kaynağını girin.</span><span class="sxs-lookup"><span data-stu-id="8b87e-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="8b87e-134">Bu veri kaynağının `InvoiceAccount` alanı, faturalandırılmış bir müşterinin hesap numarasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b87e-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="8b87e-135">**ProjInvoiceJour** uygulama tablosuna başvuran ve belirli bir döneme ait proje faturalarını filtreleyen `Record list` türünün **ProjectInvoice** veri kaynağını girin.</span><span class="sxs-lookup"><span data-stu-id="8b87e-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="8b87e-136">Bu veri kaynağının `InvoiceAccount` alanı, faturalandırılmış bir müşterinin hesap numarasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b87e-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="8b87e-137">`LISTJOIN(SalesInvoice, ProjectInvoice)` ifadesini içeren `Calculated field` türünün **AllInvoices** veri kaynağını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="8b87e-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="8b87e-138">Bu veri kaynağı, birleştirilmiş satış faturası ve proje faturası listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b87e-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="8b87e-139">`LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` ifadesini içeren `Record list` türünün **InvoicedCustomer** veri kaynağını yapılandırın.</span><span class="sxs-lookup"><span data-stu-id="8b87e-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="8b87e-140">Bu veri kaynağı, tanımlanan dönem boyunca faturalanan her benzersiz müşteri için tek bir kayıt içeren yeni bir liste döndürür.</span><span class="sxs-lookup"><span data-stu-id="8b87e-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="8b87e-141">Bu listenin `InvoiceAccount` alanı bir müşteri hesap numarası içerir.</span><span class="sxs-lookup"><span data-stu-id="8b87e-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b87e-142">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="8b87e-142">Additional resources</span></span>

[<span data-ttu-id="8b87e-143">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="8b87e-143">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]