---
title: İtalya için Elektronik faturalama eklentisini kullanmaya başlangıç
description: Bu konu, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile İtalya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039804"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a>İtalya için Elektronik faturalama eklentisini kullanmaya başlangıç

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> İtalya için Elektronik faturalama eklentisi, Microsoft Dynamics 365 Finance ve Dynamics 365 Supply Chain Management içinden elektronik fatura için kullanılabilen tüm işlevleri şimdilik desteklemeyebilir. 

Bu konu, İtalya için Elektronik faturalama eklentisini kullanmaya başlamanıza yardımcı olacak bilgiler içerir. Regulatory Configuration Services (RCS) ve Finance için ülkeye bağlı olan yapılandırma adımlarında size kılavuzluk eder. Ayrıca, hizmet yoluyla İtalya'ya özel **FatturaPA** biçiminde oluşturulan elektronik faturaları gönderme sürecinde size yol gösterir ve işleme sonuçlarının nasıl incelendiğini açıklar.

## <a name="prerequisites"></a>Önkoşullar

Bu konudaki adımları gerçekleştirmeden önce, [elektronik faturalama eklentisini kullanmaya başlama](e-invoicing-get-started.md) adımlarını tamamlamanız gerekir.

## <a name="rcs-setup"></a>RCS kurulumu

RCS kurulumu sırasında şu görevleri tamamlayacaksınız:

1. Müşteri elektronik faturalarının **FatturaPA** formatında dışa aktarılması için e-faturalama özelliğini içe aktarın.
2. Elektronik faturalar hakkında yanıtlar oluşturmak, göndermek ve almak için gerekli olan biçim yapılandırmalarını gözden geçirin.
3. Elektronik fatura gönderme senaryolarını destekleyen olayları yapılandırın.
4. E-faturalama özelliğini yayımlayın.

> [!NOTE]
> "E-faturala özelliği", Elektronik faturalama eklenti sunucusunu kullanmak üzere yapılandırılmış ve yayımlanmış olan kaynağın genel adıdır. Bu durumda müşteri elektronik faturalarının dışa aktarılması kuracağınız E-faturalama özelliğidir.

## <a name="import-the-e-invoicing-feature"></a>E-faturalama özelliğini içe aktarma

1. RCS hesabınızda oturum açın.
2. **Genelleştirme özellikleri** çalışma alanında **Özellikler** bölmesinde **E-faturalama** kutucuğunu seçin.
3. **E-faturalama Özellikleri** sayfasında, Genel depodan E-faturalama özelliğini içe aktarmak için **İçe aktar** 'ı seçin.

    > [!NOTE]
    > Kullanılabilir özelliklerin listesini göremiyorsanız, **Eşitle** 'yi seçin. 

4. **E-faturaları dışa aktar (IT)** özelliğini seçin ve **içe aktar** 'ı seçin.

