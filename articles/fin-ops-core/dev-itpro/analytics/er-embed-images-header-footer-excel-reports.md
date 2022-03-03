---
title: Sayfa üst bilgilerinde veya alt bilgilerinde katıştırılmış görüntülerle Excel biçiminde bir rapor oluşturmak için bir ER biçimi tasarlama
description: Bu konuda, sayfa üst bilgilerine veya alt bilgilerine eklenmiş resim ve şekillere sahip iş belgeleri oluşturmak için Elektronik raporlamanın (ER) nasıl kullanılacağı açıklanmaktadır.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3f3f77a9e6104a31995c9ee398504982fe43ac9e
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323798"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>Sayfa üst bilgilerinde veya alt bilgilerinde katıştırılmış görüntülerle Excel biçiminde bir rapor oluşturmak için bir ER biçimi tasarlama

[!include[banner](../includes/banner.md)]

Bu konuda, Sistem Yöneticisi veya Elektronik Raporlama İşlev Danışmanı rolüne sahip bir kullanıcının bu görevleri nasıl gerçekleştirebileceği açıklanmaktadır:

- [Elektronik raporlama (ER)](general-electronic-reporting.md) altyapısının parametrelerini yapılandırın.
- Microsoft tarafından [sağlanan](general-electronic-reporting.md#Provider) ve Microsoft Excel biçimdeki bir [şablona](er-fillable-excel.md#excel-file-component) göre [serbest metin faturaları](../../../finance/accounts-receivable/create-free-text-invoice-new.md) oluşturmak için kullanılan ER [yapılandırmalarını](general-electronic-reporting.md#Configuration) içeri aktarın.
- Microsoft tarafından sağlanan standart bir ER biçimi yapılandırmasının [özel (türetilmiş)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) sürümünü oluşturun.
- Özel ER biçimi yapılandırmasını, alt bilgide şirket logosu resmi olan bir serbest metin faturası raporu oluşturacak şekilde değiştirin.

Bu konudaki yordamlar **USMF** şirketinde tamamlanabilir. Kodlama gerekmez. Başlamadan önce aşağıdaki dosyayı da indirip kaydetmelisiniz:

| Tanım        | Dosya adı |
|--------------------|-----------|
| Şirket logosu resmi | [Şirket logosu.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>İçerik

- [Tüzel kişilik yapılandırma](#ConfigureLegalEntity)
- [ER altyapısını yapılandırma](#ConfigureFramework)

    - [ER parametrelerini yapılandırma](#ConfigureParameters)
    - [ER yapılandırma sağlayıcısı etkinleştirin](#ActivateProvider)

        - [ER yapılandırma sağlayıcıları listesini gözden geçirin](#ReviewProvidersList)
        - [Yeni bir ER yapılandırması sağlayıcısı ekleme](#AddProvider)
        - [Yeni ER yapılandırma sağlayıcısını etkinleştirme](#ActivateAddedProvider)

- [Standart ER biçimi yapılandırmalarını içe aktarın](#ImportERSolution1)

    - [Standart ER yapılandırmalarını içe aktarın](#ImportERFormat)
    - [İçe aktarılan ER yapılandırmalarını gözden geçirin](#ReviewImportedERSolution)

- [Standart ER biçimini kullanarak serbest metin faturası yazdırma](#PrintInvoice1)

    - [Yazdırma yönetimini ayarlama](#ConfigurePrintManagement1)
    - [Bir serbest metin faturası yazdır](#ProcessInvoice1)

- [Standart ER biçimini Özelleştirme](#CustomizeProvidedFormat)

    - [Özel biçim oluşturma](#DeriveProvidedFormat)
    - [Özel biçimi düzenleme](#ConfigureDerivedFormat)
    - [Özel biçimi çalıştırılabilir olarak işaretleme](#MarkFormatRunnable)

- [Özel ER biçimini kullanarak serbest metin faturası yazdırma](#PrintInvoice2)

    - [Yazdırma yönetimini ayarlama](#ConfigurePrintManagement2)
    - [Bir serbest metin faturası yazdır](#ProcessInvoice2)

- [Ek kaynaklar](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Tüzel kişilik yapılandırma

1. **Kuruluş yönetimi** \> **Kuruluşlar** \> **Tüzel kişilikler**'e gidin.
2. **Tüzel kişilikler** sayfasında, **Rapor şirketi logo resmi** hızlı sekmesinde, **Değiştir**'i seçin.
3. **Karşıya yüklenecek görüntü dosyasını seç** iletişim kutusunda **Gözat**'ı seçin ve daha önce indirdiğiniz **Company logo.png** dosyasını seçin.
4. **Kaydet**'i seçin ve ardından **Tüzel kişilikler** sayfasını kapatın.

![Tüzel kişilikler sayfasında seçilen şirket logosu resmi.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>ER altyapısını yapılandırma

Elektronik raporlama işlevi ile ilgili bir kullanıcı olarak, standart bir ER biçiminin özel bir sürümünü tasarlamak için ER çerçevesini kullanmaya başlamadan önce en düşük ER alt uygulama parametreleri kümesini konfigüre etmelisiniz.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER parametrelerini yapılandırma

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Elektronik raporlama parametreleri** kutucuğunu seçin.
3. **Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.
4. **Ekler** sekmesinde, aşağıdaki parametreleri ayarlayın:

    - **Konfigürasyonlar** alanında, **USMF** şirketi için **dosya** türünü seçin.
    - **İş arşivi**, **Geçici**, **temel** ve **diğer** alanlarında **Dosya** tipini seçin.

ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

Eklenen her ER yapılandırması bir ER konfigürasyon sağlayıcısı tarafından sahiplenilimli olarak işaretlenir. **Elektronik raporlama** çalışma alanında etkinleştirilen ER yapılandırma sağlayıcısı Bu amaçla kullanılır. Bu nedenle, ER konfigürasyonlarını eklemeye veya düzenlemeye başlamadan önce, **elektronik raporlama** çalışma alanında bir er yapılandırma sağlayıcısını etkinleştirmelisiniz.

> [!NOTE]
> ER yapılandırması yalnızca yapılandırmanın sahibi tarafından düzenlenebilir. ER yapılandırmasını düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **Elektronik raporlama** çalışma alanında etkinleştirilmelidir.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER yapılandırma sağlayıcıları listesini gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.
3. **Yapılandırma sağlayıcısı tablosu** sayfasında, her sağlayıcı kaydının benzersiz bir adı ve URL'si vardır. Bu sayfanın içeriğini gözden geçirin. **Litware, Inc.** (`https://www.litware.com`) için zaten bir kayıt varsa, sonraki yordamı atlayıp [Yeni bir ER yapılandırma sağlayıcısı ekleyin](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Yeni bir ER yapılandırması sağlayıcısı ekleme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.
3. **Yapılandırma sağlayıcıları** sayfasında, **Yeni**'yi seçin.
4. **Ad** alanına **Litware, Inc.** yazın.
5. **İnternet adresi** alanına `https://www.litware.com` girin.
6. **Kaydet**'i seçin.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Yeni ER yapılandırma sağlayıcısını etkinleştirme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme konfigürasyonları** sayfasında, **Konfigürasyon sağlayıcıları** bölümünde, **Litware, Inc.** döşemesini seçin ve sonra **etkin ayarla**'yı seçin.

ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standart ER biçimi yapılandırmalarını içe aktarın

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Standart ER yapılandırmalarını içe aktarın

Dynamics 365 Finance'un geçerli örneğine standart ER yapılandırmalarını eklemek için onları o örnek için yapılandırılmış olan ER [deposundan](general-electronic-reporting.md#Repository) içe aktarmanız gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma Sağlayıcıları** bölümünde **Microsoft** kutucuğunu seçin ve **Microsoft** sağlayıcısı için depolar listesini görüntülemek için **Depolar**'ı seçin.
3. **Yapılandırma depoları** sayfasında, **Global** türünün deposunu seçin ve sonra **Aç**'ı seçin. [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md)'e bağlanmak için yetkilendirme istenirse, yetkilendirme yönergelerini uygulayın.
4. **Yapılandırma deposu** sayfasında, sol bölmedeki yapılandırma ağacında, **Serbest metin faturası (Excel)** biçim yapılandırmasını seçin.
5. **Sürümler** hızlı sekmesinde, seçili ER biçimi yapılandırmasının en son sürümünü (örneğin, **240.112**) seçin.
6. Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.

![Yapılandırma deposu sayfasındaki standart ER yapılandırmalarını içe aktarın.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> [Global depoya](er-download-configurations-global-repo.md) erişmede sorun yaşıyorsanız, Microsoft Dynamics Lifecycle Services'den (LCS) gelen [yapılandırmaları karşıdan yükleyebilirsiniz](download-electronic-reporting-configuration-lcs.md).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>İçe aktarılan ER yapılandırmalarını gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Fatura modeli**'ni genişletin.
4. Seçili **Serbest metin faturası (Excel)** ER biçimine ek olarak, gerekli diğer ER yapılandırmaları da içer aktarılmıştır. Aşağıdaki ER yapılandırmaların konfigürasyon ağacında kullanılabilir durumda olduğundan emin olun:

    - **Fatura modeli** – Bu yapılandırma, faturalama iş etki alanının veri yapısını temsil eden veri modeli bileşenini içerir.
    - **Fatura modeli eşleştirmesi** – Bu yapılandırma, veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulduğunu açıklayan model eşleme bileşeni içerir.
    - **Serbest metin faturası (Excel)** – Bu yapılandırma biçim  ve biçim eşleme ER bileşenlerini içerir. Biçim bileşeni, Excel biçimindeki bir şablonu esas alan rapor düzenini belirtir. Biçim eşleme bileşeni model veri kaynağını içerir ve çalışma zamanında bu veri kaynağı kullanılarak rapor düzeninin nasıl doldurulacağını belirtir.

![Yapılandırmalar sayfasındaki içe aktarılan ER yapılandırmaları.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Standart ER biçimini kullanarak serbest metin faturası yazdırma

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Yazdırma yönetimini ayarlama

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **Serbest metin faturası** sayfasında, **FTI-00000002** faturasını seçin ve sonra Eylem Bölmesinde, **Fatura** sekmesinde, **Yazdırma Yönetimi** grubunda, **Yazdırma Yönetimi**'ni seçin.
3. **Yazdırma Yönetimi Kurulumu** sayfasında, soldaki ağaçta, **Modül - alacak hesapları \> Belgeler \> Serbest metin faturası** nı genişletin ve **Orijinal \<Default\>** maddeyi seçin.
4. **Rapor biçimi** alanında **Serbest metin faturası (Excel)** öğesini seçin.
5. **Yazdırma yönetimi kurulumu** sayfasından çıkmak ve **Serbest metin faturası** sayfasına dönmek için **Esc** tuşunu seçin.

![Yazdırma yönetimi kurulumu sayfasındaki standart ER biçiminde serbest metin faturasının yönetim ayarlarını yazdırın.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Bir serbest metin faturası yazdır

1. **Serbest metin faturası** sayfasında, **FTI-00000002** faturasının seçili olduğundan emin olun ve sonra Eylem Bölmesinde, **Fatura** sekmesinde, **Belge** grubunda, **Yazdır** \> **Seçili**'yi seçin.
2. Oluşturulan faturayı Excel biçiminde indirin ve önizleme için açın.
3. Sağlanan ER biçimi için Excel şablonunun yapısına uygun olarak, oluşturulan faturanın sayfa altbilgisi, geçerli sayfa numarası ve rapordaki sayfaların toplam sayısı hakkında bilgi içerir.

![Oluşturulan serbest metin faturası.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Standart ER biçimini Özelleştirme

Bu bölümdeki örnekte, Excel biçiminde serbest metin faturası oluşturmak için Microsoft tarafından sağlanan ER yapılandırmalarını kullanabilirsiniz. Ancak, şirket logosu görüntüsünü oluşturulan faturaların sayfa alt bilgisine yerleştirmek için bir özelleştirme eklemeniz gerekir.

Bu durumda, Litware, Inc. temsilcisi olarak, Microsoft tarafından sağlanan bir **Serbest metin faturası** yapılandırmasını temel alan yeni bir ER biçimi yapılandırması oluşturmanız (türetmeniz) gerekir.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Özel biçim oluşturma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Fatura modeli**'ni genişletin ve **Serbest metin faturası (Excel)** öğesini seçin. Litware, Inc. özel sürümün temeli olarak bu ER biçimi yapılandırmasının içer aktarılan sürümünü (örneğin **240.112**) kullanacaktır.
3. Açılır iletişim kutusunu açmak için **Yapılandırma oluştur**'u seçin. Bu iletişim kutusunu, özel ödeme biçimi için yeni bir yapılandırmak oluşturmak için kullanın.
4. **Yeni** alan grubunda, **Addan türet: Serbest metin faturası (Excel), Microsoft** seçeneğini seçin.
5. **Ad** alanında **Serbest metin faturası (Excel) özel** öğesini girin.
6. **Yapılandırma oluştur**'u seçin.

![Yapılandırma oluştur açılan iletişim kutusunda özel ödeme biçimi için yapılandırma oluşturma.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

**Serbest metin faturası (Excel) özel** Er biçimi yapılandırmasının 240.112.1 sürümü oluşturulur. Bu sürüm **taslak** [durumuna](general-electronic-reporting.md#component-versioning) sahip ve düzenlenebilir. Özel ER biçiminizin geçerli içeriğinin,  Microsoft tarafından sağlanan biçimin içeriğiyle aynıdır.

![Yapılandırmalar sayfasında oluşturulan ER biçimi yapılandırmasının yeni sürümü.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Özel biçimi düzenleme

Özel biçiminizi, bir şirket logosu resminin raporun her sayfasındaki alt bilgiye yerleştirileceği şekilde yapılandırın.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **Serbest metin faturası (Excel) özel** öğesini seçin.
3. **Sürümler** FastTab üzerinde, seçili yapılandırmasının gerekli **240.112.1** sürümünü seçin.
4. **Tasarımcı**’yı seçin.
5. **Biçim tasarımcısı** sayfasında Format öğeleriyle ilgili daha fazla bilgi görüntülemek için **ayrıntıları göster** 'i seçin.
6. Aşağıdaki öğeleri genişletip gözden geçirin:

    - **Excel** türünde **Serbest metin faturası** öğesi. Bu öğe, Excel çalışma kitabı biçiminde bir fatura oluşturmak için kullanılır.
    - **Sayfa** türünde **Serbest metin faturası \\ Fatura** öğesi. Bu öğe, oluşturulan Excel çalışma kitabının bir çalışma sayfasını oluşturmak için kullanılır.
    - **Alt bilgi** türünde **Serbest metin faturası \\ Fatura \\ Alt bilgi** öğesi. Bu öğe, fatura alt bilgisini doldurmak için kullanılır.

7. **Serbest metin faturası \\ Fatura \\ Altbilgi** öğesini seçin.

    ![ER işlemleri tasarımcısında alt bilgi ögesi.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Oluşturulan bir faturanın her sayfa alt bilgisi, geçerli sayfa numarası ve rapordaki sayfaların toplam sayısı hakkında bilgi içerir. Gördüğünüz gibi, **Serbest metin faturası \\ Fatura \\ Alt bilgi** öğesi alt öğe içermez. Bu nedenle, kullanılmakta olan Excel şablonu, tüm rapor alt bilgisi merkezinde sayfalama ayrıntılarını gösterecek şekilde yapılandırılmıştır.

8. **Ekle**'yi seçin ve sonra eklemekte olduğunuz biçim öğesinin **Excel \\ Resim** türünü seçin:

    1. **Hizalama** alanında, **Sağ**'ı seçin.
    2. **Yüksekliği Ölçekle** alanında **Göreli**'yi seçin.
    3. **Yüzde cinsinden ölçekle** alanına **70** girin.
    4. **Tamam**'ı seçin.

        > [!NOTE]
        > **Excel \\ Resim** öğesi, şirket logosu görüntüsü eklemek ve bunu sayfa alt bilgisinin sağ tarafına hizalamak için kullanılır.

    ![Bileşen özellikleri iletişim kutusundaki Resim öğesinin özellikleri.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Soldaki biçim yapısı ağacında, yeni eklediğiniz **Resim** öğesini seçin ve **Eşleme** sekmesinde **Model** veri kaynağını genişletin.
10. **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo** öğesini genişletin ve **model.InvoiceBase.CompanyInfo.Logo** veri kaynağı alanını seçin. [Kapsayıcı](er-formula-supported-data-types-composite.md#container) türündeki veri kaynağı alanı Şirket logosu görüntüsünü ortam içeriği olarak gösterir.
11. **Bağla**'yı seçin. **Resim** biçim öğesi şimdi **model.InvoiceBase.CompanyInfo.Logo** veri kaynağı alanı ile bağlanmıştır. Bu nedenle, çalışma zamanında şirket logosu resmi oluşturulan faturaların alt bilgisine yerleştirilir.

    ![ER İşlemleri tasarımcısındaki model.InvoiceBase.CompanyInfo.Logo veri kaynağı alanıyla sınırlanan resim biçimi öğesi.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. **Kaydet**'i seçin ve **Tasarımcı** sayfasını kapatın.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Özel biçimi çalıştırılabilir olarak işaretleme

Özel biçimin ilk sürümü oluşturulduğundan ve **Taslak** durumunda olduğundan, biçimi test amacıyla çalıştırabilirsiniz. Raporu çalıştırmak için, özel işlem biçiminizi ifade eden ödeme yöntemini kullanarak bir satıcı ödemesini işleyin. Varsayılan olarak, uygulamadan ER biçimini çağırdığınızda yalnızca **Tamamlandı** ve **Paylaşıldı** durumuna sahip sürümler [dikkate alınır](general-electronic-reporting.md#component-versioning). Bu davranış, bitmemiş tasarımları bulunan ER biçimlerinin kullanılmasını önlemeye yardımcı olur. Ancak, test çalışmalarınız için, uygulamayı **taslak** durumunda olan ER formatının biçimini kullanmaya zorlayabilirsiniz. Bu şekilde, herhangi bir değişiklik gerekiyorsa geçerli biçim sürümünü ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Uygulanabilirlik](electronic-reporting-destinations.md#applicability).

ER biçiminin taslak sürümünü kullanmak için, ER biçimini açık olarak işaretlemeniz gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Çalıştırma ayarları** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.
4. Geçerli sayfayı düzenlenebilir yapmak için **Düzenle**'yi seçin ve ardından sol bölmedeki yapılandırma ağacında **Serbest metin faturası (Excel) özel** öğesini seçin.
5. **Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın.

![Özel biçimi, Yapılandırmalar sayfasında çalıştırılabilir olarak işaretleme.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Özel ER biçimini kullanarak serbest metin faturası yazdırma

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Yazdırma yönetimini ayarlama

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **Serbest metin faturası** sayfasında, **FTI-00000002** faturasını seçin ve sonra Eylem Bölmesinde, **Fatura** sekmesinde, **Yazdırma Yönetimi** grubunda, **Yazdırma Yönetimi**'ni seçin.
3. **Yazdırma Yönetimi Kurulumu** sayfasında, soldaki ağaçta, **Modül - alacak hesapları** \> **Belgeler** \> **Serbest metin faturası**'nı genişletin ve **Orijinal** **\<Default\>** maddeyi seçin.
4. **Rapor biçimi** alanında **Serbest metin faturası (Excel) özel** öğesini seçin.
5. **Yazdırma yönetimi kurulumu** sayfasından çıkmak ve **Serbest metin faturası** sayfasına dönmek için **Esc** tuşunu seçin.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Bir serbest metin faturası yazdır

1. **Serbest metin faturası** sayfasında, **FTI-00000002** faturasının seçili olduğundan emin olun ve sonra Eylem Bölmesinde, **Fatura** sekmesinde, **Belge** grubunda, **Yazdır** \> **Seçili**'yi seçin.
2. Oluşturulan faturayı Excel biçiminde indirin ve önizleme için açın.
3. Özel ER biçiminin yapısına uygun olarak, oluşturulan faturanın sayfa alt bilgisi, raporun sayfalama bilgileri ile ilgili bilgilerin yanı sıra şirket logosu resmini de içerir.

![Sayfa alt bilgisinde şirket logosu resmi olan serbest metin faturası oluşturuldu.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Ek kaynaklar

- [Excel biçiminde belgeler oluşturmak için yapılandırma tasarlama](er-fillable-excel.md)
- [Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)
