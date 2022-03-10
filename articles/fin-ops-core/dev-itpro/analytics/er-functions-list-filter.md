---
title: FILTER ER işlevi
description: Bu konu, FILTER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: e857306574dda7bad5dd25fc7708514997d8e86f
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922435"
---
# <a name="filter-er-function"></a>FILTER ER işlevi

[!include [banner](../includes/banner.md)]

`FILTER` işlev, belirtilen koşula filtre uygulayan bir sorgu değiştirildikten sonra bir *kayıt listesi* değeri olarak belirtilmiş listeyi döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Bağımsız değişkenler

`list`: *Kayıt listesi*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`condition`: *Boole*

Belirtilen listenin kayıtlarını filtrelemek için kullanılan geçerli bir koşullu ifade.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a><a name="usage-notes"></a>Kullanım notları

[WHERE](er-functions-list-where.md) işlevinden farklı olarak bu işlev, belirtilen koşul *Tablo kayıtları* türünün herhangi bir Elektronik raporlama (ER) veri kaynağına veritabanı düzeyinde uygulanabilir. Liste ve koşul tablolar ve ilişkiler kullanılarak tanımlanabilir.

Bu işlev için yapılandırılmış olan bir veya her iki bağımsız değişken (`list` ve `condition`) bu isteğin doğrudan SQL aramasına çevrilmesine izin vermiyorsa, tasarım zamanında bir özel durum oluşturulur. Bu özel durum kullanıcıya, veritabanını sorgulamak için `list`veya `condition` kullanılıp kullanlamadığını bildirir.

> [!NOTE]
> [`VALUEIN`](er-functions-logical-valuein.md) işlevi seçim ölçütünü belirtmek için kullanıldığında, `FILTER` işlevi `WHERE` işlevinden farklı şekilde davranır.
> 
> - `VALUEIN` işlevi `WHERE` işlevinin kapsamında kullanılırsa ve `VALUEIN` ikinci bağımsız değişkeni, kayıt döndürmeyen bir veri kaynağına başvurursa, `VALUEIN` işlevinin döndürdüğü Boolean *[Yanlış](er-formula-supported-data-types-primitive.md#boolean)* değeri kabul edilir. Bu nedenle, **VendGroups** veri kaynağı hiçbir satıcı grubu kaydı döndürmediğinde `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` ifadesi hiçbir satıcı kaydı döndürmez.
> - `VALUEIN` işlevi `FILTER` işlevinin kapsamında kullanılırsa ve `VALUEIN` ikinci bağımsız değişkeni, kayıt döndürmeyen bir veri kaynağına başvurursa, `VALUEIN` işlevinin döndürdüğü Boolean *[Yanlış](er-formula-supported-data-types-primitive.md#boolean)* değeri yoksayılır. Bu nedenle, **VendGroups** veri kaynağı hiçbir satıcı grubu kaydı döndürmezse bile `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` ifadesi **Vendors** veri kaynağının tüm satıcı kayıtlarını döndürür.

## <a name="example-1"></a>Örnek 1

**Satıcı**, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, `FILTER (Vendors, Vendors.VendGroup = "40")` ifadesi, yalnızca grup 40'a dahil olan satıcıların listesini döndürür.

## <a name="example-2"></a>Örnek 2

**Satıcı**, VendTable tablosuna başvuran bir ER veri kaynağı olarak yapılandırılırsa ve **parmVendorBankGroup**, *Dize* veri türünde bir değer döndüren ER veri kaynağı olarak yapılandırılırsa, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` ifadesi yalnızca belirli bir banka grubuna ait satıcı hesaplarının bulunduğu bir liste döndürür.

## <a name="example-3"></a>Örnek 3

*Hesaplanmış alan* türünün **DS** bir veri kaynağını girersiniz ve `SPLIT ("A,B,C", ",")` ifadesini içerir. Daha sonra başka bir ifade girersiniz; `FILTER( DS, DS.Value = "B")`. Bu ifadeyi ER formül tasarımcısında kaydetmeye çalıştığınızda, aşağıdaki özel durum oluşturulur: "doğrulama hatası: FILTER işlevinin liste ifadesi sorgulanabilir değil."

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
