---
title: ORDERBY ER işlevi
description: Bu makalede, ORDERBY Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 23ace859bf75b2adb6ef8604475519a015486948
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282576"
---
# <a name="orderby-er-function"></a>ORDERBY ER işlevi

[!include [banner](../includes/banner.md)]

`ORDERBY` işlev belirtilen bağımsız değişkenlere göre sıralandıktan sonra belirtilen listeyi *kayıt listesi* değeri olarak döndürür. Bu bağımsız değişkenler ifadeler olarak tanımlanabilir.

## <a name="syntax-1"></a><a name="syntax-1"></a>Sözdizimi 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Sözdizimi 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Bu sözdizimi Microsoft Dynamics 365 Finance 10.0.25 ve sonraki sürümler için desteklenir.

## <a name="arguments"></a>Bağımsız değişkenler

`location`: *[Dize](er-formula-supported-data-types-primitive.md#string)*

Sıralamanın çalıştırılması gereken konum. Aşağıdaki seçenekler geçerlidir:

- "Query"
- "InMemory"

`list`: *[Kayıt listesi](er-formula-supported-data-types-composite.md#record-list)*

*Kayıt listesi* veri türünde bir veri kaynağının geçerli yolu.

`expression 1`: *Alan*

Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu. Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır. Bu bağımsız değişken gereklidir.

`expression N`: *Alan*

Çağrılan işlevin `list` bağımsız değişkeni tarafından başvurulan bir veri kaynağı alanının geçerli yolu. Referans gösterilen alan, ilkel veri türünde bir alan olmalıdır. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Kayıt listesi*

Oluşturulan kayıt listesi.

## <a name="usage-notes"></a>Kullanım notları

### <a name="syntax-1"></a>Sözdizimi 1

Veri sıralaması her zaman uygulama sunucusunun belleğinde yapılır. Daha fazla ayrıntı için [örnek 1](#example-1)'e bakın.

### <a name="syntax-2"></a>Sözdizimi 2

### <a name="sorting-in-memory"></a>Bellekte sıralama

`location` bağımsız değişkeni, **InMemory** olarak belirtildiğinde, veri sıralama bir uygulama sunucusunun belleğinde yapılır. Daha fazla ayrıntı için [örnek 2](#example-2)'e bakın.

### <a name="sorting-in-database"></a>Veritabanında sıralama

`location` bağımsız değişkeni **Query** olarak belirtildiğinde, veri sıralama veritabanı düzeyinde yapılır. Bu durumda, `list` bağımsız değişkeni, doğrudan veritabanı sorgusunun kurulabileceği uygulama kaynağını belirten aşağıdaki [Elektronik raporlama (ER)](general-electronic-reporting.md) veri kaynaklarından birine işaret etmelidir:

- *Tablo kayıtları* türünde veri kaynağı
- *Tablo kayıtları* türünde bir veri kaynağının ilişkisi
- *Hesaplanan alan* türünde bir veri kaynağı

`expression 1` ve `expression N` bağımsız değişkenleri, doğrudan veritabanı sorgusunun da kurulabileceği uygulama kaynağının ilgili alanlarını belirten bir ER veri kaynağının alanlarına işaret etmelidir.

Doğrudan veritabanı sorgusu oluşturulamazsa ER model eşleme tasarımcısında bir doğrulama [hatası](er-components-inspections.md#i18) oluşur. Aldığınız iletide, `ORDERBY` işlevini içeren ER ifadesinin çalışma zamanında çalıştırılamadığı belirtilir.

Daha iyi performans için sıralama çok sayıda kayıt içerebilecek uygulama veri kaynakları için yapılandırıldığında **Query** seçeneğini kullanmanızı öneririz (örneğin, işlem uygulama tabloları için).

> [!NOTE]
> `ORDEBY` işlevi doğrudan veritabanı sorgusuna çevrilemez. Bu nedenle, bu işlevi içeren bir ER veri kaynağı sorgulanamaz. Ayrıca, yalnızca sorgulanabilir veri kaynaklarının kullanılabileceği [FILTER](er-functions-list-filter.md) ve [ALLITEMSQUERY](er-functions-list-allitemsquery.md) gibi ER işlevleri kapsamında kullanılamaz.

Daha fazla ayrıntı için [örnek 3](#example-3) ve [örnek 4](#example-4)'e bakın.

### <a name="comparability"></a>Karşılaştırılabilirlik

SQL veritabanı altyapısı ve Finance uygulama sunucusu tek bir karakter için farklı bir sıralama değeri kullanabileceğinden, sıralama için bir [Dize](er-formula-supported-data-types-primitive.md#string) alanı kullanıldığında aynı kayıt listesinin sıralama sonucu farklılık gösterebilir. Daha fazla ayrıntı için [örnek 5](#example-5)'e bakın.

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Örnek 1: Bellek içi varsayılan yürütme

*Hesaplanmış alan* türüne ait veri kaynağı **DS**'si girerseniz ve `SPLIT ("C|B|A", "|")` deyim içeriyorsa, `FIRST( ORDERBY( DS, DS. Value)).Value` ifadesi **A** metin değerini döndürür.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Örnek 2: Bellek içi açık yürütme

**Satıcı**, **VendTable** tablosuna başvuran *Tablo kayıtları* türünün ER veri kaynağı olarak yapılandırılmışsa hem `ORDERBY (Vendor, Vendor.'name()')` hem de `ORDERBY ("InMemory", Vendor, Vendor.'name()')` ifadesi, ada göre artan sırada sıralanmış satıcı listesini döndürür.

ER model eşleme tasarımcısında `ORDERBY ("Query", Vendor, Vendor.'name()')` ifadesini yapılandırdığınızda, `Vendor.'name()'` yolu doğrudan veritabanı sorgusuna çevrilemeyen mantığı olan bir uygulama yöntemine başvurduğundan tasarım zamanında bir doğrulama [hatası](er-components-inspections.md#i8) oluşur.

## <a name="example-3-database-query"></a><a name="example-3"></a>Örnek 3: Veritabanı sorgusu

**TaxTransaction**, **TaxTrans** tablosuna başvuran *Tablo kayıtları* türünün ER veri kaynağı olarak yapılandırılmışsa `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` ifadesi, kayıtları uygulama veritabanı düzeyinde sıralar ve artan sırada vergi koduna göre sıralanmış vergi hareketlerinin listesini döndürür.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Örnek 4: Sorgulanabilir veri kaynakları

**TaxTransaction**, **TaxTrans** tablosuna başvuran *Tablo kayıtları* türünün ER veri kaynağı olarak yapılandırılmışsa **TaxTransactionFiltered** ER veri kaynağı, belirli bir vergi kodu için hareketleri getirecek `FILTER(TaxTransaction, TaxCode="VAT19")` ifadesini içerecek şekilde yapılandırılabilir. Yapılandırılmış **TaxTransactionFiltered** ER veri kaynağı sorgulanabilir olduğundan, `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` ifadesi, hareket tarihine göre artan sırada sıralanan filtre uygulanmış vergi hareketlerinin listesini döndürecek şekilde yapılandırılabilir.

**TaxTransactionOrdered** öğesini `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` ifadesini içeren *Hesaplanan alan* türünün ER veri kaynağı ve `FILTER(TaxTransactionOrdered, TaxCode="VAT19")` ifadesini içeren *Hesaplanan alan* türünün ER veri kaynağı olarak yapılandırırsanız ER modeli eşleme tasarımcısında tasarım zamanında bir doğrulama [hatası](er-components-inspections.md#i18) oluşur. Bu hata, [FILTER](er-functions-list-filter.md#usage-notes) işlevinin ilk bağımsız değişkeninin sorgulanabilir bir ER veri kaynağına başvurması gerekmesi ancak `ORDERBY` işlevini içeren **TaxTransactionOrdered** veri kaynağının sorgulanamaması nedeniyle oluşur.

## <a name="example-5-comparability"></a><a name="example-5"></a>Örnek 5: Karşılaştırılabilirlik

### <a name="prerequisites"></a>Önkoşullar

1. `SPLIT ("D1|_D2|D3", "|")` ifadesini içeren *Hesaplanan alan* türünün **DS1** veri kaynağını girin.
2. **[Mali boyut değerleri](../../../finance/general-ledger/financial-dimensions.md)** sayfasını açın ve **CostCenter** boyutunu seçin.
3. Aşağıdaki boyut değerlerini girin: **D1**, **\_D2** ve **D3**.

### <a name="sorting-in-memory"></a>Bellekte sıralama

1. `ORDERBY("InMemory", DS1, DS1.Value)` ifadesini içeren *Hesaplanan alan* türünün **DS2** veri kaynağını yapılandırın.
2. `FIRST(DS2).Value` ifadesinin **"D1"** metin değerini, `INDEX(DS2, COUNT(DS2)).Value` ifadesinin **"\_D2"** metin değerini ve `STRINGJOIN(DS2, DS2.Value, "|")` ifadesinin **"D1\|D3\|\_D2"** metin değerini döndürdüğüne dikkat edin.

### <a name="sorting-in-database"></a>Veritabanında sıralama

1. **FinancialDimensionValueEntity** varlığına başvuran *Tablo kayıtları* türünün veri kaynağı **DS3** girin.
2. `FILTER(DS3, DS3.FinancialDimension="CostCenter")` ifadesini içeren *Hesaplanan alan* türünün **DS4** veri kaynağını yapılandırın.
3. `ORDERBY(DS4, DS4.DimensionValue)` ifadesini içeren *Hesaplanan alan* türünün **DS5** veri kaynağını yapılandırın.
4. `FIRST(DS5).Value` ifadesinin **"D2"** metin değerini, `INDEX(DS5, COUNT(DS5)).Value` ifadesinin **"\_D3"** metin değerini ve `STRINGJOIN(DS5, DS5.Value, "|")` ifadesinin **"D2\_D1\|\|D3"** metin değerini döndürdüğüne dikkat edin.

## <a name="additional-resources"></a>Ek kaynaklar

[Liste işlevleri](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
