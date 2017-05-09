---
title: "Elektronik raporlama (Kural Yöneticisi) içinde Formül Tasarımcısı"
description: "Bu konu, formül tasarımcısının Elektronik raporlamada (ER) nasıl kullanılacağını açıklar. Belirli bir elektronik belge için ER içerisinde bir biçim tasarladığınızda, söz konusu belgenin gereksinimlerini karşılamak ve biçimlendirmek için Microsoft Excel benzeri formülleri veri dönüştürme için kullanabilirsiniz. Farklı türde işlevler desteklenmektedir -  metin, tarih ve saat, matematiksel mantıksal, bilgi, veri türü dönüştürme ve diğer (iş etki alanına özel işlevler)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ac8d6c064ca826cc1c2fed07578ca9ce0c66ef66
ms.lasthandoff: 03/31/2017


---

# <a name="formula-designer-in-electronic-reporting"></a>Elektronik raporlama (Kural Yöneticisi) içinde Formül Tasarımcısı

[!include[banner](../includes/banner.md)]


Bu konu, formül tasarımcısının Elektronik raporlamada (ER) nasıl kullanılacağını açıklar. Belirli bir elektronik belge için ER içerisinde bir biçim tasarladığınızda, söz konusu belgenin gereksinimlerini karşılamak ve biçimlendirmek için Microsoft Excel benzeri formülleri veri dönüştürme için kullanabilirsiniz. Farklı türde işlevler desteklenmektedir -  metin, tarih ve saat, matematiksel mantıksal, bilgi, veri türü dönüştürme ve diğer (iş etki alanına özel işlevler).

<a name="formula-designer-overview"></a>Formül tasarımcısına genel bakış
-------------------------

Elektronik raporlama (ER), formül tasarımcısını destekler. Bu nedenle, tasarım zamanında aşağıdaki görevler için çalışma zamanında kullanılabilecek ifadeler yapılandırabilirsiniz:

-   Microsoft Dynamics 365 for Operations veritabanından alınan verileri dönüştürmek ve bu verileri ER biçimleri için (filtreleme, gruplama, veri türü dönüştürme vb.) bir veri kaynağı olmak üzere tasarlanmış ER veri modelinde doldurmak.
-   Elektronik raporlama oluşturmaya gönderilecek biçimlendirme verisinin belirli bir ER biçiminin (talep edilen dil, kültür, kodlama vb. gibi) düzeni ve koşulları ile uyumlu olması gerekir.
-   Elektronik belge oluşturma işlemini denetleme (veri işlemeye, belgenin oluşturulmasının kesilmesine, son kullanıcılar için iletiler atılmasına vb. bağlı olarak belirli biçim öğelerinin çıktısını etkinleştirme/devre dışı bırakma).

Formül tasarımcısı sayfası aşağıdakilerden birini gerçekleştirdiğinizde açılabilir:

-   Veri kaynağı maddelerini veri modeli bileşenlerine bağlayın.
-   Veri kaynağı maddelerini biçim bileşenlerine bağlayın.
-   Veri kaynaklarının parçası olarak hesaplanan alanların bakımını tamamlayın.
-   Kullanıcı giriş parametreleri için görünürlük koşullarını tanımlayın.
-   Biçimin dönüşümlerini tasarlayın.
-   Biçimin bileşenlerinin etkinleştirme koşullarını tanımlayın.
-   Biçimin DOSYA bileşenleri için dosya adlarını tanımlayın.
-   İşlem denetimi doğrulamaları için koşulları tanımlayın.
-   İşlem denetimi doğrulamaları için ileti metnini tanımlayın.

## <a name="designing-er-formulas"></a>ER formülleri tasarlama
### <a name="data-binding"></a>Veri ilişkilendirme

ER formül tasarımcısı, veri kaynaklarından alınan verinin, söz konusu veri veri tüketicisinde çalışma zamanında kullanılabilecek şekilde dönüştürecek bir ifade tanımlamak için kullanılabilir:

-   Dynamics 365 for Operations veri kaynaklarından ve çalışma zamanı parametrelerinden ER veri modeline.
-   ER veri modelinden ER biçimine.
-   Dynamics 365 for Operations veri kaynaklarından ve çalışma zamanı parametrelerinden ER veri biçimine.

