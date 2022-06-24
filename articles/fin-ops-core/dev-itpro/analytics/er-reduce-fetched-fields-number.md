---
title: Çalışma zamanında getirilen tablo alanlarının sayısını azaltarak ER çözümlerinin performansını artırma
description: Bu makalede, çalışma zamanında getirilen tablo alanlarının sayısını azaltarak ER çözümlerinin performansını artırmaya nasıl yardımcı olacağınız açıklanmaktadır.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: eb76c415da87d421b8135a93b84f4e905f01e70d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847465"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Çalışma zamanında getirilen tablo alanlarının sayısını azaltarak ER çözümlerinin performansını artırma

[!include[banner](../includes/banner.md)]

Çeşitli biçimlerde giden belgeler oluşturan [Elektronik raporlama](general-electronic-reporting.md) (ER) [biçimleri](er-overview-components.md#format-components-for-outgoing-electronic-documents) tasarlayabilirsiniz. Bir belge oluşturulurken, bir ER biçimi, karşılık gelen bir ER [model eşlemesinde](er-overview-components.md#model-mapping-component) yapılandırılmış veri kaynaklarını çağırır. Kayıt alma amacıyla uygulama tablolarına, sorgularına veya varlıklarına erişimi yapılandırmak için *Tablo kayıtları* türünde ER veri kaynakları kullanabilirsiniz. Varsayılan olarak, *Tablo kayıtları* türündeki bir veri kaynağı istenen kayıtlardaki tüm alanların değerlerini alır. Ancak, bu türdeki bir veri kaynağını yalnızca çalışan ER biçimi için gerekli alan değerlerini getirecek şekilde yapılandırabilirsiniz. Bu yapılandırma, veri alımı ve daha fazla kayıt önbelleğe alma işlemi gerçekleştiren uygulama sunucusunun bellek tüketimini azaltmaya yardımcı olur.

*Tablo kayıtları* türündeki veri kaynaklarının getirilen alan listesini sınırlama konusunda daha fazla bilgi için bu makaledeki örneği tamamlayın.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Örnek: Çalışma zamanında getirilen tablo alanlarının sayısını azaltma

Aşağıdaki yordamlarda, Sistem Yöneticisi veya Elektronik raporlama geliştiricisi rolündeki bir kullanıcının, uygulama sunucusu belleğinin kullanımını azaltmaya yardımcı olmak amacıyla, bir ER model eşlemesini yalnızca ER biçimini çalıştırmak için gerekli alanları gösterecek şekilde nasıl yapılandıracağını gösterir.

Bu yordamlarda, Microsoft Dynamics 365 Finance'teki **USMF** şirketinde tamamlanabilir. Kodlama gerekmez.

Bu örneği tamamlamak üzere aşağıdaki rollerden biri için **USMF** şirketine erişiminiz olmalıdır:

- Elektronik raporlama işlev danışmanı
- Sistem yöneticisi

Bu örnekte, **Litware, Inc.** örnek şirketi için sağlanan ER [yapılandırmalarını](general-electronic-reporting.md#Configuration) kullanacaksınız. **Litware, Inc.** (`http://www.litware.com`) örnek şirketinin yapılandırma sağlayıcısının ER çerçevesinde listelendiğinden ve **Etkin** olarak işaretlendiğinden emin olun. Bu yapılandırma sağlayıcısı listede yoksa veya **Etkin** olarak işaretli değilse [Bir yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) konusundaki adımları izleyin.

### <a name="configure-the-er-framework"></a>ER altyapısını yapılandırma

En az ER parametre kümesini ayarlamak için [ER altyapısını yapılandırma](er-quick-start2-customize-report.md#ConfigureFramework) bölümündeki adımları izleyin. Sağlanan ER çözümünün veri kaynaklarını değiştirmek için ER çerçevesini kullanmaya başlamadan önce bu kurulumu tamamlamanız gerekir.

### <a name="import-the-sample-er-configurations"></a>Örnek ER yapılandırmalarını içe aktarma

[Özel rapor yazdırmak için yeni bir ER çözümü tasarlama](er-quick-start1-new-solution.md) makalesindeki örneği henüz tamamlamadıysanız, sağlanan ER çözümünün aşağıdaki yapılandırmaları için XML dosyalarını indirin ve yerel olarak saklayın.

| İçerik açıklaması            | Dosya adı |
|--------------------------------|-----------|
| ER data model configuration    | [Questionnaires model.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| ER model eşleme yapılandırması | [Questionnaires mapping.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| ER format configuration        | [Questionnaires format.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Ardından, sağlanan ER çözümünün yapılandırmalarını Finance örneğinize yüklemek üzere aşağıdaki adımları izleyin.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. **Yapılandırmalar** sayfasında, ER veri modeli yapılandırmasını içeri aktarın.

    1. **Exchange** 'i ve ardından **XML dosyasından yükle**'yi seçin.
    2. **Gözat**'ı seçin ve **Questionnaires model.version.1.xml** dosyasını bulup seçin ve ardından **Tamam**'ı seçin.

4. ER model eşleme yapılandırma dosyasını içeri aktarın.

    1. **Exchange** 'i ve ardından **XML dosyasından yükle**'yi seçin.
    2. **Gözat**'ı seçin, **Questionnaires mapping.1.1.xml** dosyasını bulup seçin ve ardından **Tamam**'ı seçin.

5. ER biçimi yapılandırmasını içe aktarın.

    1. **Exchange** 'i ve ardından **XML dosyasından yükle**'yi seçin.
    2. **Gözat**'ı seçin, **Questionnaires format.1.1.xml** dosyasını bulup seçin ve ardından **Tamam**'ı seçin.

6. Yapılandırma ağacında, **Soru formu modeli**'ni genişletin.
7. Yapılandırma ağacındaki içe aktarılan ER yapılandırmaları listesini inceleyin.

    ![Yapılandırmalar sayfasında içeri aktarılan ER yapılandırmaları listesini inceleme.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Sağlanan ER model eşleşmesini inceleme

1. **Yapılandırmalar** sayfasında, **Soru formu eşlemesi**'ni seçin.
2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
3. **Modeli veri kaynağına eşleme** sayfasında **Tasarımcı**'yı seçin.
4. **Model eşleme tasarımcısı** sayfasındaki Eylem Bölmesinde, **Grup** görünümünü açmak için **Grup görünümü**'nü seçin.
5. **Veri modeli** bölmesinde **Soru formu**'nu genişletin.

    **Soru formu** veri kaynağının `KMCollection` uygulama tablosuna erişecek şekilde yapılandırıldığını görürsünüz.

6. **Veri kaynakları** bölmesinde **Tablo kayıtları** \> **Soru formu** \> **Alanlar**'ı genişletin.

    `KMCollection` uygulama tablosundaki kaç alanın, *Tablo kayıtları* türündeki **Soru formu** veri kaynağı tarafından gösterildiğine dikkat edin.

    ![Grup görünümü açıkken Model eşleme tasarımcısı sayfasında sağlanan model eşlemeyi inceleme.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Eylem Bölmesinde, **Grup** görünümünü kapatmak için **Grup görünümü**'nü yeniden seçin ve **Tümünü göster** \> **Yalnızca eşlenmişleri göster**'i seçin.

    `KMCollection` uygulama tablosunun birkaç alanının, ER veri modelindeki **Soru formu** kayıt listesini doldurmak için kullanıldığını görürsünüz:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Grup görünümü kapalıyken Model eşleme tasarımcısı sayfasında sağlanan model eşlemeyi inceleme.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>ER performans izlemesini aç

ER bileşenlerinin izlenmesini etkinleştiren ER kullanıcı parametrelerini ayarlamak için [ER performans izlemesini aç ](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) makalesinde açıklanan adımları izleyin.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Sağlanan model eşlemesini kullanarak sağlanan ER biçimini çalıştırma

**Yapılandırmalar** sayfasındaki tek bir soru formu için sağlanan ER biçimini çalıştırmak üzere [ER'den tasarlanan biçim çalıştırma](er-quick-start1-new-solution.md#RunFormatFromER) makalesindeki adımları izleyin.

### <a name="review-the-execution-trace-of-the-first-run"></a>İlk çalıştırmanın yürütme izlemesini inceleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama \> Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, **Soru formu modeli**'ni genişletin ve **Soru formu eşleme**'yi seçin.

    > [!NOTE]
    > **Sürümler** hızlı sekmesindeki ayrıntılar, **Soru formu eşleme** yapılandırmasının taslak sürümünü seçtiğinizi gösterir. Bu nedenle, bu model eşlemesinin içeriğini değiştirebilirsiniz.

3. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
4. **Modeli veri kaynağına eşleme** sayfasında **Tasarımcı**'yı seçin.
5. **Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.
6. **Performans izleme sonucu ayarları** iletişim kutusunda, son biçim çalıştırmasında oluşturulan izlemeyi seçin.

    ![Performans izleme sonucu ayarları iletişim kutusunda izlemeyi seçme.](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. **Tamam**'ı seçin. 
8. **Ayrıntılar** hızlı sekmesinde, **Soru formu** veri kaynağına giden **Soru formu** yolunu filtreleyin.
9. **Soru formu** veri kaynağı çağırıldığında oluşturulan veritabanı sorgusunun ayrıntılarını gözden geçirin.

    **Soru formu** veri kaynağı çağrıldığında, çalışma zamanında `KMCollection` uygulama tablosundaki tüm alanların getirildiğini görürsünüz.

    ![Model eşleme tasarımcısı sayfasındaki veritabanı sorgusunun ayrıntılarını gözden geçirme.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Sağlanan ER model eşleşmesini değiştirme

1. **Model eşleme tasarımcısı** sayfasındaki **Veri kaynakları** bölmesinde, **Soru formu** veri kaynağını seçin.
2. **Veri kaynakları** bölmesinde **Düzenle**'yi seçin.
3. **Veri kaynağı özellikleri** iletişim kutusunda, düzenlenebilir **Soru formu** veri kaynağı çağırıldığında, çalışma zamanında getirilecek başvurulan `KMCollection` uygulama tablosu alanlarının listesini belirtmek için **Alan seçin**'i seçin.

    ![Düzenlenebilir veri kaynağı kullanılarak uygulama tablosundan getirilecek alanların listesini yapılandırmaya başlamak için Veri kaynağı özellikleri iletişim kutusunda Alanları seçin'i seçme.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. **Alanları seçin** sayfasında, **Otomatik doldur**'u seçin.

    **Seçili alanlar** listesi, model eşlemesinin önceden yapılandırılmış yapıtları temel alınarak otomatik olarak doldurulur. Model eşlemenin tüm bağlamalarında, formüllerinde veya veri kaynaklarında belirtilen başvurulan tablonun tüm alanları ve ilişkileri listeye eklenir.

    ![Alanları seçin sayfasında uygulama tablosundan getirilecek alanların listesini yapılandırma.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. **Kaydet**'i seçin ve sonra **Alanları seçin** sayfasını kapatın.
6. Veri kaynağı ayarlarında yaptığınız değişiklikleri depolamak için **Tamam**'ı seçin.
7. Eylem Bölmesinde, **Tümünü göster**'i seçin.

    **Soru formu** veri kaynağının artık **\<Fields are filtered\>** ifadesini gösterdiğini görürsünüz. Bu metin, veri kaynağının başvurulan uygulama tablosundan sınırlı sayıda alan getirmek üzere yapılandırıldığını gösterir.

    ![Modeli eşleme tasarımcısı sayfasındaki güncelleştirilmiş model eşlemesini inceleme.](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Düzenlenebilir model eşlemesinde yaptığınız değişiklikleri depolamak için **Kaydet**'i seçin.

    > [!NOTE]
    > Çalışma zamanında, ER eklenen ilişkileri analiz eder ve bunlarda kullanılan tüm alanları veritabanı sorgusuna ekler. Bu durum, söz konusu alanlar tasarım zamanında getirilen alanlar listesine açıkça eklenmese bile geçerlidir.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Güncelleştirilen model eşlemesini kullanarak sağlanan ER biçimini çalıştırma

**Yapılandırmalar** sayfasındaki tek bir soru formu için sağlanan ER biçimini çalıştırmak üzere [ER'den tasarlanan biçim çalıştırma](er-quick-start1-new-solution.md#RunFormatFromER) makalesindeki adımları izleyin.

### <a name="review-the-execution-trace-of-the-second-run"></a>İkinci çalıştırmanın yürütme izlemesini inceleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, **Soru formu modeli**'ni genişletin ve **Soru formu eşleme**'yi seçin.
3. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
4. **Modeli veri kaynağına eşleme** sayfasında **Tasarımcı**'yı seçin.
5. **Model eşleme tasarımcısı** sayfasında, Eylem Panosu üzerinde, **Performans izleme**'yi seçin.
6. **Performans izleme sonucu ayarları** iletişim kutusunda, son biçim çalıştırmasında oluşturulan izlemeyi seçin.
7. **Tamam**'ı seçin.
8. **Ayrıntılar** hızlı sekmesinde, **Soru formu** veri kaynağına giden **Soru formu** yolunu filtreleyin.
9. **Soru formu** veri kaynağı çağırıldığında oluşturulan veritabanı sorgusunun ayrıntılarını gözden geçirin.

    **Soru formu** veri kaynağı çağırıldığında, çalışma zamanında yalnızca veri kaynağını doldurmak için gerekli olan alanların `KMCollection` uygulama tablosundan getirildiğine dikkat edin.

    > [!NOTE]
    > Bölüm kimliği, veri alanı kimliği ve kayıt kimliği alanları gibi bazı alanlar, Finance uygulamasının Veri Yönetimi çerçevesi tarafından otomatik olarak eklenir.

    ![Model eşleme tasarımcısı sayfasında güncelleştirilen model eşlemesi için veritabanı sorgusunun ayrıntılarını gözden geçirme.](./media/er-reduce-fetched-fields-number-query2.png)

Bu tekniği, çalışan ER model eşlemesi ve ER biçiminin bellek tüketimini azaltmanız gerektiğinde getirilen kayıt sayısını azaltmak için kullanabilirsiniz.

## <a name="limitations"></a>Sınırlamalar

*Tablo kayıtları* türündeki bir veri kaynağı için getirilen alan sayısını sınırlandırdığınızda, veri kaynağının başvurduğu uygulama tablosunun yöntemlerini kullanamazsınız. Bunun nedeni, uygulama meta verilerinin bu yöntemleri çağırmak için gerekli tablo alanları hakkında bilgi sağlamamasıdır.

## <a name="usage-notes"></a>Kullanım notları

**Otomatik doldur** komutu alanları otomatik olarak eklemesine rağmen, daha önce eklenen alanları otomatik olarak silmez. Bu durum, söz konusu alanların düzenlenebilir model eşlemesinin bağlamalarında, formüllerinde ve veri kaynaklarında artık kullanılmıyor olması durumunda da geçerlidir.

**Otomatik doldur**'u seçtiğinizde ER, düzenlenebilir model eşlemesini düzenleme için açtığınız sırada eşlemenin sahip olduğu bağlamaları, formülleri ve veri kaynaklarını analiz eder. Düzenlenebilir model eşlemesinin bağlamalarını, formüllerini ve veri kaynaklarını değiştirdiyseniz ve **Otomatik Doldur** komutunu kullanmak istiyorsanız, model eşleme tasarımcısını kapatın ve model eşlemenizi düzenlemek için yeniden açın. 

## <a name="additional-resources"></a>Ek kaynaklar

- [Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md)
- [ER yapılandırmalarında performans sorunlarını giderme](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
