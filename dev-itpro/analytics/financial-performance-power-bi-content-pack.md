---
title: "Mali performans Power BI içeriği"
description: "Bu konu, Mali performans Power BI içeriğini açıklar. Panoyu ve içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: kweekley
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: b20f526d20d357750777d0f9bda26e4d9d55b335
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="financial-performance-power-bi-content"></a>Mali performans Power BI içeriği

[!include[banner](../includes/banner.md)]

Bu konu, **Mali performans** Microsoft Power BI içeriğini açıklar. Panoyu ve içeriğe dahil edilen raporların nasıl kullanılacağını açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek

**Mali performans** Power BI içeriğine Microsoft Dynamics Lifecycle Services (LCS) üzerinden ve PowerBI.com'dan erişebilirsiniz.

### <a name="available-from-lcs"></a>LCS'den bulunabilir
LCS'den erişilebilir olan **Mali performans** Power BI içeriği, aşağıdaki sürümleri destekler:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition Temmuz 2017 güncelleştirmesi
- Microsoft Dynamics 365 for Operations sürüm 1611 

Power BI içeriğini LCS'deki Paylaşılan varlık kitaplığında bulabilirsiniz. İçerik paketini indirmek ve kuruluşunuzda tümleştirmek hakkında daha fazla bilgi için bkz. [Microsoft LCS ve iş ortaklarınızdan Power BI içeriği](power-bi-content-microsoft-partners.md). Power BI içeriğinin nasıl uygulanacağını gösteren bir demo izlemek için bakınız [Microsoft ve Dynamics Lifecycle Services ortaklarınızdan Power BI içeriği](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.

