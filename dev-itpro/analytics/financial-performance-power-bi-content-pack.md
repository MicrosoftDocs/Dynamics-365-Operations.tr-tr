---
title: "Mali Performans Power BI içeriği"
description: "Bu konu, Microsoft Power BI için Microsoft Dynamics 365 for Operations Mali Performans içerik paketini açıklar. İçerik paketine dahil edilen pano ve raporlarını da açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
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

# <a name="financial-performance-power-bi-content"></a>Mali Performans Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu, Microsoft Power BI için Microsoft Dynamics 365 for Operations Mali Performans içerik paketini açıklar. İçerik paketine dahil edilen pano ve raporlarını da açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik paketine erişmek
--------------------------

Mali Performans içerik paketinin iki sürümü kullanılabilir. Bir sürüm Microsoft Dynamics Lifecycle Services (LCS), diğeri de PowerBI.com'da bulabilir.

-   **LCS'den kullanılabilir sürüm:** LCS'den kullanılabilen Mali Performans içerik paketi, Microsoft Dynamics 365 for Operations sürüm 1611'i destekler. İçerik paketini LCS içerisindeki Paylaşılan varlık kütüphanesinde bulabilirsiniz. İçerik paketini indirmek ve Microsoft Dynamics 365 for Operations verinize bağlamak hakkında daha fazla bilgi için bkz. [Microsoft ve ortaklarınızdan LCS içerisindeki Power BI içeriği](power-bi-content-microsoft-partners.md).
-   **PowerBI.com'da kullanılabilir sürüm:** PowerBI.com'da kullanılabilen Mali Performans içerik paketi, Microsoft Dynamics AX sürümleri 7.0 ve 7.0.1'i destekler. Dynamics 365 for Operations verinizi yüklemek ve bağlamak hakkında daha fazla bilgi için bkz. [Power BI içeriğine PowerBI.com'dan erişin](power-bi-home-page.md).

