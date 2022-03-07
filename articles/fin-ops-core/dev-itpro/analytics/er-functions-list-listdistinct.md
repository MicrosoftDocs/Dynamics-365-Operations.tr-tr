---
title: LISTDISTINCT ER işlevi
description: Bu konu, LISTDISTINCT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 7/30/2020
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
ms.openlocfilehash: 7cc51695d261a63521ae88e2a9362b6f30b9618ed89300bcaeb606b050c81350
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735586"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT ER İşlevi

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`LISTDISTINCT` işlevi, belirtilen listedeki tüm kayıtlar için belirtilen ifadeyi seçici olarak hesaplar. Her benzersiz seçici değeri için tek bir kayıt içeren yeni bir *Kayıt listesi* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`selector`: *Temel veri türü*

Belirtilen listedeki her kayıt için bir seçici değeri hesaplamada kullanılan geçerli bir ifade.

Bu parametre için aşağıdaki veri türleri desteklenir:

- Boole
- Date
- Tarih/Saat
- GUID
- Tamsayı
- Int64
- Gerçek
- Dize

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Oluşturulan listenin yapısı belirtilen listenin yapısıyla eşleşir.

Belirtilen listedeki birden çok kayıt için aynı seçici değeri hesaplanabilir. Bu durumda, oluşturulan listedeki karşılık gelen kaydın alan değerleri, seçici değerinin hesaplandığı belirtilen listedeki ilk kaydın değerleriyle eşittir.

Bu işlevin yürütülmesi, bellekte bulunan *Kayıt listesi* türünün [Elektronik raporlama (ER)](general-electronic-reporting.md) veri kaynağı üzerinde gerçekleştirilir.

**GROUPBY** veri kaynağı, farklı değerleri olan seçicinin hesaplandığı kayıtların listesini oluşturmak için de kullanılabilir. Ancak, bir performans ve bellek tüketimi açısından, `LISTDISTINCT` işlevini kullanmak **GROUPBY** veri kaynağını kullanmaktan dah aiyidir çünkü işlevi yürütme işlemi bellekte gerçekleştirilie.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, belirli bir dönemde en az bir satış faturasının veya proje faturasının düzenlendiği benzersiz müşteri hesabı numaralarının listesini nasıl elde edebileceğiniz gösterilir.

1. **CustInvoiceJour** uygulama tablosuna başvuran ve belirli bir döneme ait satış faturalarını filtreleyen `Record list` türünün **SalesInvoice** veri kaynağını girin.

    Bu veri kaynağının `InvoiceAccount` alanı, faturalandırılmış bir müşterinin hesap numarasını döndürür.

2. **ProjInvoiceJour** uygulama tablosuna başvuran ve belirli bir döneme ait proje faturalarını filtreleyen `Record list` türünün **ProjectInvoice** veri kaynağını girin.

    Bu veri kaynağının `InvoiceAccount` alanı, faturalandırılmış bir müşterinin hesap numarasını döndürür.

3. `LISTJOIN(SalesInvoice, ProjectInvoice)` ifadesini içeren `Calculated field` türünün **AllInvoices** veri kaynağını yapılandırın.

    Bu veri kaynağı, birleştirilmiş satış faturası ve proje faturası listesini döndürür.

4. `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)` ifadesini içeren `Record list` türünün **InvoicedCustomer** veri kaynağını yapılandırın.

    Bu veri kaynağı, tanımlanan dönem boyunca faturalanan her benzersiz müşteri için tek bir kayıt içeren yeni bir liste döndürür. Bu listenin `InvoiceAccount` alanı bir müşteri hesap numarası içerir.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]