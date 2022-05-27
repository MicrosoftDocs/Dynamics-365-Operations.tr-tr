---
title: Elektronik raporlama formülleri için desteklenen bileşik veri türleri
description: Bu konu, elektronik raporlama (ER) formüllerinde desteklenen bileşik veri türleri hakkında bilgi sağlar.
author: NickSelin
ms.date: 06/02/2021
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 933c8211276c1335a6a81bf4a8cb1c3f270762d4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689256"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Elektronik raporlama formülleri için desteklenen bileşik veri türleri

[!include [banner](../includes/banner.md)]

Bu konu, [elektronik raporlama (ER)](general-electronic-reporting.md) ifadelerinde desteklenen bileşik veri türleri hakkında bilgi sağlar. Bileşik veri türleri: [sınıf](#class), [konteyner](#container), [kayıt](#record), [kayıt listesi](#record-list) ve [nesne](#object).

## <a name="class"></a><a name="class"></a>Sınıf

*sınıf* veri türü, ortak uygulama sınıfına başvurur. ER'de, başvurulan sınıfın her genel yöntemi için ayrı bir alan içeren [*kayıt*](#record) olarak temsil edilir. Yöntem çağrısı parametreleştirilirken, yöntemi çağırmak üzere yapılandırılmış bir ER ifadesinde uygun türlerin gerekli bağımsız değişkenlerini de belirtmeniz gerekir.

ER eşleme ve biçim bileşenlerinde, veri kaynağı olarak sunulan ve *sınıf* türünün bir değerini döndüren **Sınıf** veri kaynağını ekleyebilirsiniz. Bu veri kaynağı, çalışma zamanında çağrılabilecek sınıfın ortak yöntemlerini gösterir.

> [!NOTE]
> Yalnızca bir değer döndüren yöntemler ER ifadelerinden çağrılabilir.
>
> Yalnızca sıfır ile sekiz arasında bağımsız değişken içeren yöntemler ER ifadelerinden çağrılabilir.

Bir *sınıf* ın varsayılan değeri **null**'dur.

Aşağıdaki görsel, **xInfo** uygulama sınıfının örneğini oluşturmak ve mevcut uygulamanın adını almak için **productName()** yöntemini çağırmak için **Sınıf** türünün **Sistem bilgisi(xInfo)** veri kaynağının nasıl eklendiğini gösterir. Geçerli uygulamanın adı, ER veri modelinin **Yazılım adı (SoftwareName)** alanı için yapılandırılan `xInfo.productName` bağlamasının yürütülmesiyle çalışma zamanında alınır. Bu bağlama, geçerli model eşlemede **Sistem bilgisi(xInfo)** veri kaynağı olarak temsil edilen **xInfo** uygulama sınıfının `productName()` yöntemini çağırır.

[![Model eşleme tasarımcıda Sınıf veri kaynağını yapılandırma.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

Aşağıdaki görsel, ER biçiminin oluşturulan belgelere sağlanan uygulama adını koymak için nasıl yapılandırıldığını göstermektedir. Kullanılan veri modelinin **Yazılım adı(SoftwareName)** alanı, ER biçiminin **softwareUsed** XML öğesi altında yuvalanmış olan **Dize** bileşenine bağlıydı. Bu nedenle, geçerli uygulamanın adı çalışma zamanında XML biçiminde oluşturulan belgenin **sofwareUsed** XML öğesine yerleştirilir.

[![ER biçim tasarımcısında elektronik giden belgenin yapısını yapılandırma.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Konteyner

*konteyner* veri türü ikili içerik taşır. Bir *konteyner* değeri, belirli bilgileri depodan oluşturulan bir belgeye taşımak için kullanılabilir. ER çerçevesinde bu veri türü, oluşturulan belgelere şirket logosu gibi ortam içerikleri yerleştirmek için sıkça kullanılır.

> [!NOTE]
> Her bir ortam öğesi bir *konteyner* değeri olarak temsil edilebilir ancak her *konteyner* değeri bir ortam öğesini temsil etmez. Bu nedenle, bir ER biçimini oluşturulmuş belgelere resim koymak için bir *konteyner* kullanacak şekilde yapılandırırsanız ancak başvurulan *konteyner* ortam içeriği döndürmezse, aşağıdaki örneğe benzer bir özel durum oluşturulabilir: "Kod yürütülürken hata oluştu: İkili (nesne), yöntem constructFromContainer geçersiz parametrelerle çağrıldı."

Bir *konteyner* in varsayılan değeri **null**'dur.

Aşağıdaki görsel, *Konteyner* türünün **Bitmap(Image)** alanının, **Konteyner** türünün **Satış faturası** model eşlemesinde **Logo** veri modeli alanına nasıl bağlı olduğunu gösterir. Bu bağlama, şirket logosunun, **SalesInvoice** kök tanımı için tasarlanan ve çalışma süresinde bu model eşlemesini kullanan bir ER biçimi için kullanılabilir olmasını sağlar.

[![ER model eşleme tasarımcısında Konteyner türünün bir alanını bağlama.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Kaydet

*Kayıt*, her biri [temel](er-formula-supported-data-types-primitive.md) bir veri türü veya bileşik veri türü değeriyle ilişkilendirilmiş adlandırılmış alanlar topluluğudur. Genellikle *kayıt*, tek bir kayıt listesi kaydını temsil etmek için kullanılır. Bu durumda, her öğe ayrı alanları, yöntemleri ve ilişkileri temsil eder.

Bir *kayıt*'ın varsayılan değeri **boş**'tur.

> [!NOTE]
> Boş bir *kayıt* taki bir alanın değerini aldığınızda , uygun veri türünün varsayılan değeri döndürülür.

Bir *kayıt*, aşağıdaki işlevler kullanılarak elde edilebilir:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

*Kayıt* değerlerinin dönüşümü hakkında daha fazla bilgi için bkz. [Liste kategorisinde ER işlevlerinin listesi](er-functions-category-list.md).

## <a name="record-list"></a><a name="record-list"></a>Kayıt listesi

*Kayıt listesi,* *kayıt* türü öğelerinin bir listesidir. Genellikle, veritabanı tablosundan getirilen kayıtların listesini temsil etmek için *kayıt listesi* kullanılır.

Varsayılan olarak, *kayıt listesi* kayıtlarına sırayla erişilir. Belirli bir kayda erişmek için [INDEX](er-functions-list-index.md) işlevini kullanabilir ve *tamsayı* dizinini belirtebilirsiniz.

Bir *kayıt listesi*'nin varsayılan değeri **boş**'tur. Bir *kayıt listesi*'nin boş olup olmayacağını değerlendirmek için [ISEMPTY](er-functions-list-isempty.md) işlevini kullanabilirsiniz.

> [!NOTE]
> Bir *kayıt listesi* boşsa, içindeki bir *kayıt* için alan değeri alma girişimleri, çalışma zamanında bir özel durum oluşmasına neden olur. Bu tür çalışma zamanı özel durumlarını nasıl engelleyebileceğinizi öğrenmek için bkz. [Boş liste olgularının dikkate alınması](er-components-inspections.md#i9).

Bir *kayıt listesi*, aşağıdaki işlevler kullanılarak başlatılabilir:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

*Kayıt listesi* değerlerinin dönüşümü hakkında daha fazla bilgi için bkz. [Liste kategorisinde ER işlevlerinin listesi](er-functions-category-list.md). *Kayıt listesi* öğelerini nasıl oluşturacağınızı, bunları uygulama verileriyle doldurmayı ve sonra iş belgeleri oluşturmayı öğrenmek üzere verileri kullanmayı öğrenmek için bkz. [Özel bir rapor yazdırmak için yeni bir ER çözümü tasarlama](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Nesne

Bir *nesne*, bir *sınıf* ın durum bilgisi olan örneğine başvurur. Bir *nesne* genellikle kaynak kodunda başlatılır. Daha sonra bir ER model eşlemesine geçirilir ve yürütme bağlamının ayrıntılarını sağlar.

Bir *nesne* nin varsayılan değeri **null**'dur.

Aşağıdaki görsel, kaynak kodundan oluşturulan bir fatura hakkındaki bilgileri **Proje faturası** model eşlemesine geçirmek için *Nesne* türünün **ReportDataContract** veri kaynağının nasıl eklendiğini gösterir. Örneğin, fatura örneği metni yürütme bağlamının bir parçası olarak geçirilir. Bu metin, ER veri modelinin **Not** alanı için konfigüre edilmiş `ReportDataContract.parmInvoiceInstanceText` bağlamasının yürütülmesiyle çalışma zamanında kaynak kodundan alınır. Bu bağlama, geçerli model eşlemede **ReportDataContract** veri kaynağı olarak temsil edilen **PSAProjInvoiceContract** uygulama sınıfının `parmInvoiceInstanceText()` yöntemini çağırır.

[![Model eşleme tasarımcıda Nesne veri kaynağını yapılandırma.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Yürütme bağlamının ayrıntılarını kaynak koddan çalışan ER çözümüne nasıl geçitireceğinizi öğrenmek için, bkz. [Tasarlanan raporu çağırmak üzere uygulama artefaktları geliştirme](er-quick-start1-new-solution.md#DevelopCustomCode).

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Elektronik raporlamada formül dili](er-formula-language.md)
- [Desteklenen temel veri türleri](er-formula-supported-data-types-primitive.md)
