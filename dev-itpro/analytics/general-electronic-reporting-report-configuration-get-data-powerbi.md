---
title: "Power BI'a veri çekmek için Elektronik raporlamayı yapılandır"
description: "Bu konu, verilerinizi Finance and Operations kurulumunuzdan Power BI hizmetlerine aktarmak amacıyla düzenlemek için Elektronik raporlama (ER) yapılandırmanızı nasıl kullanacağınızı açıklar. Örnek olarak, bu konu Intrastat hareketlerini aktarılması gereken iş verileri olarak kullanır. Power BI harita görselleştirmesi, bu Intrastat hareket verilerini şirketin içe aktarma/dışa aktarma etkinliklerinin Power BI raporundaki analizinin bir görünümünü sunmak için kullanır."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 36c5e78f4b85d0c763c35b62a6592365501db325
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017


---

# <a name="configure-electronic-reporting-to-pull-data-into-power-bi"></a>Power BI'a veri çekmek için Elektronik raporlamayı yapılandır

[!include[banner](../includes/banner.md)]


Bu konu, verilerinizi Finance and Operations kurulumunuzdan Power BI hizmetlerine aktarmak amacıyla düzenlemek için Elektronik raporlama (ER) yapılandırmanızı nasıl kullanacağınızı açıklar. Örnek olarak, bu konu Intrastat hareketlerini aktarılması gereken iş verileri olarak kullanır. Power BI harita görselleştirmesi, bu Intrastat hareket verilerini şirketin içe aktarma/dışa aktarma etkinliklerinin Power BI raporundaki analizinin bir görünümünü sunmak için kullanır.

<a name="overview"></a>Özet
--------

Microsoft Power BI harici veri kaynaklarını tutarlı, görsel olarak modern ve etkileşimli bilgilere dönüştürmek için birlikte çalışan yazılım hizmetleri, uygulamalar ve bağlayıcılardan oluşan bir koleksiyondur. Elektronik raporlama (ER), Microsoft Dynamics 365 for Finance and Operations kullanıcılarının veri kaynaklarını kolaylıkla yapılandırmasına ve Finance and Operations'tan Power BI'ya veri aktarımını düzenlemesine olanak tanır. Veriler OpenXML çalışma sayfası (Microsoft Excel çalışma kitabı dosyası) biçiminde aktarılır. Aktarılan dosyalar bu amaçla yapılandırılmış bir Microsoft SharePoint Server üzerinde depolanır. Depolanan dosyalar görselleştirme (tablo, grafik, harita vs.) içeren raporlar oluşturmak için Power BI'da kullanılır. Power BI raporları Power BI kullanıcılarıyla paylaşılır ve bunlara Power BI panoları ve Finance and Operations sayfalarından ulaşılır. Bu konuda aşağıdaki görevler açıklanmıştır:

-   Finance and Operations'ı yapılandır.
-   ER biçim yapılandırmanızı Finance and Operations uygulamasından veri almak için hazırlayın.
-   ER ortamını Power BI'ya veri aktarmak için yapılandırın.
-   Power BI raporu oluşturmak için aktarılan verileri kullanın.
-   Power BI raporunu Finance and Operations'da erişilebilir hale getirin.

## <a name="prerequisites"></a>Ön koşullar
Bu konudaki örneği tamamlamak için şu erişimlere sahip olmanız gerekir:

-   Aşağıdaki rollerden biri için Finance and Operations'a erişim:
    -   Elektronik raporlama geliştirici
    -   Elektronik raporlama işlev danışmanı
    -   Sistem yöneticisi
-   Finance and Operations ile kullanılmak için yapılandırılmış SharePoint Server erişimi
-   Power BI çerçevesine erişim

