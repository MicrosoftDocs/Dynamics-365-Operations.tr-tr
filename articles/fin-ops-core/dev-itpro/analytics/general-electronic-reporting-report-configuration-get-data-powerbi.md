---
title: Power BI'a veri çekmek için Elektronik raporlamayı (ER) yapılandırma
description: Bu konu, verilerinizi kurulumunuzdan Power BI hizmetlerine aktarmak amacıyla düzenlemek için Elektronik raporlama (ER) yapılandırmanızı nasıl kullanacağınızı açıklar.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 06859fc123e53ad58120bae6f936176176009ee1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345726"
---
# <a name="configure-electronic-reporting-er-to-pull-data-into-power-bi"></a>Power BI'a veri çekmek için Elektronik raporlamayı (ER) yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu, verilerinizi kurulumunuzdan Power BI hizmetlerine aktarmak amacıyla düzenlemek için Elektronik raporlama (ER) yapılandırmanızı nasıl kullanacağınızı açıklar. Örnek olarak, bu konu Intrastat hareketlerini aktarılması gereken iş verileri olarak kullanır. Power BI harita görselleştirmesi, bu Intrastat hareket verilerini şirketin içe aktarma/dışa aktarma etkinliklerinin Power BI raporundaki analizinin bir görünümünü sunmak için kullanır.

## <a name="overview"></a>Genel bakış

Microsoft Power BI harici veri kaynaklarını tutarlı, görsel olarak modern ve etkileşimli bilgilere dönüştürmek için birlikte çalışan yazılım hizmetleri, uygulamalar ve bağlayıcılardan oluşan bir koleksiyondur. Elektronik raporlama (ER), kullanıcıların veri kaynaklarını kolayca yapılandırmasını ve veriyi uygulamadan Power BI'ya aktarmayı ayarlamalarını sağlar. Veriler OpenXML çalışma sayfası (Microsoft Excel çalışma kitabı dosyası) biçiminde aktarılır. Aktarılan dosyalar bu amaçla yapılandırılmış bir Microsoft SharePoint Server üzerinde depolanır. Depolanan dosyalar görselleştirme (tablo, grafik, harita vs.) içeren raporlar oluşturmak için Power BI'da kullanılır. Power BI raporları Power BI kullanıcılarıyla paylaşılır ve bunlara Power BI panoları ve uygulama sayfalarından ulaşılır. Bu konuda aşağıdaki görevler açıklanmıştır:

- Microsoft Dynamics 365 Finance'ı yapılandırın.
- ER biçim yapılandırmanızı Finance uygulamasından veri almak için hazırlayın.
- ER ortamını Power BI'ya veri aktarmak için yapılandırın.
- Power BI raporu oluşturmak için aktarılan verileri kullanın.
- Power BI raporunu Finance'da erişilebilir hale getirin.

## <a name="prerequisites"></a>Önkoşullar
Bu konudaki örneği tamamlamak için şu erişimlere sahip olmanız gerekir:

- Aşağıdaki rollerden biri için erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Uygulama ile kullanılmak için yapılandırılmış SharePoint Server'a erişim
- Power BI çerçevesine erişim

