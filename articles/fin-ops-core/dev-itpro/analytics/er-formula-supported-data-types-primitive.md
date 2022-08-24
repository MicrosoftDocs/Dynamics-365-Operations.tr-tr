---
title: Elektronik raporlama formülleri için desteklenen temel veri türleri
description: Bu makalede, Elektronik raporlama (ER) formüllerinde desteklenen temel veri türleri hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 06/02/2021
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 26c166744e1705baa9dcce6b93c76f110524b7d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284589"
---
# <a name="supported-primitive-data-types-for-electronic-reporting-formulas"></a>Elektronik raporlama formülleri için desteklenen temel veri türleri

[!include [banner](../includes/banner.md)]

Bu makalede, [Elektronik raporlama (ER)](general-electronic-reporting.md) ifadelerinde desteklenen temel veri türleri hakkında bilgi sağlanmaktadır. Temel veri türlerinin bir listesi aşağıda verilmiştir:

- [boole](#boolean)
- [tarih](#date)
- [tarih saat](#datetime)
- [numaralandırma](#enumeration)
- [guid](#guid)
- [tamsayı](#integer)
- [int64](#int64)
- [gerçek](#real)
- [dize](#string)

## <a name="boolean"></a><a name="boolean"></a>Boole

*Boole* temel veri türü, *doğru* ya da *yanlış* olarak değerlendirilen bir değer içerir. Bir *boole* deyiminin beklenildiği yerlerde, **Doğru** ve **Yanlış** anahtar sözcüklerini kullanabilirsiniz. Varsayılan değer *yanlış* değeridir.

Bir *boole*'nin iç gösterimi bir *tamsayıdır*. *Tamsayı* değeri 0 (sıfır) *yanlış* olarak değerlendirilir ve diğer tüm *tamsayı* değerleri *doğru* olarak değerlendirilir. [ER formül tasarımcısında](er-advanced-formula-editor.md) *boole* döndüren konfigüre edilmiş bir ifadeyi [doğruladığınızda](general-electronic-reporting-formula-designer.md#TestFormula), bir ifade *yanlış* döndürdüğünde test sonucu bölmesi *0* (sıfır) gösterir. Aksi durumda, test sonucu bölmesi *1* gösterir.

*Boole*, örtük dönüştürme içermez. Ancak, *boole*'yi *dizeye* açıkça dönüştürmek için [TEXT](er-functions-text-text.md) işlevini kullanabilirsiniz:

- *yanlış* değeri, **Yanlış** metin dizesine dönüştürülür.
- *doğru* değeri, **Doğru** metin dizesine dönüştürülür.

> [!NOTE]
> Bu dönüştürme, sağlanan dile ve kültür [bağlamına](er-design-multilingual-reports.md) bağlı değildir.

Karşılaştırma [operatörleri](er-formula-language.md#Operators), *boole* veri türü ile kullanılabilen tek operatör türüdür. Aşağıdaki operatörler, iki *boole* değerini karşılaştırmak için kullanılabilir: \<\> ve =.

## <a name="date"></a><a name="date"></a>Date

*tarih* temel veri tipi gün, ay ve yıl bilgisini saklar. Tarihler, aşağıdaki işlevler kullanılarak başlatılabilir:

- [DATEVALUE](er-functions-datetime-datevalue.md)
- [NULLDATE](er-functions-datetime-nulldate.md)
- [SESSIONTODAY](er-functions-datetime-sessiontoday.md)
- [TODAY](er-functions-datetime-today.md)

*Tarih* veri türü 1 Ocak 1900 ve 31 Aralık 2154 arasında tarih içerebilir. Varsayılan değer **null**'dur ve dahili gösterim 1 Ocak 1900 tarihidir.

*Tarih*, örtük dönüştürme içermez. Ancak, aşağıdaki açık dönüştürme işlevlerini kullanabilirsiniz:

- [DATEFORMAT](er-functions-datetime-dateformat.md)
- [DATETODATETIME](er-functions-datetime-datetodatetime.md)
- [TEXT](er-functions-text-text.md)

[ADDDAYS](er-functions-datetime-adddays.md) işlevi, tarihlerden gün eklemenizi ve çıkarmanızı sağlar. Bu şekilde, tarihi belirli bir gün olarak geleceğe ve geçmişe taşıyabilirsiniz. [DAYS](er-functions-datetime-days.md) işlevi, tarihleri birbiriden çıkarmanızı ve gün cinsinden farkı hesaplamanızı sağlar. *Kayıt* değerlerinin dönüşümü hakkında daha fazla bilgi için bkz. [Tarih ve saat kategorisinde ER işlevlerinin listesi](er-functions-category-datetime.md).

Karşılaştırma [operatörleri](er-formula-language.md#Operators), *tarih* veri türü ile kullanılabilen tek operatör türüdür. Aşağıdaki operatörler, iki *tarih* değerini karşılaştırmak için kullanılabilir: \<\>, \<, \<=, =, \> ve \>=.

## <a name="datetime"></a><a name="datetime"></a>Datetime

*tarih saat* temel veri türü, *tar,h* türünü ve gece yarısından itibaren geçen zamanı gösteren bir değeri birleştirir. Süre; saat, dakika, saniye ve saniyenin kesirleri cinsinden gösterilir. *tarih saat* değeri ayrıca saat dilimi hakkındaki bilgileri de içerir.

*tarih saat* veri türü, 1 Ocak 1900 (iki yönlü [biçimde](/dotnet/standard/base-types/standard-date-and-time-format-strings) 1900-01-01T00:00:00.0000000+00:00 arasında tarihler olabilir) ve 31 Aralık 2154 (iki yönlü biçimde 2154/12/31T11:59:59.9999999+00:00) arasında tarihleri tutabilir. *tarih saat*'deki en küçük zaman birimi, bir saniyenin on milyonda biridir.

> [!NOTE]
> **hh** [tanımlayıcısı](/dotnet/standard/base-types/standard-date-and-time-format-strings) saat için kullanıldığında, 12:59:59:9999999 değerinin üstündeki saat değerleri geçerli saat olarak yorumlanamaz.
>
> **HH** tanımlayıcısı saat için kullanıldığında, 23:59:59:9999999 değerinin üstündeki saat değerleri geçerli saat olarak yorumlanamaz.

Varsayılan değer **null**'dur ve dahili gösterim 1 Ocak 1900'dür (iki yönlü biçimde 1900-01-01T00:00:00.0000000+00:00).

Tarih saatler, aşağıdaki işlevler kullanılarak başlatılabilir:

- [DATETIMEVALUE](er-functions-datetime-datetimevalue.md)
- [NULNULLDATETIMELDATE](er-functions-datetime-nulldatetime.md)
- [SESSIONNOW](er-functions-datetime-sessionnow.md)
- [NOW](er-functions-datetime-now.md)

*tarih saat*, örtük dönüştürme içermez. Ancak, aşağıdaki açık dönüştürme işlevlerini kullanabilirsiniz:

- [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md)
- [TEXT](er-functions-text-text.md)

*tarih saat* değerlerinin dönüşümü hakkında daha fazla bilgi için bkz. [Tarih ve saat kategorisinde ER işlevlerinin listesi](er-functions-category-datetime.md).

Karşılaştırma [operatörleri](er-formula-language.md#Operators), *tarih saat* veri türü ile kullanılabilen tek operatör türüdür. Aşağıdaki operatörler, iki *tarih saat* değerini karşılaştırmak için kullanılabilir: \<\>, \<, \<=, =, \> ve \>=.

## <a name="enumeration"></a><a name="enumeration"></a>Numaralandırma

*Numaralandırma* temel veri türü, bir harfler listesidir. Uygulama [kaynak kodunda](../dev-ref/xpp-data-primitive.md#enum) tanımlanan numaralandırmaları kullanabilirsiniz. Ayrıca, ER veri modeli ve ER biçimi bileşenlerinde kendi numaralandırmalarınızı da oluşturabilirsiniz.

Bir uygulama *numaralandırması*, herhangi bir ER model eşleme ve ER biçimi ifadelerinde kullanılabilir.

Aşağıdaki görsel, **CustVendCorrectiveReasonCode** model numaralandırmasını düzenlenebilir ER veri modeline nasıl ekleyebileceğinizi gösterir.

[![ER veri modeli tasarımcısında model numaralandırması yapılandırma.](./media/er-formula-supported-data-types-primitive-enum1.gif)](./media/er-formula-supported-data-types-primitive-enum1.gif)

Model *numaralandırması*, *numaralandırmanın* bulunduğu bir veri modeli altında oluşturulmuş bir ER model eşleme ve ER biçimi ifadelerinde kullanılabilir.

Aşağıdaki görsel, **Natura tersine çevirme masrafı alt kategorileri** biçim numaralandırmasını düzenlenebilir ER biçimine nasıl ekleyebileceğinizi gösterir.

[![ER biçim tasarımcısında biçim numaralandırması yapılandırma.](./media/er-formula-supported-data-types-primitive-enum2.gif)](./media/er-formula-supported-data-types-primitive-enum2.gif)

Bir biçim *numaralandırması* yalnızca *numaralandırmanın* yerine getirilen ER biçiminin ifadelerinde kullanılabilir.

Belirli bir numaralandırmayı yapılandırılmış bir ER bileşenine sabit değer olarak veya bir ER çözümü çalıştıran kullanıcının çalışma zamanı iletişim kutusunda tanımladığı bir değer olarak getirmek için uygun sayıda ER veri kaynağı türünü kullanmalısınız.

- Uygulama numaralandırmalarına **Dynamics 365 for Operations \ Numaralandırma** ve **Genel \ Kullanıcı girdi parametreleri** veri kaynaklarından erişebilirsiniz. Aşağıdaki görsel, **NoYes** uygulama numaralandırmasına başvuran **appenumNoYes** ve **uipNoYes** veri kaynaklarını düzenlenebilir bir ER biçimine nasıl ekleyebileceğinizi gösterir.

    [![ER biçim tasarımcısında uygulama numaralandırma veri kaynakları ekleme.](./media/er-formula-supported-data-types-primitive-enum3a.gif)](./media/er-formula-supported-data-types-primitive-enum3a.gif)

- Veri modeli numaralandırmalarına **Veri modeli \ Numaralandırma** ve **Veri modeli \ Kullanıcı giriş parametreleri** veri kaynaklarını kullanılarak erişebilirsiniz. Aşağıdaki görsel, **CustVendCorrectiveReasonCode** veri modeli numaralandırmasına başvuran **CustVendCorrectiveReasonCode** veri kaynaklarını düzenlenebilir bir ER biçimine nasıl ekleyebileceğinizi gösterir.

    [![ER biçim tasarımcısında model numaralandırma veri kaynakları ekleme.](./media/er-formula-supported-data-types-primitive-enum3b.gif)](./media/er-formula-supported-data-types-primitive-enum3b.gif)

- Biçim numaralandırmalarına **Biçim \ Numaralandırma** ve **Biçim \ Kullanıcı giriş parametreleri** veri kaynaklarını kullanılarak erişebilirsiniz. Aşağıdaki görsel, **Natura tersine çevirme masrafı alt kategorileri** veri modeli numaralandırmasına başvuran **NaturaReverseCharge** veri kaynaklarını düzenlenebilir bir ER biçimine nasıl ekleyebileceğinizi gösterir.

    [![ER biçim tasarımcısında biçim numaralandırma veri kaynakları ekleme.](./media/er-formula-supported-data-types-primitive-enum3c.gif)](./media/er-formula-supported-data-types-primitive-enum3c.gif)

*numaralandırma*, örtük dönüştürme içermez. Ancak, bir *numaralandırmayı* metin dizesine dönüştürmek için [TEXT](er-functions-text-text.md) dönüştürme işlevini kullanabilirsiniz. Bu dönüştürme dile bağlı değildir. *numaralandırma* değerini uygun dile özgü etiketlerle nasıl ilişkilendirebileceğinizi öğrenmek için, [LISTOFFIELDS](er-functions-list-listoffields.md) ve [GETENUMVALUEBYNAME](er-functions-text-getenumvaluebyname.md) işlevleriyle ilgili kullanım örneklerine bakın.

Karşılaştırma [operatörleri](er-formula-language.md#Operators), *numaralandırma* veri türü ile kullanılabilen tek operatör türüdür. Aşağıdaki operatörler, iki *numaralandırma* değerini karşılaştırmak için kullanılabilir: \<\> ve =.

## <a name="guid"></a><a name="guid"></a>Guid

*guid* temel veri türü, bir genel benzersiz tanımlayıcı (GUID) değeri içerir. GUID, benzersiz bir tanımlayıcının gerekli olduğu yerlerde, tüm bilgisayarlarda ve ağlarda kullanılabilen bir değerdir. Sayının tekrarlanması oldukça düşük bir ihtimaldir. Geçerli bir GUID aşağıdaki özellikleri karşılar:

- 32 onaltılık basamak olmalıdır.
- Ayrıca, aşağıdaki konumlara yerleştirilmiş dört tire karakteri olmalıdır: 8-4-4-4-12.
- Ayrıca, isteğe bağlı ayraçlar \{\} dizenin başında ve sonunda eklenebilir. Örneğin, **\{2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212\}** ve **2CDB0FE7-D7B3-4938-A0F0-FE28FB8FE212** geçerli GUID dizeleridir.
- Bu nedenle, ayraçların eklenip eklenmediğine bağlı olarak toplam 36 veya 38 karakter olmalıdır.
- Onaltılı basamak olarak kullanılan harfler, büyük harf (A-F), küçük harf (a-f) veya karma olabilir.

Aşağıdaki açık dönüştürme işlevlerini kullanabilirsiniz:

- [GUIDVALUE](er-functions-text-guidvalue.md)
- [TEXT](er-functions-text-text.md)

Karşılaştırma [operatörleri](er-formula-language.md#Operators), *guid* veri türü ile kullanılabilen tek operatör türüdür. Aşağıdaki operatörler, iki *guid* değerini karşılaştırmak için kullanılabilir: \<\> ve =.

## <a name="integer"></a><a name="integer"></a>Tamsayı

*tamsayı* temel veri türü, ondalık basamağı olmayan bir sayıyı temsil eder. Tamsayılar, yinelemeli ifadelerde denetim değişkenleri olarak veya kayıt listelerinde dizinler olarak kullanılır.

*tamsayı* değişmez değeri, **12345** gibi bir ER [ifadesine](general-electronic-reporting-formula-designer.md#formula-designer-overview) (formül) doğrudan girilen tamsayıdır. *tamsayı*, 32 bit genişliğindedir. Varsayılan değer **0**'dır ve iç gösterim uzun bir sayıdır. Bir *tamsayı* otomatik olarak *gerçek* bir sayıya dönüştürülür.

Ek olarak, aşağıdaki açık dönüştürme işlevlerini kullanabilirsiniz:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Bir *tamsayı* aralığı şöyledir: \[-2,147,483,647 : 2,147,483,647\]. Bu aralığın tüm tam sayıları, değişmez değer olarak kullanılabilir.

*Tamsayı* veri türüyle tüm karşılaştırma ve matematik [operatörleri](er-formula-language.md#Operators) kullanılabilir.

## <a name="int64"></a><a name="int64"></a>Int64

*int64* temel veri türü, ondalık basamağı olmayan bir sayıyı temsil eder. *Int64* değerleri, yinelemeli ifadelerde denetim değişkenleri olarak veya kayıt tanımlayıcıları olarak kullanılır.

*int64*, 64 bit genişliğindedir. Varsayılan değer **0**'dır ve iç gösterim uzun bir sayıdır. Bir *int64* otomatik olarak *gerçek* bir sayıya dönüştürülür.

Ek olarak, aşağıdaki açık dönüştürme işlevlerini kullanabilirsiniz:

- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)

Bir *int64* aralığı şöyledir: \[-9,223,372,036,854,775,807 : 9,223,372,036,854,775,807\].

*int64* veri türüyle tüm karşılaştırma ve matematik [operatörleri](er-formula-language.md#Operators) kullanılabilir.

## <a name="real"></a><a name="real"></a>Gerçek

*Gerçek* temel veri türü, tamsayılara ek olarak ondalık değerler de bulundurabilir. *Gerçek* değerinin beklendiği her yerde ondalık değişmez değerlerini kullanabilirsiniz. Ondalık değişmez değer, **2.19** gibi doğrudan kod içine girildiği şekilde ondalık değerdir.

> [!NOTE]
> ER ifadelerinde, bir nokta (.) her zaman ondalık ayırıcı olarak kullanılır.

Gerçekler tüm ifadelerde kullanılabilir ve hem karşılaştırma hem de aritmetik operatörlerle birlikte kullanılabilirler. *gerçek*, 16 basamaktan oluşan bir duyarlığa sahiptir. *Gerçek*'in varsayılan değeri **0.0**'dır ve iç gösterim ikili olarak kodlanmış bir dijital (BCD) sayıdır. BCD kodlaması, 0.1 katları olan değerlerin tam gösterimlerini sağlar. *gerçek* değişkeninin aralığı -(10)<sup>127</sup> ile (10)<sup>127</sup> arasındadı. Bu aralıktaki tüm gerçekler, ER ifadelerinde değişmez değerler olarak kullanılabilir.

*gerçek*, örtük dönüştürme içermez. Ancak, bir *gerçek* veriyi açıkça diğer veri türlerine ve diğer veri türlerini bir *gerçek* değerine dönüştürmek için aşağıdaki işlevleri kullanabilirsiniz:

- [INTVALUE](er-functions-conversion-intvalue.md)
- [INT64VALUE](er-functions-conversion-int64value.md)
- [NUMBERFORMAT](er-functions-text-numberformat.md)
- [TEXT](er-functions-text-text.md)
- [VALUE](er-functions-conversion-value.md)

*gerçek* veri türüyle tüm karşılaştırma ve matematik [operatörleri](er-formula-language.md#Operators) kullanılabilir.

## <a name="string"></a><a name="string"></a>Dize

*dize* temel veri türü metin, hesap numarası, adres ve telefon numaraları olarak kullanılan bir dizi karakteri temsil eder.

*Dize* değişmez değerleri, tırnak işaretleri ("") içine alınmış karakterlerdir. *Dize* değişmez değerleri, ER ifadelerinde *dize* değerlerinin beklendiği her yerde kullanılabilir. dizeleri, karşılaştırma gibi mantıksal ifadelerde kullanabilirsiniz. Ayrıca *dize* değerlerini **\&** operatörünü veya [CONCATENATE](er-functions-text-concatenate.md) işlevini kullanarak da art arda ekleyebilirsiniz.

> [!NOTE]
> İki *dize* değerini art arda ekler ve sonuçta elde edilen *dizenin* birden çok satıra yayılmasını istiyorsanız, değerler arasındaki satır sonu ayırıcısını kullanın. TEXT çıktısı için bu ayırıcı, [CHAR](er-functions-text-char.md)(10) veya CHAR(13) ifadesi kullanılarak oluşturulan bir karakter olabilir. HTML için **\<br\>** etiketi olabilir.

Bir *dize* için varsayılan değer, karakter içermeyen boş bir metin dizesidir ve dahili gösterim, bir karakter listesidir.

Dizeler için otomatik dönüştürme yoktur. Ancak, aşağıdaki açık dönüştürme işlevlerini kullanabilirsiniz:

- [CHAR](er-functions-text-char.md)
- [FORMAT](er-functions-text-format.md)
- [LEFT](er-functions-text-left.md)
- [LEN](er-functions-text-len.md)
- [MID](er-functions-text-mid.md)
- [PADLEFT](er-functions-text-padleft.md)
- [REPLACE](er-functions-text-replace.md)
- [RIGHT](er-functions-text-right.md)
- [TEXT](er-functions-text-text.md)
- [TRANSLATE](er-functions-text-translate.md)
- [TRIM](er-functions-text-trim.md)
- [UPPER](er-functions-text-upper.md)

*Dize* değerlerinin dönüşümü hakkında daha fazla bilgi için bkz. [Metin kategorisinin ER işlevlerinin listesi](er-functions-category-text.md).

*Dize* belirsiz sayıda karakter içerebilir.

*dize* veri türüyle tüm karşılaştırma [operatörleri](er-formula-language.md#Operators) kullanılabilir.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Elektronik raporlamada formül dili](er-formula-language.md)
- [Desteklenen bileşik veri türleri](er-formula-supported-data-types-composite.md)
