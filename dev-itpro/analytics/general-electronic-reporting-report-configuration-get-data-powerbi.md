---
title: "Elektronik güç BI verilerle Dynamics 365 işlemleri için sağlamak için raporlama ayarlayın"
description: "Bu konu, verilerinizi Dynamics 365 for Operations kurulumunuzdan Power BI hizmetlerine aktarmak amacıyla düzenlemek için Elektronik raporlama (ER) yapılandırmanızı nasıl kullanacağınızı açıklar. Örnek olarak, bu konu Intrastat hareketlerini aktarılması gereken iş verileri olarak kullanır. Power BI harita görselleştirmesi, bu Intrastat hareket verilerini şirketin içe aktarma/dışa aktarma etkinliklerinin Power BI raporundaki analizinin bir görünümünü sunmak için kullanır."
author: kfend
manager: AnnBe
ms.date: 2016-10-31 13 - 22 - 29
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: ed0192c44b6d7e88120c64e539ebb0ac3b379831
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-electronic-reporting-to-provide-power-bi-with-data-from-dynamics-365-for-operations"></a>Elektronik güç BI verilerle Dynamics 365 işlemleri için sağlamak için raporlama ayarlayın

Bu konu, verilerinizi Dynamics 365 for Operations kurulumunuzdan Power BI hizmetlerine aktarmak amacıyla düzenlemek için Elektronik raporlama (ER) yapılandırmanızı nasıl kullanacağınızı açıklar. Örnek olarak, bu konu Intrastat hareketlerini aktarılması gereken iş verileri olarak kullanır. Power BI harita görselleştirmesi, bu Intrastat hareket verilerini şirketin içe aktarma/dışa aktarma etkinliklerinin Power BI raporundaki analizinin bir görünümünü sunmak için kullanır.

<a name="overview"></a>Özet
--------

Microsoft Power BI harici veri kaynaklarını tutarlı, görsel olarak modern ve etkileşimli bilgilere dönüştürmek için birlikte çalışan yazılım hizmetleri, uygulamalar ve bağlayıcılardan oluşan bir koleksiyondur. Elektronik raporlama (ER), Microsoft Dynamics 365 for Operations kullanıcılarının veri kaynaklarını kolaylıkla yapılandırmasına ve Dynamics 365 for Operations'tan Power BI'ya veri aktarımını düzenlemesine olanak tanır. Veriler OpenXML çalışma sayfası (Microsoft Excel çalışma kitabı dosyası) biçiminde aktarılır. Aktarılan dosyalar bu amaçla yapılandırılmış bir Microsoft SharePoint Server üzerinde depolanır. Depolanan dosyalar görselleştirme (tablo, grafik, harita vs.) içeren raporlar oluşturmak için Power BI'da kullanılır. Power BI raporları Power BI kullanıcılarıyla paylaşılır ve bunlara Power BI panoları ve Dynamics 365 for Operations sayfalarından ulaşılır. Bu konuda aşağıdaki görevler açıklanmıştır:

-   Dynamics 365 for Operations uygulamasını yapılandırın.
-   ER biçim yapılandırmanızı Dynamics 365 for Operations uygulamasından veri almak için hazırlayın.
-   ER ortamını Power BI'ya veri aktarmak için yapılandırın.
-   Power BI raporu oluşturmak için aktarılan verileri kullanın.
-   Power BI raporunu Dynamics 365 for Operations'da erişilebilir hale getirin.

## <a name="prerequisites"></a>Önkoşullar
Bu konudaki örneği tamamlamak için şu erişimlere sahip olmanız gerekir:

-   Aşağıdaki rollerden biri için Dynamics 365 for Operations'a erişim:
    -   Elektronik raporlama geliştirici
    -   Elektronik raporlama işlev danışmanı
    -   Sistem yöneticisi
-   Dynamics 365 for Operations ile kullanılmak için yapılandırılmış SharePoint Server erişimi
-   Power BI çerçevesine erişim

