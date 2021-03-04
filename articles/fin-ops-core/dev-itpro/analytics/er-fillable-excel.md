---
title: Excel biçiminde belgeler oluşturmak için bir yapılandırma tasarlama
description: Bu konuda, bir Excel şablonunu doldurmak ve ardından giden Excel biçimi belgeleri oluşturmak için Elektronik raporlama (ER) biçiminin nasıl tasarlanacağı hakkında bilgi verilmektedir.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: d5733e40c67f9c97b04f126f7c3cfea9d4f8f5b5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686550"
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
> Şablonu el ile eklediğinizde [ER parametreleri](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)'nde bu amaçla yapılandırılmış bir [belge türü](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) kullanmanız gerekir.

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

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama](tasks\er-design-reports-openxml-2016-11.md)

[Excel şablonlarını yeniden uygulayarak Elektronik raporlama biçimlerini değiştirme](modify-electronic-reporting-format-reapply-excel-template.md)

[Excel raporlarına dinamik olarak sütun eklemek için yatay olarak genişletilebilir aralıkları kullanma](tasks/er-horizontal-1.md)

[Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

[Power BI'a veri çekmek için Elektronik raporlamayı (ER) yapılandırma](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]