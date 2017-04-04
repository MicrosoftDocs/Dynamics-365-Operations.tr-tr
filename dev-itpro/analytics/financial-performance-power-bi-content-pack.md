---
title: "Finansal performans Güç BI içeriği"
description: "Bu konu Microsoft Power BI için finansal işlemleri performans içerik paketi Microsoft Dynamics 365 açıklar. Pano ve içerik paketinde bulunan raporlar açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Finansal performans Güç BI içeriği

Bu konu Microsoft Power BI için finansal işlemleri performans içerik paketi Microsoft Dynamics 365 açıklar. Pano ve içerik paketinde bulunan raporlar açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik Paketi erişme
--------------------------

Finansal performans içerik paketi iki sürümlerinde kullanılabilir. Microsoft Dynamics ömrü Hizmetleri (LCS) bir sürüm kullanılabilir ve diğer PowerBI.com kullanılabilir.

-   **LCS kullanılabilir sürüm:** LCS kullanılabilir içerik paketi finansal performans 1611 işlemleri sürümü için Microsoft Dynamics 365 destekler. LCS Shared kıymet kitaplığında içerik paketi bulabilirsiniz. İçerik paketini karşıdan yüklemek ve veri işlemleri için Microsoft Dynamics 365 bağlanma hakkında daha fazla bilgi için bkz: [Microsoft ve ortaklarınız LCS içeriğinde güç BI](power-bi-content-microsoft-partners.md).
-   **PowerBI.com kullanılabilir sürüm:** PowerBI.com kullanılabilir finansal performans içerik paketi Microsoft Dynamics AX sürüm 7.0 ve 7.0.1 destekler. Bağlanmak ve veri işlemleri için Dynamics 365 yüklemek hakkında daha fazla bilgi için bkz: [PowerBI.com içeriği erişim güç BI](power-bi-home-page.md).