## <a name="main-account-setup"></a>Ana hesap kurulumu
Kuruluşlar borçlar ve gelirlerin raporlarda pozitif tutarlarda görünmesini istedikleri için ana hesapların Dynamics 365 for Operations içerisindeki kurulumu önemlidir. Bu ana hesapların pozitif tutarlarda görünmesi için, ana hesap türü **Pasif** veya **Gelir** olarak ayarlanmalıdır. Bu hesap türleri kullanıldığında, Microsoft Power BI aracılığıyla gerçekleştirilen raporlama işaretleri ters çevirir ve tutarları pozitif gösterir.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan panolar ve raporlar
İçerik paketini Dynamics 365 for Operations verinize bağladıktan sonra, pano ve raporlar mali verilerinizi gösterir. Daha önce hiç Power BI kullanmadıysanız, daha fazla bilgiyi şuradan edinin: [Power BI için Destekli Öğrenme sayfası](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Pano, altta yatan raporlara dayanan özetlenmiş veri kutucukları içerir. Her bir kutucuk, bir kuruluştaki tüm şirketlerdeki mevcut yılın özetlenmiş bilgilerini içerir. Kutucuklara bir kaç örnek:

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

Her bir kutucuk bir destek raporu tarafından desteklenmektedir. Bu raporlar çoğu zaman daha fazla bilgi sağlayan grafik ve tablolar içermektedir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                      | Raporların içerdiği bilgiler                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nakit Analizi               | Tüzel varlığa göre nakit, çeyreğe göre nakit, toplam nakit ve hesaba göre nakit **Not:** **Çeyreğe göre nakit** raporu, toplamdaki başlangıç bakiyelerini ilk çeyrekte dahil etmez. Her çeyrekte deftere nakledilen yeni hareketlerin toplamını gösterir.                                                                                |
| Mevcut Oran Analizi      | Tüzel kişiliğe göre mevcut oran, çeyreğe göre mevcut oran ve mevcut kıymetler ve borçlar için bilanço                                                                                                                                                                                                                              |
| Hızlı Oran Analizi        | Tüzel kişiliğe göre hızlı oran, çeyreğe göre hızlı oran ve nakit, alacak hesapları ve mevcut borçlar için bilançolar                                                                                                                                                                                                                      |
| Satılan Malların Maliyeti Analizi | Tüzel kişiliğe göre Satılan malın maliyeti (SMM), bu yılki ve geçen çeyreğe göre SMM, tüzel kişiliğe satışların SMM'si, toplam SMM ve SMM'nin satışa oranı                                                                                                                                                                                   |
| İşletme Sermayesi Analizi    | Tüzel kişiliğe göre işletme sermayesi, çeyreğe göre işletme sermayesi, mevcut kıymetler, mevcut varlıklar ve toplam işletme sermayesi                                                                                                                                                                                                                   |
| Kıymet ve Borç Analizi     | Tüzel varlığa göre toplam varlık getirisi ve toplam kıymetler borcu, çeyrekten bu güne toplam kıymetlere göre borç ve kıymetleri toplam getirisi, kıymetler ve borçlar                                                                                                                                                                                     |
| Kar Marjı Analizi      | Tüzel kişiliğe göre gerçek ve bütçe kar marjı, çeyreğe göre kar marjı, kar marjı oranı ve kar marjı                                                                                                                                                                                                                       |
| Net Gelir Analizi         | Tüzel kişiliğe göre gerçek ve bütçe net geliri, bu yıl ve geçen yılki net gelir ve masrafların net gelire oranı                                                                                                                                                                                                                       |
| Kazanç Analizi           | Tüzel kişiliğe göre vergi ve faiz öncesi gerçek ve bütçe kazançları (EBIT), bu yıl ve geçen yılki EBIT, giderlerin gelire oranı, gerçek ve bütçe giderlerinin gelirlere oranı                                                                                                                                                          |
| Gelir Analizi            | Toplam gelir, tüzel kişiliğe göre gerçek ve bütçe toplam geliri, bu yıl ve geçen yılki toplam gelir, tüzel kişiliğe göre gelir bütçe farkı, bu dönem ve geçen dönem toplam gelir                                                                                                                                                 |
| Gider Analizi            | Toplam giderler, tüzel kişiliğe göre gerçek ve bütçe toplam giderleri, çeyreğe göre gerçek ve bütçe toplam giderleri, hesap kategorisine göre toplam giderler ve faaliyet giderleri oranı                                                                                                                                                                 |
| Faturalandırılmış Gelir Analizi     | Toplam alacak hesapları, tüzel varlığa göre toplam alacak hesapları, çeyreğe göre toplam alacak hesapları ve alacak hesapları hesaplarının bakiyeleri **Not:** Raporlar alacak hesapları genel muhasebe hesaplarının başlangıç bakiyelerini içermez. Alacak hesaplarına nakledilen yeni hareketleri gösterirler. |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Mali Performans içerik paketindeki panoları ve raporları dolduran veriler, Dynamics 365 for Operations verileridir. İçerik paketinin temeli olarak kullanılan varlıklar aşağıdakilerdir: **Toplanan veri varlıkları**

-   **GeneralLedgerActivities** – Bu varlık, genel muhasebe bakiyelerini hesap kategorisine göre toplar.
-   **BudgetActivities** – Bu varlık, bütçe bakiyelerini hesap kategorisine göre toplar.

**Veri varlıkları**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Genel muhasebe defterleri
-   ChartofAccounts

Bu varlıklar, veri modelinde hesaplanmış ölçümler oluşturmak için kullanılıyordu. Hesaplanmış ölçümler, anahtar performans göstergeleri (KPI'ları) hesaplamak ve içerik paketinde kullanıla raporları hesaplamakta kullanılır. İçerik paketi varsayılan olarak son üç yılın ve gelecekteki bir yılın verilerini getirir. Raporlara ve panoya ek hesaplamalar dahil etmek için [Microsoft Excel çalışma kitabı](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)'nı değiştirebilirsiniz. Bu çalışma kitabı, içerik paketini oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yapmayı bitirdikten sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](..\data-entities\data-entities.md)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](configure-power-bi-integration.md)





