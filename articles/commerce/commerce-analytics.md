---
title: Commerce analizleri (Önizleme)
description: Bu konu, Microsoft Dynamics 365 Commerce'de analitik özelliğinin nasıl yüklenip kullanılacağını açıklar.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862785"
---
# <a name="commerce-analytics-preview"></a>Commerce analizleri (Önizleme)

[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'de bulunan işlevsel analitik yeteneği olan Commerce analizin (Önizleme) nasıl yükleneceğini açıklamaktadır.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce Analizleri (Önizleme) canlı demo

[Commerce Analizlerinin (Önizleme) canlı demosunu](https://aka.ms/CommerceAnalyticsDemo) deneyebilirsiniz.

![Commerce Analizleri (Önizleme) Özet](media/CommerceAnalytics_Summary.png)
![Commerce Analizleri (Önizleme) Ödemeler](media/CommerceAnalytics_Payments.png)
![Commerce Analizleri (Önizleme) Web etkinliği](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Commerce analizleri (Önizleme) sistem mimarisi

### <a name="key-components"></a>Anahtar bileşenler

Commerce analizleri (Önizleme) aşağıdaki temel bileşenlerden oluşur:

- Kullanıma hazır etkileşimli Power BI raporları
- Azure Synapse Analizleri'nde SQL görünümleri
- Azure Data Lake içinde varlık ve ontoloji verileri
- Azure Data Lake'te ham veriler

![Commerce analizlerinin sistem mimarisinin anahtar bileşenleri](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Veri akışı

#### <a name="step-1-data-generation"></a>Adım 1: Veri oluşturma

Veriler, aşağıdaki kaynaklardan birinden hareket verileri veya davranış verileri kaynağı olarak gelir:

- Bir arama merkezi, satış siparişlerini işlemek için Commerce HQ istemcisini kullanır.
- Satış noktasındaki (POS) kasiyer, satış hareketlerini işler.
- Satışlar, Gözetimsiz Commerce (Commerce Scale Unit) kullanılarak özel uygulamalarda oluşturulur.
- Bir e-ticaret müşterisi e-ticaret web sitenize göz attığında.
- Bir e-ticaret müşterisi, e-ticaret web sitenizde sipariş verdiğinde.
- Veriler, Dynamics 365 Connected Spaces gibi başka sistemler tarafından üretilir.

#### <a name="step-2-ingestion-and-pre-processing"></a>Adım 2: Giriş ve ön işlem

Hareket verileri, doğrudan (Commerce HQ istemcisinde yakalanmış olan siparişler) veya Commerce Scale Unit aracılığıyla (POS'ta, e-ticaret'de veya Gözetimsiz Commerce kullanan özel istemcilerde yakalanmış olan siparişler söz konusu olduğunda) hemen Commerce HQ'ya gider.

Daha sonra Data Lake'e aktar, hareket verilerini veri gölünüze ham veri olarak kopyalamak için kullanılır. Veri gölü içinde ham veriler, Tablolar klasöründe depolanır.

E-ticaret web etkinliği verileri, doğrudan veri gölüne gönderilir. Dynamics 365 Connected Spaces gibi başka sistemler tarafından üretilen veriler, o sistemler tarafından doğrudan veri için gönderilir.

#### <a name="step-3-transformation-and-aggregation"></a>Adım 3: Dönüşüm ve toplama

Ham veriler veri gölünüzde olduktan sonra, Commerce Analizleri hizmeti bunu okur, dönüştürür, toplar ve bunu veri gölüne mantıksal varlıklar (Varlıklar klasöründe) ve toplu ölçümler (Ontolojiler klasöründe) şeklinde yazar.

#### <a name="step-4-querying"></a>Adım 4: Sorgulama

Azure Synapse Analizleri, veri gölü içindeki verileri bir Transact-SQL (T-SQL) arabirimi yoluyla sorgulamak için kullanılır. Bu arabirim SQL görünümlerini içerir. SQL görünümleri, doğrudan bir T-SQL istemcisi (geçici çözümlemeler için) veya Power BI gibi bir görselleştirme aracı aracılığıyla veri gölü içindeki verilerin federe olarak sorgulanmasına olanak tanır.

#### <a name="step-5-modeling-and-serving"></a>Adım 5: Modelleme ve hizmet sunma

Azure Synapse Analizleri tarafından sorgulanan veriler, Power BI'nin anlamsal modeline gider. Veri türüne bağlı olarak, düzenli aralıklarla bellek içi olarak Power BI'ye aktarılır veya çalışma zamanında doğrudan sorgulanır.

Son olarak, veriler Power BI görsellerinde işlenir ve böylece kullanıcılar bunu görüntüleyebilir ve etkileşime girebilir.

## <a name="commerce-analytics-preview-functional-overview"></a>Commerce analizleri (Önizleme) işlevsel genel bakış

### <a name="summary"></a>Özet

Commerce Analizleri şablon uygulaması aşağıdaki ana rapor sayfalarını içerir:

1. [Üst düzey filtreler](#TopLevelFilters)
2. [Ürünler](#ProductsPage)
3. [Müşteriler](#CustomersPage)
4. [Kanallar](#ChannelsPage)
5. [Satışlar](#SalesPage)
6. [Kenar boşlukları](#MarginsPage)
7. [İadeler](#ReturnsPage)
8. [İskontolar](#DiscountsPage)
9. [Ödemeler](#PaymentsPage)
10. [Müşteriler](#CustomersPage)
11. [Karşılaştırma](#ComparisonPage)
12. [Web etkinliği](#WebActivityPage)
13. [Web etkinliği - Üst düzey filtre](#WebActivityTopLevelFilters)

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Üst düzey filtreler

- Tarih ayarları

    - Yıl
    - Üç aylık dönem
    - Ay
    - Hafta
    - Gün

- Kanal ayarları

    - Tüzel kişilik
    - Kanal türü
    - Müşteri türü
    - Satış türü
    - Kanal
    - Kuruluş hiyerarşisi

- Ürün ayarları

    - Kategori hiyerarşisi
    - Kategori

####  <a name="products"></a><a name="ProductsPage"></a> Ürünler

- Satışlar
- Marj
- İadeler

####  <a name="customers"></a><a name="CustomersPage"></a> Müşteriler

- Satışlar
- Marj
- İadeler

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanallar

- Satışlar
- Marj
- İadeler

### <a name="sales"></a>Satışlar <a name="SalesPage"></a>

- Teslim konumuna göre
- Kanal/mağaza/terminale göre
- Personele göre
- Tarihe göre
- Saate göre
- Ürün kategorisine göre

### <a name="margins"></a><a name="MarginsPage"></a> Kenar boşlukları

- Teslim konumuna göre
- Yan ürün
- Tarihe göre

### <a name="returns"></a><a name="ReturnsPage"></a> İadeler

- Tutara göre iade

    - Mağazaya göre
    - Yan ürün
    - Tarihe göre

- Harekete göre iade

    - Mağazaya göre
    - Yan ürün
    - Tarihe göre

### <a name="discounts"></a><a name="DiscountsPage"></a> İskontolar

- Mağazaya göre
- Yan ürün
- Tarihe göre
- Ayrıştırma

    - Tüzel kişilik
    - Mağaza
    - İskonto türü
    - İskonto adı
    - Ürün

### <a name="payments"></a><a name="PaymentsPage"></a> Ödemeler

- Kanal/terminale göre
- Ödeme yöntemi/türe göre
- Tarihe göre
- Ayrıştırma

    - Tüzel kişilik
    - Kanal türü
    - Mağaza
    - Terminal
    - Ödeme yöntemi

### <a name="customers"></a><a name="CustomersPage"></a> Müşteriler

- Yaşam süresi değeri (LTV)

    LTV, bir müşterinin tüm Dynamics 365 Commerce satış kanalları (POS, e-ticaret ve çağrı merkezi dahil) üzerinden harcadığı toplam tutara göre hesaplanır.

- Recency

    Güncellik, müşterinin en son işlem sırasında organizasyonla bu yana geçen gün sayısına göre hesaplanır. Şu anda, güncellik, e-ticaret göz atma etkinliği gibi işlemsel olmayan etkileşim sinyallerini dikkate almıyor.

- Sıklık

    Sıklık, müşterinin kuruluşla olan hareketsel etkileşimine göre hesaplanır. Şu anda, sıklık, e-ticaret göz atma etkinliği gibi işlemsel olmayan etkileşim sinyallerini dikkate almıyor.

- İlişki uzunluğu

    İlişki uzunluğu, müşteri kaydının sistemde oluşturulduğundan bu yana geçen gün sayısına göre hesaplanır.

- Hareket sayısı

### <a name="comparison"></a><a name="ComparisonPage"></a> Karşılaştırma

- Döneme göre ürün karşılaştırması

    - Satış ve satış farkı
    - Marj ve marj farkı

- Döneme göre müşteri

    - Satış ve satış farkı
    - Marj ve marj farkı

### <a name="web-activity"></a><a name="WebActivityPage"></a> Web etkinliği

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Üst düzey filtreler

- Tarih aralığı
- Kanal türü
- Kanal
- Kategori hiyerarşisi

#### <a name="acquisitions"></a>Alımlar

- Sayfa görünümleri

    - Ülke veya bölgeye göre
    - Yan ürün
    - Kullanıcının oturum açmış olduğu duruma göre
    - Tarihe göre

- E-ticaret siparişleri
- Dönüştürme oranı

    - Tarihe göre

- Dönüştürme hunisi

    - Sayfa türüne göre sayfa görünümü (giriş sayfası, kategori sayfası veya ürün ayrıntıları sayfası)
    - Sepete ekle
    - Ödeme
    - Satınalma

#### <a name="sessions"></a>Oturumlar

Oturum, kullanıcının e-ticaret web sitenize ziyareti için bir bölüm. Bir oturum 30 dakika hareketsiz veya 24 saatlik etkin kullanım sonrasında sona erer.

- Ülke veya bölgeye göre
- Kaynağa göre (harici başvuran)
- Kullanıcının oturum açmış olduğu duruma göre
- Oturum sayısı

    - Tarihe göre
    - Giriş sayfasına göre

- Oturum başına sipariş

    - Tarihe göre

- Oturum sıçrama hızı

    Oturum sıçramaları, bir kullanıcının e-ticaret web sitesini ziyaret ettikten hemen sonra bıraktığı bir oturumdur. Daha fazla bilgi için bkz. [Sıçrama oranı](https://en.wikipedia.org/wiki/Bounce_rate).

- Oturum başına tıklama

#### <a name="visitors"></a>Ziyaretçiler

E-ticaret sitenizdeki anonim bir ziyaretçi, belirli tarayıcıya göre ve kullanıcının kullandığı belirli aygıta göre benzersiz olarak tanımlanır. Commerce analizleri, farklı tarayıcılar veya cihazlar üzerinde anonim ziyaretçileri izlemez. Aynı aygıt üzerinde aynı tarayıcıyı kullanan anonim bir ziyaretçi, bir kullanıcının ön belleğe alınma verileri temizleninceye veya bir nokta (genellikle 12 ay) geçerse ve o kadar sonra gerçekleşene kadar birçok kullanıcı oturumu arasında benzersiz olarak tanımlanır.

Ziyaretçiler oturum açtıklarında e-ticaret sitenize göz attıklarında, bunlar hakkında ek bilgi sağlayabilir. Bu bilgiler kuruluşunuzun tüm Dynamics 365 Commerce satış kanallarında (POS, e-ticaret ve çağrı merkezi dahil) önceki satın almaların sonuçları gibi ziyaretçilere sahip olduğu var olan ilişkiye dayanır. Ek bilgiler; güncellik, ilişki uzunluğu, ömür değeri ve sıklık verileri içerir.

- Ziyaretçi marjı
- Ziyaretçi ortalama siparişleri
- Ziyaretçi ortalama satışları
- E-ticaret ziyaretçi sayısı

    - Tarihe göre
    - Konuma göre

        Şu anda, Commerce analizleri, e-ticaret ziyaretçilerine ilişkin konum öngörüleri için yalnızca ülke/bölge düzeyinde ayrıntı sağlayabilir.

    - Güncelliğe göre

        Güncellik, müşterinin en son işlem sırasında organizasyonla bu yana geçen gün sayısına göre hesaplanır. Şu anda, güncellik, e-ticaret göz atma etkinliği gibi işlemsel olmayan etkileşim sinyallerini dikkate almıyor.

    - İlişki uzunluğuna göre

        İlişki uzunluğu, müşteri kaydının sistemde oluşturulduğundan bu yana geçen gün sayısına göre hesaplanır.

    - Yaşam süresi değerine (LTV) göre

        LTV, bir müşterinin tüm Dynamics 365 Commerce satış kanalları (POS, e-ticaret ve çağrı merkezi dahil) üzerinden harcadığı toplam tutara göre hesaplanır.

    - Sıklığa göre

        Sıklık, müşterinin kuruluşla olan hareketsel etkileşimine göre hesaplanır. Şu anda, sıklık, e-ticaret göz atma etkinliği gibi işlemsel olmayan etkileşim sinyallerini dikkate almıyor.

#### <a name="impressions"></a>Etkiler

Bir etki, ticaret ziyaretçisinden bir ürün görselin tek bir görünümüdür. Örneğin, bir e-ticaret ziyaretçisi e-ticaret web sitenizin giriş sayfasına gider ve **En çok satanlar** listesi modülünde bir yoga matı ürününü görüntüler. Ziyaretçi, **Sizin için seçtiklerimiz** liste modülünde aynı yoga matını görüntüler. Bu durumda, iki ürün etkisi vardır. 

Şu anda, etkiler aşağıdaki yüzeylerde izleniyor:

- Listeler (örneğin, **Önerilen**, **En çok satan**, **Sizin için seçtiklerimiz** ve **Popüler**)
- Alışveriş sepeti modülü
- Arama sonucu konteyneri
- Kategori araması sonucu konteyneri

Günümüzde, bir döngü modülde veya özel görsellere işlenmiş olan ürünler, etki ilgili ölçümler içinde dikkate sayılmaz.

**Etki raporu** sayfası, aşağıdaki ölçümleri içerir:

- Etki sayısı

    - Sayfa türüne ve modülüne göre

        Sayfa türü, e-ticaret web sitenizde her sayfa için tanımlanan genel bir sayfa türüdür. Modül türü, ürünün içinde gösterildiği e-ticaret görsel modülünün türüdür.

        Modüle göre etkileri görmek için sayfa ve modül görsellerinde ayrıntıya inmeniz gerekebilir.

    - Yan ürün
    - Kullanıcının oturum açmış olduğu duruma göre
    - Tarihe göre

- Etki tıklama sayısı

    Bir e-ticaret ziyaretçisi bir ürün görseli seçtiğinde bir etki tıklaması gerçekleşir. Tipik olarak ziyaretçi sonrasında ürünle ilgili ayrıntıların yer aldığı ürün sayfasına yönlendirilir.

- Etki tıklama oranı (CTR)

    CTR, toplam etki sayısının tıklatmaların toplam sayısına bölünmesiyle hesaplanır.

## <a name="commerce-analytics-preview-installation"></a>Commerce analizleri (Önizleme) kurulumu

> [!NOTE]
> Commerce analizleri (Önizleme); Amerika Birleşik Devletleri, Kanada, Birleşik Krallık, Avrupa, Güney Doğu Asya, Doğu Asya, Avustralya ve Japonya bölgelerinde önizlemededir. Finance and Operations ortamınız bu bölgelerden herhangi birinde ise, Microsoft Dynamics Lifecycle Services (LCS) kullanarak ortamınızda bu özelliği etkinleştirebilirsiniz. Bu özelliği kullanabilmeniz için bkz. [Azure Data Lake'e aktarmayı yapılandırma](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Commerce analizlerini etkinleştirme ve konfigüre etme (Önizleme)

Commerce analizleri (Önizleme) yüklemek için bir Azure aboneliği içinde kaynak oluşturma izniniz olması gerekir. Ayrıca LCS ile eklenti yükleme izinlerinizin olması da gerekir. Adımların genel bakışı:

1. [Commerce analizleri (Önizleme) için Önizleme formunu gönderin](#joinPreview).
2. [Data Lake'e aktarmayı etkinleştirin ve yapılandırın](#enableExportToDataLake).
3. [Commerce analizleri (Önizleme) eklentisini etkinleştirme ve konfigüre etme](#enableCommerceAnalyticsAddin).
4. [Depolama hesabınız için paylaşılan bir erişim imzası (SAS) belirteci oluşturun](#getSASToken).
5. [Azure Synapse görünümleri için dağıtım betiklerini indirin](#downloadSynapseDeploymentScripts).
6. [Bir Azure Synapse workspace yükleyin ve konfigüre edin](#configureAzureSynapse).
7. [Power BI şablon uygulamasını kurun](#powerbi).

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a>Commerce analizleri (Önizleme) için Önizleme formunu gönderin

[Commerce analizleri (Önizleme) için Önizleme formunu](https://forms.office.com/r/vW5VLJGXZ2) gönderin. Formun işlenmesi için üç iş günü kadar sürer. İşlem tamamlandıktan sonra, formda sağladığınız e-posta adresine bir onay e-postası gönderilir.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a>Data Lake'e aktarmayı etkinleştirin ve yapılandırın

Commerce analizleri (Önizleme), Commerce HQ verilerini Data Lake'e vermek ve verileri yeni tutmak için Data Lake'e ver özelliğini kullanır. Commerce analizlerini (Önizleme) konfigüre etmeden önce, [Azure Data Lake'e aktarmayı yapılandırma](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) bölümündeki adımları izleyerek Data Lake'e vermeyi etkinleştirin ve yapılandırın.

Data Lake'e aktarmayı konfigüre ederken, aşağıdaki bilgileri not edin çünkü daha sonra girmeniz gerekecektir:

- <a name="keyVault"></a>Key Vault'un Etki Alanı Adı Sistemi (DNS) adı ve uygulama kimliği ile uygulama parolasını sakladığınız yerin gizli dizi adı. Daha fazla bilgi için bkz. [Kev Vault'a gizli dizi ekleme](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).
- <a name="storageAccount"></a>Data Lake örneği için depolama hesabının adı. Daha fazla bilgi için, bkz. [Aboneliğinizde Data Lake Storage (Gen2) hesabı oluşturma](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Commerce analizleri (Önizleme) eklentisini etkinleştirme ve konfigüre etme

LCS'de Commerce analizleri (Önizleme) eklentisini yüklemek için kullanmayı planladığınız ortam için LCS'de ortam yöneticisi olmanız gerekir.

Commerce analizleri (Önizleme) eklentisini kurmak ve yapılandırmak için aşağıdaki adımları izleyin.

1. [LCS](https://lcs.dynamics.com/)'de oturum açın ve ortamınıza gidin.
2. **Ortam** sayfasında, **Ortam eklentileri** sekmesinde, **Yeni eklenti kur**'u seçin.
3. İletişim kutusunda, **Commerce analizleri (Önizleme)** öğesini seçin.

    **Commerce analizleri (Önizleme)** listelenmiyorsa, Insider Program'a katıldığınızdan emin olun.

4. **Kurulum eklentisi** iletişim kutusuna, aşağıdaki bilgileri girin.

    | Bilgi | Kaynak | Örnek değer |
    |---|---|---|
    | Ortamınız için Azure AD Kiracı Kimliği | [Azure portalında](https://portal.azure.com/) oturum açın ve **Azure Active Directory** hizmetini açın. Sonra **Özellikler** sayfasını açın ve **Dizin Kimliği** alanındaki değeri kopyalayın. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | Key Vault'unuzun DNS adı | Key Vault'unuz için [DNS adını](#keyVault) girin. Önceki bölümde bu değerden bir not oluşturmuş olmanız gerekir. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Uygulama Kodu içeren gizli kod dizesi | [Uygulama kodunu depolayan gizli dizi adını](#keyVault) girin. Önceki bölümde bu değerden bir not oluşturmuş olmanız gerekir. | app-id |
    | Uygulama gizli dizisini içeren gizli kod dizesi | [Uygulama gizli dizisini depolayan gizli dizi adını](#keyVault) girin. Önceki bölümde bu değerden bir not oluşturmuş olmanız gerekir. | app-secret |

5. Onay kutusunu işaretleyerek teklif koşullarını kabul edin ve **Yükle**'yi seçin.

    Sistem, ortam için Commerce analizleri (Önizleme) eklentisini yükler ve konfigüre eder. Bu işlem birkaç dakika sürebilir. Tamamlandıktan sonra, **Commerce analizleri (Önizleme)**, **Ortam** sayfasında listelenmiş ve durumunun **Yüklü** olması gerekir.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a>Depolama hesabınız için bir SAS belirteci oluşturun

SAS belirteci, dış varlıkların depolama hesabınıza erişmesini ve sınırlı bir süre için belirli ayrıcalıklara sahip olmasını sağlar. Azure Synapse, Data Lake'de alttaki verilere erişmek için SAS belirtecini kullanır.

> [!NOTE]
> Commerce analizlerinin (Önizleme) bilinen bir sınırlaması nedeniyle, SAS belirtecinin süresi sona erdiğinde, Azure Synapse örneği, veri gölüne erişimi kaybedecektir. Bu nedenle, SAS belirtecini oluştururken, kuruluşunuzun güvenlik ilkelerinin izin verilen en uzun bitiş tarihini ayarlamalısınız.

SAS belirteci oluşturmak için aşağıdaki adımları izleyin.

1. Azure portalında, Data Lake'e dışa aktarmayı konfigüre ederken oluşturduğunuz [depolama hesabına](#storageAccount) gidin.
2. Sol bölmede, depolama hesabının altında, **Paylaşılan erişim imzasını** seçin.
3. **SAS seçenekleri** sayfasında, aşağıdaki alanları ayarlayın.

    | Alan | Değer |
    |---|---|
    | İzin verilen servisler | **Blob**'u seçin. |
    | İzin verilen kaynak türleri | **Hizmet**, **Konteyner** ve **Nesne**'yi seçin. |
    | İzin verilen izinler | **Okuma**, **Yazma**, **Silme**, **Liste**, **Ekleme** ve **Oluştur**'u seçin. |
    | Blob sürüm oluşturma izinleri | **Sürümlerin silinmesini etkinleştirir**'i seçin. |
    | Başlangıç ve bitiş tarihi/saati | SAS belirteci için uygun bir başlangıç ve bitiş tarihi ve saati ayarlayın. |
    | İzin verilen IP adresleri | Bu alanı boş bırakın. |
    | İzin verilen protokoller | **Yalnızca HTTPS**'yi seçin. |
    | Tercih edilen yönlendirme katmanı | **Temel (varsayılan)** seçeneğini belirleyin. |
    | İmzalama anahtarı | Uygun şekilde **key1** veya **key2** seçin. |

4. **SA ve bağlantı dizesi oluştur** seçeneğini belirleyin.
5. **SAS belirteci** alanındaki değeri kopyalayın ve Not Defteri gibi bir metin düzenleyicisine yapıştırın.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a>Azure Synapse görünümleri için dağıtım betiklerini indirin

Azure Synapse workspace'te gerekli görünümler oluşturmak ve yayımlamak için bir dizi komut dosyası çalıştırmalısınız. Bu adımları izleyerek betikleri indirin.

1. GitHub'da, [microsoft/Dynamics365Commerce.Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions) deposuna gidin.
2. Depoyu klonlayarak veya zip dosyası olarak karşıdan yükleyerek, kodları yerel bilgisayarınıza yükleyin.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Bir Azure Synapse workspace yükleyin ve konfigüre edin

Azure Synapse workspace yüklemek ve yapılandırmak için şu adımları izleyin.

1. Azure aboneliğinize bir Azure Synapse workspace yükleyin. Daha fazla bilgi için bkz. [Hızlı başlangıç: Synapse çalışma alanı oluşturma](/azure/synapse-analytics/quickstart-create-workspace).
2. Not defteri veya başka bir metin düzenleyicide, yerel bilgisayarınızdaki önceki bölümdeki Dynamics365Commerce.Solutions deposuna kopyaladığınız veya indirdiğiniz klasörden **SetupSynapse.sql** komut dosyası dosyasını açın. Betik dosyası, /Pipeline/CommerceAnalyticsSynapse/ klasörü altında olacaktır. Betikte, yer tutucu metnin yerine aşağıdaki tabloda gösterilen değerleri ekleyin.

    | Yer tutucu metin | Değiştirme değeri |
    |---|---|
    | placeholder_storageaccount | Data Lake'e dışa aktarmayı konfigüre ederken oluşturduğunuz [depolama hesabının](#storageAccount) adı. |
    | <a name="phContainer"></a>placeholder_container | LCS içindeki Data Lake eklentisini başarıyla yükledikten sonra Data Lake örneği içinde oluşturulmuş depolama kapsayıcısının adı. Kapsayıcı adını almak için, depolama hesabınıza göz atmak üzere Azure portalında Depolama Gezgini'ni kullanmalısınız. |
    | placeholder_sastoken | Oluşturduğunuz [SAS belirteci](#getSASToken). SAS belirteci değerinin başlangıcından soru işaretini (**?**) kaldırmayı unutmayın. |
    | <a name="phUserPwd"></a>placeholder_password | Seçtiğiniz güçlü bir parola. Bu parolayı not edin. Betiğin oluşturduğu yeni **reportreadonlyuser** hesabı için parola olarak ayarlanacak. **Sqladminuser** hesabının parolasını **girmeyin**. |

3. Betik dosyasının güncelleştirilmiş içeriğini kopyalayın.
4. Azure portalda, yeni Azure Synapse workspace'e gidin. **Genel bakış** sayfasında **Synapse Studio'yu aç**'ı seçin.
5. Synapse Studio'da **Yeni \> SQL betiği**'ni seçin ve betik dosyasının içeriğini SQL betik düzenleyicisine yapıştırın.
6. **Kullanıcı veri tabanı** alanının **ana** olarak ayarlandığından emin olun.
7. **Çalıştır**'ı seçin ve betiğin çalışmasını bitirmesini bekleyin. Kodu başarıyla yürütürken Commerce analizleri için veritabanı, veri gölüne erişim için kimlik bilgileri ve Azure Synapse örneğine bağlanmak için Power BI'nin kullanacağı salt okunur bir kullanıcı hesabı oluşturulur.
8. Yerel bilgisayarınızda, Windows PowerShell'i yönetici modunda açın ve Dynamics365.Commerce.Solutions deposundan kopyalanan veya indirilen klasörün altındaki /Pipeline/CommerceAnalyticsSynapse/ klasörüne gidin.
9. Aşağıdaki komutu çalıştırarak Windows PowerShell yürütme ilkesini ayarlayın.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. SQL Server PowerShell modülü önceden yüklü değilse, aşağıdaki komutu çalıştırarak yükleyin.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Modülün yüklenmesi sırasında, NuGet sağlayıcısını yüklemeniz istenebilir. Bu durumda, NuGet sağlayıcısı yüklemek için **Y**'yi seçin. Ayrıca, güvenilmeyen bir depodan modülleri yeniden yüklemeyi istediğinizi onaylamak isteyebilirsiniz. Bu durumda, yükleme işlemine devam etmek için **Y**'yi seçin. **PSGallery** deposuna güvenmek için isteğe bağlı olarak **Set-PSRepository** cmdlet'ini çalıştırabilirsiniz.

11. Aşağıdaki komutu çalıştırarak Azure Synapse görünümlerini yayımlayın.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Bu komutu çalıştırdığınızda, yer tutucu değerleri aşağıdaki tabloda gösterilen değerlerle değiştirin.

    | Yer tutucu değeri | Değiştirme değeri |
    |---|---|
    | SERVER_NAME | Azure Synapse Sunucusuz SQL uç noktasının adı. Bu değeri, Azure portalında Azure Synapse workspace'in **Genel bakış** sayfasından alabilirsiniz. |
    | PAROLA | **Sqladminuser** hesabının parolası. |
    | STORAGE_ACCOUNT | Data Lake için depolama hesabının adı. |
    | CONTAINER_NAME | Data Lake'e aktar özelliği tarafından oluşturulan konteynerin adı. Bu konteyner, adım 2'de [placeholder_container](#phContainer) değeri olarak belirttiğiniz konteynerdir. |
    | DATA_ROOT_PATH | Tüm verileri içeren konteyner altındaki klasör adı. |

    > [!NOTE]
    > Azure Storage tarayıcısı ve veri kök yolunu Azure portal içindeki Data Lake depolama hesabınızı kullanarak bulabilirsiniz.

12. Betiğin çalışmasını bitirmesini bekleyin. Betiğin başarıyla yürütülmesi, Azure Synapse Sunucusuz SQL örneğinde SQL görünümleri oluşturacaktır.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI şablon uygulamasını kurun

Commerce analizleri (Önizleme) için Power BI şablon uygulamasını kurmak için aşağıdaki adımları izleyin.

1. Kuruluş kimliğinizi kullanarak [Power BI portalda](https://powerbi.microsoft.com/) oturum açın.
2. [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) adresine giderek Commerce analizleri (Önizleme) Power BI şablon uygulamasını yükleyin. Uygulamanın AppSource'ta listelenmediğini belirten bir uyarı alabilirsiniz. **Yükle**'yi seçin.
3. Uygulamayı ilk kez yüklüyorsanız 5. adıma atlayın. Bu uygulamayı daha önce yüklediyseniz, uygulamayı güncelleştirmek için aşağıdaki seçenekler gösterilir:

    - **Çalışma alanını ve uygulamayı güncelleştirin** – Var olan şablon uygulamasını güncelleştirin ve uygulama örneği adı ve izin yapılandırmaları gibi var olan uygulama ayarlarınızın üzerine yazın.
    - **Uygulamayı güncelleştirmeden yalnızca çalışma alanı içeriğini güncelleştir** – Var olan şablon uygulamasını güncelleştirin, ancak var olan uygulama ayarlarınızı koruyun. *Bu seçenek, uygulama güncelleştirmeleri için önerilen seçenektir.*
    - **Uygulamanın başka bir kopyasını yeni bir çalışma alanına yükleyin** – Yeni bir çalışma alanı oluşturun ve içinde var olan şablon uygulamasının bir kopyasını oluşturun. Varolan çalışma alanı dokunulmayacak şekilde bırakılacak.

4. Güncelleştirme seçeneklerinden birini belirleyin ve sonra **Yükle**'yi seçin.
5. Sol bölmedeki **Uygulamalar**'ı seçip ardından uygulamayı seçerek yüklü uygulamayı açın.
6. **Bağlan**'ı seçerek, uygulamayı veri kaynağınıza bağlayın. Uygulamayı daha önce yüklediyseniz, sarı ileti çubuğunda **Verilerinizi bağlayın**'ı seçin.
7. Aşağıdaki alanları ayarlayın.

    | Alan | Değer |
    |---|---|
    | Sunucu | Önceki bölümde oluşturduğunuz Azure Synapse Sunucusuz SQL son noktasının adını girin. Bu değeri, Azure portalında Azure Synapse workspace'in **Genel bakış** sayfasından alabilirsiniz. |
    | Veritabanı | **CommerceAnalytics** girin. |
    | Dil | Listede bir değer seçin. Bu alan, yerelleştirilmiş ürün ve kategori adları için kullanılır. Değer, büyük/küçük harf duyarlıdır. |
    | Tarih Aralığı | Listede bir değer seçin. Seçilen ay sayısı için veriler, Power BI veri kümesine aktarılır. Seçtiğiniz değer, veri kümesinin boyutunu ve eşitleme için gereken zamanı etkiler. |

8. **Sonraki**'yi seçin. Azure Synapse SQL veritabanına bağlanmak için kimlik bilgilerini girmeniz istenir. Alanları aşağıdaki tabloda açıklandığı gibi ayarlayın.

    | Alan | Değer |
    |---|---|
    | Kimlik doğrulama yöntemi | **Temel**'i seçin. |
    | Kullanıcı adı | **reportreadonlyuser** girin. |
    | Parola | SetupSynapse.sql kodu içinde [placeholder_password](#phUserPwd) yer tutucusuyla değiştirdiğiniz değeri girin. Bu parola, **reportreadonlyuser** hesabının parolasıdır. |

9. **Oturum aç ve bağlan**'ı seçin.
10. Veri kümesi başarıyla güncellenene kadar bekleyin. Sonra , veri kümesinin güncelleştirme durumunu görüntüleyebileceğiniz uygulama çalışma alanını açmak için **Uygulamayı düzenle** düğmesini seçin. Uygulama çalışma alanında, isteğe bağlı olarak veri kümeniz için otomatik güncelleştirme zamanlamaları ayarlayabilir, izinleri yönetebilir ve uygulama örneğini yeniden adlandırabilirsiniz.

### <a name="privacy"></a><a name="privacy"></a>Gizlilik

Gizliliğiniz bizim için önemlidir. Daha fazla bilgi için [Gizlilik Bildirimimizi](https://go.microsoft.com/fwlink/?LinkId=521839) okuyun.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