## <a name="configure-document-management-parameters"></a>Belge yönetim parametrelerini yapılandırın
1.  **Belge yönetim parametreleri** sayfasında, oturum açtığınız şirkette (bu örnekte DEMF şirketi) kullanılacak SharePoint Server erişimini yapılandırın.
2.  Size erişim verildiğinden emin olmak için SharePoint Server bağlantısını test edin. [![Belge yönetim parametreleri sayfası](./media/ger-power-bi-sharepoint-server-setting-1024x369.png)](./media/ger-power-bi-sharepoint-server-setting.png)
3.  Yapılandırılmış SharePoint sitesini açın. ER'nin Power BI raporlarının bir Power BI veri kümesi kaynağı olarak gerektirdiği iş verilerine sahip olan Excel dosyalarını depolamak üzere yeni bir klasör oluşturun.
4.  Dynamics 365 for Operations uygulamasında, **Belge türleri** sayfasında, yeni oluşturduğunuz SharePoint klasörüne erişmek için kullanılacak yeni bir belge türü oluşturun. **Grup** alanında **Dosya** ve **Konum** alanında **SharePoint** girin ve SharePoint klasörünün adresini yazın. [![Belge türleri sayfası](./media/ger-power-bi-sharepoint-document-type-1024x485.png)](./media/ger-power-bi-sharepoint-document-type.png)

## <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma
1.  **Elektronik raporlama** çalışma alanında, **Elektronik raporlama parametreleri** bağlantısına tıklayın.
2.  **Ekler** sekmesinde, tüm alanlar için **Dosya** belge türünü seçin.
3.  **Elektronik raporlama** çalışma alanında, **Etkin olarak ayarla**'ya tıklayarak gerekli sağlayıcıyı etkin hale getirin. Daha fazla bilgi için **ER Hizmet sağlayıcısı seçme** görev kılavuzunu oynatın.

## <a name="use-an-er-data-model-as-the-source-of-data"></a>ER veri modelini veri kaynağı olarak kullanma
Power BI raporlarında kullanılacak iş verileri kaynağı olarak bir ER veri modeliniz olmalıdır. Bu veri modeli ER yapılandırmaları deposundan yüklenir. Daha fazla bilgi için [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını karşıdan yükleme](download-electronic-reporting-configuration-lcs.md) bölümüne bakın veya **ER Lifecycle Services'tan bir yapılandırmayı içe aktarma** görev kılavuzunu oynatın. Seçili ER yapılandırmaları deposundan karşıya yüklenecek veri modeli olarak **Intrastat**'ı seçin. (Bu örnekte, sürüm 1 modelinin kullanılır.) Daha sonra erişebilirsiniz **Intrastat** ER modeli yapılandırmasına **yapılandırmaları** sayfa. [![Yapılandırma sayfası](./media/ger-power-bi-data-model-1024x371.png)](./media/ger-power-bi-data-model.png)

