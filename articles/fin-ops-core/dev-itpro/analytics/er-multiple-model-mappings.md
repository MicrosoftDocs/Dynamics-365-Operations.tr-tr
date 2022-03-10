---
title: Tek bir model kökü için türetilmiş eşlemeleri yönetme
description: Bu konuda, tek bir model kökü için yapılandırılmış birden fazla türetilmiş eşlemenin nasıl yönetileceği açıklanmaktadır.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d71b05b3f2eda93a93f728926e675c040371781e
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324124"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Tek bir model kökü için türetilmiş eşlemeleri yönetme

[!include [banner](../includes/banner.md)]

[Elektronik raporlama (ER)](general-electronic-reporting.md) veri modeli bileşeni, giden belgeler oluşturmak için her yapılandırılmış ER biçimi bileşeninde veri kaynağı olarak kullanılır. Tek bir işletme etki alanını açıklamak için, birçok kök tanımına sahip bir veri modeli bileşeni yapılandırın. 

Her kök tanımı, söz konusu etki alanının verilerini belirli bir raporlama amacına en uygun şekilde göstermenize olanak sağlar. Her kök tanımı için, bir ER model eşleme bileşenini veri modelinizin Microsoft Dynamics 365 Finance'a özgü uygulaması olarak yapılandırabilirsiniz. Bu şekilde, veri modelinizin çalışma zamanında nasıl doldurulacağını açıklarsınız.

