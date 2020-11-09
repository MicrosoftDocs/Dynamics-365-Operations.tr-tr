---
title: Plaka etiketleri için belge yönlendirme düzeni
description: Bu konu, etiketlere değer yazdırmak için biçimlendirme yöntemlerinin nasıl kullanılacağını açıklar.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 8c96aef5d66ed8f8c44d74eee9b60f0a7d38a46d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017725"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Plaka etiketleri için belge yönlendirme düzeni

[!include [banner](../includes/banner.md)]

Belge yönlendirme düzeni, plaka etiketlerinin düzenini ve bunlar üzerine yazdırılan verileri tanımlar. Mobil cihaz menü öğelerini ve iş şablonlarını ayarlarken, yazdırma tetikleme noktalarını yapılandırırsınız.

Tipik bir senaryoda, ambar teslim alma görevlileri, teslim alma alanına gelen paletlerin içeriklerini kaydettikten hemen sonra plaka etiketlerini yazdırır. Fiziksel etiketler paletlere uygulanır. Bunlar daha sonra, sonraki yerine koyma işlemi ve gelecekteki giden malzeme çekme işlemlerinin bir parçası olarak doğrulama için kullanılabilir.

Yazdırma cihazının gönderilen metni yorumlayabilmesi koşuluyla, çok karmaşık Etiketler yazdırabilirsiniz. Örneğin, barkod içeren bir Zebra Programlama Dili (ZPL) düzeni aşağıdaki örneğe benzeyebilir.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Etiket yazdırma işleminin bir parçası olarak bu örnekteki `$LicensePlateId$` metni bir veri değeriyle değiştirilecektir.

Yazdırılacak değerleri görmek için **Ambar yönetimi \> Sorgular ve raporlar \>Plaka etiketleri** 'ne gidin.

Birçok yaygın kullanılan etiket oluşturma aracı, etiket düzenine ilişkin metni biçimlendirmenize yardımcı olabilir. Bu araçların çoğu `$FieldName$` biçimini destekler. Ek olarak, Microsoft Dynamics 365 Supply Chain Management, belge yönlendirme düzenine için alan eşlemesinin bir parçası olarak özel biçimlendirme mantığı kullanır.

## <a name="custom-number-formats"></a>Özel sayı biçimleri

Aşağıdaki biçime sahip kodlar kullanarak yazdırılan sayısal alan değerlerinin biçimlendirmesini özelleştirebilirsiniz.

```dos
$FieldName:FormatString$
```

Bu biçim için bir açıklama aşağıda verilmiştir:

- `FieldName` veri alanının adıdır (örneğin, **Miktar** ).
- `FormatString` verilerin nasıl yazdırılması gerektiğini tanımlar.

Aşağıdaki örneklerde iş miktarı ( **Miktar** ) alanının nasıl özelleştirilebileceği gösterilmektedir:

- Her zaman dört basamağı göstermek için (sıfırları yer tutucular olarak kullanarak), `$Qty:0000$` kullanın. Örneğin, miktar 10 ise, etiket "0010" olarak görünür.
- Her zaman iki ondalık basamak göstermek için `$Qty:0.00$` kullanın. Örneğin, miktar 10 ise, etiket "10,00" olarak görünür.

Kullanılabilir sayı biçimi dizelerinin tam listesi için bkz. [Özel sayı biçimlendirme dizeleri](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Özel dize biçimleri

Aşağıdaki alan ve biçim kodunu kullanarak bir dizenin ilk karakterlerini kaldırabilirsiniz.

```dos
$FieldName:#..$
```

Burada, `#` atlanacak karakter sayısını belirtir. Örneğin, ilk iki karakteri içermeyen bir Seri Sevkiyat Konteyner Kodu (SSCC) plaka numarası yazdırmak için `$LicensePlateId:2..$` kullanın. Bu durumda, lisans plaka numarası 0011111111111222221 "11111111111222221" olarak yazdırılacaktır.

## <a name="custom-datetime-formats"></a>Özel tarih/saat biçimleri

Aşağıdaki örnek, tarihleri yazdırmak için kullanılan biçimi nasıl denetleyebileceğinizi gösterir.

```dos
$PrintedDate:dd-MM-yyyy$
```

Bu örnekte, 30 Nisan 2020 tarihi "30-04-2020" olarak yazdırılacaktır.

Kullanılabilir tarih/saat biçimlerinin tam listesi için bkz. [Özel tarih ve saat biçimlendirme dizeleri](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Çok satırlı verilerden ayrı ayrı satırlar yazdırma

Bir veri alanı birden çok satır içeriyorsa (yani, satır sonları ile ayrılmış satırlar), aşağıdaki biçimi kullanarak tek bir satırı yazdırabilirsiniz.

```dos
$FieldName[#]$
```

Burada, `#` yazdırmak istediğiniz satır numarasıdır. (İlk satır için 1 kullanın.)

Örneğin, sisteminizde aşağıdaki çok satırlı adresi depolayan `AdditionalAddress` bir alan vardır:

Contoso Inc.  
123 Cadde Adı  
Bir Şehir, Bir Eyalet

Aşağıdaki kodları kullanarak, bir seferde bir satır olmak üzere bu adresi yazdırabilirsiniz.

| Kod | Yazdırılan metin |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | 123 Cadde Adı |
| `$AdditionalAddress[3]$` | Bir Şehir, Bir Eyalet |

## <a name="print-and-format-from-a-display-method"></a>Bir görüntüleme yönteminden yazdırma ve biçimlendirme

Aşağıdaki biçimi kullanarak bir görüntüleme yönteminden yazdırma yapabilirsiniz.

```dos
$DisplayMethod()$
```

Bu biçimi, bu konunun önceki kısımlarında açıklanan diğer türlerle birleştirebilirsiniz. Örneğin, `DisplayListOfItemsNumbers()` bir görüntüleme yönteminiz var ve bu yöntemin ilk öğe numarasını yazdırmak istiyorsunuz. Bu durumda, aşağıdaki kodu kullanabilirsiniz.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Etiketlerin nasıl yazdırılacağı hakkında daha fazla bilgi

Etiketlerin nasıl ayarlanacağı ve yazdırılacağı hakkında daha fazla bilgi için bkz. [Plaka etiketi yazdırmayı etkinleştirme](tasks/license-plate-label-printing.md).
