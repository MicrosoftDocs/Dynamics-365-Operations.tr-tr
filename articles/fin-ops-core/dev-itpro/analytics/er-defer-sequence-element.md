---
title: ER biçimindeki sıra öğelerinin yürütülmesini erteleme
description: Bu konu, bir Elektronik raporlama (ER) biçimindeki bir sıra öğesinin yürütülmesinin nasıl erteleneceğini açıklamaktadır.
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b1a9bb072330f586799f5cfea676d941739ca818
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562178"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>ER biçimindeki sıra öğelerinin yürütülmesini erteleme

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Genel Bakış

Metin biçiminde giden belgeleri oluşturmak amacıyla kullanılan bir ER çözümünün [biçim bileşenini](general-electronic-reporting.md#FormatComponentOutbound) [yapılandırmak](tasks/er-format-configuration-2016-11.md) için [Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesinin Operations tasarımcısını kullanabilirsiniz. Yapılandırılmış biçim bileşeninin hiyerarşik yapısı, çeşitli türlerdeki biçim öğelerinden oluşur. Bu biçim öğeleri, oluşturulan belgeleri gerekli bilgilerle çalışma zamanında doldurmak için kullanılır. Varsayılan olarak, bir ER biçimi çalıştırdığınızda, biçim öğeleri, biçim hiyerarşisinde göründükleri sırayla çalıştırılır: bire tek, üstten alta doğru. Ancak, tasarım sırasında, yapılandırılan biçim bileşeninin herhangi bir sıra öğesinin yürütme sırasını değiştirebilirsiniz.

Yapılandırılan biçimdeki bir sıra biçimi öğesi için <a name="DeferredSequenceExecution"></a>**Ertelenmiş yürütme** seçeneğini etkinleştirerek, o öğenin yürütülmesini erteleyebilirsiniz. Bu durumda, öğenin üst öğesinin tüm diğer öğeleri çalıştırılıncaya kadar öğe çalıştırılmaz.

Bu özellik hakkında daha fazla bilgi edinmek için bu konudaki örneği tamamlayın.

## <a name="limitations"></a>Sınırlamalar

**Ertelenmiş yürütme** seçeneği yalnızca metin biçiminde **giden** belgeleri oluşturmak için kullanılan bir ER biçimi için yapılandırılmış sıra öğeleri için desteklenir.

**Ertelenmiş yürütme** seçeneği, maksimum uzunluğun sınırlı olduğu, kırpılmış sıralar olarak yapılandırılmış sıralar için geçerli değildir.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Örneğin: Bir ER biçimindeki bir sıra öğesinin yürütülmesini erteleme

Aşağıdaki adımlarda, Sistem Yöneticisi veya Elektronik raporlama işlev danışmanı [rolündeki](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) bir kullanıcının, yürütme sırasının biçim hiyerarşisindeki sıradan farklı olduğu bir sıra öğesini içeren bir ER biçimini nasıl yapılandırabileceği açıklanmaktadır.

Bu adımlar Microsoft Dynamics 365 Finance'teki **USMF** şirketinde gerçekleştirilebilir.

### <a name="prerequisites"></a>Önkoşullar

Bu örneği tamamlamak üzere aşağıdaki rollerden biri için Finance'teki **USMF** şirketine erişiminiz olmalıdır:

- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

[ER biçimindeki sıra öğelerinin yürütülmesini erteleme](er-defer-xml-element.md#Example) konusundaki örneği henüz tamamlamadıysanız, örnek ER çözümünün aşağıdaki [yapılandırmalarını](general-electronic-reporting.md#Configuration) indirin.

| İçerik açıklaması            | Dosya adı |
|--------------------------------|-----------|
| ER data model configuration    | [Model to learn deferred elements.version.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER model eşleme yapılandırması | [Mapping to learn deferred elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Başlamadan önce, örnek ER çözümünün de aşağıdaki yapılandırmasını indirip kaydetmeniz gerekir.

| İçerik açıklaması     |Dosya adı |
|-------------------------|----------|
| ER format configuration | [Format to learn deferred sequences.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a>Örnek ER yapılandırmalarını içe aktarma

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında **Ertelenmiş öğeleri öğrenme modeli** yoksa, ER veri modeli yapılandırmasını içe aktarın:

    1. **Exchange** 'i ve ardından **XML dosyasından yükle**'yi seçin.
    2. **Gözat**'ı seçin, **Model to learn deferred elements.1.xml** dosyasını bulup seçin ve **Tamam**'ı seçin.

4. Yapılandırma ağacında **Ertelenmiş öğeleri öğrenmek için eşleştirme** yapılandırması yoksa, ER modeli eşleştirme yapılandırmasını içe aktarın:

    1. **Exchange** 'i ve ardından **XML dosyasından yükle**'yi seçin.
    2. **Gözat**'ı seçin, **Mapping to learn deferred elements.1.1.xml** dosyasını bulup seçin ve **Tamam**'ı seçin.

5. ER biçimi yapılandırmasını içe aktarın:

    1. **Exchange** 'i ve ardından **XML dosyasından yükle**'yi seçin.
    2. **Gözat**'ı seçin, **Format to learn deferred sequences.1.1.xml** dosyasını bulup seçin ve **Tamam**'ı seçin.

6. Yapılandırma ağacında **Ertelenmiş öğeleri öğrenme modeli**'ni genişletin.
7. Yapılandırma ağacındaki içe aktarılan ER yapılandırmaları listesini inceleyin.

    ![Yapılandırmalar sayfasındaki içe aktarılan ER yapılandırmaları](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Bir yapılandırma sağlayıcısını etkinleştirme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasındaki **Yapılandırma sağlayıcıları** bölümünde, Litware, Inc. (`http://www.litware.com`) örnek şirketine ait [yapılandırma sağlayıcısının](general-electronic-reporting.md#Provider) listelendiğinden ve Etkin olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısı listede yoksa veya etkin olarak işaretli değilse [Bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](./tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları izleyin.

    ![Yerelleştirme yapılandırmaları sayfasındaki Litware, Inc. örnek şirketi](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>İçe aktarılan model eşleşmesini inceleme

Vergi hareketlerine erişmek ve erişilen verileri istek üzerine göstermek için yapılandırılan ER modeli eşleme bileşeninin ayarlarını inceleyin.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. **Yapılandırmalar** sayfasındaki yapılandırma ağacında, **Ertelenmiş öğeleri öğrenme modeli**'ni genişletin.
4. **Ertelenmiş öğeleri öğrenmek için eşleştirme** yapılandırmasını seçin.
5. Eşleme listesini açmak için **Tasarımcı**'yı seçin.
6. Eşleme ayrıntılarını gözden geçirmek için **Tasarımcı**'yı seçin.
7. **Ayrıntıları göster**'i seçin.
8. Vergi hareketlerine erişmek üzere yapılandırılan veri kaynaklarını inceleyin:

    - *Tablo kaydı* türündeki **Hareketler** verileri kaynağı, **TaxTrans** uygulama tablosunun kayıtlarına erişmek üzere yapılandırılmıştır.
    - *Hesaplanan alan* türündeki **Fişler** veri kaynağı, gerekli fiş kodlarını bir kayıt listesi olarak (**INV-10000349** ve **INV-10000350**) döndürmek üzere yapılandırılmıştır.
    - *Hesaplanan alan* türündeki **Filtre uygulanmış** veri kaynağı, **Hareketler** veri kaynağından yalnızca gerekli fişlerin vergi hareketlerini seçmek üzere yapılandırılmıştır.
    - Ters işaretli vergi değerini göstermek üzere, **Filtre uygulanmış** veri kaynağı için *Hesaplanan alan* türündeki **\$TaxAmount** alanı eklenmiştir.
    - *Gruplama ölçütü* türündeki **Gruplandırılmış** veri kaynağı, **Filtre uygulanmış** veri kaynağının filtre uygulanmış vergi hareketlerini gruplandırmak üzere yapılandırılmıştır.
    - **Gruplandırılmış** veri kaynağının **TotalSum** toplama alanı, o veri kaynağının tüm filtre uygulanmış vergi hareketleri için **Filtre uygulanmış** veri kaynağının **\$TaxAmount** alanının değerlerini özetlemek üzere yapılandırılmıştır.

        ![" GroupBy" parametrelerini düzenleme sayfasındaki TotalSum toplama alanı](./media/ER-DeferredSequence-GroupByParameters.png)

9. Yapılandırılmış veri kaynaklarının veri modeline nasıl bağlandığını ve bu kaynakların erişilen verileri bir ER biçiminde kullanılabilir hale getirmek için nasıl gösterdiklerini inceleyin:

    - **Filtre uygulamış** veri kaynağı, veri modelinin **Data.List** alanına bağlıdır.
    - **Filtre uygulamış** veri kaynağının **\$TaxAmount** alanı, veri modelinin **Data.List.Value** alanına bağlıdır.
    - **Gruplandırılmış** veri kaynağının **TotalSum** alanı, veri modelinin **Data.Summary.Total** alanına bağlıdır.

    ![Model eşleme tasarımcısı sayfası](./media/ER-DeferredSequence-ModelMapping.png)

10. **Model eşleme tasarımcısı** ve **Model eşlemeleri** sayfalarını kapatın.

### <a name="review-the-imported-format"></a>İçe aktarılan biçimi gözden geçirin.

1. **Yapılandırmalar** sayfasındaki yapılandırmalar ağacında **Ertelenmiş sıraları öğrenme biçimi** yapılandırmasını seçin.
2. Biçim ayrıntılarını incelemek için **Tasarımcı**'yı seçin.
3. **Ayrıntıları göster**'i seçin.
4. Vergi hareketlerinin ayrıntılarını içeren metin biçiminde bir giden belge oluşturmak üzere yapılandırılmış ER biçimi bileşenlerinin ayarlarını inceleyin:

    - **Rapor\\Satırları** sıra biçimi öğesi, giden belgeyi iç içe sıralı öğelerden (**Üst bilgi**, **Kayıt** ve **Özet**) oluşturulmuş tek bir satırla doldurmak üzere yapılandırılmıştır.

        ![Biçim tasarımcısı sayfasındaki Satırlar sıra biçimi öğesi ve iç içe öğeler](./media/ER-DeferredSequence-Format.png)

    - **Rapor\\Satırları\\Üst Bilgisi** sıra biçimi öğesi, giden belgeyi, işlemin başladığı tarih ve saati gösteren tek bir üst bilgi satırıyla doldurmak üzere yapılandırılmıştır.
    - **Rapor\\Satırlar\\Kayıt** sıra biçimi öğesi, giden belgeyi her bir vergi hareketinin ayrıntılarını gösteren tek bir satırla doldurmak üzere yapılandırılmıştır. Bu vergi hareketleri noktalı virgülle ayrılır.

        ![Ayırıcı olarak noktalı virgül kullanan kayıt sıra biçimi öğesi](./media/ER-DeferredSequence-Format1.png)

    - **Rapor\\Satırlar\\Özet** sıra biçimi öğesi, giden belgeyi, işlenmiş vergi hareketlerinden alınan vergi değerlerinin toplamını içeren tek bir özet satırıyla doldurmak üzere yapılandırılmıştır.

4. **Eşleme** sekmesinde, aşağıdaki ayrıntıları inceleyin:

    - Bir giden belgede tek satır oluşturmak için **Rapor\\Satırlar\\Üst Bilgi** öğesinin bir veri kaynağına bağlanması gerekmez.
    - **Prefix1** öğesi, eklenen satırın rapor üst bilgi satırı olduğunu belirtmek için **P1** simgeleri oluşturur.
    - **ExecutionDateTime** öğesi, üst bilgi satırının eklendiği tarih ve saati (milisaniyeler dahil) oluşturur.
    - **Rapor\\Satırlar\\Kayıt** öğesi, bağlı listeden her kayıt için tek bir satır oluşturmak amacıyla **model.Data.List** listesine bağlıdır.
    - **Prefix2** öğesi, eklenen satırın, vergi hareketi ayrıntılarına ilişkin olduğunu belirtmek için **P2** simgeleri oluşturur.
    - **TaxAmount** öğesi, geçerli vergi hareketinin vergi değerini oluşturmak için **model.Data.List.Value**'ya (göreli dizin yolu görünümünde **\@.Value** olarak gösterilir) bağlıdır.
    - **RunningTotal** öğesi, vergi değerlerinin çalışma toplamı için bir yer tutucudur. Bu öğe için hiçbir bağlama veya varsayılan değer yapılandırılmadığından, şu anda öğenin çıktısı yok.
    - **ExecutionDateTime** öğesi, geçerli hareketin bu raporda işlendiği tarih ve saati (milisaniyeler dahil) oluşturur.
    - Bir giden belgede tek satır oluşturmak için **Rapor\\Satırlar\\Özet** öğesinin bir veri kaynağına bağlanması gerekmez.
    - **Prefix3** öğesi, eklenen satırın, toplam vergi değerini içerdiğini belirtmek için **P3** simgeleri oluşturur.
    - **TotalTaxAmount** öğesi, işlenen vergi hareketlerinin vergi değerleri toplamını oluşturmak için **model.Data.Summary.Total**'a bağlıdır.
    - **ExecutionDateTime** öğesi, özet satırının eklendiği tarih ve saati (milisaniyeler dahil) oluşturur.

    ![Biçim tasarımcısı sayfasındaki Eşleme sekmesi](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>İçe aktarılan biçimi çalıştırma

1. **Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.
2. Web tarayıcısının sunduğu dosyayı indirin ve incelemek üzere açın.

    ![İndirilen dosya](./media/ER-DeferredSequence-Run.png)

22. özet satırının işlenen hareketler için vergi değerlerinin toplamını sunduğuna dikkat edin. Çünkü biçim, bu toplamı döndürmek için **model.Data.Summary.Total** bağını kullanmak üzer yapılandırılmıştır. Toplam, model eşleşmesini kullanan *GroupBy* türündeki **Gruplandırılmış** veri kaynağının **TotalSum** toplamını çağırarak hesaplanır. Bu toplamı hesaplamak için, model eşleme **Filtre uygulanmış** veri kaynağında seçilen tüm hareketlerin üzerinde yinelenir. Satır 21 ve satır 22'nin yürütme sürelerini karşılaştırarak, toplamın hesaplamasının 10 milisaniye (ms) sürdüğünü belirleyebilirsiniz. Satır 2 ve satır 21'nin yürütme sürelerini karşılaştırarak, tüm işlem satırlarının oluşturulmasının 7 milisaniye sürdüğünü belirleyebilirsiniz. Bu nedenle, toplam 17 milisaniye gerekmiştir.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Toplama işleminde, oluşturulan çıktının temel alınması için biçimi değiştirme

Hareketlerin hacmi, geçerli örnekteki hacimden çok büyükse, toplama süresi uzayarak performans sorunlarına neden olabilir. Biçimin ayarını değiştirerek, bu performans sorunlarının engellenmesine yardımcı olabilirsiniz. Rapora dahil etmek için vergi değerlerine eriştiğinizden, vergi değerlerini toplamak için bu bilgileri yeniden kullanabilirsiniz. Daha fazla bilgi için bkz. [Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma](./tasks/er-format-counting-summing-1.md).

1. **Biçim tasarımcısı** sayfasındaki **Biçim** sekmesinde, biçim ağacındaki **Rapor** dosyası öğesini seçin.
2. **Çıkış ayrıntılarını topla** seçeneğini **Evet** olarak ayarlayın. Bu biçimi, [Veri toplama](er-functions-category-data-collection.md) kategorisindeki yerleşik ER işlevleriyle erişilebilen bir veri kaynağı olarak mevcut bir raporun içeriğini kullanarak yapılandırabilirsiniz.
3. **Eşleme** sekmesinde **Rapor\\Satırlar** sıra öğesini seçin.
4. **Toplanan veri anahtarı adı** ifadesini `WsColumn` olarak yapılandırın.
5. **Toplanan veri anahtarı değeri** ifadesini `WsRow` olarak yapılandırın.

    ![Biçim tasarımcısı sayfasındaki Satırlar sırası öğesi](./media/ER-DeferredSequence-Format3.png)

6. **Rapor\\Satırlar\\Kayıt\\TaxAmount** sayısal öğesini seçin.
7. **Toplanan veri anahtarı adı** ifadesini `SummingAmountKey` olarak yapılandırın.

    ![Biçim tasarımcısı sayfasındaki TaxAmount sayısal öğesi](./media/ER-DeferredSequence-Format4.png)

    Bu ayarı, her işlenmiş vergi hareketinin vergi tutarının değeri A1 hücresinin değerine eklendiği bir sanal çalışma sayfasının karşılanması olarak değerlendirebilirsiniz.

8. **Rapor\\Satırlar\\Kayıt\\RunningTotal** sayısal öğesini ve ardından **Formülü düzenle**'yi seçin.
9. `SUMIF(SummingAmountKey, WsColumn, WsRow)` ifadesini yerleşik [SUMIF](er-functions-datacollection-sumif.md) ER işleviyle yapılandırın.
10. **Kaydet**'i seçin.

    ![SUMIF ifadesi](./media/ER-DeferredSequence-FormulaDesigner.png)

11. **Formül tasarımcısı** sayfasını kapatın.
12. **Kaydet** i ve ardından **Çalıştır**'ı seçin.
13. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredSequence-Run1.png)

    Satır 21, oluşturulan çıktıyı bir veri kaynağı olarak kullanarak, tüm işlem gören hareketler için hesaplanan vergi değerlerinin çalışma toplamını içerir. Bu veri kaynağı raporun başından başlar ve son vergi hareketi üzerinden devam eder. Satır 22, *GroupBy* türündeki veri kaynağını kullanarak model eşlemesinde hesaplanan tüm işlenmiş hareketler için vergi değerlerinin toplamını içerir. Bu değerlerin eşit olduğuna dikkat edin. Bu nedenle, **GroupBy** yerine çıktı tabanlı toplama kullanılabilir. Satır 2 ve satır 21'nin yürütme sürelerini karşılaştırarak, tüm işlem satırlarının oluşturulmasının ve toplama işleminin 9 milisaniye sürdüğünü belirleyebilirsiniz. Bu nedenle, vergi değerlerinin ayrıntılı satırlarının ve toplamının oluşturulması söz konusuyken, değiştirilen biçim, orijinal biçimden yaklaşık iki kat daha hızlıdır.

14. **Rapor\\Satırlar\\Özet\\TotalTaxAmount** sayısal öğesini ve ardından **Formülü düzenle**'yi seçin.
15. Varolan ifadenin yerine `SUMIF(SummingAmountKey, WsColumn, WsRow)` ifadesini girin.
16. **Kaydet** i ve ardından **Çalıştır**'ı seçin.
17. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredSequence-Run2.png)

    Son hareket ayrıntıları satırındaki vergi değerlerinin çalışma toplamının artık özet satırındaki toplama eşit olduğuna dikkat edin.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Çıkış tabanlı toplamın değerlerini rapor üst bilgisine koyma

Örneğin vergi değerleri toplamını raporunuzun üst bilgisinde sunmanız gerekiyorsa, biçiminizde değişiklik yapabilirsiniz.

1. **Biçim tasarımcısı** sayfasındaki **Biçim** sekmesinde **Rapor\\Satırlar\\Özet** sıra öğesini seçin.
2. **Yukarı taşı**'yı seçin.
3. **Kaydet** i ve ardından **Çalıştır**'ı seçin.
4. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredSequence-Run3.png)

    Özet satırı 2'deki vergi değerleri toplamının 0'a (sıfır) eşit olduğuna dikkat edin, çünkü bu toplam, oluşturulan çıktı temel alınarak hesaplanmıştır. Satır 2 oluşturulurken, oluşturulan çıktıda henüz hareket ayrıntılarını içeren satırlar yoktur. Bu biçimi, **Rapor\\Satırlar\\Kayıt** sıra öğesi tüm vergi hareketleri için çalıştırılana kadar **Rapor\\Satırlar\\Özet** sıra öğesinin yürütülmesini ertelemek üzere yapılandırabilirsiniz.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Hesaplanan toplamın kullanılmasını sağlamak için özet sırasının yürütülmesini erteleme

1. **Biçim tasarımcısı** sayfasındaki **Biçim** sekmesinde **Rapor\\Satırlar\\Özet** sıra öğesini seçin.
2. **Ertelenmiş yürütme** seçeneğini **Evet** olarak ayarlayın.

    ![Biçim tasarımcısı sayfasındaki Özet sıra öğesinin ertelenmiş yürütme seçeneği](./media/ER-DeferredSequence-Format5.png)

3. **Kaydet** i ve ardından **Çalıştır**'ı seçin.
4. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredSequence-Run4.png)

    **Rapor\\Satırlar\\Özet** sıra öğesi artık yalnızca üst öğesi olan **Rapor\\Satırlar** altında iç içe yuvalanmış diğer öğelerin tümü çalıştırıldıktan sonra çalıştırılır. Bu nedenle, bu öğe, **Rapor\\Satırlar\\Kayıt** sıra öğesi, **model.Data.List** veri kaynağının tüm vergi hareketleri için çalıştırıldıktan sonra çalıştırılır. Satır 1, 2 ve 3'ün ve son satır 22'nin yürütme süreleri bu olguyu ortaya koyar.

## <a name="additional-resources"></a>Ek kaynaklar

- [Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma](./tasks/er-format-counting-summing-1.md)
- [Performans sorunlarını gidermek için ER biçimi yürütülmesini izle](trace-execution-er-troubleshoot-perf.md)
- [ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]