---
title: "Çalışan yetkinlikleri ve içerik geliştirme güç BI"
description: "Bu konuda işlemleri - çalışan yetkinlikleri ve güç BI Development içerik için Dynamics 365 açıklanmaktadır. İçerik paketinde bulunan raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Çalışan yetkinlikleri ve içerik geliştirme güç BI

Bu konuda işlemleri - çalışan yetkinlikleri ve güç BI Development içerik için Dynamics 365 açıklanmaktadır. İçerik paketinde bulunan raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik Paketi erişme
--------------------------

Microsoft Dynamics ömrü Hizmetleri (LCS) paylaşılan varlıkları kitaplığı'nda çalışan yetkinlikleri ve içerik geliştirme paketi bulabilirsiniz. İçerik paketini karşıdan yüklemek ve veri işlemleri için Microsoft Dynamics 365 bağlanma hakkında daha fazla bilgi için bkz: [Microsoft ve ortaklarınız LCS içeriğinde güç BI](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İşlem verileri, Dynamics 365 içerik paketi bağlandıktan sonra kuruluşunuzun veri raporlarını göster. Microsoft Power BI önce hiç kullanmadıysanız, daha fazla bilgi üzerinde öğrenebilirsiniz [BI güç destekli öğrenme sayfasını](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Hem grafik hem de ek bilgi içeren tablolar içerik paketinde bulunan raporlar vardır. Aşağıdaki tablo bu raporları açıklar.

| Rapor                            | İçindekiler                                               |
|-----------------------------------|--------------------------------------------------------|
| Uzmanlık & geliştirme analizi | Takım üyesi Yetenek tipleri ve ekip üyesi yeteneklerin türüne göre |
| Yetenek profili                     | Seçilen çalışan için yetenek profili                |
| Yetenek analizi                    | Türü ve derecesi göre yetenekler                              |

Grafikleri ve döşeme bu raporlarda filtre uygulayabilir ve grafikleri ve Pano döşemelere Sabitle. Filtre ve güç BI PIN'i hakkında daha fazla bilgi için bkz: [oluşturma ve yapılandırma bir Pano](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
İşlemler veri Dynamics 365 çalışan yetkinlikleri ve içerik geliştirme paketi raporları doldurmak için kullanılır. Aşağıdaki tabloda, içerik paketi üzerinde dayandırıldığı varlıkları gösterir.

| Varlık                            | İçindekiler                                                                                                   | Diğer varlıklarla ilişkiler                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| İşgücü\_CalendarOffset         | Dilim raporları için Takvim kaydırır                                                                          |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_şirket                | Şirketler tarafından raporlara filtre uygulamak için                                                                             |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_maaş           | Ödeme oranı ve zamanla sıklığı                                                                           |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_CurrentCompensation    | Ödeme oranı ve geçerli tarih itibarıyla sıklığı                                                              | İşgücü\_şirket iş gücü\_CurrentCompensation işgücü\_demografisi işgücü\_iş gücünün\_konumu                                                                                                                                                                                            |
| İşgücü\_CurrentPosition        | Açık pozisyonları ve doldurulmuş açık pozisyonları, tam zamanlı eşdeğeri (FTE) geçerli tarih itibariyle konumlar | İşgücü\_iş gücünün\_konumu                                                                                                                                                                                                                                                                      |
| İşgücü\_CurrentWorker          | Geçerli tarih, yaş ve çalışan sayısı itibariyle çalışanlar                                                         | İşgücü\_şirket iş gücü\_maaş işgücü\_GeographicLocation işgücü\_performans gücünün\_PersonSkill işgücü\_WorkerName işgücü\_ReportsToWorkerName işgücü\_WorkerTitle işgücü\_demografisi işgücü\_iş gücünün\_İstihdam işgücü\_konumu                     |
| İşgücü\_tarihi                   | Gün, hafta, ay ve yıl                                                                             |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_demografisi           | Doğum, cinsiyet, etnik köken ve Medeni durum tarihi                                                   |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_çalışma             | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                                                  |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_GeographicLocation     | Şehir, ilçe, posta kodu ve eyalet veya bölge                                                           |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_işi                    | İşlevi, türü ve başlık                                                                                  |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_JobPreferredSkill      | Önem, derecelendirme, yetenek ve beceri düzeyi                                                                 | İşgücü\_yetenek gücünün\_işi                                                                                                                                                                                                                                                                         |
| İşgücü\_PastPositionAssignment | Atama nedeni, başlangıç tarihi, bitiş tarihi ve iş                                                           | İşgücü\_ClaendarOffset işgücü\_tarih işgücü\_iş gücünün\_konumu                                                                                                                                                                                                                            |
| İşgücü\_performans            | Derecelendirme, açıklama ve değerlendirme modeli                                                                      |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_PersonSkill            | Düzey düzey tarihi ve beceri                                                                               | İşgücü\_yetenek                                                                                                                                                                                                                                                                                        |
| İşgücü\_PersonSkillAnalysis    | Sertifikalı, düzeyi, düzey tarih ve beceri                                                                    | İşgücü\_WorkerName işgücü\_yetenek                                                                                                                                                                                                                                                                  |
| İşgücü\_konumu               | Departman, FTE, konum, konum türü ve başlık                                                        |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_PositionTrend          | Zaman, FTE ve iş pozisyonları                                                                          | İşgücü\_CalendarOffset işgücü\_tarih işgücü\_iş gücünün\_konumu                                                                                                                                                                                                                            |
| İşgücü\_ReportsToWorkerName    | İlk adı, Soyadı ve tam adı                                                                       |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_yetenek                  | Beceri, yetenek tipini ve derecelendirme                                                                              |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_TerminatedWorker       | Çalışanlar, sonlandırma tarihi, başlık, konumu ve işi sonlandırıldı.                                             | İşgücü\_şirket iş gücü\_maaş işgücü\_GeographicLocation işgücü\_performans gücünün\_WorkerName işgücü\_ReportsToWorkerName işgücü\_CalendarOffset Workforces\_tarih işgücü\_WorkerTitle işgücü\_demografisi işgücü\_İstihdam işgücü\_iş gücünün\_konumu |
| İşgücü\_WorkerName             | İlk adı, Soyadı ve tam adı                                                                       |                                                                                                                                                                                                                                                                                                         |
| İşgücü\_WorkerTitle            | Başlık ve kıdem tarihi                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Zaman, çalışan sayısı, şirket ve konum üzerinden çalışanlar                                                        | İşgücü\_şirket iş gücü\_maaş işgücü\_GeographicLocation işgücü\_performans gücünün\_WorkerName işgücü\_ReportsToWorkerName işgücü\_CalendarOffset Workforces\_tarih işgücü\_WorkerTitle işgücü\_demografisi işgücü\_İstihdam işgücü\_işi                     |

Bu varlıklar, hesaplanmış ölçüler veri modelleri oluşturmak için kullanılıyordu. Bunlar hesaplanmış ölçüler sonra anahtar performans göstergeleri (APG) hesaplamak için kullanılır ve içerik paketinde kullanılan raporlar. Raporları ve gösterge tablosu ek hesaplamalara dahil etmek isterseniz, karşıdan yükleyip LCS CompetenciesandDevelopment.pbix dosyasından değiştirin. Bu dosyayı içerik paketi oluşturmak için kullanılan varsayılan veri modelidir. Değişiklikleri yaptıktan sonra bir Kuruluş İçerik Paketi ve eklediğiniz bilgiler içeren Pano oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



