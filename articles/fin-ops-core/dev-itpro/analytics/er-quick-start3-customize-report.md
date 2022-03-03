---
title: Elektronik bir belge oluşturmak için elektronik raporlama yapılandırmalarını özelleştirme
description: Bu konu, Microsoft tarafından sağlanan ve özel elektronik belge oluşturmak için kullanılan elektronik raporlama (ER) yapılandırmalarının nasıl özelleştirileceğini açıklamaktadır.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c8cf4866b6a8c239359d726d8cd4f03a9eb4137
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324099"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Elektronik bir belge oluşturmak için elektronik raporlama yapılandırmalarını özelleştirme

[!include[banner](../includes/banner.md)]

[Elektronik raporlama (ER) çerçevesi](general-electronic-reporting.md) Microsoft'un Microsoft Dynamics 365 Finance kurulumunuza sağladığı ER [yapılandırmalarını](general-electronic-reporting.md#Configuration) karşıya yüklemenize olanak tanır. Bu şekilde, Microsoft tarafından sağlanan yapılandırmalar elektronik müşteri faturaları (e-faturalar) oluşturmak için kullanılan ER çözümü olarak hizmet verebilir. Özel veritabanı alanlarınıza erişmek ve kaynak kodu düzenlemeye gerek kalmadan belirli gereksinimleriniz ile uyumlu olan e-faturaları oluşturmak için özel ER çözümünüzü yapılandırmak amacıyla bu ER çözümünü kullanabilirsiniz.

## <a name="overview"></a>Genel bakış

Bu konudaki örnek için, elektronik olarak faturalamak istediğiniz her müşterinin yeni özel özniteliği olarak bir federal vergi kimlik kodu belirtmeniz gerekir. Bu nedenle, oluşturulan her e-faturada vergi koduyla doldurulması gereken yeni bir madde ekleyerek geçerli olarak kullanılmakta olan faturanın yapısını özelleştirmeniz gerekir.

Bu konudaki yordamlarda, Sistem Yöneticisi, Elektronik Raporlama Geliştiricisi veya elektronik raporlama işlevsel danışmanı rolündeki bir kullanıcının bu görevleri Finans kurulumunuzda nasıl gerçekleştirebileceği açıklanmaktadır:

- [ER çerçevesini kullanmaya başlamak için gereken en az ER parametre kümesini yapılandırın](#ConfigureER).
- [E-faturalar oluşturmak için sağlanan standart ER konfigürasyonların başlangıç sürümlerini içe aktarın](#ImportERConfigurations1).
- [Standart ER yapılandırmalarını kullanmaya başlamak için alacak hesapları parametrelerini yapılandırın](#ConfigureAR1).
- [Müşterileri faturalamak için yasal varlık parametrelerini yapılandırın](#ConfigureLE).
- [Elektronik faturalama için müşteri kaydı hazırlayın](#ConfigureCustomer1).
- [Standart ER yapılandırmalarını kullanarak bir müşteri faturası ekleyin, deftere nakledin ve gönderin](#ProcessInvoice1).
- [Müşteriler için federal vergi kimlik kodunu yönetmek üzere özel bir veritabanı alanı ekleyin](#AddCustomField).
- [ER model eşleme Tasarımcısı için veritabanı değişikliklerini etkinleştirmek üzere, ER meta verilerini yenileyin](#RefreshERMetadata).
- [Yeni vergi kodunu içeren e-faturalar oluşturmak için özel ER konfigürasyonları tasarlayın](#DesignCustomERConfigurations).
- [Özel ER yapılandırmalarını kullanmaya başlamak için alacak hesapları parametrelerini yapılandırın](#ConfigureAR2).
- [Elektronik faturalama için müşteri kaydı güncelleştirin](#ConfigureCustomer2).
- [Özel ER yapılandırmalarını kullanarak bir müşteri faturası ekleyin, deftere nakledin ve gönderin](#ProcessInvoice2).
- [E-faturalar oluşturmak için sağlanan standart ER konfigürasyonların yeni sürümlerini içe aktarın](#ImportERConfigurations2).
- [Değişiklikleri özel ER yapılandırmalarınızın içindeki standart ER yapılandırmalarının yeni sürümlerine uygulayın](#RebaseCustomERConfigurations).
- [Özel ER yapılandırmalarının yeni sürümlerini kullanarak bir müşteri faturası ekleyin, deftere nakledin ve gönderin](#ProcessInvoice3).

Bu yordamların hepsi **DEMF** şirketinde gerçekleştirilebilir.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>ER altyapısını yapılandırma

Elektronik raporlama işlevsel danışmanı veya elektronik raporlama geliştiricisi rolündeki bir kullanıcı olarak, en az ER parametresi kümesini yapılandırmalısınız. Daha sonra, e-faturalar oluşturmak için kullanılan ER çözümünün standart konfigürasyonlarının özel sürümlerini tasarlamak için ER çerçevesini kullanmaya başlayabilirsiniz.

### <a name="configure-er-parameters"></a>ER parametrelerini yapılandırma

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Elektronik raporlama parametreleri** kutucuğunu seçin.
3. **Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.
4. **Ekler** sekmesinde, **Yapılandırmalar** alanında, **Dosya**'yı seçin.
5. **İş arşivi**, **Geçici**, **temel** ve **diğer** alanlarında **Dosya** tipini seçin.

ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

Eklenen her ER yapılandırması bir ER konfigürasyon sağlayıcısı tarafından sahiplenilimli olarak işaretlenir. **Elektronik raporlama** çalışma alanında etkinleştirilen ER yapılandırma sağlayıcısı Bu amaçla kullanılır. Bu nedenle, ER konfigürasyonlarını eklemeye veya düzenlemeye başlamadan önce, **elektronik raporlama** çalışma alanında bir er yapılandırma sağlayıcısını etkinleştirmelisiniz.

> [!NOTE]
> Yalnızca ER yapılandırmasının sahibi bunu düzenleyebilir. Bu nedenle, ER konfigürasyonu düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **elektronik raporlama** çalışma alanında etkinleştirilmelidir.

#### <a name="review-the-list-of-er-configuration-providers"></a>ER yapılandırma sağlayıcıları listesini gözden geçirin

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

#### <a name="activate-an-er-configuration-provider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme konfigürasyonları** sayfasında, **Konfigürasyon sağlayıcıları** bölümünde, **Litware, Inc.** döşemesini seçin ve sonra **etkin ayarla**'yı seçin.

ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Standart ER yapılandırmalarının başlangıç sürümlerini içe aktarın

Geçerli Finans kurulumunuza standart ER yapılandırmalarını eklemek için bu yapılandırmaları o kurulum için yapılandırılmış olan ER [deposundan](general-electronic-reporting.md#Repository) içe aktarmanız gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma Sağlayıcıları** bölümünde **Microsoft** kutucuğunu seçin ve Microsoft sağlayıcısı için depolar listesini görüntülemek için **Depolar**'ı seçin.
3. **Yapılandırma depoları** sayfasında, **Global** türünün deposunu seçin ve sonra **Aç**'ı seçin. Regulatory Configuration Service bağlanmak için yetkilendirme istenirse, yetkilendirme yönergelerini uygulayın.
4. **Yapılandırma deposu** sayfasında, sol bölmedeki yapılandırma ağacında, **Peppol Satış Faturası** biçim yapılandırmasını seçin.
5. **Sürümler** hızlı sekmesinde, sürüm **11.2.2**' i seçin.
6. Seçili sürümü Global depodan indirmek için **İçe Aktar**'ı seçin.

![Yapılandırma deposu sayfası.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> [Global depoya](er-download-configurations-global-repo.md) erişmede sorun yaşıyorsanız, Microsoft Dynamics Lifecycle Services'den (LCS) gelen [yapılandırmaları karşıdan yükleyebilirsiniz](download-electronic-reporting-configuration-lcs.md).

### <a name="review-the-imported-er-configurations"></a>İçe aktarılan ER yapılandırmalarını gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırmalar** sayfasında, **Yapılandırma bileşenleri** hızlı sekmesini genişletin.
4. Sol bölmedeki yapılandırma ağacında, **Fatura modelini** genişletin ve sonra **UBL satış faturası** öğesini genişletin.

Seçili **Peppol Satış Faturası** ER biçimine ek olarak, gerekli diğer ER yapılandırmalarının da içe aktarıldığına dikkat edin. İlgili çözümlerin yeni gereksinimlerle uyumlu kalması için ER yapılandırmalarının yeni sürümleri Global depoda ve LCS'de sürekli olarak yayımlandığından gerekli veri modeli yapılandırmasının son sürümleri ve model eşleme yapılandırmaları içe aktarılır.

![Yapılandırmalar sayfası.](./media/er-quick-start3-imported-solution1a.png)

Geçmişte (örneğin, 7 Ağustos 2019) **Peppol satış faturası**'nın **11.2.2** sürümünü içe aktarsaydınız geçerli finans kurulumundaki ER yapılandırmalarının içinde bulunacağı durumun benzetimini yapmak için aşağıdaki adımları izleyin.

- 7 Ağustos 2019 tarihinden sonra yayımlanan tüm ER yapılandırmalarını silmek için eylem bölmesinde **Sil**'i seçin. Tek **Fatura modeli**, **Fatura modeli eşlemesi** (önceki adı **Müşteri fatura modeli eşlemesi**), **UBL satış faturası** ve **Peppol satış faturası** yapılandırmaları bırakılmalıdır.
- Kalan yapılandırmalar için, **Sürümler** hızlı sekmesinde, 7 Ağustos 2019'dan sonra yayımlanan ER yapılandırmalarının tüm sürümlerini silmek için **Sil**'i seçin.

Ardından aşağıdaki yapılandırmaların yapılandırma ağacında kullanılabilir durumda olduğunu doğrulayın:

- **Fatura modeli** ER veri modeli konfigürasyonu (önceki adı **Müşteri fatura modeli**):

    - Sürüm 11, Faturalama iş etki alanının veri yapısını temsil eden veri modeli ER bileşeninin 10. sürümünü içerir. Bu ER yapılandırması içe aktarma için seçilmiş olan **Peppol satış faturası** ER biçiminin bir üst öğesi olarak içe aktarılır.
    - Sürüm 50, veri modeli ER bileşeninin 31. sürümünü içerir. Bu ER yapılandırması **Fatura modeli eşlemesi** ER model eşleme yapılandırmasının 7 Ağustos 2019 sürümünün bir üst öğesi olarak içe aktarılır.

    ![Yapılandırmalar sayfasındaki fatura modeli ER veri modeli yapılandırması.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Bu veri modelinin 50. sürümünü göremiyorsanız, Global depoyu açın ve **Fatura modeli eşleme** ER yapılandırmasının 50.19. sürümünü içe aktarın.

- **Fatura modeli eşleme** ER modeli eşleme yapılandırması (önceki adı **Müşteri fatura modeli eşleme**):

    - 50.19 sürümü, **Fatura modeli** Er veri modeli yapılandırmasının 50. sürümünün en son uygulaması olarak içe aktarıldı. Veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulduğunu açıklayan iki model eşleme ER bileşeni içerir.

    ![Yapılandırmalar sayfasındaki fatura modeli eşleme ER modeli eşleme yapılandırması.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Bu model eşlemenin 50.19. sürümünü göremiyorsanız, Global depoyu açın ve **Fatura modeli eşleme** ER yapılandırmasının 50.19. sürümünü içe aktarın.

- **UBL Satış faturası** ER biçim yapılandırması:

    - Sürüm 11.2 biçimi ve biçim eşleme ER bileşenlerini içerir. Format bileşeni rapor düzenini belirtir. Biçim eşleme bileşeni model veri kaynağını içerir ve çalışma zamanında bu veri kaynağı kullanılarak rapor düzeninin nasıl doldurulacağını belirtir. Bu ER biçimi, Evrensel İş Dili (UBL) biçiminde e-faturalar oluşturmak üzere yapılandırılmıştır. İçe aktarma için seçilmiş olan **Peppol satış faturası** ER biçiminin bir üst öğesi olarak içe aktarılır.

- **Peppol Satış faturası** ER biçim yapılandırması:

    - 11.2.2 sürümü, Pan-European Public Procurement OnLine (PEPPOL) formatında e-faturalar oluşturmak üzere yapılandırılmış biçim ve biçim eşleme ER bileşenlerini içerir.

    ![Yapılandırmalar sayfasındaki Peppol Satış Faturası ER biçimi yapılandırması.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Alacak hesapları parametrelerini yapılandırın

1. **Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin.
2. **Elektronik belgeler** sekmesinde, **Elektronik raporlama** hızlı sekmesinde, **Satışlar ve serbest metin faturası** alanında, **PEPPOL satış faturası** seçeneğini belirleyin.
3. **Kaydet**'i seçin.

![Alacak hesapları parametreleri sayfasındaki elektronik belgeler sekmesi.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Tüzel kişilik parametrelerini konfigüre edin

1. **Kuruluş yönetimi** \> **Kuruluşlar** \> **Tüzel kişilikler**'e gidin.
2. Seçili **DEMF** şirketi için **Banka hesap bilgileri** hızlı sekmesinde, **Rota numarası** alanına, **1234** girin.
3. **Kaydet**'i seçin.
4. **Tüzel kişilikler** sayfasını kapatın.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Müşteri kaydı hazırlama

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. **Tüm müşteriler** sayfasında, **DE-014** müşteri hesabı bağlantısını seçin.

### <a name="add-a-customer-contact"></a>Müşteri ilgili kişisi ekleme

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. Eylem Bölmesi'nde, **Müşteri** sekmesindeki **Hesaplar** grubunda **İlgili Kişiler**'i seçin.
3. **İlgili kişi ekle**'yi seçin.
4. **İlgili kişiler** sayfasında, **Adı** alanında aramayı açın, **Adam Carter**'ı seçin ve aramayı kapatmak için **Seç**'i seçin.
5. **Kaydet**'i seçin.
6. **İlgili Kişiler** sayfasını kapatın.

### <a name="define-a-primary-contact"></a>Birincil ilgili kişi tanımla

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. **Satış demografisi** hızlı sekmesinde, **birincil ilgili kişi** alanında, **Adam Carter**'ı seçin.

### <a name="set-the-e-invoicing-option"></a>E-faturalama seçeneğini ayarlama

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. **Fatura ve teslimat** hızlı sekmesinde, **E-fatura** seçeneğini **Evet** olarak ayarlayın.
3. **Kaydet**'i seçin.
4. **Tüm müşteriler** sayfasını kapatın.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Standart ER yapılandırmalarını kullanarak bir müşteri faturası işleme

Artık içe aktardığınız standart ER yapılandırmalarını, müşteriye elektronik olarak serbest metin faturası göndermek için kullanabilirsiniz.

### <a name="add-a-new-invoice"></a>Yeni bir fatura ekleme

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **Serbest metin faturası** sayfasında, **yeni**'yi seçin.
3. **Serbest metin fatura başlığı** hızlı sekmesinde, **müşteri hesabı** alanında, **DE-014** seçeneğini belirleyin.
4. **Fatura satırları** hızlı sekmesinde, bir fatura satırı otomatik olarak eklenir. Bu satır için aşağıdaki alanları ayarlayın:

    - **Açıklama** alanında, **Not defteri**'ni girin.
    - **Ana hesap** alanında **401100** değerini seçin.
    - **Birim fiyatı** alanına **1000** yazın.

5. **Kaydet**'i seçin.

![Serbest metin faturası sayfası.](./media/er-quick-start3-add-invoice.png)

Daha fazla bilgi için bkz. [Serbest metin faturası oluşturun](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Yeni bir faturayı deftere nakletme

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **Serbest metin faturası** sayfasında, eylem bölmesinde, **Deftere Naklet**'i seçin.
3. **Serbest metin faturasını deftere naklet** iletişim kutusunda **Tamam**'ı seçin.

![Serbest metin faturası ayrıntıları sayfası.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Deftere nakledilmiş bir fatura gönder

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **Serbest metin faturası** sayfasında, eylem bölmesinde, **Belge** grubunda **Gönder** \> **Orijinal**'i seçin.

    ![Orijinal faturanın önizlemesi.](./media/er-quick-start3-send-invoice.png)

3. **Serbest metin faturası** sayfasını kapatın.

### <a name="analyze-a-generated-e-invoice"></a>Oluşturulan e-faturayı analiz etme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama işleri**'ne gidin.
2. **Elektronik raporlama işleri** sayfasında, **E-fatura XML gönder** görev açıklamasına sahip ilk kaydı seçin.
3. Oluşturulan dosyalar listesine erişmek için **dosyaları göster**'i seçin.

    ![Elektronik raporlama işleri sayfası.](./media/er-quick-start3-jobs-list.png)

4. Oluşturulan e-fatura XML dosyasını indirmek için **Aç**'ı seçin.
5. E-fatura XML dosyasını analiz edin. Müşteri vergi şemasının şu anda, **schemeID** ve **schemeAgencyID** XML öznitelikleriyle gösterildiğine dikkat edin. Ayrıca, **cbc.CustomizationID** XML öğesinin şu anda aşağıdaki metni içerdiğini da unutmayın: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Oluşturulan e-fatura XML dosyasının önizlemesi.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Özel veritabanı alanı ekle

Geçerli finans kurulumunda aşağıdaki özelleştirmeyi yapmak için [özel alan](../../fin-ops/get-started/user-defined-fields.md) özelliğini kullanabilirsiniz:

- Her müşteri için bir federal vergi kimlik kodu saklayan yeni bir özel veritabanı alanı ekleyerek veritabanı yapısını özelleştirin.
- Yeni özel veritabanı alanına vergi kodu değeri girmek için kullanılabilecek yeni bir veri girişi alanı ekleyerek **müşteri** sayfasını özelleştirin.

Bu adımları izleyerek özelleştirme yapın.

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. **Tüm müşteriler** sayfasında, **DE-014** müşteri hesabı bağlantısını seçin.
3. **Genel** hızlı sekmesinde, **dil** alanının altında herhangi bir boş alanı sağ tıklatın ve sonra **Kişiselleştir: Üst Grup**'u seçin.

    **Genel** Hızlı sekmesinin içeriği vurgulanır ve **Kişiselleştirme** menüsü görüntülenir.

4. **Kişiselleştir** menüsünde **Alan Ekle**'yi seçin.
5. **Sütun Ekle** iletişim kutusunda **Yeni alan oluştur**'u seçin.
6. **Yeni alan oluştur** iletişim kutusunda, **tablo adı** alanında, **müşteriler**'i seçin.
7. **Ad öneki** alanına **FederalTaxID** yazın.

    > [!NOTE]
    > Tüm alan adı otomatik olarak **FederalTaxID\_Özel** şeklinde tanımlanır.

8. **Etiket** alanına, **Federal Vergi Kimliği** yazın.
9. **Tür** alanında, **Metin**'i seçin.
10. **Uzunluk** alanına **20** yazın.
11. **Kaydet**'i seçin.
12. Görünen ileti kutusunda, **Müşteriler** tablosu için yeni bir **federaltaxıd** alan girişi oluşturmak istediğinizi onaylamak için **Evet**'i seçin.
13. Geçerli sayfaya **FederalTaxID\_Özel** alanını eklemek için, **Ekle** <a name="insert_custom_field"></a> öğesini seçin.

    ![Tüm müşteriler sayfası.](./media/er-quick-start3-create-new-field.gif)

14. **Tüm müşteriler** sayfasını kapatın.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>ER meta verilerini Yenile

ER model eşleme tasarımcısında eklediğiniz özel alanı [görünür](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) hale getirmek için ER meta verileri yenilemeniz gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Tablo referanslarını yeniden oluştur**'a gidin.
2. **Veri modelini Güncelleştir** iletişim kutusunda **Tamam**'ı seçin.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Özel ER yapılandırmalarını tasarlama

Yeni vergi kodunu içeren e-faturalar oluşturabilmek üzere özel ER yapılandırmalarınızı tasarlamak için Microsoft tarafından sağlanan ER yapılandırmalarını kullanabilirsiniz.

### <a name="customize-the-data-model-configuration"></a>Veri modeli yapılandırmasını özelleştirme

Elektronik raporlama işlevsel danışmanı rolünde bir kullanıcı olarak, özel ER veri modelinizi tasarlayabilirsiniz.

#### <a name="add-a-custom-data-model-configuration"></a>Özel bir veri modeli yapılandırması ekleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Müşteri fatura modeli**'ni seçin.
3. Eylem Panosundan **Yapılandırma oluştur**'u seçin.
4. Açılan iletişim kutusunda **Yeni** alanında, yeni özel ER veri modeli yapılandırmasının ER veri modeli yapılandırmasına dayalı olması gerektiğini belirtmek için **İsimden Türet: Müşteri faturası modeli, Microsoft** seçeneğini belirleyin.
5. **Ad** alanına **Fatura modeli (Litware)** değerini girin.
6. Yeni ER yapılandırmasını eklemek için **Yapılandırma oluştur**'u seçin.

**Taslak** [durumundaki](general-electronic-reporting.md#component-versioning) **fatura modeli (Litware)** ER yapılandırmasının 50.1. sürümünü düzenlemek için artık ER veri modeli tasarımcısını kullanabilirsiniz.

![Yapılandırmalar sayfasındaki ER yapılandırmasının 50.1 sürümü.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Özel veri modeli yapılandırma

Federal vergi kimlik kodu değerini sağlamak üzere yeni bir alan ekleyerek özel veri modelinizi değiştirmeniz gerekir. Bu kod, veri kaynağı olarak bu veri modelini kullanacak her ER biçimi için müşteri verisinin bir parçasıdır.

1. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **fatura modeli (Litware)**'i seçin.
2. **Sürümler** hızlı sekmesinde **Taslak** durumundaki seçili ER biçim yapılandırmasının **50.1** sürümünü seçin.
3. Eylem bölmesinde, Seçili yapılandırma sürümü için **tasarımcı**'yı seçin.
4. **Veri modeli Tasarımcısı** sayfasında, veri modeli ağacında **Müşteri bilgilerini (müşteri)** seçin.
5. **Yeni**'yi seçin.
6. Açılan iletişim kutusunda, **Yeni düğüm biçimi** alanında **etkin bir düğümün al öğesi** varsayılan değerini kabul edin.
7. **Ad** alanına **FederalTaxID\_Litware** yazın.
8. **Madde türü** alanında varsayılan değer olan **dizeyi** kabul edin.
9. **Ekle**'yi seçin ve sonra **Kaydet**'i seçin.

    ![Veri modeli tasarımcısı sayfası.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > **Etiket** ve **Açıklama** alanları yeni alanın amacını açıklar. Bu alanları birden çok dilde doldurabilirsiniz. Daha fazla bilgi için bkz. [Elektronik raporlamada çok dilli rapor tasarlama](er-design-multilingual-reports.md).

10. **Veri modeli tasarımcısı** sayfasını kapatın.

#### <a name="complete-a-custom-data-model-configuration"></a>Özel bir veri modeli yapılandırması tamamlama

Diğer özel ER yapılandırmalarının eklenebilmesi için, özel ER veri modeli yapılandırmanızın 50.1 sürümü ile çalışmanızı [tamamlamanız](general-electronic-reporting.md#component-versioning) gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Fatura modeli**'ni genişletin ve **Fatura modeli (Litware)**'i seçin.
3. **Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.

Sürüm 50.1 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur. Yeni bir düzenlenebilir sürüm olan 50.2 eklendi ve **taslak** durumuna sahip. Bu sürümü, özel ER veri modeli yapılandırmanızda başka değişiklikler yapmak için kullanabilirsiniz.

![Yapılandırmalar sayfasında 50.1 sürümü tamamlandı.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Model eşleme yapılandırmasını özelleştirme

Elektronik raporlama geliştiricisi rolünde bir kullanıcı olarak, özel ER model eşlemenizi tasarlayabilirsiniz.

#### <a name="add-a-custom-model-mapping-configuration"></a>Özel bir model eşleme yapılandırması ekleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Müşteri Fatura modeli**'ni genişletin ve **Müşteri Fatura modeli eşleme**'yi seçin.
3. Eylem Panosundan **Yapılandırma oluştur**'u seçin.
4. Açılan iletişim kutusunda **Yeni** alanında, yeni özel ER model eşleme yapılandırmasının ER model eşleme yapılandırmasına dayalı olması gerektiğini belirtmek için **İsimden Türet: Müşteri faturası eşleme, Microsoft** seçeneğini belirleyin.
5. **Ad** alanına **Fatura modeli eşleme (Litware)** değerini girin.
6. **Hedef model** alanında, **Fatura modeli (litware)**'i seçin.

    > [!IMPORTANT]
    > Bu adım çok önemlidir. Bunu atlarsanız, özel veri modelinizi yapılandırılmış model eşlemesinde kullanamazsınız.

7. Yeni ER yapılandırmasını eklemek için **Yapılandırma oluştur**'u seçin.

![Yapılandırmalar sayfasında özel model eşleme yapılandırması ekleme.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Özel model eşlemesi yapılandırma

Özel model eşlemenizi değiştirmeniz ve özel veri modelinin özel **FederalTaxID\_Litware** alanının çalışma zamanında uygulama verileriyle nasıl doldurulması gerektiğini belirtmeniz gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Müşteri Fatura modeli** \> **Müşteri Fatura modeli eşleme**'yi genişletin ve **Fatura modeli eşleme (Litware)**'i seçin.
3. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
4. **Veri kaynağı eşleme modeli** sayfasında **Müşteri faturası** eşlemeyi seçin.

    ![Veri kaynağı modeli eşleme sayfası.](./media/er-quick-start3-select-customer-mapping.png)

5. **Tasarımcı**’yı seçin.
6. **Model eşleme Tasarımcısı** sayfasında, **veri kaynakları** bölmesinde, **CustInvoiceJour** uygulama tablosunu temsil eden **CustInvoiceJour** veri kaynağını genişletin.
7. **CustInvoiceJour** altında , **CustInvoiceJour** tablosu için çok-bir (N:1) tür ilişkilerin listesini incelemek için **ilişkileri** genişletin.
8. **CustInvoiceJour** \> **ilişkiler** altında **Müşteriler (CustTable)** tablosunun alanlarına ve ilişkilerine erişmek için **Müşterileri (CustTable)**'ı genişletin.
9. [Daha önce](#insert_custom_field) uygulamış olduğunuz **FederalTaxID\_Özel** veri kaynağı alanını seçin.
10. **Veri Modeli** bölmesinde, **Müşteri bilgisi (Müşteri)** öğesini genişletin ve **FederalTaxID\_Litware** veri modeli alanını seçin.
11. **Bağla**'yı seçin.

    ![Model eşleme tasarımcısı sayfası.](./media/er-quick-start3-customize-model-mapping.gif)

12. **Kaydet**'i seçin.
13. **Model eşleme tasarımcısı** sayfasını kapatın
14. **Veri kaynağı modeli eşleme** sayfasını kapatın.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Özel bir model eşleme yapılandırması tamamlama

Çalışmanızı kullanıma uygun hale getirmek için özel ER model eşleme yapılandırmanızın 50.19.1 sürümü ile [tamamlamanız](general-electronic-reporting.md#component-versioning) gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Müşteri Fatura modeli** \> **Müşteri Fatura modeli eşleme**'yi genişletin ve **Fatura modeli eşleme (Litware)**'i seçin.
3. **Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.

Sürüm 50.19.1 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur. Yeni bir düzenlenebilir sürüm olan 50.19.2 eklendi ve **taslak** durumuna sahip. Bu sürümü, özel ER model eşleme yapılandırmanızda başka değişiklikler yapmak için kullanabilirsiniz.

![Yapılandırmalar sayfasında 50.19.1 sürümü tamamlandı.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Desteklenen yapılandırma [yaşam döngüsü](general-electronic-reporting-manage-configuration-lifecycle.md) veritabanı değişikliklerinin kullanım ömrünü kapsamıyor. **Fatura modeli eşleme (Litware)** yapılandırmasının 50.19.1 sürümünü geçerli finans kurulumundan dışa aktarır ve özel **CustTable** tablosundaki özel **FederalTaxID\_Özel** alanını içermeyen başka bir kuruluma içe aktarmayı denerseniz özel bir durum oluşur. Özel durum içe aktarılan ER yapılandırmasının hedef finans kurulumunun meta verileri ile uyumlu olmadığını belirtir.

### <a name="customize-the-format-configuration"></a>Biçim yapılandırmasını özelleştirme

Elektronik raporlama işlevsel danışmanı rolünde bir kullanıcı olarak, özel ER biçiminizi tasarlayabilirsiniz.

#### <a name="add-a-custom-format-configuration"></a>Özel biçim yapılandırması ekleme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Müşteri Fatura modeli** \> **UBL Satış Faturası**'nı genişletin ve **Peppol Satış Faturası**'nı seçin.
3. Eylem Panosundan **Yapılandırma oluştur**'u seçin.
4. Açılan iletişim kutusunda **Yeni** alanında, özel ER biçim yapılandırmalarının ER biçim yapılandırmasına dayalı olması gerektiğini belirtmek için **İsimden Türet: Peppol Satış Faturası, Microsoft** seçeneğini belirleyin.
5. **Ad** alanına **Peppol Satış faturası (Litware)** değerini girin.
6. **Veri modeli** alanında, özel veri modelinizi ve model eşleştirme bileşenlerinizi kullanmak için **fatura modeli (Litware)**'i seçin.

    > [!NOTE]
    > Bu adım çok önemlidir. Bunu atlarsanız, özel veri modelinizi yapılandırılmış biçimde kullanamazsınız.

7. **Veri modeli** alanında, **InvoiceCustomer** kök tanımını seçin.
8. Yeni ER yapılandırmasını eklemek için **Yapılandırma oluştur**'u seçin.

![Yapılandırmalar sayfasında özel biçim yapılandırması ekleme.](./media/er-quick-start3-adding-custom-format.png)

**Taslak** [durumundaki](general-electronic-reporting.md#component-versioning) **Peppol Satış faturası (Litware)** ER yapılandırmasının 11.2.2.1. sürümünü düzenlemek için artık ER Operasyonları tasarımcısını kullanabilirsiniz.

![Yapılandırmalar sayfasındaki ER yapılandırmasının 11.2.2.1 sürümü.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Özel biçim yapılandırma

Faturalandırılmış bir müşterinin federal vergi kimlik kodu değerini doldurmak üzere yeni bir biçim öğesi ekleyerek özel biçiminizi değiştirmelisiniz.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Müşteri Fatura modeli** \> **UBL Satış Faturası** \> **Peppol Satış Faturası**'nı genişletin ve **Peppol Satış Faturası (Litware)**'i seçin.
3. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
4. Biçim ağacında, **xmlheader** \> **Fatura** \> **cac: accountingcustomerParty** \> **cac:Party** \> **cac:partytaxscheme** \> **cac:taxscheme** öğesini genişletin ve **cbc:ID**'yi seçin.
5. **Ekle**'yi seçin ve sonra **XML** \> **Öznitelik**'i seçin.
6. **Bileşen özelliği** iletişim kutusunda, **Ad** alanına **FederalTaxID**'yi girin.
7. Oluşturulan xml dosyasında yeni bir **federaltaxID** XML özniteliği oluşturmak için yeni bir biçim öğesi eklemek üzere **Tamam**'ı seçin.
8. Biçim ağacında, **xmlheader** \> **Fatura** \> **cac:accountingcustomerParty** \> **cac:Party** \> **cac:partytaxscheme** \> **cac:taxscheme** \> **cbc:ID** altında, **FederalTaxID**'yi seçin.
9. **Yukarı taşı**'yı seçin.

![Biçim tasarımcısı sayfasındaki yeni biçim öğesi.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Özel biçim eşlemesi yapılandırma

1. **Biçim tasarımcısı** sayfasında, **Eşleme** sekmesinde **Model** türünün **Fatura** veri kaynağını genişletin.
2. **Fatura** altında **Müşteri bilgisi (Müşteri)**'yi genişletin ve **FederalTaxID\_Litware**'i seçin.
3. **Bağla**'yı seçin.

    ![Biçim tasarımcısı sayfası.](./media/er-quick-start3-customized-format-mapping.png)

4. **Model** türünün **fatura** veri kaynağını seçin ve ardından **Düzenle**'yi seçin.
5. **Sürüm** alanında, özel veri modelinizin **1**. sürümünü seçin ve **Tamam**'ı seçin.
6. **Kaydet**'i seçin.
7. **Biçim tasarımcısı** sayfasını kapatın.

#### <a name="complete-a-custom-format-configuration"></a>Özel biçim yapılandırması tamamlama

Çalışmanızı kullanıma uygun hale getirmek için özel ER biçim yapılandırmanızın 11.2.2.1 sürümü ile [tamamlamanız](general-electronic-reporting.md#component-versioning) gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Müşteri Fatura modeli** \> **UBL Satış Faturası** \> **Peppol Satış Faturası**'nı genişletin ve **Peppol Satış Faturası (Litware)**'i seçin.
3. **Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.

Sürüm 11.2.2.1 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur. Yeni bir düzenlenebilir sürüm olan 11.2.2.2 eklendi ve **taslak** durumuna sahip. Bu sürümü, özel ER biçim yapılandırmanız üzerinde başka değişiklikler yapmak için kullanabilirsiniz.

![Yapılandırmalar sayfasında 11.2.2.1 sürümü tamamlandı.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Özel ER yapılandırmalarını kullanmaya başlamak için alacak hesapları parametrelerini yapılandırın

1. **Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin.
2. **Elektronik belgeler** sekmesinde, **Elektronik raporlama** hızlı sekmesinde, **Satışlar ve serbest metin faturası** alanında, **PEPPOL satış faturası (Litware)** seçeneğini belirleyin.
3. **Kaydet**'i seçin.

![Alacak hesapları parametreleri sayfası, elektronik belgeler sekmesi, elektronik raporlama hızlı sekmesi.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Federal vergi kimlik kodu ekleyerek müşteri kaydını güncelleştirme

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. **Tüm müşteriler** sayfasında, **DE-014** müşteri hesabı bağlantısını seçin.
3. **Genel** hızlı sekmesinde, **Federal Vergi Kimlik No** alanına, **LITWARE-6789** girin.
4. **Kaydet**'i seçin.

    ![DE-014 müşteri ayrıntıları sayfası.](./media/er-quick-start3-added-tax-id-value.png)

5. **Tüm müşteriler** sayfasını kapatın.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Özel ER yapılandırmalarını kullanarak bir müşteri faturası işleme

### <a name="select-and-send-a-posted-invoice"></a>Deftere nakledilmiş bir fatura seç ve gönder

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **Serbest metin faturası** sayfasında, önceden eklediğiniz ve deftere naklettiğiniz faturayı seçin.
3. Eylem bölmesinde, **Belge** grubunda **Gönder** \> **Orijinal**'i seçin.
4. **Serbest metin faturası** sayfasını kapatın.

### <a name="analyze-a-generated-e-invoice"></a>Oluşturulan e-faturayı analiz etme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama işleri**'ne gidin.
2. **Elektronik raporlama işleri** sayfasında, **E-fatura XML gönder** görev açıklamasına sahip son kaydı seçin.
3. Oluşturulan dosyalar listesine erişmek için **dosyaları göster**'i seçin.
4. Oluşturulan e-fatura XML dosyasını indirmek için **Aç**'ı seçin.
5. E-fatura XML dosyasını analiz edin. Özelleştirmenize uygun olarak, müşteri vergi şemasının özel **FederalTaxID** XML özniteliğinin yanı sıra **schemeID** ve **schemeAgencyID** XML özniteliklerini de içerdiğine dikkat edin. Bu yeni XML özniteliğinin değeri, Faturalanmış bir müşteri için girilen **LITWARE-6789** federal vergi kodu ile belirtilir.

    ![Özelleştirmelerinizle oluşturulan e-fatura XML dosyasının önizlemesi.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Standart ER yapılandırmalarının son sürümlerini içe aktarın

Finans kurulumundaki standart ER yapılandırmaları kümesini [güncel tutmak için](general-electronic-reporting-manage-configuration-lifecycle.md) bunların yeni sürümlerini o kurulum için yapılandırılmış ER [deposunda](general-electronic-reporting.md#Repository) kullanılabilir duruma geldiğinde içe aktarmanız gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma Sağlayıcıları** bölümünde **Microsoft** kutucuğunu seçin ve Microsoft sağlayıcısı için depolar listesini görüntülemek için **Depolar**'ı seçin.
3. **Yapılandırma depoları** sayfasında, **Global** türünün deposunu seçin ve sonra **Aç**'ı seçin. Regulatory Configuration Service bağlanmak için yetkilendirme istenirse, yetkilendirme yönergelerini uygulayın.
4. **Yapılandırma deposu** sayfasında, sol bölmedeki yapılandırma ağacında, **Peppol Satış Faturası** biçim yapılandırmasını seçin.
5. **Sürümler** hızlı sekmesinde, PEPPOL BIS 3 biçimindeki müşteri elektronik faturalarını desteklemek için sunulan seçili ER biçim yapılandırmasının **32.6.7** sürümünü seçin. Daha fazla bilgi için bkz. [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.

![Yapılandırma deposu sayfasında seçili sürüm 32.6.7.](./media/er-quick-start3-import-solution2.png)

Bu işlemin nasıl otomatikleştirilebileceği hakkında bilgi için, bkz. [ER yapılandırmalarının güncelleştirilmiş sürümlerini içe aktarma](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>İçe aktarılan ER yapılandırmalarını gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırma bileşenleri** hızlı sekmesini genişletin.
4. Sol bölmedeki yapılandırma ağacında, **Fatura modeli** öğesini genişletin. **Müşteri fatura modelinin** adının içe aktarılan ER veri modeli yapılandırmalarından birinde **fatura modeli** olarak değiştirilmiş olduğuna dikkat edin.
5. Sol bölmedeki yapılandırma ağacında, **Fatura modeli eşleme** öğesini genişletin. **Müşteri fatura modeli eşleme** adının içe aktarılan ER model eşleme yapılandırmalarından birinde **fatura modeli eşleme** olarak değiştirilmiş olduğuna dikkat edin.
6. **UBL satış faturası** \> **PEPPOL satış faturasını** genişletin.

Seçili **Peppol Satış Faturası** ER biçimine ek olarak, gerekli diğer ER yapılandırmalarının son sürümlerinin de içe aktarıldığına dikkat edin. İlgili çözümlerin yeni gereksinimlerle uyumlu kalması için ER yapılandırmalarının yeni sürümleri Global depoda ve LCS'de sürekli olarak yayımlandığından gerekli veri modeli yapılandırmasının son sürümleri ve model eşleme yapılandırmaları içe aktarılır.

Aşağıdaki ER yapılandırmaların sonunda yapılandırma ağacında kullanılabilir durumda olduğundan emin olun:

- **Fatura modeli** ER veri modeli yapılandırması:

    - Sürüm 206 (veya sonraki) Faturalama iş etki alanının veri yapısını temsil eden veri modeli ER bileşeninin 24. (veya sonraki) sürümünü içerir. Bu ER yapılandırması **Fatura modeli eşlemesi** ER model eşleme yapılandırmasının mevcut en son sürümünün bir üst öğesi olarak içe aktarılır.

    ![Yapılandırmalar sayfasında 206 sürümü.](./media/er-quick-start3-imported-solution2b1.png)

- **Fatura modeli eşleme** ER model eşleme yapılandırması:

    - 206.132 sürümü (veya sonraki), **Fatura modeli** ER veri modeli yapılandırmasının 206. sürümünün en son uygulaması olarak içe aktarıldı. Veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulduğunu açıklayan çeşitli model eşleme ER bileşenleri içerir.

    ![Yapılandırmalar sayfasında 206.132 sürümü.](./media/er-quick-start3-imported-solution2b2.png)

- **UBL Satış faturası** ER biçim yapılandırması:

    - Sürüm 32.6 biçimi ve biçim eşleme ER bileşenlerini içerir. Format bileşeni rapor düzenini belirtir. Biçim eşleme bileşeni model veri kaynağını içerir ve çalışma zamanında bu veri kaynağı kullanılarak rapor düzeninin nasıl doldurulacağını belirtir. Bu ER biçimi, UBL biçiminde e-faturalar oluşturmak üzere yapılandırılmıştır. İçe aktarma için seçilmiş olan **Peppol satış faturası** ER biçiminin bir üst öğesi olarak içe aktarılır.

- **Peppol Satış faturası** ER biçim yapılandırması:

    - 32.6.7 sürümü, PEPPOL biçiminde e-faturalar oluşturmak üzere yapılandırılmış biçim ve biçim eşleme ER bileşenlerini içerir.

    ![Yapılandırmalar sayfasında 32.6.7 sürümü.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Değişiklikleri özel ER yapılandırmalarınızın içindeki yeni standart ER yapılandırmalarına uygulayın

### <a name="adopt-your-custom-er-data-model"></a>Özel ER veri modelinizi benimseme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Fatura modeli**'ni genişletin ve **Fatura modeli (Litware)**'i seçin.
3. **Sürümler** hızlı sekmesinde seçili veri modeli yapılandırmasının **50.2** taslak sürümü için **Yeniden temellendir**'i seçin.
4. **Hedef sürüm** alanında, temel ER veri modeli yapılandırmasının **206** sürümü seçimini onaylayın ve **Tamam**'ı seçin.

    Özel ER veri modeli yapılandırmanızın taslak sürümü **50.2**'den **206.2** şeklinde yeniden numaralandırılarak artık temel ER veri modeli yapılandırmasının en son sürümündeki (206) değişikliklerle birleştirilen özelleştirmenizi içerdiğini gösterir.

    > [!NOTE]
    > Yeniden temellendirme eylemi geri alınamaz. Bu yeniden temellendirmeyi iptal etmek için, **sürümler** hızlı sekmesinde **Fatura modeli (Litware)** modelinin sürüm **50.1** öğesini seçin ve sonra **Bu sürümü Al**'ı seçin. 206.2 sürüm daha sonra **50.2** olarak yeniden numaralandırılır ve taslak sürümü 50.2 içeriği sürüm 50.1 içeriğiyle eşleşir.

5. **Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.

Sürüm 206.2 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur. Yeni bir düzenlenebilir sürüm olan 206.3 eklendi ve **taslak** durumuna sahip. Bu sürümü, özel ER veri modeli yapılandırmanızda başka değişiklikler yapmak için kullanabilirsiniz.

![Yapılandırmalar sayfasında 206.2 sürümü tamamlandı.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Özel ER model eşlemenizi benimseme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Fatura modeli** \> **Fatura modeli eşleme**'yi genişletin ve **Fatura modeli eşleme (Litware)**'i seçin.
3. **Sürümler** hızlı sekmesinde seçili model eşleme yapılandırmasının **50.19.2** taslak sürümü için **Yeniden temellendir**'i seçin.
4. **Hedef sürüm** alanında, temel ER model eşleme yapılandırmasının **206.132** sürümü seçimini onaylayın ve **Tamam**'ı seçin.

    Özel ER model eşleme yapılandırmanızın taslak sürümü **50.19.2**'den **206.132.2** şeklinde yeniden numaralandırılarak artık temel ER model eşleme yapılandırmasının en son sürümündeki (206.132) değişikliklerle birleştirilen özelleştirmenizi içerdiğini gösterir.

    Bazı yeniden temellendirme çakışmaların keşfedildiğine dikkat edin. Bu çakışmaları şimdi el ile çözmeniz gerekir.

    ![Yapılandırmalar sayfasında yeniden temellendirme çakışma iletisi.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Eylem bölmesinde **Tasarımcı**'yı seçin ve sonra eşleme listesinde **Müşteri faturası** seçeneğini belirleyin.
6. Her yeniden temellendirme çakışması için, **kendi değerini koru** seçeneğini belirleyin çünkü belirtilen her bileşen için özel veri modelinizin sürüm numarasını saklamanız gerekir.

    ![Model eşleme tasarımcı sayfasında yeniden temellendirme çakışmaları.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. **Kaydet**'i seçin ve ardından **Model eşleme tasarımcısı** sayfasını kapatın.
8. Eşleme listesinde, **proje faturası**'nı seçin.
9. Her yeniden temellendirme çakışması için, **kendi değerini koru** seçeneğini belirleyin çünkü belirtilen her bileşen için özel veri modelinizin sürüm numarasını saklamanız gerekir.
10. **Kaydet**'i seçin ve ardından **Model eşleme** sayfasını kapatın.

    > [!NOTE]
    > Yeniden temellendirme eylemi geri alınamaz. Bu yeniden temellendirmeyi iptal etmek için, **sürümler** hızlı sekmesinde **Fatura modeli eşleme (Litware)** model eşlemesinin sürüm **50.19.1** öğesini seçin ve sonra **Bu sürümü Al**'ı seçin. 206.132.2 sürüm daha sonra **50.19.2** olarak yeniden numaralandırılır ve taslak sürümü 50.19.2 içeriği sürüm 50.19.1 içeriğiyle eşleşir.

11. **Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.

Sürüm 206.132.2 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur. Yeni bir düzenlenebilir sürüm olan 206.132.3 eklendi ve **taslak** durumuna sahip. Bu sürümü, özel ER model eşleme yapılandırmanızda başka değişiklikler yapmak için kullanabilirsiniz.

![Yapılandırmalar sayfasında 206.132.2 sürümü tamamlandı.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Özel ER biçiminizi benimseme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında sol bölmedeki yapılandırma ağacında, **Fatura modeli** \> **UBL Satış Faturası** \> **Peppol Satış Faturası**'nı genişletin ve **Peppol Satış Faturası (Litware)**'i seçin.
3. **Sürümler** hızlı sekmesinde seçili biçim yapılandırmasının **11.2.2.2** taslak sürümü için **Yeniden temellendir**'i seçin.
4. **Hedef** sürüm alanında, temel ER biçim yapılandırmasının **32.6.7** sürümü seçimini onaylayın ve **Tamam**'ı seçin.

    Özel ER biçim yapılandırmanızın taslak sürümü **11.2.2.2**'den **32.6.7.2** şeklinde yeniden numaralandırılarak artık temel ER biçim yapılandırmasının en son sürümündeki (32.6.7) değişikliklerle birleştirilen özelleştirmenizi içerdiğini gösterir.

    Bazı yeniden temellendirme çakışmaların keşfedildiğine dikkat edin. Bu çakışmaları şimdi el ile çözmeniz gerekir.

5. Eylem Bölmesinde, **Tasarımcı**'yı seçin.
6. Her yeniden temellendirme çakışması için, **kendi değerini koru** seçeneğini belirleyin çünkü belirtilen her bileşen için özel veri modelinizin sürüm numarasını saklamanız gerekir.
7. **Kaydet**'i seçin.
8. **Eşleme** sekmesinde **Model** türünün **fatura** veri kaynağını seçin ve ardından **Düzenle**'yi seçin.
9. **Sürüm** alanında, özel veri modelinizin **2**. sürümünü seçin ve **Tamam**'ı seçin.
10. **Kaydet**'i seçin.

    > [!NOTE]
    > Yeniden temellendirme eylemi geri alınamaz. Bu yeniden temellendirmeyi iptal etmek için, **sürümler** hızlı sekmesinde **Peppol Satış Faturası (Litware)** biçiminin sürüm **11.2.2.1** öğesini seçin ve sonra **Bu sürümü Al**'ı seçin. 32.6.7.2 sürüm daha sonra **11.2.2.2** olarak yeniden numaralandırılır ve taslak sürümü 11.2.2.2 içeriği sürüm 11.2.2.1 içeriğiyle eşleşir.

11. **Biçim tasarımcısı** sayfasını kapatın.
12. **Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.

Sürüm 32.6.7.2 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur. Yeni bir düzenlenebilir sürüm olan 32.6.7.3 eklendi ve **taslak** durumuna sahip. Bu sürümü, özel ER biçim yapılandırmanız üzerinde başka değişiklikler yapmak için kullanabilirsiniz.

![Yapılandırmalar sayfasında 32.6.7.2 sürümü tamamlandı.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Özel ER yapılandırmalarının yeni sürümlerini kullanarak bir müşteri faturası işleme

### <a name="select-and-send-a-posted-invoice"></a>Deftere nakledilmiş bir fatura seç ve gönder

1. **Alacak hesapları** \> **Faturalar** \> **Tüm serbest metin faturaları**'na gidin.
2. **Serbest metin faturası** sayfasında, önceden eklediğiniz ve deftere naklettiğiniz faturayı seçin.
3. Eylem bölmesinde, **Belge** grubunda **Gönder** \> **Orijinal**'i seçin.

    > [!NOTE] 
    > Artık **PEPPOL Satış Faturası (Litware)** ER biçim yapılandırmasının iki sürümüne sahip olduğunuzdan ve her iki sürüm de [geçerlilik tarihi](general-electronic-reporting.md#component-date-effectivity) değeri içermediğinden bir e-fatura oluşturmak için en son sürüm kullanılır.

4. **Serbest metin faturası** sayfasını kapatın.

### <a name="analyze-a-generated-e-invoice"></a>Oluşturulan e-faturayı analiz etme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama işleri**'ne gidin.
2. **Elektronik raporlama işleri** sayfasında, **E-fatura XML gönder** görev açıklamasına sahip en son kaydı seçin.
3. Oluşturulan dosyalar listesine erişmek için **dosyaları göster**'i seçin.
4. Oluşturulan e-fatura XML dosyasını indirmek için **Aç**'ı seçin.
5. E-fatura XML dosyasını analiz edin. Özelleştirmenize uygun olarak, müşteri vergi şemasının hâlâ özel **FederalTaxID** XML özniteliğinin yanı sıra **schemeID** ve **schemeAgencyID** XML özniteliklerini de içerdiğine dikkat edin. Ek olarak, temel **UBL Satış faturası** biçiminin yeni sürümündeki değişiklikler özelleştirmeyle birleştirildiğinden, **CBC: CustomizationId** XML öğesinin metni `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` iken `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0` olarak değiştirildi.

    ![Özelleştirmelerle oluşturulan e-fatura XML dosyasının önizlemesi.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Lifecycle Services'dan ER yapılandırma indirme](download-electronic-reporting-configuration-lcs.md)
- [Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir](er-download-configurations-global-repo.md)
- [Serbest metin faturası oluşturma](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Özel alanlar oluşturma ve bunlarla çalışma](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
