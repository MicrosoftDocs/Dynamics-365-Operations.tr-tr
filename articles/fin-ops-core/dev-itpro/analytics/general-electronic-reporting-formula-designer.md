---
title: Elektronik raporlamada (ER) formül tasarımcısı
description: Bu konu, Elektronik raporlamada (ER) formül tasarımının nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: eec63fb1782c5afed0320eb841b6bfc92af31a691731ef6bac5d00ed442c0dcd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777416"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Elektronik raporlamada (ER) formül tasarımcısı

[!include [banner](../includes/banner.md)]

Bu konu, formül tasarımcısının Elektronik raporlamada (ER) nasıl kullanılacağını açıklar. Belirli bir elektronik belge için ER içerisinde bir biçim tasarladığınızda, belgenin gereksinimlerini karşılamak ve biçimlendirmek üzere formülleri veri dönüştürme için kullanabilirsiniz. Bu formüller Microsoft Excel'deki formüllere benzer. Formüllerde farklı türde işlevler desteklenmektedir: metin, tarih ve saat, matematiksel mantıksal, bilgi ve veri türü dönüştürme işlevleri ve diğer (iş etki alanına özel işlevler).

## <a name="formula-designer-overview"></a>Formül tasarımcısına genel bakış

ER formül tasarımcısını destekler. Bu nedenle, tasarım zamanında aşağıdaki görevler için çalışma zamanında kullanılabilecek ifadeler yapılandırabilirsiniz:

- Uygulama veritabanından alınan veriyi dönüştürün ve bu, bir ER biçimleri için veri kaynağı olmak üzere tasarlanan bir ER veri modeline girilmelidir. (Örneğin, bu dönüştürme işlemleri filtrelemeyi, gruplandırmayı ve veri türü dönüşümünü içerebilir.)
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

## <a name="data-binding"></a><a name="Binding"></a>Veri ilişkilendirme

ER formül tasarımcısı, veri kaynaklarından alınan verinin, söz konusu veri veri tüketicisinde çalışma zamanında aşağıdaki şekillerde girilebilecek şekilde dönüştürecek bir ifade tanımlamak için kullanılabilir:

- Uygulama veri kaynaklarından ve çalışma zamanı parametrelerinden bir ER veri modeline
- Bir ER veri modelinden ER biçimine
- Uygulama veri kaynaklarından ve çalışma zamanı parametrelerinden bir ER biçimine

Bu tür bir ifadenin tasarımı aşağıda gösterilmiştir. Bu örnekte ifade, Intrastat tablosunun **Intrastat.AmountMST** alanının değerini iki ondalık basamağa yuvarlar ve yuvarlanan değeri döndürür.

