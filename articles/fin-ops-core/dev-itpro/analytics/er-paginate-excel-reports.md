---
title: Excel'de oluşturulan belgeleri sayfalandırmak için ER biçimi tasarlama
description: Bu makalede, Microsoft Excel'de oluşturulan bir belgeyi sayfalandıran Elektronik raporlama (ER) biçiminin nasıl tasarlanacağı açıklanmaktadır.
author: kfend
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.form: EROperationDesigner
ms.openlocfilehash: e4a34dffda9e9b95f5d6c7ee382723663817ec6b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285016"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>Excel'de oluşturulan belgeleri sayfalandırmak için ER biçimi tasarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Sistem Yöneticisi veya Elektronik Raporlama İşlev Danışmanı rolünde bir kullanıcının Microsoft Excel'de giden belgeler oluşturmak ve belge sayfalandırmasını yönetmek için [Elektronik raporlama (ER)](general-electronic-reporting.md) biçimini nasıl yapılandırabileceği açıklanmaktadır.

Bu örnekte, Intrastat beyannamesi [oluşturulduğunda](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) denetim raporunu yazdırmak için kullanılan ve Microsoft tarafından sağlanan ER biçimini değiştireceksiniz. Bu rapor, bildirilen Intrastat hareketlerini gözlemlemenize olanak tanır. Değişiklikleriniz, oluşturulan denetim raporlarının sayfalandırmasını yönetmenizi sağlar.

Bu makaledeki yordamlar **DEMF** şirketinde tamamlanabilir. Kodlama gerekmez. Başlamadan önce aşağıdaki dosyaları indirip kaydedin.

| Tanım       | Dosya adı |
|-------------------|-----------| 
| Rapor şablonu 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| Rapor şablonu 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>ER altyapısını yapılandırma