## <a name="design-an-er-format-configuration"></a>ER biçimi yapılandırması tasarlama
İş verilerinin kaynağı olarak **Intrastat** veri modelini kullanan yeni bir ER biçimi yapılandırması oluşturmanız gerekir. Bu biçim yapılandırması çıktı sonuçlarını OpenXML (Excel dosyası) biçiminde elektronik belgeler olarak oluşturmalıdır. Daha fazla bilgi için **ER Raporlar için OPENXML biçiminde bir konfigürasyon oluşturma** görev kılavuzunu oynatın. Yeni yapılandırmayı, aşağıdaki çizimde gösterildiği gibi, **İçe aktarma / dışa aktarma etkinlikleri** olarak adlandırın. ER biçimini tasarlarken şablon olarak [ER verileri - içe aktarma ve dışa aktarma ayrıntıları](https://go.microsoft.com/fwlink/?linkid=845208) adlı Excel dosyasını kullanın. (Biçim şablonu alma hakkında daha fazla bilgi için görev Kılavuzu oynamak.) [![Alma / aktiviteleri yapılandırmasını ver](media/ger-power-bi-format-configuration.png)](media/ger-power-bi-format-configuration.png) değiştirmek için **alma / export aktiviteleri** yapılandırma biçimi, aşağıdaki adımları izleyin.

1.  **Tasarımcı**'ya tıklayın.
2.  **Biçim** sekmesinde, bu biçime ait dosya öğesini **Excel çıktı dosyası** olarak adlandırın. [![Excel, çıktı dosya öğesi](./media/ger-power-bi-format-configuration-file-element-name-1024x395.png)](./media/ger-power-bi-format-configuration-file-element-name.png)
3.  **Eşleme** sekmesinde, bu biçim her çalıştırıldığında oluşturulacak Excel dosyasının adını belirtin. İlgili ifadeyi **İçe aktarma ve dışa aktarma ayrıntıları** değerini döndürecek şekilde yapılandırın (.xlsx dosya adı uzantısı otomatik olarak eklenir). [![Format designer](./media/ger-power-bi-format-configuration-output-file-name-1024x396.png)](./media/ger-power-bi-format-configuration-output-file-name.png)
4.  Bu biçim için yeni bir veri kaynağı öğesi ekleyin. (Bu numaralandırma daha fazla veri bağlaması için gereklidir.)
    1.  Veri kaynağı adı **yön\_enum**.
    2.  Veri kaynağı türü olarak **Veri modeli numaralandırması**'nı seçin.
    3.  **Yön** veri modeli numaralandırmasına başvurun.

    [![Yön\_numaralandırma](./media/ger-power-bi-format-configuration-mapping-added-enum-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-added-enum.png)
5.  **Intrastat** veri modelinin öğeleri ile tasarlanan biçimin öğelerini bağlama işlemini, aşağıdaki çizimde gösterildiği gibi tamamlayın. [![Bağlama Tamamlanıyor](./media/ger-power-bi-format-configuration-mapping-details-1024x454.png)](./media/ger-power-bi-format-configuration-mapping-details.png)

ER biçimi çalıştırıldıktan sonra çıktı sonucunu Excel biçiminde üretir. Intrastat hareketlerinin ayrıntılarını çıktı sonucuna gönderir ve bunları içe aktarma etkinliklerini veya dışa aktarma etkinliklerini açıklayan hareketler olarak ayırır. ' I **çalıştırmak** Intrastat hareketlerin listesini yeni ER biçimi üzerinde test etmek için **Intrastat** sayfa (**vergi**&gt;**bildirimleri**&gt;**dış ticaret**&gt;**Intrastat**). [![Intrastat sayfası](./media/ger-power-bi-format-test-run-transactions-1024x322.png)](./media/ger-power-bi-format-test-run-transactions.png) aşağıdaki sonucu çıktı oluşturulur. Dosya biçim ayarlarında belirttiğiniz gibi,**İçe aktarma ve dışa aktarma ayrıntıları.xlsx** olarak adlandırılır. [![Alma ve verme details.xlsx](./media/ger-power-bi-format-test-run-output-1024x472.png)](./media/ger-power-bi-format-test-run-output.png)

## <a name="configure-the-er-destination"></a>ER hedefini yapılandırma
Yeni ER biçimi yapılandırmasının çıktı sonucunu özel bir şekilde göndermek için ER çerçevesini yapılandırmanız gerekir.

-   Çıktı sonucu seçili SharePoint Server klasörüne gönderilmelidir.
-   Biçim yapılandırması her yürütüldüğünde aynı Excel dosyasının yeni bir sürümü oluşturulmalıdır.

Üzerinde **elektronik raporlama** sayfa (**kuruluş yönetim**&gt;**elektronik raporlama**),'ı **elektronik raporlama hedef** madde ve yeni bir hedef ekleyin. **Referans** alanında, önceden oluşturduğunuz **İçe aktarma / dışa aktarma etkinlikleri** biçimi yapılandırmasını seçin. Referans için yeni bir dosya hedefi kaydı eklemek üzere aşağıdaki adımları izleyin.

1.  **Ad** alanına dosya hedefinin başlığını girin.
2.  **Dosya adı** alanında, Excel dosya biçimi bileşeni için **Excel çıktı dosyası** adını seçin.

Yeni hedef kaydı için **Ayarlar** düğmesine tıklayın. Daha sonra, **Hedef ayarları** iletişim kutusunda, aşağıdaki adımları izleyin.

1.  **Power BI** sekmesinde, **Etkin** seçeneğini **Evet** olarak ayarlayın.
2.  **SharePoint** alanında, önceden oluşturduğunuz **Paylaşılan** belge türünü seçin.

## <a name="schedule-execution-of-the-configured-er-format"></a>Yapılandırılmış ER biçiminin yürütülmesini planlama
Üzerinde **yapılandırmaları** sayfa (**kuruluş yönetim**&gt;**elektronik raporlama**&gt;**yapılandırmaları**), yapılandırmaları ağacında seçin **alma / export aktiviteleri** daha önce oluşturduğunuz yapılandırma. 1.1 sürümünün durumunu **Taslak**'tan **Tamamlandı** olarak değiştirerek bu biçimi kullanılabilir hale getirin. [![Yapılandırma sayfası](./media/ger-power-bi-format-configuration-complete-1024x401.png)](./media/ger-power-bi-format-configuration-complete.png) tamamlanmış sürümünü seçin **alma / export aktiviteleri** yapılandırma ve sonra **çalıştırmak**. Yapılandırılan hedefin Excel biçiminde üretilen çıktı sonucuna uygulandığına dikkat edin. Bu raporu katılımsız modda çalıştırmak için **Toplu işleme** seçeneğini **Evet** olarak ayarlayın. Bu toplu iş yürütmesinin gerekli yinelemelerini planlamak için **Tekrar**'a tıklayın. Yineleme, güncelleştirilen verilerin Dynamics 365 for Operations uygulamasından Power BI'ya ne kadar sıklıkla aktarılacağını belirler. [![Elektronik rapor parametreleri iletişim kutusu](./media/ger-power-bi-format-configuration-run-to-schedule-1024x413.png)](./media/ger-power-bi-format-configuration-run-to-schedule.png) yapılandırması tamamlandıktan sonra üzerinde ER rapor yürütme iş bulabilirsiniz **toplu işleri** sayfa (**Sistem Yönetimi &gt;sorguları &gt;toplu işleri**). [![Toplu işleri sayfası](./media/ger-power-bi-format-configuration-running-job-1024x410.png)](./media/ger-power-bi-format-configuration-running-job.png) bu işi ilk kez çalıştırdığınızda, hedef seçilen SharePoint klasöründe yapılandırılan bir adı olan yeni bir Excel dosyası oluşturur. İşin sonraki her çalıştırılmasında, hedef bu Excel dosyasının yeni bir sürümünü oluşturur. [![Excel dosyasının yeni sürümü](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2-1024x412.png)](./media/ger-power-bi-output-file-in-sharepoint-server-folder-2.png)

## <a name="create-a-power-bi-dataset-by-using-the-output-result-of-the-er-format"></a>ER biçiminin çıktı sonucunu kullanarak bir Power BI veri kümesi oluşturma
Power BI'da oturum açın ve var olan bir Power BI grubunu (çalışma alanı) açın veya yeni bir grup oluşturun. İ **Ekle** altında **dosyaları** içinde **alma veya verilere bağlanma** bölüm veya artı işaretini tıklatın (**+**) yanında **DataSet** sol bölmede. [![Bir dataset oluşturma](./media/ger-power-bi-add-dataset-1024x524.png)](./media/ger-power-bi-add-dataset.png) seçin **SharePoint – ekip siteleri** seçeneğini ve sonra kullanmakta olduğunuz SharePoint sunucusunun yolunu girin (**https://ax7partner.spoppe.com** örneğimizde). Daha sonra **/Shared Documents/GER data/PowerBI** klasörüne gidin ve yeni Power BI veri kümesinin veri kaynağı olarak oluşturduğunuz Excel dosyasını seçin. [![Excel dosyasını seçerek](./media/ger-power-bi-add-dataset-select-excel-file-1024x522.png)](./media/ger-power-bi-add-dataset-select-excel-file.png) 'ı **Bağlan**ı **alma**. Seçili Excel dosyasını temel alan yeni bir veri kümesi oluşturulur. Veri kümesi yeni oluşturulan panoya da otomatik olarak eklenebilir. [![Pano üzerindeki DataSet](./media/ger-power-bi-added-dataset-1024x489.png)](./media/ger-power-bi-added-dataset.png) düzenli güncelleştirme zorlamak bu veri kümesi için yenileme zamanlaması yapılandırmak. Periyodik güncelleştirmeler, ER raporunun SharePoint Server'da oluşturulan Excel dosyasının yeni sürümleri üzerinden periyodik olarak yürütülmesi aracılığıyla Dynamics 365 for Operations uygulamasından gelen yeni iş verilerinin kullanılabilmesini sağlar.

## <a name="create-a-power-bi-report-by-using-the-new-dataset"></a>Yeni veri kümesini kullanarak Power BI raporu oluşturun
Yeni bir Power BI raporu oluşturmak için, oluşturduğunuz **İçe aktarma ve dışa aktarma ayrıntıları** Power BI veri kümesine tıklayın. Daha sonra görselleştirmeyi yapılandırın. Örneğin, **Dolgulu harita** görselleştirmesini seçin ve aşağıdaki şekilde yapılandırın:

-   Harita görselleştirmesinin **Konum** alanına **CountryOrigin** veri kümesi alanını atayın.
-   Harita görselleştirmesinin **Renk doygunluğu** alanına **Miktar** veri kümesi alanını atayın.
-   Harita görselleştirmesinin **Filtreler** alanları koleksiyonuna **Etkinlik** ve **Yıl** veri kümesi alanlarını ekleyin.

Power BI raporunu **İçe aktarma ve dışa aktarma ayrıntıları raporu** olarak kaydedin. [![Alma ve verme Ayrıntıları raporu](./media/ger-power-bi-added-report-1024x498.png)](./media/ger-power-bi-added-report.png) map (Avusturya ve İsviçre'de bu örnek) Excel dosyasında belirtilen ülkeler/bölgeler gösterdiğine dikkat edin. Bu ülkeler/bölgeler her biri için faturalanan miktarların oranını gösterecek şekilde renklendirilmiştir. Intrastat hareketlerin listesini güncelleştirin. İtalya'dan kaynaklanan dışa aktarma hareketi eklendi. [![Intrastat hareketlerinin listesi](./media/ger-power-bi-new-run-new-transaction-1024x321.png)](./media/ger-power-bi-new-run-new-transaction.png) ER rapor sonraki zamanlanmış yürütülmesini ve bir sonraki zamanlanmış güncelleştirmede güç BI veri kümesi için bekleyin. Daha sonra, Power BI raporunu inceleyin (yalnızca içe aktarma hareketlerini göstermeyi seçin). Güncelleştirilen harita artık İtalya'yı göstermektedir. [![Güncelleştirilmiş Haritası](./media/ger-power-bi-new-run-new-map-1024x511.png)](./media/ger-power-bi-new-run-new-map.png)

## <a name="access-power-bi-report-in-dynamics-365-for-operations"></a>Power BI raporuna Dynamics 365 for Operations'da erişme
Dynamics 365 for Operations ve Power BI arasındaki tümleştirmeyi ayarlayın. Daha fazla bilgi için bkz. [Çalışma alanları için Power BI tümleştirmesini yapılandırma](configure-power-bi-integration.md). Üzerinde **elektronik raporlama** güç BI tümleşmesini destekler çalışma sayfası (**kuruluş yönetim**&gt;**çalışma**&gt;**elektronik raporlama çalışma**),'ı **seçenekleri**&gt;**açık rapor katalog**. Oluşturduğunuz **İçe aktarma ve dışa aktarma ayrıntıları** Power BI raporunu seçili sayfada bir eylem öğesi olarak göstermek için raporu seçin. Power BI'da tasarladığınız raporu gösteren Dynamics 365 for Operations sayfasını açmak için eylem öğesine tıklayın. [![Alma ve verme Ayrıntıları raporu](./media/ger-power-bi-review-bi-report-in-ax-form-1024x586.png)](./media/ger-power-bi-review-bi-report-in-ax-form.png)

<a name="see-also"></a>Ayrıca bkz.
--------

[Elektronik raporlama hedefleri](electronic-reporting-destinations.md)

[Elektronik raporlamaya genel bakış](general-electronic-reporting.md)


