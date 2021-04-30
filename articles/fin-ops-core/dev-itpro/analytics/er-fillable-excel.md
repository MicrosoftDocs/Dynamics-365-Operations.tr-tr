---
title: Excel biçiminde belgeler oluşturmak için yapılandırma tasarlama
description: Bu konuda, bir Excel şablonunu doldurmak ve ardından giden Excel biçimi belgeleri oluşturmak için Elektronik raporlama (ER) biçiminin nasıl tasarlanacağı açıklanmaktadır.
author: NickSelin
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c8d939fef4fd0f9e189ca37318c2c0306511785
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893920"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Excel biçiminde belgeler oluşturmak için bir yapılandırma tasarlama

[!include[banner](../includes/banner.md)]

Microsoft Excel çalışma kitabı biçiminde giden bir belge oluşturmak için yapılandırabileceğiniz bir ER [biçim bileşeni](general-electronic-reporting.md#FormatComponentOutbound) olan bir [Elektronik raporlama (ER)](general-electronic-reporting.md) biçimi yapılandırması tasarlayabilirsiniz. Bu amaçla belirli ER biçimli bileşenler kullanılmalıdır.

Bu özellik hakkında daha fazla bilgi edinmek için [OPENXML biçiminde raporlar oluşturmak için yapılandırma tasarlama](tasks/er-design-reports-openxml-2016-11.md) konusundaki adımları izleyin.

## <a name="add-a-new-er-format"></a>Yeni bir ER biçimi ekleme

Excel çalışma kitabı biçiminde giden bir belge oluşturmak için yeni bir ER biçimi yapılandırması eklediğinizde biçimin **Biçim türü** özniteliği için **Excel** değerini seçmeniz veya **Biçim türü** özniteliğini boş bırakmanız gerekir.

- **Excel**'i seçerseniz giden belgeyi yalnızca Excel biçiminde oluşturacak şekilde yapılandırabilirsiniz.
- Özniteliği boş bırakırsanız biçimi ER çerçevesi tarafından desteklenen herhangi bir biçimde, giden bir belge oluşturacak şekilde yapılandırabilirsiniz.

Yapılandırmanın ER biçimi bileşenini yapılandırmak için Eylem Bölmesi'nde **Tasarımcı**'yı seçin ve ER İşlem tasarımcısında düzenleme için ER biçimi bileşenini açın.

![Yapılandırma sayfası](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel dosya bileşeni

### <a name="manual-entry"></a>El ile yapılan giriş

Excel biçiminde giden bir belge oluşturmak için yapılandırılmış ER biçimine bir **Excel\\File** bileşeni eklemeniz gerekir.

![Excel\File bileşeni](./media/er-excel-format-add-file-component.png)

Giden belgenin düzenini belirtmek için giden belgelerin şablonu olarak **Excel\\File** bileşenine .xlsx uzantısına sahip bir Excel çalışma kitabı ekleyin.

> [!NOTE]
> Şablonu el ile eklediğinizde [ER parametreleri](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)'nde bu amaçla yapılandırılmış bir [belge türü](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) kullanmanız gerekir.

![Excel\File bileşenine bir ek ekleme](./media/er-excel-format-add-file-component2.png)

Yapılandırılmış ER biçimini çalıştırdığınızda ekteki şablonun nasıl doldurulacağını belirtmek için **Excel\\File** bileşenine iç içe geçirilmiş **Sayfa**, **Aralık** ve **Hücre** bileşenleri eklemelisiniz. Her iç içe geçirilmiş bileşen, adlandırılmış bir Excel öğesi ile ilişkilendirilmelidir.

### <a name="template-import"></a>Şablon içe aktarma

Yeni bir şablonu boş bir ER biçimine aktarmak için Eylem Panosu'nun **İçe Aktar** sekmesinde **Excel'den İçe Aktar**'ı seçebilirsiniz. Bu örnekte, otomatik olarak bir **Excel\\File** bileşeni oluşturulacak ve içe aktarılan şablon buna eklenecektir. Gereken tüm ER bileşenleri, keşfedilen adlandırılmış Excel öğelerinin listesine göre otomatik olarak oluşturulur.

![Excel'den İçe Aktar'ı seçme](./media/er-excel-format-import-template.png)

> [!NOTE]
> İsteğe bağlı **Sayfa** öğesini, düzenlenebilir ER biçiminde oluşturmak istiyorsanız **Excel Sayfası biçim öğesi oluşturma** seçeneğini **Evet** olarak ayarlayın.

## <a name="sheet-component"></a>Sayfa bileşeni

**Sayfa** bileşeni, ekli Excel çalışma kitabının doldurulması gereken bir çalışma sayfasını belirtir. Excel şablonundaki çalışma sayfasının adı, bu bileşenin **Sayfa** özelliğinde tanımlanır.

> [!NOTE]
> Bu bileşen, tek bir çalışma sayfası içeren Excel çalışma kitapları için isteğe bağlıdır.

ER İşlem tasarımcısının **Eşleme** sekmesinde, bileşenin oluşturulan bir belgeye konulması gerekip gerekmediğini belirtmek için bir **Sayfa** bileşeni için **Etkin** özelliğini yapılandırabilirsiniz:

- **Etkin** özelliğinin bir ifadesi, çalışma zamanında **Doğru** değerini döndürecek şekilde yapılandırılmışsa veya hiçbir ifade yapılandırılmamışsa uygun çalışma sayfası, oluşturulan belgeye yerleştirilir.
- **Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** döndürecek şekilde yapılandırılırsa oluşturulan belge bir çalışma sayfası içermez.

![Sayfa bileşeni örneği](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Aralık bileşeni

**Aralık** bileşeni, ER bileşeni tarafından kontrol edilmesi gereken bir Excel aralığını belirtir. Aralığın adı, bu bileşenin **Excel aralığı** özelliğinde tanımlanır.

**Yineleme yönü** özelliği, aralığın oluşturulan bir belgede tekrarlanıp tekrarlanmayacağını ve nasıl tekrarlanacağını belirtir:

- **Yineleme yönü** özelliği **Yineleme yok** olarak ayarlanırsa oluşturulan Excel'de uygun Excel aralığı yinelenmez.
- **Yineleme yönü** özelliği **Dikey** olarak ayarlanırsa oluşturulan Excel'de uygun Excel aralığı yinelenir. Yinelenen her aralık, bir Excel şablonundaki orijinal aralığın altına yerleştirilir. Yineleme sayısı, ER bileşenine bağlı **Kayıt listesi** türünün bir veri kaynağındaki kayıt sayısı ile tanımlanır.
- **Yineleme yönü** özelliği **Yatay** olarak ayarlanırsa oluşturulan Excel'de uygun Excel aralığı yinelenir. Yinelenen her aralık, bir Excel şablonundaki orijinal aralığın sağına yerleştirilir. Yineleme sayısı, ER bileşenine bağlı **Kayıt listesi** türünün bir veri kaynağındaki kayıt sayısı ile tanımlanır.

Yatay yineleme hakkında daha fazla bilgi edinmek için [Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma](tasks/er-horizontal-1.md) bölümündeki adımları izleyin.

**Aralık** bileşeni, adlandırılmış uygun Excel aralıklarındaki değerleri girmek için kullanılan diğer iç içe geçirilmiş ER bileşenlerine sahip olabilir.

- Değerleri girmek için **Metin** grubunun herhangi bir bileşeni kullanılırsa değer, bir Excel aralığına metin değeri olarak girilir.

    > [!NOTE]
    > Girilen değerleri, uygulamada tanımlanan yerel ayara göre biçimlendirmek için bu deseni kullanın.

- Değerleri girmek için **Excel** grubunun **Hücre** bileşeni kullanılıyorsa değer, bir Excel aralığına **Hücre** bileşeninin bağlanmasıyla tanımlanan veri türünün değeri olarak girilir (örneğin, **Dize**, **Gerçek** veya **Tamsayı**).

    > [!NOTE]
    > Excel uygulamasının, girilen değerleri giden belgeyi açan yerel bilgisayarın yerel ayarına göre biçimlendirmesini sağlamak için bu deseni kullanın.

ER İşlem tasarımcısının **Eşleme** sekmesinde, bileşenin oluşturulan bir belgeye konulması gerekip gerekmediğini belirtmek için bir **Aralık** bileşeni için **Etkin** özelliğini yapılandırabilirsiniz:

- **Etkin** özelliğinin bir ifadesi, çalışma zamanında **Doğru** değerini döndürecek şekilde yapılandırılmışsa veya hiçbir ifade yapılandırılmamışsa uygun aralık, oluşturulan belgeye doldurulur.
- **Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** değerini döndürecek şekilde yapılandırılmışsa ve bu aralık tüm satırları veya sütunları temsil etmiyorsa oluşturulan belge içinde uygun aralık doldurulmaz.
- **Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** değerini döndürmek üzere yapılandırılmışsa ve bu aralık, tüm satırları veya sütunları temsil ediyorsa oluşturulan belge, bu satırları ve sütunları gizli satırlar ve sütunlar olarak içerir.

## <a name="cell-component"></a>Hücre bileşeni

**Hücre** bileşeni; adlandırılmış Excel hücrelerini, şekillerini ve resimlerini doldurmak için kullanılır. **Hücre** ER bileşeni tarafından doldurulması gereken bir adlandırılmış Excel nesnesini belirtmek için **Hücre** bileşeninin **Excel aralığı** özelliğinde bu nesnenin adını belirtmeniz gerekir.

ER İşlem tasarımcısının **Eşleme** sekmesinde, nesnenin oluşturulan bir belge içine doldurulmasının gerekip gerekmediğini belirtmek üzere bir **Hücre** bileşeni için **Etkin** özelliğini yapılandırabilirsiniz:

- **Etkin** özelliğinin bir ifadesi, çalışma zamanında **Doğru** değerini döndürecek şekilde yapılandırılmışsa veya hiçbir ifade yapılandırılmamışsa uygun nesne, oluşturulan belgeye doldurulur. Bu **Hücre** bileşeninin bağlanması, uygun nesneye koyulan bir değeri belirtir.
- **Etkin** özelliğinin bir ifadesi, çalışma zamanında **Yanlış** döndürecek şekilde yapılandırılırsa uygun nesne oluşturulan belgeye doldurulmaz.

**Hücre** bileşeni, hücreye bir değer girilecek şekilde yapılandırıldığında ilkel veri türünün değerini döndüren bir veri kaynağına bağlanabilir (örneğin, **Dize**, **Gerçek** veya **Tamsayı**). Bu durumda değer, hücreye aynı veri türünün değeri olarak girilir.

**Hücre** bileşeni, bir Excel şekline bir değer girilecek şekilde yapılandırıldığında ilkel veri türünün değerini döndüren bir veri kaynağına bağlanabilir (örneğin, **Dize**, **Gerçek** veya **Tamsayı**). Bu durumda değer, Excel şekline o şeklin metni olarak girilir. **Dize** olmayan veri türlerinin değerleri için metne dönüştürme otomatik olarak yapılır.

> [!NOTE]
> **Hücre** bileşenini, yalnızca şekil metni özelliğinin desteklendiği durumlarda bir şekli dolduracak şekilde yapılandırabilirsiniz.

**Hücre** bileşeni, bir Excel resminde bir değer girilecek şekilde yapılandırıldığında ikili biçimdeki görüntüyü temsil eden **Kapsayıcı** veri türünün değerini döndüren bir veri kaynağına bağlanabilir. Bu durumda değer, Excel resmine görüntü olarak girilir.

> [!NOTE]
> Her Excel resmi ve şekli, sol üst köşesi tarafından belirli bir Excel hücresine veya aralığına tutturulmuş olarak kabul edilir. Excel resmini veya şeklini yinelemek istiyorsanız tutturulduğu hücreyi veya aralığı yinelenmiş hücre veya aralık olarak yapılandırmanız gerekir.

Görüntüleri ve şekilleri gömme hakkında daha fazla bilgi için, bkz. [ER kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

## <a name="page-break-component"></a>Sayfa sonu bileşeni

**PageBreak** bileşeni, Excel'i yeni bir sayfa başlatmaya zorlar. Excel'in varsayılan sayfalandırmasını kullanmak istediğinizde bu bileşen gerekli değildir ancak Excel'in, ER biçiminizle sayfalandırmayı yapılandırmasını istediğinizde bunu kullanmanız gerekir.

## <a name="footer-component"></a>Alt bilgi bileşeni

**Alt bilgi** bileşeni, Excel çalışma kitabında oluşturulan çalışma sayfasının alt bilgilerini doldurmak için kullanılır.

> [!NOTE]
> Oluşturulan Excel çalışma kitabındaki farklı çalışma sayfaları için farklı alt bilgileri belirtmek üzere her **sayfa** bileşeni için bu bileşeni ekleyebilirsiniz.

Tek bir **Alt bilgi** bileşenini yapılandırdığınızda, bileşenin kullanıldığı sayfaları belirlemek için **üst bilgi/alt bilgi görünümü** özelliğini kullanabilirsiniz. Aşağıdaki değerler kullanılabilir:

- **Herhangi biri:** Ana Excel çalışma sayfasının herhangi bir sayfası için yapılandırılmış **alt bilgi** bileşenini çalıştırın.
- **İlk**: Ana Excel çalışma sayfasının sadece ilk sayfası için yapılandırılmış **alt bilgi** bileşenini çalıştırın.
- **Çift sayı**: Ana Excel çalışma sayfasının sadece çift sayılı sayfaları için yapılandırılmış **alt bilgi** bileşenini çalıştırın.
- **Tek sayı**: Ana Excel çalışma sayfasının sadece tek sayılı sayfaları için yapılandırılmış **alt bilgi** bileşenini çalıştırın.

Tek bir **sayfa** bileşeni için, her biri **üst bilgi/alt bilgi görünümü** özelliği için farklı bir değere sahip birkaç **alt bilgi** bileşeni ekleyebilirsiniz. Bu şekilde, Excel çalışma sayfasındaki farklı sayfa türleri için farklı alt bilgiler oluşturabilirsiniz.

> [!NOTE]
> Tek bir **sayfa** bileşeni için eklediğiniz her bir **alt bilginin** **üst bilgi/alt bilgi görünümü** özelliği için farklı bir değere sahip olduğundan emin olun. Aksi takdirde, [doğrulama hatası](er-components-inspections.md#i16) oluşur. Aldığınız hata iletisi, tutarsızlık hakkında sizi uyarır.

Eklenen **alt bilgi** bileşeni altında **metin\\Dize**, **Metin\\Tarih/Saat** veya başka bir türün gerekli iç içe bileşenlerini ekleyin. Sayfa alt bilginizin nasıl doldurulacağını belirtmek için bu bileşenler için bağları yapılandırın.

Oluşturulan bir alt bilginin içeriğini doğru şekilde biçimlendirmek için özel [biçimlendirme kodları](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) da kullanabilirsiniz. Bu yaklaşımın nasıl kullanılacağını öğrenmek için, Bu konunun ilerleyen kısımlarında [örnek 1](#example-1)'deki adımları izleyin.

> [!NOTE]
> ER biçimlerini yapılandırdığınızda, Excel [sınırını](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) ve tek bir üst bilgi ya da alt bilgi için maksimum karakter sayısını göz önünde bulundurmaya dikkat edin.

## <a name="header-component"></a>Üst bilgi bileşeni

**Üst bilgi** bileşeni, Excel çalışma kitabında oluşturulan çalışma sayfasının üst bilgilerini doldurmak için kullanılır. **Alt bilgi** bileşeni gibi kullanılır.

## <a name="edit-an-added-er-format"></a>Eklenen bir ER biçimini düzenleme

### <a name="update-a-template"></a>Şablon güncelleştirme

Güncelleştirilmiş bir şablonu düzenlenebilir bir ER biçimine aktarmak için Eylem Panosu'nun **İçe Aktar** sekmesinde **Excel'den Güncelleştir**'i seçebilirsiniz. Bu işlem sırasında, seçili **Excel\\Dosya** bileşeninin bir şablonu yeni bir şablonla değiştirilecektir. Düzenlenebilir ER biçiminin içeriği, güncelleştirilmiş ER şablonunun içeriği ile senkronize edilecektir.

- ER biçimi bileşeni, düzenlenebilir biçimde bulunmazsa her Excel adı için otomatik olarak yeni bir ER biçimi bileşeni oluşturulur.
- Her ER biçimi bileşeni, uygun Excel adı bulunamazsa düzenlenebilir ER biçiminden silinir.

> [!NOTE]
> Düzenlenebilir ER biçiminde isteğe bağlı **Sayfa** öğesi oluşturmak istiyorsanız **Excel Sayfası biçim öğesi oluşturma** seçeneğini **Evet** olarak ayarlayın.
>
> Düzenlenebilir ER biçimi, başlangıçta **Sayfa** öğeleri içeriyorsa güncelleştirilmiş bir şablonu içe aktardığınızda **Excel Sayfası biçim öğesi oluşturma** seçeneğini **Evet** olarak ayarlamanızı öneririz. Aksi takdirde, özgün **Sayfa** öğesinin tüm iç içe geçirilmiş öğeleri sıfırdan oluşturulacaktır. Bu nedenle, yeniden oluşturulan biçim öğelerinin tüm bağları güncelleştirilmiş ER biçiminde kaybolacaktır.

![Excel iletişim kutusundan Güncelleştir'de Excel Çalışma Sayfası biçim öğesi oluşturma seçeneği](./media/er-excel-format-update-template.png)

Bu özellik hakkında daha fazla bilgi edinmek için [Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme](modify-electronic-reporting-format-reapply-excel-template.md) bölümündeki adımları izleyin.

## <a name="validate-an-er-format"></a>ER biçimini doğrulama

Düzenlenebilir bir ER biçimini doğruladığınızda Excel adının şu anda kullanılan Excel şablonunda bulunduğundan emin olmak için bir tutarlılık denetimi yapılır. Herhangi bir tutarsızlık size bildirilecektir. Bazı tutarsızlıklar için sorunları otomatik olarak düzeltme seçeneği sunulur.

![Doğrulama hatası iletisi](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Excel formüllerinin hesaplamasını denetleme

Microsoft Excel çalışma kitabı biçiminde giden bir belge oluşturulduğunda, söz konusu belgenin bazı hücrelerinde Excel formülleri olabilir. **Elektronik raporlama çerçevesinde EPPlus kitaplığı kullanımını etkinleştir** özelliği etkinleştirildiğinde, kullanılan Excel şablonundaki **Hesaplama Seçenekleri** [parametresinin](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) değerini değiştirerek formüllerin ne zaman hesaplanacağını kontrol edebilirsiniz.

- Oluşturulan belgeye yeni aralıklar, hücreler vb. her eklendiğinde tüm bağımlı formülleri yeniden hesaplamak için **Otomatik**'i seçin.
    >[!NOTE]
    > Bu, birden çok ilişkili formül içeren Excel şablonları için performans sorununa neden olabilir.
- Belge oluşturulduğunda formüllerin yeniden hesaplanmasını önlemek için **El ile** seçeneğini belirleyin.
    >[!NOTE]
    > Formülün yeniden hesaplanması, oluşturulan belge Excel kullanılarak önizleme için açıldığında el ile gerçekleştirilir.
    > Oluşturulan belgede, formül içeren hücrelerde değer bulunmayabilir. Bu nedenle, Excel'de önizleme olmadan oluşturulan belge kullanımını varsayan bir ER hedefi (PDF dönüşümü, posta gönderme) yapılandırırken bu seçeneği kullanmayın.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Örnek 1: Alt bilgi içeriğini Biçimlendir

1. Yazdırılabilir bir serbest metin faturası (FTI) belgesi [oluşturmak](er-generate-printable-fti-forms.md) için sağlanan ER yapılandırmalarını kullanın.
2. Oluşturulan belgenin alt bilgisini gözden geçirin. Geçerli sayfa numarası ve belgedeki toplam sayfa sayısı hakkında bilgi içerdiğine dikkat edin.

    ![Excel biçiminde Oluşturulan belgenin alt bilgisini gözden geçirme](./media/er-fillable-excel-footer-1.gif)

3. ER biçim tasarımcısında gözden geçirmek için örnek ER biçimini [açın](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format).

    **Fatura** çalışma sayfasının alt bilgisi, **Alt bilgi** bileşeni altında bulunan iki **dize** bileşeninin ayarlarına göre oluşturulur:

    - İlk **dize** bileşeni, Excel'i belirli bir biçimlendirmeyi uygulamaya zorlamak için aşağıdaki özel biçimlendirme kodlarını doldurur:

        - **&C**: Alt bilgi metnini ortaya hizalar.
        - **&"Segoe UI,Regular"&8**: Alt bilgi metnini "Segoe UI Regular" 8 punto boyutundaki yazı tipinde gösterir.

    - İkinci **dize** bileşeni, geçerli sayfa numarasını ve geçerli belgedeki toplam sayfa sayısını içeren metni doldurur.

    ![Biçim tasarımcısı sayfasında ER biçimi bileşeni alt bilgisini gözden geçirme](./media/er-fillable-excel-footer-2.png)

4. Geçerli Sayfa alt bilgisini değiştirmek için örnek ER biçimini özelleştirin:

    1. Örnek ER biçimini temel alan türetilmiş **serbest metin faturası (Excel) özel** ER biçimi [oluşturun](er-quick-start2-customize-report.md#DeriveProvidedFormat).
    2. **Fatura** çalışma sayfasının **alt bilgi** bileşeni için ilk yeni **dize** çifti bileşenlerini ekleyin:

        1. Şirket adını sola hizalayan ve 8 punto "Segoe UI Regular" yazı tipinde (**"&L&"Segoe UI, normal"&8"**) sunan bir **dize** bileşeni ekleyin.
        2. Şirket adını (**model.InvoiceBase.CompanyInfo.Name**) dolduran bir **dize** bileşeni ekleyin.

    3. **Fatura** çalışma sayfasının **alt bilgi** bileşeni için ikinci bir yeni **dize** çifti bileşenleri ekleyin:

        1. İşlem tarihini sağa hizalayan ve 8 punto "Segoe UI Regular" yazı tipinde (**"&R&"Segoe UI, normal"&8"**) sunan bir **dize** bileşeni ekleyin.
        2. İşleme tarihini özel bir biçimde (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd)**) dolduran bir dize **bileşeni** ekleyin.

        ![Biçim tasarımcısı sayfasında ER biçimi bileşeni alt bilgisini gözden geçirme](./media/er-fillable-excel-footer-3.png)

    4. Türetilmiş **serbest metin faturası (Excel) özel** ER biçiminin taslak sürümünü [tamamlayın](er-quick-start2-customize-report.md#CompleteDerivedFormat).

5. Yazdırma yönetimini örnek ER biçimi yerine, türetilmiş **serbest metin faturası (Excel) özel** ER biçimini kullanacak şekilde [yapılandırın](er-generate-printable-fti-forms.md#configure-print-management).
6. Yazdırılabilir bir FTI belgesi oluşturun ve oluşturulan belgenin alt bilgisini gözden geçirin.

    ![Excel biçiminde Oluşturulan belgenin alt bilgisini gözden geçirme](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama](tasks\er-design-reports-openxml-2016-11.md)

[Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme](modify-electronic-reporting-format-reapply-excel-template.md)

[Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma](tasks/er-horizontal-1.md)

[Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

[Power BI'a veri çekmek için Elektronik raporlamayı (ER) yapılandırma](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]