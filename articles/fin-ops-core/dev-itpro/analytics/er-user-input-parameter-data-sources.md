---
title: Bir raporun parametrelerini belirtmek için KULLANICI GİRİŞİ PARAMETRESİ veri kaynaklarını kullanma
description: Bu makalede, oluşturduğunuz raporların parametrelerini belirtmek için KULLANICI GİRİŞİ PARAMETRESİ veri kaynaklarının nasıl kullanılacağı açıklanmaktadır.
author: NickSelin
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.openlocfilehash: 62b7a8173416a1d36a2985823d186a7a0e6a7e60
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872986"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Bir raporun parametrelerini belirtmek için KULLANICI GİRİŞİ PARAMETRESİ veri kaynaklarını kullanma

[!include[banner](../includes/banner.md)]

[Elektronik raporlama](general-electronic-reporting.md) (ER) [model eşlemesi](er-overview-components.md#model-mapping-component) ve ER [biçimi](er-overview-components.md#format-component) bileşenlerini tasarladığınızda, herhangi bir ER biçimini yürütme işlemi başlamadan önce çalışma zamanında iletişim kutusundaki veri girişi alanlarında belirtilebilecek gerekli değerleri almak için *KULLANICI GİRİŞİ PARAMETRESİ* türünde veri kaynakları kullanabilirsiniz. Bu makalede, şu anda desteklenen *KULLANICI GİRİŞİ PARAMETRESİ* veri kaynakları açıklanmaktadır.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Zorunlu özellikler

Her *KULLANICI GİRİŞİ PARAMETRESİ* türündeki veri kaynakları için aşağıdaki özellikleri belirtmeniz gerekir:

- **Ad** alanında, veri kaynağının dahili adını girin. Bu adı, diğer [ifadelerde](er-formula-language.md) ve yapılandırılan model eşleme veya biçim bileşeninin bağlamalarında kullanabilirsiniz.

## <a name="optional-properties"></a><a name="optional-properties"></a>İsteğe bağlı özellikler

*KULLANICI GİRİŞİ PARAMETRESİ* türündeki veri kaynakları için isteğe bağlı olarak aşağıdaki özellikleri belirtebilirsiniz:

- **Etiket** alanında, çalışma zamanında iletişim kutusunda ilgili veri girişi alanı için kullanılan etiketi belirtin. **Etiket** alanını etkinleştirip **Çevir**'i seçerek farklı dil kodları için farklı etiket metni ekleyebilirsiniz.
- **Yardım** alanında, *KULLANICI GİRİŞİ PARAMETRESİ* türündeki düzenlenebilir bir veri kaynağı seçildiğinde tasarım zamanında **Biçim tasarımcısı** sayfasının veya **Model eşleme tasarımcısı** sayfasının alt kısmında gösterilecek yardım metnini belirtin. Bu metin, düzenlenebilir biçim veya model eşleme bileşenini yapılandırırken kullanıcılara yardımcı olmak için veri kaynağıyla ilgili ek ayrıntılar sağlayabilir. **Çevir**'i seçerek, farklı dil kodları için farklı yardım metinleri ekleyebilirsiniz.

    > [!NOTE]
    > [Dile özgü etiketler ve metin](er-design-multilingual-reports.md#format-component) eklemek için kullanabileceğiniz **Çevir** düğmesi, yalnızca veri kaynağını ekledikten, değişikliklerinizi kaydettikten ve veri kaynağını düzenlemek üzere yeniden açtıktan sonra kullanılabilir hale gelir.

- **Salt okunur** alanında, *[Boole](er-formula-supported-data-types-primitive.md#boolean)* değeri döndüren bir ifade yapılandırın.

    - Yapılandırılmış ifade çalışma zamanında **Doğru** değerini döndürürse, iletişim kutusunda ilgili veri girişi alanı soluk görünür ve bu alanın değerini değiştiremezsiniz.
    - Yapılandırılmış ifade çalışma zamanında **Yanlış** değerini döndürürse veya yapılandırılmış ifade yoksa, iletişim kutusunda ilgili veri girişi alanı kullanılabilir ve bu alanın değerini değiştirebilirsiniz.

- **Varsayılan değer** alanında, başvurulan parametre türünün değerini döndüren bir ifade yapılandırın. Bu değer, çalışma zamanında iletişim kutusundaki ilgili veri girişi alanı için varsayılan değeri doldurmak amacıyla kullanılabilir.

    Bir ER biçimi çalıştırdığınızda, çalışma zamanında iletişim kutusundaki ilgili veri girişi alanına girdiğiniz değer, bellekte önceden kullanılmış olan değer olarak kaydedilir. Önceden kullanılan değerler; her alan, ER biçimi, geçerli kullanıcı ve geçerli kuruluş (şirket) için ayrı ayrı kaydedilir.

    - Daha önce kullanılan değerden bağımsız olarak, **Varsayılan değer** ifadesi tarafından döndürülen değerin her zaman varsayılan değer olarak kullanılması gerekiyorsa **Her zaman varsayılan değere sıfırla** seçeneğini **Evet** olarak ayarlayın.
    - **Varsayılan değer** ifadesi tarafından döndürülen değerin, yalnızca daha önce kullanılan değerin olmadığı durumlarda varsayılan değer olarak kullanılması gerekiyorsa **Her zaman varsayılan değere sıfırla** seçeneğini **Hayır** olarak ayarlayın.

    > [!NOTE]
    > **Her zaman varsayılan değere sıfırla** seçeneğini **Evet** olarak ayarlarsanız, **Varsayılan değer** alanında bir ifade yapılandırılması gerekir.

- **Çoklu seçime izin ver** seçeneğini **Evet** olarak ayarlarsanız, çalışma zamanında yapılandırılan parametre için birden çok değer seçebilirsiniz. **Hayır** olarak ayarlarsanız, yalnızca tek bir değer seçebilirsiniz.

    > [!NOTE]
    > Bu seçenek tüm *KULLANICI GİRİŞİ PARAMETRESİ* türleri için geçerli değildir. Tasarım zamanında, yapılandırılan kullanıcı girişi parametresinin çoklu seçime izin vermediğini ve yalnızca tek bir değerin seçilebileceğini veya girilebileceğini kullanıcıya bildirmek için bir özel durum oluşturulur.
    >
    > **Çoklu seçime izin ver** seçeneğini **Evet** olarak ayarlar ve **Varsayılan değer** alanında bir ifade belirtirseniz, bu ifade yalnızca tek bir varsayılan değer ayarlamak için kullanılabilir.

- Yapılandırılan parametrenin çalışma zamanında iletişim kutusunda gösterilip gösterilmeyeceğini belirlemek için **Görünürlüğü düzenle**'yi seçin.

    > [!NOTE]
    > *KULLANICI GİRİŞİ PARAMETRESİ* türündeki veri kaynaklarının varsayılan görünürlüğü bulundukları ER bileşenine bağlıdır.
    >
    > - Bir veri kaynağı biçim bileşeninde yapılandırılırsa, varsayılan olarak görünür olur.
    > - Bir veri kaynağı, model eşleme bileşeninde yapılandırılırsa yalnızca ER bileşeni çalıştırıldığında veri kaynağının değeri sonucu etkiliyorsa görünür. Örneğin, bir veri kaynağı eklediniz ancak bunu geçerli model eşleme bileşeninin ifadelerinde ve bağlamalarında kullanmadınız. Bu durumda, varsayılan olarak, ilgili veri girişi alanı çalışma zamanında iletişim kutusunda gösterilmez. 

    **Formül tasarımcısı** sayfasındaki **Formül** alanında, bir *Boole* değeri döndüren bir ifade yapılandırın.

    - Yapılandırılmış ifade çalışma zamanında **Doğru** değerini döndürürse veya yapılandırılmış ifade yoksa, ilgili veri girişi alanı çalışma zamanında iletişim kutusunda görünür.
    - Yapılandırılan ifade **Yanlış** değerini döndürürse, ilgili veri girişi alanı çalışma zamanında iletişim kutusunda gizlenir. Çalışma zamanında diğer ifadeler tarafından çağrıldığında, diğer ayarlara bağlı olarak varsayılan değeri, daha önce kullanılan değeri veya geçerli veri türü değeri için varsayılanı döndürür.

## <a name="type-specific-properties"></a>Türe özgü özellikler

### <a name="application-dependent-user-input-parameter"></a>Uygulamaya bağımlı kullanıcı giriş parametresi

Microsoft Dynamics 365 Finance uygulamasının geçerli örneği için belirtilen veri türündeki gerekli değeri veya değerleri almak için **Genel** \> **Kullanıcı girişi parametresi** veri kaynağını kullanın. Bir ER bileşenine bu türde bir veri kaynağı eklediğinizde, aşağıdaki özellikleri belirtin:

- **Operations veri türü adı (EDT, numaralandırma)** alanında, uygulama [genişletilmiş veri türü (EDT)](../extensibility/extensible-edts.md) veya uygulama numaralandırması seçin.

> [!NOTE]
> Bu *KULLANICI GİRİŞ PARAMETRESİ* türündeki düzenlenebilir bir veri kaynağında **Operations veri türü adı (EDT, numaralandırma)** başvurusunu değiştirdiğinizde **Salt okunur** ve **Varsayılan değer** alanlarında yapılandırılan ifadeleri incelemenizi öneririz.

Aşağıdaki çizimde, **Instat XML (DE)** ER biçim yapılandırmasında yapılandırılan `$TaxRegNum` veri kaynağının özellikleri gösterilmektedir. Bu veri kaynağı, çalışma zamanında iletişim kutusunda **Vergi kayıt numarası** veri girişi alanını sunmak için *Açıklama* EDT'sini kullanacak şekilde yapılandırılmıştır.

![Biçim tasarımcısı sayfasındaki iletişim kutusunda KULLANICI GİRİŞ PARAMETRESİ türündeki veri kaynağının özellikleri.](./media/er-user-input-parameter-data-sources-01.png)

Aşağıdaki çizimde, İnstrastat beyanı [oluşturmak](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) için **Instat XML (DE)** ER biçimi yapılandırması çalıştırıldığında çalışma zamanında gösterilen iletişim kutusu gösterilir. Yapılandırılan **Vergi kayıt numarası** alanının veri girişi için kullanılabilir olmasına dikkat edin.

![İntrastat sayfasında çalışan ER biçiminin İntrastat raporu iletişim kutusu.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a> veri modeli numaralandırma kullanıcı girişi parametresi

Tek bir veri modeli [numaralandırmasının](er-formula-supported-data-types-primitive.md#enumeration) gerekli değerini veya değerlerini elde etmek için **Veri modeli** \> **Numaralandırma kullanıcı girişi parametresi** veri kaynağını kullanın. Bir ER bileşenine bu türde bir veri kaynağı eklediğinizde, aşağıdaki özellikleri belirtin:

- **Model** alanında, temel veri modeli için bir başvuru belirtin.
- **Model numaralandırma** alanında, başvurulan veri modeli numaralandırmasına bir başvuru belirtin.
- **Sürüm** alanında, başvurulan model numaralandırmasını içeren ER veri modeli bileşeninin düzeltme numarasını seçin.

    > [!TIP]
    > Tasarım zamanında, ilgili ER veri modeli yapılandırmasının taslak sürümünde bulunan başvurulan veri modeli bileşeninin numaralandırmalar listesine erişmek için **Sürüm** alanını boş bırakabilirsiniz. Bu şekilde, model eşleme veya biçim bileşeninin taslak sürümünü ve temel veri modeli bileşeninin taslak sürümünü eşzamanlı olarak düzenleyebilirsiniz.
    >
    > Ancak, **Sürüm** alanının yalnızca model eşleme veya biçim bileşeninin taslak sürümünde boş bırakılabileceğini unutmayın. Bir ER model eşleme veya biçim yapılandırmasının durumunu **Taslak** yerine **Tamamlandı** olarak değiştirdiğinizde, bu alan, geçerli Finance örneğindeki mevcut en yüksek model düzeltme numarasıyla otomatik olarak doldurulur. Temel veri modelinizin taslak sürümünde yeni bir numaralandırma veya yeni bir numaralandırma değeri kullanır ve düzenlenebilir model eşleme veya biçim bileşeninde buna atıfta bulunursanız, ER model eşleme veya biçim yapılandırmanızın taslak sürümü tamamlanmadan önce temel veri modeli yapılandırmasının taslak sürümünü tamamlayın. Aksi takdirde, model eşleme veya biçim yapılandırmasının durumu **Taslak** yerine **Tamamlandı** olarak değiştiğinde, "Yol bulunamadı" özel durumu oluşturulur. İletide, temel veri modelinde başvurulan numaralandırma veya numaralandırma değerinin eksik olduğu bildirilir.

Aşağıdaki çizimde, **Instat XML (DE) Contoso** ER biçim yapılandırmasında yapılandırılan `$ReportDirection` veri kaynağının özellikleri gösterilmektedir. **Instat XML (DE) Contoso** yapılandırması, **Instat XML (DE)** yapılandırmasından [türetilmiştir](general-electronic-reporting.md#Configuration). Bu veri kaynağı, çalışma zamanında iletişim kutusunda uygun arama alanını sunmak için *ReportDirection* model numaralandırmasını kullanacak şekilde yapılandırılmıştır.

![Biçim tasarımcısı sayfasındaki iletişim kutusunda KULLANICI GİRİŞ PARAMETRESİ türündeki veri kaynağının özellikleri.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a> biçim numaralandırma kullanıcı girişi parametresi

Tek bir veri modeli numaralandırmasının gerekli değerini veya değerlerini elde etmek için **Biçim numaralandırma** \> **Numaralandırma kullanıcı girişi parametresi** türündeki veri kaynağını kullanın. Bir ER bileşenine bu türde bir veri kaynağı eklediğinizde, aşağıdaki özellikleri belirtin:

- **Biçim numaralandırma** alanında, düzenlenebilir biçim için bir numaralandırma belirtin.

> [!NOTE]
> Bu türdeki veri kaynakları yalnızca düzenlenebilir biçim bileşeni kapsamında yapılandırılabilir.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Kaynak kodundan USER INPUT PARAMETER türünün veri kaynağı değerlerini başlatma](er-initiate-uip-data-source-value-from-source-code.md)