## <a name="main-account-setup"></a>Ana hesap kurulumu
Kur ana hesapların işlemleri için Dynamics 365, kuruluşların Borçlar ve gelir tutarlarını raporlarda pozitif tutarlar olarak görünmesini istediğiniz için önemlidir. Bu ana hesaplar için pozitif tutarlar görünmesi ana hesap türünü ayarlamak **SORUMLULUĞUN** veya **gelir**. Bu hesap türleri kullanıldığında, Microsoft güç BI raporlama işaretleri ters ve pozitif olarak tutarları gösterir.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Pano ve içerik paketinde bulunan raporlar
İçerik paketini Dynamics 365 for Operations verinize bağladıktan sonra, pano ve raporlar mali verilerinizi gösterir. Güç BI önce hiç kullanmadıysanız, daha fazla bilgi üzerinde öğrenebilirsiniz [BI güç destekli öğrenme sayfasını](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Pano, altta yatan raporlara dayanan özetlenmiş veri kutucukları içerir. Her bir kutucuk, bir kuruluştaki tüm şirketlerdeki mevcut yılın özetlenmiş bilgilerini içerir. Döşeme bazıları şunlardır:

-   Nakit
-   Bu yılki Toplam Gelir
-   Bu yılki Toplam Gider
-   Bu yılki Net Gelir
-   Hızlı Oran
-   Hesap kategorisine göre bu yılki Toplam Giderler
-   Cari Oran
-   Toplam Varlıklara Göre Borç
-   Gerçek ve Tahmini Gelir kıyaslaması
-   Bu yılki Faturalanmış Gelir
-   Bu yılki İşletim giderleri Oranı
-   Bu yılki Kar Marjı
-   Gerçek ve Bütçe Giderleri karşılaştırması - Tüm şirketler

Her döşeme destekleyen bir rapor tarafından desteklenmektedir. Bu raporlar çoğu zaman daha fazla bilgi sağlayan grafik ve tablolar içermektedir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                      | Raporların içerdiği bilgiler                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nakit Analizi               | Tüzel kişilik, üç aylık nakit, toplam nakit ve nakit hesabına göre nakit **Not:****üç aylık nakit** rapor içermez başına bakiyeleri toplama ilk üç ay için. Bu, her üç aylık dönemde deftere nakledilen yeni hareketler toplamı gösterilir.                                                                                |
| Mevcut Oran Analizi      | Tüzel kişiliğe göre mevcut oran, çeyreğe göre mevcut oran ve mevcut kıymetler ve borçlar için bilanço                                                                                                                                                                                                                              |
| Hızlı Oran Analizi        | Hızlı oranı tüzel kişilik tarafından üç aylık dönem ve bakiyeleri, paraya göre hızlı oranı geçerli alacak ve Borçlar hesapları                                                                                                                                                                                                                      |
| Satılan Malların Maliyeti Analizi | Tüzel kişiliğe göre Satılan malın maliyeti (SMM), bu yılki ve geçen çeyreğe göre SMM, tüzel kişiliğe satışların SMM'si, toplam SMM ve SMM'nin satışa oranı                                                                                                                                                                                   |
| İşletme Sermayesi Analizi    | Tüzel kişiliğe göre işletme sermayesi, çeyreğe göre işletme sermayesi, mevcut kıymetler, mevcut varlıklar ve toplam işletme sermayesi                                                                                                                                                                                                                   |
| Kıymet ve Borç Analizi     | Tüzel varlığa göre toplam varlık getirisi ve toplam kıymetler borcu, çeyrekten bu güne toplam kıymetlere göre borç ve kıymetleri toplam getirisi, kıymetler ve borçlar                                                                                                                                                                                     |
| Kar Marjı Analizi      | Tüzel kişiliğe göre gerçek ve bütçe kar marjı, çeyreğe göre kar marjı, kar marjı oranı ve kar marjı                                                                                                                                                                                                                       |
| Net Gelir Analizi         | Tüzel kişiliğe göre gerçek ve bütçe net geliri, bu yıl ve geçen yılki net gelir ve masrafların net gelire oranı                                                                                                                                                                                                                       |
| Kazanç Analizi           | Tüzel kişiliğe göre vergi ve faiz öncesi gerçek ve bütçe kazançları (EBIT), bu yıl ve geçen yılki EBIT, giderlerin gelire oranı, gerçek ve bütçe giderlerinin gelirlere oranı                                                                                                                                                          |
| Gelir Analizi            | Toplam gelir, tüzel kişiliğe göre gerçek ve bütçe toplam geliri, bu yıl ve geçen yılki toplam gelir, tüzel kişiliğe göre gelir bütçe farkı, bu dönem ve geçen dönem toplam gelir                                                                                                                                                 |
| Gider Analizi            | Toplam giderler, tüzel kişiliğe göre gerçek ve bütçe toplam giderleri, çeyreğe göre gerçek ve bütçe toplam giderleri, hesap kategorisine göre toplam giderler ve faaliyet giderleri oranı                                                                                                                                                                 |
| Faturalandırılmış Gelir Analizi     | Alacak hesapları toplamı, toplam tüzel kişilik tarafından hesapları, toplam üç aylık dönemlere göre Alacak hesapları ve Alacak hesapları hesaplarının bakiyelerini **Not:** raporları hesapları alacağı genel muhasebe hesaplarının bakiyeleri başlayan eklemeyin. Bunlar, alacak hesaplarına nakledilen yeni hareketlerinin toplamını gösterir. |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Pano ve raporlarda finansal performans içerik paketi dolduran Dynamics 365 işlemleri için veri veridir. İçerik Paketi için temel olarak kullanılan aşağıdaki varlıklar: **toplama veri varlıkları**

-   **GeneralLedgerActivities** – bu varlık tarafından hesap kategorisi genel muhasebe bakiyelerini toplar.
-   **BudgetActivities** – bu varlık tarafından hesap kategorisinin bütçe bakiyeleri toplar.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Genel muhasebe defterleri
-   ChartofAccounts

Bu varlıklar, hesaplanmış ölçüler veri modelleri oluşturmak için kullanılıyordu. Anahtar performans göstergeleri (APG) hesaplamak için kullanılan hesaplanmış ölçüler ve içerik paketinde kullanılan raporlar. İçerik paketi varsayılan olarak son üç yılın ve gelecekteki bir yılın verilerini getirir. Raporlara ve panoya ek hesaplamalar dahil etmek için [Microsoft Excel çalışma kitabı](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)'nı değiştirebilirsiniz. Bu çalışma kitabı, içerik paketini oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yapmayı bitirdikten sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)



