---
title: ALLITEMSQUERY ER işlevi
description: Bu konu, ALLITEMSQUERY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: 37546fccf804a4522638147d39206997e8c0c24c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745381"
---
# <a name="allitemsquery-er-function"></a>ALLITEMSQUERY ER işlevi

[!include [banner](../includes/banner.md)]

Bu `ALLITEMSQUERY` işlev birleşik bir SQL sorgusu olarak çalışır. Belirtilen yolla eşleşen tüm öğeleri temsil eden bir kayıt listesinden oluşan, yeni bir düzleştirilmiş *kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Bağımsız değişkenler

`path`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu. En az bir ilişki içermesi gerekir.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Yol, *kayıt listesi* veri türünün veri kaynağı öğesine geçerli veri kaynağı yolu olarak tanımlanmalıdır. En az bir ilişki içermesi gerekir. *Dize* yolu ve *tarih* gibi veri öğeleri, elektronik raporlama (ER) ifade oluşturucuda tasarım zamanında hata vermelidir.

Bu işlev SQL kullanılarak doğrudan çağrılabilecek bir uygulama nesnesine başvuran *kayıt listesi* veri türünün veri kaynaklarına (örneğin bir tablo, varlık veya sorgu) uygulandığında, birleştirilmiş bir SQL sorgusu olarak çalışır. Aksi durumda, bellekte [ALLITEMS](er-functions-list-allitems.md) işlevi olarak çalışır.

## <a name="example"></a>Örnek

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- CustInvoiceTable tablosuna başvuran *Tablo kayıtları* türünün **CustInv** veri kaynağı
- `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")` ifadeyi içeren *hesaplanmış alan* türünün **FilteredInv** bir veri kaynağı
- `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)` ifadeyi içeren *hesaplanmış alan* türünün **JourLines** bir veri kaynağı

**JourLines** veri kaynağını çağırmak için model eşlemenizi çalıştırırken aşağıdaki SQL deyimi çalıştırılır:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)
