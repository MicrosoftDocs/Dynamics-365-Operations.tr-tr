---
title: Brezilya için Elektronik faturalama eklentisini kullanmaya başlangıç
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile Brezilya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 0320bd1d9e93cc30ed75f28e387ac2ec8dbfc226
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4962847"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Brezilya için Elektronik faturalama eklentisini kullanmaya başlangıç 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Brezilya için elektronik faturalama eklentisi, şu anda Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management üzerinde oluşturulan mali belge tümleştirmelerinde kullanılabilen tüm işlevleri desteklemez.

Bu konu, Brezilya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Regulatory Configuration Services'te (RCS) ülkeye bağlı olan yapılandırma adımlarında Finance ve Supply Chain Management uygulamalarında size kılavuzluk eder. Ayrıca servis üzerinden bir NF-e mali belgesi (Elektronik mali belge modeli 55) gönderme sürecinde size yol gösterir ve işleme sonuçlarının ve mali belgelerin durumunun nasıl gözden geçirdiğinin açıklar.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki adımları gerçekleştirmeden önce, [elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) adımlarını tamamlamanız gerekir.

## <a name="rcs-setup"></a>RCS kurulumu

RCS kurulumu sırasında şu görevleri tamamlayacaksınız:

1. NF-e mali belgeleri için E-faturalama özelliğini içe aktarın.
2. Onaya NF-e mali belgelerini göndermek için gerekli dosya biçimlerini gözden geçirin.
3. Onaylı bir NF-e iptalini istemek için gereken dosya biçimlerini gözden geçirin.
4. Onaya NF-e mali belgelerini göndermek için gerekli olayı yapılandırın.
5. Onaylı bir NF-e iptalini istemek için gereken olayı yapılandırın.
6. E-faturalama özelliğini elektronik faturalama eklenti ortamına atayın.
7. E-faturalama özelliğini yayımlayın.

> [!NOTE]
> "E-faturala özelliği", Elektronik faturalama eklenti sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır. E-fatura özellik kurulumu, başka şeylerin yanı sıra, yapılandırılabilir dışarı aktarma ve içe aktarma dosyaları oluşturmak için Elektronik Raporlama (ER) yapılandırma biçimlerinin kullanılması ve isteklerin gönderilmesi, yanıtları içe aktarmaya ve yanıt içeriğini ayrıştırmaya olanak tanıyan eylemleri ve eylem akışlarının kullanımını birleştirir.

## <a name="import-the-e-invoicing-feature"></a>E-faturalama özelliğini içe aktarma

