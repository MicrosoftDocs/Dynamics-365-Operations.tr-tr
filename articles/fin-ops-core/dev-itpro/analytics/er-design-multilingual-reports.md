---
title: Elektronik raporlamada çok dilli raporlar tasarlama
description: Bu konu, çok dilli raporlar tasarlamak ve oluşturmak için Elektronik raporlama (ER) etiketlerini nasıl kullanabileceğinizi açıklamaktadır.
author: NickSelin
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf02e8f90fb83acd8448339f411489851742af18
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674441"
---
# <a name="design-multilingual-reports-in-electronic-reporting"></a>Elektronik raporlamada çok dilli raporlar tasarlama

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Özet

Bir iş kullanıcısı olarak, [Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesini, çeşitli ülkelerin veya bölgelerin yasal gereksinimlerine uygun şekilde oluşturulması gereken giden belgeler için biçimler yapılandırmak amacıyla kullanabilirsiniz. Bu gereksinimler, giden belgelerin farklı ülkeler veya bölgeler için farklı dillerde oluşturulmasını gerektirdiğinde, dile bağlı kaynaklar içeren tek bir ER [biçimi](general-electronic-reporting.md#FormatComponentOutbound) yapılandırabilirsiniz. Bu şekilde, çeşitli ülkeler veya bölgeler için giden belgeler oluşturmak üzere biçimi yeniden kullanabilirsiniz. Ayrıca, bir giden belgeyi ilgili müşteriler, satıcılar, alt kuruluşlar veya diğer taraflar için farklı dillerde oluşturmak üzere tek bir ER biçimi kullanmak isteyebilirsiniz.

ER veri modellerini ve model eşlemelerini, oluşturulan belgelere hangi uygulama verilerinin konulacağını belirleyen veri akışını tanımlamak için yapılandırılmış ER biçimlerinin veri kaynakları olarak yapılandırabilirsiniz. Bir ER yapılandırma [sağlayıcısı](general-electronic-reporting.md#Provider) olarak, belirli giden belgeleri oluşturmak üzere ER çözümünün bileşenleri olarak yapılandırılmış [veri modelleri](general-electronic-reporting.md#data-model-and-model-mapping-components), [model eşlemeleri](general-electronic-reporting.md#data-model-and-model-mapping-components) ve [biçimler](general-electronic-reporting.md#FormatComponentOutbound) [yayımlayabilirsiniz](tasks/er-upload-configuration-into-lifecycle-services.md#upload-a-configuration-into-lcs). Müşterilerin, kullanılabilmesi ve özelleştirilebilmesi için yayımlanmış ER çözümü [yüklemesine](general-electronic-reporting-manage-configuration-lifecycle.md) olanak tanıyabilirsiniz. Müşterilerin başka dillerde konuşabildiğini düşünüyorsanız, ER bileşenlerini dile bağlı kaynaklar içerecek şekilde yapılandırabilirsiniz. Bu şekilde, düzenlenebilir bir ER bileşeninin içeriği, tasarım zamanında müşterinin kullanıcı tarafından tercih edilen dilinde sunulabilir.

Dile bağlı kaynakları ER etiketleri olarak yapılandırabilirsiniz. Böylece, ER bileşenlerini aşağıdaki amaçlarla yapılandırmak için bu etiketleri kullanabilirsiniz:

- Tasarım zamanında:

    - Yapılandırılan ER bileşenlerinin içeriğini kullanıcı tarafından tercih edilen dilde sunun.

- Çalışma zamanında:

    - Giden belgeler için dile bağlı içerik oluşturun.
    - Kullanıcı tarafından tercih edilen dilde uyarı ve hata iletileri sağlayın.
    - Kullanıcı tarafından tercih edilen dilde gerekli alanlar için istemde bulun.

ER etiketleri, farklı bileşenler içeren her bir ER [yapılandırmasında](general-electronic-reporting.md#Configuration) yapılandırılabilir. Etiketler, ER veri modellerinin, ER model eşlemelerinin ve ER biçim bileşenlerinin yapılandırılmış mantığından bağımsız olarak korunabilir.

Her ER etiketi, o etiketi tutan ER yapılandırmasının kapsamında benzersiz olan bir kimlikle tanımlanır. Her etiket, Microsoft Dynamics 365 Finance'ın geçerli örneğinde desteklenen her dil için etiket metni içerebilir. Desteklenen bu diller, dağıtılan özelleştirmelerin dillerini içerir.

## <a name="entry"></a>Giriş

Bir ER veri modeli, ER model eşlemesi veya ER biçimi tasarladığınızda, çevrilebilir içerik içerebilecek bir alanı seçişinizde **Çevir** seçeneği gösterilir. Bu seçeneği belirlediğinizde, seçili alanı **Metin çevirisi** <a name="TextTranslationPane">bölmesindeki</a> bir ER etiketine bağlayabilirsiniz. Varolan bir ER etiketi seçebilir veya henüz kullanılabilir değilse yeni bir ER etiketi ekleyebilirsiniz. Bir ER etiketini seçer ya da eklerseniz, geçerli Finance örneğindeki desteklenen her dil için ilgili metin ekleyebilirsiniz.

Aşağıdaki şekil, bu çevirinin düzenlenebilir bir ER veri modelinde nasıl yapıldığını gösterir. Bu örnekte, düzenlenebilir **Fatura modeli** için **PurchaseOrder** alanının **Açıklama** özniteliği Avusturya Almancası (DE-AT) ve Japonca (JA) dillerine çevrilir.

![ER veri modeli tasarımcısında bir ER etiketinin çevirisini sağlama.](./media/er-multilingual-labels-refer.png)

Düzenlenebilir ER bileşeninde bulunan etiketler için yalnızca etiket metni çevrilebilir. Örneğin, bir ER model eşleme veri kaynağının etiket özniteliği için **Çevir**'i seçerseniz ve daha sonra üst ER veri modelinde bulunan bir ER etiketi seçerseniz, etiketin içeriğini görürsünüz ancak bunu değiştiremezsiniz. Bu gibi durumlarda, **Çevrilmiş metin** alanı aşağıdaki çizimde gösterildiği gibi kullanılamaz.

![ER veri modeli eşleme tasarımcısında sağlanan bir ER etiketi çevirisini gözden geçirme.](./media/er-multilingual-labels-refer-mapping.png)

> [!NOTE]
> Düzenlenebilir ER bileşenine girilmiş olan etiketi silmek için tasarımcıları kullanamazsınız.

## <a name="scope"></a>Kapsam

ER etiketlerine, ER bileşenlerinin birçok çevrilebilir özniteliğinden başvuruda bulunulabilir.

### <a name="data-model-component"></a>Veri modeli bileşeni

Bir ER veri modeli yapılandırdığınızda, bunun için ER etiketleri ekleyebilirsiniz. Model öğesinin **Etiket** ve **Açıklama** öznitelikleri, her modelin alanı ve her <a id="LinkModelEnum"></a> model numaralandırma değeri ER veri modeline eklenen bir ER etiketine bağlanabilir.

![ER veri modeli tasarımcısında Açıklama özniteliği için çeviri sağlama.](./media/er-multilingual-labels-refer.png)

Bir ER veri modeli bu şekilde yapılandırıldığında, içeriği ER veri modeli tasarımcısı kullanıcılarına her kullanıcının tercih edilen dilinde sunulur. Bu nedenle, model bakımı basitleştirilmiştir. Aşağıdaki resimler, bu işlevin tercih edilen dili DE-AT ve JA olarak ayarlanmış kullanıcılar için nasıl çalıştığını gösterir.

![Tercih edilen dili DE-AT olarak ayarlanmış bir kullanıcı için ER veri modeli tasarımcısı düzeni.](./media/er-multilingual-labels-refer-de.png)

![Tercih edilen dili JA olarak ayarlanmış bir kullanıcı için ER veri modeli tasarımcısı düzeni.](./media/er-multilingual-labels-refer-ja.png)

### <a name="model-mapping-component"></a>Model eşleme bileşeni

ER model eşlemesi bir ER veri modelini temel aldığından, başvurulan veri modeli öğelerinin etiketleri model eşleme tasarımcısında kullanıcının tercih ettiği dilde görüntülenir. Aşağıdaki şekil, yapılandırılan veri modeline eklenmiş olan **Açıklama** özniteliğinin etiketi kullanılarak, düzenlenebilir model eşlemesinde **PurchaseOrder** alanı anlamının nasıl açıklandığını gösterir. Bu etiketin kullanıcının tercih ettiği dilde (bu örnekte DE-AT) sunulduğuna dikkat edin.

![Tercih edilen dili DE-AT olarak ayarlanmış bir kullanıcı için ER model eşleme tasarımcısı düzeni.](./media/er-multilingual-labels-show-mapping.png)

**Kullanıcı giriş parametresi** veri kaynağının **Etiket** özniteliği bir ER etiketine bağlı olarak yapılandırıldığında, bu veri kaynağına karşılık gelen parametre alanı çalışma zamanında kullanıcı iletişim kutusunda kullanıcıların tercih ettikleri dilde sunulur.

### <a name="format-component"></a>Biçim bileşeni

Bir ER biçimi yapılandırdığınızda, bunun için ER etiketleri ekleyebilirsiniz. Her yapılandırılmış veri kaynağının **Etiket** ve **Yardım metni** öznitelikleri, ER biçimine eklenen bir ER etiketine bağlanabilir. Her <a id="LinkFormatEnum"></a>biçimi numaralandırma değerinin **Etiket** ve **Açıklama** öznitelikleri de düzenlenebilir ER biçiminden erişilebilen bir ER etiketine bağlanabilir.

> [!NOTE]
> Bu öznitelikleri, bu ER veri modeli için yapılandırılmış olan her ER biçiminde model etiketlerini yeniden kullanan üst ER veri modelinin bir ER etiketine da bağlayabilirsiniz.

Bir ER biçimi bu şekilde yapılandırıldığında, biçimin içeriği ER İşlemi tasarımcısı kullanıcılarına her kullanıcının tercih edilen dilinde sunulur. Bu nedenle, yapılandırılan mantığın biçim bakımı ve analizi basitleştirilmiştir.

ER biçimi bir ER veri modelini temel aldığından, veri modeli öğelerinde başvurulan etiketler ER biçim tasarımcısında kullanıcının tercih ettiği dilde görüntülenir.

**Kullanıcı giriş parametresi** veri kaynağının **Etiket** özniteliği bir ER etiketine bağlı olarak yapılandırıldığında, çalışma zamanında parametreye karşılık gelen alan kullanıcıya bir istem olarak sunulur. Aşağıdaki resimlerde, tasarım zamanında **Kullanıcı giriş parametresi** veri kaynağının **Etiket** özniteliğini bir ER etiketine nasıl bağlayabileceğinizi ve bu şekilde çalışma zamanında kullanıcılardan parametre için tercih edilen farklı dillerde nasıl istemde bulunulabildiği (İngilizde Amerika Birleşik Devletleri (EN-US) ve DE-AT dilleri için gösterilmiştir).

![ER İşlemi tasarımcısında bir kullanıcı giriş parametresi özniteliklerinin çevirisini sağlama.](./media/er-multilingual-labels-refer-format.png)

![EN-US kullanıcı dili tercih edildiğinde çalışma zamanında ER Satıcı ödemesi işlemesi.](./media/er-multilingual-labels-show-runtime-en.png)

![DE-AT kullanıcı dili tercih edildiğinde çalışma zamanında ER Satıcı ödemesi işlemesi.](./media/er-multilingual-labels-show-runtime-de.png)

### <a name="expressions"></a>İfadeler

ER [ifadesinde](er-formula-language.md) bir etiket kullanmak için **@"GER\_LABEL:X"** sözdizimini kullanmanız gerekir; burada **@** öneki işlenenin etikete nasıl başvuruda bulunduğunu,  **GER\_LABEL** bir ER etiketinin bulunduğunu ve  **X** ER etiketinin kodunu belirtir.

![ER formül tasarımcısında bir ER etiketine başvuru içeren bir ER ifadesi yapılandırma.](./media/er-multilingual-labels-expression1.png)

Bir sistem (uygulama) etiketine başvurmak için, **@"X"** söz dizimini kullanın; burada **@** işlenenin bir etikete başvuruda bulunduğunu ve **X** sistem etiketi kodunu belirtir.

![ER formül tasarımcısında bir uygulamaya başvuru içeren bir ER ifadesi yapılandırma.](./media/er-multilingual-labels-expression2.png)

#### <a name="model-mapping"></a>Model eşleme

ER model eşlemesindeki ifade etiket kullanılarak yapılandırılabilir. Bu eşleme giden belge oluşturmak için çalıştırılan bir ER biçimi tarafından çağrıldığında, yürütme bağlamı bir dil kodu içerir. Yapılandırılan bir ifade etiketi, söz konusu bağlamın dili için yapılandırılmış olan etiket metniyle doldurulur.

Başvurulan bir etikette, model eşlemesini çağıran biçim yürütme bağlamının diline ait bir çeviri yoksa, bunun yerine EN-US dilindeki etiket metni kullanılır.

#### <a name="format"></a>Biçim

ER biçimindeki ER ifadesi etiketler kullanılarak yapılandırılabilir. Bu biçim giden belge oluşturmak için çalıştırıldığında, yürütme bağlamı bir dil kodu içerir. Yapılandırılan bir ifade etiketi, söz konusu bağlamın dili için yapılandırılmış olan etiket metniyle doldurulur.

![ER formül tasarımcısında düzenlenebilir ER ifadesinin ER etiketi için çeviri sağlama.](./media/er-multilingual-labels-refer-in-expression.png)

![ER İşlem tasarımcısında bir ER etiketine başvuran veri bağlaması örneği.](./media/er-multilingual-labels-refer-in-binding.png)

Raporu kullanıcının tercih ettiği dilde oluşturmak için, bir ER biçiminin **DOSYA** bileşenini yapılandırabilirsiniz.

![Raporu kullanıcının tercih ettiği dilde oluşturmak için ER İşlem tasarımcısında DOSYA bileşenini ayarlama.](./media/er-multilingual-labels-language-context-user.png)

Bir ER biçimi bu şekilde yapılandırırsanız, rapor ER etiketlerinin ilgili metni kullanılarak oluşturulur. Aşağıdaki resimlerde, EN-US ve DE-AT kullanıcı dilleri için rapor örnekleri gösterilmektedir.

![Tercih edilen EN-US kullanıcı dilinde oluşturulan raporu önizleme.](./media/er-multilingual-labels-report-preview-en.png)

![Tercih edilen DE-AT kullanıcı dilinde oluşturulan raporu önizleme.](./media/er-multilingual-labels-report-preview-de.png)

Başvurulan bir etikette, biçim yürütme bağlamının diline ait bir çeviri yoksa, bunun yerine EN-US dilindeki etiket metni kullanılır.

## <a name="language"></a>Dil

ER, oluşturulan bir rapor için dil belirtmek üzere farklı yöntemleri destekler. **Biçim** sekmesindeki **Dil tercihleri** alanında aşağıdaki değerleri seçebilirsiniz:

- **Şirket tercihi**: Şirket tarafından belirtilen dilde rapor oluşturun.

    ![ER İşlem tasarımcısında oluşturulan raporun dili olarak şirket tarafından tercih edilen bir dil belirtin.](./media/er-multilingual-labels-language-context-company.png)

- **Kullanıcı tercihi**: Kullanıcının tercih ettiği dilde rapor oluşturun.
- **Açıkça tanımlanmış**: Tasarım zamanında belirtilen bir dilde rapor oluşturun.

    ![ER İşlem tasarımcısında oluşturulan raporun dili olarak tasarım sırasında tanımlanan bir dil belirtin.](./media/er-multilingual-labels-language-context-fixed.png)

- **Çalışma zamanında tanımlanmış**: Çalışma zamanında belirtilen bir dilde rapor oluşturun. Bu değeri seçerseniz, **Dil** alanında, dil (ör. ilgili müşterinin dili) için dil kodunu döndüren bir ER ifadesi yapılandırın.

    ![ER İşlem tasarımcısında oluşturulan raporun dili olarak çalışma zamanında tanımlanan bir dil belirtin.](./media/er-multilingual-labels-language-context-runtime.png)

## <a name="culture-specific-formatting"></a>Kültüre özel biçimlendirme

ER, oluşturulan bir rapor için kültür belirtmek üzere farklı yöntemleri destekler. Bu nedenle tarih, saat ve sayısal değerler için kültüre özgü doğru biçimlendirme kullanılabilir. Bir ER biçimi tasarladığınızda, **Biçim** sekmesinde, **Kültür tercihleri** alanında, **Ortak\\Dosya**, **Excel\\Dosya**, **PDF\\Dosya** veya **PDF \\Birleştirici** türündeki her biçim bileşeni için aşağıdaki değerlerden birini seçebilirsiniz:

- **Kullanıcı tercihi** – Değerleri, kullanıcının tercih ettiği kültüre göre biçimlendirin. Bu kültür, **Kullanıcı seçenekleri** sayfasının **Tercihler** sekmesindeki **Tarih, saat ve sayı biçimi** alanında tanımlanır.

    ![Kullanıcının tercih edilen kültürünü, ER İşlem Tasarımcısı'nda oluşturulan bir raporun kültürü olarak tanımlama.](./media/er-multilingual-labels-culture-context-user-preferred.png)

- **Açıkça tanımlanmış** – Değerleri, tasarım zamanında belirtilen kültüre göre biçimlendirin.

    ![Tasarım zamanında belirtilen kültürü, ER İşlem Tasarımcısı'nda oluşturulan bir raporun kültürü olarak tanımlama.](./media/er-multilingual-labels-culture-context-fixed.png)

- **Çalışma süresinde tanımlanmış** – Değerleri, çalışma zamanında belirtilen kültüre göre biçimlendirin. Bu değeri seçerseniz, **Eşleme** sekmesinde **Tarih, saat ve sayı biçimi** alanında, ilgili müşterinin kültürü gibi kültür için kültür kodu döndüren bir ER ifadesi yapılandırın.

    ![Çalışma zamanında belirtilen kültürü, ER İşlem Tasarımcısı'nda oluşturulan bir raporun kültürü olarak tanımlama.](./media/er-multilingual-labels-culture-context-runtime.png)

> [!NOTE]
> Belirli bir kültürü tanımladığınız bir ER bileşeni, bir metin değerini doldurmak üzere yapılandırılmış alt ER bileşenleri içerebilir. Varsayılan olarak, ana bileşenin kültürü bu bileşenlerin değerlerini biçimlendirmek için kullanılır. Bu bileşenlerin bağlarını yapılandırmak ve değer biçimlendirmesi için alternatif bir kültür uygulamak için aşağıdaki yerleşik ER işlevlerini kullanabilirsiniz:
>
> - [DATEFORMAT](er-functions-datetime-dateformat.md#syntax-2)
> - [DATETIMEFORMAT](er-functions-datetime-datetimeformat.md#syntax-2)
> - [NUMBERFORMAT](er-functions-text-numberformat.md#syntax-2)
>
> Sürüm 10.0.20 ve sonrasında, **Ortak\\Dosya** ve **Excel\\Dosya** türlerinin biçim bileşenlerinin yerel ayarları, oluşturulan bir belgenin [PDF dönüştürmesinde](electronic-reporting-destinations.md#OutputConversionToPDF) değerleri biçimlendirmek için kullanılır.

## <a name="translation"></a>Çeviri

Düzenlenebilir bir ER bileşenine gerekli ER etiketlerini ekleyebilirsiniz. Bir ER etiketi eklendiğinde, iki şekilde çevrilebilir: el ile ve otomatik olarak.

### <a name="manual-translation"></a>El ile çeviri

**Metin çevirisi** [bölmesine](#TextTranslationPane) bir ER etiketi eklediğinizde, bunu geçerli Finance kurulumunda desteklenen tüm dillere el ile çevirebilirsiniz. **Sistem dili** veya **Kullanıcı dili** bölümündeki **Dil** alanında tercih edilen dili seçebilir, uygun metni karşılık gelen **Çevrilmiş metin** alanına girebilir ve **Çevir**'i seçebilirsiniz. Bu işlemin, her gerekli dil ve eklediğiniz her etiket için yinelenmesi gerekir.

### <a name="automatic-translation"></a>Otomatik çeviri

ER bileşeni yapılandırması, düzenlenebilir ER bileşeninin içinde bulunduğu ER yapılandırmasının taslak sürümünde yapılır.

![Taslak durumundaki yapılandırmanın sürümüne erişim sağlayan ER Yapılandırmaları sayfası.](./media/er-multilingual-labels-configurations.png)

Bu konuda daha önce de anlatıldığı gibi, gerekli ER etiketlerini düzenlenebilir bir ER bileşenine ekleyebilirsiniz. Bu şekilde, EN-US dilindeki ER etiketlerinin metnini belirtebilirsiniz. Daha sonra, yerleşik ER işlevini kullanarak ER bileşeninin etiketlerini dışa aktarabilirsiniz. Düzenlenebilir ER bileşenini içeren bir ER yapılandırmasının taslak sürümünü seçin ve sonra da **Exchange \>Etiketleri dışa aktar**'ı seçin.

![Seçili yapılandırma sürümünden ER etiketlerini dışa aktarmaya olanak tanıyan ER Yapılandırmaları sayfası.](./media/er-multilingual-labels-export.png)

Tüm etiketleri veya dışa aktarmanın başında belirttiğiniz tek bir dilin etiketlerini dışa aktarabilirsiniz. Etiketler, XML dosyaları içeren bir zip dosyası olarak dışa aktarılır. Her XML dosyası tek bir dil için etiketler içerir.

![DE-AT dili için ER etiketlerini içeren dışa aktarılmış dosya örneği.](./media/er-multilingual-labels-in-xml.png)

Bu biçim, etiketlerin [Dynamics 365 Translation Service](../lifecycle-services/translation-service-overview.md) gibi harici çeviri hizmetleri tarafından otomatik olarak çevrilmesi için kullanılır. Çevrilen etiketleri aldığınızda bunları, bu etiketlere sahip olan ER bileşenlerini içeren ER yapılandırmasının taslak sürümüne geri aktarabilirsiniz. Düzenlenebilir ER bileşenini içeren bir ER yapılandırmasının taslak sürümünü seçin ve **Exchange \>Etiketleri yükle**'yi seçin.

![Seçili yapılandırma sürümüne ER etiketlerini aktarmaya olanak tanıyan ER Yapılandırmaları sayfası.](./media/er-multilingual-labels-load.png)

Çevrilmiş etiketler seçili ER yapılandırmasına aktarılır. ER yapılandırmasında bulunan çevrilmiş etiketler değiştirilir. ER yapılandırmasında herhangi bir çevrilmiş etiket eksikse, eklenir.

## <a name="lifecycle"></a>Yaşam döngüsü

Düzenlenebilir ER bileşeni etiketleri, bileşenin diğer içeriğiyle birlikte, ER yapılandırmasının uygun sürümünde korunur.

Temel bir ER bileşeninin etiketlerine, yaptığınız değişiklikleri tanıtmak için oluşturduğunuz ER bileşeninin türetilmiş bir sürümünde başvuruda bulunulabilir.

ER sürüm oluşturma işlemi, ER bileşenindeki herhangi bir özniteliğe etiket atamayı denetler. Etiket atamasında yapılan değişiklikler, sağlanan ER bileşeninin türetilmiş bir sürümü olarak oluşturulmuş düzenlenebilir ER bileşeninin değişiklik listesine (delta) kaydedilir. Bu değişiklikler, türetilmiş sürüm yeni bir temel sürüm için yeniden temel alındığında doğrulanacaktır.

## <a name="functions"></a>İşlevler

Yerleşik [LISTOFFIELDS](er-functions-list-listoffields.md) ER işlevi, ER bileşenlerinin bazı öğeleri için yapılandırılmış olan ER etiketlerine erişebilir.

Bu konuda daha önce de anlatıldığı gibi, her [modelin](#LinkModelEnum) **Etiket** ve **Açıklama** öznitelikleri veya [biçim](#LinkFormatEnum) ER numaralandırması değeri, uygun ER bileşeninde erişilebilir olan ER etiketine bağlanabilir. ER numaralandırmasını bağımsız değişken olarak kullanarak **LISTOFFIELDS** işlevini çağırdığınız bir ER ifadesi yapılandırabilirsiniz. Bu ifade, bu işlevin bağımsız değişkeni olarak tanımlanan bir ER numaralandırmasının her değeri için kayıt içeren bir liste döndürür. Her kayıt, bir ER numaralandırması değerine bağlantılı olanbir ER etiketi değerini içerir:

- **Etiket** özniteliklerini bağlantılı ER etiketinin değeri, döndürülen kaydın **Etiket** alanında saklanır.
- **Açıklama** özniteliklerini bağlantılı ER etiketinin değeri, döndürülen kaydın **Açıklama** alanında saklanır.

## <a name="performance"></a><a name=performance></a>Performans

Tercih ettiğiniz [dilde](#language) rapor oluşturmak için veya içeriğin tercih ettiğiniz dile göre ayrıştırıldığı gelen belgeyi içeri aktarmak için bir ER biçimi bileşenini yapılandırdığınızda [Özellik yönetimi](../../fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında **ER çalıştırıldığında geçerli kullanıcının tercih ettiği dili önbelleğe al** özelliğini etkinleştirmenizi öneririz. Bu özellik, özellikle ER formülleri ve bağlamalarındaki etiketlere birden çok başvuru ve tercih ettiğiniz dilde kullanıcı iletileri oluşturmak için birçok [doğrulama](general-electronic-reporting-formula-designer.md#TestFormula) kuralı içeren ER biçimi bileşenleri için performansı artırmaya yardımcı olur.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Elektronik Raporlama işlevleri](er-formula-language.md#Functions)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
