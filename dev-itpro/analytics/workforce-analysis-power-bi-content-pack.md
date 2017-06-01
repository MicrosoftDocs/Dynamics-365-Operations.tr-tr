---
title: "İşgücü Ölçümleri Power BI içeriği"
description: "Bu konu Dynamics 365 for Operations - İşgücü Ölçümleri Power BI içeriğini açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2a3f611d29e041a5f05e3f93fd2330f4218b9dd1
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="workforce-metrics-power-bi-content"></a>İşgücü Ölçümleri Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu Dynamics 365 for Operations - İşgücü Ölçümleri Power BI içeriğini açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik paketine erişmek
--------------------------

İşgücü Ölçümleri içerik paketini, Microsoft Dynamics Lifecycle Services (LCS) içindeki Paylaşılan varlık kütüphanesinde bulabilirsiniz. İçerik paketini indirmek ve Microsoft Dynamics 365 for Operations verinize bağlamak hakkında daha fazla bilgi için bkz. [Microsoft ve ortaklarınızdan LCS içerisindeki Power BI içeriği](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İçerik paketini Dynamics 365 for Operations verinize bağladıktan sonra, raporlar kuruluşunuzun verilerinde görünür. Daha önce hiç Microsoft Power BI kullanmadıysanız, daha fazla bilgiyi şuradan edinin: [Power BI için Destekli Öğrenme sayfası](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). İçerik paketinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                                           | İçindekiler                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Çalışan Sayısı Analizi Şirket, Departman, Konum | Şirkete, departmana, konuma göre çalışan sayısı ve toplam çalışan sayısı.                                                                                                                           |
| Çalışan sayısı Analiz İşi, Adım, Yönetici            | İşe, Adıma, Yöneticiye göre çalışan sayısı ve toplam çalışan sayısı.                                                                                                                                      |
| Çalışan sayısı Trend Analizi                         | Şirkete göre bu yılki ve geçen yılki çalışan sayısı karşılaştırması ve geçmiş 12 ay için dönen çalışan sayısı                                                                                                                        |
| İşgücü Demografikleri                           | Yaş ve cinsiyet, etnik köken, kıdem ve medeni hale göre çalışan sayısı, tam zamanlı öğrencilerin sayısı, ortalama görev süresi, ortalma yaş ve kadın - erkek çalışan oranı |
| Pozisyon Analizi                                | Departmana göre açık pozisyonlar, kapatılacak açık pozisyonlar, etkin - devre dışı pozisyonlar ve deparatmana göre pozisyonlar                                                                                                   |
| Yıpranma Analizi                               | Bu yıl ve geçen yıl yıpranma karşılaştırması, yıpranma, ayrılan kişilerin ortalama kıdemi, ayrılan kişilerin ortalama yaşı ve ayrılma sebebine göre çalışanlar                                                                   |
| Departmana göre kişiler                             | Departmana, pozisyona ve atama başlama ve bitiş tarihlerine göre personel sayısına sahip çalışanlar                                                                                                                       |
| Kıdemlilik Analizi                               | Şirkete ve kıdemlilik listesine göre ortalama yıl                                                                                                                                                              |
| Yıl Dönümleri ve Hizmet Yılı               | Hizmet yılına ve yıl dönümlerine göre personel                                                                                                                                                                    |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 for Operations verisi, İşgücü Ölçümleri içerik paketindeki raporları doldurmak için kullanılır. Aşağıdaki tablo, içerik paketinin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                            | İçindekiler                                                                                                   | Diğer varlıklarla ilişkiler                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| İşgücü\_CalendarOffset         | Raporları dilimlemek için takvim kaydırmaları                                                                          | İşgücü\_PastPositionAssignment İşgücü\_PositionTrend İşgücü\_WorkerTrend İşgücü\_TerminatedWorker                                                                                                                                                                                                                     |
| İşgücü\_Şirket                | Raporların filtreleneceği şirketler                                                                             | İşgücü\_CurrentCompensation İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                        |
| İşgücü\_Compensation           | Zaman içerisindeki ödeme oranı ve sıklık                                                                           | İşgücü\_CurrentCompensation İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                        |
| İşgücü\_CurrentCompensation    | Günün tarihi itibariyle ödeme oranı ve sıklık                                                              | İşgücü\_Şirket İşgücü\_Maaş İşgücü\_Demografi İşgücü\_İş İşgücü\_Konum                                                                                                                                                                                                                            |
| İşgücü\_CurrentPosition        | Günün tarihine göre konumlar, tam zaman eşdeği (FTE), açık konumlar ve açıktan doldurulana konumlar | İşgücü\_iş İşgücü\_Konum                                                                                                                                                                                                                                                                                               |
| İşgücü\_CurrentWorker          | Günün tarihi, ya ve insan sayısına göre çalışanlar                                                         | İşgücü\_Şirket İşgücü\_Maaş İşgücü\_GeographicLocation İşgücü\_Performans İşgücü\_WorkerName İşgücü\_ReportsToWorkerName İşgücü\_WorkerTitle İşgücü\_Demografikler İşgücü\_İş İşgücü\_İstihdam İşgücü\_Konum İşgücü\_WorkerBenefit                                            |
| İşgücü\_Tarih                   | Günler, haftalar, aylar ve yıllar                                                                             | İşgücü\_PastPositionAssignment İşgücü\_PositionTrend İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                     |
| İşgücü\_Demografikler           | Doğum tarihi, cinsiyet, etnik köken ve medeni hal                                                   | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                                                       |
| İşgücü\_İstihdam             | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                                                  | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                                                       |
| İşgücü\_GeographicLocation     | Şehir, ilçe, posta kodu ve eyalet veya bölge                                                           | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                                                       |
| İşgücü\_İş                    | İşlev, tür ve başlık                                                                                  | İşgücü\_CurrentPosition İşgücü\_CurrentWorker                                                                                                                                                                                                                                                                              |
| İşgücü\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| İşgücü\_PastPositionAssignment | Atama neden, başlangıç tarihi, bitiş tarihi ve iş                                                           | İşgücü\_CalendarOffset İşgücü\_Tarih İşgücü\_İş İşgücü\_Konum                                                                                                                                                                                                                                                     |
| İşgücü\_Performans            | Değerlendirme, açıklama ve derecelendirme modeli                                                                      | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                                                       |
| İşgücü\_PersonSkill            | Düzey ve yetenek                                                                                            | İşgücü\_Yetenek                                                                                                                                                                                                                                                                                                                 |
| İşgücü\_PersonSkillAnalysis    | Sertifikalı, seviye ve yetenek                                                                                | İşgücü\_Yetenek İşgücü\_WorkerName                                                                                                                                                                                                                                                                                           |
| İşgücü\_Konum               | Departman, FTE, konum, konum türü başlığı                                                        | İşgücü\_CurrentPosition İşgücü\_CurrentWorker                                                                                                                                                                                                                                                                              |
| İşgücü\_PositionTrend          | Zaman içerisindeki konumlar, FTE ve iş                                                                          | İşgücü\_CalendarOffset İşgücü\_Tarih İşgücü\_İş İşgücü\_Konum                                                                                                                                                                                                                                                     |
| İşgücü\_ReportsToWorkerName    | Adı, ikinci ad ve tam adı                                                                       | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                                                       |
| İşgücü\_Yetenek                  | Beceri, beceri türü ve derecelendirme                                                                              | İşgücü\_PersonSkill İşgücü\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| İşgücü\_TerminatedWorker       | Çıkartılan çalışanlar, çıkartılma tarihi, başlık, konum ve iş                                             | İşgücü\_Şirket İşgücü\_Maaş İşgücü\_GeographicLocation İşgücü\_Performans İşgücü\_WorkerName İşgücü\_ReportsToWorkerName İşgücü\_CalendarOffset İşgücü\_Tarih İşgücü\_WorkerTitle İşgücü\_Demografikler İşgücü\_İstihdam İşgücü\_İş İşgücü\_Konum İşgücü\_WorkerBenefit |
| İşgücü\_WorkerBenefit          | Yürürlük tarihi, kazanç seçeneği, kazanç planı ve kazanç türü                                             | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                                                       |
| İşgücü\_WorkerName             | Adı, ikinci ad ve tam adı                                                                       | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend İşgücü\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| İşgücü\_WorkerTitle            | Başlık ve kıdem tarihi                                                                                   | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker İşgücü\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Zaman içerisinde çalışanlar, çalışan sayısı, şirket ve konum                                                        | İşgücü\_Şirket İşgücü\_Maaş İşgücü\_GeographicLocation İşgücü\_Performans İşgücü\_WorkerName İşgücü\_ReportsToWorkerName İşgücü\_CalendarOffset İşgücü\_Tarih İşgücü\_WorkerTitle İşgücü\_Demografikler İşgücü\_İstihdam İşgücü\_İş İşgücü\_WorkerBenefit                     |

Bu varlıklar, veri modelinde hesaplanmış ölçümler oluşturmak için kullanılıyordu. Bu hesaplanmış ölçümler daha sonra anahtar performans göstergeleri (KPI'ları) hesaplamak ve içerik paketinde kullanıla raporları hesaplamakta kullanılır. Raporlarınıza ve panonuza ek hesaplamalar dahil etmek istiyorsanız, CompensationandBenefits.pbix dosyasını LCS'den indirebilir ve değiştirebilirsiniz. Bu dosya, içerik paketini oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yaptıktan sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





