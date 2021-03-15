---
title: Satıcı fatura girişi çalışma alanı
description: Bu konu, satıcı faturalarıyla ilgili çalışma alanının nasıl ayarlanacağını ve Microsoft Power BI üzerinden kullanılabilen bilgileri gösterir.
author: abruer
manager: AnnBe
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2020-09-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 04aca717c3f255799699d63fb74ee0b543f8c8ba
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993275"
---
# <a name="vendor-invoice-entry-workspace"></a>Satıcı fatura girişi çalışma alanı

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konu, satıcı faturalarıyla ilgili çalışma alanının nasıl ayarlanacağını ve Microsoft Power BI üzerinden kullanılabilen bilgileri gösterir. Bu çalışma alanındaki satıcı faturası bilgileri belirli kullanıcılar için filtrelenmiştir ve grafik biçiminde görüntülenir.

## <a name="overview"></a>Genel bakış

**Satıcı faturası girişi** çalışma alanı satıcı faturasının işlenmesiyle ilgili bilgileri gösterir. Bir **İşim** görünümü ve bir **Analiz - Tüm şirketler** sayfası içerir. **İşim** görünümü özet kutucuklarını, satıcı hareketi ızgaralarını ve ilgili satıcı bilgilerini gösterir. **Analiz - Tüm şirketler** sayfası, Power BI yeteneklerini, satıcı faturalarıyla ilgili görselleri göstermek için kullanır.

## <a name="set-up-the-workspace-to-show-power-bi-content"></a>Çalışma alanını Power BI içeriğini gösterecek şekilde ayarlama

**Satıcı fatura girişi** çalışma alanındaki Power BI görsel öğelerde verilerin gösterilebilmesi için önce bu kurulumu tamamlamanız gerekir.

1. **Özellik Yönetimi** çalışma alanında, **satıcı faturası Otomasyonu** özelliğini bulmak için listeyi filtreleyin.
3. **Şimdi etkinleştir**'i seçin.
4. Faturaların el ile müdahale gerektirmeden baştan sona işlendiğinden emin olmak için bir satıcı faturası iş akışı ayarlayın. İş akışı ayarlamak için **Borç hesapları \> Kurulum \> Borç hesapları iş akışları**'na gidin.
5. **Borç hesapları \> Kurulum \> Borç hesapları parametreleri** bölümüne gidin ve **satıcı fatura Otomasyonu** sekmesini seçin. Daha fazla bilgi için bkz [Satıcı faturası otomasyonu için seçenekler ayarlama](vnd-invoice-set-up-options.md).
6. **İçe aktarılan faturaları otomatik olarak iş akışına gönder** seçeneğini **Evet** olarak ayarlayın.
7. Ürün fişleri otomatik olarak eşleştirilmeli ise, **ürün fişlerini fatura satırlarıyla otomatik olarak eşle** seçeneğini **Evet** olarak ayarlayın.
8. Kalan, isteğe bağlı ayarları inceleyin ve kuruluşunuzun gereksinimlerine göre konfigüre edin.
9. **Sistem para birimi** ve **Sistem döviz kuru** alanlarını ayarlamak için **Sistem yönetimi \> Kurulum \> Sistem Paramatreleri**'ne gidin.
10. **Genel Muhasebe \> Ayarlar \> Muhasebe**'ye gidin ve **Muhasebe Para Birimi** ve **Döviz Kuru Türü**'nü ayarlayın.
11. **Genel muhasebe \> Para birimi \> Döviz kurları**'na gidin ve işlem para birimi ile hesap para birimi arasındaki ve hesap para birimi ile sistem para birimi arasındaki döviz kurlarını girin.
12. **Sistem Yönetimi \> Kurulum \> Varlık deposuna** gidin ve **satıcı faturası Otomasyon ölçümünü** arayın. **Yenile**'yi seçin.

Çalışma alanında görüntülenen bilgileri görüntülemek için borç hesapları yöneticisi veya borç hesapları memuru güvenlik rolüne sahip olmanız gerekir.

