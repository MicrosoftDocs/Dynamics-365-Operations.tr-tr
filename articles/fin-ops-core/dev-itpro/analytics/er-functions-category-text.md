---
title: Metin kategorisindeki ER işlevlerinin listesi
description: Bu makalede, Elektronik raporlama (ER) uygulamasında desteklenen metin işlevleri hakkında bilgi sağlanmaktadır.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 502a68d51705114adc096a1cd2217210f4e925bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885557"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Metin kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

*Dize* veri türünün veri kaynakları üzerinde işlem gerçekleştirmek için elektronik raporlama (ER) metin işlevleri kullanılabilir. Bu makale, bu işlevlerin özetini sunmaktadır.

## <a name="list-of-supported-functions"></a>Desteklenen işlevler listesi

| İşlev | Tanım |
|----------|-------------|
| [Char](er-functions-text-char.md) | Bu işlev, belirtilen Unicode sayısı tarafından başvurulan tek bir karakteri gösteren bir *dize* değeri döndürür. |
| [Art arda eklemek](er-functions-text-concatenate.md) | Bu işlev, bir dizeye katıldıktan sonra, belirtilen tüm metin dizelerini bir *Dize* değeri olarak döndürür. |
| [Biçim](er-functions-text-format.md) | Bu işlevi, belirtilen dizeyi, tüm **%N** oluşumlarını *N*'ci bağımsız değişken ile değiştirerek biçimlendirdikten sonra *Dize* değeri olarak döndürür. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Bu işlevi, belirtilen numaralandırma veri kaynağındaki belirli bir *Enum* değerini *dize* değeri olarak belirtilen numaralandırma adını kullanarak arar. *Numaralama* değeri bulunursa, işlev bunu döndürür. |
| [GetLabelText](er-functions-text-getlabeltext.md) | Bu işlev, belirtilen bir etiketin belirtilen dilde çevirisini temsil eden bir *[Dize](er-formula-supported-data-types-primitive.md#string)* değeri döndürmek için belirli bir etiketi arar. |
| [GuidValue](er-functions-text-guidvalue.md) | Bu işlevi, belirtilen *Dize* veri türündeki girişi *GUID* veri türünde bir veri öğesine dönüştürür. |
| [JsonValue](er-functions-text-jsonvalue.md) | Bu işlevi, verileri, belirtilen koda göre skaler bir değer çıkarmak için belirtilen yolla erişilen JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırın. Sonra da bir *dize* değeri olarak ayıklanan skalar değeri döndürür. |
| [Sola](er-functions-text-left.md) | Bu işlev belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür. |
| [Len](er-functions-text-len.md) | Bu işlev, belirtilen dizedeki karakter sayısını bir *tamsayı* değeri olarak döndürür. |
| [Lower](er-functions-text-lower.md) | Bu işlev, küçük harflere dönüştürüldükten sonra bir *dize* değeri olarak belirtilen metin dizesini döndürür. |
| [Mid](er-functions-text-mid.md) | Bu işlev belirtilen pozisyondan başlayarak belirtilen dizenin başından itibaren belirtilen sayıda karakteri gösteren bir *[Dize](er-formula-supported-data-types-primitive.md#string)* değeri döndürür. |
| [NewGUID](er-functions-text-newguid.md) | Bu işlev, yeni oluşturulan bir *[GUID](er-formula-supported-data-types-primitive.md#guid)* değerini döndürür. |
| [NumberFormat](er-functions-text-numberformat.md) | Bu işlev, belirli bir tarih değerini belirtilen biçimde ve isteğe bağlı olarak belirtilen kültür içinde belirtilen sayıyı gösteren bir *dize* değeri döndürür. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Bu işlevi belirtilen sayıyı bir *dize* değeri olarak (metin dizelerine dönüştürüldükten sonra) belirtilen dilde yazılmış şekilde döndürür. |
| [PadLeft](er-functions-text-padleft.md) | Bu işlevi, belirtilen dizenin başlangıcının belirtilen karakterlerin bir veya daha fazlasıyla doldurulduğu belirtilen uzunlukta bir *dize* döndürür. |
| [QrCode](er-functions-text-qrcode.md) | Bu işlev, belirtilen dizgi için hızlı yanıt kodu (QR kodu) görüntüsünü ikili biçimde gösteren bir *konteyner* değeri döndürür. |
| [Değiştir](er-functions-text-replace.md) | Bu işlev, belirtilen metin dizesini bir bütün veya bir kısmı başka bir dizeyle değiştirildikten sonra *dize* değeri olarak döndürür. |
| [Sağa](er-functions-text-right.md) | Bu işlevi belirtilen dizenin sonundan itibaren belirtilen sayıda karakteri gösteren bir *dize* değeri döndürür. |
| [Metin](er-functions-text-text.md) | Bu işlevi, belirtilen giriş geçerli uygulama örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrildikten sonra bleirtilen sayıyı *dize* değeri olarak döndürür. |
| [Çevir](er-functions-text-translate.md) | Bu işlev, başka bir karakter kümesi için belirtilen metnin karakterlere değiştirilmesi sonucunu içeren bir *Dize* değeri döndürür. |
| [Trim](er-functions-text-trim.md) | Bu işlev, sekme, satır başı, satır beslemesi ve form besleme karakterlerinin yerine tek bir boşluk karakteriyle konulduktan sonra, baştaki ve sondaki boşlukların kesildikten sonra ve sözcüklerin arasındaki birden çok boşluk kaldırıldığında bir *Dize* değeri olarak belirtilen metin dizesini döndürür. |
| [Upper](er-functions-text-upper.md) | Bu işlev, büyük harflere dönüştürüldükten sonra bir *dize* değeri olarak belirtilen metin dizesini döndürür. |

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlamada formül dili](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