[![Veri bağlama ifadesi.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Aşağıdaki çizim bu tür bir ifadenin nasıl kullanılabileceğini gösterir. Bu örnekte, tasarlanmış ifadenin sonucu, **Vergi raporlama modeli** veri modelinin **Transaction.InvoicedAmount** bileşenine girilir.

[![Kullanılan veri bağlama ifadesi.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Çalışma zamanında, tasarlanan formül olan `ROUND (Intrastat.AmountMST, 2)` **AmountMST** alanındaki değeri Intrastat tablosundaki her kayıt için iki ondalık basamağa yuvarlar. Daha sonra yuvarlanan değeri **Vergi raporlama** veri modelinin **Transaction.InvoicedAmount** bileşenine girer.

## <a name="data-formatting"></a><a name="Transformation"></a>Veri biçimlendirme

ER formül tasarımcısı, veri kaynaklarından alınan verinin, söz konusu veri, elektronik belgenin oluşturulmasında kullanılabilecek şekilde biçimlendirecek bir ifade tanımlamak için kullanılabilir. Bir biçim için yeniden kullanılması gereken tipik bir kural olarak uygulanması gereken bir biçimlendirmeniz olabilir. Bu durumda, bu biçimlendirmeyi biçim yapılandırmasına, biçimlendirme ifadesine sahip adlandırılmış bir dönüştürme olarak bir kez girebilirsiniz. Daha sonra, bu adlandırılmış dönüşüm, oluşturduğunuz biçimlendirme ifadesine çıktının biçimlendirilmesi gereken birçok biçim bileşenine bağlanabilir.

Bu tür bir dönüştürmenin tasarımı aşağıda gösterilmiştir. Bu örnekte, **TrimmedString** dönüşümü, *Dize* veri türünden gelen verileri baştaki ve sondaki boşlukları kaldırarak keser. Bunun ardından, kesilmiş dize değerini döndürür.

[![Dönüşüm.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Aşağıdaki çizim bu tür bir dönüştürmenin nasıl kullanılabileceğini gösterir. Bu örnekte, birçok biçim bileşeni metni çıktı olarak çalışma zamanında oluşturulan elektronik belgeye gönderir. Bu biçim bileşenlerinin tümü ada göre **TrimmedString** dönüştürmesine başvurur.

[![Kullanılan dönüştürme.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Önceki örnekte yer alan **partyName** gibi biçim bileşenleri **TrimmedString** dönüşümüne referansta bulunur, dönüştürme metni çıktı olarak oluşturulan elektronik belgeye gönderir. Bu metin baştaki ve sondaki boşlukları içermez.

Tek tek uygulanması zorunlu olan bir biçimlendirmeniz varsa, bu biçimlendirmeyi belirli bir biçim bileşeninin bir bağlamasının tekil ifadesi olarak tanıtabilirsiniz. Aşağıdaki çizim bu türde bir ifadeyi gösterir. Bu örnekte **partyType** biçim bileşeni veri kaynağındaki **Model.Company.RegistrationType** alanından gelen veriyi büyük harfe dönüştüren bir ifade aracılığıyla veri kaynağına bağlıdır. Sonra ifade metni çıktı olarak elektronik belgeye gönderir.

[![Ayrı bir bileşene biçimlendirme uygulama.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>İşlem akış denetimi

ER formül tasarımcısı, elektronik belge oluşturma işlem akışını denetleyen ifadeleri tanımlamak için kullanılabilir. Aşağıdaki görevlerini yerine getirebilirsiniz:

- Bir belge oluşturma işleminin ne zaman durdurulması gerektiği koşullarını tanımlayın.
- Durdurulan işlemler hakkında kullanıcıya iletiler oluşturan veya devam eden rapor oluşturma işlemleri hakkında yürütme günlüğü iletileri oluşturan ifadeleri belirtin.
- Oluşturulan elektronik belgelerinin dosya adlarını belirtin ve bunların oluşturulma koşullarını denetleyin.

İşlem akışı denetiminin her kuralı ayrı ayrı bir doğrulama olarak tasarlanmıştır. Aşağıdaki çizim bu türde bir doğrulamayı gösterir. u örnekteki yapılandırmanın bir açıklaması aşağıdadır:

- Doğrulama, XML dosyasının oluşturulduğu sırada **INSTAT** düğümü oluşturulurken değerlendirilir.
- Hareketin listesi boşsa, doğrulama işlem yürütmesini durdurur ve **YANLIŞ** döndürür.
- Doğrulama, kullanıcının tercih ettiği dilde SYS70894 etiket metnini içeren bir hata iletisi döndürür.

[![Doğrulama.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

ER formül tasarımcısı elektronik belgenin oluşturulması ve dosya oluşturma işlemini denetlemek için bir dosya adı oluşturmak için de kullanılabilir. Aşağıdaki çizim, bu türdeki bir işlem akış denetiminin tasarımını gösterir. u örnekteki yapılandırmanın bir açıklaması aşağıdadır:

- **model.Intrastat** veri kaynağındaki kayıtların listesi toplu işlere bölünür. Her toplu iş en çok 1000 kayıt içerir.
- Çıktı her toplu işlem için XML biçiminde oluşturulmuş bir dosya içeren bir zip dosyası oluşturur.
- Bir ifade, elektronik belge oluşturması için dosya adı ve dosya adı uzantısını birleştirerek bir dosya adı döndürür. İkinci toplu iş ve tüm sonraki toplu işler için, dosya adı toplu iş kimliğini bir sonek olarak içerir.
- Bir ifade (**DOĞRU** döndürerek) en az bir kayıt içeren toplu işler için dosya oluşturma işlemini etkinleştirir.

[![İşlem akış denetimi.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Belge içeriği denetimi

ER formül tasarımcısı, çalışma zamanında oluşturulan elektronik belgelere hangi verilerin yerleştirileceğini denetleyen ifadeleri konfigüre etmek için kullanılabilir. İfadeler veri işlemeye ve konfigürasyon mantığına bağlı olarak biçimin belirli öğelerinin çıkışını etkinleştirebilir veya devre dışı bırakabilir. Bu deyimler, **Operasyonlar tasarımcısı** sayfasındaki **Eşleştirme** sekmesinde bulunan **Etkin** alanına tek bir biçim öğesi için girilebilir. İfadeleri *Boole* değeri döndüren bir mantık koşulu olarak girebilirsiniz:

- Koşul **true** dönerse, geçerli biçim öğesi çalıştırılır.
- Koşul **false** dönerse, geçerli biçim öğesi atlanır.

Aşağıdaki çizim bu türde bir ifadeyi gösterir. (Microsoft tarafından sağlanan **ISO20022 kredi transfer (No)** biçimi konfigürasyonunun sürüm 11.12.11 bir örnek olarak kullanılmıştır.) **Xmlheader** biçim bileşeni, ISO 20022 XML ileti standartlarına göre kredi aktarım iletisinin yapısını açıklamak için yapılandırılmıştır. **Xmlheader/Document/Cstmrcdttrfınitn/PmtInf/CdtTrfTxInf/Rmtinf/Ustrd** Format bileşeni oluşturulan iletiye eklemek için konfigüre edilir, **Ustrd** XML öğesi ve havale bilgilerini aşağıdaki XML öğelerinin metin olarak yapılandırılmamış biçimi:

- **PaymentNotes** bileşeni ödeme notlarının metnini oluşturmak için kullanılır.
- **DelimitedSequence** bileşeni, geçerli kredi transferini kapatmak için kullanılan virgülle ayrılmış fatura numaralarını oluşturur.

[![PaymentNotes ve DelimitedSequence bileşenleri.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> **PaymentNotes** ve **DelimitedSequence** bileşenleri soru işareti kullanılarak etiketlenir. Soru işareti, bileşen kullanmanın koşullu olduğunu belirtir. Bu durumda, bileşenlerin kullanımı aşağıdaki ölçütlere dayanır:
>
> - **PaymentNotes** bileşeni için tanımlanan `@.PaymentsNotes <> ""` ifadesi, popülasyonu **Ustrd** XML öğesine, geçerli kredi transferi için bu metin boş olmadığında ödeme notları metnini etkinleştirir (**Doğru** olarak döndürerek).
>
>    [![PaymentNotes bileşeni için ifade.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - **DelimitedSequence** bileşeni için tanımlanmıştır `@.PaymentsNotes = ""` ifadesi, (**DOĞRU** değerini döndürerek) popülasyonu bu kredi transferi için ödeme notları metni boş olduğunda, mevcut kredi transferini düzenlemek için kullanılan virgül fatura numaraları **Ustrd** XML öğesine döndürerek ayırır.
>
>    [![DelimitedSequence bileşeni için ifade.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Bu ayara dayalı olarak, her bir borçlu ödeme, **Ustrd** XML öğesi için oluşturulan ileti, her bir ödeme notu metnini içerecektir veya bu metin boş olduğunda, bu ödemeyi kapatmak için kullanılan virgüllü fatura numaralarıyla ayrılmış metin içerir.

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Yapılandırılan formüllerin doğrulanması

Konfigüre edilen formülün nasıl çalıştığını doğrulamak için **formül Tasarımcısı** sayfasında **test**'i seçin.

[![Bir formülü doğrulamak için testi seçme.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Formül bağımsız değişkenlerinin değerleri gerektiğinde,**formül Tasarımcısı** sayfasında **test ifadesi** iletişim kutusunu açabilirsiniz. Çoğu durumda, yapılandırılan bağlamalar tasarım zamanında çalıştırılmadığından, bu bağımsız değişkenlerin el ile tanımlanması gerekir. **Formül Tasarımcısı** sayfasındaki **test sonucu** sekmesi yapılandırılan formülün yürütülmesinden elde edilen sonucu gösterir.

Aşağıdaki örnek, Intrastat emtia kodunda yalnızca rakamlar bulunduğundan emin olmak için yabancı ticari etki alanı için konfigüre edilen formülü nasıl test edebileceğinizi gösterir.

Bu formülü test ettiğinizde, **test ifadesi** iletişim kutusunu, test için Intrastat Emtia kodunun değerini belirtmek için kullanabilirsiniz.

[![Test için Intrastat Emtia kodunu belirtme.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Intrastat Emtia kodunu belirledikten ve **Tamam**'ı seçtiğinizde, **formül Tasarımcısı** sayfasındaki **test sonucu** sekmesi konfigüre edilen formülün yürütülme sonucunu gösterir. Böylece, sonucun kabul edilebilir olup olmadığı değerlendirebilirsiniz. Sonuç kabul edilebilir değilse, formülü güncelleştirebilir ve tekrar test edebilirsiniz.

[![Test sonucu.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Bazı formüller tasarım zamanında sınanamaz. Örneğin, bir formül **test sonucu** sekmesinde görüntülenemeyen bir veri türünün sonucunu döndürebilir. Bu durumda, formülün sınanmamakta olmadığını bildiren bir hata iletisi alırsınız.

[![Hata iletisi.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Elektronik raporlamada formül dili](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]