## <a name="my-work-view"></a>İşim görünümü

### <a name="company-selection"></a>Şirket seçimi

**Otomasyon satıcı faturaları** özelliği açık olduğunda, çalışma alanının üst kısmında bir **şirket** alanı belirir. **Şirket** alanındaki seçim, çalışma alanında görüntülenen tüm bilgileri etkiler. Varsayılan olarak görünüm, oturum açmış olduğunuz şirketle ilgili bilgileri gösterir. **Şirket** alanında farklı bir şirket seçerek, o şirketle ilgili bilgileri çalışma alanında gösterebilirsiniz. Daha sonra, seçili şirketteki ilgili sayfaya gitmek için çalışma alanında bir kutucuk seçebilirsiniz.

### <a name="summary-tiles"></a>Özet kutucukları

**Çalışmam** görünümünün **bekleyen faturalar özetindeki** kutucuklar satıcı faturanız durumunun genel görünümünü verir. Henüz deftere nakledilmemiş günlükleri ve beklemedeki faturaları görebilirsiniz. Ayrıca, satıcı fatura Otomasyonu özelliğiyle ilişkili dört kutucuk vardır:

- El ile giriş eşleştirme gerekli
- Başarısız eşleştirme doğrulaması
- İş akışına gönderilmeyen faturalar
- İçeri aktarılmayan faturalar

(Bu dört kutucuk, satıcı fatura Otomasyonu özelliğinin özellik yönetiminde açık olmasını gerektirir.)

**Satıcı faturalarını kurtar** kutucuğunu kullanmak için, bu özelliğin borç hesapları parametrelerinde açık olması gerekir. **Borç hesapları \> borç hesapları parametrelerine** gidin ve **Fatura** sekmesinde, **satıcı faturası kurtarmaya izin ver** seçeneğini **Evet** olarak ayarlayın.

Özellik açık olduğunda, **günlük** adlı bir bölümde ayrıca çalışma alanında gruplandırılmış üç kutucuk görürsünüz. Kutucuklar, **Günlükler**, **Günlükler - Bana atananlar** ve **Fatura havuzu** olarak adlandırılmıştır. 

**Bekleyen faturalar Özeti** bölümündeki bilgiler, oturum açma işlemi için varsayılan şirket olarak ayarlanan şirket içindir.

### <a name="creating-new-records"></a>Yeni kayıtlar oluşturma

Yeni bir fatura kaydı oluşturmak için, **Yeni**'yi seçin ve sonra listede aşağıdaki kayıt türlerinden birini seçin:

- Satıcı faturası
- Fatura günlüğü
- Genel fatura günlüğü
- Fatura defteri
- Fatura onayı

Oluşturduğunuz kaydın, oturum açmış olduğunuz şirketi değil şirket filtresini temel aldığına dikkat edin. Örneğin, **UMSF** şirketinde oturum açtınız, ancak şirket filtresi **GBSI** olarak ayarlıdır. Bu durumda, **yeni**'yi seçip sonra listede bir kayıt türü seçtiğinizde, kayıt GBSI şirketinde oluşturulur.

### <a name="documents-not-invoiced-grids"></a>Faturalanmamış belgeler ızgaraları

**Faturalanmamış belgeler** bölümü, satıcı faturalarını bekleyen belgeleri gösteren ızgaralar içerir.

**Açık satınalma siparişleri** ızgarası, henüz tam olarak faturalanmamış tüm satınalma siparişlerini gösterir. Bir satınalma siparişi için satıcı faturası oluşturmak üzere **şimdi Faturala** düğmesini kullanabilirsiniz. Bir satınalma siparişi için ön ödeme faturası oluşturmak üzere **Şimdi ön ödeme faturalandırması yap** düğmesini kullanabilirsiniz.

**Ürün girişleri** ızgarası, henüz tam olarak faturalanmamış tüm satınalma girişi işlemlerini gösterir. Bir satınalma siparişi için satıcı faturası oluşturmak üzere **şimdi Faturala** düğmesini kullanabilirsiniz.

