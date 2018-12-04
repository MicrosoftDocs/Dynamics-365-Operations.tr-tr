---
title: "Elektronik raporlamada (ER) formül tasarımcısı"
description: "Bu konu, formül tasarımcısının Elektronik raporlamada (ER) nasıl kullanılacağını açıklar."
author: NickSelin
manager: AnnBe
ms.date: 10/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f0ded563ecf0b6d0ce67f046f631d8c4dcfc7802
ms.openlocfilehash: 1dc584355c8992ee701169fd5d29ad7b0300a498
ms.contentlocale: tr-tr
ms.lasthandoff: 10/23/2018

---

# <a name="formula-designer-in-electronic-reporting-er"></a>Elektronik raporlamada (ER) formül tasarımcısı

[!include [banner](../includes/banner.md)]

Bu konu, formül tasarımcısının Elektronik raporlamada (ER) nasıl kullanılacağını açıklar. Belirli bir elektronik belge için ER içerisinde bir biçim tasarladığınızda, belgenin gereksinimlerini karşılamak ve biçimlendirmek üzere formülleri veri dönüştürme için kullanabilirsiniz. Bu formüller Microsoft Excel'deki formüllere benzer. Formüllerde farklı türde işlevler desteklenmektedir: metin, tarih ve saat, matematiksel mantıksal, bilgi, veri türü dönüştürme ve diğer (iş etki alanına özel işlevler).

## <a name="formula-designer-overview"></a>Formül tasarımcısına genel bakış

ER formül tasarımcısını destekler. Bu nedenle, tasarım zamanında aşağıdaki görevler için çalışma zamanında kullanılabilecek ifadeler yapılandırabilirsiniz:

- Microsoft Dynamics 365 for Finance and Operations veritabanından alınan verileri dönüştürün ve bu verileri ER biçimleri için (filtreleme, gruplama, veri türü dönüştürme vb.) bir veri kaynağı olmak üzere tasarlanmış ER veri modeline girin. (Örneğin, bu dönüştürme işlemleri filtrelemeyi, gruplandırmayı ve veri türü dönüşümünü içerebilir.)
- Oluşturulan bir elektronik belgeye belirli bir ER biçiminin düzenine ve koşullarına uygun olarak gönderilmesi gereken verileri biçimlendirin. (Örneğin, biçimlendirme istenen dil veya kültüre ya da kodlamaya uygun olarak yapılabilir).
- Elektronik belge oluşturma işlemini kontrol edin. (Örneğin, ifadeler veri işlemeye bağlı olarak biçimin belirli öğelerinin çıkışını etkinleştirebilir veya devre dışı bırakabilir. Aynı zamanda, belge oluşturma işlemini durdurabilir veya kullanıcılara ileti gönderebilir.)

**Formül tasarımcısı** sayfasını aşağıdaki eylemlerden birini gerçekleştirirken açabilirsiniz:

- Veri kaynağı maddelerini veri modeli bileşenlerine bağlayın.
- Veri kaynağı maddelerini biçim bileşenlerine bağlayın.
- Veri kaynaklarının parçası olan hesaplanan alanların bakımını tamamlayın.
- Kullanıcı giriş parametreleri için görünürlük koşullarını tanımlayın.
- Biçimin dönüşümlerini tasarlayın.
- Biçimin bileşenlerinin etkinleştirme koşullarını tanımlayın.
- Biçimin DOSYA bileşenleri için dosya adlarını tanımlayın.
- İşlem denetimi doğrulamaları için koşulları tanımlayın.
- İşlem denetimi doğrulamaları için ileti metnini tanımlayın.

## <a name="designing-er-formulas"></a>ER formülleri tasarlama

### <a name="data-binding"></a>Veri ilişkilendirme

ER formül tasarımcısı, veri kaynaklarından alınan verinin, söz konusu veri veri tüketicisinde çalışma zamanında girilebilecek şekilde dönüştürecek bir ifade tanımlamak için kullanılabilir:

- Finance and Operations veri kaynaklarından ve çalışma zamanı parametrelerinden ER veri modeline
- Bir ER veri modelinden ER biçimine
- Finance and Operations veri kaynaklarından ve çalışma zamanı parametrelerinden ER biçimine

Bu tür bir ifadenin tasarımı aşağıda gösterilmiştir. Bu örnekte ifade, Finance and Operations Intrastat tablosunun **Intrastat.AmountMST** alanının değerini iki ondalık basamağa yuvarlar ve yuvarlanan değeri döndürür.