1. RCS hesabınızda oturum açma
2. **Genelleştirme özellikleri** çalışma alanında **Özellikler** bölmesinde **E-faturalama** kutucuğunu seçin.
3. **E-faturalama Özellikleri** sayfasında, Genel depodan NF-e mali belge E-faturalama özelliğini içe aktarmak için **İçe aktar**'ı seçin.

    ![İçe aktarma düğmesi](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. NF-e mali belge özelliğini seçin ve **İçe aktar**'ı seçin.

    ![NF-e özelliğini içe aktarma](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>NF-e mali belgeler özelliğinin yeni bir sürümünü oluşturma

- **E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Yeni** ögesini seçin.

![Yeni e-faturalama özellik sürümü ekleme](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Yapılandırma sürümünü güncelleştirme

1. **E-faturalama özellikleri** sayfasında, **Yapılandırmalar** sekmesinde, yapılandırma sürümlerini (ER dosya biçimi yapılandırmaları) yönetmek için **Ekle** veya **Sil**'i seçin.

    ![E-faturalama özellik yapılandırmalarını yönetme](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - NF-e mali belge özelliğinin yeni sürümünü oluşturduğunuzda, tüm yapılandırma sürümleri (ER dosya biçimleri) en son sürümden devralınır.
    - Onaya NF-e mali belgesini göndermek üzere aşağıdaki yapılandırma sürümleri gereklidir:

        - NFe gönderim dışa aktarma biçimi
        - NFe yanıt iletisi alma
        - NFe hata günlüğü alma

    - NF-e iptalini göndermek için aşağıdaki yapılandırma sürümü gereklidir:

        - NFe iptal dışa aktarma biçimi

2. Listede bir yapılandırma sürümü seçin ve sonra da yapılandırmayı düzenleyebileceğiniz veya görüntüleyebileceğiniz **Biçim tasarımcısı** sayfasını açmak için **Düzenle** veya **Görüntüle**'yi seçin.

    ![Biçim tasarımcısı sayfasını açma](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. **Biçim tasarımcısı** sayfasını, ER biçimi dosya yapılandırmalarını düzenlemek veya görüntülemek için kullanın. Daha fazla bilgi için bkz. [Elektronik belge yapılandırmalarını oluşturma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Biçim tasarımcısı sayfası](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>E-faturalama özellik kurulumlarını yönetme

- **E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, E-faturalama özellik kurulumlarını (yani NF-e etkinlikleri) yönetmek için **Ekle** veya **Sil** ögesini seçin.

![E-faturalama özellik kurulumlarını yönetme](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Başka bir e-faturalama özelliğinden türetilen NF-e mali belge özelliğinin yeni bir sürümünü oluşturduğunuzda, tüm özellik kurulumları (NF-e olayları) en son sürümden devralınır.

Onaya NF-e mali belgelerini göndermek için **Gönder** özellik kurulumu gereklidir.

NF-e iptali göndermek için **İptal** özelliği kurulumu gereklidir.

#### <a name="configure-the-submit-feature-setup"></a>Gönderme özelliği kurulumunu yapılandırma

1. **E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **Gönder**'i seçin.
2. **Düzenle** öğesini seçin.

    ![E-faturalama özellik kurulumunu düzenleme](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. **Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin.

    ![Eylemler sekmesi](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Onaya NF-e göndermek için gerekli eylemleri gözden geçirin.

    | Eylem kodu | Eylem adı                  | Eylem açıklaması                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Belgeyi dönüştür           | Gönderme için NF-e XML dosyasını oluşturun.                          |
    | 2         | Belgeyi imzala                | XML dosyasına dijital sertifika uygulayın.                    |
    | 3         | Brezilya SEFAZ hizmetini çağır | İmzalı XML dosyasını yetkilendirme için Web hizmetlerine gönderin. |
    | 4         | Yanıtı işle             | Web servis yanıtını alın.                                     |
    | 5         | Belgeyi dönüştür           | Yanıt olarak alınan dosyanın içeriğini ayrıştırın.     |
    | 6         | Belgeyi dönüştür           | Gönderimin durumunu sorgulamak için XML dosyasını oluşturun.    |
    | 7         | Brezilya SEFAZ hizmetini çağır | Gönderme durumunu talep eden XML dosyasını gönderin.          |
    | 8         | Yanıtı işle             | Web servis yanıtını alın.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>SEFAZ Web Hizmetleri için URL'yi ayarlama 

1. **Özellik sürümü kurulumu** sayfasında, **Eylemler** sekmesindeki **Eylemler** hızlı sekmesinde, **Brezilya SEFAZ servisini çağır** seçeneğini belirleyin (eylem kimliği **3**).
2. **Parametreler** hızlı sekmesinde, **URL adresi parametresi** alanına, NF-e gönderimi için SEFAZ Web hizmetinin URL'sini girin.
3. **Eylemler** hızlı sekmesinde, **Brezilya SEFAZ servisini çağır** (eylem kimliği **7**) öğesini seçin.
4. **Parametreler** hızlı sekmesinde, **URL adresi parametresi** alanına, NF-e gönderimi için SEFAZ Web hizmetinin URL'sini girin.

#### <a name="configure-the-cancellation-feature-setup"></a>İptal özelliği kurulumunu yapılandırma

1. **E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **İptal**'i seçin.
2. **Düzenle** öğesini seçin.
3. **Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin.
4. Onaylı bir NF-e iptalini istemek için gereken eylemleri gözden geçirin.

    | Eylem kodu | Eylem adı                  | Eylem açıklaması                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Belgeyi dönüştür           | Gönderme için NF-e iptal XML dosyasını oluşturun.            |
    | 2         | Belgeyi imzala                | XML dosyasına dijital sertifika uygulayın.                   |
    | 3         | Brezilya SEFAZ hizmetini çağır | İmzalı XML dosyasını iptal için Web hizmetlerine gönderin. |
    | 4         | Yanıtı işle             | Web servis yanıtını alın.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>SEFAZ Web Hizmetleri için URL'yi ayarlama

1. **Özellik sürümü kurulumu** sayfasında, **Eylemler** sekmesindeki **Eylemler** hızlı sekmesinde, **Brezilya SEFAZ servisini çağır** seçeneğini belirleyin (eylem kimliği **3**).
2. **Parametreler** hızlı sekmesinde, **URL adresi parametresi** alanına, onaylı NF-e iptali için SEFAZ Web hizmetinin URL'sini girin.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>E-faturalama ortamını kullanılabilir hale getirme ve Taslak sürümü atama

1. **E-faturalama özellikleri** sayfasında, **Ortamlar** sekmesinde, **Etkinleştir** ögesini seçin.
2. **Ortamlar** alanında, ortamı seçin.
3. **Geçerlilik başlangıcı** alanında, yeni ortamın geçerli olacağı tarihi seçin.
4. **Etkinleştir**'i seçin.

![E-faturalama ortamını etkinleştirme](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Durumu Tamamlandı olarak değiştirme

1. **E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Taslak** durumundaki e-faturalama özelliğinin sürümünü seçin.
2. **Durumu değiştir \> Tamamla**'yı seçin.

### <a name="change-the-status-to-publish"></a>Durumu Yayımla olarak değiştirme

1. **E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Tamamlandı** durumundaki e-faturalama özelliğinin sürümünü seçin.
2. **Durumu değiştir \> Yayımla**'yı seçin.

![E-faturalama özelliğini yayımlama](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Finance ve Supply Chain Management uygulamalarında Elektronik faturalama eklenti kurulumu

Kurulum sırasında şu görevleri tamamlayacaksınız:

1. Brezilya için NF-e Federal özelliğini açın.
2. Belirli ER veri modelini, ER veri modeli eşleştirmesini ve NF-e mali belgeleri için gereken biçimleri içe aktarın.
3. ER yapılandırmalarını içe aktarın ve gönderme işleminin sonucu döndürüldükten sonra mali belgenizin durumunu güncelleştirmek için gerekli olan yanıt tiplerini ayarlayın.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Brezilya için NF-e Federal özelliğini açma

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Özellikler** sekmesinde, **BR00053** özellik referansları için satırlarda **Etkinleştir** onay kutusunu seçin.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>NF-e mali belgeleri için gerekli ER veri modeli eşleştirmesini içe aktarma

1. Finance'de oturum açın.
2. **Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft**'u seçin. Bu yapılandırma sağlayıcısının **Etkin** olarak ayarlandığından emin olun. Sağlayıcının **Etkin** olarak nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve etkin olarak işaretleme](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. **Depolar**'ı seçin.
4. **Genel kaynak \> Aç**'ı seçin.
5. **Mali belge eşleme** yapılandırmalarını içe aktarın.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>ER yapılandırmalarını içe aktarma ve mali belgeler için yanıt tiplerini ayarlama

1. **Elektronik raporlama** çalışma alanında, **Yapılandırma sağlayıcıları** bölümünde, **Microsoft**'u seçin.
2. **Depolar**'ı seçin.
3. **Genel kaynak \> Aç**'ı seçin.
4. **NF-e hata günlük alma (BR)**, **NF-e yanıt veri alma biçimi (BR)** ve **NF-e yanıt iletisi alma (BR)** ögelerini içe aktarın.
5. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
6. **Elektronik belge** sekmesinde **Ekle**'yi seçin.
6. **Tablo adı** alanında, **Mali belge başlığı** değerini girin.
7. **Belge bağlamı** alanında, **Müşteri faturası bağlam modeli – Mali belge bağlamı**'nı seçin.
8. **Yanıt türleri**'ni seçin.
9. **Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **Yanıt**'ı seçin.
10. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
11. **Model eşleme** alanında, **Yanıt iletisi içe aktarma biçimi - Yanıt iletisinden model eşlemesi** ögesini seçin.
12. **Kaydet**'i seçin.
13. **Yeni**'yi seçin ve sonra **Yanıt türü** alanında, **ResponseData** ögesini girin.
14. **Gönderim durumu** alanında, **Bekliyor**'u seçin.
15. **Model eşleme** alanında, **NFe yanıtı veri içe aktarma biçimi – Yanıt verilerini içe aktarma** ögesini seçin.
16. **Kaydet**'i seçin.

## <a name="electronic-invoice-processing"></a>Elektronik fatura işleme

Finance'de işlem sırasında şu görevleri tamamlayacaksınız:

1. Elektronik faturalama eklentisi aracılığıyla mali belge gönderin.
2. Gönderme yürütme günlüklerini görüntüleyin ve işlemenin sonuçlarını gözden geçirin.
3. Elektronik faturalama eklentisi aracılığıyla mali belge iptalini gönderin.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>SEFAZ yetkilendirmesi için NF-e mali belgeleri gönderme 

**Yapılandırılabilir Elektronik faturalama eklenti tümleştirmesi** özelliğini açtıktan sonra, onaya NF-e mali belgelerini göndermek için kullanılan eski işlem (**NF-e işlemini dışa/içe aktarma**) artık kullanılamaz. **Elektronik belge gönderme** adı verilen yeni bir işlemle değiştirilir.

> [!NOTE]
> Devam etmeden önce, müşterinin mali kurulumu tarafından verilen bir veya daha fazla müşteri mali belge modeli 55 olduğundan emin olun. Bu mali belgelerin yönü **Giden** olarak ayarlanmalıdır ve durumu **Oluşturuldu** olmalıdır. Daha fazla bilgi için bkz. [Müşteri mali belgelerini düzenleme (Brezilya)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönder** sayfasına gidin.
2. Herhangi bir belgenin ilk gönderimi için, **Belgeyi yeniden gönder** seçeneğini her zaman **Hayır** olarak ayarlayın. Belgeyi servis aracılığıyla yeniden göndermeniz gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın.
3. **Dahil edilecek kayıtlar** hızlı sekmesinde, gönderilecek belgeleri seçmek üzere bir sorgu oluşturabileceğiniz **Sorgulama** iletişim kutusunu açmak için **Filtre**'yi seçin.
4. **Aralık** sekmesinde **Ekle**'yi seçin.
5. **Tablo** alanında, **Mali belge başlığı** değerini seçin.
6. **Türetilmiş tablo** alanında, **Mali belge başlığı** değerini seçin.
6. **Alan** alanında, **Numara** değerini seçin.
7. **Ölçüt** alanına, gönderilmesi gereken mali belgenin numarasını girin.
8. **Sorgulama** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
8. Seçili belgeleri göndermek için **Tamam**'ı seçin.

> [!NOTE]
> Servis aracılığıyla ilk belgeyi gönderme denemeniz sırasında, Elektronik faturalama eklentisi ile bağlantıyı onaylamanız istenecektir. **Elektronik Belge Gönderme Hizmetine bağlanmak için burayı tıklayın** ögesini seçin.

### <a name="view-all-submission-logs"></a>Bütün gönderme günlüklerini görüntüleme

**Yapılandırılabilir Elektronik faturalama eklenti tümleştirmesi** özelliğini açtıktan sonra, belge gönderme işlemini takip etmenizi sağlayan yeni bir sayfa kullanılabilir. Gönderilen tüm belgelerin gönderme günlüklerini görüntülemek için bu sayfayı kullanabilirsiniz.

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
2. **Belge türü** alanında, yalnızca mali belgelerle ilgili filtre uygulamak için **Mali belge başlığı**'nı seçin.
3. Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.

![Gönderme günlüğü ayrıntılarını görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> NF-e mali belgeler için **Hata kodu** sütunu, SEFAZ Web hizmeti tarafından döndürülen dönüş kodunu gösterir.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Mali belge sayfası yoluyla gönderme günlüklerini görüntüleme

**Yapılandırılabilir Elektronik faturalandırma eklentisi tümleştirme** özelliğini açtıktan sonra, mali belge sayfası aracılığıyla gönderme günlüklerini de görüntüleyebilirsiniz.

1. **Genel muhasebe \> Sorgulamalar ve raporlar \> Mali belgeler \> Tüm mali belgeler** sayfasına gidin.
2. Daha önce Elektronik faturalama eklentisi aracılığıyla gönderilen bir mali belge seçin.
3. Eylem Bölmesi'ndeki **NF-e federal** sekmesinde, **Elektronik belge günlüğü**'nü seçin.

![Mali belge sayfası yoluyla gönderme günlüklerini görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>SEFAZ iptali için onaylı NF-e mali belgeleri gönderme

**Yapılandırılabilir Elektronik faturalama eklentisi tümleştirmesi** özelliği etkinleştirildikten sonra, NF-e mali belgelerini iptal etmek için kullanılan eski işlem artık kullanılamaz. **Elektronik belge gönderme günlüğü** sayfasına katıştırılmış yeni bir iptal işlemi ile değiştirilir.

> [!NOTE]
> Onaylanmış bir NF-e mali belge için müşteri mali belgesini iptal etme işlemini çalıştırdığınızdan emin olun. Daha fazla bilgi için bkz. [Müşteri mali belgelerini iptal etme (Brezilya)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
2. Mali belgeyi seçin ve sonra **İşlevler \> İlgili gönderimleri gönder**'i seçin.
3. İlgili gönderim için bir açıklama girin ve **Tamam**'ı seçin.

### <a name="view-cancellation-submission-logs"></a>İptal gönderim günlüklerini görüntüleme

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
2. **Belge türü** alanında, yalnızca mali belgelerle ilgili filtre uygulamak için **Mali belge başlığı**'nı seçin.
3. Mali belgeyi seçin ve sonra Eylem Bölmesi'nde, **Sorgulamalar \> İlgili gönderim**'i seçin.

    İlgili gönderimler, ilk olarak yapılan ana gönderimle ilgili gönderimlerdir. Örneğin, belirli bir NFe'ye yetki veren gönderim ana gönderimdir. SEFAZ içinde aynı NF-e'nin iptal işlemini isteyen gönderim ilgili bir gönderimdir. Yalnızca, başka bir gönderimden yapılan işin iptal edilmesini talep ettiğinden var olur.

    **İlgili gönderimler** sayfası, belirli bir mali belge için tüm ilgili gönderimleri ve bunların gönderim durumlarını gösterir. Aşağıdaki çizimde, ilk satır, mali belgenin onayını talep eden gönderimi temsil eder. İkinci satır, bu mali belgeyi iptal eden gönderimi temsil eder.

    ![İptal gönderim günlüklerini görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları**'nı seçin.

    ![İptal gönderim günlüğü detaylarını görüntüleme](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Gizlilik bildirimi
BR-00053 (NF-e Federal) özelliğinin etkinleştirilmesi, kuruluş vergi kayıt kodunu içeren sınırlı verilerin gönderilmesini gerektirebilir. Bu, devlete ait Web servisi ile tümleştirme için gerekli önceden tanımlanmış biçimde vergi dairesine elektronik fatura göndermek amacıyla vergi dairesi tarafından yetkilendirilen üçüncü taraf kuruluşlarına iletilecektir. Bir yönetici, **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** sayfasına giderek BR-00053 (NF-e Federal) özelliğini etkinleştirebilir ve devre dışı bırakabilir. **Özellikler** sekmesini seçin, BR-00053 özelliğini içeren satırı seçin ve sonra uygun seçimi yapın. Bu harici sistemlerden alınan verilerin bu Dynamics 365 çevrimiçi hizmetine aktarılması [gizlilik bildirimimize](https://go.microsoft.com/fwlink/?LinkId=512132) tabidir. Daha fazla bilgi için, lütfen ülkeye özel özellik belgelerindeki Gizlilik bildirimi bölümlerine bakın.


## <a name="additional-resources"></a>Ek kaynaklar

- [Elektronik faturalama eklentisine genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-get-started.md)
- [Elektronik faturalamayı eklentisini kurma](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]