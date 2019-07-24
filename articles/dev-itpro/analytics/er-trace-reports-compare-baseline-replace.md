---
title: Oluşturulan ER raporları sonuçlarının izlenmesi ve temel değerlerle karşılaştırılmasına ilişkin geliştirmeler
description: Bu konu, 10.0.3 (Haziran 2019) sürümünde ER temel özelliklerinin Microsoft Dynamics 365 for Finance and Operations'da nasıl geliştirildiği hakkında bilgi sağlar.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700694"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a>Oluşturulan ER raporları sonuçlarının izlenmesi ve temel değerlerle karşılaştırılmasına ilişkin geliştirmeler

[!include[banner](../includes/banner.md)]

Bu konuda, Elektronik raporlama (ER) çerçevesinin temel özelliğinde yapılan ilk iyileştirmeler kümesi açıklanmaktadır. Bu iyileştirmeler Microsoft Dynamics 365 for Finance and Operations 10.0.3 (Haziran 2019) sürümünde ve sonrasında kullanılabilir.

## <a name="automate-the-setting-of-baseline-rules"></a>Temel kuralları ayarını otomatikleştirme

[Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) konusu ER formatındaki uygulamalar hakkında bilgi toplamak için ER çerçevesini nasıl yapılandıracağınızı ve bu uygulamaların sonuçlarını nasıl değerlendireceğinizi açıklar. Bu konudaki örnekte, tamamlanması gereken adımlar gösterilmektedir.

Adımlara bir kaç örnek:

- Giden dosya oluşturmak için bir ER biçimi çalıştırın ve dosyayı yerel olarak depolayın.
- Yerel olarak depolanan dosyayı bir ER biçimi için eklenmiş olan temel bir ek olarak ekleyin.
- Eklenen temel için bir temel kuralı yapılandırın. Bu yapılandırma aşağıdaki adımları içerir:

    - Giden dosya oluşturmak için kullanılan bir ER biçimi öğesi belirtin.
    - Oluşturulan giden dosyaya başvuran eki seçin.

> [!NOTE]
> Yeni ER özellikleri otomatik olmasını etkinleştirse bile bu adımların el ile gerçekleştirilmesi gerekir. Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Örnek: Temel kurallar ayarını otomatikleştirme

Bu örnekteki adımları tamamlamak için ilk önce [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) yukardaki "Add a new baseline for a designed ER format" bölümünün adımlarını tamamlamalısınız.

### <a name="review-added-baseline"></a>Eklenen temeli inceleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Temelleri** seçin.

    > [!NOTE]
    > Eylem Bölmesi'ndeki **Temeller** düğmesi yalnızca **Şirket içi hata ayıklama modu**'nda ER kullanıcı parametresi açıldığında kullanılabilir.

Temel, seçilmiş **ER temellerini öğrenme biçimi** formatında eklendi ancak temel kuralları bu temel için henüz eklenmedi.

