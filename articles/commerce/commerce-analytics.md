---
title: Commerce analizleri (Önizleme)
description: Bu konu, Microsoft Dynamics 365 Commerce'de analitik özelliğinin nasıl yüklenip kullanılacağını açıklar.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7e3721421e15bc3e5937691cdbaee51e4d3cdd17
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349755"
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
- Azure Synapse Analytics'te SQL görünümleri
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

Azure Synapse Analytics, veri gölü içindeki verileri bir Transact-SQL (T-SQL) arabirimi yoluyla sorgulamak için kullanılır. Bu arabirim SQL görünümlerini içerir. SQL görünümleri, doğrudan bir T-SQL istemcisi (geçici çözümlemeler için) veya Power BI gibi bir görselleştirme aracı aracılığıyla veri gölü içindeki verilerin federe olarak sorgulanmasına olanak tanır.

#### <a name="step-5-modeling-and-serving"></a>Adım 5: Modelleme ve hizmet sunma

Azure Synapse Analytics tarafından sorgulanan veriler, Power BI'nin anlamsal modeline gider. Veri türüne bağlı olarak, düzenli aralıklarla bellek içi olarak Power BI'ye aktarılır veya çalışma zamanında doğrudan sorgulanır.

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

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Üst düzey filtreler

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

#### <a name="products"></a><a name="ProductsPage"></a> Ürünler

- Satışlar
- Marj
- İadeler