## <a name="configure-document-management-parameters"></a>Belge yönetim parametrelerini yapılandırın
1.  **Belge yönetim parametreleri** sayfasında, oturum açtığınız şirkette (bu örnekte DEMF şirketi) kullanılacak SharePoint Server erişimini yapılandırın.
2.  Size erişim verildiğinden emin olmak için SharePoint Server bağlantısını test edin. [![Belge yönetim parametreleri sayfası](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Yapılandırılmış SharePoint sitesini açın. ER'nin Power BI raporlarının bir Power BI veri kümesi kaynağı olarak gerektirdiği iş verilerine sahip olan Excel dosyalarını depolamak üzere yeni bir klasör oluşturun.
4.  Finance and Operations uygulamasında, **Belge türleri** sayfasında, yeni oluşturduğunuz SharePoint klasörüne erişmek için kullanılacak yeni bir belge türü oluşturun. **Grup** alanında **Dosya** ve **Konum** alanında **SharePoint** girin ve SharePoint klasörünün adresini yazın. [![Belge türleri sayfası](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma
1.  **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri** bağlantısına tıklayın.
2.  **Ekler** sekmesinde, tüm alanlar için **Dosya** belge türünü seçin.
3.  **Elektronik raporlama** çalışma alanında, **Etkin olarak ayarla**'ya tıklayarak gerekli sağlayıcıyı etkin hale getirin. Daha fazla bilgi için **ER Hizmet sağlayıcısı seçme** görev kılavuzunu oynatın.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>ER veri modelini veri kaynağı olarak kullanma
Power BI raporlarında kullanılacak iş verileri kaynağı olarak bir ER veri modeliniz olmalıdır. Bu veri modeli ER yapılandırmaları deposundan yüklenir. Daha fazla bilgi için [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükleme](download-electronic-reporting-configuration-lcs.md) bölümüne bakın veya **ER Lifecycle Services'tan bir yapılandırmayı içe aktarma** görev kılavuzunu oynatın. Seçili ER yapılandırmaları deposundan karşıya yüklenecek veri modeli olarak **Intrastat**'ı seçin. (Bu örnekte, modelin 1. sürümü kullanılır.) Daha sonra **Intrastat** ER model yapılandırmasına **Yapılandırmalar** sayfasından erişebilirsiniz. [![Yapılandırmalar sayfası](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>ER biçimi yapılandırması tasarlama
İş verilerinin kaynağı olarak **Intrastat** veri modelini kullanan yeni bir ER biçimi yapılandırması oluşturmanız gerekir. Bu biçim yapılandırması çıktı sonuçlarını OpenXML (Excel dosyası) biçiminde elektronik belgeler olarak oluşturmalıdır. Daha fazla bilgi için **ER Raporlar için OPENXML biçiminde bir konfigürasyon oluşturma** görev kılavuzunu oynatın. Yeni yapılandırmayı, aşağıdaki çizimde gösterildiği gibi, **İçe aktarma / dışa aktarma etkinlikleri** olarak adlandırın. ER biçimini tasarlarken şablon olarak [ER verileri - içe aktarma ve dışa aktarma ayrıntıları](https://go.microsoft.com/fwlink/?linkid=845208) adlı Excel dosyasını kullanın. (Bir biçim şablonunu içe aktarmak hakkında daha fazla bilgi için, görev kılavuzunu oynatın.) [![İçe / dışa aktarma etkinlikleri yapılandırması](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) **İçe / dışa aktarma etkinlikleri** biçim yapılandırmasını değiştirmek için şu adımları izleyin.

1.  **Tasarımcı**'ya tıklayın.
2.  **Biçim** sekmesinde, bu biçime ait dosya öğesini **Excel çıktı dosyası** olarak adlandırın. [![Excel çıktı dosyası öğesi](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  **Eşleme** sekmesinde, bu biçim her çalıştırıldığında oluşturulacak Excel dosyasının adını belirtin. İlgili ifadeyi **İçe aktarma ve dışa aktarma ayrıntıları** değerini döndürecek şekilde yapılandırın (.xlsx dosya adı uzantısı otomatik olarak eklenir). [![Biçim tasarımcısı](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Bu biçim için yeni bir veri kaynağı öğesi ekleyin. (Bu numaralandırma daha fazla veri bağlaması için gereklidir.)
    1.  Veri kaynağını **direction\_enum** olarak adlandırın.
    2.  Veri kaynağı türü olarak **Veri modeli numaralandırması**'nı seçin.
    3.  **Yön** veri modeli numaralandırmasına başvurun.

    [![direction\_enum](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  **Intrastat** veri modelinin öğeleri ile tasarlanan biçimin öğelerini bağlama işlemini, aşağıdaki çizimde gösterildiği gibi tamamlayın. [![Bağı tamamlamak](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

ER biçimi çalıştırıldıktan sonra çıktı sonucunu Excel biçiminde üretir. Intrastat hareketlerinin ayrıntılarını çıktı sonucuna gönderir ve bunları içe aktarma etkinliklerini veya dışa aktarma etkinliklerini açıklayan hareketler olarak ayırır. **Intrastat** sayfasındaki Intrastat hareketlerinin listesi için yeni ER biçimini test etmek üzere **Çalıştır**'a tıklayın (**Vergi** &gt; **Bildirimler** &gt; **Dış ticaret** &gt; **Intrastat**). [![Intrastat sayfası](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) Aşağıdaki çıktı sonucu oluşturulur. Dosya biçim ayarlarında belirttiğiniz gibi,**İçe aktarma ve dışa aktarma ayrıntıları.xlsx** olarak adlandırılır. [![İçe aktarma ve dışa aktarma ayrıntıları.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER hedefini yapılandırma
Yeni ER biçimi yapılandırmasının çıktı sonucunu özel bir şekilde göndermek için ER çerçevesini yapılandırmanız gerekir.

-   Çıktı sonucu seçili SharePoint Server klasörüne gönderilmelidir.
-   Biçim yapılandırması her yürütüldüğünde aynı Excel dosyasının yeni bir sürümü oluşturulmalıdır.

**Elektronik raporlama** sayfasında (**Organizasyon yönetimi** &gt; **Elektronik raporlama**), **Elektronik raporlama hedefi** öğesine tıklayın ve yeni bir hedef ekleyin. **Referans** alanında, önceden oluşturduğunuz **İçe aktarma / dışa aktarma etkinlikleri** biçimi yapılandırmasını seçin. Referans için yeni bir dosya hedefi kaydı eklemek üzere aşağıdaki adımları izleyin.

1.  **Ad** alanına dosya hedefinin başlığını girin.
2.  **Dosya adı** alanında, Excel dosya biçimi bileşeni için **Excel çıktı dosyası** adını seçin.

Yeni hedef kaydı için **Ayarlar** düğmesine tıklayın. Daha sonra, **Hedef ayarları** iletişim kutusunda, aşağıdaki adımları izleyin.

1.  **Power BI** sekmesinde, **Etkin** seçeneğini **Evet** olarak ayarlayın.
2.  **SharePoint** alanında, önceden oluşturduğunuz **Paylaşılan** belge türünü seçin.

## <a name="schedule-execution-of-the-configured-er-format"></a>Yapılandırılmış ER biçiminin yürütülmesini planlama
**Yapılandırmalar** sayfasında (**Organizasyon yönetimi** &gt; **Elektronik raporlama** &gt; **Yapılandırmalar**), yapılandırmalar ağacından önceden oluşturduğunuz **İçe aktarma / dışa aktarma etkinlikleri** yapılandırmasını seçin. 1.1 sürümünün durumunu **Taslak**'tan **Tamamlandı** olarak değiştirerek bu biçimi kullanılabilir hale getirin. [![Yapılandırmalar sayfası](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) **İçe aktarma / dışa aktarma etkinlikleri** yapılandırmasının tamamlanmış sürümünü seçin ve **Çalıştır**'a tıklayın. Yapılandırılan hedefin Excel biçiminde üretilen çıktı sonucuna uygulandığına dikkat edin. Bu raporu katılımsız modda çalıştırmak için **Toplu işleme** seçeneğini **Evet** olarak ayarlayın. Bu toplu iş yürütmesinin gerekli yinelemelerini planlamak için **Tekrar**'a tıklayın. Yineleme, güncelleştirilen verilerin Finance and Operations uygulamasından Power BI'ya ne kadar sıklıkla aktarılacağını belirler. [![Elektronik rapor parametreleri iletişim kutusu](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) Yapılandırıldıktan sonra, ER raporu yürütme işini **Toplu işler** sayfasında (**Sistem yönetimi &gt; Sorgulamalar &gt; Toplu işler**) bulabilirsiniz. [![Toplu işler sayfası](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) Bu iş ilk kez çalıştırıldığında hedef, seçili SharePoint klasöründe yapılandırılan ada sahip yeni bir Excel dosyası oluşturur. İşin sonraki her çalıştırılmasında, hedef bu Excel dosyasının yeni bir sürümünü oluşturur. [![Excel dosyasının yeni sürümü](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>ER biçiminin çıktı sonucunu kullanarak bir Power BI veri kümesi oluşturma
Power BI'da oturum açın ve var olan bir Power BI grubunu (çalışma alanı) açın veya yeni bir grup oluşturun. **İçe Aktarma veya Verilere Bağlanma** bölümünde, **Dosyalar** altında **Ekle**'ye tıklayın veya sol bölmede **Veri kümeleri**'nin yanındaki artı işaretine (**+**) tıklayın. [![Bir veri seti oluşturmak](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) **SharePoint – Ekip siteleri** seçeneğini belirleyin ve kullandığınız SharePoint Server yolunu girin (örneğimizde **https://ax7partner.spoppe.com**). Daha sonra **/Shared Documents/GER data/PowerBI** klasörüne gidin ve yeni Power BI veri kümesinin veri kaynağı olarak oluşturduğunuz Excel dosyasını seçin. [![Excel dosyasını seçmek](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) **Bağlan**'ı tıklatın ve sonra **İçe aktarma**'yı tıklatın. Seçili Excel dosyasını temel alan yeni bir veri kümesi oluşturulur. Veri kümesi yeni oluşturulan panoya da otomatik olarak eklenebilir. [![Panodaki veri seti](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) Periyodik güncelleştirmeyi zorlamak amacıyla bu veri kümesi için yenileme zamanlamasını yapılandırın. Periyodik güncelleştirmeler, ER raporunun SharePoint Server'da oluşturulan Excel dosyasının yeni sürümleri üzerinden periyodik olarak yürütülmesi aracılığıyla Finance and Operations uygulamasından gelen yeni iş verilerinin kullanılabilmesini sağlar.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Yeni veri kümesini kullanarak Power BI raporu oluşturun
Yeni bir Power BI raporu oluşturmak için, oluşturduğunuz **İçe aktarma ve dışa aktarma ayrıntıları** Power BI veri kümesine tıklayın. Daha sonra görselleştirmeyi yapılandırın. Örneğin, **Dolgulu harita** görselleştirmesini seçin ve aşağıdaki şekilde yapılandırın:

-   Harita görselleştirmesinin **Konum** alanına **CountryOrigin** veri kümesi alanını atayın.
-   Harita görselleştirmesinin **Renk doygunluğu** alanına **Miktar** veri kümesi alanını atayın.
-   Harita görselleştirmesinin **Filtreler** alanları koleksiyonuna **Etkinlik** ve **Yıl** veri kümesi alanlarını ekleyin.

Power BI raporunu **İçe aktarma ve dışa aktarma ayrıntıları raporu** olarak kaydedin. [![Ayrıntılar raporu içe ve dışa aktarmak](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) Haritanın Excel dosyasında belirtilen ülkeleri/bölgeleri (bu örnekte Avusturya ve İsviçre) gösterdiğine dikkat edin. Bu ülkeler/bölgeler her biri için faturalanan miktarların oranını gösterecek şekilde renklendirilmiştir. Intrastat hareketlerin listesini güncelleştirin. İtalya'dan kaynaklanan dışa aktarma hareketi eklendi. [![Intrastat hareketler listesi](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) ER raporunun bir sonraki planlanan yürütülmesini ve Power BI veri kümesinin bir sonraki planlanan güncelleştirmesini bekleyin. Daha sonra, Power BI raporunu inceleyin (yalnızca içe aktarma hareketlerini göstermeyi seçin). Güncelleştirilen harita artık İtalya'yı göstermektedir. [![Güncelleştirilen harita](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-finance-and-operations"></a>Power BI raporunu Finance and Operations'da erişilebilir hale getirin.
Finance and Operations ve Power BI arasındaki tümleştirmeyi ayarlayın. Daha fazla bilgi için bkz. [Çalışma alanları için Power BI tümleştirmesini yapılandırma](configure-power-bi-integration.md). Power BI tümleştirmesini destekleyen **Elektronik raporlama** çalışma alanı sayfasında (**Organizasyon yönetimi** &gt; **Çalışma alanları** &gt; **Elektronik raporlama çalışma alanı**), **Seçenekler** &gt; **Rapor kataloğunu aç**'a tıklayın. Oluşturduğunuz **İçe aktarma ve dışa aktarma ayrıntıları** Power BI raporunu seçili sayfada bir eylem öğesi olarak göstermek için raporu seçin. Power BI'da tasarladığınız raporu gösteren Finance and Operations sayfasını açmak için eylem öğesine tıklayın. [![İçe aktarma ve dışa aktarma ayrıntıları raporu](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Ayrıca bkz.
--------

[Elektronik raporlama hedefleri](electronic-reporting-destinations.md)

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)




