---
title: LISTOFFIELDS ER işlevi
description: Bu makalede, LISTOFFIELDS Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: c36630280ed351048022bafd4c6f634afd1b1319
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877110"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS ER işlevi

[!include [banner](../includes/banner.md)]

`LISTOFFIELDS` işlev, *numaralandırmanın* veya *konteyner (kayıt)* türünün belirtilen bağımsız değişkeninin yapısına göre oluşturulan bir *kayıt listesi* değeri döndürür.

## <a name="syntax-1"></a>Sözdizimi 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Bağımsız değişkenler

`path`: Veri kaynağı referansı

Aşağıdaki veri tiplerinden birinin veri kaynağının geçerli referans yolu:

- Model numaralandırma
- Biçim numaralandırma
- Uygulama numaralandırma
- Konteyner (kayıt)

`language`: *Dize*

Bir dil kodunu temsil eden metin.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

Oluşturulan liste aşağıdaki alanlara sahip kayıtları içerir:

- **Ad** (*Dize* veri türü)
- **Etiket** (*Dize* veri türü)
- **Açıklama** (*Dize* veri türü)
- **Çevrildi** (*Boole* veri türü)

`path` bağımsız değişken *konteyner (kayıt)* türünün bir veri kaynağına başvuruyorsa, başvurulan konteyner kaydının her alanı için, oluşturulan listeye yeni bir kayıt eklenir. Oluşturulan her kayıt için, **Ad** alanı, geçerli kaydın oluşturulduğu Başvurulmuş konteyner kaydı alanının adını döndürür.

`path` bağımsız değişken *Numaralandırma* türlerinden birinin bir veri kaynağına başvuruyorsa, başvurulan numaralandırmanın her numaralandırma değeri için, oluşturulan listeye yeni bir kayıt eklenir. Oluşturulan her kayıt için, **ad** alanı geçerli kaydın oluşturulduğu Başvurulmuş numaralandırmanın değerini döndürür, **Açıklama** alanı ilgili numaralandırmanın açıklamasını döndürür ve **Etiket** alanı o numaralandırmanın etiketini döndürür.

Çalışma zamanında, sözdizimi 1 kullanıldığında, **Etiket** ve **Açıklama** alanları, çalışmakta olan elektronik raporlama (ER) biçiminin dil ayarlarını temel alan değerler döndürmelidir.

- İstenen dile ait Etiketler ve açıklamalar varsa, **etiket** ve **Açıklama** alanları o dile dayalı olarak değerleri verir ve **Çevrilmiş** alan **doğru** döner.
- İstenen dile ait Etiketler ve açıklamalar yoksa, **etiket** ve **Açıklama** alanları varsayılan **TR-TR** diline dayalı olarak değerleri verir ve **Çevrilmiş** alan **Yanlış** döner.

Çalışma zamanında, sözdizimi 2 kullanıldığında, **Etiket** ve **Açıklama** alanları, sözde işlevin ikinci bağımsız değişkeni olarak tanımlanan dil ayarlarını temel alan değerler döndürmelidir.

- İstenen dile ait Etiketler ve açıklamalar varsa, **etiket** ve **Açıklama** alanları o dile dayalı olarak değerleri verir ve **Çevrilmiş** alan **doğru** döner.
- İstenen dile ait Etiketler ve açıklamalar yoksa, **etiket** ve **Açıklama** alanları **TR-TR** diline dayalı olarak değerleri verir ve **Çevrilmiş** alan **Yanlış** döner.

## <a name="example-1"></a>Örnek 1

Aşağıdaki örnekte, bir ER veri modelinde oluşturulan numaralandırma gösterilmektedir.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Aşağıdaki örnek ayrıntıları göstermektedir:

- Veri kaynağı olarak bir rapora eklenen model numaralandırma.
- Bir ER ifadesi `LISTOFFIELDS` işlevi parametresi olarak bir model numaralandırma kullanır.
- Oluşturulan ER ifadesini kullanarak bir rapora eklenen *kayıt listesi* türünün veri kaynağı.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Aşağıdaki örnek `LISTOFFIELDS` işlevi kullanılarak oluşturulan ve *kayıt listesi* türündeki veri kaynağına bağlı olan ER biçim öğelerini gösterir.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Ana **DOSYA** ve **KLASÖR** biçim öğelerinin dil ayarlarına uygun olarak, etiketler ve açıklamalar için çevrilen metin ER biçiminin çıktısına girilir.

## <a name="example-2"></a>Örnek 2

Örneğin, **enumType** veri modeli numaralandırması için **enumType\_de** ve **enumType\_deCH** veri kaynaklarını yapılandırmak üzere *Hesaplanan alan* veri kaynağı türünü kullanırsınız:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

Bu durumda, bu çevirinin kullanılabilir olması durumunda, numaralandırma değeri etiketiki İsviçre Almancası dilinde almak için aşağıdaki ifadeyi kullanabilirsiniz. İsviçre Almanca çeviri kullanılamıyorsa, Almanca etiketi olur.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]