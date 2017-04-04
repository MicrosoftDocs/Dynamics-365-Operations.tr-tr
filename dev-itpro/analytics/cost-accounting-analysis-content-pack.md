---
title: "Maliyet muhasebesi analiz güç BI içeriği"
description: "Bu konu güç BI içeriği Maliyet muhasebesi analiz nelerin dahil edileceğini açıklar. Güç BI raporlara erişimi açıklar ve içerik oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Maliyet muhasebesi analiz güç BI içeriği

Bu konu güç BI içeriği Maliyet muhasebesi analiz nelerin dahil edileceğini açıklar. Güç BI raporlara erişimi açıklar ve içerik oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar.

<a name="overview"></a>Özet
--------

**Maliyet muhasebesi analiz** Microsoft Power BI içeriği maliyet denetleyicileri veya bir kuruluşun Maliyet kontrolü yapmaktan sorumlu olan herkes için tasarlanmıştır. Bu maliyet, büyüklük ve fiili maliyeti, bütçe maliyeti ve esnek bütçe maliyeti Maliyet oranı gibi anahtar ölçümleri içerir. Bu hareketin maliyet muhasebesi verileri Microsoft Dynamics 365 içinde işlemler için kullanır ve bir raporlama para birimi cinsinden tüm organizasyon için maliyetleri toplam görünümünü sağlar. Birkaç tüzel kurum olabilir olsa bile yöneticileri kendi kuruluş birimleri maliyet denetimi gerçekleştirmek için maliyet nesneler tarafından verilere filtre uygulayabilirsiniz. Çünkü **Maliyet muhasebesi analiz** güç BI İçerik yöneticileri kendi operasyonel birimleri için pozitif ve negatif eğilimleri hakkında bildirilebilir bütçe maliyetlerini ve fiili maliyetler arasındaki farkları vurgular. Yöneticileri nasıl maliyet farklarını ortaya çıkan ve etkili önlem ayrıntılı bilgiler elde etmek için maliyet öğesi hiyerarşileri veya öğeleri tek tek maliyet aşağı inebilir. **Maliyet muhasebesi analiz** güç BI maliyet muhasebeci analiz yapalım maliyet tüm kuruluş maliyeti nesneler arasında nasıl akacağını içerik. Maliyet muhasebesi hakkında daha fazla bilgi için bkz: [Maliyet muhasebesi giriş sayfası](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Maliyet muhasebesinde erişim düzeyi güvenlik tanımlama ve güç BI satır düzeyi güvenliği ile birleştirerek, tüm maliyet nesne sahipleri erişim izni verebilirsiniz **Maliyet muhasebesi analiz** güç BI içeriği. Tüm verileri görsel sonra temel maliyet muhasebesinde denetlenen erişim düzeyi üzerinde filtre edilir. Erişim düzeyi güvenliği ve satır düzeyi güvenliği hakkında daha fazla bilgi için bkz: [için güç BI Maliyet muhasebesi içerik için güvenlik kurma](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Güç BI içeriğine erişerek
Bulabilirsiniz **Maliyet muhasebesi analiz** güç BI içeriğinde paylaşılan varlıkları kitaplığı Microsoft Dynamics ömrü Hizmetleri (LCS). İçeriği karşıdan yüklemek ve, Dynamics 365 işlemler veri bağlama hakkında daha fazla bilgi için bkz: [Microsoft ve ortaklarınız LCS içeriğinde güç BI](power-bi-content-microsoft-partners.md). **Not:** KB4011327 ** ** için bir önkoşuldur **Maliyet muhasebesi analiz** güç BI içeriği.  Yaşam döngüsü hizmetlerine oturum açtıktan sonra burada KB erişebilirsiniz: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Güç BI içeriğinde bulunan ölçümleri
İçerik rapor sayfaları kümesi içerir. Her sayfa, grafikler, döşeme ve tablo görünür ölçümler kümesinden oluşur. Aşağıdaki tabloda görsel bir bakış sağlar **Maliyet muhasebesi analiz** güç BI içeriği.

| Rapor sayfası                      | Grafik                                                                                                                         | Kutucuk                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Mali Döneme göre maliyet kontrol    | Fiili Maliyet ve maliyet öğesi hiyerarşi düzeyi tarafından bütçe maliyeti                                                                   | Fiili Maliyet vs bütçe maliyeti                    |
|                                  | Maliyet öğesi hiyerarşi düzeyi tarafından bütçe farkı                                                                               | Fiili Maliyet oranı vs Bütçe maliyet fiyatı          |
|                                  | İlk 10 öğe maliyeti yüzde cinsinden bütçe farkı                                                                          | Gerçek büyüklük vs bütçe büyüklüğü          |
| Yıl başından bugüne göre maliyet kontrol     | Fiili Maliyet ve Takvim yılı döneme göre bütçe maliyeti                                                                           | Fiili Maliyet vs bütçe maliyeti                    |
|                                  | Takvim yılı döneme göre bütçe farkı                                                                                       | Fiili Maliyet oranı vs Bütçe maliyet fiyatı          |
|                                  | İlk 10 öğe maliyeti yüzde cinsinden bütçe farkı                                                                          | Gerçek büyüklük vs bütçe büyüklüğü          |
| Mali yıla göre maliyet fiyatı         | Gerçek maliyet oranı maliyet davranışı tarafından                                                                                             | Fiili Maliyet oranı vs Bütçe maliyet fiyatı          |
|                                  | Gerçek maliyet oranı maliyet oranı farkı bütçe, Bütçe Maliyet oranı yüzde ve maliyet öğesi hiyerarşi düzeyi tarafından Bütçe Maliyet oranı | Gerçek büyüklük vs bütçe büyüklüğü          |
|                                  | Maliyet öğesi hiyerarşi düzeyi tarafından bütçe farkı                                                                               |                                               |
|                                  | İlk 10 öğe maliyeti yüzde cinsinden bütçe farkı                                                                          |                                               |
| Esnek bütçe mali döneme göre | Fiili maliyeti, Bütçe maliyet ve maliyet öğesi hiyerarşi düzeyi tarafından esnek bütçe maliyeti                                             | Gerçek büyüklük vs bütçe büyüklüğü          |
|                                  | Bütçe farkı ve maliyet öğesi hiyerarşi düzeyi tarafından esnek bütçe farkı                                                  | Fiili Maliyet vs esnek bütçe maliyeti           |
|                                  | Fiili maliyeti, bütçe maliyeti ve esnek maliyet yana davranış maliyet ve maliyet öğesi hiyerarşi düzeyi                                  | Gerçek maliyet oranı vs esnek bütçe maliyet oranı |
| Mali Döneme göre Maliyet raporu  | Fiili Maliyet Maliyet öğesi hiyerarşi düzeyi ve maliyet nesne boyut üye adı                                             |                                               |
|                                  | Fiili Maliyet Maliyet nesne boyut üye adı ve maliyet öğesi boyut üye adı                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 işlemleri veriler için rapor sayfaları doldurmak için kullanılan **Maliyet muhasebesi analiz** güç BI içeriği. Bu veriler hazırlanır toplama ölçümleri temsil varlık deposunda olduğu analytics için en iyi duruma getirilmiş bir Microsoft SQL veritabanı. Daha fazla bilgi için bkz: [varlık deposu ile tümleştirme güç genel bakış BI](power-bi-integration-entity-store.md). Aşağıdaki anahtar toplama ölçümleri temel olarak kullanılır.

| Varlık                  | Anahtar toplama ölçüm | Dynamics 365 işlemleri için veri kaynağı | Alan     | Açıklama                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Maliyet muhasebesi girişleri | SUM(amount)               | CAMDATAAggregatedCostEntry                  | Tutar    | Maliyet muhasebesinin muhasebe para birimi cinsinden tutar |
| İstatistiksel girişler     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry           | Büyüklük |                                               |

Aşağıdaki tabloda anahtar toplam ölçüleri birkaç hesaplanmış ölçüler içinde içeriğin dataset oluşturmak için nasıl kullanıldığını gösterir.

| Ölçü                                       | Ölçü birimi nasıl hesaplanır                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Gerçek maliyet                                   | Hesapla ('maliyet muhasebesi Girişleri'\[ölçü birimi\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_değer\] = 0)            |
| Bütçe maliyeti                                   | Hesapla ('maliyet muhasebesi Girişleri'\[ölçü birimi\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_değer\] = 1)            |
| Bütçe maliyet farkı                          | \[Bütçe maliyeti\] - \[gerçek maliyet\]                                                                                      |
| Bütçe farkı yüzdesi                    | IF (\[bütçe maliyeti\] = 0, blank(), \[bütçe farkı\] / \[bütçe maliyeti\])                                                |
| Gerçek büyüklük                              | Hesapla ('İstatistik Girişleri'\[FullMagnitude\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_değer\] = 0)          |
| Bütçe büyüklüğü                              | Hesapla (\[FullMagnitude\], 'Hareket sürümleri'\[ISSOURCEVERSIONBUDGET\_değer\] = 1)                               |
| İstatistiksel bütçe farkı                   | \[Bütçe büyüklüğü\] - \[gerçek büyüklük\]                                                                            |
| İstatistiksel bütçe farkı yüzdesi        | IF (\[bütçe büyüklüğü\] = 0, blank(), \[istatistiksel bütçe farkı\] / \[bütçe büyüklüğü\])                          |
| Gerçek maliyet oranı                              | IF (\[gerçek büyüklük\] = 0, BLANK(), \[fiili maliyeti\] / \[gerçek büyüklük\])                                          |
| Bütçe maliyet oranı                              | IF (\[bütçe büyüklüğü\] = 0, BLANK(), \[bütçe maliyeti\] / \[bütçe büyüklüğü\])                                          |
| Bütçe Maliyet oranı farkı                     | \[Bütçe Maliyet oranı\] - \[gerçek maliyet oranı\]                                                                            |
| Bütçe Maliyet oranı farkı yüzdesi          | IF (\[bütçe maliyeti\] = 0, blank(), \[bütçe maliyeti oranı farkı\] / \[Bütçe Maliyet oranı\])                                 |
| Sabit bütçe maliyeti                             | Hesapla (\[bütçe maliyeti\], 'maliyet muhasebe girişleri'\[COSTBEHAVIOR\] = 1)                                              |
| Değişken bütçe maliyeti                          | Hesapla (\[bütçe maliyeti\], 'maliyet muhasebe girişleri'\[COSTBEHAVIOR\] = 2)                                              |
| Sabit esnek bütçe maliyeti                    | \[Sabit bütçe maliyeti\]                                                                                                  |
| Değişken esnek bütçe maliyeti                 | IF (\[bütçe büyüklüğü\] = 0, BLANK(), (\[değişken bütçe maliyeti\] / \[bütçe büyüklüğü\]) \*\[gerçek büyüklük\])       |
| Esnek bütçe maliyeti                          | \[Esnek bütçe maliyeti sabit\] + \[değişken esnek bütçe maliyeti\]                                                     |
| Esnek bütçe farkı                      | \[Esnek bütçe maliyeti\] - \[gerçek maliyet\]                                                                             |
| Esnek bütçe farkı yüzdesi           | IF (\[esnek bütçe maliyeti\] = 0, BLANK(), \[esnek bütçe farkı\] / \[esnek bütçe maliyeti\])                     |
| Esnek Bütçe Maliyet oranı                     | IF (\[gerçek büyüklük\] = 0, BLANK(), \[esnek bütçe maliyeti\] / \[gerçek büyüklük\])                                 |
| Esnek Bütçe Maliyet oranı farkı            | \[Esnek Bütçe Maliyet oranı\] - \[gerçek maliyet oranı\]                                                                   |
| Esnek Bütçe Maliyet oranı farkı yüzdesi | IF (\[esnek bütçe maliyet oranı\] = 0, BLANK(), \[esnek bütçe maliyet oranı farkı\] / \[esnek bütçe maliyet oranı\]) |

Aşağıdaki anahtar boyutları daha parçalı yapı elde etmek ve daha derin analitik incelemeler sağlamak için toplam ölçüleri dilim için filtre olarak kullanılır.

| Varlık                             | Öznitelik örnekleri                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Maliyet muhasebesi defterleri            | Maliyet muhasebesi defteri                                                                                               |
| Maliyet kontrolü birimleri                 | Maliyet kontrolü birimi adı                                                                                               |
| Maliyet öğesi boyutları            | Maliyet öğeler boyut adı, maliyet öğesi boyut üye adı, maliyet öğesi boyut üye açıklaması          |
| Maliyet nesnesi boyutları             | Maliyet nesne boyut adı, nesne boyut üye adı maliyet, maliyet nesne boyut üye açıklaması              |
| İstatistiksel boyutlar             | İstatistiksel boyut adı, istatistiksel boyut üye adı, istatistiksel boyut üye açıklaması              |
| Boyut hiyerarşileri maliyet nesnesi  | Nesne boyut hiyerarşi adı maliyet, maliyet nesne boyut hiyerarşi ağacı nesne boyut hiyerarşi düzeyi Maliyet    |
| Boyut hiyerarşileri öğe maliyeti | Öğenin boyut hiyerarşi adı maliyet, maliyet öğesi boyut hiyerarşisi ağaç öğesi boyut hiyerarşi düzeyi Maliyet |
| İstatistiksel boyut hiyerarşileri  | İstatistiksel boyut hiyerarşi adı, istatistiksel boyut hiyerarşi düzeyi, istatistiksel boyut hiyerarşi ağacı    |
| Hareket sürümleri               | Sürüm adı                                                                                                         |
| Mali takvimler                   | Takvim, Takvim açıklaması                                                                                       |
| Mali yıl                       | Takvim yılı                                                                                                        |
| Mali dönemler                     | Takvim yılı dönem                                                                                                 |

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)
-   [Güç BI için maliyet muhasebesi içerik için güvenlik kurma](setup-security-cost-accounting-content-pack.md)


