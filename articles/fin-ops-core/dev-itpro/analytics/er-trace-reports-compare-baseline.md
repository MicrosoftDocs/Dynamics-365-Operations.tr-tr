---
title: Oluşturulan rapor sonuçlarını izleme ve temel değerlerle karşılaştırma
description: Bu konu, oluşturulan ER raporlama (ER) raportlarının sonuçlarını temel rapor değerleriyle nasıl karşılaştıracağınız hakkında bilgi vermektedir.
author: NickSelin
manager: AnnBe
ms.date: 06/17/2019
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
ms.openlocfilehash: 1643e7fb3128faf6ad638d4cdad313b3667463b1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181692"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Oluşturulan rapor sonuçlarını izleme ve temel değerlerle karşılaştırma

[!include[banner](../includes/banner.md)]

Giden elektronik belgeler oluşturan ER raporlama (ER) biçimlerinin sonuçlarını izleyebilirsiniz. İzleme oluşturma açıldığı zaman (**Hata ayıklama modunda çalıştır** ER kullanıcı parametresini kullanarak), her ER raporu çalıştırıldığında ER biçimi yürütme günlüğünde yeni bir izleme kaydı oluşturulur. Oluşturulan her izlemede aşağıdaki ayrıntılar depolanır:

- Doğrulama kurallarıyla oluşturulan tüm uyarılar
- Doğrulama kurallarıyla oluşturulan tüm hatalar
- İzleme kaydının ekleri olarak depolanan tüm oluşturulan dosyalar

Her ER biçimi için ayrı ayrı temel uygulama dosyaları depolayabilirsiniz. Dosyalar, çalıştırılan raporların beklenen sonuçlarını açıklıyorsa temel dosya olarak nitelendirilir. İzleme oluşturma açıkken çalıştırılmış bir ER biçimine ilişkin bir temel dosya varsa izleme, daha önce sözü edilen ayrıntıların yanı sıra, oluşturulan elektronik belgeyi temel dosyayla karşılaştırma sonucunu depolar. Oluşturulan elektronik belgeyi ve temel dosyasını tek tıklamayla bir zip dosyasına alabilirsiniz. Bunun ardından, WinDiff gibi harici bir araç kullanarak ayrıntılı bir karşılaştırma yapabilirsiniz.

Oluşturulan elektronik belgelerde beklenen içeriğin olup olmadığını analiz etmek için izlemeyi değerlendirebilirsiniz. Kod tabanı değiştiği zaman bu değerlendirmeyi bir kullanıcı kabul testi (UAT) ortamında yapabilirsiniz (örneğin uygulamanın yeni bir örneğine geçtiğiniz, düzeltme paketleri yüklediğiniz veya kod değişiklikleri dağıttığınız zaman). Bu sayede, değerlendirmenin, kullanılan ER raporlarının yürütülmesini etkilemediğinden emin olabilirsiniz. Birçok ER raporu için, değerlendirme müdahalesiz modda yapılabilir.

Bu özellik hakkında daha fazla bilgi için, **7.5.4.3 BT hizmetlerini/çözümlerini test etme (10679)** iş sürecinin birer parçası olan ve [Microsoft İndirme Merkezi](https://go.microsoft.com/fwlink/?linkid=874684)'dan indirilebilen **ER - Raporlar oluşturma ve sonuçları karşılaştırma (Bölüm 1)** ve **ER - Raporlar oluşturma ve sonuçları karşılaştırma (Bölüm 2)** görev kılavuzlarını oynatın. Bu görev kılavuzları, oluşturulan elektronik belgeleri değerlendirmek üzere temel dosyaları kullanmak için ER çerçevesini yapılandırma işleminde size yol gösterir.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Örnek: Oluşturulan rapor sonuçlarını izleme ve bunları temel değerlerle karşılaştırma

Bu prosedür ER. biçimi yürütmeleri hakkında bilgi toplamak ve bu yürütmelerin sonuçlarını değerlendirmek için ER çerçevesinin nasıl yapılandırılacağı açıklamaktadır. Bu değerlendirmenin bir parçası olarak, oluşturulan belgeler temel dosyalarıyla karşılaştırılır. Bu örnekte, örnek şirket için gerekli ER yapılandırmalarını oluşturacaksınız. Bu yordam Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmış kullanıcılar içindir. Bu adımlar herhangi bir veri kümesi kullanılarak tamamlanabilir.

Bu konudaki adımları tamamlamak için öncelikle [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) adımlarını tamamlamanız gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma sağlayıcıları** bölümünde, Litware, Icn. örnek şirketine ait yapılandırma sağlayıcısının listelendiğinden ve **Etkin** olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md). adımlarını takip edin.

