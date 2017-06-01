---
title: "Personel Yeterlikleri ve Geliştirme Power BI içeriği"
description: "Bu konu Dynamics 365 for Operations - Personel Yeterlik ve Gelişim Power BI içeriğini açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 770a832efe8ee2da44d65670b1818be4fcf4bcc0
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Personel Yeterlikleri ve Geliştirme Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu Dynamics 365 for Operations - Personel Yeterlik ve Gelişim Power BI içeriğini açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik paketine erişmek
--------------------------

Personel Yeterlikleri ve Gelişim içerik paketini, Microsoft Dynamics Lifecycle Services (LCS) içindeki Paylaşılan varlık kütüphanesinde bulabilirsiniz. İçerik paketini indirmek ve Microsoft Dynamics 365 for Operations verinize bağlamak hakkında daha fazla bilgi için bkz. [Microsoft ve ortaklarınızdan LCS içerisindeki Power BI içeriği](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İçerik paketini Dynamics 365 for Operations verinize bağladıktan sonra, raporlar kuruluşunuzun verilerinde görünür. Daha önce hiç Microsoft Power BI kullanmadıysanız, daha fazla bilgiyi şuradan edinin: [Power BI için Destekli Öğrenme sayfası](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). İçerik paketinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                            | İçindekiler                                               |
|-----------------------------------|--------------------------------------------------------|
| Yeterlik ve Gelişim Analizi | Takım üyesi yetenek türleri ve türe göre takım üyesi yetenekleri |
| Yetenek Profili                     | Seçilen personelin yetenek profili                |
| Yetenek Analizi                    | Tür ve derecelendirmeye göre yetenekler                              |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 for Operations verisi, Personel Yeterlik ve Gelişim içerik paketindeki raporları doldurmak için kullanılır. Aşağıdaki tablo, içerik paketinin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                            | İçindekiler                                                                                                   | Diğer varlıklarla ilişkiler                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| İşgücü\_CalendarOffset         | Raporları dilimlemek için takvim kaydırmaları                                                                          |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_Şirket                | Raporların filtreleneceği şirketler                                                                             |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_Compensation           | Zaman içerisindeki ödeme oranı ve sıklık                                                                           |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_CurrentCompensation    | Günün tarihi itibariyle ödeme oranı ve sıklık                                                              | İşgücü\_Şirket İşgücü\_CurrentCompensation İşgücü\_Demografi İşgücü\_İş İşgücü\_Konum                                                                                                                                                                                            |
| İşgücü\_CurrentPosition        | Günün tarihine göre konumlar, tam zaman eşdeği (FTE), açık konumlar ve açıktan doldurulana konumlar | İşgücü\_iş İşgücü\_Konum                                                                                                                                                                                                                                                                      |
| İşgücü\_CurrentWorker          | Günün tarihi, ya ve insan sayısına göre çalışanlar                                                         | Workforce\_Şirket İşgücü\_Maaş İşgücü\_GeographicLocation İşgücü\_Performans İşgücü\_PersonSkill İşgücü\_WorkerName İşgücü\_ReportsToWorkerName İşgücü\_WorkerTitle İşgücü\_Demografikler İşgücü\_İş İşgücü\_İstihdam İşgücü\_Position                     |
| İşgücü\_Tarih                   | Günler, haftalar, aylar ve yıllar                                                                             |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_Demografikler           | Doğum tarihi, cinsiyet, etnik köken ve medeni hal                                                   |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_İstihdam             | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                                                  |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_GeographicLocation     | Şehir, ilçe, posta kodu ve eyalet veya bölge                                                           |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_İş                    | İşlev, tür ve başlık                                                                                  |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_JobPreferredSkill      | Önem, derecelendirme, yetenek ve beceri düzeyi                                                                 | İşgücü\_Yetenek İşgücü\_İş                                                                                                                                                                                                                                                                         |
| İşgücü\_PastPositionAssignment | Atama neden, başlangıç tarihi, bitiş tarihi ve iş                                                           | İşgücü\_ClaendarOffset İşgücü\_Tarih İşgücü\_İş İşgücü\_Konum                                                                                                                                                                                                                            |
| İşgücü\_Performans            | Değerlendirme, açıklama ve derecelendirme modeli                                                                      |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_PersonSkill            | Düzey, düzey tarihi ve yetenek                                                                               | İşgücü\_Yetenek                                                                                                                                                                                                                                                                                        |
| İşgücü\_PersonSkillAnalysis    | Sertifikalı, seviye, seviye tarihi ve yetenek                                                                    | İşgücü\_WorkerName İşgücü\_Yetenek                                                                                                                                                                                                                                                                  |
| İşgücü\_Konum               | Departman, FTE, konum, konum türü başlığı                                                        |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_PositionTrend          | Zaman içerisindeki konumlar, FTE ve iş                                                                          | İşgücü\_CalendarOffset İşgücü\_Tarih İşgücü\_İş İşgücü\_Konum                                                                                                                                                                                                                            |
| İşgücü\_ReportsToWorkerName    | Adı, ikinci ad ve tam adı                                                                       |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_Yetenek                  | Beceri, beceri türü ve derecelendirme                                                                              |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_TerminatedWorker       | Çıkartılan çalışanlar, çıkartılma tarihi, başlık, konum ve iş                                             | İşgücü\_Şirket İşgücü\_Maaş İşgücü\_GeographicLocation İşgücü\_Performans İşgücü\_WorkerName İşgücü\_ReportsToWorkerName İşgücü\_CalendarOffset İşgücü\_Tarih İşgücü\_WorkerTitle İşgücü\_Demografikler İşgücü\_İstihdam İşgücü\_İş İşgücü\_Konum |
| İşgücü\_WorkerName             | Adı, ikinci ad ve tam adı                                                                       |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_WorkerTitle            | Başlık ve kıdem tarihi                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Zaman içerisinde çalışanlar, çalışan sayısı, şirket ve konum                                                        | İşgücü\_Şirket İşgücü\_Maaş İşgücü\_GeographicLocation İşgücü\_Performans İşgücü\_WorkerName İşgücü\_ReportsToWorkerName İşgücü\_CalendarOffset İşgüçleri\_Date İşgücü\_WorkerTitle İşgücü\_Demographics İşgücü\_Employment İşgücü\_İş                     |

Bu varlıklar, veri modelinde hesaplanmış ölçümler oluşturmak için kullanılıyordu. Bu hesaplanmış ölçümler daha sonra anahtar performans göstergeleri (KPI'ları) hesaplamak ve içerik paketinde kullanıla raporları hesaplamakta kullanılır. Raporlarınıza ve panonuza ek hesaplamalar dahil etmek istiyorsanız, CompetenciesandDevelopment.pbix dosyasını LCS'den indirebilir ve değiştirebilirsiniz. Bu dosya, içerik paketini oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yaptıktan sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





