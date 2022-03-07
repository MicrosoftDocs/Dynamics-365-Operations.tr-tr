---
title: Oluşturulan raporlarda Word içerik denetimlerini gizleme
description: Bu konu, içerik denetimlerinin gizlendiği Microsoft Word dosyaları olarak raporlar oluşturmak üzere elektronik raporlama (ER) biçiminin nasıl yapılandırılacağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562130"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>Oluşturulan raporlarda Word içerik denetimlerini gizleme

[!include [banner](../includes/banner.md)]

Raporları Microsoft Word belgeleri olarak oluşturmak için, raporlar için Word belgesi şeklinde bir şablon tasarlamanız gerekir. Bu şablon, çalışma zamanında doldurulacak veriler için yer tutucu olarak Word içerik denetimleri içermelidir. Raporlarınız için şablon olarak oluşturulan Word belgesini kullanmak için yeni bir [Elektronik raporlama (ER)](general-electronic-reporting.md) [çözümü](er-quick-start1-new-solution.md) [yapılandırabilirsiniz](er-design-configuration-word.md). Çözüm, ER [biçimi](general-electronic-reporting.md#FormatComponentOutbound) bileşeni içeren bir ER [yapılandırması](general-electronic-reporting.md#Configuration) içermelidir. Bu ER biçimi, rapor oluşturma için tasarlanmış şablonu kullanacak şekilde yapılandırılmalıdır.

Dynamics 365 Finance sürüm 10.0.6 ve sonrasında, oluşturulan belgelerdeki bazı Word içerik denetimlerini gizlemek için ER biçiminizde formüller yapılandırabilirsiniz.

Aşağıdaki adımlarda, sistem yöneticisine veya elektronik raporlama işlevsel Danışman rolüne atanan bir kullanıcının, Word dosyaları olarak raporlar oluşturan ve bir Word şablonu kullanılarak yapılandırılmış olan oluşturulan raporlarda bazı içerik denetimlerini gizleyen bir ER biçiminin nasıl yapılandırılabileceği açıklanmaktadır.

Bu adımlar GBSI şirketinde gerçekleştirilebilir.

## <a name="prerequisites"></a>Önkoşullar

Bu adımları tamamlamak için önce şu görev kılavuzlarındaki adımları tamamlamalısınız:

- [OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama](./tasks/er-design-reports-openxml-2016-11.md)
- [Word biçiminde raporlar oluşturmak için ER yapılandırmalarını Excel şablonlarıyla yeniden kullanma](./tasks/er-design-configuration-word-2016-11.md)

Bu görev kılavuzlarının adımlarını tamamladığınızda, aşağıdaki öğeler hazırlanır:

- Word biçiminde belge oluşturmak üzere yapılandırılan **örnek çalışma sayfası raporu** ER biçimi
- **Çalıştırılabilir** olarak işaretlenmiş **örnek çalışma sayfası raporu** ER biçiminin bir [taslak](general-electronic-reporting.md#component-versioning) versiyonu
- Satıcı ödeme işlemleri için **örnek çalışma sayfası raporu** ER biçimini kullanmak üzere yapılandırılan bir **elektronik** ödeme yöntemi

Ayrıca örnek rapor için aşağıdaki şablonu indirmeli ve kaydetmelisiniz:

- [Ödeme Raporunun Bağlı Şablonu 2 (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>İndirilen Word şablonunu inceleme

1. Word masaüstü uygulamasında, daha önce indirdiğiniz **SampleVendPaymDocReportBounded2.docx** şablon dosyasını açın.
2. Şablon dosyasının, işlenmiş ödemelerde karşılanan her bir para birimi kodu için toplam ödeme tutarlarını gösteren bir Özet bölümü içerdiğini doğrulayın.

    - Özet bölümü, Word belgesinin ayrı bir tablosunda bulunur.
    - Bu tablonun ilk satırı bölüm başlığı olarak tablo sütunları başlıklarını içerir.
    - Bu tablonun ikinci satırı, Bölüm ayrıntıları olarak tekrarlanan içerik denetimini içerir.
    - Bu içerik denetimi **Rapor** özel XML parçasının **summarylines** alanıyla eşleştirilir.
    - Bu eşlemeye dayalı olarak içerik denetimi, düzenlenebilir ER biçiminin **summarylines** öğesiyle ilişkilendirilir.

    > [!NOTE]
    > Tekrarlanan içerik denetimi, eşlendiği özel XML parçasının alanıyla eşleşen **summarylines** anahtarı tarafından etiketlenir.

    ![Word şablonu düzeni](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>Mevcut ER rapor yapılandırmasını seçme

Aşağıdaki adımlarda, daha önce sözü edilen görev kılavuzlarındaki adımları tamamladığınızda yapılandırdığınız varolan ER yapılandırmasını yeniden kullanabilirsiniz.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **Örnek çalışma sayfası raporu**'nu seçin.
4. Seçili ER biçiminin taslak sürümünü düzenlemek için **Tasarımcı**'yı seçin.

## <a name="replace-the-current-template-with-the-new-template"></a>Geçerli şablonu yeni şablon ile değiştirme

Şu anda, Word biçiminde çıktı oluşturmak için SampleVendPaymDocReportBounded.docx dosyası şablon olarak kullanılmaktadır. Aşağıdaki adımlarda bu Word şablonunu, daha önce indirdiğiniz SampleVendPaymDocReportBounded2.docx Word şablonuyla değiştireceksiniz.

1. **Biçim tasarımcısı** sayfasında, **Ekler**'i seçin.
2. **Ekler** sayfasında, mevcut şablonu kaldırmak için **Sil**'i seçin.
3. Silmeyi onaylamak için **Evet**'i seçin.
4. **Yeni** \> **Dosya**'yı seçin.
5. **Göz at**'ı seçin ve daha önce indirdiğiniz **SampleVendPaymDocReportBounded2.docx** dosyasını bulup seçin.
6. **Tamam**'ı seçin.
7. **Ekler** sayfasını kapatın.
8. **Biçim Tasarımcısı** sayfasında, **şablon** alanında **SampleVendPaymDocReportBounded2.docx** dosyasını girin veya seçin.

## <a name="run-the-format-to-create-word-output"></a>Word çıktısı oluşturmak için biçimi yürütme

1. **Borç hesapları** \> **Ödemeler** \> **Ödeme günlüğü**'ne gidin.
2. **Satıcı ödemeleri** sayfasında, **liste** sekmesinde, tüm ödemeleri seçin.
3. **Ödeme durumu** \> **Hiçbiri**'ni seçin.
4. **Ödemeleri oluştur**'u seçin.
5. **Ödeme yöntemi** alanında **Elektronik**'i seçin.
6. **Banka hesabı** alanında **GBSI OPER** öğesini seçin.
7. **Tamam**'ı seçin.
8. **Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin ve oluşturulan çıktıyı analiz edin.

    ![Satıcı ödemeleri sayfasındaki işlenecek ödemeler](./media/er-design-configuration-word-suppress-controls-image2.gif)

    Çıktı Word biçiminde sunulur ve Özet bölümünü içerir.

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>Özet bölümünü gizlemek için düzenlenebilir biçimi yapılandırma

Oluşturulan bir belgede Özet bölümünü gizlemek istiyorsanız, bu ER biçimini çalıştıran bir kullanıcının isteğine bağlı olarak, düzenlenebilir ER biçimini değiştirmelisiniz.

1. **Kuruluş Yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin ve düzenleme için ER biçiminin taslak sürümünü açın.
2. **Raporlama yapılandırmaları**'nı seçin. 
3. **Yapılandırmalar** sayfasında, yapılandırma ağacında, **Ödeme modeli** \> **Örnek çalışma sayfası raporu**'nu genişletin.
4. **Tasarımcı**’yı seçin.
5. **Biçim Tasarımcısı** sayfasında, **Word**'ü genişletin ve **summarylines**'ı seçin.
6. **Eşleme** sekmesinde, çalışma zamanında kullanıcıya Özet bölümünün gizlenip gizlenmeyeceğini sormak için yeni bir veri kaynağı ekleyin:

    1. **Kök ekle**'yi seçin.
    2. **Veri kaynağı ekle** iletişim kutusunda **Kullanıcı giriş parametresi veri kaynağı özellikleri** iletişim kutusunu açmak için **Genel\Kullanıcı girişi parametresi**'ni seçin.
    3. **Ad** alanına, **uipSuppress** yazın.
    4. **Etiket** alanına **Özet bölümünü gizle** yazın.
    5. **Operasyonlar veri türü adı** alanında, **NoYes** yazın veya girin.
    6. **Tamam**'ı seçin.

7. **NoYes** uygulama numaralandırmasının yeni bir veri kaynağını ekleyin:

    1. **Kök ekle**'yi seçin.
    2. **Veri kaynağı Ekle** iletişim kutusunda, **Dynamics 365 for Operations\Numaralandırma**'yı seçerek **'Numaralandırma'veri kaynağı özellikleri** iletişim kutusunu açın.
    3. **Ad** alanına, **enumNoYes** yazın.
    4. **Etiket** alanına **Seçenekleri gizle** yazın.
    5. **Operasyonlar veri türü adı** alanında, **NoYes** yazın veya girin.
    6. **Tamam**'ı seçin.

8. Seçili **summarylines** biçim öğesi için, seçili biçim öğesiyle ilişkilendirilmiş Word içerik denetiminin ne zaman gizleneceğini belirten formülü yapılandırın:

    1. **Eşleme** sekmesinde, **kaldırılan** bölümünde **[Formül Tasarımcısı sayfasını](general-electronic-reporting-formula-designer.md)** sayfasını açmak için **Düzenle**'yi seçin.
    2. **Formül** alanına, `uipSuppress = enumNoYes.Yes` formülünü girin.
    3. **Kaydet**'i seçin ve sonra **Formül tasarımcısı** sayfasını kapatın.

        > [!NOTE]
        > Bu formül oluşturulan belgeye, **diğer tüm biçim öğeleri çalıştırıldıktan sonra** uygulanacaktır. Bu formülü uygulamak için formülün yapılandırıldığı bir biçim öğesi (Bu örnekte **summarylines**) olarak etiketlenmiş bir Word içerik denetimi, oluşturulmuş bir belgede bulunur. Bu içerik denetimi, bulunduğu Word tablosu satırıyla birlikte tümüyle kaldırılır. Özet bölümünün ayrıntılar satırı oluşturulan belgeden kaldırılır.
        >
        > Tasarım zamanında, kullandığınız Word şablonunda hiçbir içerik denetiminin, **kaldırılmış** özelliğin yapılandırıldığı bir biçim öğesinin adıyla eşleşen bir etikete sahip olmamasına rağmen, bir biçim öğesi için **kaldırılmış** formülü yapılandırabilirsiniz. Tasarım zamanında biçimi doğruladığınızda, bu tutarsızlık hakkında bir [uyarı](er-components-inspections.md#i14) alırsınız.
        >
        > Çalışma zamanında, Word şablonunda kullandığınız herhangi bir içerik denetiminin, **kaldırılmış** özelliğinin yapılandırıldığı bir biçim öğesinin adıyla eşleşen bir etiketi yoksa bir özel durum oluşur.

    4. **Eşleme** sekmesinde, **kaldırılan** bölümünde, **Üst öğe ile** seçeneğini **Evet** olarak ayarlayın.

        > [!NOTE]
        > Özet bölüm detaylarının bulunduğu satırın üst nesnesi olarak tüm Word tablosunu kaldırmak için bu seçeneği **Evet** olarak ayarlamalısınız. Bu seçeneği **Hayır** olarak ayarlarsanız , bölüm başlığı satırı oluşturulan belgede kalır.

9. Düzenlenebilir biçime yaptığınız değişiklikleri kaydetmek için **Kaydet**'i seçin.

    ![Word biçiminde oluşturulan çıktı](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>Word çıktısı oluşturmak için değiştirilen biçimi yürütme

1. **Borç hesapları** \> **Ödemeler** \> **Ödeme günlüğü**'ne gidin.
2. Oluşturduğunuz ödeme günlüğünü seçin ve ardından **Satırlar**'ı seçin.
3. **Satıcı ödemeleri** sayfasında, tüm satırları seçin ve ardından **ödeme durumu** \> **Yok**'u seçin.
4. **Ödemeleri oluştur**'u seçin.
5. **Ödeme yöntemi** alanında **Elektronik**'i seçin.
6. **Banka hesabı** alanında **GBSI OPER** öğesini seçin.
7. **Tamam**'ı seçin.
8. **Elektronik rapor parametreleri** iletişim kutusunda **Özet bölümünü gizle** alanında **Evet**'i seçin.
9. **Tamam**'ı seçin ve oluşturulan çıktıyı analiz edin.

    ![Word biçiminde oluşturulan çıktı](./media/er-design-configuration-word-suppress-controls-image4.gif)

    Gizlenmiş olduğu için, çıktıda Özet bölümü bulunmadığına dikkat edin.

## <a name="additional-resources"></a>Ek kaynaklar

- [OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama](./tasks/er-design-reports-openxml-2016-11.md)
- [Word biçiminde raporlar oluşturmak için yeni ER yapılandırması tasarlama](er-design-configuration-word.md)
- [Word biçiminde raporlar oluşturmak için ER yapılandırmalarını Excel şablonlarıyla yeniden kullanma](./tasks/er-design-configuration-word-2016-11.md)
- [Çalışma zamanı sorunlarını önlemek için yapılandırılmış ER bileşenini denetleme](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]