#### <a name="customers"></a><a name="CustomersPage"></a> Müşteriler

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
> Commerce analizleri (Önizleme); Amerika Birleşik Devletleri, Kanada, Birleşik Krallık, Avrupa, Güney Doğu Asya, Doğu Asya, Avustralya ve Japonya bölgelerinde önizlemededir. Finance ve Operations ortamınız bu bölgelerden herhangi birinde ise, Microsoft Dynamics Lifecycle Services (LCS) kullanarak ortamınızda bu özelliği etkinleştirebilirsiniz. Bu özelliği kullanabilmeniz için bkz. [Azure Data Lake'e aktarmayı yapılandırma](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a>Commerce analizlerini etkinleştirme ve konfigüre etme (Önizleme)

Commerce analizleri (Önizleme) yüklemek için bir Azure aboneliği içinde kaynak oluşturma izniniz olması gerekir. Ayrıca LCS ile eklenti yükleme izinlerinizin olması da gerekir. 

Commerce analizleri (Önizleme) etkinleştirmek ve yapılandırmak için aşağıdaki adımları izleyin.

1. [Data Lake'e Aktarma eklentisini etkinleştirin ve yapılandırın](#enableExportToDataLake).
1. [Bir Azure Synapse workspace yükleyin ve konfigüre edin](#configureAzureSynapse).
1. [Anahtar kasasına gizli diziler ekleyin ](#addSecrets).
1. [Commerce analizleri (Önizleme) eklentisini etkinleştirme ve konfigüre etme](#enableCommerceAnalyticsAddin).
1. [Power BI şablon uygulamasını kurun](#powerbi).

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a>Data Lake'e Aktarma eklentisini etkinleştirin ve yapılandırın

> [!IMPORTANT]
> Data Lake'e Aktar eklentisini yapılandırdığınızda, gerçek zamanlı veri değişikliklerinin etkin olmamasını sağlamak için Data Lake eklenti kurulumu sayfasındaki **Gerçek zamanlı veri değişiklikleri** onay kutusunu temizleyin. **Gerçek zamanlı veri değişiklikleri** özelliği önizlemededir ve şu anda Commerce Analytics tarafından desteklenmez. Bu özelliği etkinleştirirseniz, Commerce Analytics Data Lake, verilerinizi işleyemez ve Power BI raporlarınızın çoğu veri göstermez.

Commerce analizleri (Önizleme), Commerce genel merkez verilerini Data Lake'e vermek ve verileri yeni tutmak için Data Lake'e ver özelliğini kullanır. Commerce analizlerini (Önizleme) konfigüre etmeden önce, [Azure Data Lake'e aktarmayı yapılandırma](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) bölümündeki adımları izleyerek Data Lake'e vermeyi etkinleştirin ve yapılandırın.

Data Lake'e Aktarma eklentisini konfigüre ettiğinizde aşağıdaki bilgileri not edin çünkü daha sonra girmeniz gerekecektir:

- <a name="keyVault"></a>Sağladığınız anahtar kasanın Etki Alanı Adı Sistemi (DNS) adı.
- Sağladığınız gizli dizi adları ve uygulama kimliği ve uygulama gizli dizisi bulunur. Daha fazla bilgi için bkz. [Kev Vault'a gizli dizi ekleme](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a>Bir Azure Synapse workspace yükleyin ve konfigüre edin

Commerce Analytics (Önizleme), Azure Synapse workspace'de isteğe bağlı Synapse SQL sağlanmasını gerektirir. Azure Synapse workspace yüklemek ve yapılandırmak için şu adımları izleyin.

1. Azure aboneliğinize bir Azure Synapse workspace yükleyin. Daha fazla bilgi için bkz. [Hızlı başlangıç: Synapse çalışma alanı oluşturma](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a>Çalışma alanı sağlandıktan sonra, kaynağa genel bakış sayfasını açın ve **Sunucusuz SQL son nokta** değerini not alın. Bu değeri bir sonraki bölümde anahtar kasada saklamanız gerekir.
1. Genel bakış sayfasında, çalışma alanınız için Azure Synapse Studio'yu açmak üzere **Synapse Studio'yu aç** bağlantısını seçin.
1. Sol menüdeki **Yönet** öğesini seçin. Menü adlarını görmek için, sol menüde genişletme bağlantısını seçmeniz gerekebilir.
1. **Güvenlik grubu** altında **Erişim denetimi**'ni seçin. 
1. **Ekle**'yi seçin.
1. **Rol ataması ekleme** bölmesinde, seçenekleri aşağıdaki tabloda açıklandığı gibi ayarlayın.

    | Seçenek | Değer |
    |--------|-------|
    | Kapsam | **Çalışma alanı**'nı seçin. |
    | Rol | **Synapse SQL Yöneticisi**'ni seçin.|
    | Kullanıcı seç | [Data Lake'e Aktarma eklentisinin kurulumu sırasında oluşturduğunuz](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication) uygulamanın adını arayın. Uygulama arama sonuçlarında göründüğünde, bunu seçin. Uygulama artık **Seçili kullanıcılar, gruplar veya hizmet sorumluları** bölümünde görüntülenecektir. |

1. Rol atamasını tamamlamak için **Uygula** seçeneğini belirleyin. Uygulamaya Synapse SQL Yönetici ayrıcalıkları verilir. Bu nedenle, Commerce Analytics (Önizleme) LCS eklentisinin konfigürasyonu sırasında gerekli görünümleri oluşturabilir.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a>Anahtar kasasına gizli diziler ekleyin

Data Lake'e Aktarma eklentisini yapılandırırken kullandığınız aynı [anahtar kasasında](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault), aşağıdaki tabloda gösterilen gizli dizileri eklemeniz gerekir. Her bir gizli dizi için gizli dizi adını ve belirlenen değeri sağlamanız gerekir.

| Önerilen gizli dizi adı | Gizli anahtar değeri | Örnek gizli dizi değeri |
|---------|---------|---------|
| synapse-sql-server | [Azure Synapse workspace'in yapılandırırken](#serverlessep) not aldığınız sunucusuz SQL uç noktası. | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a>readonly-sql-pwd | SQL salt okuma kullanıcısı için belirlenen parola. Power BI raporu, sunucusuz SQL'ye bağlanmak için bu parolayı kullanır. Parolayı belirlemek için kuruluşunuzun parola ilkelerini izleyin. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a>Commerce analizleri (Önizleme) eklentisini etkinleştirme ve konfigüre etme

LCS'de Commerce analizleri (Önizleme) eklentisini yüklemek için kullanmayı planladığınız ortam için LCS'de ortam yöneticisi olmanız gerekir.

Commerce analizleri (Önizleme) eklentisini kurmak ve yapılandırmak için aşağıdaki adımları izleyin.

1. [LCS](https://lcs.dynamics.com/)'de oturum açın ve ortamınıza gidin.
2. **Ortam** sayfasında, **Ortam eklentileri** sekmesinde, **Yeni eklenti kur**'u seçin.
3. İletişim kutusunda, **Commerce analizleri (Önizleme)** öğesini seçin.
4. **Kurulum eklentisi** iletişim kutusuna, aşağıdaki bilgileri girin.

    | Bilgi | Kaynak | Örnek değer |
    |---|---|---|
    | Azure Active Directory (Azure AD) Kiracı Kimliği | [Azure portalında](https://portal.azure.com/) oturum açın ve **Azure Active Directory** hizmetini açın. Sonra **Özellikler** sayfasını açın ve **Kiracı Kimliği** alanındaki değeri kopyalayın. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | Azure Key Vault'unuzun DNS adı | Key Vault'unuz için DNS adını girin. [Data Lake'e Aktarma eklentisini yapılandırırken](#keyVault) bu değeri kaydetmeniz gerekirdi. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Uygulama Kodu içeren gizli dizi adı | Uygulama kodunu depolayan gizli dizi adını girin. [Data Lake'e Aktarma eklentisini yapılandırırken](#keyVault) bu değeri kaydetmeniz gerekirdi. | `app-id` |
    | Uygulama gizli dizisini içeren gizli dizi adı | Uygulama gizli dizisini depolayan gizli dizi adını girin. [Data Lake'e Aktarma eklentisini yapılandırırken](#keyVault) bu değeri kaydetmeniz gerekirdi. | `app-secret` |
    | Azure Synapse için sunucusuz SQL uç noktayı içeren gizli dizi adı | Sunucusuz SQL uç noktasının saklandığı gizli dizi adını girin. Gizli diziyi, [anahtar değerine gizli diziler eklerken](#addSecrets) oluşturmuş olmanız gerekir. | `synapse-sql-server` |
    | Azure Synapse'de SQL salt okuma kullanıcıları için belirlenmiş parolayı içeren gizli dizi adı | Sunucusuz SQL salt okuma kullanıcısı için ayarlanacak parolayı içeren gizli dizi adını girin. Bu kullanıcı sizin için oluşturulur ve sunucusuz SQL sunucusuna bağlanmak için Power BI raporunda kullanılmalıdır. Gizli diziyi, [anahtar değerine gizli diziler eklerken](#addSecrets) oluşturmuş olmanız gerekir. | `readonly-sql-pwd` |

1. Onay kutusunu işaretleyerek teklif koşullarını kabul edin ve **Yükle**'yi seçin.

    Sistem, ortam için Commerce analizleri (Önizleme) eklentisini yükler ve konfigüre eder. Bu işlem birkaç dakika sürebilir. Tamamlandıktan sonra, **Commerce analizleri (Önizleme)**, **Ortam** sayfasında listelenmiş ve durumunun **Yüklü** olması gerekir.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI şablon uygulamasını kurun

Commerce analizleri (Önizleme) için Power BI şablon uygulamasını kurmak için aşağıdaki adımları izleyin.

1. Kuruluş kimliğinizi kullanarak [Power BI portalda](https://powerbi.microsoft.com/) oturum açın.
1. [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) adresine giderek Commerce analizleri (Önizleme) Power BI şablon uygulamasını yükleyin. Alternatif olarak [Dynamics 365 Commerce Analytics için AppSource sayfasını](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) ziyaret edin ve **Şimdi al**'ı seçin.
1. Uygulamayı ilk kez yüklüyorsanız 5. adıma atlayın. Bunu daha önceden yüklediyseniz uygulamayı güncelleştirmek için aşağıdaki seçenekler bulunur:

    - **Çalışma alanını ve uygulamayı güncelleştirin** – Var olan şablon uygulamasını güncelleştirin ve uygulama örneği adı ve izin yapılandırmaları gibi var olan uygulama ayarlarınızın üzerine yazın.
    - **Uygulamayı güncelleştirmeden yalnızca çalışma alanı içeriğini güncelleştir** – Var olan şablon uygulamasını güncelleştirin, ancak var olan uygulama ayarlarınızı koruyun. *Bu seçenek, uygulama güncelleştirmeleri için önerilen seçenektir.*
    - **Uygulamanın başka bir kopyasını yeni bir çalışma alanına yükleyin** – Yeni bir çalışma alanı oluşturun ve içinde var olan şablon uygulamasının bir kopyasını oluşturun. Varolan çalışma alanı dokunulmayacak şekilde bırakılacak.

1. Güncelleştirme seçeneklerinden birini belirleyin ve sonra **Yükle**'yi seçin.
1. Sol bölmedeki **Uygulamalar**'ı seçip ardından uygulamayı seçerek yüklü uygulamayı açın.
1. **Bağlan**'ı seçerek, uygulamayı veri kaynağınıza bağlayın. Uygulamayı daha önce yüklediyseniz, sarı ileti çubuğunda **Verilerinizi bağlayın**'ı seçin.
1. Aşağıdaki alanları ayarlayın.

    | Alan | Değer |
    |---|---|
    | Sunucu | [Azure Synapse workspace oluşturduktan](#serverlessep) sonra not aldığınız sunucusuz SQL uç noktasını girin. |
    | Veritabanı | **CommerceAnalytics** girin. |
    | Dil | Listede bir değer seçin. Bu alan, yerelleştirilmiş ürün ve kategori adları için kullanılır. Değer, büyük/küçük harf duyarlıdır. |
    | Tarih Aralığı | Listede bir değer seçin. Seçilen ay sayısı için veriler, Power BI veri kümesine aktarılır. Seçtiğiniz değer, veri kümesinin boyutunu ve eşitleme için gereken zamanı etkiler. |

1. **Sonraki**'yi seçin. Azure Synapse SQL veri tabanına bağlanmak için kimlik bilgilerini girmeniz istendiğinde, alan değerlerini aşağıdaki tabloda gösterildiği şekilde belirleyin.

    | Alan | Değer |
    |---|---|
    | Kimlik doğrulama yöntemi | **Temel**'i seçin. |
    | Kullanıcı adı | **reportreadonlyuser** girin. |
    | Parola | [Anahtar kasasında SQL salt okunur kullanıcı için sakladığınız](#roUser) parolayı girin. |

1. **Oturum aç ve bağlan**'ı seçin.
1. Veri kümesi başarıyla güncellenene kadar bekleyin. Sonra , veri kümesinin güncelleştirme durumunu görüntüleyebileceğiniz uygulama çalışma alanını açmak için **Uygulamayı düzenle** öğesini seçin. Uygulama çalışma alanında, isteğe bağlı olarak veri kümeniz için otomatik güncelleştirme zamanlamaları ayarlayabilir, izinleri yönetebilir ve uygulama örneğini yeniden adlandırabilirsiniz.

### <a name="privacy"></a><a name="privacy"></a>Gizlilik

Gizliliğiniz bizim için önemlidir. Daha fazla bilgi için [Gizlilik Bildirimimizi](https://go.microsoft.com/fwlink/?LinkId=521839) okuyun.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