Bu tür bir ifadenin tasarımı aşağıda gösterilmiştir. Bu örnekte ifade, Dynamics 365 for Operations **Intrastat** tablosunun **Intrastat.AmountMST** alanının değerini, değer iki ondalık basamağa yuvarlandıktan sonra döndürür. [![resim-ifadesi-bağlama](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg) Aşağıda, bu tür bir ifadenin nasıl kullanılabileceği gösterilmiştir. Bu örnekte, tasarlanmış ifadenin sonucu, **Vergi raporlama modeli** veri modelinin **Transaction.InvoicedAmount** bileşeninde doldurulur. [![resim-ifade-baglama2](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg) Çalışma zamanında, tasarlanmış formül **ROUND (Intrastat.AmountMST, 2)**, **Intrastat** tablosunun **AmountMST** alanının değerini iki ondalık sayıya yuvarlar ve yuvarlanmış değeri **Vergi raporlama** veri modelinin **Transaction.InvoicedAmount** bileşenine doldurur.

### <a name="data-formatting"></a>Veri biçimlendirme

ER formül tasarımcısı, veri kaynaklarından alınan verinin, söz konusu veri, elektronik belgenin oluşturulmasında kullanılabilecek şekilde biçimlendirecek bir ifade tanımlamak için kullanılabilir. Bir biçim olarak yeniden kullanılacak tipik bir kural olarak uygulanacak bir biçimlendirmeniz varsa, bu biçimlendirmeyi, tek seferde bir biçimlendirme yapılandırmasında, biçimlendirme ifadesine sahip bir adlandırılmış bir dönüştürmesi olarak kullanıma sokabilirsiniz. Daha sonra bu adlandırılan dönüştürme oluşturulmuş ifadeye göre hangi çıktının biçimlendirilmesi gerektiği birçok biçimi bileşenler ile bağlanabilir. Bu tür bir dönüştürmenin tasarımı aşağıda gösterilmiştir. Bu örnekte, **TrimmedString** dönüşümü, **dize** veri türünden gelen verileri alır ve baştaki ve sondaki boşlukları dize değerini döndürdüğünde keser. [![resim-dönüşüm-tasarımı](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg) Aşağıdaki çizim bu tür bir dönüştürmenin nasıl kullanılabileceğini gösterir. Bu örnekte, çalışma zamanında elektronik belge oluşturmasına metni çıktı olarak gönderen çeşitli biçim bileşeni **TrimmedString** dönüştürmesine adıyla başvururlar. [![resim-dönüşüm-kullanımı](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg) Biçim bileşenleri **TrimmedString** dönüşümüne referansta bulunduğunda (örneğin, önceki çizimdeki **partyName** bileşeni) bu, oluşturulan belgeye metni çıktı olarak gönderir. Metin baştaki ve sondaki boşlukları içermez. Tek tek uygulanması zorunlu olan bir biçimlendirmeniz varsa, bu biçimlendirmeyi belirli bir biçim bileşeninin bir bağlamasının tekil ifadesi olarak tanıtabilirsiniz. Aşağıdaki çizim bu türde bir ifadeyi gösterir. Bu örnekte **partyType** biçim bileşeni, veri kaynağına **Model.Company.RegistrationType** alanından gelen veriyi bir ifade yardımıyla büyük harfe dönüştüren ve bu metni çıktı olarak elektronik belgeye gönderir. [![resim-formül-ile-bağlama](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

### <a name="process-flow-control"></a>İşlem akış denetimi

ER formül tasarımcısı, belge oluşturma işlem akışını denetleyen ifadeleri tanımlamak için kullanılabilir. Aşağıdakileri yapabilirisiniz:

-   Bir belge oluşturma işleminin ne zaman durdurulması gerektiği koşullarını tanımlayın.
-   Durdurulan işlemler hakkında son kullanıcıya iletiler oluşturan veya devam eden rapor oluşturma işlemleri hakkında yürütme günlüğü iletileri oluşturan ifadeleri belirtin.
-   Oluşturma belgelerinin dosya adlarını belirtin ve bunların oluşturulma koşullarını denetleyin.

İşlem akışı denetiminin her kuralı ayrı ayrı bir doğrulama olarak tasarlanmıştır. Aşağıdaki çizim bu türde bir doğrulamayı gösterir. u örnekteki yapılandırmanın bir açıklaması aşağıdadır:

-   **INSTAT** düğümü, oluşturma XML dosyasında oluşturulduğunda doğrulama değerlendirilir.
-   Hareketin listesi boşsa, doğrulama işlem yürütmesini durdurur ve **YANLIŞ** döndürür.
-   Doğrulama, kullanıcının tercih ettiği dilde SYS70894 etiket metnini içeren bir hata iletisi döndürür.

[![resim-doğrulama](./media/picture-validation.jpg)](./media/picture-validation.jpg) Doğrulama örneği ER formül tasarımcısı elektronik belgenin oluşturulması ve dosya oluşturma işlemini denetlemek için bir dosya adı belirtmekte de kullanılabilir. Aşağıdaki çizim, bu türdeki bir işlem akış denetiminin tasarımını gösterir. u örnekteki yapılandırmanın bir açıklaması aşağıdadır:

-   **model.Intrastat** veri kaynağının kayıt listesi, her biri 1.000 kayda kadar içeren çeşitli toplu işlere bölünmüştür.
-   Çıktı her toplu işlem için XML biçiminde oluşturulmuş bir dosya içeren bir zip dosyası oluşturur.
-   Bir ifade, elektronik belge oluşturması için dosya adı ve dosya uzantısını birleştirerek bir dosya adı döndürür. İkinci toplu iş ve tüm sonraki toplu işler için, dosya adı toplu iş kimliğini bir sonek olarak içerir.
-   Bir ifade (**DOĞRU** döndürerek) en az bir kayıt içeren toplu işler için dosya oluşturma işlemini etkinleştirir.

[![resim-dosya-kontrolü](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

### <a name="basic-syntax"></a>Temel sözdizimi

ER ifadeleri aşağıdaki öğelerden birini veya tümünü içerebilirler:

-   Sabitler
-   İşleçler
-   Referanslar
-   Yollar
-   İşlevler

#### <a name="constants"></a>Sabitler

İfadeler tasarlarken metin veya sayısal sabitler (hesaplanmayan değerler) içeren ifadeler kullanabilirsiniz. Örneğin **VALUE ("100") + 20 **ifadesi, sayısal sabit 20 ve dize sabiti "100" kullanır ve **120** sayısal değerini döndürür. ER formül tasarımcısı kaçış sıralarını destekler. Bu özellik, ifade dizesinin bir bölümünün farklı ele alınması gerektiğini belirtebileceğiniz anlamına gelir. Örneğin **"Leo Tolstoy ""Savaş ve Barış"" Cilt 1""** ifadesi aşağıdaki metin dizesini döndürür: **Leo Tolstoy "Savaş ve Barış" Cilt 1**.

#### <a name="operators"></a>İşleçler

Aşağıdaki tablo, toplama, çıkarma, bölme ve çarpma gibi temel matematik işlemleri gerçekleştirmek için kullanabileceğiniz aritmetik işleçleri gösterir.

| İşleç | Anlamı              | Örnek |
|----------|----------------------|---------|
| +        | Fark hesap eki             | 1+2     |
| -        | Çıkartma Olumsuzluğu | 5-2 -1  |
| \*       | Çarpma       | 7\*8    |
| /        | Bölüm             | 9/3     |

Aşağıdaki tablo, iki değeri karşılaştırmak için kullanabileceğiniz desteklenen karşılaştırma işleçlerini gösterir.

| İşleç | Anlamı                  | Örnek    |
|----------|--------------------------|------------|
| =        | Eşittir                    | X=Y        |
| &gt;     | Büyüktür             | X&gt;Y     |
| &lt;     | Küçüktür                | X&lt;Y     |
| &gt;=    | Büyüktür veya eşittir | X&gt;=Y    |
| &lt;=    | Küçüktür veya eşittir    | X&lt;=Y    |
| &lt;&gt; | Eşit değil             | X&lt;&gt;Y |

Ayrıca bir veya daha fazla metin dizesini tek bir metin parçası içine birleştirmek için veya metin birleştirme işleci olarak bir ampersan (&) kullanabilirsiniz.

| İşleç | Anlamı     | Örnek                                        |
|----------|-------------|------------------------------------------------|
| &        | Art arda eklemek | "Yazdırılacak bir şey yok" & ": " & "kayıt bulunamadı" |

#### <a name="operator-precedence"></a>İşleç önceliği

Bir bileşik ifadenin parçalarının hangi sırada değerlendirilecekleri önemlidir. Örneğin, **1 + 4 / 2** deyiminin sonucu, bölme işleminin mi yoksa toplama işleminin mi önce gerçekleşeceğine göre farklılık göstermektedir. Bir ifadenin nasıl değerlendirileceğini açıkça tanımlamak için parantezleri kullanabilirsiniz. Örneğin, toplama işlemi önce yapılması gerektiğini belirtmek için yukarıdaki ifadeyi şuna değiştirebilirsiniz **(1 + 4) / 2**. Eğer bir ifadede gerçekleştirilmesi gereken işleçlerin sırası özellikle belirtilmemişse sıralama, desteklenen işleçlerin varsayılan önceliğine dayandırılır. Aşağıdaki tablolar, işleçleri ve her birine atanan önceliği gösterir. Daha yüksek bir önceliğe sahip işleçler (örneğin, 7) daha düşük önceliğe sahip işleçlerden önce değerlendirilirler (örneğin, 1).

| Öncelik | İşleçler      | Sözdizimi                                                   |
|------------|----------------|----------------------------------------------------------|
| 7          | Gruplama       | ( … )                                                    |
| 6          | Üye erişimi  | … 'i tıklatın. …                                                    |
| 5          | İşlev çağrısı  | … ( … )                                                  |
| 4          | Çarpımsal | … \* … … / …                                             |
| 3          | Eklenecek       | … + … … - …                                              |
| 2          | Karşılaştırma     | … &lt; … … &lt;= … … =&gt; … … &gt; … … = … … &lt;&gt; … |
| 1          | Ayrılma     | … , …                                                    |

Aynı satırda olan işleçler eşit önceliğe sahiptirler. Eğer bir ifade bu işleçlerden bir taneden fazla içeriyorsa, ifade soldan sağa değerlendirilir. Örneğin, **1 + 6 / 2 \* 3 &gt; 5** ifadesi, **doğru** sonucunu verir. Deyimlerin okunmasını ve bakımını daha kolay hale getirmek için, deyimlerin arzu edilen değerlendirme sıralarını, parantezler kullanarak açıkça belirtmenizi tavsiye ederiz.

#### <a name="references"></a>Referanslar

Bir ifadenin tasarımında kullanılabilir olan bir mevcut ER bileşeninin tüm veri kaynakları (bir model ya da bir biçim), adlandırılmış referanslar olarak kullanılabilirler. Örneğin, mevcut ER veri modeli, **DATATIME** veri türünün değerini döndüren **ReportingDate** veri kaynağını içerir. Bu değeri oluşturulan belgede doğru biçimlendirmek için veri kaynağına ifadede şu şekilde referans gösterebilirsiniz **DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy"** Referans gösterilen bir veri kaynağının adındaki, alfabenin bir harfini temsil etmeyen tüm karakterlerden önce bir tek tırnak işareti (') gelmelidir. Referans gösterilen veri kaynağı alfabede temsil edilmeyen en az bir simgeyi içeriyorsa (örneğin noktalama işaretleri ya da diğer yazılı simgeler), adın tek tırnak işaretleri içerisine alınması gerekir. Burada bazı örnekler verilmiştir:

-   **Today's date & time** veri kaynağının bir ER deyiminde şu şekilde referans gösterilmiş olması gerekir **'Today''s date & time'**
-   **Müşteriler** veri kaynağının **name()** yöntemi, bir ER deyimi içerisinde aşağıdaki gibi referans gösterilmelidir: **Customers.'name()'**

#### <a name="path"></a>Yol

Bir ifade yapılandırılmış bir veri kaynağına başvurduğunda, bu veri kaynağının belirli bir temel öğesini seçmek için bir yol tanımı kullanabilirsiniz. Yapılandırılmış veri kaynağının öğelerini tek tek ayırmak için bir nokta karakteri (.) kullanılır. Örneğin, mevcut ER veri modeli, kayıtların bir listesini döndüren **InvoiceTransactions** veri kaynağını içerir. ** InvoiceTransactions** kayıt yapısı sayısal değerler döndüren **AmountDebit** ve **AmountCredit** alanlarını içerir. Bu nedenle, faturalanan tutarı hesaplamak için aşağıdaki deyimi tasarlayabilirsiniz: **InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit**

#### <a name="functions"></a>İşlevler

Sonraki bölüm, ER deyimlerinde kullanılabilecek işlevleri açıklamaktadır. İfade bağlamının tüm veri kaynakları (geçerli ER veri modeli ya da ER biçimi ) ve bunun yanı sıra sabitler çağırma işlev değişkenleri listesine uygun işlevleri çağırma parametreleri olarak kullanılabilir. Örneğin, mevcut ER veri modeli, kayıtların bir listesini döndüren **InvoiceTransactions** veri kaynağını içerir. ** InvoiceTransactions** kayıt yapısı sayısal değerler döndüren **AmountDebit** ve **AmountCredit** alanlarını içerir. Bu sebeple, faturalanan tutarı hesaplamak için, dahili ER yuvarlama işlevini kullanan aşağıdaki deyimi tasarlayabilirsiniz: **ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)**

## <a name="supported-functions"></a>Desteklenen işlevler
Aşağıdaki tablolar, ER veri modelleri ve ER raporları tasarlamak için kullanabileceğiniz veri düzenleme işlevleri açıklamaktadır. İşlevlerin listesi sabit değildir ve geliştiriciler tarafından genişletilebilir. Kullanabileceğiniz işlevlerin listesini görmek için ER formül tasarımcısında işlevler bölmesine erişin.

### <a name="date-and-time-functions"></a>Tarih ve saat işlevleri

| İşlev                                   | Açıklama                                                                                                                                                                                                                                                                                                                                                      | Örnek                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADDDAYS (datetime, gün)                   | Belirtilen gün sayısını belirtilen datetime değerine ekleyin.                                                                                                                                                                                                                                                                                                | **ADDDAYS (NOW(), 7)** bugünden yedi gün sonraki tarih ve saati döndürür.                                                                                                                                                                                                                            |
| DATETODATETIME (tarih)                      | Belirtilen tarih değerini tarih/saat değerine dönüştürür.                                                                                                                                                                                                                                                                                                            | **DATETODATETIME (CompInfo. 'getCurrentDate()')** geçerli Dynamics 365 for Operations oturum tarihi olan 24/12/2015 tarihini **24/12/2015 00:00:00** olarak çevirir. Bu örnekte, **CompInfo**, CompanyInfo tablosuna referans gösteren **Dynamics 365 for Operations/Table** türünde bir ER veri kaynağıdır. |
| NOW ()                                     | Geçerli Dynamics 365 for Operations uygulama sunucusu oturum tarih ve saatini bir datetime değerine döndürür.                                                                                                                                                                                                                                                             |                                                                                                                                                                                                                                                                                                       |
| TODAY ()                                   | Geçerli Dynamics 365 for Operations uygulama sunucusu oturum tarihini bir tarih değerine döndürür.                                                                                                                                                                                                                                                                          |                                                                                                                                                                                                                                                                                                       |
| NULLDATE ()                                | Bir **null** tarih değeri döndür.                                                                                                                                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                       |
| NULLDATETIME ()                            | Bir **null** datetime değeri döndür.                                                                                                                                                                                                                                                                                                                                |                                                                                                                                                                                                                                                                                                       |
| DATETIMEFORMAT (datetime, biçim)          | Belirtilen datetime değerini belirtilen bir biçimdeki dizeye dönüştürmek. (Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx).)                                                                        | **DATETIMEFORMAT (NOW(), "dd-MM-yyyy")** geçerli Dynamics 365 for Operations uygulama sunucusu tarihi olan 24/12/2015 tarihini belirtilen özel biçime göre **"24-12-2015"** tarihine döndürür.                                                                                                          |
| DATETIMEFORMAT (datetime, biçim, kültür) | Belirtilen datetime değerini ve [kültürü](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx) belirtilen bir biçimdeki dizeye dönüştürmek. (Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)). | **DATETIMEFORMAT (NOW(), "d", "de")** geçerli Dynamics 365 for Operations uygulama sunucusu tarihi olan 24/12/2015 tarihini, seçilen Alman kültürüne göre **"24.12.2015"** tarihine döndürür.                                                                                                             |
| SESSIONTODAY ()                            | Geçerli Dynamics 365 for Operations oturum tarihini bir tarih değerine döndürür.                                                                                                                                                                                                                                                                                      |                                                                                                                                                                                                                                                                                                       |
| SESSIONNOW ()                              | Geçerli Dynamics 365 for Operations oturum tarihini ve saatini tarih/saat değerine döndürür.                                                                                                                                                                                                                                                                         |                                                                                                                                                                                                                                                                                                       |
| DATEFORMAT (tarih, biçim)                  | Belirtilen biçimi kullanarak tarihin dize gösterimini verir.                                                                                                                                                                                                                                                                                                    | **DATEFORMAT (SESSIONTODAY (), "dd-MM-yyyy")** geçerli Dynamics 365 for Operations oturum tarihi olan 24/12/2015 tarihini belirtilen özel biçime göre "**"24-12-2015"**" tarihine döndürür.                                                                                                                      |
| DATEFORMAT (tarih, biçim, kültür)         | Belirtilen tarih değerini, belirtilen biçimde ve [kültür](https://msdn.microsoft.com/en-us/goglobal/bb896001.aspx)'de bir dizeye dönüştürür. (Desteklenen biçimler hakkında daha fazla bilgi için bkz. [standart](https://msdn.microsoft.com/en-us/library/az4se3k1(v=vs.110).aspx) ve [özel](https://msdn.microsoft.com/en-us/library/8kb3ddd4(v=vs.110).aspx)).     | **DATETIMEFORMAT (SESSIONNOW (), "d", "de")** geçerli Dynamics 365 for Operations uygulama sunucusu tarihi olan 24/12/2015 tarihini seçilen Alman kültürüne göre **"24.12.2015"** tarihine döndürür.                                                                                                                       |

### <a name="list-functions"></a>Liste işlevleri

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>İşlev</th>
<th>Açıklama</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>SPLIT (input, uzunluk)</td>
<td>Belirtilen giriş dizesini her biri belirli uzunlukta alt dizelere bölün. Sonucu yeni bir liste olarak döndürün.</td>
<td><strong>SPLIT (&quot;abcd&quot;, 3)</strong> <strong>STRING</strong> alanına sahip iki kaydı içeren yeni bir listeyi döndürür. İlk kayıttaki alan <strong>&quot;abc&quot;</strong> metnini içeriyor ve ikinci kayıttaki alan <strong>&quot;d&quot;</strong> metnini içeriyorsa.</td>
</tr>
<tr class="even">
<td>SPLITLIST (list, sayı)</td>
<td>Belirtilen listeyi, her biri belirtilen sayıda kayıt içeren toplu işleri bölün. Sonucu, aşağıdaki öğeleri içeren yeni bir toplu iş listesi olarak döndürür:
<ul>
<li>Toplu işler düzenli listelerdir (<strong>Değer </strong>bileşen)</li>
<li>Geçerli toplu iş numarası (<strong>BatchNumber </strong>bileşeni)</li>
</ul></td>
<td>Aşağıdaki örnekte, <strong>Satırlar</strong> veri kaynağı, her biri en çok iki kayıt içeren toplu işlere bölünen, üç kaydın kayıt listesi olarak oluşturulur. <a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a> Bu, tasarlanan biçim düzenini gösterir; burada <strong>Satırlar</strong> veri kaynağına bağlantılar her bir toplu iş ve içindeki kayıtlar için tek tek düğümleri temsil eden XML biçiminde çıktı üretmek için oluşturulur. <a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a> Tasarlanan biçim yürütüldüğünde çıkan sonuç aşağıdadır. <a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a></td>
</tr>
<tr class="odd">
<td>LIST (kayıt 1 [, kayıt 2, ...])</td>
<td>Belirtilen değişkenlerden oluşturulan yeni bir liste döndür.</td>
<td><strong>LIST (model.MainData, model.OtherData)</strong>, <strong>MainData</strong> ve <strong>OtherData</strong> alan listesinin, kayıt listelerinin tüm alanlarını içeren boş bir kaydı döndürür.</td>
</tr>
<tr class="even">
<td>LISTJOIN (liste 1, liste 2, ...)</td>
<td>Belirtilen değişkenlerin listesinden oluşturulan birleştirilmiş bir liste döndür.</td>
<td><strong>LISTJOIN (SPLIT (&quot;abc&quot;, 1), SPLIT (&quot;def&quot;, 1))</strong> <strong>DİZE</strong> veri türünün bir alanının tek harfler içerdiği altı listelik bir kaydı döndürür.</td>
</tr>
<tr class="odd">
<td>ISEMPTY (liste)</td>
<td>Eğer belirtilen liste herhangi bir öğe içermiyorsa <strong>DOĞRU</strong> döndürür. Aksi takdirde <strong>YANLIŞ</strong> döndürür.</td>
<td></td>
</tr>
<tr class="even">
<td>EMPTYLIST (liste)</td>
<td>Belirtilmiş olan listeyi, liste yapısı için bir kaynak olarak kullanarak boş bir liste döndürür.</td>
<td><strong>EMPTYLIST (SPLIT (&quot;abc&quot;, 1))</strong> <strong>SPLIT</strong> işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir liste döndürür.</td>
</tr>
<tr class="odd">
<td>FIRST (liste)</td>
<td>Eğer kayıt boş değilse, belirtilen listedeki ilk kaydı döndür. Aksi takdirde, bir özel durum ilan et.</td>
<td></td>
</tr>
<tr class="even">
<td>FIRSTORNULL (liste)</td>
<td>Eğer kayıt boş değilse, belirtilen listedeki ilk kaydı döndür. Aksi takdirde bir <strong>null</strong> kaydı döndür.</td>
<td></td>
</tr>
<tr class="odd">
<td>LISTOFFIRSTITEM (liste)</td>
<td>Belirtilen listenin sadece ilk öğesini içeren bir liste döndür.</td>
<td></td>
</tr>
<tr class="even">
<td>ALLITEMS (yol)</td>
<td>Belirtilen yolla eşleşen tüm öğelerin temsil edildiği yeni bir düzleştirilmiş liste döndür. Yol, kayıt listesi veri türünün veri kaynağı öğesine geçerli veri kaynağı yolu olarak tanımlanmalıdır. Dize yolu, tarih vb. veri öğeleri, ER ifade oluşturucudaki tasarım zamanında hata vermelidir.</td>
<td>Eğer <strong>SPLIT(&quot;abcdef&quot; , 2)</strong> veri kaynağı (DS) olarak girerseniz, <strong>COUNT( ALLITEMS (DS.Value))</strong>, <strong>3</strong> döndürür.</td>
</tr>
<tr class="odd">
<td>ORDERBY (liste [ifade 1, ifade 2,...])</td>
<td>İfadeler olarak tanımlanabilen, belirtilmiş bağımsız değişkenlere göre sıralanmış belirtilen listeyi döndür.</td>
<td><strong>Satıcı </strong>, VendTable tablosuna başvuran ER kaynağı olarak yapılandırıldığında,<strong> ORDERBY (Vendors, Vendors.'name()')</strong>, satıcıların isme göre sıralanan listesini artan sıraya göre dizilmiş şekilde döndürür.</td>
</tr>
<tr class="even">
<td>REVERSE (liste)</td>
<td>Belirtilen listeyi ters sıralama düzeninde döndür.</td>
<td><strong>Satıcı </strong>, VendTable tablosuna başvuran ER kaynağı olarak yapılandırıldığında, <strong>REVERSE (ORDERBY (Vendors, Vendors.'name()')) )</strong>, satıcıların isme göre sıralanan listesini azalan sıraya göre dizilmiş şekilde döndürür.</td>
</tr>
<tr class="odd">
<td>WHERE (liste, koşul)</td>
<td>Belirtilen koşula göre filtrelenmiş olan belirtilen listeyi döndürür. <strong>FİLTRE</strong> işlevinin aksine belirtilen koşul bellekteki listeye uygulanır.</td>
<td><strong>Satıcı</strong>, VendTable tablosuna başvuran ER kaynağı olarak yapılandırıldığında, <strong>WHERE(Vendors, Vendors.VendGroup = &quot;40&quot;)</strong>, grup 40'a dahil olan satıcıların listesini döndürür.</td>
</tr>
<tr class="even">
<td>ENUMERATE (liste)</td>
<td>Belirtilen listenin numaralandırılmış kayıtlarından oluşan ve aşağıdaki öğeleri gösteren yeni bir liste döndürür:
<ul>
<li>Belirtilen liste kayıtları, düzenli olarak (<strong>Değer </strong>bileşeni) listeler</li>
<li>Geçerli kayıt dizini (<strong>Numara </strong>bileşeni)</li>
</ul></td>
<td>Aşağıdaki örnekte, <strong>Enumerated</strong> veri kaynağı, satıcı kayıtlarının, <strong>satıcılar</strong> veri kaynağına başvuran <strong>VendTable</strong> tablo sunun numaralandırılmış bir listesi olarak oluşturulur. <a href="./media/picture-enumerate-datasource.jpg"><img src="./media/picture-enumerate-datasource.jpg" alt="Enumerated data source" class="alignnone wp-image-290711 size-full" width="387" height="136" /></a>Tekil satıcıları, numaralandırılmış düğümler olarak temsil eden XML biçiminde çıktı oluşturmak için veri ilişkilendirmelerinin oluşturulduğu biçim buradadır. <a href="./media/picture-enumerate-format.jpg"><img src="./media/picture-enumerate-format.jpg" alt="Format that has data bindings" class="alignnone wp-image-290721 size-full" width="414" height="138" /></a> Bu, tasarlanan biçim yürütüldüğünde çıkan sonuçtur. <a href="./media/picture-enumerate-result.jpg"><img src="./media/picture-enumerate-result.jpg" alt="Result of running the format" class="alignnone wp-image-290731 size-full" width="567" height="176" /></a></td>
</tr>
<tr class="odd">
<td>COUNT (liste)</td>
<td>Eğer liste boş değilse, belirtilen listedeki kayıtların sayısını döndür. Aksi takdirde <strong>0</strong> (sıfır) döndürür.</td>
<td><strong>SPLIT</strong> işlevi iki kayıttan oluşan bir liste oluşturduğu için, <strong>COUNT (SPLIT(&quot;abcd&quot; , 3))</strong> <strong>2</strong> döndürür.</td>
</tr>
<tr class="even">
<td>LISTOFFIELDS (yol)</td>
<td>Aşağıdaki türlerden birinin bağımsız değişkeninden oluşturulan kayıtlar listesine döndürür:
<ul>
<li>Model numaralandırma</li>
<li>Biçim numaralandırma</li>
<li>Kapsayıcı</li>
</ul>
Oluşturulan liste aşağıdaki alanları olan kayıtlar içerir:
<ul>
<li>Dosya Adı</li>
<li>Etiket</li>
<li>Açıklama</li>
</ul>
Etiket ve Açıklama alanları, biçimin dil ayarlarına göre çalışma zamanı değerlerine döndürülür.</td>
<td>Aşağıdaki örnek bir veri modelinde oluşturulan numaralandırmayı gösterir. <a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="GER LISTOFFIELDS function - model enumeration" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>Aşağıdaki örnek şunu gösterir:
<ul>
<li>Veri kaynağı olarak bir rapora eklenen model numaralandırma.</li>
<li>Bu işlevin parametresi olarak model numaralandırma kullanmak için tasarlanan ER ifadesi.</li>
<li>Oluşturulan ER ifadesini kullanarak bir rapora eklenen kayıt listesi türünün veri kaynağı.</li>
</ul>
<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="GER LISTOFFIELDS function - in format expression" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a> Aşağıdaki örnek LISTOFFIELDS işlevi kullanılarak oluşturulan kayıt listesi türü veri kaynağına bağlı olan ER biçim öğelerini gösterir.<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="GER LISTOFFIELDS function - format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>Bu, tasarlanmış biçim yürütme işleminin sonucudur.<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="GER LISTOFFIELDS function - format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a><strong>Note:</strong> Çevrilmiş etiket metinleri ve açıklamaları ana DOSYA ve KLASÖR biçim öğeleri için yapılandırılan dil ayarlarına uygun olarak ER biçim çıktısına doldurulur.</td>
</tr>
<tr class="odd">
<td>STRINGJOIN (liste, alan adı, ayırıcı)</td>
<td>Seçili ayırıcı ile ayrılan bir listeden bir alanın birbirine bağlanan değerlerinin dizesini döndürür.</td>
<td>DS veri kaynağı olarak SPLIT(“abc” , 1) girdiğinizde STRINGJOIN (DS, DS.Value, “:”) ifadesi “a:b:c” sonucunu verir</td>
</tr>
<tr class="even">
<td>SPLITLISTBYLIMIT (liste, sınır değeri, sınır kaynağı)</td>
<td>Verilen listeyi alt listelerin yeni listesine ayırır ve kayıt listesi içeriğinde sonucu verir. Sınır kaynağı parametresi, kaynak listeyi ayırmak için sınırın değerini belirtir. Sınır kaynağı parametresi toplamın artırıldığı adımı belirtir. Sınır kaynağı tanımlanan sınırı aştığında sınır, verilen listedeki tek bir öğeye uygulanmaz.</td>
<td>Aşağıdaki örnek veri kaynaklarını kullanan örnek biçimi gösterir. <a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="GER SPLITLISTBYLIMIT - format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a><a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="GER SPLITLISTBYLIMIT - datasources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>Bu, emtia öğelerinin düz listesini sunan biçim yürütmenin sonucudur.<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="GER SPLITLISTBYLIMIT - output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>Aşağıdaki örnek aynı biçimin, emtia öğelerinin listesini, tek bir toplu işin emtiaları toplam ağırlıklarıyla, aşmamaları gereken 9 sınırını toplu işler olarak göstermek sunmak üzere ayarlanmıştır<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="GER SPLITLISTBYLIMIT - format 1" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a><a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="GER SPLITLISTBYLIMIT - datasources 1" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>Bu ayarlanmış biçim yürütmenin sonucudur. <a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="GER SPLITLISTBYLIMIT - output 1" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a><strong>Not:</strong> Sınırının kaynak (ağırlık) değeri (11) tanımlanan sınırı (9) geçtiğinden sınır, kaynak listedeki son maddeye uygulanmaz. Rapor oluştururken (gerekirse) alt listeleri yok saymak (atlamak) için <strong>WHERE</strong> işlevini veya ilgili biçim öğesinin <strong>Etkinleştirildi</strong> ifadesini kullanın.</td>
</tr>
<tr class="odd">
<td>FİLTRE (liste, koşul)</td>
<td>Sorguyu değiştirerek belirtilen koşul için filtrelenmiş verilen listeye döndürür. <strong>WHERE</strong> işlevinin aksine, belirtilen koşul veri tabanı düzeyinde Tablo kayıt türünün herhangi bir ER veri kaynağına uygulanabilir.</td>
<td><strong>Satıcı</strong>, <strong>VendTable</strong> tablosuna referansta bulunan ER veri kaynağı olarak yapılandırıldığında FİLTRE (Satıcılar, Vendors.VendGroup = &quot;40&quot;) yalnızca grup "40" listesinde bulunan satıcıların listesini döndürür</td>
</tr>
</tbody>
</table>

### <a name="logical-functions"></a>Mantıksal işlevler

| İşlev                                                                                | Açıklama                                                                                                                                                                                                                                                                     | Örnek                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CASE (ifade, seçenek 1, sonuç 1 \[, seçenek 2, sonuç 2\]... \[, varsayılan sonuç\]) | Belirtilen ifade değerini, belirtilen alternatif seçeneklere karşı değerlendirin. İfadenin değerine eşit olan seçeneğin sonucunu döndür. Aksi halde, isteğe bağlı olarak girilen varsayılan sonucu (daha öncesinde bir seçenek olmayan son parametreyi) döndürür. | **CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")**, geçerli Dynamics 365 for Operations oturum tarihi Ekim ve Aralık ayları arasındaysa **KIŞ** dizesini döndürür. Aksi halde, boş bir dize döndürür. |
| IF (koşul, değer 1, değer 2)                                                        | Belirli bir koşul karşılandığında belirtilen değer 1'i döndürür. Aksi takdirde değer 2'yi döndür. Eğer değer 1 ve değer 2, kayıt veya kayıt listeleriyse, sonuç sadece her iki listede de mevcut olan alanları içerecektir.                                                                     | **IF (1=2, "koşul karşılandı", "koşul karşılanmadı")**, **"koşul karşılanmadı"** dizesini döndürür.                                                                                                                                                      |
| NOT (koşul)                                                                         | Belirtilen koşulun ters mantıksal değerini döndürür.                                                                                                                                                                                                                   | **DEĞİL (DOĞRU)**, **YANLIŞ** döndürür.                                                                                                                                                                                                                            |
| VE (koşul 1\[, koşul 2, ...\])                                                 | *Tüm *belirtilen koşullar doğruysa, **DOĞRU** döndür. Aksi takdirde **YANLIŞ** döndürür.                                                                                                                                                                                            | **VE (1=1, "a"="a")**,**DOĞRU** döndürür. **AND (1=2, "a"="a")** **YANLIŞ** döndürür.                                                                                                                                                                           |
| VEYA (koşul 1\[, koşul 2, ...\])                                                  | *Tüm *belirtilen koşullar yanlışsa, **YANLIŞ** döndür. *Herhangi bir *belirtilen koşul doğruysa **DOĞRU** döndür.                                                                                                                                                                 | **VEYA (1=2, "a"="a")**,**DOĞRU** döndürür.                                                                                                                                                                                                                      |

### <a name="mathematical-functions"></a>Matematik işlevi

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>İşlev</th>
<th>Açıklama</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ABS (numara)</td>
<td>Belirtilen sayının mutlak değerini döndürür (sayının işareti olmadan).</td>
<td><strong>ABS (-1)</strong>, <strong>1</strong> döndürür.</td>
</tr>
<tr class="even">
<td>KUVVET (sayı, kuvvet)</td>
<td>Belirtilen pozitif sayının, belirtilen kuvvetine yükseltilmesinin sonucunu döndür.</td>
<td><strong>KUVVET (10, 2)</strong>, <strong>100</strong> döndürür.</td>
</tr>
<tr class="odd">
<td>NUMBERVALUE (dize, ondalık ayırıcı, basamak gruplandırma ayırıcı)</td>
<td>Belirtilen dizeyi sayıya dönüştürün. Belirtilen sembol, bir ondalık sayının tamsayı ve ondalık kısımlarını ayırmak için kullanılır ve belirtilen binlik ayırıcısı da kullanılır.</td>
<td><strong>NUMBERVALUE(&quot;1 234,56&quot;, &quot;,&quot;, &quot; &quot;)</strong> <strong>1234,56</strong> değerini döndürür.</td>
</tr>
<tr class="even">
<td>VALUE (dize)</td>
<td>Belirtilen dizeyi sayıya dönüştürün. Virgül ve nokta karakterleri (.) ondalık ayırıcı olarak kabul edilir ve önde gelen bir tire (-) eksi işareti olarak kullanılır. Belirtilen dizenin içinde sayısal olmayan karakterlerle karşılaşılırsa, bir özel durum hatası oluştur.</td>
<td><strong>DEĞER (&quot;1 234,56&quot;)</strong> bir istisna oluşturur.</td>
</tr>
<tr class="odd">
<td>ROUND (sayı, ondalık basamak)</td>
<td>Belirtilen sayıdaki ondalık basamağa yuvarlanmış olan belirtilen sayıyı döndürür.
<ul>
<li>Eğer belirtilen ondalık değer 0'dan (sıfır) büyük ise, belirtilen sayı, belirtilen miktardaki ondalık basamağa yuvarlanır.</li>
<li>Belirtilen ondalık değeri 0 (sıfır) ise, belirtilen sayı en yakın tamsayıya yuvarlanır.</li>
<li>Eğer belirtilen ondalık değer 0'dan (sıfır) küçük ise, belirtilen sayı, belirtilen ondalık basamağın soluna yuvarlanır.</li>
</ul></td>
<td><strong>ROUND (1200.767, 2)</strong> iki ondalık basamağa yuvarlar ve <strong>1200.77</strong> sonucunu döndürür. <strong>ROUND (1200.767, -3)</strong> 1.000'in en yakın katına yuvarlar ve <strong>1000</strong> döndürür.</td>
</tr>
<tr class="even">
<td>ROUNDDOWN (sayı, ondalık basamak)</td>
<td>Belirtilen miktardaki ondalık basamağa aşağı yuvarlanmış (sıfıra doğru) olan belirtilmiş sayıyı döndürür. <strong>Not:</strong> Bu işlev <strong>YUVARLA</strong> gibi davranır ancak bu her zaman belirtilen aşağı doğru yuvarlar.</td>
<td><strong>ROUNDDOWN (1200.767, 2)</strong> iki ondalık basamağa aşağı yuvarlar ve <strong>1200.76</strong> sonucunu döndürür. <strong>ROUNDDOWN (1700.767, -3)</strong> 1.000'in en yakın katına aşağı yuvarlar ve <strong>1000</strong> döndürür.</td>
</tr>
<tr class="odd">
<td>ROUNDUP (sayı, ondalık basamak)</td>
<td>Belirtilen miktardaki ondalık basamağa yukarı yuvarlanmış (sıfırdan uzağa) olan belirtilmiş sayıyı döndürür. <strong>Not:</strong> Bu işlev <strong>YUVARLA</strong> gibi davranır ancak bu her zaman belirtilen sayıyı yukarı doğru yuvarlar.</td>
<td><strong>ROUNDUP (1200.763, 2)</strong> iki ondalık basamağa yukarı yuvarlar ve <strong>1200.77</strong> sonucunu döndürür. <strong>ROUNDUP (1200.767, -3)</strong> 1.000'in en yakın katına yukarı yuvarlar ve <strong>2000</strong> döndürür.</td>
</tr>
</tbody>
</table>

### <a name="record-functions"></a>Kayıt işlevleri

| İşlev             | Açıklama                                                                                                                                                                                                                                     | Örnek                                                                                                                                             |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| NULLCONTAINER (liste) | Belirtilen kayıt listesi veya kayıt ile aynı yapıya sahip bir **null** kaydı döndürür. **Not: **bu işlev artık kullanılmamaktadır. Bunun yerine **EMPTYRECORD** kullanın.                                                                                  | **NULLCONTAINER (SPLIT ("abc", 1))**, **SPLIT** işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür. |
| EMPTYRECORD (kayıt) | Belirtilen kayıt listesi veya kayıt ile aynı yapıya sahip bir **null** kaydı döndürür. **Not:** Bir **null** kaydı, tüm alanların boş değere sahip olduğu bir kayıttır (sayılar için **0** \[sıfır\], dizeler için boş dize ve benzeri şekilde). | **EMPTYRECORD (SPLIT ("abc", 1))**, **SPLIT** işlevi tarafından döndürülen listeyle aynı yapıya sahip, boş yeni bir kayıt döndürür.   |

### <a name="text-functions"></a>Metin işlevleri

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>İşlev</th>
<th>Açıklama</th>
<th>Örnek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>UPPER (dize)</td>
<td>Büyük harfe dönüştürülmüş olan, belirtilen dizeyi döndürür.</td>
<td><strong>UPPER(&quot;Örnek&quot;)</strong>, <strong>&quot;ÖRNEK&quot;</strong> sonucunu döndürür.</td>
</tr>
<tr class="even">
<td>LOWER (dize)</td>
<td>Küçük harfe dönüştürülmüş olan, belirtilen dizeyi döndürür.</td>
<td><strong>LOWER(&quot;Örnek&quot;)</strong>, <strong>&quot;örnek&quot;</strong> sonucunu döndürür.</td>
</tr>
<tr class="odd">
<td>LEFT (dize, karakter sayısı)</td>
<td>Belirtilen dizenin başından belirtilen sayıda karakteri döndür.</td>
<td><strong>LEFT (&quot;Örnek&quot;, 3)</strong>, <strong>&quot;Örn&quot;</strong> döndürür.</td>
</tr>
<tr class="even">
<td>RIGHT (dize, karakter sayısı)</td>
<td>Belirtilen dizenin sonundan belirtilen sayıda karakteri döndür.</td>
<td><strong>SAĞ ("&quot;Örnek&quot;, 3)</strong>, <strong>&quot;nek&quot;</strong> döndürür.</td>
</tr>
<tr class="odd">
<td>MID (dize, Başlangıç pozisyonu, karakter sayısı)</td>
<td>Belirtilen dizenin, belirtilen konumdan başlayarak, belirtilen sayıdaki karakterini döndür.</td>
<td><strong>MID (&quot;Örnek&quot;, 2, 3)</strong>, <strong>&quot;rne&quot;</strong> döndürür.</td>
</tr>
<tr class="even">
<td>LEN (dize)</td>
<td>Belirtilen dizedeki karakterlerin sayısını döndür.</td>
<td><strong>LEN (&quot;Örnek&quot;)</strong>, <strong>6</strong> döndürür.</td>
</tr>
<tr class="odd">
<td>CHAR (numara)</td>
<td>Belirtilen Unicode numarası tarafından başvuruda bulunulan karakter dizesini döndürür.</td>
<td><strong>CHAR (255)</strong>, <strong>&quot;ÿ&quot;</strong> döndürür. <strong>Not:</strong> Döndürülen dize DOSYA biçimi üst öğesinde seçtiğiniz kodlamaya bağlıdır. Desteklenen kodlamalar listesi <a href="https://msdn.microsoft.com/en-us/library/system.text.encoding(v=vs.110).aspx">Kodlama Sınıfı</a> konusunda bulunabilir.</td>
</tr>
<tr class="even">
<td>CONCATENATE (dize 1 [, dize 2, …])</td>
<td>Bir dizeye dahil edilen, belirtilen tüm dizeleri döndür.</td>
<td><strong>CONCATENATE (&quot;abc&quot;, &quot;def&quot;)</strong>, <strong>&quot;abcdef&quot;</strong>döndürür. <strong>Not:</strong> <strong>&quot;abc&quot; &amp; &quot;def&quot;</strong> ifadesi de <strong>&quot;abcdef&quot;</strong> döndürür.</td>
</tr>
<tr class="odd">
<td>TRANSLATE (dize, kalıp, değiştirme)</td>
<td>Belirtilen desen dizesindeki tüm karakterlerin, belirtilen değiştirme dizesindeki karakterlerle değiştirildiği, belirtilmiş olan dizeyi döndürür.</td>
<td><strong>TRANSLATE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;)</strong> deseni değiştirir <strong>&quot;cd&quot;</strong>, şunun ile: <strong>&quot;GH&quot;</strong> ve bunu döndürür: <strong>&quot;abGHef&quot;</strong>.</td>
</tr>
<tr class="even">
<td>REPLACE (dize, desen, değiştirme, normal ifade işareti)</td>
<td>Belirtilen normal ifade bayrağı <strong>doğru</strong> olduğunda, bir desen olarak bu işlev için belirtilen normal ifade uygulanarak modifiye edilen belirtilen dizeyi döndür. Bu ifade, değiştirilmesi gereken karakterleri bulmakta kullanılır. Belirtilen değiştirme bağımsız değişkenindeki karakterler, bulunan karakterleri değiştirmek için kullanılır. Belirtilen normal ifade bayrağı <strong>yanlış</strong> ise, bu işlev <strong>TRANSLATE</strong> gibi davranır.</td>
<td>  <strong>REPLACE (&quot;+1 923 456 4971&quot;, &quot;[^0-9]&quot;, &quot;&quot;, true)</strong> üm sayısal olmayan karakterleri kaldıran bir normal ifade uygular ve <strong>&quot;19234564971&quot;</strong> döndürür. <strong>REPLACE (&quot;abcdef&quot;, &quot;cd&quot;, &quot;GH&quot;, yanlış)</strong> <strong>&quot;cd&quot;</strong> desenini <strong>&quot;GH&quot;</strong> satırı ile değiştirir ve <strong>&quot;abGHef&quot;</strong> döndürür.</td>
</tr>
<tr class="odd">
<td>TEXT (giriş)</td>
<td>Geçerli Dynamics 365 for Operations örneğinin sunucu yerel ayarlarına göre biçimlendirilmiş bir metin dizesine çevrilmiş olan belirtilen girişi döndürür. <strong>gerçek</strong> türün değerleri için, dize dönüşümü iki ondalık basamakla sınırlıdır.</td>
<td>Dynamics 365 for Operations örneği yerel sunucusu <strong>TR-TR</strong> olarak tanımlanırsa <strong>TEXT (NOW ())</strong>, geçerli Dynamics 365 for Operations oturum tarihi olan 12/17/2015 tarihini metin dizesi olarak <strong>&quot;17.12.2015 07:59:23&quot;</strong> tarihine döndürür. <strong>TEXT (1/3)</strong> <strong>&quot;0.33&quot;</strong> döndürür.</td>
</tr>
<tr class="even">
<td>FORMAT (dize 1, dize 2[, dize 3, ...])</td>
<td>Tüm <strong>%N</strong> oluşumlarını <em>n</em>'inci bağımsız değişken ile değiştirilmiş belirtilen dizeyi döndür. Bağımsız değişkenler, dizelerdir. Bir parametre için bir bağımsız değişken sağlanmamışsa, parametre izede <strong>&quot;%N&quot;</strong> olarak döndürülür. <strong>gerçek</strong> türün değerleri için, dize dönüşümü iki ondalık basamakla sınırlıdır.</td>
<td>Bu örnekte, <strong>PaymentModel</strong> veri kaynağı müşteri kayıtlarının listesini <strong>Müşteri</strong> bileşeni ve işleme tarihi değerini <strong>ProcessingDate</strong> alan üzerinden verir. <a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a> Seçilen müşteriler için elektronik dosya oluşturmak üzere tasarlanmış ER biçiminde veri kaynağı olarak <strong>PaymentModel</strong> seçilir ve işlem akışını denetler. Seçilmiş bir müşteri, raporun işlendiği tarihte durdurulmuşsa, son kullanıcılar için bir özel durum oluşturulur. Bu tür bir işleme denetimi için tasarlanmış formül aşağıdaki kaynakları kullanabilir:
<ul>
<li>Aşağıdaki metne sahip Dynamics 365 for Operations SYS70894 etiketi:
<ul>
<li><strong>TR-TR dili için:</strong> &quot;Yazdırılacak hiçbir şey yok&quot;</li>
<li><strong>DE dili için:</strong> &quot;Nichts zu drucken&quot;</li>
</ul></li>
<li>Aşağıdaki metne sahip Dynamics 365 for Operations SYS18389 etiketi:
<ul>
<li><strong>TR-TR dili için:</strong> &quot;Müşteri %1, %2 için durduruldu.&quot;</li>
<li><strong>DE dili için:</strong> &quot;Debitor '%1' wird für %2 gesperrt.&quot;</li>
</ul></li>
</ul>
Tasarlanabilir formül şudur: FORMAT (CONCATENATE (@&quot;SYS70894&quot;, &quot;. &quot;, @&quot;SYS18389&quot;), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, &quot;d&quot;)) Eğer bir rapor <strong>Litware Perakende müşterisi</strong> için 17 Aralık 2015 tarihinde, <strong>TR-TR</strong> kültüründe ve <strong>TR-TR</strong> dilinde işlenmişse, bu formül son kullanıcıya bir özel durum iletisi olarak sunulabilecek aşağıdaki metni içerir: &quot;Yazdırılacak hiçbir şey yok. Müşteri Litware perakende 17/12/2015 için durduruldu.&quot; Eğer aynı rapor<strong> Litware Perakende müşterisi</strong> için 17 Aralık 2015 tarihinde <strong>DE</strong> kültürü ve <strong>DE</strong> dilinde işlenmişse, bu formül başka bir tarih biçimini kullanan aşağıdaki metni döndürür: &quot;Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.&quot; <strong>Not: </strong>Aşağıdaki sözdizimi, etiketler için ER formüllerinde kullanılır:
<ul>
<li><strong>Dynamics 365 for Operations kaynaklarından etiketler için:</strong>  <strong>@&quot;X&quot;</strong>, burada X Uygulama Nesne Ağacı (AOT) etiket kimliğidir.</li>
<li><strong>ER yapılandırmaları içinde bulunan etiketler için:</strong>  <strong>@&quot;ER_LABEL:X&quot;</strong>, burada X, ER yapılandırma etiket kimliğidir.</li>
</ul></td>
</tr>
<tr class="odd">
<td>NUMBERFORMAT (sayı, biçim)</td>
<td>Belirtilen sayının, belirtilen biçimdeki dize olarak temsilini döndür. (Desteklenen biçimler hakkında bilgi için bkz. <a href="https://msdn.microsoft.com/en-us/library/dwhawy9k(v=vs.110).aspx">standart</a> ve <a href="https://msdn.microsoft.com/en-us/library/0c899ak8(v=vs.110).aspx">özel</a>.) Bu işlevin çalıştırıldığı bağlam, sayıları biçimlendirmek için kullanılan kültürü belirler.</td>
<td>TR-TR kültürü için <strong>NUMBERFORMAT (0.45, &quot;p&quot;)</strong>, <strong>&quot;%45,00&quot;</strong> döndürür. <strong>NUMBERFORMAT (10.45, &quot;#&quot;)</strong>, <strong>&quot;10&quot;</strong> döndürür.</td>
</tr>
<tr class="even">
<td>NUMERALSTOTEXT (sayı, dil, para birimi, para birimi adını yazdır bayrağı, ondalık basamaklar)</td>
<td>Tanımlanmış dildeki metin dizelerine hecelenen (dönüştürülen) sayıya döner. Dil kodu isteğe bağlıdır: Boş dize olarak tanımlandığında yerine çalışan içerik dil kodu (bir dosya veya klasör oluşturmak için tanımlanan) kullanılır. Para birimi kodu isteğe bağlıdır. Boş dize olarak tanımlandığında, şirket para birimi alınır. <strong>Para birimi adını yazdır</strong> parametresi ve <strong>Ondalık basamaklar</strong> parametresinin yalnızca aşağıdaki dil kodları için analiz edildiğini unutmayın: <strong>CS</strong>, <strong>ET</strong>, <strong>HU</strong>, <strong>LT</strong>, <strong>LV</strong>, <strong>PL</strong>, <strong>RU</strong>. <strong>Para birimi adını yazdır</strong> parametresinin yalnızca para birimi gerilemesini destekleyen ülkeye bağlı Dynamics 365 for Operation şirketleri için analiz edildiğini unutmayın.</td>
<td>NUMERALSTOTEXT (1234.56, &quot;TR&quot;, &quot;&quot;, yanlış, 2) “Bin iki yüz otuz dört ve 56” döndürür NUMERALSTOTEXT (120, &quot;PL&quot;, &quot;&quot;, yanlış, 0) “Sto dwadzieścia” döndürür NUMERALSTOTEXT (120.21, &quot;RU&quot;, &quot;EUR&quot;, doğru, 2) “Сто двадцать евро 21 евроцент” döndürür</td>
</tr>
<tr class="odd">
<td>PADLEFT (dize, uzunluk, doldurma karakterleri)</td>
<td>Geçerli dizenin başlangıcının belirtilen karakterlerle doldurulduğu belirtilen uzunlukta bir dize verir.</td>
<td>PADLEFT ("1234", 10,"") “      1234” metin dizesini döndürür</td>
</tr>
</tbody>
</table>

### <a name="data-collection-functions"></a>Veri toplama işlevleri

İşlev

Açıklama

Örnek

FORMATELEMENTNAME ()

Geçerli biçimin öğesinin adını verir. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında boş dizeye döner.

Bu işlevlerin kullanımı hakkında daha fazla bilgi edinmek için **ER Sayma ve toplama için çıktı biçiminde verileri kullanma** (**BT hizmeti/çözüm bileşenleri al/geliştir** iş sürecinin parçası) Görev kılavuzuna başvurun.

SUMIFS (toplamı alınacak temel dize, ölçüt aralığı1 dizesi, ölçüt değeri1 dizesi \[, ölçüt aralığı2 dizesi, ölçütlere değeri2 dizesi, ...\])

Bu biçim yürütme işlemi sırasında toplanan ve girilen koşulları (aralık ve değer çiftleri) karşılayan XML düğümlerinin (bir anahtar olarak tanımlanan ada sahip) değerlerine ait bir toplama döner. Geçerli dosyaların **Çıkış ayrıntılarını topla **bayrağı kapatıldığında sıfır değerine döner.

SUMIF (toplama için temel dize, ölçüt aralığı dizesi, ölçüt değeri dizesi)

Bu biçim yürütme işlemi sırasında toplanan ve girilen koşulu (aralık ve değer) karşılayan XML düğümlerinin (bir anahtar olarak tanımlanan ada sahip) değerlerine ait bir toplama döner. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında sıfır değerine döner.

COUNTIFS (ölçüt aralığı1 dizesi, ölçüt değeri1 dizesi \[, ölçüt aralığı2 dizesi, ölçütlere değeri2 dizesi, ...\])

Bu biçim yürütme işlemi sırasında toplanan ve girilen koşulları (aralık ve değer çiftleri) karşılayan XML düğüm sayısına döner. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında sıfır değerine döner.

COUNTIF (ölçüt aralığı dizesi, ölçüt değeri dizesi)

Bu biçim yürütme işlemi sırasında toplanan ve girilen koşulu (aralık ve değer) karşılayan XML düğüm sayısına döner. Geçerli dosyaların **Çıkış ayrıntılarını topla** bayrağı kapatıldığında sıfır değerine döner.

COLLECTEDLIST (ölçüt aralığı1 dizesi, ölçüt değeri1 dizesi \[, ölçüt aralığı2 dizesi, ölçütlere değeri2 dizesi, ...\])

Bu biçim yürütme işlemi sırasında toplanan ve girilen koşulları (aralık ve değer) karşılayan XML düğüm değerlerinin listesine döner. Geçerli dosyaların **Çıkış ayrıntılarını topla **bayrağı kapatıldığında boş listeye döner.

### <a name="other-business-domainspecific-functions"></a>Diğer (belirli iş etki alanı) işlevleri

| İşlev                                                                         | Açıklama                                                                                                                                                                                                                                                        | Örnek                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONVERTCURRENCY (tutar, kaynak para birimi, hedef para birimi, tarih, şirket)        | Belirtilen parasal tutarı kaynak para biriminden, belirtilen tarihte Dynamics 365 for Operations şirketin belirtilen ayarları kullanarak hedef para birimine dönüştürür.                                                                            | **CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")**, şimdiki oturum tarihinde, DEMF şirket ayarlarına dayalı olarak bir euro'nun ABD doları olarak karşılığını döndürür.                                                                                                                                  |
| ROUNDAMOUNT (sayı, ondalık, yuvarlama kuralı)                                       | Belirtilmiş yuvarlama kuralına ve belirtilen ondalık basamağa göre belirtilen tutarı yuvarla. **Not:** Yuvarlama kuralı Dynamics 365 for Operations **RoundOffType** numaralandırmasının bir değeri olarak belirtilmelidir.                          | Eğer **model.RoundOff** parametresi ****Aşağıya**** olarak ayarlanmışsa, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)**, **1000,78** değerini döndürür. Eğer **model.RoundOff** parametresi **Normal** ya da **Yukarıya yuvarla** olarak ayarlanmışsa, **ROUNDAMOUNT (1000.787, 2, model.RoundOff)**, **1000,79** değerini döndürür. |
| CURCredRef (basamak)                                                              | Belirtilen fatura numarasının basamaklarına dayalı olarak bir alacaklı başvurusu döndür.                                                                                                                                                                                  | **CURCredRef ("Satıcı-200002")**, **"2200002"** döndürür.                                                                                                                                                                                                                                                         |
| MOD\_97 (basamak)                                                                 | Belirtilen fatura numarasının basamaklarına dayalı olarak bir alacaklı başvurusunu bir MOD97 ifadesi olarak döndür.                                                                                                                                                            | **MOD\_97 ("VEND-200002")**, **"20000285"** döndürür.                                                                                                                                                                                                                                                           |
| ISOCredRef (basamak)                                                              | Bir ISO alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak döndür. **Not: **ISO uyumlu olmayan alfabelerden sembolleri elemek için, giriş parametresinin işleve gönderilmeden önce çevrilmesi gerekir. | **ISOCredRef ("VEND-200002")**, **"RF23VEND-200002"** döndürür.                                                                                                                                                                                                                                                 |
| CN\_GBT\_AdditionalDimensionID (dize, sayı)                                  | Ek mali boyut kimliğini alın. Boyutlar bu dizede kimlikler virgüllerle ayrılmış olarak gösterilir. Sayılar, bu dizede istenen boyutun sıra kodunu tanımlar.                                                                            | CN\_GBT\_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH",3) “CC” döndürür                                                                                                                                                                                                                                      |
| GetCurrentCompany ()                                                             | Geçerli oturum açan şirketin kodunu döndürür.                                                                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                               |
| CH\_BANK\_MOD\_10 (basamaklar)                                                       | Belirtilen fatura numarasının basamaklarını temel alarak bir alacaklı referansı olan MOD10 ifadesini döndürür.                                                                                                                                                                      | CH\_BANK\_MOD\_10 ("VEND-200002") 3 döndürür                                                                                                                                                                                                                                                                   |
| FA\_SUM (sabit kıymet kodu, değer modeli kodu, başlangıç tarihi, bitiş tarihi)               | Bir döneme ait sabit kıymet tutarlarının hazırlanan veri kapsayıcısını verir.                                                                                                                                                                                         | FA\_SUM ("COMP 000001", "Geçerli", Tarih1, Tarih2) Tarih1'den Tarih2'ye kadar olan bir dönem için "Geçerli" değer modeli ile hazırlanmış "COMP-000001" sabit kıymet veri kapsayıcısını döndürür.                                                                                                                        |
| FA\_BALANCE (sabit kıymet kodu, değer modeli kodu, raporlama yılı, raporlama tarihi) | Sabit kıymet bakiyelerinin hazırlanan veri kapsayıcısını döndürür. Raporlama yılı, Dynamics 365 for Operations numaralandırması **AssetYear** değeri olarak belirtilmelidir.                                                                                           | FA\_SUM ("COMP 000001", "Geçerli", AxEnumAssetYear.ThisYear, SESSIONTODAY ()) geçerli 365 for Operations oturum tarihinde "Geçerli" değer modeli ile "COMP-000001" sabit kıymeti için hazırlanan bilanço veri kapsayıcısını döndürür.                                                                |

### <a name="functions-list-extension"></a>Liste uzantı işlevleri

ER, ER ifadelerinde kullanılan işlevlerin listesini genişletmenize olanak sağlar. Bazı mühendislik çabaları gereklidir. Ayrıntılı bilgi için bkz: [Elektronik raporlama işlevlerinin listesini genişletme](general-electronic-reporting-formulas-list-extension.md).

<a name="see-also"></a>Ayrıca bkz.
--------

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlama (ER) işlev listesini genişletme](general-electronic-reporting-formulas-list-extension.md)