[![Veri ilişkilendirme](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Aşağıdaki çizim bu tür bir ifadenin nasıl kullanılabileceğini gösterir. Bu örnekte, tasarlanmış ifadenin sonucu, **Vergi raporlama modeli** veri modelinin **Transaction.InvoicedAmount** bileşenine girilir.

[![Kullanılan veri bağlama](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Çalışma zamanında, tasarlanan formül olan **ROUND (Intrastat.AmountMST, 2)** **AmountMST** alanındaki değeri Intrastat tablosundaki her kayıt için iki ondalık basamağa yuvarlar. Daha sonra yuvarlanan değeri **Vergi raporlama** veri modelinin **Transaction.InvoicedAmount** bileşenine girer.

### <a name="data-formatting"></a>Veri biçimlendirme

ER formül tasarımcısı, veri kaynaklarından alınan verinin, söz konusu veri, elektronik belgenin oluşturulmasında kullanılabilecek şekilde biçimlendirecek bir ifade tanımlamak için kullanılabilir. Bir biçim için yeniden kullanılması gereken tipik bir kural olarak uygulanması gereken bir biçimlendirmeniz olabilir. Bu durumda, bu biçimlendirmeyi biçim yapılandırmasına, biçimlendirme ifadesine sahip adlandırılmış bir dönüştürme olarak bir kez girebilirsiniz. Daha sonra, bu adlandırılmış dönüşüm, oluşturduğunuz biçimlendirme ifadesine çıktının biçimlendirilmesi gereken birçok biçim bileşenine bağlanabilir.

Bu tür bir dönüştürmenin tasarımı aşağıda gösterilmiştir. Bu örnekte, **TrimmedString** dönüşümü, **Dize** veri türünden gelen verileri baştaki ve sondaki boşlukları kaldırarak keser. Bunun ardından, kesilmiş dize değerini döndürür.

[![Dönüşüm](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Aşağıdaki çizim bu tür bir dönüştürmenin nasıl kullanılabileceğini gösterir. Bu örnekte, birçok biçim bileşeni metni çıktı olarak çalışma zamanında oluşturulan elektronik belgeye gönderir. Bu biçim bileşenlerinin tümü ada göre **TrimmedString** dönüştürmesine başvurur.

[![Kullanılan dönüştürme](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Önceki örnekte yer alan **partyName** gibi biçim bileşenleri **TrimmedString** dönüşümüne referansta bulunur, dönüştürme metni çıktı olarak oluşturulan elektronik belgeye gönderir. Bu metin baştaki ve sondaki boşlukları içermez.

Tek tek uygulanması zorunlu olan bir biçimlendirmeniz varsa, bu biçimlendirmeyi belirli bir biçim bileşeninin bir bağlamasının tekil ifadesi olarak tanıtabilirsiniz. Aşağıdaki çizim bu türde bir ifadeyi gösterir. Bu örnekte **partyType** biçim bileşeni veri kaynağındaki **Model.Company.RegistrationType** alanından gelen veriyi büyük harfe dönüştüren bir ifade aracılığıyla veri kaynağına bağlıdır. Sonra ifade metni çıktı olarak elektronik belgeye gönderir.

[![Ayrı bir bileşene biçimlendirme uygulama](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>İşlem akış denetimi

ER formül tasarımcısı, elektronik belge oluşturma işlem akışını denetleyen ifadeleri tanımlamak için kullanılabilir. Aşağıdaki görevlerini yerine getirebilirsiniz:

- Bir belge oluşturma işleminin ne zaman durdurulması gerektiği koşullarını tanımlayın.
- Durdurulan işlemler hakkında kullanıcıya iletiler oluşturan veya devam eden rapor oluşturma işlemleri hakkında yürütme günlüğü iletileri oluşturan ifadeleri belirtin.
- Oluşturulan elektronik belgelerinin dosya adlarını belirtin ve bunların oluşturulma koşullarını denetleyin.

İşlem akışı denetiminin her kuralı ayrı ayrı bir doğrulama olarak tasarlanmıştır. Aşağıdaki çizim bu türde bir doğrulamayı gösterir. u örnekteki yapılandırmanın bir açıklaması aşağıdadır:

- Doğrulama, XML dosyasının oluşturulduğu sırada **INSTAT** düğümü oluşturulurken değerlendirilir.
- Hareketin listesi boşsa, doğrulama işlem yürütmesini durdurur ve **YANLIŞ** döndürür.
- Doğrulama, kullanıcının tercih ettiği dilde Finance and Operations SYS70894 etiket metnini içeren bir hata iletisi döndürür.

[![Doğrulama](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER formül tasarımcısı elektronik belgenin oluşturulması ve dosya oluşturma işlemini denetlemek için bir dosya adı oluşturmak için de kullanılabilir. Aşağıdaki çizim, bu türdeki bir işlem akış denetiminin tasarımını gösterir. u örnekteki yapılandırmanın bir açıklaması aşağıdadır:

- **model.Intrastat** veri kaynağındaki kayıtların listesi toplu işlere bölünür. Her toplu iş en çok 1000 kayıt içerir.
- Çıktı her toplu işlem için XML biçiminde oluşturulmuş bir dosya içeren bir zip dosyası oluşturur.
- Bir ifade, elektronik belge oluşturması için dosya adı ve dosya adı uzantısını birleştirerek bir dosya adı döndürür. İkinci toplu iş ve tüm sonraki toplu işler için, dosya adı toplu iş kimliğini bir sonek olarak içerir.
- Bir ifade (**DOĞRU** döndürerek) en az bir kayıt içeren toplu işler için dosya oluşturma işlemini etkinleştirir.

[![Dosya denetimi](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Temel sözdizimi

ER ifadeleri aşağıdaki öğelerden birini veya tümünü içerebilirler:

- Sabitler
- İşleçler
- Referanslar
- Yollar
- İşlevler

#### <a name="constants"></a>Sabitler

İfadeleri tasarlarken metin ve sayısal sabitler (hesaplanmayan değerler) içeren ifadeler kullanabilirsiniz. Örneğin **VALUE ("100") + 20** ifadesi, sayısal sabit olarak **20** ve dize sabiti olarak **"100"** kullanır ve **120** sayısal değerini döndürür. ER formül tasarımcısı kaçış sıralarını destekler. Bu nedenle, farklı şekilde ele alınması gereken bir ifade dizesi belirtebilirsiniz. Örneğin **"Leo Tolstoy ""Savaş ve Barış"" Cilt 1""** ifadesi aşağıdaki metin dizesini döndürür: **Leo Tolstoy "Savaş ve Barış" Cilt 1**.

#### <a name="operators"></a>İşleçler

Aşağıdaki tablo, toplama, çıkarma, bölme ve çarpma gibi temel matematik işlemleri gerçekleştirmek için kullanabileceğiniz aritmetik işleçleri gösterir.

| İşleç | Anlamı               | Örnek |
|----------|-----------------------|---------|
| +        | Fark hesap eki              | 1+2     |
| -        | Çıkartma, olumsuzluk | 5-2, -1 |
| \*       | Çarpma        | 7\*8    |
| /        | Bölüm              | 9/3     |

Aşağıdaki tablo desteklenen karşılaştırma işleçlerini göstermektedir. Bu işleçleri iki değeri karşılaştırmak için kullanabilirsiniz.

| İşleç | Anlamı                  | Örnek    |
|----------|--------------------------|------------|
| =        | Eşittir                    | X=Y        |
| &gt;     | Büyüktür             | X&gt;Y     |
| &lt;     | Küçüktür                | X&lt;Y     |
| &gt;=    | Büyüktür veya eşittir | X&gt;=Y    |
| &lt;=    | Küçüktür veya eşittir    | X&lt;=Y    |
| &lt;&gt; | Eşit değil             | X&lt;&gt;Y |

Ayrıca, bir metin birleştirme işleci olarak (&) işareti kullanabilirsiniz. Bu şekilde, bir veya daha fazla metin dizesini tek bir metin içinde birleştirebilir veya art arda ekleyebilirsiniz.

| İşleç | Anlamı     | Örnek                                             |
|----------|-------------|-----------------------------------------------------|
| &        | Art arda eklemek | "Yazdırılacak bir şey yok" & ":&nbsp;" & "kayıt bulunamadı" |

##### <a name="operator-precedence"></a>İşleç önceliği

Bir bileşik ifadenin parçalarının hangi sırada değerlendirilecekleri önemlidir. Örneğin, **1 + 4 / 2** deyiminin sonucu, bölme işleminin mi yoksa toplama işleminin mi önce gerçekleşeceğine göre farklılık göstermektedir. Bir ifadenin nasıl değerlendirileceğini açıkça tanımlamak için parantezleri kullanabilirsiniz. Örneğin, toplama işleminin önce yapılması gerektiğini belirtmek için yukarıdaki ifadeyi şuna değiştirebilirsiniz: **(1 + 4) / 2**. Bir ifadede gerçekleştirilmesi gereken işleçlerin sırasını özellikle belirtmezseniz sıralama, desteklenen işleçlerin varsayılan önceliğine dayandırılır. Aşağıdaki tablo, işleçlerin her birine atanan önceliği gösterir. Daha yüksek bir önceliğe sahip işleçler (örneğin, 7) daha düşük önceliğe sahip işleçlerden önce değerlendirilirler (örneğin, 1).

| Öncelik | İşleçler      | Sözdizimi                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruplama       | ( … )                                                                   |
| 6          | Üye erişimi  | … 'i tıklatın. …                                                                   |
| 5          | İşlev çağrısı  | … ( … )                                                                 |
| 4          | Çarpımsal | … \* …<br>… / …                                                         |
| 3          | Eklenecek       | … + …<br>… - …                                                          |
| 2          | Karşılaştırma     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Ayrılma     | … , …                                                                   |

Bir ifadenin aynı önceliğe sahip birden çok işleç içeriyorsa, bu işleçler soldan sağa doğru değerlendirilir. Örneğin, **1 + 6 / 2 \* 3 &gt; 5** ifadesi, **doğru** sonucunu verir. Deyimlerin okunmasını ve bakımını daha kolay hale getirmek için, deyimlerin ifadedeki arzu edilen işlem sıralarını, parantezler kullanarak açıkça belirtmenizi tavsiye ederiz.

#### <a name="references"></a>Referanslar

Bir ifadenin tasarımında kullanılabilir olan bir mevcut ER bileşeninin tüm veri kaynakları, adlandırılmış referanslar olarak kullanılabilirler. (Geçerli ER bileşeni bir model veya biçim olabilir.) Örneğin, geçerli ER veri modeli **ReportingDate** veri kaynağını içerir ve bu veri kaynağı **DATETIME** veri türünde bir değer döndürür. Oluşturulan belgede bu değeri uygun şekilde biçimlendirmek için ifadedeki veri kaynağına başvurabilirsiniz: **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")**.

Referansta bulunan veri kaynağının adında yer alan ve alfabedeki bir harfi temsil etmeyen tüm karakterlerin önünde tek bir tırnak işareti (') olmalıdır. Referans gösterilen veri kaynağı adı alfabede temsil edilmeyen en az bir simgeyi içeriyorsa, adın tekli tırnak işaretleri içerisine alınması gerekir. (Örneğin, alfabetik olmayan simgeler noktalama işaretleri veya diğer yazılı simgeleri olabilir.) Bazı örnekler şunlardır:

- **Bugünün tarihi ve saati** veri kaynağının bir ER deyiminde şu şekilde referans gösterilmiş olması gerekir: **'Bugünün tarihi ve saati'**.
- **Müşteriler** veri kaynağının **name()** yöntemi, bir ER deyimi içerisinde aşağıdaki gibi referans gösterilmelidir: **Customers.'name()'**.

Finance and Operations veri kaynaklarının yöntemlerinde parametreler varsa, yöntemleri çağırmak için aşağıdaki sözdizimi kullanılır:

- **Sistem** veri kaynağının **isLanguageRTL** yönteminde **Dize** veri türünün **EN-US** parametresi varsa, bu yönteme bir ER deyiminde **System.'isLanguageRTL'("EN-US")** olarak referans verilmelidir.
- Bir yöntem adı yalnızca alfasayısal simgelerden oluşuyorsa tırnak işaretleri zorunlu değildir. Ancak, bir tablonun bir yönteminin adı köşeli parantez içerdiğinde zorunludur.

**Sistem** veri kaynağı **Global** Finance and Operations uygulama sınıfına referansta bulunan bir ER eşlemesine eklendiğinde, ifade **YANLIŞ** Boole değerini döndürür. Değiştirilen ifade **System.' isLanguageRTL'("AR")** **DOĞRU** Boole değeri döndürür.

Değerlerin bu yöntem türünün parametrelerine geçiş şeklini sınırlandırabilirsiniz:

- Bu tür yöntemlere yalnızca sabitler geçirilebilir. Sabitlerin değerleri tasarım zamanında tanımlanır.
- Yalnızca basit (temel) veri türleri bu tür parametreler için desteklenir. (Temel veri türleri şunlardır: tamsayı, gerçek, Boole, dize, vb.)

#### <a name="paths"></a>Yollar

Bir ifade yapılandırılmış bir veri kaynağına başvurduğunda, bu veri kaynağının belirli bir temel öğesini seçmek için bir yol tanımı kullanabilirsiniz. Yapılandırılmış veri kaynağının öğelerini tek tek ayırmak için bir nokta karakteri (.) kullanılır. Örneğin, mevcut ER veri modeli **InvoiceTransactions** veri kaynağını içerir ve bu veri kaynağı kayıtların listesini döndürür. **InvoiceTransactions** kayıt yapısı her ikisi de sayısal değerler döndüren **AmountDebit** ve **AmountCredit** alanlarını içerir. Bu nedenle, faturalanan tutarı hesaplamak için şu deyimi tasarlayabilirsiniz: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**.

#### <a name="functions"></a>İşlevler

Sonraki bölüm, ER deyimlerinde kullanılabilecek işlevleri açıklamaktadır. İfade bağlamının tüm veri kaynakları (geçerli ER veri modeli ya da ER biçimi ) çağırma işlevlerinin bağımsız değişkenleri listesine uygun işlevleri çağırma parametreleri olarak kullanılabilir. Sabitler çağırma işlevleri parametreleri olarak da kullanılabilir. Örneğin, mevcut ER veri modeli **InvoiceTransactions** veri kaynağını içerir ve bu veri kaynağı kayıtların listesini döndürür. **InvoiceTransactions** kayıt yapısı her ikisi de sayısal değerler döndüren **AmountDebit** ve **AmountCredit** alanlarını içerir. Bu sebeple, faturalanan tutarı hesaplamak için, dahili ER yuvarlama işlevini kullanan şu deyimi tasarlayabilirsiniz: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**.

## <a name="supported-functions"></a>Desteklenen işlevler

Aşağıdaki tablolar, ER veri modelleri ve ER raporları tasarlamak için kullanabileceğiniz veri düzenleme işlevleri açıklamaktadır. İşlevlerin listesi sabit değildir. Geliştiriciler listeyi genişletebilir. Kullanabileceğiniz işlevlerin listesini görmek için ER formül tasarımcısında işlevler bölmesini açın.

### <a name="date-and-time-functions"></a>Tarih ve saat işlevleri

| İşlev | Açıklama | Örnek |
|----------|-------------|---------|
| ADDDAYS (datetime, gün) | Belirtilen gün sayısını belirtilen tarih/saat değerine ekleyin. | **ADDDAYS (NOW(), 7)** bugünden yedi gün sonraki tarih ve saati döndürür. |
| DATETODATETIME (tarih) | Belirtilen tarih değerini tarih/saat değerine dönüştürün. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** geçerli Finance and Operations oturum tarihi olan Aralık 24, 2015'i **12/24/2015 12:00:00 AM** olarak döndürür. Bu örnekte, **CompInfo** **Finance and Operations/Table** türünde bir ER veri kaynağıdır ve CompanyInfo tablosuna referans verir. |
| NOW () | Geçerli Finance and Operations uygulama sunucusu tarihi ve saatini bir tarih/saat değeri olarak döndürür. | |
| TODAY () | Geçerli Finance and Operations uygulama sunucusu tarih ve saatini bir tarih değeri olarak döndürür. | |
| NULLDATE () | Bir **null** tarih değeri döndür. | |
| NULLDATETIME () | Bir **boş** tarih/saat değeri döndürür. | |
| DATETIMEFORMAT (datetime, biçim) | Belirtilen tarih/saat değerini belirtilen bir biçimdeki dizeye dönüştürür. (Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** Aralık 24, 2015 olan Finance and Operations uygulama sunucusu tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür. |
| DATETIMEFORMAT (datetime, biçim, kültür) | Belirtilen tarih/saat değerini ve [kültürü](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx) belirtilen bir biçimdeki dizeye dönüştürür. (Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (NOW(), "d", "de")** Aralık 24, 2015 olan geçerli Finance and Operations uygulama sunucusu tarihini seçilen Alman kültürünü temel alarak **"24.12.2015"** olarak döndürür. |
| SESSIONTODAY () | Geçerli Finance and Operations oturumu tarih ve saatini bir tarih değeri olarak döndürür. | |
| SESSIONNOW () | Geçerli Finance and Operations oturum tarihi ve saatini bir tarih/saat değeri olarak döndürür. | |
| DATEFORMAT (tarih, biçim) | Belirtilen tarihin, belirtilen biçimdeki dize olarak temsilini döndür. | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** Aralık 24, 2015 olan Finance and Operations oturum tarihini belirtilen özel biçimi temel alarak **"24-12-2015"** olarak döndürür. |
| DATEFORMAT (tarih, biçim, kültür) | Belirtilen tarih değerini, belirtilen biçimde ve [kültür](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)'de bir dizeye dönüştürür. (Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).) | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** Aralık 24, 2015 olan geçerli Finance and Operations oturumu tarihini seçilen Alman kültürünü temel alarak **"24.12.2015"** olarak döndürür. |
| DAYOFYEAR (tarih) | Ocak 1 ve belirtilen tarih arasındaki günlerin sayısının bir tamsayı temsilini döndürür. | **DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))** **61** döndürür. **DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))** **1** döndürür. |
| GÜN (tarih 1, tarih 2) | İlk belirtilen tarih ile ikinci belirtilen tarih arasındaki gün sayısını döndürür. İlk tarih ikinci tarihten sonra olduğunda pozitif bir değer döndürür; ilk tarih ikinci tarihle aynı olduğunda **0** (sıfır) değerini döndürür veya ilk tarih ikinci tarihten önceyse, negatif değer döndürür. | **DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS(NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))** **-1** döndürür. |

### <a name="data-conversion-functions"></a>Veri dönüştürme işlemleri

| İşlev | Tanım | Örnek |
|----------|-------------|---------|
| DATETODATETIME (tarih) | Belirtilen tarih değerini tarih/saat değerine dönüştürün. | **DATETODATETIME (CompInfo. 'getCurrentDate()')** geçerli Finance and Operations oturum tarihi olan Aralık 24, 2015'i **12/24/2015 12:00:00 AM** olarak döndürür. Bu örnekte, **CompInfo** **Finance and Operations/Table** türünde bir ER veri kaynağıdır ve CompanyInfo tablosuna referans verir. |
| DATEVALUE (dize, biçim) | Belirtilen dizenin, belirtilen biçimdeki tarih olarak temsilini döndür. | **DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")** belirtilen özel biçimi ve varsayılan uygulamanın **EN-US** kültürünü temel alarak Aralık 21, 2016 tarihini döndürür. |
| DATEVALUE (dize, biçim, kültür) | Belirtilen dizenin, belirtilen biçim ve kültürdeki tarih olarak temsilini döndür. | **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")** belirtilen özel biçim ve kültürü temel alarak Ocak 21, 2016 tarihini döndürür. Bununla birlikte, **DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")** belirtilen dizenin geçerli bir tarih olarak tanınmadığını kullanıcıya bildirmek için bir özel durum oluşturur. |
| DATETIMEVALUE (dize, biçim) | Belirtilen dizenin, belirtilen biçimdeki tarih/saat olarak temsilini döndür. | **DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")** belirtilen özel biçimi ve varsayılan uygulamanın **EN-US** kültürünü temel alarak 2:55:00 AM, Aralık 21, 2016 değerini döndürür. |
| DATETIMEVALUE (dize, biçim, kültür) | Belirtilen dizenin, belirtilen biçim ve kültürdeki tarih/saat olarak temsilini döndür. | **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")** belirtilen özel biçimi ve kültürü temel alarak 2:55:00 AM Aralık 21, 2016 değerini döndürür. Bununla birlikte **DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")** belirtilen dizenin geçerli bir tarih olarak tanınmadığını kullanıcıya bildirmek için bir özel durum oluşturur. |

### <a name="list-functions"></a>Liste işlevleri

<table>
<thead>
<tr>
<th>İşlev</th>
<th>Tanım</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr>
<td>SPLIT (input, uzunluk)</td>
<td>Belirtilen giriş dizesini her biri belirli uzunlukta alt dizelere bölün. Sonucu yeni bir liste olarak döndürün.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> <strong>STRING</strong> alanına sahip iki kaydı içeren yeni bir listeyi döndürür. İlk kayıttaki alan <strong>&quot;abc&quot;</strong> metnini içeriyor ve ikinci kayıttaki alan <strong>&quot;d&quot;</strong> metnini içeriyorsa.</td>
</tr>
<tr>
<td>BÖLME (giriş, ayırıcı)</td>
<td>Belirtilen giriş dizesini belirli sınırlayıcıya dayanarak alt dizelere bölün.</td>
<td><strong>BÖL (&quot;XAb aBy&quot;, &quot;aB&quot;)</strong>, <strong>DİZE</strong> alanına sahip üç kaydı içeren yeni bir listeyi döndürür. İlk kayıttaki alan, <strong>&quot;X&quot;</strong> metni, ikinci kayıttaki alan &quot;&nbsp;&quot; metni, üçüncü kayıttaki alan <strong>&quot;y&quot;</strong> metni içerir. Sınırlayıcı boşsa bir kayıt içeren yeni bir liste döner; kayıtta giriş metnini içeren <strong>DİZE</strong> alanı vardır. Giriş boşsa, yeni boş bir liste döner.
Giriş veya sınırlayıcı (boş) belirtilmezse, bir uygulama özel durum oluşturulur.</td>
</tr>
<tr>
<td>SPLITLIST (list, sayı)</td>
<td>Belirtilen listeyi, her biri belirtilen sayıda kayıt içeren toplu işleri bölün. Sonucu, aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:
<ul>
<li>Toplu işler düzenli listelerdir (<strong>Değer </strong>bileşen)</li>
<li>Geçerli toplu iş numarası (<strong>BatchNumber</strong>bileşeni)</li>
</ul>
</td>
<td>Aşağıdaki örnekte, üç kaydın kayıt listesi olarak <strong>Satırlar</strong> veri kaynağı oluşturulur. Bu liste her biri en çok iki kayıt içeren toplu işlere ayrılır.
<p><a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Aşağıdaki örnekte tasarlanmış biçim düzeni gösterilir. Bu biçim düzeninde, <strong>Satırlar</strong> veri kaynağına bağlamalar XML biçiminde çıktı üretmek için oluşturulur. Bu çıktı her toplu iş ve içindeki kayıtlar için ayrı ayrı düğümleri sunar.</p>
<p><a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a></p>
<p>Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.</p>
<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>
</td>
</tr>
<tr>
<td>LIST (record 1 [, record 2, …])</td>
<td>Belirtilen değişkenlerden oluşturulan yeni bir liste döndür.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong>, <strong>MainData</strong> ve <strong>OtherData</strong> alan listesinin, kayıt listelerinin tüm alanlarını içeren boş bir kaydı döndürür.</td>
</tr>
<tr>
<td>LISTJOIN (list 1, list 2, …)</td>
<td>Belirtilen değişkenlerin listesinden oluşturulan birleştirilmiş bir liste döndür.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> altı kaydın listesini döndürür; <strong>DİZE</strong> veri türündeki alanlardan biri tek harfler içerir.</td>
</tr>
<tr>
<td>ISEMPTY (liste)</td>
<td>Belirtilen liste herhangi bir öğe içermiyorsa <strong>DOĞRU</strong> döndürür. Aksi takdirde <strong>YANLIŞ</strong> döndürür.</td>
<td></td>
</tr>
<tr>
<td>EMPTYLIST (liste)</td>
<td>Belirtilmiş olan listeyi, liste yapısı için bir kaynak olarak kullanarak boş bir liste döndürür.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> <strong>SPLIT</strong> işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir liste döndürür.</td>
</tr>
<tr>
<td>FIRST (liste)</td>
<td>Eğer kayıt boş değilse, belirtilen listedeki ilk kaydı döndür. Aksi takdirde, bir özel durum ilan et.</td>
<td></td>
</tr>
<tr>
<td>FIRSTORNULL (liste)</td>
<td>Eğer kayıt boş değilse, belirtilen listedeki ilk kaydı döndür. Aksi takdirde bir <strong>null</strong> kaydı döndür.</td>
<td></td>
</tr>
<tr>
<td>LISTOFFIRSTITEM (liste)</td>
<td>Belirtilen listenin sadece ilk öğesini içeren bir liste döndür.</td>
<td></td>
</tr>
<tr>
<td>ALLITEMS (yol)</td>
<td>Bu işlev bir bellek içi seçim olarak çalışır. Belirtilen yolla eşleşen tüm öğelerin temsil edildiği yeni bir düzleştirilmiş liste döndürür. Yol, kayıt listesi veri türünün veri kaynağı öğesine geçerli veri kaynağı yolu olarak tanımlanmalıdır. Dize yolu ve tarih gibi veri öğeleri, ER ifade oluşturucuda tasarım zamanında hata vermelidir.</td>
<td>Eğer <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> veri kaynağı (DS) olarak girerseniz, <strong>COUNT( ALLITEMS (DS.Value))</strong>, <strong>3</strong> döndürür.</td>
</tr>
<tr>
<td>ALLITEMSQUERY (yol)</td>
<td>Bu işlev birleşik bir SQL sorgusu olarak çalışır. Belirtilen yolla eşleşen tüm öğelerin temsil edildiği yeni bir düzleştirilmiş liste döndürür. Belirtilen yol, kayıt listesi veri türünün veri kaynağı öğesine geçerli veri kaynağı yolu olarak tanımlanmalı ve en az bir ilişki içermelidir. Dize yolu ve tarih gibi veri öğeleri, ER ifade oluşturucuda tasarım zamanında hata vermelidir.</td>
<td>Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:
<ul>
<li>CustInvoiceTable tablosuna başvuran <strong>CustInv</strong> (<strong>Tablo kayıtları</strong> türü)</li> 
<li><strong>FILTER (CustInv, CustInv.InvoiceAccount = &quot;US-001&quot;)</strong> ifadesini içeren <strong>FilteredInv</strong> (<strong>Hesaplanan alan</strong> türü)</li>
<li><strong>ALLITEMSQUERY (FilteredInv.'&lt;Relations'.CustInvoiceJour.'&lt;Relations'.CustInvoiceTrans)</strong> ifadesini içeren <strong>JourLines</strong> (<strong>Hesaplanan alan</strong> türü)</li>
</ul>
<p><strong>JourLines</strong> veri kaynağını çağırmak için model eşlemenizi çalıştırırken aşağıdaki SQL deyimi çalıştırılır:</p>
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN CUSTINVOICETRANS T3 WHERE...
</td>
</tr>
<tr>
<td>ORDERBY (liste [ifade 1, ifade 2,...])</td>
<td>Belirtilen bağımsız değişkenlere göre sıralandıktan sonra belirtilen listeyi döndürür. Bu bağımsız değişkenler ifadeler olarak tanımlanabilir.</td>
<td><strong>Satıcı</strong>, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılsa,<strong>ORDERBY (Vendors, Vendors.'name()')</strong>, satıcıların isme göre sıralanan listesini artan sıraya göre dizilmiş şekilde döndürür.</td>
</tr>
<tr>
<td>REVERSE (liste)</td>
<td>Belirtilen listeyi ters sıralama düzeninde döndür.</td>
<td><strong>Satıcı </strong>, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong>, satıcıların isme göre sıralanan listesini azalan sıraya göre dizilmiş şekilde döndürür.</td>
</tr>
<tr>
<td>WHERE (liste, koşul)</td>
<td>Belirtilen koşula göre filtrelendikten sonra belirtilen listeyi döndürür. Belirtilen koşul bellekteki listeye uygulanır. Bu şekilde, <strong>WHERE</strong> işlevi <strong>FILTER</strong> işlevinden ayrılır.</td>
<td><strong>Satıcı</strong>, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong>, yalnızca grup 40'a dahil olan satıcıların listesini döndürür.</td>
</tr>
<tr>
<td>ENUMERATE (liste)</td>
<td>Belirtilen listenin numaralandırılmış kayıtlarından oluşan ve aşağıdaki öğeleri gösteren yeni bir liste döndürür:
<ul>
<li>Belirtilen liste kayıtları, düzenli olarak (<strong>Değer </strong>bileşeni) listeler</li>
<li>Geçerli kayıt dizini (<strong>Numara </strong>bileşeni)</li>
</ul>
</td>
<td>Aşağıdaki örnekte, <strong>Numaralandırılan</strong> veri kaynağı, VendTable tablosuna başvuran <strong>Satıcılar</strong> veri kaynağındaki satıcı kayıtlarının numaralandırılmış bir listesi olarak oluşturulur.
<p><a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a></p>
<p>Aşağıdaki örnekte biçim gösterilmiştir. Bu biçimde, veri bağlamaları XML biçiminde çıktı üretmek için oluşturulur. Bu çıktı ayrı ayrı satıcıları numaralandırılmış düğümler olarak gösterir.</p>
<p><a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a></p>
<p>Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.</p>
<a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a>
</td>
</tr>
<tr>
<td>COUNT (liste)</td>
<td>Eğer liste boş değilse, belirtilen listedeki kayıtların sayısını döndür. Aksi takdirde <strong>0</strong> (sıfır) döndürür.</td>
<td><strong>SPLIT</strong> işlevi iki kayıttan oluşan bir liste oluşturduğu için, <strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> <strong>2</strong> döndürür.</td>
</tr>
<tr>
<td>LISTOFFIELDS (yol)</td>
<td>Aşağıdaki türlerden birinin bağımsız değişkeninden oluşturulan kayıtlar listesini döndürür:
<ul>
<li>Model numaralandırma</li>
<li>Biçim numaralandırma</li>
<li>Kapsayıcı</li>
</ul>
<p>Oluşturulan liste aşağıdaki alanlara sahip kayıtları içerir:</p>
<ul>
<li>Dosya Adı</li>
<li>Etiket</li>
<li>Tanım</li>
</ul>
Çalışma zamanında, <strong>Etiket</strong> ve <strong>Açıklama</strong> alanları, biçimin dil ayarlarını temel alan değerler döndürür.
</td>
<td>Aşağıdaki örnekte, bir veri modelinde oluşturulan numaralandırma gösterilmektedir.
<p><a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a></p>
<p>Aşağıdaki örnek ayrıntıları göstermektedir:</p>
<ul>
<li>Veri kaynağı olarak bir rapora eklenen model numaralandırma.</li>
<li>Bir ER ifadesi <strong>LISTOFFIELDS</strong> işlevi parametresi olarak bir model numaralandırma kullanır.</li>
<li>Oluşturulan ER ifadesini kullanarak bir rapora eklenen kayıt listesi türünün veri kaynağı.</li>
</ul>
<p><a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a></p>
<p>Aşağıdaki örnek <strong>LISTOFFIELDS</strong> işlevi kullanılarak oluşturulan ve kayıt listesi türündeki veri kaynağına bağlı olan ER biçim öğelerini gösterir.</p>
<p><a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a></p>
<p>Aşağıdaki örnekte tasarlanan biçim çalıştırıldığında elde edilen sonuç gösterilir.</p>
<p><a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a></p>
<blockquote>[!NOTE] Ana DOSYA ve KLASÖR biçim öğelerinin dil ayarlarına uygun olarak, etiketler ve açıklamalar için çevrilen metin ER biçiminin çıktısına girilir.</blockquote>
</td>
</tr>
<tr>
<td>LISTOFFIELDS (yol, dil)</td>
<td>Model numaralandırması, biçim numaralandırması veya kapsayıcı gibi bir bağımsız değişkenden oluşturulan bir kayıt listesi döndürür. Oluşturulan liste aşağıdaki alanlara sahip kayıtları içerir:
<ul>
<li>Dosya Adı</li>
<li>Etiket</li>
<li>Tanım</li>
<li>Çevrildi</li>
</ul>
Çalışma zamanında, <strong>Etiket</strong> ve <strong>Açıklama</strong> alanları, biçimin dil ayarlarını ve belirtilen dili temel alan değerler döndürür. <strong>Çevrildi</strong> alanı <strong>Etiket</strong> alanının belirtilen dile çevrilmiş olduğunu belirtir.
</td>
<td>Örneğin, <strong>enumType</strong> veri modeli numaralandırması için <strong>enumType_de</strong> ve <strong>enumType_deCH</strong> veri kaynaklarını yapılandırmak üzere <strong>Hesaplanan alan</strong> veri kaynağı türünü kullanırsınız.
<ul>
<li>enumType_de = <strong>LISTOFFIELDS</strong> (enumType, &quot;de&quot;)</li>
<li>enumType_deCH = <strong>LISTOFFIELDS</strong> (enumType, &quot;de-CH&quot;)</li>
</ul>
<p>Bu durumda, bu çevirinin kullanılabilir olması durumunda, numaralandırma değeri etiketiki İsviçre Almancası dilinde almak için aşağıdaki ifadeyi kullanabilirsiniz. İsviçre Almanca çeviri kullanılamıyorsa, Almanca etiketi olur.</p>
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
</td>
</tr>
<tr>
<td>STRINGJOIN (liste, alan adı, ayırıcı)</td>
<td>Belirtilen listedeki belirtilen alanın art arda eklenmiş değerlerinden oluşan bir dize döndürür. Değerler belirtilen sınırlayıcı ile ayrılır.</td>
<td>Veri kaynağı (DS) olarak <strong>SPLIT(&quot;abc&quot; , 1)</strong> girerseniz, <strong>STRINGJOIN (DS, DS.Value, &quot;-&quot;)</strong> <strong>&quot;a-b-c&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>SPLITLISTBYLIMIT (liste, sınır değeri, sınır kaynağı)</td>
<td>Belirtilen listeyi alt listelerin yeni listesine ayırır ve kayıt listesi içeriğinde sonucu verir. <strong>Sınır değeri</strong> parametresi, orijinal listeyi bölmek için sınırın değerini tanımlar. <strong>Sınır kaynağı</strong> parametresi toplamın artırıldığı adımı tanımlar. Sınır kaynağı tanımlanan sınırı aştığında sınır, kaynak listedeki tek bir öğeye uygulanmaz.</td>
<td>Aşağıdaki şekilde bir biçim gösterilmektedir. 
<p><a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a></p>
<p>Aşağıdaki şekilde, biçim için kullanılan veri kaynakları gösterilmektedir.</p>
<p><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a></p>
<p>Aşağıdaki örnekte biçim çalıştırıldığında elde edilen sonuç gösterilir. Bu durumda, çıktı emtia maddelerinin düz listesi olur.</p>
<p><a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a></p>
<p>Aşağıdaki örneklerde, tek bir toplu iş 9 limitini geçmemesi gereken toplam ağırlığa sahip emtiaları içerdiğinde, emtia maddelerinin listesini toplu işlerde ayarlananla aynı biçimde gösterir.</p>
<p><a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a></p>
<p><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a></p>
<p>Aşağıdaki örnekte düzeltilen biçim çalıştırıldığında elde edilen sonuç gösterilir.</p>
<p><a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a></p>
<blockquote>[!NOTE] Sınırının kaynak (ağırlık) değeri (11) tanımlanan sınırı (9) geçtiğinden sınır, kaynak listedeki son maddeye uygulanmaz. Rapor oluştururken gerekirse alt listeleri yok saymak (atlamak) için <strong>WHERE</strong> işlevini veya ilgili biçim öğesinin <strong>Etkinleştirildi</strong> ifadesini kullanın.</blockquote>
</td>
</tr>
<tr>
<td>FİLTRE (liste, koşul)</td>
<td>Sorgu belirtilen koşula göre filtre uygulayacak şekilde değiştirildikten sonra belirtilen listeyi döndürür. <strong>WHERE</strong> işlevinden farklı olarak bu işlev, belirtilen koşul <strong>Tablo kayıtları</strong> türünün herhangi bir ER veri kaynağına veritabanı düzeyinde uygulanabilir. Liste ve koşul tablolar ve ilişkiler kullanılarak tanımlanabilir.</td>
<td><strong>Satıcı</strong>, VendTable tablosuna başvuran ER kaynağı olarak yapılandırılırsa, <strong>FILTER (Vendors, Vendors.VendGroup = &quot;40&quot;)</strong>, yalnızca grup 40'a dahil olan satıcıların listesini döndürür. <strong>Satıcı</strong>, VendTable tablosuna başvuran bir ER veri kaynağı olarak yapılandırılırsa ve <strong>parmVendorBankGroup</strong>, <strong>Dize</strong> veri türünde bir değer döndüren ER veri kaynağı olarak yapılandırılırsa, <strong>FILTER (Vendor.'&lt;Relations'.VendBankAccount, Vendor.'&lt;Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)</strong> yalnızca belirli bir banka grubuna ait satıcı hesaplarının bulunduğu bir liste döndürür.</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Mantıksal işlevler

| İşlev | Tanım | Örnek |
|----------|-------------|---------|
| CASE (ifade, seçenek 1, sonuç 1 \[, seçenek 2, sonuç 2\] … \[, varsayılan sonuç\]) | Belirtilen ifade değerini, belirtilen alternatif seçeneklere karşı değerlendirin. İfadenin değerine eşit olan seçeneğin sonucunu döndürür. Aksi takdirde, varsayılan sonuç belirtilmişse, isteğe bağlı varsayılan sonucu döndürür. (Varsayılan sonuç öncesinde bir seçenek olmayan son parametredir). | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "KIŞ", "11", "KIŞ", "12", "KIŞ", "")**, eğer geçerli Finance and Operations oturum tarihi Ekim ve Aralık arasındaysa, **KIŞ** dizesini döndürür. Aksi halde, boş bir dize döndürür. |
| IF (koşul, değer 1, değer 2) | Belirtilen koşul karşılandığında ilk belirtilen değeri döndürür. Aksi takdirde, ikinci belirtilen değeri döndürür. Değer 1 ve değer 2, kayıt veya kayıt listeleriyse, sonuç sadece her iki listede de mevcut olan alanları içerir. | **IF (1=2, "koşul karşılandı", "koşul karşılanmadı")**, **"koşul karşılanmadı"** dizesini döndürür. |
| NOT (koşul) | Belirtilen koşulun ters mantıksal değerini döndürür. | **DEĞİL (DOĞRU)**, **YANLIŞ** döndürür. |
| AND (koşul 1\[, koşul 2, …\]) | *Tüm* belirtilen koşullar doğruysa, **DOĞRU** döndür. Aksi takdirde **YANLIŞ** döndürür. | **VE (1=1, "a"="a")**,**DOĞRU** döndürür. **AND (1=2, "a"="a")** **YANLIŞ** döndürür. |
| OR (koşul 1\[, koşul 2, …\]) | *Tüm* belirtilen koşullar yanlışsa, **YANLIŞ** döndür. *Herhangi bir* belirtilen koşul doğruysa **DOĞRU** döndür. | **VEYA (1=2, "a"="a")**,**DOĞRU** döndürür. |
| VALUEIN (giriş listesi, liste öğe ifadesi) | Belirtilen girişin, belirtilen listede belirli bir öğe değerinin eşleşip eşleşmediğini belirler. Belirtilen girdi en az bir kayıt için çalışan belirtilen ifade sonucuyla eşleşiyorsa **DOĞRU** döner. Aksi takdirde **YANLIŞ** döndürür. **Giriş** parametresi bir veri kaynağı öğesinin yolunu gösterir. Bu öğenin değeri eşleşir. **Liste** parametresi, bir ifade içeren kayıtların listesi olarak kayıt listesi türünün bir veri kaynağı öğesinin yolunu gösterir. Bu öğenin değeri belirtilen giriş ile karşılaştırılır. **Liste öğe ifadesi** bağımsız değişkeni işaret eden ya da belirtilen listenin eşleştirmek için kullanılacak tek bir alan içeren bir ifadeyi temsil eder. | Örnek için sonra bölüme [Örnek: VALUEIN (giriş, liste, liste öğesi ifadesi)](#examples-valuein-input-list-list-item-expression) bakın. |

#### <a name="examples-valuein-input-list-list-item-expression"></a>Örnekler: VALUEIN (giriş listesi, liste öğe ifadesi)
Genel olarak, **VALUEIN** işlevi bir dizi **OR** koşuluna çevrilir:

(input = list.item1.value) OR (input = list.item2.value) OR …

##### <a name="example-1"></a>Örnek 1
Model eşlemeniz içinde şu veri kaynağını tanımladınız: **Liste** (**Hesaplanan alan** türü). Bu veri kaynağı **SPLIT ("a,b,c", ",")** ifadesini içeriyor.

**VALUEIN ("B", List, List.Value)** ifadesi olarak yapılandırılmış bir veri kaynağı çağrılıysa **TRUE** olarak döner. Bu durumda, **VALUEIN** işlevi aşağıdaki bir dizi koşula çevrilir:

**(("B" = "a") or ("B" = "b") or ("B" = "c"))**, where **("B" = "b")**, şuna eşit: **TRUE**

**VALUEIN ("B", List, LEFT(List.Value, 0))** ifadesi olarak yapılandırılmış bir veri kaynağı çağrılıysa **FALSE** olarak döner. Bu durumda, **VALUEIN** işlevi aşağıdaki koşula çevrilir:

**("B" = "")**, which isn't equal to **TRUE**

Böyle bir koşul metninde karakter sayısı üst sınırının 32.768 karakter olduğuna dikkat edin. Bu nedenle, çalışma zamanında bu sınırı aşan veri kaynakları oluşturmamanız gerekir. Sınır aşılırsa uygulama çalışmayı durdurur ve bir özel durum gönderilir. Örneğin, veri kaynağı **WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)** olarak yapılandırılmışsa ve **List1** ve **List2** listeleri büyük miktarda kayıt içeriyorsa bu durum ortaya çıkabilir.

Bazı durumlarda, **VALUEIN** işlevi **EXISTS JOIN** işleci kullanarak bir veritabanı ifadesi çevrilir. Bu davranış, **FİLTRE** işlevi kullanıldığında ve aşağıdaki koşullar sağlandığında olur:

- **SORGU İSTE** seçeneği kayıtlar listesi anlamına gelen **VALUEIN** işlevinin veri kaynağı için kapatılır. (Hiçbir ek koşul, çalışma zamanında bu veri kaynağına uygulanmaz.)
- Kayıtlar listesi anlamına gelen **VALUEIN** işlevinin veri kaynağı için hiçbir iç içe ifade yapılandırılmaz.
- **VALUEIN** işlevinin bir liste öğesi belirtilen veri kaynağının bir alanını belirtilir (bir ifade veya bir yöntem değil).

Bu örnekte daha önce açıklandığı gibi **WHERE** işlevi yerine bu seçeneği kullanmayı düşünün.

##### <a name="example-2"></a>Örnek 2

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- Intrastat tablosuna başvuran **In** (**Tablo kayıtları** türü)
- IntrastatPort tablosuna başvuran **Port** (**Tablo kayıtları** türü)

**FILTER (In, VALUEIN(In.Port, Port, Port.PortId)** olarak yapılandırılmış bir veri kaynağı çağrıldığında aşağıdaki SQL ifadesi Intrastat tablosunun filtre uygulanan kayıtlarını döndürmek için oluşturulur:

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

**dataAreaId** alanları için nihai SQL deyimi **IN** işleci kullanılarak oluşturulur.

##### <a name="example-3"></a>Örnek 3

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- **Le** (**Hesaplanan alan** türü), **SPLIT ("DEMF,GBSI,USMF", ",")** ifadesini içerir
- **In** (**Tablo kayıtları** türü), Intrastat tablosu anlamına gelir ve **Şirketler arası** seçeneği açıktır

**FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)** ifadesi olarak yapılandırılmış bir veri kaynağı çağrıldığında son SQL deyimi aşağıdaki koşulu içerir:

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

### <a name="mathematical-functions"></a>Matematik işlevi

| İşlev | Tanım | Örnek |
|----------|-------------|---------|
| ABS (numara) | Belirtilen sayının mutlak değerini döndürür. (Diğer bir deyişle, işareti olmadan sayıyı döndürür.) | **ABS (-1)**, **1** döndürür. |
| KUVVET (sayı, kuvvet) | Belirtilen pozitif sayının, belirtilen kuvvetine yükseltilmesinin sonucunu döndür. | **KUVVET (10, 2)**, **100** döndürür. |
| NUMBERVALUE (dize, ondalık ayırıcı, basamak gruplandırma ayırıcı) | Belirtilen dizeyi sayıya dönüştürün. Belirtilen ondalık basamak ayırıcısı ondalık sayısının tam sayısı ile kesirli sayıları arasında kullanılır. Belirtilen basamak gruplandırma ayırıcısı binler basamağı ayırıcısı olarak kullanılır. | **NUMBERVALUE("1 234,56", ",", " ")**, **1234.56** değerini döndürür. |
| VALUE (dize) | Belirtilen dizeyi sayıya dönüştürün. Virgül ve nokta karakterleri (.) ondalık ayırıcı olarak kabul edilir ve önde gelen bir tire (-), bir eksi işareti olarak kullanılır. Belirtilen dizenin sayısal olmayan karakterler içermesi durumunda bir özel durum oluşturur. | **DEĞER ("1 234,56")** bir istisna oluşturur. |
| ROUND (sayı, ondalık basamak) | Belirtilen sayıyı, ondalık basamağındaki sayısı yuvarladıktan sonra döndürür.<ul><li>**Ondalık** parametresinin değeri 0'dan (sıfır) büyükse, belirtilen sayı birçok ondalık basamağa yuvarlanır.</li><li>**Ondalık** parametresinin değeri **0** (sıfır) ise, belirtilen sayı en yakın tamsayıya yuvarlanır.</li><li>**Ondalık** parametresinin değeri 0'dan (sıfır) küçükse, belirtilen sayı ondalık basamağın soluna yuvarlanır.</li></ul> | **ROUND (1200.767, 2)** iki ondalık basamağa yuvarlar ve **1200.77** sonucunu döndürür. **ROUND (1200.767, -3)** 1.000'in en yakın katına yuvarlar ve **1000** döndürür. |
| ROUNDDOWN (sayı, ondalık basamak) | Belirtilen sayıyı, ondalık basamağındaki sayısı aşağı yuvarladıktan sonra döndürür.<blockquote>[!NOTE] Bu işlev **YUVARLA** işlevi gibi davranır ancak belirtilen sayıyı daima aşağı doğru (sıfıra doğru) yuvarlar.</blockquote> | **ROUNDDOWN (1200.767, 2)** iki ondalık basamağa aşağı yuvarlar ve **1200.76** sonucunu döndürür. **ROUNDDOWN (1700.767, -3)** 1.000'in en yakın katına aşağı yuvarlar ve **1000** döndürür. |
| ROUNDUP (sayı, ondalık basamak) | Belirtilen sayıyı, ondalık basamağındaki sayı yukarı yuvarladıktan sonra döndürür.<blockquote>[!NOTE] Bu işlev **YUVARLA** işlevi gibi davranır ancak belirtilen sayıyı daima yukarı doğru (sıfırdan uzağa doğru) yuvarlar.</blockquote> | **ROUNDUP (1200.763, 2)** iki ondalık basamağa yukarı yuvarlar ve **1200.77** sonucunu döndürür. **ROUNDUP (1200.767, -3)** 1.000'in en yakın katına yukarı yuvarlar ve **2000** döndürür. |

### <a name="data-conversion-functions"></a>Veri dönüştürme işlemleri

| İşlev | Açıklama | Örnek |
|----------|-------------|---------|
| VALUE (dize) | Belirtilen dizeyi sayıya dönüştürün. Virgül ve nokta karakterleri (.) ondalık ayırıcı olarak kabul edilir ve önde gelen bir tire (-), bir eksi işareti olarak kullanılır. Belirtilen dizenin sayısal olmayan karakterler içermesi durumunda bir özel durum oluşturur. | **DEĞER ("1 234,56")** bir istisna oluşturur. |
| NUMBERVALUE (dize, ondalık ayırıcı, basamak gruplandırma ayırıcı) | Belirtilen dizeyi sayıya dönüştürün. Belirtilen ondalık basamak ayırıcısı ondalık sayısının tam sayısı ile kesirli sayıları arasında kullanılır. Belirtilen basamak gruplandırma ayırıcısı binler basamağı ayırıcısı olarak kullanılır. | **NUMBERVALUE("1 234,56", ",", " ")** **1234.56** döndürür. |
| INTVALUE (dize) | Belirtilen dizenin tamsayı temsilini döndürür. Ondalık basamaklar kesilir. | **INTVALUE ("100.77")** **100** döndürür. |
| INTVALUE (sayı) | Belirtilen sayının tamsayı temsilini döndürür. Ondalık basamaklar kesilir. | **INTVALUE (-100.77)** **-100** döndürür. |
| INT64VALUE (dize) | Belirtilen dizenin int64 temsilini döndürür. Ondalık basamaklar kesilir. | **INT64VALUE ("22565422744")** **22565422744** döndürür. |
| INT64VALUE (numara) | Belirtilen sayının int64 temsilini döndürür. Ondalık basamaklar kesilir. | **INT64VALUE (22565422744.00)** **22565422744** döndürür. |

### <a name="record-functions"></a>Kayıt işlevleri

| İşlev | Açıklama | Örnek |
|----------|-------------|---------|
| NULLCONTAINER (liste) | Belirtilen kayıt listesi veya kayıt ile aynı yapıya sahip bir **null** kaydı döndürür.<blockquote>[!NOTE] Bu işlev artık kullanılmamaktadır. Bunun yerine **EMPTYRECORD** kullanın.</blockquote> | **NULLCONTAINER (SPLIT ("abc", 1))**, **SPLIT** işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür. |
| EMPTYRECORD (kayıt) | Belirtilen kayıt listesi veya kayıt ile aynı yapıya sahip bir **null** kaydı döndürür.<blockquote>[!NOTE] **Boş** kayıt, tüm alanlarda boş değeri bulunan kayıttır. Boş değer sayılar için **0** (sıfır), dizeler için boş bir dize vb.'dir.</blockquote> | **EMPTYRECORD (SPLIT ("abc", 1))**, **SPLIT** işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür. |

### <a name="text-functions"></a>Metin işlevleri

<table>
<thead>
<tr>
<th>İşlev</th>
<th>Tanım</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr>
<td>UPPER (dize)</td>
<td>Belirtilen dizeyi büyük harfe dönüştürdükten sonra döndürür.</td>
<td><strong>UPPER(&quot;Örnek&quot;)</strong>, <strong>&quot;ÖRNEK&quot;</strong> sonucunu döndürür.</td>
</tr>
<tr>
<td>LOWER (dize)</td>
<td>Belirtilen dizeyi küçük harfe dönüştürdükten sonra döndürür.</td>
<td><strong>LOWER(&quot;Örnek&quot;)</strong>, <strong>&quot;örnek&quot;</strong> sonucunu döndürür.</td>
</tr>
<tr>
<td>LEFT (dize, karakter sayısı)</td>
<td>Belirtilen dizenin başından belirtilen sayıda karakteri döndür.</td>
<td><strong>LEFT (&quot;Örnek&quot;, 3)</strong>, <strong>&quot;Örn&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>RIGHT (dize, karakter sayısı)</td>
<td>Belirtilen dizenin sonundan belirtilen sayıda karakteri döndür.</td>
<td><strong>SAĞ ("&quot;Örnek&quot;, 3)</strong>, <strong>&quot;nek&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>MID (dize, Başlangıç pozisyonu, karakter sayısı)</td>
<td>Belirtilen dizenin, belirtilen konumdan başlayarak, belirtilen sayıdaki karakterini döndür.</td>
<td><strong>MID (&quot;Örnek&quot;, 2, 3)</strong>, <strong>&quot;rne&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>LEN (dize)</td>
<td>Belirtilen dizedeki karakterlerin sayısını döndür.</td>
<td><strong>LEN (&quot;Örnek&quot;)</strong>, <strong>6</strong> döndürür.</td>
</tr>
<tr>
<td>CHAR (numara)</td>
<td>Belirtilen Unicode numarası tarafından başvuruda bulunulan karakter dizesini döndürür.</td>
<td><strong>CHAR (255)</strong>, <strong>&quot;ÿ&quot;</strong> döndürür.
<blockquote>[!NOTE] Bu işlevin döndürdüğü dize DOSYA biçimi üst öğesinde seçtiğiniz kodlamaya bağlıdır. Desteklenen kodlamalar listesi için bkz. <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodlama sınıfı</a>.</blockquote>
</td>
</tr>
<tr>
<td>CONCATENATE (dize 1 [, dize 2, …])</td>
<td>Tüm belirtilen metin dizelerini bir dizeye bağlandıktan sonra döndürür.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong>, <strong>&quot;abcdef&quot;</strong>döndürür.
<blockquote>[!NOTE] <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> ifadesi ayrıca <strong>&quot;abcdef&quot;</strong> döndürür.</blockquote>
</td>
</tr>
<tr>
<td>TRANSLATE (dize, kalıp, değiştirme)</td>
<td>Belirtilen desen dizesindeki tüm karakterlerin, belirtilen değiştirme dizesindeki karakterlerle değiştirildiği, belirtilmiş olan dizeyi döndürür.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> deseni değiştirir <strong>&quot;cd&quot;</strong>, şunun ile: <strong>&quot;GH&quot;</strong> ve bunu döndürür: <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr>
<td>REPLACE (dize, desen, değiştirme, normal ifade işareti)</td>
<td>Belirtilen <strong>normal ifade bayrağı</strong> parametresi <strong>doğru</strong> olduğunda, belirtilen dizeyi bu işlev için <strong>desen</strong> bağımsız değişkeni olarak belirtilen normal ifadeyi uygulayarak değiştirdikten sonra döndürür. Bu ifade, değiştirilmesi gereken karakterleri bulmakta kullanılır. Belirtilen <strong>değiştirme</strong> bağımsız değişkenindeki karakterler, bulunan karakterleri değiştirmek için kullanılır. Belirtilen <strong>normal ifade bayrağı</strong> parametresi <strong>yanlış</strong> ise, bu işlev <strong>TRANSLATE</strong> gibi davranır.</td>
<td><strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> üm sayısal olmayan karakterleri kaldıran bir normal ifade uygular ve <strong>&quot;19234564971&quot;</strong> döndürür. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, yanlış)</strong> <strong>&quot;cd&quot;</strong> desenini <strong>&quot;GH&quot;</strong> satırı ile değiştirir ve <strong>&quot;abGHef&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>TEXT (giriş)</td>
<td>Belirtilen giriş geçerli Finance and Operations örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrildikten sonra döndürür. <strong>gerçek</strong> türün değerleri için, dize dönüşümü iki ondalık basamakla sınırlıdır.</td>
<td>Finance and Operations örneğinin sunucu yerel ayarı <strong>EN-US</strong> olarak tanımlanırsa, <strong>TEXT (NOW ())</strong> geçerli Finance and Operations oturum tarihi olan Aralık 17, 2015 değerini <strong>&quot;12/17/2015 07:59:23 AM&quot;</strong> metin dizesi olarak döndürür. <strong>TEXT (1/3)</strong> <strong>&quot;0.33&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>FORMAT (dize 1, dize 2[, dize 3, …])</td>
<td>Belirtilen dizeyi, tüm <strong>%N</strong> oluşumlarını <em>n</em>'ci bağımsız değişken ile değiştirerek biçimlendirdikten sonra döndürür. Bağımsız değişkenler, dizelerdir. Bir parametre için bir bağımsız değişken sağlanmamışsa, parametre izede <strong>&quot;%N&quot;</strong> olarak döndürülür. <strong>gerçek</strong> türün değerleri için, dize dönüşümü iki ondalık basamakla sınırlıdır.</td>
<td>Aşağıdaki örnekte, <strong>PaymentModel</strong> veri kaynağı müşteri kayıtlarının listesini <strong>Müşteri</strong> bileşeni ve işleme tarihi değerini <strong>ProcessingDate</strong> alanı üzerinden döndürür.
<p><a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a></p>
<p>Seçilen müşteriler için elektronik dosya oluşturmak üzere tasarlanmış ER biçiminde veri kaynağı olarak <strong>PaymentModel</strong> seçilir ve işlem akışını denetler. Seçilmiş bir müşteri raporun işlendiği tarihte durdurulmuşsa, kullanıcıyı bilgilendirmek için bir özel durum oluşturulur. Bu tür bir işleme denetimi için tasarlanmış formül aşağıdaki kaynakları kullanabilir:</p>
<ul>
<li>Aşağıdaki metne sahip Finance and Operations SYS70894 etiketi:
<ul>
<li><strong>TR-TR dili için:</strong> &quot;Yazdırılacak hiçbir şey yok&quot;</li>
<li><strong>DE dili için:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Aşağıdaki metne sahip Finance and Operations SYS18389 etiketi:
<ul>
<li><strong>TR-TR dili için:</strong> &quot;Müşteri %1, %2 için durduruldu.&quot;</li>
<li><strong>DE dili için:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
<p>Tasarlanabilen formül şudur:</p>
<p>FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;))</p>
<p>Rapor <strong>Litware Retail</strong> müşterisi için Aralık 17, 2015 tarihinde <strong>EN-US</strong> kültüründe ve <strong>EN-US</strong> dilinde işlenmişse bu formül son kullanıcıya özel durum iletisi olarak sunulabilecek aşağıdaki metni içerir:</p>
<p>&quot;Yazdırılacak hiçbir şey yok. Müşteri Litware perakende 17/12/2015 için durduruldu.&quot;</p>
<p>Aynı rapor <strong>Litware Retail</strong> müşterisi için Aralık 17, 2015 tarihinde <strong>DE</strong> kültürü ve <strong>DE</strong> dilinde işlenmişse, formül başka bir tarih biçimini kullanan aşağıdaki metni döndürür:</p>
<p>&quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot;</p>
<blockquote>[!NOTE] Aşağıdaki sözdizimi, etiketler için ER formüllerinde kullanılır:
<ul>
<li><strong>Finance and Operations kaynaklarından etiketler için:</strong> <strong>@&quot;X&quot;</strong>, burada <strong>X</strong> Uygulama Nesne Ağacı (AOT) etiket kimliğidir.</li>
<li><strong>ER yapılandırmaları içinde bulunan etiketler için:</strong> <strong>@&quot;GER_LABEL:X&quot;</strong>, burada <strong>X</strong>, ER yapılandırma etiket kimliğidir.</li>
</ul>
</blockquote>
</td>
</tr>
<tr>
<td>NUMBERFORMAT (sayı, biçim)</td>
<td>Belirtilen sayının, belirtilen biçimdeki dize olarak temsilini döndür. (Desteklenen biçimler hakkında bilgi için bkz. <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standart</a> ve <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">özel</a>.) Bu işlevin çalıştırıldığı bağlam, sayıları biçimlendirmek için kullanılan kültürü belirler.</td>
<td>TR-TR kültürü için <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong>, <strong>&quot;%45,00&quot;</strong> döndürür. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong>, <strong>&quot;10&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>NUMERALSTOTEXT (sayı, dil, para birimi, para birimi adını yazdır bayrağı, ondalık basamaklar)</td>
<td>Belirtilen sayıyı, belirtilen dilde yazıldıktan (metin dizelerine dönüştürüldükten) sonra döndürür. Dil kodu isteğe bağlıdır. Boş dize olarak tanımlandığında, çalışma bağlamının dil kodu kullanılır. (Çalışılan bağlamın dil kodu oluşturulan klasör veya dosya için tanımlanır.) Para birimi kodu da isteğe bağlıdır. Boş dize olarak tanımlandığında, şirket para birimi kullanılır.
<blockquote>[!NOTE] <strong>Para birimi adını yazdır bayrağı</strong> ve <strong>ondalık basamak</strong> parametreleri yalnızca şu dil kodları için analiz edilir: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong> ve <strong>RU</strong>. Ek olarak, <strong>para birimi adını yazdır bayrağı</strong> parametresi yalnızca ülke veya bölge bağlamının para birimi adlarının gerilemesini destekleyen Finance and Operations şirketleri için analiz edilir.</blockquote>
</td>
<td><strong>NUMERALSTOTEXT (1234.56, &quot;EN&quot;, &quot;&quot;, false, 2)</strong> <strong>&quot;One Thousand Two Hundred Thirty Four and 56&quot;</strong> döndürür. <strong>NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, false, 0)</strong> <strong>&quot;Sto dwadzieścia&quot;</strong> döndürür. <strong>NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, true, 2)</strong> <strong>&quot;Сто двадцать евро 21 евроцент&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>PADLEFT (dize, uzunluk, doldurma karakterleri)</td>
<td>Belirtilen dizenin başlangıcının belirtilen karakterlerle doldurulduğu belirtilen uzunlukta bir dize döndürür.</td>
<td><strong>PADLEFT (&quot;1234&quot;, 10, &quot;&nbsp;&quot;)</strong> <strong>&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234&quot;</strong> metin dizesini döndürür.</td>
</tr>
<tr>
<td>TRIM (dize)</td>
<td>Belirtilen metin dizesini baştaki ve sondaki boşluklar kesildikten ve sözcükler arasındaki birden fazla boşluk kaldırıldıktan sonra döndürür.</td>
<td><strong>TRIM (&quot;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Sample&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;text&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&quot;)</strong>  <strong>&quot;Örnek metin&quot;</strong> döndürür.</td>
</tr>
<tr>
<td>GETENUMVALUEBYNAME (veri kaynağı yolu numaralandırması, değer etiket metni numaralandırması)</td>
<td>Belirli bir numaralandırma veri kaynağının değerini, numaralandırma etiketinin belirtilen metnini temel alarak döndürür.</td>
<td>Aşağıdaki örnekte, bir veri modelinde oluşturulan <strong>ReportDirection</strong> numaralandırması gösterilmektedir. Etiketlerin numaralandırma değerleri ile tanımlandığını unutmayın.
<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a></p>
<p>Aşağıdaki örnek ayrıntıları göstermektedir:</p>
<ul>
<li>Veri kaynağı <strong>$Direction</strong> olarak bir rapora eklenen <strong>ReportDirection</strong> model numaralandırması.</li>
<li>Bu işlevin parametresi olarak model numaralandırma kullanmak için tasarlanan <strong>$IsArrivals</strong> ER ifadesi. Bu ifadenin değeri <strong>DOĞRU</strong>'dur.</li>
</ul>
<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>
</td>
</tr>
<tr>
<td>GUIDVALUE (giriş)</td>
<td>Belirtilen <strong>Dize</strong> veri türündeki girişi <strong>GUID</strong> veri türünde bir veri öğesine dönüştürün.<blockquote>[!NOTE] Ters yönde dönüştürme yapmak için (diğer bir deyişle, <strong>GUID</strong> veri türünün belirtilen girişini <strong>Dize</strong> veri türünün veri öğesine dönüştürmek için), <strong>TEXT()</strong> işlevini kullanabilirsiniz.</blockquote></td>
<td>Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:
<ul>
<li><strong>GUIDVALUE (&quot;AF5CCDAC-F728-4609-8C8B-A4B30B0C0AA0&quot;)</strong> ifadesini içeren <strong>myID</strong> (<strong>Hesaplanan alan</strong> türü)</li>
<li>UserInfo tablosuna başvuran <strong>Users</strong> (<strong>Tablo kayıtları</strong> türü)</li>
</ul>
Bu veri kaynakları tanımlandığında, UserInfo tablosunu <strong>GUID</strong> veri türünde <strong>objectId</strong> alanıyla filtrelemek için <strong>FILTER (Users, Users.objectId = myID)</strong> gibi bir ifade kullanabilirsiniz.
</td>
</tr>
<tr>
<td>JSONVALUE (kod, yol)</td>
<td>Verileri, belirtilen koda göre skaler bir değer çıkarmak için belirtilen yolla erişilen JavaScript Nesne Gösterimi (JSON) biçiminde ayrıştırın.</td>
<td>Veri kaynağı <strong>$JsonField</strong>, JSON biçimindeki şu verileri içerir: <strong>{&quot;BuildNumber&quot;:&quot;7.3.1234.1&quot;, &quot;KeyThumbprint&quot;:&quot;7366E&quot;}</strong>. Bu veri kaynağı için, </strong>JSONVALUE ( &quot;BuildNumber&quot;, $JsonField)</strong>, <strong>Dize</strong> veri türünde <strong>7.3.1234.1</strong> döndürür.</td>
</tr>
</tbody>
</table>

### <a name="data-conversion-functions"></a>Veri dönüştürme işlemleri

| İşlev | Tanım | Örnek |
|----------|-------------|---------|
| TEXT (giriş) | Belirtilen giriş geçerli Finance and Operations örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrildikten sonra döndürür. **gerçek** türün değerleri için, dize dönüşümü iki ondalık basamakla sınırlıdır. | Finance and Operations örneğinin sunucu yerel ayarı **EN-US** olarak tanımlanırsa, **TEXT (NOW ())** geçerli Finance and Operations oturum tarihi olan Aralık 17, 2015 değerini **12/17/2015 07:59:23 AM** metin dizesi olarak döndürür. **TEXT (1/3)**, **"0.33"** döndürür. |
| QRCODE (dize) | Belirtilen dize için base64 ikili biçiminde Hızlı Yanıt Kodu (QR kodu) görüntüsü döndürür. | **QRCODE ("Örnek metin")** **U2FtcGxlIHRleHQ=** döndürür. |

### <a name="data-collection-functions"></a>Veri toplama işlevleri

| İşlev | Tanım | Örnek |
|----------|-------------|---------|
| FORMATELEMENTNAME () | Geçerli biçimin öğesinin adını döndürür. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında boş bir size döndürür. | Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için **ER Sayma ve toplama için çıktı biçiminde verileri kullanma** görev kılavuzuna (**BT hizmeti/çözüm bileşenleri alma/geliştirme** iş sürecinin parçasıdır) başvurun. |
| SUMIFS (toplamı alınacak temel dize, ölçüt aralığı1 dizesi, ölçüt değeri1 dizesi \[, ölçüt aralığı2 dizesi, ölçütlere değeri2 dizesi, ...\]) | Bu biçimi yürütme sırasında toplanan ve belirtilen koşulları (aralık ve değer çiftleri) karşılayan XML düğümlerinin (bir anahtar olarak tanımlanan ada sahip) değerlerine ait bir toplama döndürür. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında **0** (sıfır) değeri döndürür. | |
| SUMIF (toplama için temel dize, ölçüt aralığı dizesi, ölçüt değeri dizesi) | Bu biçimi yürütme sırasında toplanan ve belirtilen koşulu (aralık ve değer) karşılayan XML düğümlerinin (bir anahtar olarak tanımlanan ada sahip) değerlerine ait bir toplama döndürür. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında **0** (sıfır) değeri döndürür. | |
| COUNTIFS (ölçüt aralığı1 dizesi, ölçüt değeri1 dizesi \[, ölçüt aralığı2 dizesi, ölçütlere değeri2 dizesi, ...\]) | Biçimi yürütme sırasında toplanan ve belirtilen koşulları (aralık ve değer çiftleri) karşılayan XML düğüm sayısını döndürür. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında **0** (sıfır) değeri döndürür. | |
| COUNTIF (ölçüt aralığı dizesi, ölçüt değeri dizesi) | Biçimi yürütme sırasında toplanan ve belirtilen koşulu (aralık ve değer) karşılayan XML düğüm sayısını döndürür. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında **0** (sıfır) değeri döndürür. | |
| COLLECTEDLIST (ölçüt aralığı1 dizesi, ölçüt değeri1 dizesi \[, ölçüt aralığı2 dizesi, ölçütlere değeri2 dizesi, ...\]) | Biçimi yürütme sırasında toplanan ve belirtilen koşulları (aralık ve değer) karşılayan XML düğümleri için toplanmış değerler listesini döndürür. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında boş liste döndürür. | |

### <a name="other-business-domainspecific-functions"></a>Diğer (belirli iş etki alanı) işlevleri

| İşlev | Açıklama | Örnek |
|----------|-------------|---------|
| CONVERTCURRENCY (tutar, kaynak para birimi, hedef para birimi, tarih, şirket) | Belirtilen parasal tutarı kaynak para biriminden, belirtilen tarihte belirtilen Finance and Operations şirketinin ayarlarını kullanarak belirtilen hedef para birimine dönüştürür. | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")**, şimdiki oturum tarihinde, DEMF şirket ayarlarına dayalı olarak bir euro'nun ABD doları olarak karşılığını döndürür. |
| ROUNDAMOUNT (sayı, ondalık, yuvarlama kuralı) | Belirtilen yuvarlama kuralına göre belirtilen tutarı belirtilen ondalık basamak sayısına yuvarlar.<blockquote>[!NOTE] Yuvarlama kuralı Finance and Operations **RoundOffType** numaralandırmasının bir değeri olarak belirtilmelidir.</blockquote> | **model.RoundOff** parametresi **Aşağıya** olarak ayarlanırsa, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)** **1000.78** değerini döndürür. Eğer **model.RoundOff** parametresi **Normal** ya da **Yukarıya yuvarla** olarak ayarlanmışsa, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)**, **1000,79** değerini döndürür. |
| CURCredRef (basamak) | Belirtilen fatura numarasının basamaklarına dayalı olarak bir alacaklı başvurusu döndür. | **CURCredRef ("Satıcı-200002")**, **"2200002"** döndürür. |
| MOD\_97 (basamak) | Belirtilen fatura numarasının basamaklarına dayalı olarak bir alacaklı başvurusunu bir MOD97 ifadesi olarak döndür. | **MOD\_97 ("VEND-200002")**, **"20000285"** döndürür. |
| ISOCredRef (basamak) | Bir Uluslararası Standartlar Kuruluşu (ISO) alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak döndürür.<blockquote>[!NOTE] ISO uyumlu olmayan alfabelerden sembolleri elemek için, giriş parametresinin işleve gönderilmeden önce çevrilmesi gerekir.</blockquote> | **ISOCredRef ("VEND-200002")**, **"RF23VEND-200002"** döndürür. |
| CN\_GBT\_AdditionalDimensionID (dize, sayı) | Belirtilen ek mali boyut kodunu alın. **Dize** parametresinde, boyutlar virgülle ayrılmış kodlar olarak gösterilir. **Sayı** parametresi, dizedeki istenen boyutun sıra kodunu tanımlar. | **CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3)** **"CC"** döndürür. |
| GetCurrentCompany () | Bir kullanıcının oturum açmış olduğu tüzel kişiliğin (şirket) kodunun metin olarak gösterimini döndürür. | **GETCURRENTCOMPANY ()**, Finance and Operations'da **Contoso Entertainment System USA** şirketinde oturum açmış bir kullanıcı için **USMF** döndürür. |
| CH\_BANK\_MOD\_10 (basamaklar) | Belirtilen fatura numarasının basamaklarına dayalı olarak bir alacaklı başvurusunu bir MOD10 ifadesi olarak döndürür. | **CH\_BANK\_MOD\_10 ("VEND-200002")** **3** döndürür. |
| FA\_SUM (sabit kıymet kodu, değer modeli kodu, başlangıç tarihi, bitiş tarihi) | Belirtilen dönem için sabit kıymet tutarının hazırlanan veri kapsayıcısını döndürür. | **FA\_SUM ("COMP-000001", "Current", Date1, Date2)** **Date1** ile **Date2** arasındaki dönem için **"Current"**  değer modeline sahip **"COMP-000001"** sabit kıymet için hazırlanan veri kapsayıcısını döndürür. |
| FA\_BALANCE (sabit kıymet kodu, değer modeli kodu, raporlama yılı, raporlama tarihi) | Sabit kıymet bakiyesinin hazırlanan veri kapsayıcısını döndürür. Raporlama yılı, Finance and Operations'daki **AssetYear** numaralandırması değeri olarak belirtilmelidir. | **FA\_SUM ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())** geçerli Finance and Operations oturum tarihinde **"Current"** değer modeline sahip **"COMP-000001"** sabit kıymet bakiyeleri için hazırlanan veri kapsayıcısını döndürür. |
| TABLENAME2ID (dize) | Belirtilen tablo adı için tablo kodunun tam sayı olarak gösterimini döndürür. | **TABLENAME2ID ("Intrastat")** **1510** döndürür. |
| ISVALIDCHARACTERISO7064 (dize) | Belirtilen dize, geçerli bir uluslararası banka hesap numarasını (IBAN) temsil ediyorsa, **DOĞRU** boole değerini döndürür. Aksi takdirde, **YANLIŞ** Boole değeri döndürür. | **ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")**, **DOĞRU** döndürür. **ISVALIDCHARACTERISO7064 ("AT61")** **YANLIŞ** döndürür. |
| NUMSEQVALUE (numara serisi kodu, kapsamı, kapsam kimliği) | Belirtilen numara serisi kodu, kapsamı ve kapsam kimliğine dayalı bir numara serisinin yeni oluşturulan değeri döndürür. Kapsamın **ERExpressionNumberSequenceScopeType** sabit listesi (**paylaşılan**, **Tüzel kişilik**, veya **şirket**) değeri olarak belirtilmesi gerekir. **Paylaşılan** kapsamı için, kapsam kimliği olarak boş bir dize belirtin. **Şirket** ve **Tüzel kişilik** kapsamları için, kapsam kimliği olarak şirket kodu belirtin. **Şirket** ve **Tüzel kişilik** kapsamları için, kapsam kimliği olarak boş bir dize belirtirseniz geçerli şirket kodu kullanılır. | Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:<ul><li>**enumScope** (**Dynamics 365 for Operations numaralandırma** türü), başvuran için **ERExpressionNumberSequenceScopeType** numaralandırmay karşılık gelir</li><li>**NumSeq** (**Hesaplanan alan** türü), **NUMSEQVALUE ("Gene\_1", enumScope.Company, "")** ifadesini içerir</li></ul>**NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için yapılandırılmış **Gene\_1** numara serisinin yeni oluşturulan değeri geri döner. |
| NUMSEQVALUE (numara sıra kodu) | Bir numara sırasının belirtilen numara sırasına bağlı olarak yeni oluşturulan değeri, **Şirket** kapsamı ve (kapsam kimliği olarak) altında ER biçimi çalışan bağlam sağlayan şirketin kodu döner. | Model eşlemeniz içinde şu veri kaynağını tanımladınız: **NumSeq** (**Hesaplanan alan** türü). Bu veri kaynağı **NUMSEQVALUE ("Gene\_1")** ifadesini içeriyor. **NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için yapılandırılmış **Gene\_1** numara serisinin yeni oluşturulan değeri geri döner. |
| NUMSEQVALUE (numara sıra kodu kayıt kimliği) | Belirtilen numara serisi kayıt kimliğine dayalı bir numara serisinin yeni oluşturulan değeri döndürür. | Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:<ul><li>LedgerParameters tablosuna başvuran **LedgerParms** (**Tablo** türü)</li><li>**NumSeq** (**Hesaplanan alan** türü), **NUMSEQVALUE (LedgerParameters.'numRefJournalNum()'.NumberSequenceId)** ifadesini içerir</li></ul>**NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için Genel muhasebe parametrelerinde yapılandırılmış Gene1 numara serisinin yeni oluşturulan değeri geri döner. Bu numara serisi benzersiz biçimde günlükleri tanıtır ve hareketleri birbirine bağlayan toplu iş numarası görevi görür. |

### <a name="functions-list-extension"></a>Liste uzantı işlevleri

ER, ER ifadelerinde kullanılan işlevlerin listesini genişletmenize olanak sağlar. Bazı mühendislik çabaları gereklidir. Ayrıntılı bilgi için bkz: [Elektronik raporlama işlevlerinin listesini genişletme](general-electronic-reporting-formulas-list-extension.md).

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Elektronik raporlama (ER) işlev listesini genişletme](general-electronic-reporting-formulas-list-extension.md)

