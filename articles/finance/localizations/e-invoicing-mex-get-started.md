---
title: Meksika için Elektronik faturalamayı kullanmaya başlama
description: Bu konu, Meksika için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1112ba8394afb3aa9c9b4f68249524498bd8b32
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894895"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a>Meksika için Elektronik faturalamayı kullanmaya başlama

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Meksika için elektronik faturalama şu anda Comprobante Fiscal Digital por Internet (CFDI) belgesindeki kullanılabilir ve Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management üzerinde oluşturulan ilgili tümleştirmelerde tüm işlevleri desteklemeyebilir.

Bu konu, Meksika için Elektronik faturalamayı kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Regulatory Configuration Services (RCS) ve Finance için ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder. Ayrıca, servis üzerinden CFDI faturalarını göndermek için Finance'de izlemeniz gereken adımlarda size yol gösterir ve işlem sonuçlarının nasıl gözden geçirileceğini ve CFDI faturalarının durumunu açıklamaktadır.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki adımları gerçekleştirmeden önce, [elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md) adımlarını tamamlamanız gerekir.

## <a name="rcs-setup"></a>RCS kurulumu

RCS kurulumu sırasında şu görevleri tamamlayacaksınız:

1. CFDI faturalarını işlemek için e-faturalama özelliğini içe aktarın.
2. CFDI faturaları hakkında yanıtlar oluşturmak, göndermek ve almak, iptal hakkındaki yanıtları göndermek ve almak için gereken biçim yapılandırmalarını gözden geçirin.
3. CFDI fatura gönderme senaryolarını destekleyen olayları yapılandırın.
4. CFDI faturalarını işlemek için e-faturalama özelliğini yayınlayın.

> [!NOTE]
> "E-faturala özelliği", Elektronik faturalama sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır. Bu durumda, CFDI faturaları (MX), ayarlayacağınız e-faturalama özelliğidir.

## <a name="import-the-e-invoicing-feature"></a>E-faturalama özelliğini içe aktarma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özellikleri** çalışma alanında **Özellikler** bölmesinde **E-faturalama** kutucuğunu seçin.
3. **E-faturalama özellikleri** sayfasında, Genel depodan **CFDI faturaları (MX)** özelliğini içe aktarmak için **İçe aktar**'ı seçin.

    > [!NOTE]
    > Listede özelliği göremiyorsanız, **Eşitle**'yi seçin ve 3. adımı tekrarlayın.

