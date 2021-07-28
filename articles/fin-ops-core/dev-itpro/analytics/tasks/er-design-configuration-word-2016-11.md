---
title: Word biçiminde raporlar oluşturmak için Excel şablonlarıyla ER yapılandırmalarını yeniden kullanma
description: Bu konuda, Excel çalışma kitapları olarak rapor oluşturmak üzere tasarlanmış rapor biçimlerinin, Word belgeleri olarak rapor oluşturmak üzere nasıl yapılandırılabileceği açıklanmaktadır.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d152449b55ab111cf5bac363b38d32c3658a56e3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359423"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>Word biçiminde raporlar oluşturmak için Excel şablonlarıyla ER yapılandırmalarını yeniden kullanma

[!include [banner](../../includes/banner.md)]

Microsoft Word belgeleri olarak rapor oluşturmak için yeni bir [Elektronik raporlama (ER)](../general-electronic-reporting.md) [biçimi](../general-electronic-reporting.md#FormatComponentOutbound) [yapılandırabilirsiniz](../er-design-configuration-word.md). Alternatif olarak, başlangıçta Excel çalışma kitabı olarak rapor üretmek üzere tasarlanan bir ER biçimini yeniden kullanabilirsiniz. Bu durumda, Excel şablonunu bir Word şablonuyla değiştirmelisiniz.

Aşağıdaki yordamlarda, Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolündeki bir kullanıcının, Excel dosyaları halinde rapor oluşturmak üzere tasarlanan bir ER biçimini yeniden kullanarak Word dosyası halinde rapor oluşturmak için ER biçimini nasıl yapılandırabileceği açıklanmaktadır.

Bu yordamlar, GBSI şirketinde gerçekleştirilebilir.

## <a name="prerequisites"></a>Önkoşullar

Bu yordamları tamamlamak için öncelikle [OPENXML biçiminde raporlar oluşturmak için bir ER yapılandırması tasarlama](er-design-reports-openxml-2016-11.md) görev kılavuzundaki adımları tamamlamanız gerekir.

Ayrıca örnek rapor için aşağıdaki şablonları indirmeli ve yerel olarak kaydetmelisiniz:

- [Ödeme Raporu Şablonu (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Ödeme Raporunun Bağlı Şablonu (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

Bu yordamlar, Dynamics 365 for Operations 1611 sürümüne (Kasım 2016) eklenmiş bir özellik içindir.

## <a name="select-the-existing-er-report-configuration"></a>Mevcut ER rapor yapılandırmasını seçme

1. Dynamics 365 Finance'te **Kuruluş yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Litware, Inc.** yapılandırma sağlayıcısının **Etkin** olarak seçildiğinden emin olun. Böyle değilse, [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md) görev kılavuzundaki adımları izleyin.
3. **Raporlama yapılandırmaları**'nı seçin. Rapor çıktısını OPENXML biçiminde oluşturmak için tasarlanmış olan mevcut ER yapılandırmasını yeniden kullanacaksınız.
4. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **Örnek çalışma sayfası raporu**'nu seçin.

    > [!NOTE]
    > Seçili ER biçiminin taslak sürümü, **Sürümler** hızlı sekmesinde düzenlenebilir.

5. **Tasarımcı**’yı seçin.
6. **Biçim tasarımcısı** sayfasında, kök biçim öğesinin başlığının Excel şablonunun şu anda kullanıldığını belirttiğini görebilirsiniz.

![Mevcut yapılandırmayı seçme.](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>İndirilen Word şablonunu inceleme

1. Word masaüstü uygulamasında, daha önce indirdiğiniz **SampleVendPaymDocReport.docx** şablon dosyasını açın.
2. Şablonun yalnızca ER çıkışı olarak oluşturmak istediğiniz belgenin düzenini içerdiğini doğrulayın.

![Masaüstü uygulamasındaki Word şablon düzeni.](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>Excel şablonunu Word şablonuyla değiştirin ve özel bir XML bölümü ekleyin

Şu anda, Excel belgesi OPENXML biçiminde çıktı üretmek için şablon olarak kullanılmaktadır. Bu şablonu, daha önce indirdiğiniz SampleVendPaymDocReport.docx Word şablon dosyasıyla değiştireceksiniz. Ayrıca özel bir XML bölümü ekleyerek Word şablonunu genişleteceksiniz.

1. Finance'teki **Biçim tasarımcısı** sayfasında yer alan **Biçim** sekmesinde **Ekler**'i seçin.
2. **Ekler** sayfasında, mevcut Excel şablonunu kaldırmak için **Sil**'i seçin. Değişikliği onaylamak için **Evet**'i seçin.
3. **Yeni** \> **Dosya**'yı seçin.

    > [!NOTE]
    > ER biçimlerinin şablonlarını depolamak için ER parametrelerinde [yapılandırılan](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) bir belge türünü seçmeniz gerekir.

4. **Göz at**'ı seçin ve daha önce indirdiğiniz **SampleVendPaymDocReport.docx** dosyasını bulup seçin.
5. **Tamam**'ı seçin.
6. **Ekler** sayfasını kapatın.
7. **Biçim tasarımcısı** sayfasındaki **Şablon** alanında, daha önce kullanılan Excel şablonu yerine Word şablonunu kullanmak için **SampleVendPaymDocReport.docx** dosyasını girin veya seçin.
8. **Kaydet**'i seçin.

    **Kaydet** eylemi, yapılandırma değişikliklerini depolamanın yanı sıra ekli Word şablonunu da güncelleştirir. Tasarlanan biçimin hiyerarşi yapısı, ekli Word belgesine **Rapor** adında yeni bir özel XML bölümü olarak eklenir. Ekli Word şablonu, ER çıkışı olarak oluşturulacak belgenin düzenini ve ER'nin çalışma zamanında bu şablona gireceği verilerin yapısını içerir.

9. Kök biçim öğesinin başlığının Word şablonunun şu anda kullanıldığını belirttiğini görebilirsiniz.

    ![Excel şablonunu Word şablonuyla değiştirme ve özel bir XML bölümü ekleme.](../media/er-design-configuration-word-2016-11-image03.gif)

10. **Biçim** sekmesinde, **Ekler**'i seçin.

Şimdi, **Rapor** özel XML bölümünün öğelerini Word belgesinin içerik denetimleriyle eşleyebilirsiniz.

[Özel XML bölümlerinin](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) öğeleriyle eşleştirilen [içerik denetimlerine](/office/client-developer/word/content-controls-in-word) sahip formlar olarak Word belgeleri tasarlama işlemi hakkında bilgi sahibiyseniz belgeyi oluşturmak için bir sonraki yordamda yer alan adımları tamamlayın. Daha fazla bilgi için bkz. [Kullanıcıların Word'de doldurduğu veya yazdırdığı formlar oluşturma](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b). Aksi takdirde, sonraki yordama geçin.

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>Özel XML bölümüne sahip bir Word belgesi alma ve veri eşleme işlemini gerçekleştirme

1. Finance'teki **Ekler** sayfasında, Finance'te seçili şablonu indirmek ve yerel olarak Word belgesi biçiminde saklamak için **Aç**'ı seçin.
3. Word masaüstü uygulamasında biraz önce indirdiğiniz belgeyi açın.
4. **Geliştirici** sekmesinde **XML Eşleme Bölmesi**'ni seçin.

    > [!NOTE]
    > **Geliştirici** sekmesi şeritte görüntülenmezse eklemek için şeridi özelleştirin.

5. **XML Eşleme** bölmesindeki **Özel XML Bölümü** alanında **Rapor** özel XML bölümünü seçin.
6. Seçili **Rapor** özel XML bölümü ile Word belgesinin içerik denetimlerini eşleyin.
7. Güncelleştirilmiş Word belgesini yerel olarak **SampleVendPaymDocReportBounded.docx** adıyla kaydedin.

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Özel XML bölümünün içerik denetimleriyle eşlendiği Word şablonunu gözden geçirme

1. Word masaüstü uygulamasında **SampleVendPaymDocReportBounded.docx** şablon dosyasını açın.
2. Şablonun ER çıkışı olarak oluşturmak istediğiniz belgenin düzenini içerdiğini doğrulayın. Çalışma zamanında ER'nin bu şablona gireceği veriler için yer tutucu olarak kullanılan içerik denetimleri, **Rapor** özel XML bölümü öğeleri ile Word belgesinin içerik denetimleri arasında yapılandırılan eşlemelere bağlıdır.

![Masaüstü uygulamasındaki Word şablonunun önizlemesi.](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>Özel XML bölümünün içerik denetimleriyle eşlendiği Word şablonunu indirme

1. Finance'teki **Ekler** sayfasında, **Rapor** özel XML bölümü öğeleri ve içerik denetimleri arasında eşleme olmayan Word şablonunu kaldırmak için **Sil**'i seçin. Değişikliği onaylamak için **Evet**'i seçin.
2. **Rapor** özel XML bölümü öğeleri ve içerik denetimleri arasında eşleme içeren yeni bir şablon dosyası eklemek için **Yeni** \> **Dosya**'yı seçin.

    > [!NOTE]
    > ER biçimlerinin şablonlarını depolamak için ER parametrelerinde [yapılandırılan](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) bir belge türünü seçmeniz gerekir.

3. **Göz at**'ı seçin ve ardından indirdiğiniz veya [Özel XML bölümüne sahip bir Word belgesi alma ve veri eşleme işlemini gerçekleştirme](#get-word-doc) bölümündeki yordamı tamamlayarak hazırladığınız **SampleVendPaymDocReportBounded.docx** dosyasını seçin.
4. **Tamam**'ı seçin.
5. **Ekler** sayfasını kapatın.
6. **Biçim tasarımcısı** sayfasındaki **Şablon** alanında az önce indirdiğiniz belgeyi seçin.
7. **Kaydet**'i seçin.
8. **Biçim tasarımcısı** sayfasını kapatın.

## <a name="mark-the-configured-format-as-runnable"></a>Yapılandırılmış biçimi çalıştırılabilir olarak işaretleme

Düzenlenebilir biçimin taslak sürümünü çalıştırmak için sürümü [çalıştırılabilir](../er-quick-start2-customize-report.md#MarkFormatRunnable) hale getirmeniz gerekir.

1. Finance'te **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
2. **Kullanıcı parametreleri** iletişim kutusunda, **Çalıştırma ayarları** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.
3. Geçerli sayfayı düzenlemeye hazır hale getirmek için gerektiğinde **Düzenle**'yi seçin.
4. Seçili durumdaki **Örnek çalışma sayfası** yapılandırması için **Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın.
5. **Kaydet**'i seçin.

## <a name="run-the-format-to-create-output-in-word-format"></a>Word biçiminde çıktı oluşturmak için biçimi çalıştırma

1. Finance'te **Borç hesapları** \> **Ödemeler** \> **Ödeme günlüğü**'ne gidin.
2. Daha önce girmiş olduğunuz bir ödeme günlüğünde **Satırlar**'ı seçin.
3. **Satıcı ödemeleri** sayfasında, ızgaradaki tüm satırları seçin.
4. **Ödeme durumu** \> **Hiçbiri**'ni seçin.

    ![Satıcı ödemeleri sayfasındaki işlenecek ödemeler.](../media/er-design-configuration-word-2016-11-image05.png)

5. Eylem bölmesinde, **Ödeme oluştur**'u seçin.
6. Gösterilen iletişim kutusunda şu adımları izleyin:

    1. **Ödeme yöntemi** alanında **Elektronik**'i seçin.
    2. **Banka hesabı** alanında **GBSI OPER** öğesini seçin.
    3. **Tamam**'ı seçin.

7. **Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin.
8. Oluşturulan çıktı, Word biçiminde sunulur ve işlenen ödemelerin ayrıntılarını içerir. Oluşturulan çıktıyı analiz edin.

    ![Word biçiminde oluşturulan çıktı.](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>Ek kaynaklar

- [Word biçiminde raporlar oluşturmak için yeni ER yapılandırması tasarlama](../er-design-configuration-word.md)
- [Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
