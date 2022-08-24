---
title: Ülke bağlamına bağımlı ER model eşlemelerini yapılandırma
description: Bu makalede, ER model eşlemelerini kullanımlarını, denetleyen tüzel kişiliğin ülke/bölge bağlamına bağlı olacak şekilde nasıl ayarlayabileceğiniz açıklanmaktadır.
author: kfend
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable
ms.openlocfilehash: 5db0936682e0cc052622658ac14046013bc4fd87
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277771"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Ülke bağlamına bağımlı ER model eşlemelerini yapılandırma

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER model) eşlemelerini Dynamics 365 Finance'e özgü genel bir ER veri modeli uygulayacak şekilde yapılandırabilirsiniz. Bu makalede, bir ER veri modelinin birden çok ER model eşlemesini farklı ülke/bölge bağlamlarına sahip şirketlerde çalıştıran ilgili ER biçimleri tarafından nasıl kullanıldıkları denetlenerek tasarlama açıklanmaktadır.

## <a name="prerequisites"></a>Ön Koşullar

Bu makaledeki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:

- Aşağıdaki rollerden biri için Finance'a erişim:
    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Aşağıdaki rollerden biri için Finance uygulamasıyla aynı kiracıya yönelik sağlanan Regulatory Configuration Services (RCS) örneğine erişim:
    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

