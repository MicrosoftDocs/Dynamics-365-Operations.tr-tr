---
title: Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme
description: Bu konuda, parametreli HESAPLANAN ALAN veri kaynaklarını ekleyerek, Elektronik raporlama (ER) çözümlerinin performansını artırmaya nasıl yardımcı olabileceğiniz açıklanmaktadır.
author: NickSelin
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 299570d6a94b0f9e7ee7cf490d4c1aeeb86d5716
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749525"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Parametreli HESAPLANAN ALAN veri kaynakları ekleyerek ER çözümleri performansını iyileştirme

[!include [banner](../includes/banner.md)]

Bu konuda çalıştırılan [Elektronik raporlama (ER)](general-electronic-reporting.md) biçimlerinin [performans izlemelerini](trace-execution-er-troubleshoot-perf.md) nasıl alabileceğinizi açıklanır ve sonra da bu izlemelerden alınan bilgileri kullanarak parametreli **Hesaplanan alan** veri kaynağı yapılandırarak nasıl performansı artırabileceğiniz açıklanır.

ER yapılandırmalarının iş belgeleri oluşturmak amacıyla tasarlanması işleminin bir parçası olarak, uygulamadan veri getirmek ve oluşturulan çıktıya girmek için kullanılan yöntemi tanımlayın. **Hesaplanmış alan** türünde bir parametreli ER veri kaynağı tasarlayarak, veritabanı çağrılarının sayısını azaltabilir ve ER ile yapılan biçimlendirme çalışmasının ayrıntılarını toplamada yer alan zaman ve maliyeti önemli ölçüde azaltabilirsiniz.

## <a name="prerequisites"></a>Önkoşullar