### <a name="available-from-powerbicom"></a>PowerBI.com'dan kullanılabilir
PowerBI.com'dan erişilebilir olan **Finansal performans** Power BI içeriği Microsoft Dynamics AX sürüm 7.0 ve 7.0.1'i destekler. Dynamics AX verinizi yüklemek ve bağlamak hakkında daha fazla bilgi için bkz. [Power BI içeriğine PowerBI.com'dan erişin](power-bi-home-page.md).

## <a name="main-account-setup"></a>Ana hesap kurulumu
Kuruluşlar borçlar ve gelirlerin raporlarda pozitif tutarlarda görünmesini istedikleri için ana hesapların kurulumu önemlidir. Bu ana hesapların pozitif tutarlarda görünmesi için, ana hesap türü **Pasif** veya **Gelir** olarak ayarlanmalıdır. Bu hesap türleri kullanıldığında, Power BI aracılığıyla gerçekleştirilen raporlama işaretleri ters çevirir ve tutarları pozitif gösterir.

## <a name="dashboard-and-reports-that-are-included-in-the-power-bi-content"></a>Power BI içerik paketinde bulunan panolar ve raporlar
Pano, altta yatan raporlara dayanan özetlenmiş veri kutucukları içerir. Her bir kutucuk, bir kuruluştaki tüm şirketlerdeki mevcut yılın özetlenmiş bilgilerini içerir. Kutucuklara bir kaç örnek:

- Nakit
- Bu yılki Toplam Gelir
- Bu yılki Toplam Gider
- Bu yılki Net Gelir
- Hızlı Oran
- Hesap kategorisine göre bu yılki Toplam Giderler
- Cari Oran
- Toplam Varlıklara Göre Borç
- Gerçek ve Tahmini Gelir kıyaslaması
- Bu yılki Faturalanmış Gelir
- Bu yılki İşletim giderleri Oranı
- Bu yılki Kar Marjı
- Gerçek ve Bütçe Giderleri karşılaştırması - Tüm şirketler

Her bir kutucuk bir destek raporu tarafından desteklenmektedir. Bu raporlar çoğu zaman daha fazla bilgi sağlayan grafik ve tablolar içermektedir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                      | Raporların içerdiği bilgiler |
|-----------------------------|--------------------------------------|
| Nakit Analizi               | Tüzel kişiliğe göre nakit, çeyreğe göre nakit, toplam nakit ve hesaba göre nakit<blockquote>[!NOTE]<br>Üç aya göre nakit bilgisi, ilk çeyrek için toplamdaki başlangıç bakiyelerini içermez. Her çeyrekte deftere nakledilen yeni hareketlerin toplamını gösterir.</blockquote> |
| Mevcut Oran Analizi      | Tüzel kişiliğe göre mevcut oran, çeyreğe göre mevcut oran ve mevcut kıymetler ve borçlar için bilanço |
| Hızlı Oran Analizi        | Tüzel kişiliğe göre hızlı oran, çeyreğe göre hızlı oran ve nakit, alacak hesapları ve mevcut borçlar için bilançolar |
| Satılan Malların Maliyeti Analizi | Tüzel kişiliğe göre Satılan malın maliyeti (SMM), bu yılki ve geçen çeyreğe göre SMM, tüzel kişiliğe satışların SMM'si, toplam SMM ve SMM'nin satışa oranı |
| İşletme Sermayesi Analizi    | Tüzel kişiliğe göre işletme sermayesi, çeyreğe göre işletme sermayesi, mevcut kıymetler, mevcut varlıklar ve toplam işletme sermayesi |
| Kıymet ve Borç Analizi     | Tüzel varlığa göre toplam varlık getirisi ve toplam kıymetler borcu, çeyrekten bu güne toplam kıymetlere göre borç ve kıymetleri toplam getirisi, kıymetler ve borçlar |
| Kar Marjı Analizi      | Tüzel kişiliğe göre gerçek ve bütçe kar marjı, çeyreğe göre kar marjı, kar marjı oranı ve kar marjı |
| Net Gelir Analizi         | Tüzel kişiliğe göre gerçek ve bütçe net geliri, bu yıl ve geçen yılki net gelir ve masrafların net gelire oranı |
| Kazanç Analizi           | Tüzel kişiliğe göre vergi ve faiz öncesi gerçek ve bütçe kazançları (EBIT), bu yıl ve geçen yılki EBIT, giderlerin gelire oranı, gerçek ve bütçe giderlerinin gelirlere oranı |
| Gelir Analizi            | Toplam gelir, tüzel kişiliğe göre gerçek ve bütçe toplam geliri, bu yıl ve geçen yılki toplam gelir, tüzel kişiliğe göre gelir bütçe farkı, bu dönem ve geçen dönem toplam gelir |
| Gider Analizi            | Toplam giderler, tüzel kişiliğe göre gerçek ve bütçe toplam giderleri, çeyreğe göre gerçek ve bütçe toplam giderleri, hesap kategorisine göre toplam giderler ve faaliyet giderleri oranı |
| Faturalandırılmış Gelir Analizi     | Alacak hesapları toplamı, tüzel kişiliğe göre alacak hesap toplamı, çeyreğe göre alacak hesap toplamı ve alacak hesaplarının bilançosu<blockquote>[!NOTE]<br>Bu bilgi, alacak hesapları genel muhasebe hesapları için başlangıç bakiyelerini içermez. Alacak hesaplarına nakledilen yeni hareketleri gösterir.</blockquote> |

Tüm bu raporlardaki grafikler ve kutucuklar filtrelenebilir ve panoya sabitlenebilir. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
**Mali performans** Power BI içeriğinin temeli olarak kullanılan varlıklar aşağıdakilerdir: 

**Toplanan veri varlıkları**

- **GeneralLedgerActivities** – Bu varlık, genel muhasebe bakiyelerini hesap kategorisine göre toplar.
- **BudgetActivities** – Bu varlık, bütçe bakiyelerini hesap kategorisine göre toplar.

**Veri varlıkları**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Genel muhasebe defterleri
- ChartofAccounts

Bu varlıklar, veri modelinde hesaplanmış ölçümler oluşturmak için kullanılıyordu. Hesaplanmış ölçümler, anahtar performans göstergeleri (KPI'ları) hesaplamak ve içerikte kullanıla raporları hesaplamakta kullanılır. İçerik, varsayılan olarak son üç yılın ve gelecekteki bir yılın verilerini getirir. Raporlara ve panoya ek hesaplamalar dahil etmek için [Microsoft Excel çalışma kitabı](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi)'nı değiştirebilirsiniz. Bu çalışma kitabı, içeriği oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yapmayı bitirdikten sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

