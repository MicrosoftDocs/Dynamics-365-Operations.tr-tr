---
title: FILTER ER işlevi
description: Bu konu, FILTER Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
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
ms.openlocfilehash: adeefd08531f59e478efbb45ab294b3bc8216f4c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042171"
---
# <a name="FILTER">FILTER ER işlevi</a>

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

## <a name="usage-notes"></a>Kullanım notları

[WHERE](er-functions-list-where.md) işlevinden farklı olarak bu işlev, belirtilen koşul *Tablo kayıtları* türünün herhangi bir Elektronik raporlama (ER) veri kaynağına veritabanı düzeyinde uygulanabilir. Liste ve koşul tablolar ve ilişkiler kullanılarak tanımlanabilir.

Bu işlev için yapılandırılmış olan bir veya her iki bağımsız değişken (`list` ve `condition`) bu isteğin doğrudan SQL aramasına çevrilmesine izin vermiyorsa, tasarım zamanında bir özel durum oluşturulur. Bu özel durum kullanıcıya, veritabanını sorgulamak için `list`veya `condition` kullanılıp kullanlamadığını bildirir.

## <a name="example-1"></a>Örnek 1

**Satıcı**, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, `FILTER (Vendors, Vendors.VendGroup = "40")` ifadesi, yalnızca grup 40'a dahil olan satıcıların listesini döndürür.

## <a name="example-2"></a>Örnek 2

**Satıcı**, VendTable tablosuna başvuran bir ER veri kaynağı olarak yapılandırılırsa ve **parmVendorBankGroup**, *Dize* veri türünde bir değer döndüren ER veri kaynağı olarak yapılandırılırsa, `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` ifadesi yalnızca belirli bir banka grubuna ait satıcı hesaplarının bulunduğu bir liste döndürür.

## <a name="example-3"></a>Örnek 3

*Hesaplanmış alan* türünün **DS** bir veri kaynağını girersiniz ve `SPLIT ("A,B,C", ",")` ifadesini içerir. Daha sonra başka bir ifade girersiniz; `FILTER( DS, DS.Value = "B")`. Bu ifadeyi ER formül tasarımcısında kaydetmeye çalıştığınızda, aşağıdaki özel durum oluşturulur: "doğrulama hatası: FILTER işlevinin liste ifadesi sorgulanabilir değil."

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)