- Bu konudaki örnekleri tamamlamak için aşağıdaki [rollerden](../sysadmin/tasks/assign-users-security-roles.md) birine erişiminiz olmalıdır:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Şirketin **DEMF** olarak ayarlanması gerekir.
- Bu konunun [Ek 1](#appendix1) bölümündeki adımları izleyerek konudaki örnekleri tamamlamak için gerekli olan Microsoft ER çözümü bileşenlerini indirin.
- Örnek Microsoft er çözümünün performansını artırmaya yardımcı olmak amacıyla ER altyapısını kullanmak için gereken en az ER parametre kümesini yapılandırmak için bu konunun [Ek 2](#appendix2) bölümündeki adımları izleyin.

## <a name="import-the-sample-er-solution"></a>Örnek ER çözümünü içe aktarma

Satıcı hareketleri sunan yeni bir rapor oluşturmak üzere yeni bir ER çözümü tasarladığınızı düşünün. Şu anda, seçilen satıcı için hareketleri **Satıcı hareketleri** sayfasında bulabilirsiniz. (**Borç hesapları** \> **Satıcılar** \> **Tüm satıcılar**'a gidin, bir satıcı seçin ve Eylem Panosu üzerinde, **Satıcı** sekmesinde, **Hareketler** grubunda, **Hareketler**'i seçin.) Ancak, tüm satıcı hareketinin aynı anda elektronik bir belgede XML biçiminde olmasını istersiniz. Bu çözüm, gerekli veri modelini, model eşlemeyi ve biçim bileşenlerini içeren birkaç ER yapılandırmasından oluşur.

İlk adım, satıcı hareketleri raporu oluşturmak için örnek ER çözümünü içe aktarmaktır.

1. Şirketiniz için sağlanan Microsoft Dynamics 365 Finance örneğinde oturum açın.
2. Bu konuda, **Litware, Inc.** örnek şirket için yapılandırmalar oluşturacak ve değiştireceksiniz. Bu yapılandırma sağlayıcısının Finance'e eklenmiş olduğundan ve etkin olarak seçildiğinden emin olun. Daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. **Elektronik raporlama** çalışma alanında **Raporlama yapılandırmaları** kutucuğunu seçin.
4. **Yapılandırmalar** sayfasında, önkoşul olarak karşıdan yüklediğiniz ER yapılandırmalarını aşağıdaki sırada Finance içine aktarın: veri modeli, model eşleme, biçim. Her bir yapılandırma için şu adımları izleyin:

    1. Eylem Bölmesinde, **Exchange** \> **XML dosyasından yükle**'yi seçin.
    2. ER yapılandırması için XML biçiminde uygun dosyayı seçmek için **Gözat**'ı seçin.
    3. **Tamam**'ı seçin.

![Yapılandırmalar sayfasında içe aktarılan yapılandırmalar](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Örnek ER çözümüne göz atma

### <a name="review-the-model-mapping"></a>Model eşlemeyi gözden geçirme

1. **Yapılandırmalar** sayfasında yapılandırma ağacında, **Performans geliştirme modeli**'ni genişletin ve **Performans geliştirme eşleme**'yi seçin.
2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
3. **Veri kaynağı eşleme modeli** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.

    Bu ER model eşlemesi aşağıdaki eylemleri gerçekleştirmek üzere tasarlanmıştır:

    - VendTrans tablosunda (**Trans** veri kaynağı) saklanan satıcı hareketlerinin listesini getirir.
    - Her hareket için, VendTable tablosundan, hareketin ( satıcı veri kaynağı) deftere nakledildiği satıcının kaydını (**\#Vend** veri kaynağı) getir.

    > [!NOTE]
    > **\#Vend** veri kaynağı, var olan çok-bir ilişkisi **\@\>Relations'.VendTable\_AccountNum** kullanarak ilgili satıcı kaydını getirmek üzere yapılandırılmıştır.

    Bu yapılandırmadaki model eşlemesi, bu model için oluşturulan ve Finance'de yürütülen ER biçimleri için temel veri modelini uygular. Bu nedenle **Trans** veri kaynaklarının içeriği soyut **model** veri kaynakları gibi ER biçimleri için sunulur.

    ![Model eşleme tasarımcı sayfasında Trans veri kaynağı](media/er-calculated-field-ds-performance-mapping-1.png)

4. **Model eşleme tasarımcısı** sayfasını kapatın
5. **Veri kaynağı modeli eşleme** sayfasını kapatın.

### <a name="review-format"></a>Biçimi gözden geçirme

1. **Yapılandırmalar** sayfasında yapılandırma ağacında, **Performans geliştirme modeli**'ni genişletin ve **Performans geliştirme biçimi**'ni seçin.
2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
3. **Biçim tasarımcısı** sayfasında **Eşleme** sekmesinde **Genişlet/Daralt** seçeneğini belirtin.
4. **Model**, **Veri** ve **Hareket** öğelerini genişletin.

    Bu ER biçimi, XML biçiminde satıcı hareketleri raporu oluşturmak için tasarlanmıştır.

    ![Biçim tasarımcısı sayfasında veri kaynaklarını ve yapılandırılmış biçim öğelerinin bağlarını biçimlendirme](media/er-calculated-field-ds-performance-format.png)

5. **Biçim tasarımcısı** sayfasını kapatın.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Yürütülmesini izlemek için örnek ER çözümünü çalıştırma

ER çözümünün ilk sürümünü tasarlamayı bitirdiğinizi varsayalım. Şimdi çözümü Finance örneğiniz içinde test etmek ve yürütme performansını analiz etmek istiyorsunuz.

### <a name="turn-on-the-er-performance-trace"></a>ER performans izlemesini aç

1. **DEMF** şirketini seçin.
2. Bir ER biçimi çalıştırılırken, performans izleme oluşturmak için [ER performans izlemesini aç](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) adımlarını izleyin.

    ![Kullanıcı parametreleri iletişim kutusu](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>ER biçimini çalıştır

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme biçimi** öğesini seçin.
3. Eylem Bölmesinde, **Çalıştır**'ı seçin.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Model eşleme performansını çözümlemek için performans izlemesini kullanma

1. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme eşleme** öğesini seçin.
2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
3. **Model eşlemeleri** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.
4. **Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.
5. Oluşturulan en son izlemeyi seçin ve sonra **Tamam**'ı seçin.

Geçerli model eşleştirmesinin bazı veri kaynağı öğeleri için yeni bilgiler artık kullanılabilir hale gelir:

- Veri kaynağı kullanılarak veri almada harcanan gerçek süre
- Aynı zaman, tüm model eşleşmesinin yürütülmesi için harcanan toplam sürenin yüzdesi olarak ifade edilen saat

![Model eşleme tasarımcısı sayfasında yürütme zamanı ayrıntıları](./media/er-calculated-field-ds-performance-mapping-2.png)

**Performans istatistikleri** kılavuzunda, **Trans** veri kaynağının VendTrans tablosunu bir kez çağırdığı gösterilir. **Trans** veri kaynağının **\[265\]\[Q:265\]** değeri, uygulama tablosundan 265 satıcı hareketinin getirildiğini ve veri modeline döndürüldüğünü gösterir.

**Performans istatistikleri** kılavuzu ayrıca geçerli model eşleştirmesinin, **\#Vend** veri kaynağı çalıştırılırken veritabanı isteklerinin çoğaltılacağını da gösterir. Bu çoğaltma işlemi aşağıdaki nedenlerle yapılır:

- Toplam 530 çağrı için satıcı tablosu, her 265 tekrarlandırılmış satıcı hareketi için iki kez çağrılır:

    - Satıcı hesap numarasını girmek için bir çağrı yapılır.
    - Satıcı adını girmek için bir çağrı yapılır.

- Alınan hareketler yalnızca beş satıcı için deftere nakledildiğinden, tekrarlandırılmış her satıcı hareketi için satıcı tablosu çağrılır. 530 çağrının 525 tanesi çoğaltılır. Aşağıdaki şekilde, tekrarlanan çağrılar (veritabanı istekleri) hakkında aldığınız ileti gösterilir.

![Model eşleme tasarımcısı sayfasındaki yinelenen veritabanı istekleri hakkında ileti](./media/er-calculated-field-ds-performance-mapping-2a.png)

Toplam model eşleme yürütme süresinin (yaklaşık sekiz saniye), yüzde 80'ninden fazlasının (yaklaşık 6 saniye) VendTable uygulama tablosundan değerleri alırken harcandığını unutmayın. Bu yüzde beş satıcının iki özniteliği için çok büyük olup, VendTrans uygulama tablosundaki bilginin hacmiyle karşılaştırılır.

Her hareket için satıcı ayrıntılarını almak amacıyla yapılan çağrı sayısını azaltmak ve model eşleme performansını artırmak için, **\#Vend** veri kaynağı için önbelleğe alma özelliğini kullanabilirsiniz.

> [!NOTE]
> **Trans\\\#Vend** veri kaynağı, çalışma süresinde, **Trans** veri kaynağının geçerli hareketinin kapsamında önbelleğe alınır.

**\#Vend** veri kaynağını önbelleğe alarak, çoğaltılan çağrıların sayısını 525'ten 260'a düşürürsünüz, ancak çoğaltma işlemini tamamen ortadan kalkmaz. Çoğaltmayı tamamen kaldırmak için, **Hesaplanmış alan** türünde yeni bir parametreli veri kaynağı yapılandırabilirsiniz.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Yürütme izlemesinin bilgilerine dayalı olarak model eşlemeyi geliştirin

### <a name="change-the-logic-of-the-model-mapping"></a>Model eşlemenin mantığını değiştirme

Veritabanında çoğaltılan çağrıların engellenmesine yardımcı olmak amacıyla, önbelleğe almayı ve **Hesaplanan alan** türü veri kaynağını kullanmak için bu adımları izleyin.

1. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme eşleme** öğesini seçin.
2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
3. **Model eşlemeleri** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.
4. **Model eşleme Tasarımcısı** sayfasında, VendTable uygulama tablosundaki kayıtlara erişmek üzere **Tablo kayıtları** türünde bir veri kaynağı eklemek için aşağıdaki adımları izleyin:

    1. **Veri kaynağı türleri** bölmesinde, **Dynamics 365 for Operations** seçeneğini genişleterek **Tablo kayıtları**'nı seçin.
    2. **Kök ekle**'yi seçin.
    3. İletişim kutusunda, **Ad** alanına **Vend** girin.
    4. **Tablo** alanına, **VendTable** girin.
    5. **Tamam**'ı seçin.

5. Yalnızca bu veri kaynakları bir kapsayıcıda bulunuyorsa, **Hesaplanmış alan** türündeki veri kaynaklarına yapılan çağrıları parametreleştirebilirsiniz. Bu nedenle, **Hesaplanan alan** türünde yeni bir parametreli veri kaynağı tutmak üzere **Boş kapsayıcı** türünde bir veri kaynağı eklemek için aşağıdaki adımları izleyin:

    1. **Veri kaynağı türleri** bölmesinde, **Genel** seçeneğini genişleterek **Boş kapsayıcı**'yı seçin.
    2. **Kök ekle**'yi seçin.
    3. İletişim kutusunda, **Ad** alanına **Kutu** girin.
    3. **Tamam**'ı seçin.

    ![Model eşleme tasarımcı sayfasında Kutu veri kaynağı](./media/er-calculated-field-ds-performance-mapping-3.png)

6. **Hesaplanan alan** türüne ait parametreli bir veri kaynağı eklemek için aşağıdaki adımları izleyin:

    1. **Veri kaynakları** bölmesinde **Kutu**'yu seçin.
    2. **Veri kaynağı türleri** bölmesinde, **İşlevler** öğesini genişletin ve **Hesaplanan alan** öğesini seçin.
    3. **Ekle**'yi seçin.
    4. İletişim kutusunda, **Ad** alanına **Vend** girin.
    5. **Formül düzenle**’yi seçin.
    6. **Formül Tasarımcısı** sayfasında, bu veri kaynağı çağrıldığında sağlanması gereken parametreleri belirtmek için **Parametreler**'i seçin.
    7. **Parametreler** iletişim kutusunda, **Yeni**'yi seçin.
    8. **Ad** alanına **parmVendAccNumber** girin.
    9. **Tür** alanında **Dize**'yi seçin.
    10. **Tamam**'ı seçin.
    11. **Formül** alanında, **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** değerini girin.
    12. **Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.
    13. Yeni veri kaynağını eklemek için **Tamam**'ı seçin.

7. Eklenen veri kaynağını yürütme sırasında önbelleğe alınmış olarak işaretlemek için aşağıdaki adımları izleyin:

    1. **Veri kaynakları** bölmesinde **Box\\Vend** değerini seçin.
    2. **Önbellek**'i seçin.

    > [!NOTE]
    > **Box\\Vend** veri kaynağı, çalışma süresinde, **Trans** veri kaynağının bütün satıcı hareketinin kapsamında önbelleğe alınır.

8. **Box\\Vend** veri kaynağı kutusunu kullanacak şekilde iç içe geçmiş **Trans\\\#Vend** veri kaynağını güncelleştirmek için aşağıdaki adımları izleyin:

    1. **Veri kaynakları** bölmesinde **Trans** öğesini genişletin.
    2. **Trans\\\#Vend** veri kaynağını seçin ve **Düzenle** \> **Formülü düzenle** öğesini seçin.
    3. **Formül Tasarımcısı** sayfasında, **Formül** alanına, **Box.Vend(\@.AccountNum)** değerini girin.
    4. **Kaydet**'i seçin ve ardından **Formül tasarımcısı** sayfasını kapatın.
    5. Seçili veri kaynağındaki değişikliklerinizi tamamlamak için **Tamam**'ı seçin.

9. **Kaydet**'i seçin.

    ![Model eşleme tasarımcı sayfasında Vend veri kaynağı](./media/er-calculated-field-ds-performance-mapping-4.png)

10. **Model eşleme tasarımcısı** sayfasını kapatın
11. **Model eşlemeleri** sayfasını kapatın

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER model eşlemesinin değiştirilmiş sürümünü tamamlayın

1. **Yapılandırmalar** sayfasında, **Sürümler** hızlı sekmesinde, **Performans geliştirme eşleme** yapılandırmasının **1.2** sürümünü seçin.
2. **Durumu değiştir** \> **Tamamla** öğesini ve ardından **Tamam**'ı seçin.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Çalışmayı izlemek için değiştirilmiş ER çözümünü çalıştırın

Yeni bir performans izleme oluşturmak için bu konuda daha önce işlenen [ER biçimini çalıştır](#run-format) bölümündeki adımları tekrar edin.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Model eşlemede ayarlamaları çözümlemek için performans izlemesini kullanma 

1. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Performans geliştirme eşleme** öğesini seçin.
2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
3. **Model eşlemeleri** sayfasında Eylem Panosu üzerinde **Tasarımcı**'yı seçin.
4. **Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.
5. Oluşturulan en son izlemeyi seçin ve sonra **Tamam**'ı seçin.

Model eşleştirmesinde yaptığınız ayarlamaların veritabanındaki yinelenen sorguları elediğine dikkat edin. Bu model eşleme için veritabanı tablolarına ve veri kaynaklarına yapılan çağrı sayısı da azaltılmıştır.

![Model eşleme tasarımcı sayfası 1'de bilgiyi izleme](./media/er-calculated-field-ds-performance-mapping-5.png)

Toplam yürütme süresi yaklaşık 20 kat düşürüldü (yaklaşık 8 saniyeden 400 milisaniyeye). Bu nedenle, tüm ER çözümü performansı iyileştirilmiştir.

![Model eşleme tasarımcı sayfası 2'de bilgiyi izleme](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Ek 1: Örnek Microsoft ER çözümünün bileşenlerini indirme

Aşağıdaki dosyaları indirip yerel olarak saklamalısınız.

| Dosya                                        | İçerik |
|---------------------------------------------|---------|
| Performans geliştirme modeli.sürüm.1     | [Örnek ER verisi modeli yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Performans geliştirme eşleştirme.sürümü.1.1 | [Örnek ER model eşleme yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Performans geliştirme biçimi.sürümü.1.1  | [Örnek ER biçim yapılandırması](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Ek 2: ER altyapısını yapılandırma

Örnek Microsoft ER çözümünün performansını artırmak için ER altyapısını kullanmaya başlamadan önce, asgari ER parametre kümesini yapılandırmanız gerekir.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER parametrelerini yapılandırma

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Elektronik raporlama parametreleri** kutucuğunu seçin.
3. **Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.
4. **Ekler** sekmesinde, aşağıdaki parametreleri ayarlayın:

    - **Konfigürasyonlar** alanında, **DEMF** şirketi için **dosya** türünü seçin.
    - **İş arşivi**, **Geçici**, **temel** ve **diğer** alanlarında **Dosya** tipini seçin.

ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

Eklenen her ER yapılandırması bir ER konfigürasyon sağlayıcısı tarafından sahiplenilimli olarak işaretlenir. **Elektronik raporlama** çalışma alanında etkinleştirilen ER yapılandırma sağlayıcısı Bu amaçla kullanılır. Bu nedenle, ER konfigürasyonlarını eklemeye veya düzenlemeye başlamadan önce, **elektronik raporlama** çalışma alanında bir er yapılandırma sağlayıcısını etkinleştirmelisiniz.

> [!NOTE]
> Yalnızca ER yapılandırmasının sahibi yapılandırmayı düzenleyebilir. Bu nedenle, ER konfigürasyonu düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **elektronik raporlama** çalışma alanında etkinleştirilmelidir.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER yapılandırma sağlayıcıları listesini gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.
3. **Yapılandırma sağlayıcısı tablosu** sayfasında, her sağlayıcı kaydının benzersiz bir adı ve URL'si vardır. Bu sayfanın içeriğini gözden geçirin. **Litware, Inc.** için zaten bir kayıt varsa, sonraki yordamı atlayıp [Yeni bir ER yapılandırma sağlayıcısı ekleme](#ActivateProvider) bölümüne geçin.

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Yeni bir ER yapılandırması sağlayıcısı ekleme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.
3. **Yapılandırma sağlayıcıları** sayfasında, **Yeni**'yi seçin.
4. **Ad** alanına **Litware, Inc.** yazın.
5. **İnternet adresi** alanına `https://www.litware.com` girin.
6. **Kaydet**'i seçin.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme konfigürasyonları** sayfasında, **Konfigürasyon sağlayıcıları** bölümünde, **Litware, Inc.** döşemesini seçin ve sonra **etkin ayarla**'yı seçin.

ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md)
- [Hesaplanan alan türünün ER veri kaynaklarının parametreleştirilmiş çağrılarını destekleme](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]