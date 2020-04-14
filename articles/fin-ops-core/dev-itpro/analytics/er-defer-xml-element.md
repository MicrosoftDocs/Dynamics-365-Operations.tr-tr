---
title: ER biçimindeki XML öğelerinin yürütülmesini erteleme
description: Bu konu, bir Elektronik raporlama (ER) biçimindeki bir XML öğesinin yürütülmesinin nasıl erteleneceğini açıklamaktadır.
author: NickSelin
manager: kfend
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58381f491cda199d77e555e5d3da04714b6a5f8f
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138935"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>ER biçimindeki XML öğelerinin yürütülmesini erteleme

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Genel Bakış

XML biçiminde giden belgeleri oluşturmak amacıyla kullanılan bir ER çözümünün [biçim bileşenini](general-electronic-reporting.md#FormatComponentOutbound) [yapılandırmak](./tasks/er-format-configuration-2016-11.md) için [Elektronik raporlama (ER)](general-electronic-reporting.md) çerçevesinin Operations tasarımcısını kullanabilirsiniz. Yapılandırılmış biçim bileşeninin hiyerarşik yapısı, çeşitli türlerdeki biçim öğelerinden oluşur. Bu biçim öğeleri, oluşturulan belgeleri gerekli bilgilerle çalışma zamanında doldurmak için kullanılır. Varsayılan olarak, bir ER biçimi çalıştırdığınızda, biçim öğeleri, biçim hiyerarşisinde göründükleri sırayla çalıştırılır: bire tek, üstten alta doğru. Ancak, tasarım sırasında, yapılandırılan biçim bileşeninin herhangi bir XML öğesinin yürütme sırasını değiştirebilirsiniz.

Yapılandırılan biçimdeki bir XML öğesi için <a name="DeferredXmlElementExecution"></a>**Ertelenmiş yürütme** seçeneğini etkinleştirerek, o öğenin yürütülmesini erteleyebilirsiniz. Bu durumda, öğenin üst öğesinin tüm diğer öğeleri çalıştırılıncaya kadar öğe çalıştırılmaz.

Bu özellik hakkında daha fazla bilgi edinmek için bu konudaki örneği tamamlayın.

## <a name="limitations"></a>Sınırlamalar

**Ertelenmiş yürütme** seçeneği yalnızca XML biçiminde **giden** belgeleri oluşturmak için kullanılan bir ER biçimi için yapılandırılmış XML öğeleri için desteklenir.

**Ertelenmiş yürütme** seçeneği yalnızca bir başka XML öğesi içinde bulunan XML öğeleri için desteklenir. Bu nedenle, başka biçim öğeleri türlerinde yer alan (örneğin bir **XML sequence** öğesindeki) XML öğelerine uygulanamaz.

**Dosyayı böl** seçeneği **Evet** olarak ayarlandığı zaman, **Ertelenmiş yürütme** seçeneği **Ortak\\Dosya** biçim öğesinde bulunan XML öğeleri için desteklenmez. XML dosyalarının nasıl bölüneceği hakkında daha fazla bilgi için bkz. [Oluşturulan XML dosyalarını dosya boyutu ve içerik miktarına göre bölme](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Örneğin: Bir ER biçimindeki bir XML öğesinin yürütülmesini erteleme

Aşağıdaki adımlarda, Sistem Yöneticisi veya Elektronik raporlama işlev danışmanı [rolündeki](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) bir kullanıcının, yürütme sırasının biçim hiyerarşisindeki sıradan farklı olduğu bir XML öğesini içeren bir ER biçimini nasıl yapılandırabileceği açıklanmaktadır.

Bu adımlar Microsoft Dynamics 365 Finance'teki **USMF** şirketinde gerçekleştirilebilir.

### <a name="prerequisites"></a>Önkoşullar

Bu örneği tamamlamak üzere aşağıdaki rollerden biri için Finance'teki **USMF** şirketine erişiminiz olmalıdır:

- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

[ER biçimindeki XML öğelerinin yürütülmesini erteleme](er-defer-sequence-element.md#Example) konusundaki örneği henüz tamamlamadıysanız, örnek ER çözümünün aşağıdaki [yapılandırmalarını](general-electronic-reporting.md#Configuration) indirin.

| İçerik açıklaması            | Dosya adı |
|--------------------------------|-----------|
| ER data model configuration    | [Model to learn deferred elements.version.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER model eşleme yapılandırması | [Mapping to learn deferred elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Başlamadan önce, örnek ER çözümünün de aşağıdaki yapılandırmasını indirip yerel bilgisayarınıza kaydetmeniz gerekir.

| İçerik açıklaması     | Dosya adı |
|-------------------------|-----------|
| ER biçim yapılandırması | [Format to learn deferred XML elements.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

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
    2. **Gözat**'ı seçin, **Format to learn deferred XML elements.1.1.xml** dosyasını bulup seçin ve **Tamam**'ı seçin.

6. Yapılandırma ağacında **Ertelenmiş öğeleri öğrenme modeli**'ni genişletin.
7. Yapılandırma ağacındaki içe aktarılan ER yapılandırmaları listesini inceleyin.

    ![Yapılandırmalar sayfasındaki içe aktarılan ER yapılandırmaları](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Bir yapılandırma sağlayıcısını etkinleştirme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasındaki **Yapılandırma sağlayıcıları** bölümünde, Litware, Inc. (`http://www.litware.com`) örnek şirketine ait [yapılandırma sağlayıcısının](general-electronic-reporting.md#Provider) listelendiğinden ve Etkin olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısı listede yoksa veya etkin olarak işaretli değilse [Bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](./tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları izleyin.

    ![Yerelleştirme yapılandırmaları sayfasındaki Litware, Inc. örnek şirketi](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

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

        ![" GroupBy" parametrelerini düzenleme sayfasındaki TotalSum toplama alanı](./media/ER-DeferredXml-GroupByParameters.png)

9. Yapılandırılmış veri kaynaklarının veri modeline nasıl bağlandığını ve bu kaynakların erişilen verileri bir ER biçiminde kullanılabilir hale getirmek için nasıl gösterdiklerini inceleyin:

    - **Filtre uygulamış** veri kaynağı, veri modelinin **Data.List** alanına bağlıdır.
    - **Filtre uygulamış** veri kaynağının **\$TaxAmount** alanı, veri modelinin **Data.List.Value** alanına bağlıdır.
    - **Gruplandırılmış** veri kaynağının **TotalSum** alanı, veri modelinin **Data.Summary.Total** alanına bağlıdır.

    ![Model eşleme tasarımcısı sayfası](./media/ER-DeferredXml-ModelMapping.png)

10. **Model eşleme tasarımcısı** ve **Model eşlemeleri** sayfalarını kapatın.

### <a name="review-the-imported-format"></a>İçe aktarılan biçimi gözden geçirin.

1. **Yapılandırmalar** sayfasındaki yapılandırmalar ağacında **Ertelenmiş XML öğelerini öğrenme biçimi** yapılandırmasını seçin.
2. Biçim ayrıntılarını incelemek için **Tasarımcı**'yı seçin.
3. **Ayrıntıları göster**'i seçin.
4. Vergi hareketlerinin ayrıntılarını içeren XML biçiminde bir giden belge oluşturmak üzere yapılandırılmış ER biçimi bileşenlerinin ayarlarını inceleyin:

    - **Rapor\\İleti** XML öğesi, giden belgeyi iç içe XML öğelerini (**Üst bilgi**, **Kayıt** ve **Özet**) içeren tek bir düğümle doldurmak üzere yapılandırılmıştır.
    - **Rapor\\İleti\\Üst Bilgi** XML öğesi, giden belgeyi, işlemin başladığı tarih ve saati gösteren tek bir üst bilgi düğümüyle doldurmak üzere yapılandırılmıştır.
    - **Rapor\\İleti\\Kayıt** XML öğesi, giden belgeyi tek bir vergi hareketinin ayrıntılarını gösteren tek bir kayıt düğümüyle doldurmak üzere yapılandırılmıştır.
    - **Rapor\\İleti\\Özet** XML öğesi, giden belgeyi, işlenmiş vergi hareketlerinden alınan vergi değerlerinin toplamını içeren tek bir özet düğümüyle doldurmak üzere yapılandırılmıştır.

    ![Biçim tasarımcısı sayfasındaki İleti XML öğesi ve iç içe XML öğeleri](./media/ER-DeferredXml-Format.png)

5. **Eşleme** sekmesinde, aşağıdaki ayrıntıları inceleyin:

    - Bir giden belgede tek bir düğüm oluşturmak için **Rapor\\İleti\\Üst Bilgi** öğesinin bir kaynağa bağlanması gerekmez.
    - **ExecutionDateTime** özniteliği, üst bilgi düğümünün eklendiği tarih ve saati (milisaniyeler dahil) oluşturur.
    - **Rapor\\İleti\\Kayıt** öğesi, bağlı listeden her kayıt için tek bir kayıt düğümü oluşturmak amacıyla **model.Data.List** listesine bağlıdır.
    - **TaxAmount** özniteliği, geçerli vergi hareketinin vergi değerini oluşturmak için **model.Data.List.Value**'ya (göreli dizin yolu görünümünde **\@.Value** olarak gösterilir) bağlıdır.
    - **RunningTotal** özniteliği, vergi değerlerinin çalışma toplamı için bir yer tutucudur. Bu öznitelik için hiçbir bağlama veya varsayılan değer yapılandırılmadığından, şu anda öğenin çıktısı yok.
    - **ExecutionDateTime** özniteliği, geçerli hareketin bu raporda işlendiği tarih ve saati (milisaniyeler dahil) oluşturur.
    - Bir giden belgede tek düğüm oluşturmak için **Rapor\\İleti\\Özet** öğesinin bir veri kaynağına bağlanması gerekmez.
    - **TotalTaxAmount** özniteliği, işlenen vergi hareketlerinin vergi değerleri toplamını oluşturmak için **model.Data.Summary.Total**'a bağlıdır.
    - **ExecutionDateTime** özniteliği, özet düğümünün eklendiği tarih ve saati (milisaniyeler dahil) oluşturur.

    ![Biçim tasarımcısı sayfasındaki Eşleme sekmesi](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>İçe aktarılan biçimi çalıştırma

1. **Biçim tasarımcısı** sayfasında, **Çalıştır**'ı seçin.
2. Web tarayıcısının sunduğu dosyayı indirin ve incelemek üzere açın.

    ![İndirilen dosya](./media/ER-DeferredXml-Run.png)

Özet düğümünün işlenen hareketler için vergi değerlerinin toplamını sunduğuna dikkat edin. Çünkü biçim, bu toplamı döndürmek için **model.Data.Summary.Total** bağını kullanmak üzer yapılandırılmıştır. Toplam, model eşleşmesindeki *GroupBy* türünde **Gruplandırılmış** veri kaynağının **TotalSum** toplamını çağırarak hesaplanır. Bu toplamı hesaplamak için, model eşleme **Filtre uygulanmış** veri kaynağında seçilen tüm hareketlerin üzerinde yinelenir. Özet düğümünün ve son kayıt düğümünün yürütme sürelerini karşılaştırarak, toplam hesaplamasının 12 milisaniye (ms) olduğunu belirleyebilirsiniz. İlk ve son kayıt düğümlerinin yürütme sürelerini karşılaştırarak, tüm kayıt düğümlerini oluşturmanın 9 milisaniye sürdüğünü belirleyebilirsiniz. Bu nedenle, toplam 21 milisaniye gerekmiştir.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Hesaplamada, oluşturulan çıktının temel alınması için biçimi değiştirme

Hareketin hacmi, geçerli örnekteki hacimden çok büyükse, hesaplama süresi uzayarak performans sorunlarına neden olabilir. Biçimin ayarını değiştirerek, bu performans sorunlarının engellenmesine yardımcı olabilirsiniz. Rapora dahil etmek için vergi değerlerine eriştiğinizden, vergi değerlerini hesaplamak için bu bilgileri yeniden kullanabilirsiniz. Daha fazla bilgi için bkz. [Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma](./tasks/er-format-counting-summing-1.md).

1. **Biçim tasarımcısı** sayfasındaki **Biçim** sekmesinde, biçim ağacındaki **Rapor** dosyası öğesini seçin.
2. **Çıkış ayrıntılarını topla** seçeneğini **Evet** olarak ayarlayın. Bu biçimi, [Veri toplama](er-functions-category-data-collection.md) kategorisindeki yerleşik ER işlevleriyle erişilebilen bir veri kaynağı olarak, oluşturulmuş bir raporun içeriğini kullanarak yapılandırabilirsiniz.
3. **Eşleme** sekmesinde **Rapor\\İleti\\Kayıt** XML öğesini seçin.
4. **Toplanan veri anahtarı adı** ifadesini `WsColumn` olarak yapılandırın.
5. **Toplanan veri anahtarı değeri** ifadesini `WsRow` olarak yapılandırın.

    ![Biçim tasarımcısı sayfasındaki Kayıt XML öğesi](./media/ER-DeferredXml-Format3.png)

6. **Rapor\\İleti\\Kayıt\\TaxAmount** özniteliğini seçin.
7. **Toplanan veri anahtarı adı** ifadesini `SummingAmountKey` olarak yapılandırın.

    ![Biçim tasarımcısı sayfasındaki TaxAmount özniteliği](./media/ER-DeferredXml-Format4.png)

    Bu ayarı, her işlenmiş vergi hareketinin vergi tutarının değeri A1 hücresinin değerine eklendiği bir sanal çalışma sayfasının karşılanması olarak değerlendirebilirsiniz.

8. **Rapor\\İleti\\Kayıt\\RunningTotal** özniteliğini ve ardından **Formülü düzenle**'yi seçin.
9. `SUMIF(SummingAmountKey, WsColumn, WsRow)` ifadesini yerleşik [SUMIF](er-functions-datacollection-sumif.md) ER işleviyle yapılandırın ve ardından **Kaydet**'i seçin.

    ![SUMIF ifadesi](./media/ER-DeferredXml-FormulaDesigner.png)

10. **Formül tasarımcısı** sayfasını kapatın.
11. **Kaydet**i ve ardından **Çalıştır**'ı seçin.
12. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredXml-Run1.png)

    Son kayıt düğümü, oluşturulan çıktıyı bir veri kaynağı olarak kullanarak, tüm işlem gören hareketler için hesaplanan vergi değerlerinin çalışma toplamını içerir. Bu veri kaynağı raporun başından başlar ve son vergi hareketi üzerinden devam eder. Özet düğümü, *GroupBy* türündeki veri kaynağını kullanarak model eşlemesinde hesaplanan tüm işlenmiş hareketler için vergi değerlerinin toplamını içerir. Bu değerlerin eşit olduğuna dikkat edin. Bu nedenle, **GroupBy**yerine çıktı tabanlı toplama kullanılabilir. İlk kayıt düğümü ve özet düğümü yürütme sürelerini karşılaştırarak, tüm kayıt düğümlerini oluşturma ve toplama işlemlerinin 11 milisaniye sürdüğünü belirleyebilirsiniz. Bu nedenle, vergi değerlerinin kayıt düğümlerinin ve toplamının oluşturulması söz konusuyken, değiştirilen biçim, orijinal biçimden yaklaşık iki kat daha hızlıdır.

13. **Rapor\\İleti\\Özet\\TotalTaxAmount** özniteliğini ve ardından **Formülü düzenle**'yi seçin.
14. Varolan ifadenin yerine `SUMIF(SummingAmountKey, WsColumn, WsRow)` ifadesini girin.
15. **Kaydet**i ve ardından **Çalıştır**'ı seçin.
16. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredXml-Run2.png)

    Son kayıt düğümündeki vergi değerlerinin çalışma toplamının artık özet düğümündeki toplama eşit olduğuna dikkat edin.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Çıkış tabanlı toplamın değerlerini rapor üst bilgisine koyma

Örneğin vergi değerleri toplamını raporunuzun üst bilgisinde sunmanız gerekiyorsa, biçiminizde değişiklik yapabilirsiniz.

1. **Biçim tasarımcısı** sayfasındaki **Biçim** sekmesinde **Rapor\\İleti\\Özet** XML öğesini seçin.
2. **Yukarı taşı**'yı seçin.
3. **Kaydet**i ve ardından **Çalıştır**'ı seçin.
4. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredXml-Run3.png)

    Özet düğümündeki vergi değerleri toplamının 0'a (sıfır) eşit olduğuna dikkat edin, çünkü bu toplam, oluşturulan çıktı temel alınarak hesaplanmıştır. İlk kayıt düğümü oluşturulurken, oluşturulan çıktıda henüz hareket ayrıntılarını içeren kayıt düğümleri yoktur. Bu biçimi, **Rapor\\İleti\\Kayıt** öğesi tüm vergi hareketleri için çalıştırılana kadar **Rapor\\İleti\\Özet** öğesinin yürütülmesini ertelemek üzere yapılandırabilirsiniz.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Hesaplanan toplamın kullanılmasını sağlamak için özet XML öğesinin yürütülmesini erteleme

1. **Biçim tasarımcısı** sayfasındaki **Biçim** sekmesinde **Rapor\\İleti\\Özet** XML öğesini seçin.
2. **Ertelenmiş yürütme** seçeneğini **Evet** olarak ayarlayın.

    ![Biçim tasarımcısı sayfasındaki Özet XML öğesinin ertelenmiş yürütme seçeneği](./media/ER-DeferredXml-Format5.png)

3. **Kaydet**i ve ardından **Çalıştır**'ı seçin.
4. Web tarayıcısının sunduğu dosyayı indirin ve inceleyin.

    ![İndirilen dosya](./media/ER-DeferredXml-Run4.png)

    **Rapor\\İleti\\Özet** öğesi artık yalnızca üst öğesi olan **Rapor\\İleti** altında iç içe yuvalanmış diğer öğelerin tümü çalıştırıldıktan sonra çalıştırılır. Bu nedenle, bu öğe, **Rapor\\İleti\\Kayıt** öğesi, **model.Data.List** veri kaynağının tüm vergi hareketleri için çalıştırıldıktan sonra çalıştırılır. İlk ve son kayıt düğümlerinin ve üst bilgi ve özet düğümlerin yürütme süreleri bu olguyu ortaya koyar.

## <a name="additional-resources"></a>Ek kaynaklar

- [Sayım ve toplama işlemlerini yapmak için biçimi yapılandırma](./tasks/er-format-counting-summing-1.md)
- [Performans sorunlarını gidermek için ER biçimi yürütülmesini izle](trace-execution-er-troubleshoot-perf.md)
- [ER biçimindeki sıra öğelerinin yürütülmesini erteleme](er-defer-sequence-element.md#Example)
