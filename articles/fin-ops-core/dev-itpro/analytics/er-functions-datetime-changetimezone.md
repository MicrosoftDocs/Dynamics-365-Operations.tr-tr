---
title: CHANGETIMEZONE ER işlevi
description: Bu makalede, CHANGETIMEZONE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: be94f57cfcb6115ea386a279c379662f7d401d11
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903599"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER işlevi

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE` işlevi, Eşgüdümlü evrensel saatdeki (Greenwich saati \[GMT\]) belirli bir tarih/saat değerinden bir tarih/saat değerine dönüştürülmüş bir *[Tarih Saat](er-formula-supported-data-types-primitive.md#datetime)* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Bağımsız değişkenler

`datetime`: *TarihSaat*

Eşgüdümlü Evrensel Saat dilimindeki, dönüştürülecek tarih/saat değerini gösteren bir tarih/saat değeri.

`base time zone`: *[Dize](er-formula-supported-data-types-primitive.md#string)*

Dönüştürme öncesinde belirli bir tarih/saat değerinin kaydırılacağı saat diliminin adı.

`target time zone`: *Dize*

Dönüştürme sırasında belirli bir tarih/saat değerinin dönüştürüleceği saat diliminin adı.

## <a name="return-values"></a>Dönüş değerleri

*Tarih/Saat*

Eşgüdümlü evrensel saat dilimindeki sonuçta elde edilen tarih/saat değeri.

## <a name="usage-notes"></a>Kullanım notları

Kaynak ve hedef saat dilimlerini belirtmek için, [İnternet Atanmış Numaralar Yetkilisi (IANA)](https://www.iana.org/) tarafından [sağlanan](https://data.iana.org/time-zones/releases/) veya Microsoft Windows tarafından [desteklenen](/windows-hardware/manufacture/desktop/default-time-zones) saat dilimi adlarını kullanabilirsiniz.

Sağlanan ad IANA listesinde veya Windows kayıt defterinde bulunmazsa, çalışma zamanında "Saat dilimi '\<time zone name\>' durumu yok" durumu görüntülenir.

Yaz saatinin gözlendiği saat dilimleri için dönüştürme, Eşgüdümlü Evrensel Saat yaz saati farkını dikkate alır. Bu farktan elde edilen en son bilgiler dönüştürme sırasında kullanılır.

## <a name="example-1"></a>Örnek 1

Bu örnekte, Windows için saat dilimi adları kullanılır.

**Hesaplanan alan** türünün **DSX** veri kaynağını yapılandırırsınız. Aşağıdaki ifadeyi içerir.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

**Hesaplanan alan** türünün **DSY** veri kaynağının ifadesini `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` olarak yapılandırırsanız, **DSX** veri kaynağı şu metni döndürür: **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Bu metin, 1 Haziran'da sağlanan iki saat dilimi arasındaki saat farkının 24 saatten fazla olduğunu gösterir. Bu nedenle, ana saat dilimi hedef saat diliminin önünde olduğundan, dönüştürülmüş tarih/saat değeri verilen tarih/saat değerinden bir gün öncedir.

**Hesaplanan alan** türünün **DSY** veri kaynağının ifadesini `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` olarak yapılandırırsanız, **DSX** veri kaynağı şu metni döndürür: **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Bu metin, 1 Aralık'ta sağlanan iki saat dilimi arasındaki saat farkının 24 saatten az olduğunu gösterir. Bu nedenle, dönüştürülmüş tarih/saat değeri verilen tarih/zaman değerine eşittir.

> [!NOTE]
> Aynı saat dilimlerinde sağlanan saat dilimlerinde farklı bir Eşgüdümlü Evrensel Saat yaz saati farkı gözlemlendiği için, aynı zaman dilimi çiftinde verilen ve dönüştürülmüş tarih/saat değerleri arasında farklı bir fark geri döner.

## <a name="example-2"></a>Örnek 2

Bu örnekte, IANA saat dilimi adları kullanılır.

**Hesaplanan alan** türünün **DSX** veri kaynağını yapılandırırsınız. Aşağıdaki ifadeyi içerir.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

**Hesaplanan alan** türünün **DSY** veri kaynağının ifadesini `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` olarak yapılandırırsanız, **DSX** veri kaynağı şu metni döndürür: **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Bu metin, 1 Haziran'da sağlanan iki saat dilimi arasındaki saat farkının 24 saatten fazla olduğunu gösterir. Bu nedenle, ana saat dilimi hedef saat diliminin önünde olduğundan, dönüştürülmüş tarih/saat değeri verilen tarih/saat değerinden bir gün öncedir.

**Hesaplanan alan** türünün **DSY** veri kaynağının ifadesini `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` olarak yapılandırırsanız, **DSX** veri kaynağı şu metni döndürür: **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Bu metin, 1 Aralık'ta sağlanan iki saat dilimi arasındaki saat farkının 24 saatten az olduğunu gösterir. Bu nedenle, dönüştürülmüş tarih/saat değeri verilen tarih/zaman değerine eşittir.

## <a name="example-3"></a>Örnek 3

**Hesaplanan alan** türünün **DSX** veri kaynağını yapılandırırsınız. Aşağıdaki ifadeyi içerir.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

**Hesaplanan alan** türünün **DSY** veri kaynağının ifadesini `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")` olarak yapılandırırsanız, **DSX** veri kaynağı şu metni döndürür: **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Bu metin, 1 Haziran'da sağlanan iki saat dilimi arasındaki saat farkının 24 saatten fazla olduğunu gösterir. Bu nedenle, hedef saat dilimi hedef ana diliminin önünde olduğundan, dönüştürülmüş tarih/saat değeri verilen tarih/saat değerinden bir gün sonradır.

## <a name="example-4"></a>Örnek 4

Bir dış kaynaktan saat dilimi bilgisi içermeyen metin olarak bir tarih/saat damgası alabilirsiniz. Ancak, kaynağın çalıştığı saat dilimini bilmeyebilirsiniz. Örneğin, İspanya'da çalışan bir hizmetle ilgili tarih/zaman damgası olarak **01/12/2021 12:55:00** alırsınız. Bu tarih/zaman değerini veritabanına doğru şekilde kaydetmek için aşağıdaki dönüştürmeyi tamamlayın:

- **Hesaplanan alan** türünün **DSY** veri kaynağını, metinden Eşgüdümlü Evrensel Saat tarih/saat değerine dönüştürecek şekilde yapılandırın.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- **Hesaplanan alan** türünün **DSX** veri kaynağını, harici kaynağın saat diliminin tarih/saat değeri olarak dönüştürülen tarih/saat değerini Eşgüdümlü Evrensel Saat olacak şekilde yapılandırın.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Tarih/zaman dönüştürme için `CHANGETIMEZONE` işlevini kullandığınızda, veritabanında herhangi bir tarih/saat değerinin Eşgüdümlü Evrensel Saat dilimindeki değer olarak depolandığını unutmayın. Bu değerin uygulama sayfalarında sunulabilmesi için, bunlar dönüştürülür. Dönüşüm, şu anda oturum açmış olan uygulama kullanıcısı için tercih edilen bölge olarak [ayarlanan](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) saat dilimini dikkate alır.

## <a name="additional-resources"></a>Ek kaynaklar

[Tarih ve saat işlevleri](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