![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline2.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")

### <a name="make-a-new-baseline-rule"></a>Yeni temel kuralı oluştur

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.
3. Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.
4. **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
5. **Kimlik Gir** alanına, **1** yazın.
6. **Temel dosyaları oluştur** seçeneğini **Evet** olarak ayarlayın.
7. **Tamam**'ı seçin.

    ![Elektronik rapor parametreleri iletişim kutusu](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Elektronik rapor parametreleri iletişim kutusu ekran görüntüsü")

8. **Temelleri** seçin.

    ![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")

    Oluşturulan giden dosya otomatik olarak yürütülen ER biçiminin temeline iliştirildi. Temel kuralı bu temele otomatik olarak eklendi ve eklenen dosyaya referans da içeriyor.

9. **Ad** alanına, **Temel 1** yazın.
10. **Dosya adı maskesi** alanında **.xml** girin.
11. **Kaydet**'i seçin.

### <a name="run-the-format"></a>Biçimi çalıştır

Artık [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) konusunun örneğindeki kalan adımları, "Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme" bölümünden başlayarak tamamlamaya hazırsınız.

> [!NOTE]
> **Temel** hızlı sekmesinde otomatik olarak eklenen temel kurallarını sildiğinizde başvurulan ek otomatik olarak silinmez.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Temeli, ER çıktısının sürekli değişen kısımlarını yok sayacak şekilde yapılandırma

Bir ER biçimi, biçim çalıştırıldığında değiştirilen bilgileri içerecek şekilde tasarlandığında, oluşturulan sonuçları temel değerleriyle karşılaştırmak üzere ER temel özelliğini kullanması için biçim gerekir. Örneğin, bilgi işleme tarihi ve saati ya da üretilen bir belgenin farklı biçimlerdeki (genel benzersiz kimlik tanımlayıcı\[GUID\], vb.) benzersiz kimlik tanımlayıcısı olabilir. Yeni ER Me özellikleri temel kuralını, biçim yürütmesinin sonuçlarıyla temel değerlerini karşılaştırmak amacıyla kullanırken, bir ER biçiminin değiştirilebilir öğelerini yoksaymak için yapılandırmanıza olanak sağlar. Bu özellik hakkında daha fazla bilgi edinmek için aşağıdaki örneği tamamlayın.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Örnek: Temeli, ER çıktısının sürekli değişen kısımlarını yoksayacak şekilde yapılandırma

Bu örnekteki adımları tamamlamak için ilk önce [Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md) konusunun örneklerinin adımlarını tamamlamalısınız.

### <a name="modify-a-configured-er-format"></a>Yapılandırılmış ER biçimini değiştirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.
3. Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.
4. **Tasarımcı**’yı seçin.
5. Ağaçta **Output\\Document**'i seçin.
6. **Ekle**'yi seçin.
7. Açılan iletişim kutusunda, ağaçta **XML\\Attribute** öğesini seçin.
8. **Ad** alanına **ProcessingDateTime** girin.
9. **Tamam**'ı seçin.
10. Ağaçtaki**Eşleştirme** sekmesinde **Çıkış\\Belge\\ProcessingDateTime**'ı seçin.
11. **Formül düzenle**’yi seçin.
12. **Formül** alanına şu ifadeyi girin: **DATETIMEFORMAT(NOW(), "O")**
13. **Kaydet**i seçin ve sonra **Test et**'i seçin.
14. Yapılandırılan ifadeyi yeniden test etmek için tekrar **Test et**'i seçin.

    ![Formül tasarımcı sayfası](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Formül tasarımcı sayfası ekran görüntüsü")

    > [!NOTE]
    > **Test sonucu** sekmesi, yapılandırılan ifadenin her çağrıldığında farklı bir tarih ve saat değeri döndürdüğünü gösterir.

15. **Formül tasarımcısı** sayfasını kapatın ve sonra **Kaydet**'i seçin.

    ![Biçim tasarımcı sayfası](media/GER-BaselineSample-FormatMappingDesign2.PNG "Biçim tasarımcı sayfası ekran görüntüsü")

16. **Biçim tasarımcısı** sayfasını kapatın.

### <a name="remove-an-existing-baseline-rule"></a>Varolan temel kuralı kaldır

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Temelleri** seçin.
3. Temel listesinde, **ER temellerini öğrenme biçimi**'ni yapılandırmak üzere biçim için yapılandırılan temeli seçin.
4. Daha önce yapılandırdığınız **Temeller** hızlı sekmesinde temel kuralını kaldırmak için **Sil**'i seçin.

![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline3.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Tasarlanan ER biçiminin bağlaması için değişiklikleri tanımlama

1. **Yapılandırmalar** sayfasında, **Değişiklikler** hızlı sekmesinde **Seçili bileşenler**'i seçin.
2. Biçim bileşenleri ağacında **Çıktı**'yı genişletin, **Çıktı\\Belge**'yi genişletin ve sonra onay kutusunu **Çıktı\\Belge\\ProcessingDateTime** için seçin.

    ![Bileşenler iletişim kutusunu seçme](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Bileşenler iletişim kutusunu seçme ekran görüntüsü")

3. **Tamam**'ı seçin.

![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline4.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")

Seçilen ER biçim bileşeni, **Değişiklikler** hızlı sekmesindeki bileşenler listesine eklenmiştir. Taban ER biçimi hata ayıklama modunda çalıştırıldığında, her bileşen için biçimin bağlaması, **Bağlama** sütununda gösterilen bağlama ile değiştirilir. **Değişiklikler** hızlı sekmesinde listelenen bir bileşenin varsayılan bağlamasını değiştirmek için, **Düzenle**'yi seçin.

### <a name="make-a-new-baseline-rule"></a>Yeni temel kuralı oluştur

Bu konunun yukarısındaki "Örnek": temel kurallar ayarını otomatikleştirme" bölümündek adımları takip edin. Bir bildirim, giden dosyanın temel ayarları kullanılarak üretildiğini ve biçim bağlamalarının zorlanmış bir şekilde değiştirilmesini size bildirir.

![Yapılandırma sayfasında Bildirim](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Yapılandırma sayfasında Bildirim ekran görüntüsü")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Formaların değiştirilmesine ilişkin uyarıları gizleme

Belirli ER. parametreleri ayarlayarak, biçim bağlamalarının değiştirilmesi hakkında uyarıcı bildirimleri gizleyebilirsiniz. Bu gizleme Regression Suite Automation Tool kullanılarak biçim bağlamaları müdahalesiz modda değiştirildiğinde yararlı olabilir. Bu durumda, uyarı çalışan test olayının hatası olarak kabul edilebilir.

1. **Yapılandırmalar** sayfasında, Eylem Bölmesinde **Yapılandırmalar** sekmesinde **Kullanıcı parametreleri**'ni seçin.
2. **Temel uyarıları bastır** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.

![Kullanıcı parametreleri iletişim kutusu](media/GER-BaselineSample-ERUserParameters1.png "Kullanıcı parametreleri iletişim kutusu ekran görüntüsü")

### <a name="review-the-generated-baseline-file"></a>Oluşturulan temel dosyayı gözden geçirin.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Temelleri** seçin.
3. **Ekler**'i seçin.

    ![Ekler sayfası](media/GER-BaselineSample-AttachedBaselineFile.PNG "Ekler sayfası ekran görüntüsü")

    > [!NOTE]
    > Oluşturulan dosya, formatın bağlayıcısından değil, eklenen temel kuralda yapılandırılan bağlamanın işlem tarih ve saat metnini (**"#"**) içerir.

4. **Ekler** sayfasını kapatın.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. Ağaçta, **ER temelini öğrenme modeli**'ni genişletin.
3. Ağaçta **ER temelini öğrenme modeli\\ER temelini öğrenme biçimi**'ni seçin.
4. **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
5. **Kimlik Gir** alanına, **1** yazın.
6. **Tamam**'ı seçin.
7. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar hata ayıklama**'ya gidin.

Yürütme günlükleri, oluşturulan dosyanın yapılandırılmış bir temelle karşılaştırılmasının sonuçlarıyla ilgili bilgiler içerir. Bu günlükte, yürütülen biçim, giden dosyasında sürekli değişen bir tarih ve saat değeri girmek için bağlama içerse bile oluşturulan dosya ve taban temelin eşit olduğunu gösterir.

> [!NOTE]
> Giden dosya, biçimlerin bağlarını değiştirmeye zorlayan temel ayarlar kullanılarak oluşturulmuş olsa da değiştirme ile ilgili herhangi bir uyarı almazsınız.

## <a name="exchange-baseline-settings-between-environments"></a>Ortamlar arasında Döviz temeli ayarları

### <a name="export-baseline-settings"></a>Dışa aktarma temeli ayarları

Yeni ER özellikleri, geçerli Finance and Operations ortamından seçili ER biçimi için temel ayarlarını dışa aktarmanız ve bunları XML dosyaları olarak depolayabilmenizi sağlar. 

Temel ayarlarını dışa aktarmak için **Elektronik raporlama biçim temelleri** sayfasında **Dışa aktar**'ı seçin.

### <a name="import-baseline-settings"></a>Temel ayarları içe aktar

Dışa aktarılan temel ayarları farklı Finance and Operations ortamına içe aktarılabilir. Ortam önce bir ER biçimi olarak içe aktarılmalıdır. Bundan sonra temel ayarları içe aktarabilirsiniz.

Yerel olarak depolanmış bir XML dosyasından ayarları dışa aktarmak için **Elekronik raporlama biçimi temelleri** sayfasında **Dışa aktarı**'ı seçin ve sonra XML dosyasını seçmek için **Gözat**'ı seçin.

![Temel ayarları iletişim kutusunu içe aktar](media/GER-BaselineSample-ImportBaseline1.PNG "Temel ayarları iletişim kutusunu içe aktar ekran görüntüsü")

Geçerli belge yönetimi ayarları ve seçili belge türü temel alınarak Microsoft SharePoint Sunucusunda depolanan bir XML dosyasından temel ayarları almak için **Elektronik raporlama biçim temelleri** sayfasında **Kaynaktan içe aktar**'ı seçin. Sonra belge türünü ve XML dosyasını seçin. SharePoint klasöre erişmek için gereken belge türü önceden yapılandırılmalıdır.

![Kaynak iletişim kutusundan içe aktar](media/GER-BaselineSample-ImportBaseline2.PNG "Kaynak iletişim kutusundan içe aktar ekran görüntüsü")

> [!NOTE]
> Görev kaydediciyi **Kaynağı içe aktar** iletişim kutusunda gereken belge türünü ve dosya adını seçmeye yönelik adımları kaydetmek için kullanabilirsiniz. Bu şekilde, gerekli temel ayarları SharePoint sunucusunda tutabilir ve Regression Suite Automation Tool'u kullanarak otomatik testleri çalıştırdığınızda, bunları bir görev kaydı yürüterek otomatik olarak alabilirsiniz .

## <a name="additional-resources"></a>Ek kaynaklar

- [Oluşturulan rapor sonuçlarını izleme ve temel değerlerle karşılaştırma](er-trace-reports-compare-baseline.md)
- [Görev kaydedici](../user-interface/task-recorder.md)