### <a name="configure-document-management-parameters"></a>Belge yönetim parametrelerini yapılandırın

1. **Kuruluş yönetimi** \> **Belge yönetimi** \> **Belge türü**'ne gidin ve temel dosyaları saklamak için yeni dosya türü oluşturun.
2. **Sınıf** alanında, **Dosya ekle**'yi girin.
3. **Grup** alanında, **Dosya**'yı girin.

![Belge türleri sayfası](media/GER-BaselineSample-SetupDocumentType.PNG "Belge türleri sayfası ekran görüntüsü")

> [!NOTE]
> ER temel özelliğini kullanmayı planladığınız her bir veri kümesi için aynı ada sahip yeni bir belge türü yapılandırılmalıdır.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Temel özelliğini kullanmaya başlamak için ER parametrelerini yapılandırma

1. **İlgili bağlantılar** içinde, **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri**'ni seçin.

    ![Elektronik raporlama çalışma alanı](media/GER-BaselineSample-ERWorkspace.PNG "Elektronik raporlama çalışma alanı ekran görüntüsü")

2. **Ekler** sekmesinde **Temel** alanına, oluşturduğunuz belge türünü girin ya da seçin.

    ![Elektronik raporlama parametreler sayfasının ekler sekmesi](media/GER-BaselineSample-ERParameters.PNG "Elektronik raporlama parametrelerinin ekler sekmesi ekran görüntüsü")

3. **Kaydet**'i seçin ve **Elektronik raporlama parametreleri** sayfasını kapatın.

### <a name="add-a-new-er-model-configuration"></a>Yeni bir ER model yapılandırması ekleme

1. **Elektronik raporlama** çalışma alanı içinde **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
2. Eylem Panosundan **Yapılandırma oluştur**'u seçin.
3. Açılır menüdeki iletişim kutusunda, **Ad** alanına **ER temelini öğrenme modeli**'ni girin.
4. ER veri modeli girişinin oluşturulmasını onaylamak için **Yapılandırma yarat**'ı seçin.

![Açılan iletişim kutusu yapılandırması oluşturma](media/GER-BaselineSample-ModelAdd.PNG "Açılan iletişim kutusu yapılandırması oluşturma")

### <a name="design-a-data-model"></a>Bir veri modeli tasarlama

1. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Tasarımcı**'yı seçin.
2. **Yeni**'yi seçin.
3. Açılır menüdeki iletişim kutusundaki **Ad** alanına **Kök** girin.
4. **Ekle**'yi seçin.
5. **Kök referansı**'nı seçin.
6. **Tamam**'ı seçin ve sonra **Kaydet**'i seçin.
7. **Model tasarımcısı** sayfasını kapatın.
8. **Durumu değiştir**'i seçin.
9. **Tamamla**y'ı seçin ve sonra **Tamam**'i seçin.

![Yapılandırma sayfası](media/GER-BaselineSample-ModelComplete.PNG "Yapılandırma sayfası ekran görüntüsü")

### <a name="add-a-new-er-format-configuration"></a>Yeni bir ER biçim yapılandırması ekleme

1. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Yapılandırma Oluştur**'u seçin.
2. Açılan iletişim kutusunda **Yeni** alan grubunda, **Biçim ve veri modeline dayalı ER temelini öğrenme modeli** seçeneğini seçin.
3. **Ad** alanına **ER temellerini öğrenme biçimi** girin.
4. ER biçim girişinin oluşturulmasını onaylamak için **Yapılandırma yarat**'ı seçin.

![Açılan iletişim kutusu yapılandırması oluşturma](media/GER-BaselineSample-FormatAdd.PNG "Açılan iletişim kutusu yapılandırması oluşturma ekran görüntüsü")

### <a name="design-a-format"></a>Bir biçim tasarlama

Bu örnekte, XML belgeleri oluşturmak için basit bir ER biçimi oluşturacaksınız.

1. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Tasarımcı**'yı seçin.
2. **Kök ekle**'yi seçin.
2. Açılan iletişim kutusunda şu adımları izleyin:

    1. Ağaçta **Common\\File**'ı seçin.
    2. **Ad** alanına, **Çıktı** yazın.
    3. **Tamam**'ı seçin.

3. **Ekle**'yi seçin.
4. Açılan iletişim kutusunda şu adımları izleyin:

    1. Ağaçta **XML\\Element**'i seçin.
    2. **Ad** alanına, **Belge** girin.
    3. **Tamam**'ı seçin.

5. Ağaçta **Output\\Document**'i seçin.
6. **Ekle**'yi seçin.
7. Açılan iletişim kutusunda şu adımları izleyin:

    1. Ağaçta **XML\\Attribute**'u seçin.
    2. **Ad** alanına, **Kimlik** yazın.
    3. **Tamam**'ı seçin.

    ![Biçim tasarımcısı sayfası](media/GER-BaselineSample-FormatLayoutDesign.PNG "Biçim tasarımcısı sayfası ekran görüntüsü")

8. **Eşleme** sekmesinde **Sil**'i seçin.
9. **Kök ekle**'yi seçin.
10. Açılan iletişim kutusunda ağaçtaki **Genel\\Kullanıcı giriş parametresi**'ni seçin ve aşağıdaki adımları takip edin:

    1. **Ad** alanına, **Kimlik** yazın.
    2. **Etiket** alanına, **Kimlik Gir** yazın.
    3. **Tamam**'ı seçin.

11. Ağaçta **Output\\Document\\Id**'yi seçin.
12. **Bağla**'yı seçin ve sonra **Kaydet**'i seçin.

![Biçim tasarımcısı sayfası](media/GER-BaselineSample-FormatMappingDesign.PNG "Biçim tasarımcısı sayfası ekran görüntüsü")

Tasarlanan yapıya bağlı olarak, yapılandırılmış biçim bir XML dosyası oluşturur. Bu XML kullanıcının bir ER çalışma zamanı kutusuna girdiği değere ayarlanmış **Kimlik** özelliğine sahip **Kök** öğresini içerir.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Tasarlanan bir ER biçimi için yeni bir temel dosyası oluşturma