ER model eşleme bileşenleri ER veri modeli [yapılandırmalarında](general-electronic-reporting.md#Configuration) ve ER model eşleme yapılandırmalarında bulunabilir. Tek bir ER yapılandırması, her biri tek bir kök tanımı için yapılandırılan birçok eşleme bileşeni içerebilir. Alternatif olarak, tek bir ER yapılandırması tek bir kök tanımı için yapılandırılan yalnızca tek bir eşleme bileşeni içerebilir.

Birçok yapılandırma sağlayıcısı aynı ER veri modeli için ER model eşleme yapılandırmaları sunabilir. Bu model eşleme yapılandırmaları, farklı kök tanımlarının eşleme bileşenlerini içerebilir. Bir [sağlayıcı](general-electronic-reporting.md#Provider) tarafından sunulan bir kök tanımı için model eşleme kullanıyor ve başka bir sağlayıcı tarafından sunulan başka bir kök tanımı için bir model eşleme kullanıyor olabilirsiniz.

Bu konudaki yordamlar, aynı kök tanımı için yapılandırılan farklı model eşleme bileşenleri içeren ER veri modelinin birden fazla ER model eşleme yapılandırmasının nasıl yönetileceği açıklanmaktadır. 

Bu konudaki yordamları tamamlamak için Sistem yöneticisi veya Elektronik raporlama geliştiricisi rolüne atanmanız gerekir.

Aşağıdaki yordamların tümü USMF şirketinde yapılabilir. Kodlama gerekmez.

## <a name="configure-the-er-framework"></a>ER altyapısını yapılandırma

Elektronik raporlama geliştiricisi rolüne sahip bir kullanıcı olarak, iş belgeleri oluşturmak için ER çerçevesini kullanmaya başlamadan önce [minimum ER parametreleri kümesini yapılandırmanız](er-quick-start2-customize-report.md#ConfigureFramework) gerekir.

## <a name="import-the-standard-er-format-configurations"></a>Standart ER biçimi yapılandırmalarını içe aktarın

Geçerli Finance kurulumunuza standart ER yapılandırmalarını eklemek için bu yapılandırmaları o kurulum için yapılandırılmış olan ER deposundan içe aktarmanız gerekir. Aşağıdaki ER biçimi yapılandırmalarını içeri aktarmak için [Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indirme](er-download-configurations-global-repo.md) konusundaki adımları izleyin.

- **Serbest metin faturası (Excel)**, sürüm 220.106
- **Proje faturası (Excel)**, sürüm 226.27

## <a name="review-the-imported-er-configurations"></a>İçe aktarılan ER yapılandırmalarını gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Fatura modeli**'ni genişletin.

    ![Yapılandırmalar sayfasında içeri aktarılan yapılandırmaları inceleme.](./media/er-multiple-model-mappings-image1.png)

4. **Serbest metin faturası (Excel)** biçimin inceleyin:

    1. Sol bölmedeki yapılandırma ağacında, **Serbest metin faturası (Excel)** öğesini seçin.
    2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
    3. **Biçim tasarımcısı** sayfasındaki **Eşleme** sekmesinde yer alan veri kaynakları listesinde **Model**'i seçin.
    4. **Görüntüle**'yi seçin.
    
       Geçerli ER biçimi, **Fatura modelinin** **InvoiceCustomer** kök tanımını kullanacak şekilde yapılandırılır. Bu biçim çalıştırıldığında ve **Model** veri kaynağı çağrıldığında **InvoiceCustomer** kök tanımı için yapılandırılan model eşleme, uygulama verilerine erişmek ve veri modelini doldurmak için kullanılır.

        ![Biçim tasarımcısı sayfasındaki model veri kaynağını inceleme.](./media/er-multiple-model-mappings-image2.png)

    6. **Biçim tasarımcısı** sayfasını kapatın.

5. **Fatura modeli eşleme** yapılandırmasının içeriğini gözden geçirin:

    1. Sol bölmedeki yapılandırma ağacında, **Fatura modeli eşleme** öğesini seçin.
    2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
    3. **Modeli veri kaynağına eşleme** sayfasında, geçerli ER model eşleme yapılandırmasının birden fazla model eşleme bileşeni içerdiğini göreceksiniz.

        + **Müşteri Faturası** model eşleme, **Fatura modelinin** **InvoiceCustomer** kök tanımı için yapılandırılır. Bu nedenle **Serbest metin faturası (Excel)** ER biçimi çalıştırıldığında bu ER biçiminin **Müşteri Faturası** model eşlemesi uygulama verilerine erişmek ve veri modelini doldurmak için seçilebilir.
        + **Proje Faturası** model eşlemesi, **Fatura modelinin** **InvoiceProject** kök tanımı için yapılandırılır. Bu nedenle **Proje faturası (Excel)** ER biçimi çalıştırıldığında bu ER biçiminin **Proje Faturası** model eşlemesi uygulama verilerine erişmek ve veri modelini doldurmak için seçilebilir.

        ![Modeli veri kaynağına eşleme sayfasında fatura modeli eşleme.](./media/er-multiple-model-mappings-image3.png)

    4. **Veri kaynağı modeli eşleme** sayfasını kapatın.
    5. Bu ER yapılandırmasının 240.175 sürümünden sonraki tüm sürümlerini silmek için **Sürümler** hızlı sekmesinde **Sil**'i seçin.

6. **Proje faturası modeli eşleme (RDP)** yapılandırmasının içeriğini gözden geçirin:

    1. Sol bölmedeki yapılandırma ağacında, **Porje faturası modeli eşleme (RDP)** öğesini seçin.
    2. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
    3. **Modeli veri kaynağına eşleme** sayfasında, geçerli ER modeli eşleme yapılandırmasının **InvoiceProject** model eşlemesini içerdiğini ve bu model eşlemesinin **Fatura modeli** **InvoiceProject** kök tanımı için yapılandırıldığını görürsünüz. **Proje faturası (Excel)** ER biçimi çalıştırıldığında, uygulama verilerine erişmek ve veri modelini doldurmak için bu ER biçiminin **InvoiceProject** model eşlemesini seçin.

        ![Modeli veri kaynağına eşleme sayfasında proje faturası modeli eşleme.](./media/er-multiple-model-mappings-image4.png)

    4. **Veri kaynağı modeli eşleme** sayfasını kapatın.
    5. Bu ER yapılandırmasının 226.35 sürümünden sonraki tüm sürümlerini silmek için **Sürümler** hızlı sekmesinde **Sil**'i seçin.

## <a name="customize-the-imported-er-configurations"></a>İçeri aktarılan ER yapılandırmalarını özelleştirme

Bu bölümde, Microsoft tarafından sağlanan model eşlemelerinin nasıl [özelleştirileceği](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) açıklanmaktadır. Örneğin, özel mantığınızı uygulamak veya eksik bağları eklemek için özelleştirme gerekli olabilir.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Fatura modeli eşleme yapılandırmasını özelleştirme

1. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Fatura modeli eşleme (Litware)** öğesini seçin.
2. Eylem Panosundan **Yapılandırma oluştur**'u seçin.
3. **Yapılandırma oluştur** açılır iletişim kutusundaki **Yeni** alanında **Addan türet: Fatura modeli eşleme, Microsoft** seçeneğini belirleyin.
4. **Ad** alanına **Fatura modeli eşleme Litware** değerini girin.
5. **Yapılandırma oluştur**'u seçin.
6. Türetilmiş eşlemenin [taslak](general-electronic-reporting.md#component-versioning) sürümünü çalışma zamanında kullanılabilir olarak [işaretleyin](er-quick-start2-customize-report.md#MarkFormatRunnable):

    1. Eylem Bölmesindeki **Yapılandırmalar** sekmesinde yer alan **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
    2. **Kullanıcı parametreleri** iletişim kutusunda, **Çalıştırma ayarları** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.
    3. Sayfayı düzenlemeye hazır hale getirmek için gerektiğinde **Düzenle**'yi seçin.
    4. Şu anda yapılandırma ağacında seçili olan **Fatura modeli eşleme Litware** yapılandırması için **Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın.

7. Eylem bölmesinde bu yapılandırmanın model eşlemelerini incelemek için **Tasarımcı**'yı seçin.

    ![Modeli veri kaynağına eşleme sayfasındaki fatura modeli eşlemelerini inceleme.](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Artık özel mantığınızı yapılandırmak için tasarımcıda bu ER yapılandırmasının ER model eşleme bileşenlerini açabilirsiniz. Daha fazla bilgi için, bkz. [Model eşleme yapılandırmasını özelleştirme](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. **Veri kaynağı modeli eşleme** sayfasını kapatın.

Şimdi her biri **InvoiceCustomer** kök tanımı için yapılandırılmış bir model eşlemesine sahip olan **Fatura modeli eşleme** ve **Fatura modeli eşleme Litware** yapılandırmalarına sahipsiniz. Model eşlemelerinden birini, **InvoiceCustomer** kök tanımına sahip model veri kaynağı içeren **Serbest metin faturası (Excel)** gibi ER biçimlerinden biri tarafından kullanılan varsayılan model eşlemesi olarak açıkça atayın. Aksi takdirde, ER biçimlerinden birini çalıştırdığınızda, düzenlediğinizde veya doğruladığınızda, hiçbir varsayılan model eşlemesinin açıkça atanmadığını bildiren aşağıdaki özel durum oluşur:
 
> \<configuration names separated by commas\> yapılandırmalarındaki \<model name\> \<root descriptor\> veri modeli için birden fazla model eşlemesi var. Yapılandırmalardan birini varsayılan olarak ayarlayın.

![Yapılandırmalar sayfasında biçimi düzenleme için açma.](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Proje faturası model eşleme (RDP) yapılandırmasını özelleştirme

1. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Proje faturası model eşleme (RDP)** öğesini seçin.
2. Eylem Panosundan **Yapılandırma oluştur**'u seçin.
3. **Yapılandırma oluştur** iletişim kutusundaki **Yeni** alanında **Addan türet: Proje faturası model eşleme (RDP)** seçeneğini belirleyin.
4. **Ad** alanına **Proje faturası modeli eşleme Litware** değerini girin.
5. **Yapılandırma oluştur**'u seçin.
6. Şu anda yapılandırma ağacında seçili olan **Proje faturası model eşleme Litware** yapılandırması için **Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın.
7. Eylem bölmesinde bu yapılandırmanın model eşlemelerini incelemek için **Tasarımcı**'yı seçin.

    ![Modeli veri kaynağına eşleme sayfasında özelleştirilmiş proje faturası model eşlemelerini inceleme.](./media/er-multiple-model-mappings-image7.png)

8. **Veri kaynağı modeli eşleme** sayfasını kapatın.

Şimdi **Fatura modeli eşleme**, **Proje faturası model eşleme (RDP)** ve **Proje faturası model eşleme Litware** yapılandırmalarına sahipsiniz. Bu yapılandırmalardan her birinin, **InvoiceProject** kök tanımı için yapılandırılmış bir model eşlemesi vardır. Herhangi bir ER biçimi tarafından kullanılan varsayılan model eşlemesi olarak model eşlemelerinden birini açıkça atayın. Örneğin, **InvoiceProject** kök tanımına sahip bir model veri kaynağı içeren **Proje faturası (Excel)** biçimini kullanın. Aksi takdirde, ER biçimlerinden birini çalıştırdığınızda veya düzenlediğinizde, hiçbir varsayılan model eşlemesinin açıkça atanmadığını bildiren bir özel durum oluşur.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Varsayılan model eşlemelerini içeren yapılandırma olarak türetilmiş Fatura modeli eşleme Litware yapılandırmasını seçme

1. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Fatura modeli eşleme Litware** öğesini seçin.
2. **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.

    ![Yapılandırmalar sayfasında varsayılan model eşlemesi olarak model eşlemesi ayarlama.](./media/er-multiple-model-mappings-image8.png)

    Bu ayar nedeniyle, **Serbest metin faturası (Excel)** öğesini çalıştırdığınızda veya bunu düzenlediğinizde veya doğruladığınızda **Müşteri Faturası Kopyası** model eşlemesi kullanılır. **Fatura modeli eşleme** yapılandırmasından **Müşteri faturası** model eşlemesi yoksayılır.

    Şimdi, **Serbest metin faturası (Excel)** biçimini biçim tasarımcısında inceleme için açabilirsiniz.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Varsayılan model eşlemelerini içeren yapılandırma olarak türetilmiş Proje faturası modeli eşleme Litware yapılandırmasını seçme

1. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Proje faturası modeli eşleme Litware** öğesini seçin.
2. **Model eşleme için varsayılan** seçeneğini **Evet** olarak ayarlayın.

    Bu durumda, önceki bölümdeki **Fatura modeli eşleme Litware** yapılandırması için açıklanan durumun aksine, **Proje faturası model eşleme Litware** yapılandırmasından **InvoiceProject Kopyası** model eşlemeyi kullanmaya başlayamazsınız. **InvoiceProject** kök tanımı için model eşlemesi içeren iki yapılandırma, şu anda varsayılan yapılandırma olarak işaretlenmiştir. Bu nedenle, kullanım için eşit önceliğe sahiplerdir. Bu sorunu gidermek için, yordamın kalan adımlarını tamamlayın.

3. Sol bölmedeki yapılandırma ağacında, **Fatura modeli eşleme Litware** öğesini seçin.
4. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
5. **Modeli veri kaynağına eşleme** sayfasında, gerektiğinde sayfayı düzenlenebilir yapmak için **Düzenle**'yi seçin.
6. **Proje Faturası Kopyası** model eşlemesini seçin ve ardından bunun için **Silindi** onay kutusunu seçin.

    ![Modeli veri kaynağına eşleme sayfasında model eşlemeyi sanal olarak silindi biçiminde ayarlama.](./media/er-multiple-model-mappings-image9.png)

    Bu ayar nedeniyle, **Fatura modeli eşleme Litware** yapılandırması, **InvoiceProject** kök tanımı için model eşlemesi yokmuş gibi işlem görür. Varsayılan olarak düzenlenen **InvoiceProject Kopyası** model eşlemesi. Bu model eşlemesini içeren **Proje faturası model eşleme Litware** yapılandırması, varsayılan yapılandırma olarak işaretlenir. Varsayılan olarak işaretlendiği için **Proje faturası model eşleme (RDP)** yapılandırmasında **InvoiceProject** model eşlemesinden daha yüksek bir önceliğe sahiptir.

## <a name="other-considerations"></a>Dikkat edilecek diğer noktalar

**Proje faturası modeli eşleme Litware** yapılandırmasının **InvoiceProject Kopyası** model eşlemesi, **ReportDataProvider** veri kaynağını kullanacak şekilde tasarlanmıştır. Veri kaynağı, **PsaProjInvoiceDP** uygulama sınıfına başvuran *Nesne* türünün parçasıdır. Bu sınıf, Yazdırma yönetimi çerçevesinin proje faturası SQL Server Raporlama Servisleri (SSRS) raporuna ait veri sağlayıcısı olarak uygulanır. Bu veri kaynağını ER [tümleştirme noktası](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents) olarak seçin. Yazdırma yönetimi raporları için geçerli ER uygulaması bu ayarı dikkate alır. Daha fazla ayrıntı için, **ERPrintMgmtDataProviderReport** uygulama sınıfının kaynak kodunu gözden geçirin. Çalışma zamanında, **ReportDataProvider** veri kaynağının model eşleme tümleştirme noktası olarak atanması Finance'i bu eşleme bileşenini, **Proje faturası modeli eşleme (RDP)** yapılandırmasındaki **InvoiceProject** eşleme bileşeninden daha yüksek önceliğe sahip olacak şekilde işlemeye zorlar.

## <a name="see-also"></a>Ayrıca bkz.

- [Ayrı ER yapılandırmalarında ER model eşlemesini yönetme](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Ülke bağlamına bağımlı ER model eşlemeleri yapılandırma](er-country-dependent-model-mapping.md)
- [Elektronik raporlama çerçevesi API değişiklikleri](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