**Bekleyen satıcı faturaları** ızgarası iş akışı sistemine gönderilmemiş olan tüm satıcı faturalarını gösterir. Belirli bir satıcı faturasını aramak için **arama** alanını ve/veya şirket filtresini kullanabilirsiniz. Izgarada görünen bir işlemi düzenlemek için **Düzenle** düğmesini kullanabilirsiniz.

**Satınalma siparişi bul** ızgarasında belirli bir satınalma siparişini aramak için **arama** alanını kullanabilirsiniz.

### <a name="related-information"></a>İlgili bilgiler

Çalışma alanının sağ tarafındaki bağlantıları kullanarak deftere nakledilen faturalar hakkındaki bilgileri görüntüleyebilirsiniz. Bu bağlantılar **Açık satıcı faturalarını**, **Fatura günlüğünü**, **fatura geçmişini ve eşleme ayrıntılarını** içerir. **Satıcılar** bölümünde, beklemede olan tüm satıcıları gösteren bir filtre uygulanmış listeye erişebilir veya **tüm satıcılar** bağlantısını kullanabilirsiniz. **Tüm satınalma siparişleri** ve **açık ön ödemeler** bağlantıları da kullanılabilir.

### <a name="analytics--all-companies-page"></a>Analizler – Tüm şirketler sayfası

**Borç hesapları parametreleri** sayfasında **içe aktarılan faturaları otomatik olarak iş akışına gönder** seçeneği **Evet** olarak ayarlandığında, Otomasyon Analizini görüntüleyebilirsiniz. **Analiz-tüm şirketler** sayfası, onaylayan kişi ve şirket tarafından onaylanan satıcı faturaları gibi önemli ölçümleri sağlar. Bu sayfa beş rapor sayfası içerir. Bir sayfa genel bakış sağlarken ve diğer sayfalar Borç hesapları ödeme otomasyon ölçümleri hakkında ayrıntılı bilgiler sağlar.

Aşağıdaki tablo, her bir rapor sayfasında kullanılabilen görselleştirmeleri gösterir.

| Rapor sayfası                    | Görselleştirme |
|--------------------------------|----------------|
| Satıcı faturası genel bakış        | <ul><li>Sistem para biriminde otomasyonda bekleyen satıcı faturaları</li><li>İçe aktarmanın başarısız olduğu faturalar</li><li>İş akışındaki faturalar</li><li>Son 30 günde temassız faturalar</li><li>Son 30 gündeki toplam otomatik faturalar</li><li>Sistem para birimi cinsinden açık faturaların bakiyesi</li><li>Başarısızlık nedenleri, son 30 gün</li><li>Otomatik olarak işlenen deftere nakledilmiş faturaların yüzdesi</li><li>Fatura işlemeye kalan günler</ul></li> |
| Otomasyon durumu              | <ul><li>Son 30 günde temassız faturalar</li><li>Son 30 günde şirkete ait temassız faturalar</li><li>Son 30 günde satıcı grubuna ait temassız faturalar</li><li>Otomatik olarak işlenen deftere nakledilmiş faturaların yüzdesi</li><li>Fatura işlemeye kalan günler</li></ul> |
| İçe aktarmanın başarısız olduğu faturalar | <ul><li>İçe aktarmanın başarısız olduğu faturalar</li><li>İçe aktarmanın başarısız olduğu şirkete ait faturalar</li></ul> |
| Otomasyon hatası nedenleri | <ul><li>Faturalar başarısız oldu</li><li>Şirkete ait başarısız olan faturalar</li><li>Satıcı grubuna ait başarısız olan faturalar</li></ul> |
| İş akışı durumu                | <ul><li>İş akışındaki faturalar</li><li>Satıcı fatura iş akışı örnekleri</li><li>Onaylayan başına atama</li><li>Şirket başına satıcı faturası iş akışı</li><li>Onaylana göre iş akışındaki ortalama gün sayısı</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]