![CFDI faturaları (MX) özelliğini içe aktarma](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

**CFDI faturaları (MX)** özelliğini Global depodan içe aktardığınızda, yapılandırmalar ve eylemlerle birlikte tüm özellik ayarları da içe aktarılır.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>CFDI faturaları (MX) özelliğinin yeni bir sürümünü oluşturma

Örneğin, URL'lerin güncelleştirilmesi gerekiyorsa, yeni bir sürüm oluşturabilirsiniz. Daha fazla bilgi için, bkz. [E-faturalama CFDI](tasks/mx-00010-e-invoicing-cfdi.md).

- **E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Yeni** ögesini seçin.

![Yeni e-faturalama özellik sürümü ekleme](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Yapılandırma sürümünü güncelleştirme

1. **E-faturalama özellikleri** sayfasında, **Yapılandırmalar** sekmesinde, yapılandırma sürümlerini (ER dosya biçimi yapılandırmaları) yönetmek için **Ekle** veya **Sil**'i seçin.

    ![E-faturalama özellik yapılandırmalarını yönetme](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Yeni bir sürüm oluşturduğunuzda, tüm yapılandırmalar en son yayınlanan sürümden devralınır. CFDI faturalarını işlemek için aşağıdaki yapılandırmalar gereklidir:

    - CFDI faturası (BusinessDocumentService)
    - CFDI yanıt iletisi alma
    - CFDI hata günlüğü alma
    - CFDI iptal isteği (MX) (BusinessDocumentService)
    - CFDI faturası (BusinessDocumentService)

2. Listede bir yapılandırma sürümü seçin ve sonra da yapılandırmayı düzenleyebileceğiniz veya görüntüleyebileceğiniz **Biçim tasarımcısı** sayfasını açmak için **Düzenle** veya **Görüntüle**'yi seçin.

    ![Biçim tasarımcısı sayfasını açma](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. **Biçim tasarımcısı** sayfasını, ER biçimi dosya yapılandırmalarını düzenlemek ve görüntülemek için kullanın. Daha fazla bilgi için bkz. [Elektronik belge yapılandırmalarını oluşturma](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Biçim tasarımcısı sayfası](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>E-faturalama özellik kurulumlarını yönetme

- **E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, E-faturalama özellik kurulumlarını yönetmek için **Ekle**, **Sil** veya **Düzenle** ögesini seçin.

![E-faturalama özellik kurulumlarını yönetme](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Onaya CFDI faturalarını göndermek için (XML dosyasını oluşturun, XML dosyasını gönderin ve yanıtı işleyin), **Satış faturası** özellik kurulumu gereklidir.

CFDI fatura iptali göndermek için **İptal etme** ve **İptal etme** özelliği kurulumları gereklidir.

### <a name="configure-the-sales-invoice-feature-setup"></a>Satış faturası özellik kurulumunu yapılandırma

1. **E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **Satış faturası**'nı seçin.
2. Eylemleri, uygulanabilirlik kurallarını ve değişkenleri yapılandırmak için **Düzenle** ögesini seçin.

    ![E-faturalama özellik kurulumunu düzenleme](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. **Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin. Eylemler, olayın tam olarak yürütülmesi için sırayla çalıştırılması gereken işlemlerin listesini tanımlar.

    ![Eylemler sekmesi](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Eylem kodu | Eylem                   | Eylem adı                                  | Eylem açıklaması                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Belgeyi dönüştür       | Dijital işareti olmadan CFDI E-fatura oluşturma | CFDI e-fatura oluşturun.                                |
    | 2         | Belgeyi imzala            | Dijital imza                                 | E-faturayı gönderim için dijital olarak imzalayın.                |
    | 3         | Meksika PAC hizmetini çağır | CFDI e-fatura gönder                        | Windows Communication Foundation (WCF) istemcisi, CFDI e-faturasını gönderir. |
    | 4         | Yanıtı işle         | Web servis yanıtını çözümle                 | Web hizmeti yanıtını çözümleyin ve hata günlüğünü döndürür. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Meksika PAC Web Hizmetleri için URL'yi ayarlama 

1. **Özellik sürümü kurulumu** sayfasında, **Eylemler** sekmesindeki **Eylemler** hızlı sekmesinde, **Meksika PAC Servisi çağır** seçeneğini belirleyin.
2. **Parametreler** hızlı sekmesinde, **URL adresi** alanına, CFDI fatura gönderimi için Web hizmetinin URL'sini girin.

> [!NOTE]
> **İptal** ve **İptal isteği** özelliği kurulumları için **Meksika PAC servisini çağır** eylemi URL'sini güncelleştirmek üzere aynı adımları kullanın.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Taslak sürümünü bir E-faturalama ortamına atama

1. **E-faturalama özellikleri** sayfasında, **Ortamlar** sekmesinde, **Etkinleştir** ögesini seçin.
2. **Ortamlar** alanında, ortamı seçin.
3. **Geçerlilik başlangıcı** alanında, yeni ortamın geçerli olacağı tarihi seçin.
3. **Etkinleştir**'i seçin.

![E-faturalama ortamını etkinleştirme](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Sürüm durumunu Tamamlandı olarak değiştirme

1. **E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Taslak** durumundaki e-faturalama özelliğinin sürümünü seçin.
2. **Durumu değiştir \> Tamamla**'yı seçin.

## <a name="change-the-version-status-to-published"></a>Sürüm durumunu Yayımlandı olarak değiştirme

- **E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Durumu değiştir \> Yayımla** ögesini seçin.

## <a name="publish-the-e-invoicing-feature"></a>E-faturalama özelliğini yayımlama

1. **E-faturalama özellikleri** sayfasında, **CFDI faturaları (MX)** özelliğinin durumunu yönetmek için **Sürümler** sekmesini seçin.
2. Özelliğin durumunu değiştirmek için **Durumu değiştir**'i seçin.

![E-faturalama özelliğinin durumunu değiştirme](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a>Finance'de Elektronik faturalama tümleştirmesi kurulumu

Finance içindeki Elektronik faturalamayı ayarlamak için şu görevleri tamamlayacaksınız:

1. ER veri modelini, ER veri modeli eşleştirmesini ve CFDI faturaları için gereken biçimleri içe aktarın.
2. CFDI faturalarını güncelleştirmek için yanıt tiplerini yapılandırın. Bu yanıt türleri yetkili sertifika sağlayıcı (PAC) sunucusundan yanıt olarak kullanılır.

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>ER veri modelini, ER veri modeli eşleştirmesini ve CFDI faturaları için bağlam yapılandırmalarını içe aktarın

1. Finance'de oturum açın.
2. **Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** başlığını seçin. Bu yapılandırma sağlayıcısının **Etkin** olarak ayarlandığından emin olun. Sağlayıcının **Etkin** olarak nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve etkin olarak işaretleme](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. **Depolar**'ı seçin.
4. **Genel kaynak \> Aç**'ı seçin.
5. **Fatura modeli**, **Fatura modeli eşlemesi**, **CFDI fatura biçimi (MX)**, **CFDI fatura iptal isteği biçimi (MX)** ve **CFDI fatura iptali biçimi (MX)** ögelerini ni içe aktarın.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>CFDI faturalarını işlemek için özelliği açma

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Özellikler** sekmesinde, **MX-00010** ve **MX-00016** özellik referansları için satırlarda **Etkinleştir** onay kutusunu seçin.

![CFDI faturalarını işlemek için özellikleri açma](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>ER yapılandırmalarını içe aktarma ve CFDI faturalarını güncelleştirmek için yanıt tiplerini ayarlama

#### <a name="import-er-configurations"></a>ER yapılandırmaları içe aktarın

1. **Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft** başlığını seçin.
3. **Depolar**'ı seçin.
4. **Genel kaynak \> Aç**'ı seçin.
5. **Yanıt iletisi modeli**, **CFDI hata günlüğü alma (MX)** ve **CFDI yanıt iletisi içeri aktarma (MX)** ögelerini içeri aktarın.

#### <a name="set-up-the-response-types"></a>Yanıt türlerini ayarlama

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Elektronik belge** sekmesinde **Ekle**'yi seçin.
3. Müşteri fatura günlüğünü girin ve sonra **Tablo adı** alanında proje faturasını seçin.
4. Her tablo için, ilgili belge bağlamını tanımlayın:

    - **Müşteri fatura günlüğü** için **Müşteri fatura bağlamı**'nı girin.
    - **Proje faturası** için **Proje fatura bağlamı**'nı girin.

4. Elektronik faturalamadan döndürülecek ve bir müşteri fatura günlüğünde veya proje faturasına dahil edilen yanıt türlerini yapılandırmak için **Yanıt türleri**'ni seçin.
5. **Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **Yanıt**'ı seçin.
6. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
7. **Model eşleme** alanında, **Yanıt iletisi içe aktarma biçimi - Yanıt iletisinden model eşlemesi** ögesini seçin.
8. **Kaydet**'i seçin.
9. **Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **ResponseData** ögesini seçin.
10. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
11. **Model eşleme** alanında, **CFDI yanıtı veri içe aktarma biçimi (ayrıntılar) – Yanıt verilerini içe aktarma** ögesini seçin.
12. **Kaydet**'i seçin.

## <a name="process-electronic-invoices-in-finance"></a>Finance içindeki elektronik faturaları işleme 

Elektronik faturalama ile Finance içindeki CFDI faturalarının işlenmesi sırasında aşağıdaki görevleri gerçekleştirebilirsiniz:

- CFDI faturalarını gönderin.
- Gönderme yürütme günlüklerine bakın.
- Bir CFDI faturasının iptalini gönderin.

### <a name="submit-cfdi-invoices"></a>CFDI faturalarını gönderme

**Yapılandırılabilir Elektronik faturalama tümleştirmesi** özelliğini açtıktan sonra, **CFDI faturalarını göndermek için Elektronik faturayı dışa/içe aktar** işlemi (**Alacak hesapları \> Fatura \> E-faturalar**) artık kullanılamaz. **Elektronik belge gönderme** adı verilen yeni bir işlemle değiştirilir.

> [!NOTE]
> Yeni **Elektronik belge gönder** işlemini kullanmadan önce, Meksika e-faturaları için gerekli olan kurulumun tamamlandığını doğrulayın. Daha fazla bilgi için bkz. [CFDI düzen sürümü 3.3](./latam-mex-cfdi-3-3.md).

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönder** sayfasına gidin.
2. Herhangi bir belgenin ilk gönderimi için, **Belgeyi yeniden gönder** seçeneğini her zaman **Hayır** olarak ayarlayın. Belgeyi servis aracılığıyla yeniden göndermeniz gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın.
3. **Dahil edilecek kayıtlar** hızlı sekmesinde, gönderilecek belgeleri seçmek üzere bir sorgu oluşturabileceğiniz **Sorgulama** iletişim kutusunu açmak için **Filtre**'yi seçin.

![Bir CFDI belgesi gönderme](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Servis aracılığıyla ilk belgeyi gönderme denemeniz sırasında, Elektronik faturalama ile bağlantıyı onaylamanız istenecektir. **Elektronik Belge Gönderme Hizmetine bağlanmak için burayı tıklayın** ögesini seçin.

### <a name="view-submission-logs"></a>Gönderme günlüklerini görüntüleme

Gönderme günlüklerini gönderilen tüm belgelerin veya yalnızca gönderilen bir belge için görüntüleyebilirsiniz.

#### <a name="view-all-submission-logs"></a>Bütün gönderme günlüklerini görüntüleme

**Yapılandırılabilir Elektronik faturalama tümleştirmesi** özelliğini açtıktan sonra, belge gönderme işlemini takip etmenizi sağlayan yeni bir sayfa kullanılabilir. Gönderilen tüm belgelerin gönderme günlüklerini görüntülemek için bu sayfayı kullanabilirsiniz.

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
2. **Belge türü** alanında, gerekli elektronik belgelerle ilgili olarak filtre uygulamak için **Müşteri fatura günlüğü** seçeneğini belirleyin.

    ![Gönderme günlüklerinin görüntülemek üzere bir belge türü seçme](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.

    ![Gönderme günlüğü ayrıntılarını görüntüleme](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Gönderme günlüklerindeki bilgiler üç hızlı sekme arasında bölünür:

- **İşleme eylemleri**: Bu hızlı sekmede, RCS'de ayarlanan özellik sürümünde yapılandırılan eylemler için yürütme günlükleri gösterilmektedir. **Durum** sütunu eylemin başarıyla çalıştırılıp çalıştırılmadığını gösterir.
- **Eylem dosyaları**: Bu hızlı sekme, eylemlerin yürütülmesi sırasında oluşturulan ara dosyaları gösterir. Dosyayı indirmek ve görüntülemek için **Görünüm** öğesini seçebilirsiniz.
- **İşleme eylem günlüğü**: Bu hızlı sekmede, elektronik faturalama ve hedef Web servisi arasındaki iletişimin sonuçları gösterilir. Ayrıca Web servis işlemi tarafından döndürülen sonuçları da gösterir. **Hata kodu** sütunu, yetkilendirme Web hizmeti tarafından döndürülen dönüş kodunu gösterir.

Gönderilen CFDI faturası yetkilendirilirse, durumu **Onaylandı** olarak güncelleştirilir.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>CFDI faturalarından gönderme günlüklerini görüntüleme

**Yapılandırılabilir Elektronik faturalandırma tümleştirme** özelliğini açtıktan sonra, tüm CFDI faturalarından gönderme günlüklerini de görüntüleyebilirsiniz.

1. **Alacak hesapları \> Sorgulamalar ve raporlar \> CFDI (elektronik faturalar)** seçeneğine gidin.
2. **Yapılandırılabilir Elektronik faturalama tümleştirme** özelliği etkinleştirildikten sonra gönderilen bir CFDI faturası seçin.
3. Eylem Bölmesi'ndeki **Geçmiş** sekmesinde, **Elektronik belge günlüğü**'nü seçin.

![CFDI faturalarından gönderme günlüklerini görüntüleme](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> **Yapılandırılabilir Elektronik faturalama tümleştirme** özelliği açılmadan önce gönderilen CFDI faturaları için **Geçmiş** düğmesi kullanılabilir. **Yapılandırılabilir Elektronik faturalama tümleştirme** özelliği açıldıktan sonra gönderilen CFDI faturaları için **Geçmiş** düğmesi kullanılamaz.

### <a name="submit-cancellation-of-cfdi-invoices"></a>CFDI faturalarına ait iptal gönderme

**Yapılandırılabilir Elektronik faturalama tümleştirmesi** özelliği etkinleştirildikten sonra, CFDI faturalarını iptal etmek için kullanılan eski işlem artık kullanılamaz. **Elektronik belge gönderme günlüğü** sayfasına katıştırılmış yeni bir iptal işlemi ile değiştirilir.

1. **Alacak hesapları \> Sorgulamalar ve raporlar \> CFDI (elektronik faturalar)** seçeneğine gidin.
2. CFDI faturası **Onaylandı** durumundaysa, **İşlevler \> CFDI'yi iptal et** ögesini seçin.
3. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
4. CFDI faturasını seçin ve sonra **İşlevler \> İlgili gönderimleri gönder**'i seçin.
5. İlgili gönderim için bir açıklama girin ve **Tamam**'ı seçin.

#### <a name="view-cancellation-submission-logs"></a>İptal gönderim günlüklerini görüntüleme

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
2. **Belge türü** alanında, yalnızca müşteri faturası günlüğü ile ilgili olarak filtre uygulamak için **Müşteri fatura günlüğü** seçeneğini belirleyin.
3. CFDI faturasını seçin ve sonra Eylem Bölmesi'nde, **Sorgulamalar \> İlgili gönderim**'i seçin.

    **İlgili gönderimler** sayfası, belirli bir CFDI faturası için tüm ilgili gönderimleri ve bunların gönderim durumlarını gösterir. Aşağıdaki çizimde, ilk satır, CFDI faturasının onayını talep eden gönderimi temsil eder. İkinci satır, bu CFDI faturasını iptal eden gönderimi temsil eder.

    ![İptal gönderim günlüklerini görüntüleme](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.

    ![İptal gönderim günlüğü detaylarını görüntüleme](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Gizlilik bildirimi
**CFDI Meksika elektronik fatura (MX)** özelliğinin etkinleştirilmesi kuruluş vergi kayıt kodunu içeren sınırlı verilerin gönderilmesini gerektirebilir. Bu, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bir yönetici, **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** sayfasına giderek **CFDI Meksika elektronik fatura (MX)** özelliğini etkinleştirebilir ve devre dışı bırakabilir. **Özellikler** sekmesini seçin, **CFDI Meksika elektronik fatura (MX)** özelliğini içeren satırları seçin ve sonra uygun seçimi yapın. Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.

## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalamaya genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalamayı kullanmaya başlama](e-invoicing-get-started.md)
- [Elektronik faturalamayı ayarlama](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]