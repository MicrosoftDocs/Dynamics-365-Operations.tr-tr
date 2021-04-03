---
title: ALLITEMSQUERY ER işlevi
description: Bu konu, ALLITEMSQUERY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 56ac956cdfe28d282b8a80d7caec34a50eca5dbe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559615"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="19656-103">ALLITEMSQUERY ER işlevi</span><span class="sxs-lookup"><span data-stu-id="19656-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19656-104">Bu `ALLITEMSQUERY` işlev birleşik bir SQL sorgusu olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="19656-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="19656-105">Belirtilen yolla eşleşen tüm öğeleri temsil eden bir kayıt listesinden oluşan, yeni bir düzleştirilmiş *kayıt listesi* değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="19656-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="19656-106">Sözdizimi</span><span class="sxs-lookup"><span data-stu-id="19656-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="19656-107">Bağımsız değişkenler</span><span class="sxs-lookup"><span data-stu-id="19656-107">Arguments</span></span>

<span data-ttu-id="19656-108">`path`: *Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="19656-108">`path`: *Record list*</span></span>

<span data-ttu-id="19656-109">*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.</span><span class="sxs-lookup"><span data-stu-id="19656-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="19656-110">En az bir ilişki içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="19656-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="19656-111">Dönüş değerleri</span><span class="sxs-lookup"><span data-stu-id="19656-111">Return values</span></span>

<span data-ttu-id="19656-112">*Kayıt listesi*</span><span class="sxs-lookup"><span data-stu-id="19656-112">*Record list*</span></span>

<span data-ttu-id="19656-113">Oluşturulan kayıt listesi.</span><span class="sxs-lookup"><span data-stu-id="19656-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="19656-114">Kullanım notları</span><span class="sxs-lookup"><span data-stu-id="19656-114">Usage notes</span></span>

<span data-ttu-id="19656-115">Yol, *kayıt listesi* veri türünün veri kaynağı öğesine geçerli veri kaynağı yolu olarak tanımlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="19656-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="19656-116">En az bir ilişki içermesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="19656-116">It must also contain at least one relation.</span></span> <span data-ttu-id="19656-117">*Dize* yolu ve *tarih* gibi veri öğeleri, elektronik raporlama (ER) ifade oluşturucuda tasarım zamanında hata vermelidir.</span><span class="sxs-lookup"><span data-stu-id="19656-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="19656-118">Bu işlev SQL kullanılarak doğrudan çağrılabilecek bir uygulama nesnesine başvuran *kayıt listesi* veri türünün veri kaynaklarına (örneğin bir tablo, varlık veya sorgu) uygulandığında, birleştirilmiş bir SQL sorgusu olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="19656-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="19656-119">Aksi durumda, bellekte [ALLITEMS](er-functions-list-allitems.md) işlevi olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="19656-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="19656-120">Örnek</span><span class="sxs-lookup"><span data-stu-id="19656-120">Example</span></span>

<span data-ttu-id="19656-121">Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:</span><span class="sxs-lookup"><span data-stu-id="19656-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="19656-122">CustInvoiceTable tablosuna başvuran *Tablo kayıtları* türünün **CustInv** veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="19656-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="19656-123">`FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` ifadeyi içeren *hesaplanmış alan* türünün **FilteredInv** bir veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="19656-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="19656-124">`ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` ifadeyi içeren *hesaplanmış alan* türünün **JourLines** bir veri kaynağı</span><span class="sxs-lookup"><span data-stu-id="19656-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="19656-125">**JourLines** veri kaynağını çağırmak için model eşlemenizi çalıştırırken aşağıdaki SQL deyimi çalıştırılır:</span><span class="sxs-lookup"><span data-stu-id="19656-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="19656-126">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="19656-126">Additional resources</span></span>

[<span data-ttu-id="19656-127">Liste işlevleri</span><span class="sxs-lookup"><span data-stu-id="19656-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]