Bu makaledeki bazı adımlarda bir ER biçiminin yürütülmesi gerekir. Bazı durumlarda, ER biçiminin yürütülmesi oturum açtığınız şirketin ülke/bölge bağlamından etkilenir. Gereken ülke/bölge bağlamına sahip şirket RCS'de mevcutsa geçerli RCS örneğinde bir ER biçimi çalıştırabilirsiniz. Aksi takdirde, ER veri modelini kullanan ER model eşlemesinin ve ER biçimi yapılandırmalarının tamamlanmış bir sürümünü Finance kurulumunuza yüklemeniz ve ardından bu Finance kurulumunda ER biçimini çalıştırmanız gerekir. RCS'de yer alan yapılandırmaları bir Finance kurulumuna içe aktarma hakkında bilgi için bkz. [Yapılandırmaları RCS'den içe aktarma](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Tek model eşleme durumu

Gereken ER bileşenlerini tasarlamak için bu makalenin [Ek 1](#appendix1) bölümündeki adımları izleyin. Artık **Giriş noktası 1** tanımı için model eşlemeyi içeren **Eşleme (Genel)** model eşleme yapılandırmasına sahipsiniz.

![ER yapılandırmalar sayfası, biçim eşleme konfigürasyonu.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Yapılandırılmış biçimi çalıştırma

1.  **Yapılandırmalar sayfası**'nda **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
2.  **Tamam**'ı seçin.

Web tarayıcısının, yürütülen ER biçimi tarafından oluşturulan metin dosyasını indirmeyi teklif ettiğini unutmayın. Bu biçim **Giriş noktası 1** tanımını kullanmak üzere yapılandırıldığından ve şu anda temel modelde bu tanım için eşlemeyi içeren yalnızca tek bir model eşleme kullanılabilir olduğundan yürütülen ER biçimi, **Eşleme (Genel)** yapılandırmasının **Eşleme (Genel)** model eşlemesini veri kaynağı olarak kullanmıştır. Bu nedenle indirilen dosya **Genel işlev 1** metnini içerir.

## <a name="multiple-shared-model-mappings-case"></a>Birden çok paylaşılan model eşleme durumu

Gereken ER bileşenlerini tasarlamak için bu makalenin [Ek 2](#appendix2) bölümündeki adımları izleyin. Artık her biri **Giriş noktası 1** tanımı için model eşlemeyi içeren **Eşleme (Genel)** ve **Eşleme (Genel) özel** model eşleme yapılandırmalarına sahipsiniz.

![ER yapılandırmalar sayfası, genel özel konfigürasyonu eşleştirme.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Yapılandırılmış biçimi çalıştırma

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşlemeleri öğrenme biçimi**'ni seçin.
2.  **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
3.  **Tamam**'ı seçin.

Seçili ER biçiminin yürütülmesinin başarısız olduğunu unutmayın. **Eşleme (Genel)** ve **Eşleme (Genel) özel** model eşleme yapılandırmalarında **Eşlemeleri öğrenme modeli** ve **Giriş noktası 1** tanımı için birden fazla model eşlemesi olduğunu bildiren bir hata iletisi alırsınız. Bu ileti ayrıca bu yapılandırmalardan birini varsayılan yapılandırma olarak seçmenizi önerir.

![ER yapılandırmalar sayfası hata iletisiyle oluştu.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Varsayılan eşleme yapılandırmasını tanımlama

**Eşleme (Genel) özel** model eşleme yapılandırmasını, bu yapılandırmaya ait eşlemeleri **Eşlemeleri öğrenme biçimi** ER biçimi için veri kaynakları olarak kullanılabilecek şekilde varsayılan yapılandırma olarak tanımlamak için bu adımları izleyin.

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşleme (Genel) özel** öğesini seçin.
2.  Geçerli sayfayı gerektiği şekilde düzenlemeye hazır hale getirmek için **Düzenle**'yi seçin.
3.  **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.
4.  **Kaydet**'i seçin.

![ER yapılandırmalar sayfası, model eşleme kaydırıcısı için varsayılan değer Evet olarak ayarlanır.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Yapılandırılmış biçimi çalıştırma

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşlemeleri öğrenme biçimi**'ni seçin.
2.  **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
3.  **Tamam**'ı seçin.

Seçili ER biçiminin yürütülmesinin başarılı olduğunu unutmayın. Web tarayıcısı, yürütülen ER biçimi tarafından oluşturulan metin dosyasını indirmeyi teklif eder. Bu biçim **Giriş noktası 1** tanımını kullanmak üzere yapılandırıldığından ve **Eşleme (Genel) özel** model eşleme yapılandırması varsayılan yapılandırma olarak seçildiğinden yürütülen ER biçimi, **Eşleme (Genel) özel** yapılandırmasının **Eşleme (Genel) kopya** model eşlemesini veri kaynağı olarak kullanmıştır. Bu nedenle indirilen dosya **Genel işlev 1 özel** metnini içerir.

> [!NOTE]
> Oturum açtığınız şirketi değiştirir ve bu ER biçimini yeniden çalıştırırsanız varsayılan ER model eşleme yapılandırması, şirkete bağımlı kısıtlamalar içermediğinden oluşturulan dosyada aynı içeriği alırsınız.

## <a name="multiple-mixed-model-mappings-case"></a>Birden çok karışık model eşleme durumu

Gereken ER bileşenlerini tasarlamak için bu makalenin [Ek 3](#appendix3) bölümündeki adımları izleyin. Artık **Giriş noktası 1** tanımı için model eşlemeyi içeren **Eşleme (Genel)**, **Eşleme (Genel) özel** ve **Eşleme (FR) model eşleme** yapılandırmalarına sahipsiniz.

**Eşleme (FR)** model eşleme yapılandırması sürüm 1'in yalnızca Fransızca ülke/bölge bağlamına sahip Finance şirketlerinde çalıştırılan **Eşlemeleri öğrenme modeli** modelinin ER biçimleri için geçerli olacak şekilde yapılandırıldığını unutmayın.

![ER yapılandırmalar sayfası, Modem eşleme (FR) yapılandırması.](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Yapılandırılmış biçimi çalıştırma

1.  Şirketi **FRSI** olarak değiştirin.
2.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşlemeleri öğrenme biçimi**'ni seçin.
3.  **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
4.  **Tamam**'ı seçin.

Seçili ER biçiminin yürütülmesinin başarılı olduğunu unutmayın. Web tarayıcısı, yürütülen ER biçimi tarafından oluşturulan metin dosyasını indirmeyi teklif eder. Bu biçim **Giriş noktası 1** tanımını kullanmak üzere yapılandırıldığından ve **Eşleme (Genel) özel** model eşleme yapılandırması varsayılan yapılandırma olarak seçildiğinden yürütülen ER biçimi, **Eşleme (Genel) özel** yapılandırmasının **Eşleme (Genel) kopya** model eşlemesini veri kaynağı olarak kullanmıştır. Bu nedenle indirilen dosya **Genel işlev 1 özel** metnini içerir.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Fransa'ya özgü eşleme yapılandırmasını varsayılan yapılandırma olarak tanımlama

Özel **Eşleme (FR)** model eşleme yapılandırmasını varsayılan yapılandırma olarak tanımlamak için bu adımları izleyin. Bu eşleme, Fransa'ya özgü olduğundan **ISO ülke/bölge kodları** alanında belirtilen **FR** ülke koduna sahip tüm model yapılandırmaları arasında varsayılan yapılandırma olarak kabul edilir.

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşleme (FR)** öğesini seçin.
2.  Geçerli sayfayı gerektiği şekilde düzenlemeye hazır hale getirmek için **Düzenle**'yi seçin.
3.  **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.
4.  **Kaydet**'i seçin.

![ER yapılandırmalar sayfası, Eşleme (FR) yapılandırması, model eşleme kaydırıcısı için varsayılan değer Evet olarak ayarlanır.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Yapılandırılmış biçimi çalıştırma

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşlemeleri öğrenme biçimi**'ni seçin.
2.  **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
3.  **Tamam**'ı seçin.

Seçili ER biçiminin yürütülmesinin başarılı olduğunu unutmayın. Web tarayıcısı, yürütülen ER biçimi tarafından oluşturulan metin dosyasını indirmeyi teklif eder. Bu biçim **Giriş noktası 1** tanımını kullanmak için yapılandırıldığından ve **Eşleme (FR)** model eşleme yapılandırması, varsayılan yapılandırma olarak seçildiğinden yürütülen ER biçimi, **Eşleme (FR)** yapılandırmasının **Eşleme (FR)** model eşlemesini veri kaynağı olarak kullanmıştır. Bu nedenle indirilen dosya **FR işlev 1** metnini içerir.

> [!NOTE]
> Oturum açtığınız şirketi değiştirir ve bu ER biçimini yeniden çalıştırırsanız çıktı, seçili şirketin ülke/bölge bağlamına bağımlı olur.

## <a name="other-model-mapping-cases"></a>Diğer model eşleme durumları

Gördüğünüz gibi, ER biçimini yürütmek üzere bir model eşlemenin seçilmesi aşağıdaki şekilde çalışır:

- ER biçiminin kullandığı model eşleme tanımı (bu makaledeki örneklerde **Giriş noktası 1**) belirtilir.
- Belirtilen tanıma sahip ve yapılandırılan ülke/bölge bağlamı kısıtlamalarını karşılayan bir eşleme içeren tüm eşleme yapılandırmaları, ER biçimini (bu makaledeki örneklerde **Eşleme (Genel)**, **Eşleme (Genel) özel** ve **Eşleme (FR)**) çalıştırmak için kullanılabilir.
- Ülke/bölge bağlamı kısıtlamalarının bulunduğu varsayılan model eşlemeleri seçim yaparken yüksek önceliğe sahiptir (bu makaledeki örneklerde **Eşleme (FR)**).
- Ülke/bölge bağlamı kısıtlamalarının bulunmadığı varsayılan model eşlemeleri seçim yaparken bir sonraki yüksek önceliğe sahiptir (bu makaledeki örneklerde **Eşleme (Genel) özel**).
- Ülke/bölge bağlamı kısıtlamalarının bulunduğu model eşlemeleri, seçim yaparken ülke/bölge bağlamı kısıtlamalarının bulunmadığı bir model eşlemeye göre daha yüksek önceliğe sahiptir.

Aşağıdaki tabloda model eşleme ayarları için tüm olası durumlardaki model eşleme seçimi sonuçları hakkında bilgi sağlanmaktadır:

- Sütun 1, ülke/bölge bağlamı kısıtlamalarının bulunmadığı ilk model eşlemenin (örneğin, paylaşılan **Eşleme (Genel)** eşlemesi) sunulup sunulmadığını ve bunun için **Model eşleme için varsayılan** seçeneğinin **Evet** olarak ayarlanıp ayarlanmadığını gösterir.
- Sütun 2, ülke/bölge bağlamı kısıtlamalarının bulunmadığı ikinci model eşlemenin (örneğin, **Eşleme (Genel) özel** eşlemesi) sunulup sunulmadığını ve bunun için **Model eşleme için varsayılan** seçeneğinin **Evet** olarak ayarlanıp ayarlanmadığını gösterir.
- Sütun 3, ülke/bölge A bağlamı kısıtlamalarının bulunduğu ilk model eşlemenin (örneğin, Fransa'ya özgü **Eşleme (FR)** eşlemesi) sunulup sunulmadığını ve bunun için **Model eşleme için varsayılan** seçeneğinin **Evet** olarak ayarlanıp ayarlanmadığını gösterir.
- Sütun 4, ülke/bölge A bağlamı kısıtlamalarının bulunduğu ikinci model eşlemenin sunulup sunulmadığını ve bunun için **Model eşleme için varsayılan** seçeneğinin **Evet** olarak ayarlanıp ayarlanmadığını gösterir.
- Sütun 5, ER biçiminin ülke/bölge A bağlamına sahip bir şirketin denetimi altında yürütülmesi için seçilen model eşleme sonucunu gösterir.
- Sütun 6, ER biçiminin ülke/bölge B bağlamına sahip bir şirketin denetimi altında yürütülmesi için seçilen model eşleme sonucunu gösterir.

Tabloda artı işareti (+), ER biçimini (Finance veya RCS) çalıştırmak için kullanılan Microsoft Azure hizmetinin mevcut kurulumunda model eşleme yapılandırmasının varlığını gösterir.

| Sandık | Ülke/bölge bağlamı olmayan model eşleme 1 (MM1) | Ülke/bölge bağlamı olmayan model eşleme 2 (MM2) | Ülke/bölge A bağlamı olan model eşleme 1 (MM1A) | Ülke/bölge A bağlamı olan model eşleme 2 (MM2A) | Ülke/bölge A bağlamı olan bir şirketin denetimi altında çalıştırma | Ülke/bölge B bağlamı olan bir şirketin denetimi altında çalıştırma |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Hata (eksik eşleme)   | Hata (eksik eşleme)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Hata (birden çok eşleme) | Hata (birden çok eşleme)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Hata (birden çok eşleme) | MM1                        |
|     6   |     +   | varsayılan |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | varsayılan |         | MM1A                      | MM1                        |
|     8   |     +   |         | varsayılan |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | varsayılan | varsayılan | Hata (birden çok eşleme) | MM1                        |
|    10   | varsayılan |         |         |         | MM1                       | MM1                        |
|    11   | varsayılan |    +    |         |         | MM1                       | MM1                        |
|    12   | varsayılan |         |    +    |         | MM1                       | MM1                        |
|    13   | varsayılan | varsayılan |         |         | Hata (birden çok eşleme) | Hata (birden çok eşleme)  |
|    14   | varsayılan |         | varsayılan |         | MM1A                      | MM1                        |
|    15   | varsayılan |         | varsayılan | varsayılan | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | varsayılan | varsayılan | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>ER biçiminin yürütülmesinde hangi eşlemenin kullanıldığını öğrenme

### <a name="configure-er-user-parameters"></a>ER kullanıcı parametrelerini yapılandırma

1.  **Yapılandırmalar** sayfasında, Eylem Bölmesi'nde **YAPILANDIRMALAR** sekmesinde **Kullanıcı parametreleri**'ni seçin.
2.  **Hata ayıklama modu** seçeneğini **Evet** olarak ayarlayın.
4.  **Tamam**'ı seçin.

### <a name="run-the-configured-format"></a>Yapılandırılmış biçimi çalıştırma

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşlemeleri öğrenme biçimi**'ni seçin.
2.  **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
3.  **Tamam**'ı seçin.

### <a name="review-the-er-debug-log"></a>ER hata ayıklama günlüğünü gözden geçirme

1.  Gezinti bölmesinde, **Modüller \> Kuruluş yönetimi \> Elektronik raporlama \> Yapılandırma hata ayıklama günlüğü**'ne gidin.
2.  **Bu sayfayı yeniden yükleyin** düğmesini seçin.

![ER çalıştırma günlükleri sayfası.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Yürütülen ER biçimi için ER hata ayıklama günlüğüne yeni bir kayıt eklendiğini unutmayın. Bu kaydın **Düzey** alanı **Bilgi** olarak ayarlandığından kayıt bilgi amaçlıdır. Biçim bileşeni alanı **Eşleme yapılandırması** olarak ayarlandığından kayıt, (**Yapılandırma adı** alanında seçilen) **Eşlemeleri öğrenme biçimi** ER biçiminin yürütülmesi sırasında kullanılan model eşleme hakkında sizi bilgilendirir. **Oluşturulan metin** alanının içeriği, **Eşleme (FR)** yapılandırmasında yer alan **Eşleme (FR)** eşleme bileşeninin bu raporu çalıştırmak için kullanıldığı konusunda sizi bilgilendirir.

## <a name="appendix-1"></a><a name="appendix1"></a> Ek 1

### <a name="configure-a-sample-data-model"></a>Örnek veri modeli yapılandırma

RCS kurulumunuzda oturum açın.

Bu örnekte, Litware, Inc. adlı örnek şirket için bir yapılandırma oluşturacaksınız. Bu adımları tamamlamak için öncelikle RCS'de [ER Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedüründeki adımları tamamlamanız gerekir.

#### <a name="create-an-er-data-model-configuration"></a>ER veri modeli yapılandırması oluşturma

1.  Varsayılan panoda **Elektronik raporlama**'yı seçin.
2.  **Raporlama yapılandırmaları** kutucuğunu seçin.
3.  **Yapılandırmalar** sayfasında, **Yapılandırma oluştur**'u seçin.
4.  Açılan iletişim kutusunda, **Ad** alanına **Eşlemeleri öğrenme modeli** girin.
5.  **Yapılandırma oluştur**'u seçin.
6.  **Yapılandırma bileşenleri** hızlı sekmesini seçin.

Bu ER yapılandırmasının taslak sürümü 1'in düzenlemeye hazır olduğunu unutmayın. Bu sürüm veri modeli bileşenini içerir.

#### <a name="design-a-sample-data-model"></a>Örnek veri modeli tasarlama

1.  **Yapılandırmalar sayfası**'nda, **Tasarımcı**'yı seçin.
2.  **Yeni**'yi seçin.
3.  Açılan iletişim kutusunda, **Ad** alanına **Giriş noktası 1** girin.
4.  **Ekle**'yi seçin.
5.  **Yeni**'yi seçin.
6.  Açılan iletişim kutusunda, **Ad** alanına **İşlev tanımı** girin.
7.  **Ekle**'yi seçin.
8.  **Yeni**'yi seçin.
9.  Açılan iletişim kutusunda, **Yeni düğüm** alan grubunda, **Model kökü**'nü seçin.
10. **Ad** alanına **Giriş noktası 2** girin.
11. **Giriş noktası 2**'yi seçin.
12. **Ekle**'yi seçin.
13. **Yeni**'yi seçin.
14. Açılan iletişim kutusunda, **Ad** alanına **İşlev tanımı** girin.
15. **Ekle**'yi seçin.

    ![ER veri modeli tasarımcısı sayfası.](./media/RCS-Context-specific-mapping-Model.PNG)

16. **Kaydet**'i seçin.
17. Sayfayı kapatın.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Model yapılandırmasının değiştirilmiş sürümünü tamamlama

1.  **Yapılandırmalar** sayfasında **Sürümler** hızlı sekmesinde **Durumu değiştir**'i seçin.

    > Gerekli model eşlemeleri ve biçimlerini tasarlamak üzere kullanılabilmesi için tasarlanan model yapılandırmasının durumunu **Taslak** yerine **Tamamlandı** olarak değiştirin.

2.  **Tamamlandı**'yı seçin.
3.  **Tamam**'ı seçin.

Oluşturduğunuz yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.

### <a name="configure-a-sample-model-mapping"></a>Örnek model eşlemesi yapılandırma

#### <a name="create-an-er-model-mapping-configuration"></a>ER model eşleme yapılandırması oluşturma

1.  **Yapılandırmalar** sayfasında, **Yapılandırma oluştur**'u seçin.
2.  Açılan iletişim kutusunda **Yeni** alan grubunda, **Eşlemeleri öğrenme Modeli veri modeline dayalı model eşleme** seçeneğini belirleyin.
3.  **Ad** alanına **Eşleme (Genel)** girin.
4.  **Veri modeli tanımı** alanında, **Giriş noktası 1**'i seçin.
5.  **Yapılandırma oluştur**'u seçin.

Bu ER yapılandırmasının taslak sürümü 1'in düzenlemeye hazır olduğunu unutmayın. Bu sürüm model eşleme bileşenini içerir.

#### <a name="design-a-sample-model-mapping"></a>Örnek model eşlemesi tasarlama

1.  **Yapılandırmalar** sayfasında, **Tasarımcı**'yı seçin.

    **Modele** model eşlemesi yön türünün **Giriş noktası 1** tanımı için bu bileşene otomatik olarak eklendiğini unutmayın.
    
2.  Eklenen model eşlemesini düzenlemeye başlamak için **Tasarımcı**'yı seçin.
3.  **Veri modeli** bölümünde, **Düzenle**'yi seçin.
4.  **Formül** alanına **Genel işlev 1** girin.
5.  **Kaydet**'i seçin.
6.  **Formül tasarımcısı** sayfasını kapatın.

    ![ER model eşleme Tasarımcısı sayfası, giriş noktası 1 tanımı.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  **Kaydet**'i seçin.
8.  **Model eşleme tasarımcısı** sayfasını kapatın
9.  **Yeni**'yi seçin.
10. **Tanım** alanında, **Giriş noktası 2**'yi seçin.
11. **Ad** alanına **Eşleme (Genel) 2** girin.
12. **Tasarımcı**’yı seçin.
13. **Veri modeli** bölümünde, **Düzenle**'yi seçin.
14. **Formül** alanına **Genel işlev 2** girin.
15. **Kaydet**'i seçin.
16. **Formül tasarımcısı** sayfasını kapatın.

    ![ER model eşleme Tasarımcısı sayfası, giriş noktası 2 tanımı.](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. **Kaydet**'i seçin.
18. **Model eşleme tasarımcısı** sayfasını kapatın

    ![Giriş noktası tanımlarıyla ER model eşlemeleri sayfası.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. **Model eşlemeleri** sayfasını kapatın

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Model eşleme yapılandırmasının değiştirilmiş sürümünü tamamlama

1.  **Yapılandırmalar sayfası**'nda **Sürümler** hızlı sekmesinde **Durumu değiştir**'i seçin.

    > ER biçimleri tarafından kullanılabilmesi için tasarlanan model eşleme yapılandırmasının durumunu **Taslak** yerine **Tamamlandı** olarak değiştirin.

2.  **Tamamlandı**'yı seçin.
3.  **Tamam**'ı seçin.

Oluşturulan yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.

### <a name="configure-a-sample-format"></a>Örnek biçim yapılandırma

#### <a name="create-an-er-format-configuration"></a>ER biçimi yapılandırması oluşturma

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşlemeleri öğrenme modeli** seçeneğini belirleyin.
2.  **Yapılandırma oluştur**'u seçin.
3.  Açılan iletişim kutusunda **Yeni** alan grubunda, **Eşlemeleri öğrenme modeli veri modeline dayalı biçim** seçeneğini belirleyin.
4.  **Ad** alanına, **Eşlemeleri öğrenme biçimi** girin.
5.  **Veri modeli tanımı** alanında, **Giriş noktası 1**'i seçin.
6.  **Yapılandırma oluştur**'u seçin.

Bu ER yapılandırmasının taslak sürümü 1'in düzenlemeye hazır olduğunu unutmayın. Bu sürüm biçim bileşenini içerir.

#### <a name="design-a-sample-format"></a>Örnek biçim tasarlama

1.  **Yapılandırmalar** sayfasında, **Tasarımcı**'yı seçin.
2.  **Kök ekle**'yi seçin.
3.  **Metin** grubunda, **Dize** seçeneğini belirleyin.
4.  **Tamam**'ı seçin.

#### <a name="bind-format-elements-to-a-data-source"></a>Biçim öğelerini veri kaynağına bağlama

1.  **Biçim tasarımcısı** sayfasında, **Eşleme** sekmesinde model veri kaynağını genişletin.
2.  **İşlev açıklaması** alanını seçin.
3.  **Bağla**'yı seçin.

    ![ER biçim tasarımcısı sayfası.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  **Kaydet**'i seçin.
5.  Sayfayı kapatın.

## <a name="appendix-2"></a><a name="appendix2"></a> Ek 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Genel özelleştirme için örnek model eşlemesi yapılandırma

Yapılandırma sağlayıcısının (iş ortağı) size sağladığı bir model eşlemesini yapılandırmak ve ardından özelleştirilmiş sürümü ER biçimleriniz için bir veri kaynağı olarak kullanmak isteyebilirsiniz. Bu durumda, var olan model eşlemelerinde gerekli değişiklikleri yapmak için özel bir ER model eşleme yapılandırması oluşturmanız gerekir. Bu ekteki prosedürlerde örnek olarak **Eşleme (Genel)** model eşlemesi kullanılmıştır.

#### <a name="create-an-er-model-mapping-configuration"></a>ER model eşleme yapılandırması oluşturma

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşleme (Genel)** seçeneğini belirleyin.
2.  **Yapılandırma oluştur**'u seçin.
3.  Açılan iletişim kutusunda, **Yeni** alan grubunda **Addan türet: Eşleştirme (Genel), Litware, Inc.** seçeneğini belirleyin.
4.  **Ad** alanına, **Eşleme (Genel) özel** girin.
5.  **Yapılandırma oluştur**'u seçin.

Bu ER yapılandırmasının taslak sürümü 1'in düzenlemeye hazır olduğunu unutmayın.

#### <a name="design-a-sample-model-mapping"></a>Örnek model eşlemesi tasarlama

1.  **Yapılandırmalar** sayfasında, **Tasarımcı**'yı seçin.

    > Temel yapılandırmanın model eşlemelerinin otomatik olarak bu yapılandırmaya kopyalandığını unutmayın.

2.  **Eşleme (Genel) Kopya** eşlemesini seçin.
3.  **Tasarımcı**’yı seçin.
4.  **Veri modeli** bölümünde, **Düzenle**'yi seçin.
5.  **Formül** alanına **"Genel işlev 1 özel"** girin.
6.  **Kaydet**'i seçin.
7.  Sayfayı kapatın.

    ![ER model eşleme Tasarımcısı sayfası, genel işlev 1 özel formülü.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  **Kaydet**'i seçin.
9.  Sayfayı kapatın.
10. **Eşleme (Genel) 2 Kopya** eşlemesini seçin.
11. **Tasarımcı**’yı seçin.
12. **Veri modeli** bölümünde, **Düzenle**'yi seçin.
13. **Formül** alanına **"Genel işlev 2 özel"** girin.
14. **Kaydet**'i seçin.
15. Sayfayı kapatın.

    ![ER model eşleme Tasarımcısı sayfası, genel işlev 2 özel formülü.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. **Kaydet**'i seçin.
17. Sayfayı kapatın.

    ![Eşleme için veri kaynağı eşleme sayfasına ER modeli (genel) kopyalama eşlemesi.](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Sayfayı kapatın.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Model eşleme yapılandırmasının değiştirilmiş sürümünü tamamlama

1.  **Yapılandırmalar** sayfasında **Sürümler** hızlı sekmesinde **Durumu değiştir**'i seçin.

    > ER biçimleri tarafından kullanılabilmesi için tasarlanan model eşleme yapılandırmasının durumunu **Taslak** yerine **Tamamlandı** olarak değiştirin.

2.  **Tamamlandı**'yı seçin.
3.  **Tamam**'ı seçin.

Oluşturulan yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.

## <a name="appendix-3"></a><a name="appendix3"></a> Ek 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Ülkeye/bölgeye özgü özelleştirme için örnek model eşlemesi yapılandırma

Bazı ER biçimlerinde, veri hazırlığı için ülkeye/bölgeye özgü gereksinimler olabilir. Bu durumda, ayrı bir ER model eşleme yapılandırması yönetebilir ve bu ülkeye/bölgeye özgü gereksinimlerin uygulanmasını genel uygulamadan ayırabilirsiniz. Bu ekteki prosedürlerde örnek olarak, **Eşlemeleri öğrenme biçimi** ER biçimi ve Fransızcaya özgü gereksinimler kullanılmıştır.

#### <a name="create-an-er-model-mapping-configuration"></a>ER model eşleme yapılandırması oluşturma

Ülkeye/bölgeye özgü gereksinimleri uygulamak için öncelikle yeni bir ER model eşleme yapılandırması oluşturun. Özel ER model eşleme yapılandırmanızı temel olarak kullanın.

1.  **Yapılandırmalar** sayfasında, yapılandırmalar ağacında, **Eşleme (Genel) özel** öğesini seçin.
2.  **Yapılandırma oluştur**'u seçin.
3.  Açılan iletişim kutusunda, **Yeni** alan grubunda **Addan türet: Eşleştirme (Genel) özel, Litware, Inc.** seçeneğini belirleyin.
4.  **Ad** alanına **Eşleme (FR)** girin.
5.  **Yapılandırma oluştur**'u seçin.

Bu ER yapılandırmasının taslak sürümü 1'in düzenlemeye hazır olduğunu unutmayın.

#### <a name="design-a-sample-model-mapping"></a>Örnek model eşlemesi tasarlama

1.  **Yapılandırmalar** sayfasında, **Tasarımcı**'yı seçin.

    > Temel yapılandırmanın model eşlemelerinin otomatik olarak bu yapılandırmaya kopyalandığını unutmayın.

2.  **Eşleme (Genel) Kopya Kopya** eşlemesini seçin.
3.  **Eşleme (FR)** olarak yeniden adlandırın.
4.  **Tasarımcı**’yı seçin.
5.  **Veri modeli** bölümünde, **Düzenle**'yi seçin.
6.  **Formül** alanına **FR işlev 1** girin.
7.  **Kaydet**'i seçin.
8.  Sayfayı kapatın.

    ![ER model eşleme Tasarımcısı sayfası, FR işlev 1 formülü.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  **Kaydet**'i seçin.
10. Sayfayı kapatın.
11. **Eşleme (Genel) 2 Kopya Kopya** eşlemesini seçin.
12. **Eşleme (FR) 2** olarak yeniden adlandırın.
13. **Tasarımcı**’yı seçin.
14. **Veri modeli** bölümünde, **Düzenle**'yi seçin.
15. **Formül** alanına **FR işlev 2** girin.
16. **Kaydet**'i seçin.
17. Sayfayı kapatın.

    ![ER model eşleme Tasarımcısı sayfası, FR işlev 2 formülü.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. **Kaydet**'i seçin.
19. Sayfayı kapatın.

    ![Veri kaynağı eşleme sayfasına ER modeli.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Sayfayı kapatın.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Kullanım için ülke/bölge bağlamı kısıtlamalarını belirleme

1.  **Yapılandırmalar** sayfasında, **ISO Ülke/bölge kodları** hızlı sekmesinde **Yeni**'yi seçin.
2.  **ISO** alanında, **FR**'yi seçin.
3.  **Kaydet**'i seçin.

ER biçimini çalıştırmak için Finance uygulamasındaki belirli bir şirkette oturum açmanız gerektiğini unutmayın. Bu nedenle, bu şirket ER biçiminin yürütülmesini ve temel ER veri modelinin doğru ER modeli eşlemesinin seçilmesini denetleyen bir taraf olarak kabul edilebilir. **FR** ülke kodunun eklenmesiyle, bu biçim Fransızca ülke/bölge bağlamına sahip bir şirketin denetimi altında çalıştırıldığında bu model eşlemesinin yalnızca temel veri modelinin ER biçimi tarafından seçilmek üzere kullanılabilir olduğunu belirtirsiniz.

ER model eşleme yapılandırmasının tek bir sürümü için birden çok ülke/bölge kodu ekleyebilirsiniz. Bu şekilde, bu model eşleme yapılandırmasında yer alan model eşlemeleri farklı ülke/bölge bağlamına sahip şirketlerin denetimi altında çalıştırılan bir ER biçimi için kullanılabilir.

Ülke/bölge kodları listesinin ER model eşleme yapılandırmasının her sürümü için belirlendiğini ve sürümler arasında değişiklik gösterebileceğini unutmayın.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Model eşleme yapılandırmasının değiştirilmiş sürümünü tamamlama

1.  **Yapılandırmalar** sayfasında **Sürümler** hızlı sekmesinde **Durumu değiştir**'i seçin.

    > ER biçimleri tarafından kullanılabilmesi için tasarlanan model eşleme yapılandırmasının durumunu **Taslak** yerine **Tamamlandı** olarak değiştirin.

2.  **Tamamlandı**'yı seçin.
3.  **Tamam**'ı seçin.

Oluşturulan yapılandırmanın tamamlanmış sürüm 1 olarak kaydedildiğini unutmayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[Ayrı ER yapılandırmalarında ER model eşlemesini yönetme](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Ülke/bölge bağlamı uygulama](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>RCS'de iki paylaşılan ER model eşleme yapılandırması yapılandırdım ve bunlardan birini varsayılan model eşleme yapılandırması olarak işaretledim. Model eşlemelerini test etmek için aynı temel ER veri modeli yapılandırması için oluşturulmuş bir ER biçimini başarıyla çalıştırdım. Ardından tüm ER çözümünü (ER veri modeli, iki ER model eşleme yapılandırması ve ER biçimi yapılandırması) Finance uygulamasında içe aktardım. Finance uygulamasında aynı ER biçimini çalıştırmayı denediğimde neden bir hata iletisi alıyorum?
Varsayılan model eşleme ayarı ortama özgüdür. RCS'de yapılandırılır ancak Finance uygulamasına dışa aktarılamaz. Bu ER biçimini başarıyla çalıştırmak için ER model eşleme yapılandırmalarından birini, Finance uygulamasında da varsayılan model eşleme yapılandırması olarak işaretlemeniz gerekir.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Bir modeli paylaşılan model eşleme olarak yapılandırdım ve bunun taslak sürümünü tamamladım. Ardından aynı veri modeli için yeni bir model eşleme yapılandırması ekledim ve bunu Fransızcaya özgü olarak yapılandırdım. Bu ER biçiminin doğru kök tanımını kullanmasına ve yürütme işleminin Fransızca ülke/bölge bağlamına sahip şirketin denetimi altında gerçekleştirilmesine rağmen ER biçimini çalıştırdığımda neden paylaşılan model eşlemesi seçiliyor?
Paylaşılan model eşleme yapılandırmasının varsayılan model eşleme yapılandırması olarak işaretlenmediğinden emin olun. Aksi takdirde eşleme seçimi sırasında daha yüksek önceliğe sahip olur. Ayrıca ER biçimini yürütme sırasında bir eşleme seçildiğinde Fransızcaya özgü model eşleme yapılandırmasının dikkate alındığından emin olun. ER model eşleme yapılandırması yalnızca aşağıdaki koşullardan en az biri karşılandığında kullanılabilir:
- ER model eşleme yapılandırmasının en az bir sürümünün **Tamamlandı** veya **Paylaşılan** durumunda olması. Bu durumda, ER biçimini yürütmek için en yüksek sürüm numarasına sahip sürüm kullanılır.
- ER model eşleme yapılandırması için **Taslağı çalıştır** seçeneğinin açık olması. Bu durumda, ER biçimini yürütmek için **Taslak** durumuna sahip sürüm kullanılır.
> **Ayarı çalıştır** ER kullanıcı parametresi açıldığında **Taslağı çalıştır** seçeneği, her ER model eşleme yapılandırmasının **Yapılandırmalar** sayfasında kullanılabilir hale gelir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