1. **Yapılandırmalar** sayfasında, **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
2. **Kimlik Gir** alanına, **1** yazın.
3. **Tamam**'ı seçin.

    ![Elektronik rapor parametreleri iletişim kutusu](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Elektronik rapor parametreleri iletişim kutusu ekran görüntüsü")

4. Oluşturulan **out.Admin.xml** dosyasının yerel bir dosyasının kaydedin, böylece bu ER biçiminde temel olarak daha sonra kullanabilirsiniz.

    ![Yapılandırma sayfasında oluşturulan sayfa hakkında bildirim](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Yapılandırma sayfasında oluşturulan sayfa hakkında bildirim ekran görüntüsü")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Temel özelliğini kullanmak için ER parametrelerini yapılandırma

1. **Yapılandırmalar** sayfasında, Eylem Bölmesinde **Yapılandırmalar** sekmesinde **Kullanıcı parametreleri**'ni seçin.
2. **Hata ayıklama modu** seçeneğini **Evet** olarak ayarlayın.
3. **Tamam**'ı seçin.

![Kullanıcı parametreleri iletişim kutusu](media/GER-BaselineSample-ERUserParameters.PNG "Kullanıcı parametreleri iletişim kutusu ekran görüntüsü")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Tasarlanan bir ER biçimi için yeni bir temel dosyası ekleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. Eylem Bölmesinde, **Temeller**'i seçin.

    ![Yapılandırma sayfasında temeller düğmesi](media/GER-BaselineSample-OpenBaselinePage.PNG "Yapılandırma sayfasında temeller düğmesi ekran görüntüsü")

3. Eylem Bölmesinde, **Yeni**'yi seçin.
4. Daha önce tasarladığınız **ER temellerini öğrenme biçimi** ER biçimini seçin.
5. **Kaydet**'i seçin.

![Elektronik raporlama biçim temelleri sayfası](media/GER-BaselineSample-AddBaseline.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")

Bu temel **ER temellerini öğrenme biçimi** biçimi için eklenir.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Eklenen temel için bir temel kuralı yapılandırma

1. **Elektronik raporlama biçim temelleri** sayfasında, eylem bölmesinde, **Ekler** düğmesini (ataş simgesi) seçin.
2. Eylem Bölmesinde **Yeni** \> **Dosya**'yı seçin. ER parametrelerinde, **Dosya** belge türünün önceden temel dosyaları depolamak için kullanılan belge türü olarak seçilmiş olması gerekir.
3. **Gözat**'ı seçin ve daha önce ER biçiminde yapılandırdığınızda oluşan **out.Admin.xml** dosyasını seçin.

    ![Ekler sayfası](media/GER-BaselineSample-UploadBaselineFile.PNG "Ekler sayfası ekran görüntüsü")

4. **Ekler** sayfasını kapatın.
5. **Temeller** hızlı sekmesinde **Yeni**'yi seçin.
6. **Ad** alanına, **Temel 1** yazın.
7. **Dosya bileşen adı** alanında, **Çıkış**'ı girin veya seçin. Bu değer, yapılandırılmış temelin, **Çıktı** biçimi öğesi kullanılarak oluşturulan bir dosyayla karşılaştırılacağını belirtir.
8. **Dosya adı maskesi** alanında **\*.xml**'i girin.

    > [!NOTE]
    > Dosya adı maskesini tanımlayabilirsiniz. Dosya adı maskesi tanımlandığında, temel kayıt, oluşturulan çıktıyı yalnızca, oluşturulan çıktı dosyasının adı maskeyi sağladığında değerlendirmek için kullanılacaktır.

9. Yapılandırılan temel yalnızca **ER temellerini öğrenme biçimi** ER biçimi belirli şirketlerde oturum açan kullanıcılar tarafından çalıştırılıyorsa bu şirketleri **Şirketler** alanında seçin.
10. **Temel** alanında **out.Admin** ekini girin ya da seçin.
11. **Kaydet**'i seçin.

![Elektronil raporlama biçim temelleri sayfası](media/GER-BaselineSample-SetupBaselineLine.PNG "Elektronik raporlama biçim temelleri sayfası ekran görüntüsü")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. Ağaçta **ER temellerini öğrenme modellerini** genişletin ve sonra **ER temellerini öğrenme modelleri\\ER temellerini öğrenme biçimleri**'ni seçin.
3. **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
4. **Kimlik Gir** alanına, **1** yazın.
5. **Tamam**'ı seçin.
6. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar hata ayıklama**'ya gidin.

    ![Elektronik raporlama yürütme günlükleri sayfası](media/GER-BaselineSample-ReviewBaselineComparison1.PNG " Elektronik raporlama yürütme günlükleri sayfası ekran görüntüsü")

    > [!NOTE]
    > Yürütme günlükleri, oluşturulan dosyanın yapılandırılmış bir temelle karşılaştırılmasının sonuçlarıyla ilgili bilgiler içerir. Bu örnekte, günlük, oluşturulan dosya ve temelin eşit olduğunu gösterir.

7. **Tümünü sil**'i seçin.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Tasarlanan ER biçimini çalıştırma ve sonuçları analiz etmek için günlüğü gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. Ağaçta **ER temellerini öğrenme modellerini** genişletin ve sonra **ER temellerini öğrenme modelleri\\ER temellerini öğrenme biçimleri**'ni seçin.
3. **Sürümler** hızlı sekmesinde **Çalıştır**'ı seçin.
4. **Kimlik Gir** alanına, **2** yazın.
5. **Tamam**'ı seçin.
6. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar hata ayıklama**'ya gidin.

    ![Elektronik raporlama yürütme günlükleri sayfası](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Elektronik raporlama yürütme günlükleri sayfası ekran görüntüsü")

    > [!NOTE]
    > Yürütme günlükleri, oluşturulan dosyanın yapılandırılmış bir temelle karşılaştırılmasının sonuçlarıyla ilgili bilgiler içerir. Bu örnekte, günlük, oluşturulan dosya ve temelin farklı olduğunu gösterir.

7. **Karşılaştır**'ı seçin.

> [!NOTE]
> Oluşturulan dosya ve temel dosyası bir ZIP dosyası olarak sunulur. Dosyaları karşılaştırmak ve farkları incelemek için WinDiff gibi harici karşılaştırma araçlarını kullanabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md)