En az ER parametre kümesini ayarlamak için [ER altyapısını yapılandırma](er-quick-start2-customize-report.md#ConfigureFramework) bölümündeki adımları izleyin. Standart ER biçiminin özel bir sürümünü tasarlamak için ER çerçevesini kullanmaya başlamadan önce bu kurulumu tamamlamanız gerekir.

## <a name="import-the-standard-er-format-configuration"></a>Standart ER biçimi yapılandırmasını içeri aktarma

Standart ER yapılandırmalarını Dynamics 365 Finance kurulumunuza eklemek için [Standart ER biçimi yapılandırmasını içeri aktarma](er-quick-start2-customize-report.md#ImportERSolution1) bölümündeki adımları izleyin. **Intrastat raporu** biçim yapılandırmasına dair sürüm **1.9**'u içeri aktarın. Temel **Intrastat modeli** yapılandırmasına dair temel sürüm 1, depodan otomatik olarak içeri aktarılır.

## <a name="customize-the-standard-er-format"></a>Standart ER biçimini Özelleştirme

### <a name="create-the-custom-er-format"></a>Özel ER biçimini oluşturma

Bu senaryoda, şu anda etkin ER yapılandırması sağlayıcısı olarak seçilen Litware, Inc. temsilcisisiniz. Temel olarak **Intrastat raporu** yapılandırmasını kullanarak yeni bir ER biçimi yapılandırması oluşturmanız gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, sol bölmedeki yapılandırma ağacında **Intrastat modeli**'ni genişletin ve **Intrastat raporu** seçeneğini belirleyin. Litwin, Inc. özel sürümün temeli olarak bu ER biçim yapılandırmasının sürüm 1,9 ' sini kullanacaktır.
3. Açılır iletişim kutusunu açmak için **Yapılandırma oluştur**'u seçin. Bu iletişim kutusunu, özel ödeme biçimi için yeni bir konfigürasyon oluşturmanıza olanak sağlar.
4. **Yeni** alan grubunda, **Addan türetilen: Intrastat raporu, Microsoft** seçeneğini belirleyin.
5. **Ad** alanına **Intrastat raporu Litware** ifadesini girin.
6. Yeni biçimi oluşturmak için **Yapılandırma oluştur**'u seçin.

**Intrastat raporu Litware** ER biçimi yapılandırmasına dair sürüm 1.9.1 oluşturulur. Bu sürüm **Taslak** durumuna sahiptir ve düzenlenebilir. Özel ER biçiminizin geçerli içeriğinin,  Microsoft tarafından sağlanan biçimin içeriğiyle aynıdır.

### <a name="make-the-custom-format-runnable"></a>Özel biçimi çalıştırılabilir hale getirme

Artık özel biçiminizin ilk sürümü oluşturulduğundan ve **Taslak** durumunda olduğundan biçimi test amacıyla çalıştırabilirsiniz. Raporu çalıştırmak için, özel işlem biçiminizi ifade eden ödeme yöntemini kullanarak bir satıcı ödemesini işleyin. Varsayılan olarak, uygulamadan ER biçimini çağırdığınızda yalnızca **Tamamlandı** ve **Paylaşıldı** durumuna sahip sürümler dikkate alınır. Bu davranış, bitmemiş tasarımları bulunan ER biçimlerinin kullanılmasını önlemeye yardımcı olur. Ancak, test çalışmalarınız için, uygulamayı **taslak** durumunda olan ER formatının biçimini kullanmaya zorlayabilirsiniz. Bu şekilde, herhangi bir değişiklik gerekiyorsa geçerli biçim sürümünü ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Uygulanabilirlik](electronic-reporting-destinations.md#applicability).

ER biçiminin taslak sürümünü kullanmak için, ER biçimini açık olarak işaretlemeniz gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Çalıştırma ayarları** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.
4. Geçerli sayfayı düzenlemeye hazır hale getirmek için gerektiğinde **Düzenle**'yi seçin.
5. Sol bölmedeki yapılandırma ağacında, **Intrastat raporu Litware**'i seçin.
6. **Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın ve ardından **Kaydet**'i seçin.

    ![Yapılandırmalar sayfasındaki Taslak Çalıştır seçeneği.](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>Özel ER biçimini kullanmak için Dış ticaret parametrelerini ayarlama

Özel biçimi kullanabilmeniz için Dış ticaret parametrelerini yapılandırmak üzere bu adımları izleyin.

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **Dış ticaret parametreleri**'ne gidin.
2. **Dış ticaret parametreleri** sayfasında, **Elektronik raporlama** hızlı sekmesinde, **Dosya biçimi eşlemesi** alanında **Intrastat raporu Litware**'i seçin.
3. **Rapor biçimi eşlemesi** alanında, **Intrastat raporu Litware**'i seçin.
4. **Kaydet**'i seçin.

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>İndirilen rapor şablonunu kullanmak için özel biçimi yapılandırma

### <a name="review-the-first-downloaded-excel-template"></a>İlk indirilen Excel şablonunu gözden geçirme

1. Excel masaüstü uygulamasında, daha önce indirdiğiniz **ERIntrastatReportDemo1.xlsx** şablon dosyasını açın.
2. Şablonun, oluşturulan belgelerdeki rapor üst bilgisi, rapor ayrıntıları ve rapor alt bilgisi bölümlerini oluşturmak için adlandırılmış aralıklar içerdiğini doğrulayın.

    ![Masaüstü uygulamasındaki Excel şablonu 1'in düzeni.](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>Geçerli Excel şablonunu özel ER biçiminde değiştirme

Özel ER biçimine yeni bir Excel şablonu eklemeniz gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, sol bölmedeki yapılandırma ağacında **Intrastat modeli** \> **Intrastat raporu**'nu genişletin ve **Intrastat raporu Litware** yapılandırmasını seçin.
3. **Tasarımcı**’yı seçin.
4. **Biçim tasarımcısı** sayfasında, Eylem Bölmesi'nde **Ayrıntıları göster**'i seçin.
5. **Intrastat: Excel** kök biçim bileşeninin seçili olduğundan emin olun ve ardından Eylem Bölmesi'nde, **İçeri Aktar** sekmesinde, **İçeri Aktar** grubunda **Excel'den güncelleştir**'i seçin.
6. **Excel'den güncelleştir** iletişim kutusunda **Şablonu güncelleştir**'i seçin.
7. **Aç** iletişim kutusunda, daha önce indirdiğiniz **ERIntrastatReportDemo1.xlsx** dosyasını göz atıp indirin ve ardından **Aç**'ı seçin.
8. **Tamam**'ı seçin.
9. **Kaydet**'i seçin.

![Yeni Excel şablonu eklendikten sonra ER biçimi tasarımcısında biçim yapısı.](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>Oluşturulan raporda madde açıklamasını göstermek için veri bağlamayı değiştirme

1. **Biçim tasarımcısı** sayfasında **Eşleme** sekmesini seçin.
2. **Intrastat** \> **Rapor satırları**'nı genişletin ve **Emtia kodu** bileşenini seçin.
3. **Formül düzenle**’yi seçin.
4. `@.CommodityCode` bağlama formülünü `CONCATENATE(@.CommodityCode, " ", @.ProductName)` olarak değiştirin.
5. **Kaydet**'i seçin.

![ER biçim tasarımcısında madde açıklamasını göstermek için yapılandırılmış bağlama.](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>Intrastat beyannamesi denetim raporu oluşturma

İlk olarak, **Intrastat** sayfasında raporlamak için Intrastat hareketlerine sahip olduğunuzdan emin olun.

![Intrastat sayfasındaki hareketler.](./media/er-paginate-excel-reports-transactions1.gif)

Ardından Intrastat beyannamesinin denetim raporunu oluşturmak için özel ER biçimini kullanın.

1. **Vergi** \> **Bildirimler** \> **Dış ticaret** \> **İntrastat**'a gidin.
2. **Intrastat** sayfasında, Eylem Bölmesi'nde **Çıkış** \> **Rapor**'u seçin.
3. **Intrastat Raporu** iletişim kutusunda, raporu çalıştırmak için şu adımları izleyin:

    1. Belirli Intrastat hareketlerini rapora eklemek için **Başlangıç tarihi** ve **Bitiş tarihi** alanlarını ayarlayın.
    2. **Dosya oluştur** seçeneğini **Hayır** olarak ayarlayın.
    3. **Rapor oluştur** seçeneğini **Evet** olarak ayarlayın.
    4. **Tamam**'ı seçin.

4. Oluşturulan belgeyi indirin ve kaydedin.
5. Belgeyi Excel'de açın ve gözden geçirin.

    ![Masaüstü uygulamasında oluşturulan Excel belgesi.](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>Oluşturulan belgeleri sayfalandırmak için özel biçimi yapılandırma

### <a name="review-the-second-downloaded-excel-template"></a>İkinci indirilen Excel şablonunu gözden geçirme

1. Excel'de, daha önce indirdiğiniz **ERIntrastatReportDemo2.xlsx** şablon dosyasını açın.
2. Bu şablonla **ERIntrastatReportDemo1.xlsx** şablonunu karşılaştırın ve bunun, oluşturulan belgelerde sayfaya özel bölümler oluşturup doldurmak için birkaç yeni Excel adı içeriğini doğrulayın:

    - Sayfa üst bilgileri oluşturmak için **ReportPageHeader** aralığı eklenir.
    - Sayfa alt bilgileri oluşturmak için **ReportPageFooter** aralığı eklenir.
    - Sayfa başına hareket sayısını göstermek için **ReportPageFooter\_PageLines** hücresi yapılandırılır.
    - Sayfa başına toplam hareket tutarını göstermek için **ReportPageFooter\_PageAmount** hücresi yapılandırılır.
    - Sayfa başına toplam hareket ağırlığını göstermek için **ReportPageFooter\_PageWeight** hücresi yapılandırılır.
    - Sayfa başlangıcından geçerli sayfaya kadar hareketlerin çalıştırma sayacını göstermek için **ReportPageFooter\_RunningCounterLines** hücresi yapılandırılır.
    - Sayfa başlangıcından geçerli sayfaya kadar tüm hareketler için tutar çalıştırma toplamını göstermek üzere **ReportPageFooter\_RunningTotalAmount** hücresi yapılandırılır.
    - Sayfa başlangıcından geçerli sayfaya kadar hareketler için ağırlık çalıştırma toplamını göstermek üzere **ReportPageFooter\_RunningTotalWeight** hücresi yapılandırılır.

    ![Masaüstü uygulamasındaki Excel şablonu 2'in düzeni.](./media/er-paginate-excel-reports-template2a.gif)

    Hücre metnini kaydırmak için bu şablonun **CommodityCode** hücresi yapılandırılır. Hareket ayrıntıları satırı satırın yüksekliğine otomatik olarak uyacak şekilde yapılandırıldığından **CommodityCode** hücresindeki metin kaydırıldığında tüm satırın yüksekliği otomatik olarak değişir.

    ![Hücre metnini kaydırmak için yapılandırılan CommodityCode hücresi.](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>Geçerli Excel şablonunu özel ER biçiminde değiştirmeyi yineleme

1. Bu makalenin [Geçerli Excel şablonunu özel ER biçiminde değiştirme](#replace-template) bölümündeki adımları izleyin. Ancak 7. adımda **ERIntrastatReportDemo2.xlsx** dosyasını seçin.
2. **Biçim tasarımcısı** sayfasında, **Intrastat**'ı genişletin.
3. Yapıyı uygulanan Excel şablonunun yapısıyla eşitlemek için düzenlenebilir ER biçimine eklenen [Aralık](er-fillable-excel.md#range-component) biçim bileşenlerini adlandırın:

    1. **ReportPageHeader** Excel adıyla ilişkili olan **Aralık** bileşenini seçin.
    2. **Biçim** sekmesinde, **Ad** alanına **Rapor sayfası üst bilgisi**'ni girin.
    3. **ReportPageFooter** Excel adıyla ilişkili olan **Aralık** bileşenini seçin.
    4. **Biçim** sekmesinde, **Ad** alanına **Rapor sayfası alt bilgisi**'ni girin.

4. **Kaydet**'i seçin.

![Excel şablonu değiştirildikten sonra ER biçimi tasarımcısında biçim yapısı.](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>Belge sayfalandırmasını uygulamak için biçim yapısını değiştirme

1. **Biçim tasarımcısı** sayfasında, sol bölmedeki biçim ağacında **Intrastat** kök bileşenini seçin.
2. **Ekle**'yi seçin.
3. **Ekle** iletişim kutusunda, **Excel** bileşen grubunda [Sayfa](er-fillable-excel.md#page-component) bileşenini seçin.
4. **Bileşen özellikleri** iletişim kutusunda, **Ad** alanına **Rapor sayfası**'nı girin. Daha sonra **Tamam**'ı seçin.
5. Oluşturulan her sayfada sayfa üst bilgisi olarak **Rapor sayfası üst bilgisi** bileşenini kullanmak için şu adımları izleyin:

    1. **Rapor sayfası üst bilgisi** bileşenini seçin ve ardından **Kes** seçeneğini belirleyin.
    2. **Rapor sayfası** bileşenini seçin ve ardından **Yapıştır** seçeneğini belirleyin.
    3. **Rapor sayfası**'nı genişletin.
    4. Bu aralığı sayfa üst bilgisi olarak [dikkate almak](er-fillable-excel.md#page-component-structure) için **Sayfa** bileşenini zorlamak üzere **Rapor sayfası üst bilgisi**'ni seçin ve ardından **Biçim** sekmesinde, **Çoğaltma yönü** alanında **Çoğaltma yok** seçeneğini belirleyin.

6. Rapor satırlarındaki içeriğin dikkate alınması için oluşturulan bir belgeyi sayfalandırmak üzere şu adımları izleyin:

    1. **Rapor satırları** bileşenini seçin ve ardından **Kes** seçeneğini belirleyin.
    2. **Rapor sayfası** bileşenini seçin ve ardından **Yapıştır** seçeneğini belirleyin.

7. Rapor alt bilgisini rapor satırlarından sonra ancak son sayfa alt bilgisinden önce eklemek için şu adımları izleyin:

    1. **Rapor alt bilgisi** bileşenini seçin ve ardından **Kes** seçeneğini belirleyin.
    2. **Rapor sayfası** bileşenini seçin ve ardından **Yapıştır** seçeneğini belirleyin.

8. Oluşturulan her sayfada sayfa alt bilgisi olarak **Rapor sayfası alt bilgisi** bileşenini kullanmak için şu adımları izleyin:

    1. **Rapor sayfası alt bilgisi** bileşenini seçin ve ardından **Kes** seçeneğini belirleyin.
    2. **Rapor sayfası** bileşenini seçin ve ardından **Yapıştır** seçeneğini belirleyin.
    3. Bu aralığı sayfa alt bilgisi olarak [dikkate almak](er-fillable-excel.md#page-component-structure) için **Sayfa** bileşenini zorlamak üzere **Rapor sayfası alt bilgisi**'ni seçin ve ardından **Biçim** sekmesinde, **Çoğaltma yönü** alanında **Çoğaltma yok** seçeneğini belirleyin.

![Belge sayfalandırması uygulandıktan sonra ER biçimi tasarımcısında biçim yapısı.](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>Sayfa alt bilgisi toplamlarını hesaplamak için veri kaynakları ekleme

Sayfa toplamını, çalıştırma sayacını ve çalıştırma toplam değerleri hesaplamak ve bunları sayfa alt bilgisi bölümünde göstermek için yeni veri kaynaklarını yapılandırmanız gerekir. Bu amaçla [Veri toplama](er-data-collection-data-sources.md) veri kaynaklarını kullanmanız önerilir.

1. **Biçim tasarımcısı** sayfasında **Eşleme** sekmesini seçin.
2. **Kök ekle**'yi seçin ve ardından şu adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **Genel** bölümünde **Konteyneri boşalt**'ı seçin.
    2. **"Konteyneri boşalt" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Toplam**'ı girin.
    3. **Tamam**'ı seçin.

3. **Toplam** veri kaynağını seçin, **Ekle** seçeneğini belirleyin ve ardından şu adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **Genel** bölümünde **Konteyneri boşalt**'ı seçin.
    2. **"Konteyneri boşalt" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Sayfa**'yı girin.
    3. **Tamam**'ı seçin.

4. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **Genel** bölümünde **Konteyneri boşalt**'ı seçin.
    2. **"Konteyneri boşalt" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Çalıştırma**'yı girin.
    3. **Tamam**'ı seçin.

5. **Total.Page** veri kaynağını seçin, **Ekle** seçeneğini belirleyin ve ardından şu adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler** bölümünde **Veri toplama**'yı seçin.
    2. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Tutar**'ı girin.
    3. **Madde türü** alanında **Gerçek**'i seçin.
    4. **Tüm değerleri topla** seçeneğini **Evet** olarak ayarlayın.
    5. **Tamam**'ı seçin.

6. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler** bölümünde **Veri toplama**'yı seçin.
    2. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Ağırlık**'ı girin.
    3. **Madde türü** alanında **Gerçek**'i seçin.
    4. **Tüm değerleri topla** seçeneğini **Evet** olarak ayarlayın.
    5. **Tamam**'ı seçin.

7. **Total.Running** veri kaynağını seçin, **Ekle** seçeneğini belirleyin ve ardından şu adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler** bölümünde **Veri toplama**'yı seçin.
    2. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Tutar**'ı girin.
    3. **Madde türü** alanında **Gerçek**'i seçin.
    4. **Tüm değerleri topla** alanını **Evet** olarak ayarlayın.
    5. **Tamam**'ı seçin.

8. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler** bölümünde **Veri toplama**'yı seçin.
    2. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Ağırlık**'ı girin.
    3. **Madde türü** alanında **Gerçek**'i seçin.
    4. **Tüm değerleri topla** alanını **Evet** olarak ayarlayın.
    5. **Tamam**'ı seçin.

9. Yeniden **Ekle**'yi seçin ve ardından aşağıdaki adımları izleyin:

    1. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler** bölümünde **Veri toplama**'yı seçin.
    2. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Satırlar**'ı girin.
    3. **Madde türü** alanında **Tamsayı**'yı seçin.
    4. **Tüm değerleri topla** alanını **Evet** olarak ayarlayın.
    5. **Tamam**'ı seçin.

10. **Kaydet**'i seçin.

### <a name="add-data-sources-to-control-page-footer-visibility"></a>Sayfa alt bilgisi görünürlüğünü denetlemek için veri kaynakları ekleme

Sayfa alt bilgisi görünürlüğünü denetlemek istiyorsanız ve işlem içermiyorsa son sayfaya alt bilgiyi eklemeyi planlamıyorsanız gerekli çalıştırma sayacını hesaplamak için yeni bir veri kaynağı yapılandırın.

1. **Biçim tasarımcısı** sayfasında **Eşleme** sekmesini seçin.
2. **Total.Running** veri kaynağını seçin ve **Ekle** seçeneğini belirleyin.
3. **Veri kaynağı ekle** iletişim kutusunda, **İşlevler** bölümünde **Veri toplama**'yı seçin.
4. **"Veri toplama" veri kaynağı özellikleri** iletişim kutusunda, **Ad** alanına **Lines2** öğesini girin.
5. **Madde türü** alanında **Tamsayı**'yı seçin.
6. **Tüm değerleri topla** seçeneğini **Evet** olarak ayarlayın.
7. **Tamam**'ı seçin.
8. **Kaydet**'i seçin.

![ER biçim tasarlayıcısında eklenen veri kaynakları.](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>Toplam değerleri toplamak için bağlamaları yapılandırma

1. **Biçim tasarımcısı** sayfasında, biçim ağacında **Rapor satırları** bileşenini genişletin ve iç içe **Fatura değeri** bileşenini seçin.
2. **Formül düzenle**’yi seçin.
3. `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` bağlama formülünü `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))` olarak değiştirin.

    > [!NOTE]
    > Yinelenen her hareket için bir Excel hücresine tutar değerini koymaya ek olarak bu bağlama, veri toplama **Total.Page.Amount** veri kaynağındaki değeri toplar.

4. İç içe **Ağırlık** bileşenini seçin.
5. **Formül düzenle**’yi seçin.
6. `@.'$RoundedWeight'` bağlama formülünü `Total.Page.Weight.Collect(@.'$RoundedWeight')` olarak değiştirin.

    > [!NOTE]
    > Yinelenen her hareket için bir Excel hücresine ağırlık değerini koymaya ek olarak bu bağlama, veri toplama **Total.Page.Weight** veri kaynağındaki değeri toplar.

![ER biçim tasarımcısında toplam değerleri toplamak için yapılandırılan bağlamalar.](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>Sayfa alt bilgi toplamlarını doldurmak için bağlamaları yapılandırma

1. **Biçim tasarımcısı** sayfasında, biçim ağacında **Rapor sayfası alt bilgisi** bileşenini genişletin, Excel **ReportPageFooter\_PageAmount** hücresine başvuran iç içe **Aralık** bileşenini seçin ve ardından şu adımları izleyin:

    1. Sağ bölmedeki veri kaynakları ağacında **Total.Page.Amount.Sum()** maddesini seçin.
    2. **Bağla**'yı seçin.
    3. **Formül düzenle**’yi seçin.
    4. Formülü `Total.Page.Amount.Sum(false)` olarak güncelleştirin.

    > [!NOTE]
    > Tutar çalıştırma toplamını, sayfa başına toplam satır sayısını ve satırların çalıştırma sayacını hesaplamak için bu veriler gerektiğinden geçerli sayfa için toplanan verileri tutmak üzere bu işlevin bağımsız değişkenini **Yanlış** olarak belirtmeniz gerekir.

2. Biçim ağacında, Excel **ReportPageFooter\_PageWeight** hücresine başvuran iç içe **Aralık** bileşenini seçin ve ardından şu adımları izleyin:

    1. Sağ bölmedeki veri kaynakları ağacında **Total.Page.Weight.Sum()** maddesini seçin.
    2. **Bağla**'yı seçin.
    3. **Formül düzenle**’yi seçin.
    4. Formülü `Total.Page.Weight.Sum(false)` olarak güncelleştirin.

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>Sayfa çalıştırma toplamlarını doldurmak için bağlamaları yapılandırma

1. **Biçim tasarımcısı** sayfasında, biçim ağacında **Rapor sayfası alt bilgisi** bileşenini genişletin, Excel **ReportPageFooter\_RunningTotalAmount** hücresine başvuran iç içe **Aralık** bileşenini seçin ve ardından şu adımları izleyin:

    1. Sağ bölmedeki veri kaynakları ağacında **Total.Running.Amount.Collect()** maddesini seçin.
    2. **Bağla**'yı seçin.
    3. **Formül düzenle**’yi seçin.
    4. Formülü `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` olarak güncelleştirin.

    > [!NOTE]
    > `Total.Running.Amount.Sum(false)` işleneni, önceden toplanmış tutar çalıştırma toplamını döndürür. `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` işleneni, geçerli sayfanın toplam tutarını döndürür. Bu değer `Total.Running.Amount` çalıştırma toplamı koleksiyonuna konulur konulmaz `Total.Page.Amount` veri koleksiyonunu sıfırlamak için ikinci işlenenin iç içe işlevinin bağımsız değişkenini **Doğru** olarak belirtmeniz gerekir. Belirtilen bağımsız değişkenin, sonraki sayfa toplamını 0 (sıfır) değerinden toplamak için başlaması gerekir.
    >
    > Geçerli sayfada Excel **ReportPageFooter\_RunningTotalAmount** hücresinde tutar çalıştırma toplamını girmek için `Total.Running.Amount.Sum(false)` işlevi çağrılır.

2. Biçim ağacında, Excel **ReportPageFooter\_RunningTotalWeight** hücresine başvuran iç içe **Aralık** bileşenini seçin ve ardından şu adımları izleyin:

    1. Sağ bölmedeki veri kaynakları ağacında **Total.Running.Weight.Collect()** maddesini seçin.
    2. **Bağla**'yı seçin.
    3. **Formül düzenle**’yi seçin.
    4. Formülü `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))` olarak güncelleştirin.

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>Sayfa çalıştırma sayacını doldurmak için bağlamaları yapılandırma

1. **Biçim tasarımcısı** sayfasında, biçim ağacında **Rapor sayfası alt bilgisi** bileşenini genişletin ve Excel **ReportPageFooter\_RunningCounterLines** hücresine başvuran iç içe **Aralık** bileşenini seçin.
2. **Formül düzenle**’yi seçin.
3. `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))` formülünü ekleyin.

    > [!NOTE]
    > Bu formül, tüm rapor için toplanan tutar değerlerinin sayısını döndürür. Bu sayı, geçerli anda yinelenen hareketlerin sayısına eşittir. Aynı anda, formül **Total.Running.Lines** koleksiyonundaki döndürülen değeri toplar.

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>Sayfa alt bilgisi sayacını doldurmak için bağlamaları yapılandırma

1. **Biçim tasarımcısı** sayfasında, biçim ağacında **Rapor sayfası alt bilgisi** bileşenini genişletin ve Excel **ReportPageFooter\_PageLines** hücresine başvuran iç içe **Aralık** bileşenini seçin.
2. **Formül düzenle**’yi seçin.
3. `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)` formülünü ekleyin.

    > [!NOTE]
    > Bu formül, tüm rapor için **Total.Page.Amount.Result** öğesinde toplanan hareket sayısı ile **Total.Running.Lines.Sum** öğesinde bu aşamada depolanan hareket sayısı arasındaki fark olarak geçerli sayfadaki hareket sayısını hesaplar. Geçerli sayfa için hareket sayısı Excel **ReportPageFooter\_RunningCounterLines** hücresine başvuran **Aralık** bileşeninin bağlamasında **Total.Running.Lines** öğesinde depolandığından geçerli sayfadaki hareket sayısı henüz dahil edilmez. Bu nedenle bu fark, geçerli sayfadaki hareket sayısına eşittir.

![ER biçim tasarımcısında sayfa alt bilgisi sayacında doldurmak için yapılandırılan bağlamalar.](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>Bileşen görünürlüğünü yapılandırma

Aşağıdaki öğeleri gizlemek için oluşturulan belgenin belirli bir sayfasında sayfa üst bilgisinin ve alt bilgisinin görünürlüğünü değiştirebilirsiniz:

- Rapor üst bilgisi zaten sütun başlıkları içerdiğinden ilk sayfadaki sayfa üst bilgisi
- Son sayfa için ortaya çıkabilen hareketlerin olmadığı sayfalardaki sayfa üst bilgisi
- Son sayfa için ortaya çıkabilen hareketlerin olmadığı sayfalardaki sayfa alt bilgisi

Görünürlüğü değiştirmek için **Rapor sayfası üst bilgisi** ve **Rapor sayfası alt bilgisi** bileşenlerinin **Etkin** özelliğini güncelleştirin.

1. **Biçim tasarımcısı** sayfasında, biçim ağacında **Rapor sayfası** bileşenini genişletin, iç içe **Rapor sayfası üst bilgisi** bileşenini seçin ve ardından şu adımları izleyin:

    1. **Etkin** alanı için **Düzenle**'yi seçin.
    2. **Formül tasarımcısı** sayfasında, **Formül** alanına aşağıdaki ifadeyi girin:

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. Biçim ağacında, iç içe **Rapor sayfası alt bilgisi** bileşenini seçin ve ardından şu adımları izleyin:

    1. **Etkin** alanı için **Düzenle**'yi seçin.
    2. **Formül tasarımcısı** sayfasında, **Formül** alanına aşağıdaki ifadeyi girin:

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` yapımı, geçerli sayfadaki hareket sayısını hesaplamak için kullanılır. `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` yapımı, sonraki sayfa alt bilgisinin görünürlüğünü doğru şekilde işlemek için geçerli sayfadaki hareket sayısını koleksiyona eklemek üzere kullanılır.
    >
    > Temel bir bileşenin **Etkin** özelliği iç içe bileşenlerin bağlamaları işlendikten **sonra** işlendiğinden burada `Total.Running.Lines` koleksiyonu yeniden kullanılamaz. **Etkin** özelliği işlendiğinde `Total.Running.Lines` koleksiyonu zaten geçerli sayfadaki hareket sayısı kadar artırılır.

3. **Kaydet**'i seçin.

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>Intrastat beyannamesi denetim raporu oluşturma (güncelleştirildi)

1. **Intrastat** sayfasında 24 harekete sahip olduğunuzdan emin olun. Denetim raporu oluşturup gözden geçirmek için bu makalenin [Intrastat beyannamesi denetim raporu oluşturma](#generate-intrastat-control-report) bölümündeki adımları yineleyin.

    Tüm hareketler ilk sayfada sunulur. Sayfa toplamları ve sayaçları, rapor toplamlarına ve sayaçlarına eşittir. Rapor üst bilgisi zaten sütun başlıkları içerdiğinden ilk sayfadaki sayfa üst bilgisi aralığı gizlenir. Bu sayfa hiç hareket içermediğinden ikinci sayfada sayfa üst bilgisi ve alt bilgisi gizlenir.

    ![Masaüstü uygulamasında oluşturulan Excel belgesi.](./media/er-paginate-excel-reports-document2.gif)

2. **Madde numarası** kodunu **D00006**'dan **L0010**'a değiştirerek **Intrastat** sayfasındaki iki hareketi güncelleştirin. Yeni maddenin **Etkin stereo hoparlör çifti** ürün adının artık orijinal maddenin **Standart hoparlör** ürün adından uzun olduğunu unutmayın. Bu durum, oluşturulan belgenin karşılık gelen hücresinde metin kaydırmayı zorlar. Belge sayfalandırması ve sayfayla ilgili toplama ve sayma artık güncelleştirilmelidir. Denetim raporu oluşturup gözden geçirmek için [Intrastat beyannamesi denetim raporu oluşturma](#generate-intrastat-control-report) bölümündeki adımları yineleyin.

    Şu anda hareketler iki sayfada sunulmaktadır ve sayfa toplamları ve sayaçlar doğru şekilde hesaplanmaktadır. Sayfa üst bilgisi aralığı, ilk sayfada doğru şekilde gizlenir ve ikinci sayfada görünür. Sayfa alt bilgisi, hareket içerdiklerinden iki sayfada da görünür.

    ![Masaüstü uygulamasında güncelleştirilen oluşturulan Excel belgesi.](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>Sayfa biçimi bileşeni tarafından son sayfa işlendiğinde kabul etmenin bir yolu var mıdır?

**Sayfa** bileşeni, oluşturulan belgede işlenen sayfa sayısı ve toplam sayfa sayısı hakkındaki bilgileri [göstermez](er-fillable-excel.md#page-component-limitations). Bununla birlikte, son sayfayı kabul etmek için ER [formülleri](er-formula-language.md) yapılandırabilirsiniz. Aşağıda bir örnek verilmiştir:

- **Rapor sayfası** bileşenini kullanarak zaten işlenmiş hareketlerin toplam sayısını hesaplayın. Bu hesaplamayı `COUNT(Total.Page.Amount.Result)` formülünü kullanarak yapabilirsiniz. 
- **Rapor satırları** bileşeni için yapılandırılan `model.CommodityRecord` bağlamasına dayalı olarak işlenmesi gereken hareketlerin toplam sayısını hesaplayın. Bu hesaplamayı `COUNT(model.CommodityRecord)` formülünü kullanarak yapabilirsiniz.
- Son sayfayı kabul etmek için iki sayıyı karşılaştırın. Değerler eşit olduğunda son sayfa oluşturulur.

> [!NOTE]
> Bu yaklaşımı yalnızca **Rapor satırları** bileşeninin **Etkin** özelliğinin, [Kayıt listesinin](er-formula-supported-data-types-composite.md#record-list) yinelenen bazı [kayıtları](er-formula-supported-data-types-composite.md#record) için çalışma zamanında [Yanlış](er-formula-supported-data-types-primitive.md#boolean) sonucunu döndürebilen formül içermemesi durumunda kullanmanızı öneririz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Excel biçiminde belgeler oluşturmak için yapılandırma tasarlama](er-fillable-excel.md)
- [VERİ TOPLAMA veri kaynaklarını Elektronik raporlama (ER) biçimlerinde kullanma](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