![E-faturalar dışa aktarma (IT) özelliğini içe aktarma](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

**E-faturalar dışa aktarma (IT)** özelliğini Genel depodan içe aktardığınızda, sonraki bölümlerde açıklanan tüm ayarlar da alınır.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>E-faturaları dışa aktar (IT) özelliğinin yeni bir sürümünü oluşturma

1. **E-faturalama özellikleri** sayfasında, **Sürümler** sekmesinde, **Yeni** ögesini seçin. 

    ![Yeni e-faturalama özellik sürümü ekleme](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Sonra, e-faturalama özelliğiyle ilişkilendirilmiş Elektronik raporlama (ER) biçimlerini yapılandırabilirsiniz.

2. **Yapılandırmalar** sekmesinde, yapılandırma sürümlerini yönetmek için **Ekle** 'yi seçin.

    ![E-faturalama özellik yapılandırma sürümlerini yönetme](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    Bu adımda, İtalya için e-faturaları dışa aktarmak için kullanılan farklı dosyaların ER biçimlerini ekler ve yapılandırırsınız. İtalyan FatturaPA e-faturalar için, aşağıdaki standart yapılandırmaları veya e-faturalama için kullandığınız gerçek özelleştirilmiş yapılandırmaları kullanın:

    - Satış faturası (IT)
    - Proje faturası (IT)

    Başka bir E-faturalama özelliğinden türetilen bir E-faturalama özelliği oluşturduğunuzda, tüm ER biçimleri orijinal özellikten devralınır.

3. Belirli bir ER biçimi dosya yapılandırması seçin.
4. **Biçim tasarımcısı** sayfasını açmak için **Düzenle** veya **Görüntüle** 'yi seçin.

    ![Biçim tasarımcısı sayfasını açma](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. **Biçim tasarımcısı** sayfasını, ER biçimi dosya yapılandırmalarını düzenlemek ve görüntülemek için kullanın.

    ![Biçim tasarımcısı sayfası](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>E-faturalama özellik kurulumlarını yönetme

- **E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, E-faturalama özellik kurulumlarını yönetmek için **Ekle** , **Sil** veya **Düzenle** ögesini seçin.

![E-faturalama özellik kurulumlarını yönetme](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

Bu adımda, XML çıkış dosyalarının **FatturaPA** biçiminde oluşturulması ve dijital imzalanması (gerekirse) dahil olmak üzere elektronik faturalara uygulanabilir olayları yapılandırabilirsiniz.

### <a name="configure-the-sales-invoice-feature-setup"></a>Satış faturası özellik kurulumunu yapılandırma

1. **E-faturalama özellikleri** sayfasında, **Kurulumlar** sekmesinde, **Özellik kurulumu** sütununda **Satış faturası** 'nı seçin.
2. **Düzenle** öğesini seçin.
3. **Özellik sürümü kurulumu** sayfasında, eylemler listesini yönetmek için **Eylemler** sekmesini seçin. Eylemler, olayın tam olarak yürütülmesi için sırayla çalıştırılması gereken işlemlerin listesini tanımlar.

    ![Eylemler sekmesi](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Eylem kodu | Eylem adı        | Eylem açıklaması                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Belgeyi dönüştür | E-fatura XML dosyasını **FatturaPA** biçiminde oluşturun. |
    | 2         | Belgeyi imzala      | XML dosyasına dijital imza uygulayın.             |

4. Uygulanabilirlik kurallarını görüntülemek ve sürdürmek için **Uygulanabilirlik kuralları** sekmesini seçin. Uygulanabilirlik kuralları, eylemin çalışacağı bağlamı tanımlar.

    ![Uygulanabilirlik kuralları sekmesi](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Değişkenleri görüntülemek ve sürdürmek için **Değişkenler** sekmesini seçin.

    ![Değişkenler sekmesi](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Eylemleri çalıştırmak için gerekli olan ortak değişkenleri tanımlayın.

### <a name="configure-the-project-invoice-feature-setup"></a>Proje faturası özellik kurulumunu yapılandırma 

**Proje faturası** özelliği kurulumunu yapılandırmak için gerekli adımlar ve ayarlar, **Satış faturası** özelliği kurulumuyla ilgili adımlara ve ayarlara benzer. Proje faturalarıyla çalışırken satış faturalarına ilişkin yordamlara bakın.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>E-faturalama özelliğini ortama atama

1. **E-faturalama özellikleri** sayfasında, **Ortamlar** sekmesinde, **Etkinleştir** ögesini seçin.
2. **Ortamlar** alanında, ortamı seçin.
3. **Geçerlilik başlangıcı** alanında, yeni ortamın geçerli olacağı tarihi seçin.
4. **Etkinleştir** 'i seçin. 

![E-faturalama ortamını etkinleştirme](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>E-faturalama özelliğini yayımlama

Sürüm durumunu **Tamamlandı** veya **Yayımlandı** olarak değiştirerek e-faturalama özelliğini yayımlayabilirsiniz.

### <a name="change-the-version-status-to-completed"></a>Sürüm durumunu Tamamlandı olarak değiştirme

1. **E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Taslak** durumundaki e-faturalama özelliğinin sürümünü seçin.
2. **Durumu değiştir \> Tamamla** 'yı seçin. 

### <a name="change-the-version-status-to-published"></a>Sürüm durumunu Yayımlandı olarak değiştirme 

1. **E-faturalama Özellikleri** sayfasındaki **Sürümler** sekmesinde, **Tamamlandı** durumundaki e-faturalama özelliğinin sürümünü seçin.
2. **Durumu değiştir \> Yayımla** 'yı seçin.

![E-faturalama özelliğinin durumunu değiştirme](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a>Finance'de Elektronik faturalama eklentisi tümleştirmesi kurulumu

Finance kurulumu sırasında şu görevleri tamamlayacaksınız:

1. ER veri modelini, ER veri modeli eşleştirmesini ve FatturaPA e-faturaları için bağlam yapılandırmalarını içe aktarın.
2. İtalya e-faturalarını dijital olarak imzalamak için gerekli sertifikayı yapılandırın.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>ER veri modelini, veri modeli eşlemesini ve biçimlerini içe aktarma

1. **Elektronik raporlama** çalışma alanında, **İş Belge Servisi** yapılandırma sağlayıcısının **Etkin** olarak ayarlandığını doğrulayın.
2. **Depolar** 'ı seçin.
3. **Genel kaynak \> Aç** 'ı seçin.
4. **Fatura modeli** , **Fatura modeli eşlemesi** ve **Müşteri faturası bağlam modeli** ögelerini içe aktarın.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>İtalya için müşteri elektronik faturalarını dışa aktarma özelliğini açma

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Özellikler** sekmesinde, **IT00036** özellik referansları için satırlarda **Etkinleştirildi** onay kutusunu seçin.

![FatturaPA özelliğini etkinleştirme](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Elektronik belge yapılandırma

1. **Kuruluş yönetimi \> Kurulum \> Elektronik belge parametreleri** bölümüne gidin.
2. **Elektronik belge** sekmesinde, **Ekle** 'yi seçin ve İtalya e-faturaları oluşturmak için gerekli tabloları girin:

    - **Tablo adı:** Müşteri fatura günlüğü
    - **Tablo adı:** Proje faturası

3. Her tablo için, ilgili belge bağlamını tanımlayın:

    - **Müşteri fatura günlüğü** için **Müşteri fatura bağlamı** 'nı seçin.
    - **Proje faturası** için **Proje fatura bağlamı** 'nı seçin.

![Yanıt türlerini ayarlama](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Elektronik fatura işleme

Finance'de işlem sırasında şu görevleri tamamlayacaksınız:

1. Elektronik faturalama eklentisi ile İtalya için e-faturaları oluşturma
2. Yürütme günlüklerini görüntüleme ve işlemenin sonuçlarını gözden geçirme

### <a name="generate-electronic-invoices"></a>Elektronik faturaları oluşturma

**Yapılandırılabilir Elektronik faturalama eklentisi tümleştirme** özelliğini açtıktan ve **IT00036** özelliğini etkinleştirdikten sonra, İtalya için e-faturaları oluşturmak için eski Finance işlemi artık kullanılamaz. **Elektronik belge gönderme** adı verilen yeni bir işlemle değiştirilir.

E-fatura belgelerinizin gerektirdiği gibi belgeleri el ile gönderebilirsiniz.

> [!NOTE]
> Devam etmeden önce, İtalya'ya ait e-faturalar için gerekli olan kurulumun tamamlandığından emin olun. Daha fazla bilgi için bkz. [Müşteri elektronik faturaları](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices). Elektronik faturalama eklentisi etkinleştirilmesi nedeniyle, bu konuda açıklanan bazı kurulum adımları kullanılamayabilir.

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönder** sayfasına gidin.
2. Herhangi bir belgenin ilk gönderimi için, **Belgeyi yeniden gönder** seçeneğini **Hayır** olarak ayarlayın. Belgeyi servis aracılığıyla yeniden göndermeniz gerekiyorsa, bu seçeneği **Evet** olarak ayarlayın.
3. **Dahil edilecek kayıtlar** hızlı sekmesinde, gönderilecek belgeleri seçmek üzere bir sorgu oluşturabileceğiniz **Sorgulama** iletişim kutusunu açmak için **Filtre** 'yi seçin.

![Elektronik belgeleri gönder iletişim kutusu](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Filtre sorgusu

1. **Sorgulama** iletişim kutusunda, hem satış faturaları hem de proje faturaları için filtreleme koşullarını yapılandırın veya gönderilmeyen tüm faturaları dahil etmek için koşulları boş bırakın.

    ![Gönderme filtresi ölçütlerini ayarlama](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. **Sorgulama** iletişim kutusunu kapatmak için **Tamam** 'ı seçin.
3. Seçili belgeleri göndermek için **Tamam** 'ı seçin.

> ![NOT] Servis aracılığıyla ilk belgeyi gönderme denemeniz sırasında, Elektronik faturalama eklentisi ile bağlantıyı onaylamanız istenecektir. **Elektronik Belge Gönderme Hizmetine bağlanmak için burayı tıklayın** ögesini seçin.

#### <a name="view-submission-logs"></a>Gönderme günlüklerini görüntüleme

Gönderilen tüm belgelerin gönderme günlüklerini görüntüleyebilirsiniz.

1. **Kuruluş Yönetimi \> Dönemlik \> Elektronik belgeler \> Elektronik belgeleri gönderme günlüğü** sayfasına gidin.
2. **Belge türü** alanında, gerekli elektronik belgelerle ilgili olarak filtre uygulamak için **Müşteri fatura günlüğü** veya **Proje faturası** seçeneğini belirleyin.

    ![Gönderme günlüklerinin görüntülemek üzere bir belge türü seçme](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    **Gönderim durumu** sütununda gösterilen değer, gönderme işleminin durumunu temsil eder. İşlemin yapılandırılmış olarak çalışıp çalışmadığını ve başka bir eylemin gerekli olup olmadığını gösterir.

3. Eylem Bölmesi'nde, gönderme yürütme günlüklerinin ayrıntılarını görüntülemek için **Sorgulamalar \> Gönderme ayrıntıları** 'nı seçin.

    ![Gönderme günlüğü ayrıntılarını görüntüleme](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. **İşleme eylemleri** hızlı sekmesinde, RCS'de ayarlanan özellik sürümünde yapılandırılan eylemler için yürütme günlüklerini görüntüleyebilirsiniz. **Durum** sütunu eylemin başarıyla çalıştırılıp çalıştırılmadığını gösterir.
5. **Eylem dosyaları** hızlı sekmesinde, eylemlerin yürütülmesi sırasında oluşturulan ara dosyaları görüntüleyebilirsiniz. Çıkış XML dosyasını **FatturaPA** biçiminde indirmek ve içeriğini görüntülemek için **Görünüm** öğesini seçebilirsiniz.

## <a name="related-topics"></a>İlgili konular

- [Elektronik faturalama eklentisine genel bakış](e-invoicing-service-overview.md)
- [Elektronik faturalama eklentisini kullanmaya başlangıç](e-invoicing-get-started.md)
- [Elektronik faturalamayı eklentisini kurma](e-invoicing-setup.md)