## <a name="configure-document-management-parameters"></a>Belge yönetim parametrelerini yapılandırın
1. **Belge yönetim parametreleri** sayfasında, oturum açtığınız şirkette (bu örnekte DEMF şirketi) kullanılacak SharePoint Server erişimini yapılandırın.
2. Size erişim verildiğinden emin olmak için SharePoint Server bağlantısını test edin.

    [![Belge yönetim parametreleri sayfası.](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)

3. Yapılandırılmış SharePoint sitesini açın. ER'nin Power BI raporlarının bir Power BI veri kümesi kaynağı olarak gerektirdiği iş verilerine sahip olan Excel dosyalarını depolamak üzere yeni bir klasör oluşturun.
4. **Belge türleri** sayfasında, yeni oluşturduğunuz SharePoint klasörüne erişmek için kullanılacak yeni bir belge türü oluşturun. **Grup** alanında **Dosya** ve **Konum** alanında **SharePoint** girin ve SharePoint klasörünün adresini yazın.

    [![Belge türleri sayfası.](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma
1. **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri** bağlantısına tıklayın.
2. **Ekler** sekmesinde, tüm alanlar için **Dosya** belge türünü seçin.
3. **Elektronik raporlama** çalışma alanında, **Etkin olarak ayarla**'ya tıklayarak gerekli sağlayıcıyı etkin hale getirin. Daha fazla bilgi için **ER Hizmet sağlayıcısı seçme** görev kılavuzunu oynatın.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>ER veri modelini veri kaynağı olarak kullanma
Power BI raporlarında kullanılacak iş verileri kaynağı olarak bir ER veri modeliniz olmalıdır. Bu veri modeli ER yapılandırmaları deposundan yüklenir. Daha fazla bilgi için [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükleme](download-electronic-reporting-configuration-lcs.md) bölümüne bakın veya **ER Lifecycle Services'tan bir yapılandırmayı içe aktarma** görev kılavuzunu oynatın. Seçili ER yapılandırmaları deposundan karşıya yüklenecek veri modeli olarak **Intrastat**'ı seçin. (Bu örnekte, modelin 1. sürümü kullanılır.) Daha sonra **Intrastat** ER model yapılandırmasına **Yapılandırmalar** sayfasından erişebilirsiniz.

[![Yapılandırmalar sayfasında Intrastat ER model yapılandırması.](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>ER biçimi yapılandırması tasarlama
İş verilerinin kaynağı olarak **Intrastat** veri modelini kullanan yeni bir ER biçimi yapılandırması oluşturmanız gerekir. Bu biçim yapılandırması çıktı sonuçlarını OpenXML (Excel dosyası) biçiminde elektronik belgeler olarak oluşturmalıdır. Daha fazla bilgi için **ER Raporlar için OPENXML biçiminde bir konfigürasyon oluşturma** görev kılavuzunu oynatın. Yeni yapılandırmayı, aşağıdaki çizimde gösterildiği gibi, **İçe aktarma / dışa aktarma etkinlikleri** olarak adlandırın. ER biçimini tasarlarken şablon olarak [ER verileri - içe aktarma ve dışa aktarma ayrıntıları](https://download.microsoft.com/download/f/7/5/f755c0fd-025c-4aa9-920b-909abb8302ad/ER-data-import-and-export-details.xlsx) adlı Excel dosyasını kullanın. (Biçim şablonunu içe aktarma hakkında daha fazla bilgi için görev kılavuzunu oynatın.)

[![Etkinlik yapılandırmasını içe aktarma / dışa aktarma.](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png)

**İçe aktarma / dışa aktarma etkinlikleri** biçim yapılandırmasını değiştirmek için aşağıdaki adımları izleyin.

1. **Tasarımcı**'ya tıklayın.
2. **Biçim** sekmesinde, bu biçime ait dosya öğesini **Excel çıktı dosyası** olarak adlandırın.

    [![Excel çıktı dosyası öğesi.](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)

3. **Eşleme** sekmesinde, bu biçim her çalıştırıldığında oluşturulacak Excel dosyasının adını belirtin. İlgili ifadeyi **İçe aktarma ve dışa aktarma ayrıntıları** değerini döndürecek şekilde yapılandırın (.xlsx dosya adı uzantısı otomatik olarak eklenir).

    [![Biçim tasarımcısı.](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)

4. Bu biçim için yeni bir veri kaynağı öğesi ekleyin. (Bu numaralandırma daha fazla veri bağlaması için gereklidir.)

    1. Veri kaynağını **direction\_enum** olarak adlandırın.
    2. Veri kaynağı türü olarak **Veri modeli numaralandırması**'nı seçin.
    3. **Yön** veri modeli numaralandırmasına başvurun.

    [![direction_enum.](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)

5. **Intrastat** veri modelinin öğeleri ile tasarlanan biçimin öğelerini bağlama işlemini, aşağıdaki çizimde gösterildiği gibi tamamlayın.

    [![Bağlamayı tamamlama.](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

ER biçimi çalıştırıldıktan sonra çıktı sonucunu Excel biçiminde üretir. Intrastat hareketlerinin ayrıntılarını çıktı sonucuna gönderir ve bunları içe aktarma etkinliklerini veya dışa aktarma etkinliklerini açıklayan hareketler olarak ayırır. **Intrastat** sayfasındaki Intrastat hareketlerinin listesi için yeni ER biçimini test etmek üzere **Çalıştır**'a tıklayın (**Vergi** &gt; **Bildirimler** &gt; **Dış ticaret** &gt; **Intrastat**).

[![Intrastat sayfası.](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png)

Aşağıdaki çıktı sonucu oluşturulur. Dosya biçim ayarlarında belirttiğiniz gibi,**İçe aktarma ve dışa aktarma ayrıntıları.xlsx** olarak adlandırılır.

[![Import and export details.xlsx.](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER hedefini yapılandırma
Yeni ER biçimi yapılandırmasının çıktı sonucunu özel bir şekilde göndermek için ER çerçevesini yapılandırmanız gerekir.

- Çıktı sonucu seçili SharePoint Server klasörüne gönderilmelidir.
- Biçim yapılandırması her yürütüldüğünde aynı Excel dosyasının yeni bir sürümü oluşturulmalıdır.

**Elektronik raporlama** sayfasında (**Organizasyon yönetimi** &gt; **Elektronik raporlama**), **Elektronik raporlama hedefi** öğesine tıklayın ve yeni bir hedef ekleyin. **Referans** alanında, önceden oluşturduğunuz **İçe aktarma / dışa aktarma etkinlikleri** biçimi yapılandırmasını seçin. Referans için yeni bir dosya hedefi kaydı eklemek üzere aşağıdaki adımları izleyin.

1. **Ad** alanına dosya hedefinin başlığını girin.
2. **Dosya adı** alanında, Excel dosya biçimi bileşeni için **Excel çıktı dosyası** adını seçin.

Yeni hedef kaydı için **Ayarlar** düğmesine tıklayın. Daha sonra, **Hedef ayarları** iletişim kutusunda, aşağıdaki adımları izleyin.

1. **Power BI** sekmesinde, **Etkin** seçeneğini **Evet** olarak ayarlayın.
2. **SharePoint** alanında, önceden oluşturduğunuz **Paylaşılan** belge türünü seçin.

## <a name="schedule-execution-of-the-configured-er-format"></a>Yapılandırılmış ER biçiminin yürütülmesini planlama
1. **Yapılandırmalar** sayfasında (**Organizasyon yönetimi** &gt; **Elektronik raporlama** &gt; **Yapılandırmalar**), yapılandırmalar ağacından önceden oluşturduğunuz **İçe aktarma / dışa aktarma etkinlikleri** yapılandırmasını seçin.
2. 1.1 sürümünün durumunu **Taslak**'tan **Tamamlandı** olarak değiştirerek bu biçimi kullanılabilir hale getirin.

    [![Yapılandırmalar sayfasında içe/dışa aktarma etkinlikleri yapılandırması.](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png)

3. **İçe aktarma / dışa aktarma etkinlikleri** yapılandırmasının tamamlanmış sürümünü seçin ve **Çalıştır**'a tıklayın. Yapılandırılan hedefin Excel biçiminde üretilen çıktı sonucuna uygulandığına dikkat edin.
4. Bu raporu katılımsız modda çalıştırmak için **Toplu işleme** seçeneğini **Evet** olarak ayarlayın.
5. Bu toplu iş yürütmesinin gerekli yinelemelerini planlamak için **Tekrar**'a tıklayın. Yineleme, güncelleştirilen verilerin Power BI'ya ne kadar sıklıkla aktarılacağını belirler.

    [![Elektronik rapor parametreleri iletişim kutusu.](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png)

6. Yapılandırıldıktan sonra, ER raporu yürütme işini **Toplu işler** sayfasında (**Sistem yönetimi &gt; Sorgular &gt; Toplu işler**) bulabilirsiniz.

    [![Toplu işler sayfası.](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png)

7. Bu iş ilk kez çalıştırıldığında hedef, seçili SharePoint klasöründe yapılandırılan ada sahip yeni bir Excel dosyası oluşturur. İşin sonraki her çalıştırılmasında, hedef bu Excel dosyasının yeni bir sürümünü oluşturur.

    [![Excel dosyasının yeni sürümü.](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>ER biçiminin çıktı sonucunu kullanarak bir Power BI veri kümesi oluşturma
1. Power BI'da oturum açın ve var olan bir Power BI grubunu (çalışma alanı) açın veya yeni bir grup oluşturun. **İçe Aktarma veya Verilere Bağlanma** bölümünde, **Dosyalar** altında **Ekle**'ye tıklayın veya sol bölmede **Veri kümeleri**'nin yanındaki artı işaretine (**+**) tıklayın.

    [![Veri kümesi oluşturma.](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png)

2. **SharePoint - Ekip siteleri** seçeneğini belirleyin ve ardından kullandığınız SharePoint Server yolunu girin (örneğimizde `https://ax7partner.litware.com`).
3. **/Shared Documents/GER data/PowerBI** klasörüne gidin ve yeni Power BI veri kümesinin veri kaynağı olarak oluşturduğunuz Excel dosyasını seçin.

    [![Excel dosyasını seçme.](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png)

4. **Bağlan**'a ve ardından **İçe aktar**'a tıklayın. Seçili Excel dosyasını temel alan yeni bir veri kümesi oluşturulur. Veri kümesi yeni oluşturulan panoya da otomatik olarak eklenebilir.

    [![Panodaki veri kümesi.](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png)

5. Periyodik güncelleştirmeyi zorlamak amacıyla bu veri kümesi için yenileme zamanlamasını yapılandırın. Periyodik güncelleştirmeler, ER raporunun SharePoint Server'da oluşturulan Excel dosyasının yeni sürümleri üzerinden periyodik olarak yürütülmesi aracılığıyla yeni iş verilerinin kullanılabilmesini sağlar.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Yeni veri kümesini kullanarak Power BI raporu oluşturun
1. Oluşturduğunuz **İçe aktarma ve dışa aktarma ayrıntıları** Power BI veri kümesine tıklayın.
2. Görselleştirmeyi yapılandırın. Örneğin, **Dolgulu harita** görselleştirmesini seçin ve aşağıdaki şekilde yapılandırın:

    - Harita görselleştirmesinin **Konum** alanına **CountryOrigin** veri kümesi alanını atayın.
    - Harita görselleştirmesinin **Renk doygunluğu** alanına **Miktar** veri kümesi alanını atayın.
    - Harita görselleştirmesinin **Filtreler** alanları koleksiyonuna **Etkinlik** ve **Yıl** veri kümesi alanlarını ekleyin.

3. Power BI raporunu **İçe aktarma ve dışa aktarma ayrıntıları raporu** olarak kaydedin.

    [![İçe aktarma ve dışa aktarma ayrıntıları raporu.](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png)

    Haritanın Excel dosyasında belirtilen ülkeleri/bölgeleri (bu örnekte Avusturya ve İsviçre) gösterdiğine dikkat edin. Bu ülkeler/bölgeler her biri için faturalanan miktarların oranını gösterecek şekilde renklendirilmiştir.

4. Intrastat hareketlerin listesini güncelleştirin. İtalya'dan kaynaklanan dışa aktarma hareketi eklendi.

    [![Intrastat hareketleri listesi.](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png)

5. ER raporunun bir sonraki planlanan yürütülmesini ve Power BI veri kümesinin bir sonraki planlanan güncelleştirmesini bekleyin. Daha sonra, Power BI raporunu inceleyin (yalnızca içe aktarma hareketlerini göstermeyi seçin). Güncelleştirilen harita artık İtalya'yı göstermektedir.

    [![Güncelleştirilen harita.](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance"></a>Finance'ta Power BI raporuna erişim
Power BI ile tümleştirmeyi ayarlayın. Daha fazla bilgi için bkz. [Çalışma alanları için Power BI tümleştirmesini yapılandırma](configure-power-bi-integration.md).

1. Power BI tümleştirmesini destekleyen **Elektronik raporlama** çalışma alanı sayfasında (**Organizasyon yönetimi** &gt; **Çalışma alanları** &gt; **Elektronik raporlama çalışma alanı**), **Seçenekler** &gt; **Rapor kataloğunu aç**'a tıklayın.
2. Oluşturduğunuz **İçe aktarma ve dışa aktarma ayrıntıları** Power BI raporunu seçili sayfada bir eylem öğesi olarak göstermek için raporu seçin.
3. Power BI'da tasarladığınız raporu gösteren sayfayı açmak için eylem öğesine tıklayın.

    [![Power BI'da tasarlanan içe aktarma ve dışa aktarma ayrıntıları raporu.](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik raporlama (ER) hedefleri](electronic-reporting-destinations.md)

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
