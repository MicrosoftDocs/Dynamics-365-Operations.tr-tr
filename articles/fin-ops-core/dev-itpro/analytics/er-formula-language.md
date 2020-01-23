---
title: Elektronik raporlamada formül dili
description: Bu konu, Elektronik raporlamada (ER) formül dili nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/18/2019
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
ms.openlocfilehash: 3b1c6a3f3fd5b55012d89a6c9f0bf2ed5dddd13c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916672"
---
# <a name="electronic-reporting-formula-language"></a>Elektronik raporlamada formül dili

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER), güçlü bir veri dönüştürme deneyimi sağlar. ER formül tasarımcısında gerekli olan veri eklemelerini ifade etmek için kullanılan dil, Microsoft Excel'deki formül diline benzer.

## <a name="basic-syntax"></a>Temel sözdizimi

ER ifadeleri aşağıdaki öğelerden birini veya tümünü içerebilirler:

- [Sabitler](#Constants)
- [İşleçler](#Operators)
- [Referanslar](#References)
- [Yollar](#Paths)
- [İşlevler](#Functions)

## <a name="Constants">Sabitler</a>

İfadeleri tasarlarken metin ve sayısal sabitler (hesaplanmayan değerler) içeren ifadeler kullanabilirsiniz. Örneğin `VALUE ("100") + 20` ifadesi, sayısal sabit **20** ve dize sabiti **"100"** kullanır ve **120** sayısal değerini döndürür.

ER formül tasarımcısı kaçış sıralarını destekler. Bu nedenle, farklı şekilde ele alınması gereken bir ifade dizesi belirtebilirsiniz. Örneğin, `"Leo Tolstoy ""War and Peace"" Volume 1"` deyimi, **Leo Tolstoy "Savaş ve barış" 1. Cilt** metin dizesini döndürür.

## <a name="Operators">İşleçler</a>

Aşağıdaki tablo, toplama, çıkarma, bölme ve çarpma gibi temel matematik işlemleri gerçekleştirmek için kullanabileceğiniz aritmetik işleçleri gösterir.

| İşleç | Anlamı               | Örnek     |
|----------|-----------------------|-------------|
| +        | Fark hesap eki              | `1+2`       |
| -        | Çıkartma, olumsuzluk | `5-2`, `-1` |
| \*       | Çarpma        | `7\*8`      |
| /        | Bölüm              | `9/3`       |

Aşağıdaki tablo desteklenen karşılaştırma işleçlerini göstermektedir. Bu işleçleri iki değeri karşılaştırmak için kullanabilirsiniz.

| İşleç | Anlamı                  | Örnek      |
|----------|--------------------------|--------------|
| =        | Eşittir                    | `X=Y`        |
| &gt;     | Büyüktür             | `X>Y`        |
| &lt;     | Küçüktür                | `X<Y`        |
| &gt;=    | Büyüktür veya eşittir | `X>=Y`       |
| &lt;=    | Küçüktür veya eşittir    | `X<=Y`       |
| &lt;&gt; | Eşit değil             | `X<>Y`       |

Ayrıca, bir metin birleştirme işleci olarak (&) işareti kullanabilirsiniz. Bu şekilde, bir veya daha fazla metin dizesini tek bir metin içinde birleştirebilir veya art arda ekleyebilirsiniz.

| İşleç | Anlamı     | Örnek                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Art arda eklemek | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>İşleç önceliği

Bir bileşik ifadenin parçalarının hangi sırada değerlendirilecekleri önemlidir. Örneğin, `1 + 4 / 2` deyiminin sonucu, bölme işleminin mi yoksa toplama işleminin mi önce gerçekleşeceğine göre farklılık göstermektedir. Bir ifadenin nasıl değerlendirileceğini açıkça tanımlamak için parantezleri kullanabilirsiniz. Örneğin, toplama işleminin önce yapılması gerektiğini belirtmek için yukarıdaki ifadeyi şuna değiştirebilirsiniz: `(1 + 4) / 2` Bir ifadede gerçekleştirilmesi gereken işleçlerin sırasını özellikle belirtmezseniz sıralama, desteklenen işleçlerin varsayılan önceliğine dayandırılır. Aşağıdaki tablo, işleçlerin her birine atanan önceliği gösterir. Daha yüksek bir önceliğe sahip işleçler (örneğin, 7) daha düşük önceliğe sahip işleçlerden önce değerlendirilirler (örneğin, 1).

| Öncelik | İşleçler      | Sözdizimi                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruplama       | ( … )                                                                   |
| 6          | Üye erişimi  | … 'i tıklatın. …                                                                   |
| 5          | İşlev çağrısı  | … ( … )                                                                 |
| 4          | Çarpımsal | … \* …<br>… / …                                                         |
| 3          | Eklenecek       | … + …<br>… - …                                                          |
| 2          | Karşılaştırma     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Ayrılma     | … , …                                                                   |

Bir ifadenin aynı önceliğe sahip birden çok işleç içeriyorsa, bu işleçler soldan sağa doğru değerlendirilir. Örneğin, `1 + 6 / 2 \* 3 > 5` ifadesi, **doğru** sonucunu verir. Deyimlerin okunmasını ve bakımını daha kolay hale getirmek için, deyimlerin ifadedeki arzu edilen işlem sıralarını, parantezler kullanarak açıkça belirtmenizi tavsiye ederiz.

## <a name="References">Referanslar</a>

Bir ifadenin tasarımında kullanılabilir olan bir mevcut ER bileşeninin tüm veri kaynakları, adlandırılmış referanslar olarak kullanılabilirler. Geçerli ER bileşeni, bir model eşleme veya bir biçim olabilir. Örneğin, mevcut ER model eşlemesi, *DateTime* veri türünün değerini döndüren **ReportingDate** veri kaynağını içerir. Oluşturulan belgede bu değeri uygun şekilde biçimlendirmek için ifadedeki veri kaynağına başvurabilirsiniz: `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Referansta bulunan veri kaynağının adında yer alan ve alfabedeki bir harfi temsil etmeyen tüm karakterlerin önünde tek bir tırnak işareti (') olmalıdır. Referans gösterilen veri kaynağı adı alfabede temsil edilmeyen en az bir simgeyi içeriyorsa, adın tekli tırnak işaretleri içerisine alınması gerekir. Örneğin, alfabetik olmayan simgeler noktalama işaretleri veya diğer yazılı simgeleri olabilir. Burada bazı örnekler verilmiştir:

- **Bugünün tarihi ve saati** veri kaynağının bir ER deyiminde şu şekilde referans gösterilmiş olması gerekir: `'Today''s date & time'`.
- **Müşteriler** veri kaynağının **name()** yöntemi, bir ER deyimi içerisinde aşağıdaki gibi referans gösterilmelidir: `Customers.'name()'`.

Uygulama veri kaynaklarının yöntemlerinde parametreler varsa, yöntemleri çağırmak için aşağıdaki sözdizimi kullanılır:

- **Sistem** veri kaynağının **isLanguageRTL** yönteminde *Dize* veri türünün **EN-US** parametresi varsa, bu yönteme bir ER deyiminde `System.isLanguageRTL("EN-US")` olarak referans verilmelidir.
- Bir yöntem adı yalnızca alfasayısal simgelerden oluşuyorsa tırnak işaretleri zorunlu değildir. Ancak, bir tablonun bir yönteminin adı köşeli parantez içerdiğinde zorunludur.

**Sistem** veri kaynağı **Global** uygulama sınıfına referansta bulunan bir ER eşlemesine eklendiğinde, `System.isLanguageRTL("EN-US ")` ifade **YANLIŞ** *Boole* değerini döndürür. Değiştirilen ifade `System.isLanguageRTL("AR")`, **DOĞRU** *Boole* değerini döndürür.

Değerlerin bu yöntem türünün parametrelerine geçiş şeklini sınırlandırabilirsiniz:

- Bu tür yöntemlere yalnızca sabitler geçirilebilir. Sabitlerin değerleri tasarım zamanında tanımlanır.
- Yalnızca basit (temel) veri türleri bu tür parametreler için desteklenir. Temel veri türleri şunlardır: *tamsayı*, *gerçek*, *Boole* ve *dize*.

## <a name="Paths">Yollar</a>

Bir ifade yapılandırılmış bir veri kaynağına başvurduğunda, bu veri kaynağının belirli bir temel öğesini seçmek için bir yol tanımı kullanabilirsiniz. Yapılandırılmış veri kaynağının öğelerini tek tek ayırmak için bir nokta karakteri (.) kullanılır. Örneğin, mevcut ER model eşlemesi **InvoiceTransactions** veri kaynağını içerir ve bu veri kaynağı kayıtların listesini döndürür. **InvoiceTransactions** kayıt yapısı her ikisi de sayısal değerler döndüren **AmountDebit** ve **AmountCredit** alanlarını içerir. Bu nedenle, faturalanan tutarı hesaplamak için aşağıdaki ifadeyi tasarlayabilirsiniz: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Bu `InvoiceTransactions.AmountDebit` ifadedeki yapım, *kayıt listesi* türünün **Faturalamaİşlemleri** veri kaynağının **TutarBorç** alanına erişmek için kullanılan yoldur.

### <a name="relative-path"></a>Göreli yol

Yapılandırılmış bir veri kaynağının yolu "et" işareti (@) ile başlıyorsa, bu göreli bir yoldur. Kullanılan sıradüzenli ağaç yapısının mutlak yolunun kalan bölümü yerine, "et" işareti gösterilir. Aşağıdaki şekilde bir örneği gösterilmiştir. Burada, `Ledger.'accountingCurrency()'` mutlak yol, **muhasebe** veri kaynağından alınan muhasebe para birimi değerinin, veri modelinin **MuhasebeParaBirimi** alanına girildiğini gösterir.

![ER model eşleme Tasarımcısı sayfasındaki mutlak yol örneği](./media/ER-FormulaLanguage-AbsolutePath.png)

Aşağıdaki çizimdeki örnek, göreli bir yolun nasıl kullanıldığını göstermektedir. `@.AccountNum` göreli yolu, **Intrastat** veri kaynağının **AccountNum** alanının (veri modelinin hiyerarşik ağacındaki **AccountNum** alanının bir üst düzeyde görüntülenir) müşteri veya satıcı hesap numarasını girmek için veri kaynağının **AccountNum** alanı kullanılacağını belirtir.

![ER model eşleme Tasarımcısı sayfasındaki göreli yol örneği](./media/ER-FormulaLanguage-RelativePath1.png)

Mutlak yolun kalan bölümü de [ER formül düzenleyicisinde](general-electronic-reporting-formula-designer.md) gösterilir.

![ER formül Tasarımcısı sayfasında, mutlak yolun kalan bölümü](./media/ER-FormulaLanguage-RelativePath2.png)

## <a name="Functions">İşlevler</a>

ER yerleşik işlevler ER deyimlerinde kullanılabilir. İfade bağlamının tüm veri kaynakları (geçerli ER model eşlemesi ya da ER biçimi ) çağırma işlevlerinin bağımsız değişkenleri listesine uygun işlevleri çağırma parametreleri olarak kullanılabilir. Sabitler çağırma işlevleri parametreleri olarak da kullanılabilir. Örneğin, mevcut ER model eşlemesi **InvoiceTransactions** veri kaynağını içerir ve bu veri kaynağı kayıtların listesini döndürür. **InvoiceTransactions** kayıt yapısı her ikisi de sayısal değerler döndüren **AmountDebit** ve **AmountCredit** alanlarını içerir. Bu sebeple, faturalanan tutarı hesaplamak için, dahili ER yuvarlama işlevini kullanan şu deyimi tasarlayabilirsiniz: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

ER model eşlemeleri ve ER raporları tasarladığınızda, aşağıdaki kategorilerdeki ER işlevlerini kullanabilirsiniz:

- [Tarih ve saat işlevleri](er-functions-category-datetime.md)
- [Liste işlevleri](er-functions-category-list.md)
- [Mantıksal işlevler](er-functions-category-logical.md)
- [Matematik işlevi](er-functions-category-mathematical.md)
- [Kayıt işlevleri](er-functions-category-record.md)
- [Metin işlevleri](er-functions-category-text.md)
- [Veri toplama işlevleri](er-functions-category-data-collection.md)
- [Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)
- [Tür dönüştürme işlevleri](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Liste uzantı işlevleri

ER, ER ifadelerinde kullanılan işlevlerin listesini genişletmenize olanak sağlar. Bazı mühendislik çabaları gereklidir. Ayrıntılı bilgi için bkz. [Elektronik raporlama (ER) işlev listesini genişletme](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Bileşik ifadeler

Veri türlerinin eşleşmesi koşuluyla, farklı kategorilerdeki işlevleri kullanan bileşik ifadeler oluşturabilirsiniz. İşlevleri birlikte kullandığınızda, bir işlevdeki çıkış veri türünü başka bir işlev için gerekli olan giriş veri türüne eşleştirin. Örneğin, bir alanı bir ER biçim öğesine bağlamakta olası bir "liste-sahip-boş" hatasının oluşmaması için, aşağıdaki örnekte görüldüğü gibi, [liste](er-functions-category-list.md) kategorisinden işlevleri [mantıksal](er-functions-category-logical.md) kategorideki bir işlevle birleştirin. Burada, formül, ilgili listeden gerekli toplama değerini vermeden önce **IntrastatTotals** listesinin boş olup olmadığını test etmek için [Eğer](er-functions-logical-if.md) işlevini kullanır. **IntrastatTotals** listesi boşsa, formül **0** (sıfır) değerini döndürür.

```
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Çoklu çözüm

Genellikle, farklı kategorilerdeki işlevleri veya aynı kategorideki farklı işlevleri kullanarak aynı veri dönüştürme sonucunu birden çok yolla elde edebilirsiniz. Örneğin, önceki ifade [liste](er-functions-category-list.md) kategorisinden [COUNT](er-functions-list-count.md) işlevi kullanılarak da yapılandırılabilir.

```
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlama işlev listesini genişletme](general-electronic-reporting-formulas-list-extension.md)
