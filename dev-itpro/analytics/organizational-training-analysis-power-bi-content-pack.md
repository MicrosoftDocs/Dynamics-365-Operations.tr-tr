---
title: "Kuruluş eğitim güç BI içeriği"
description: "Bu konuda Dynamics 365 işlemleri - kuruluş eğitim güç BI içeriği açıklar. İçerik Paketi erişimi açıklar ve veri modeli ve içerik paketi oluşturmak için kullanılan varlıkları tanımlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Kuruluş eğitim güç BI içeriği

Bu konuda Dynamics 365 işlemleri - kuruluş eğitim güç BI içeriği açıklar. İçerik Paketi erişimi açıklar ve veri modeli ve içerik paketi oluşturmak için kullanılan varlıkları tanımlar.

<a name="accessing-the-content-pack"></a>İçerik Paketi erişme
--------------------------

Paylaşılan varlıkları kitaplığı Microsoft Dynamics ömrü Hizmetleri (LCS), kuruluş eğitim içerik paketi bulabilirsiniz. İçerik paketini karşıdan yüklemek ve veri işlemleri için Microsoft Dynamics 365 bağlanma hakkında daha fazla bilgi için bkz: [Microsoft ve ortaklarınız LCS içeriğinde güç BI](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İşlem verileri, Dynamics 365 içerik paketi bağlandıktan sonra kuruluşunuzun veri raporlarını göster. Microsoft Power BI önce hiç kullanmadıysanız, daha fazla bilgi üzerinde öğrenebilirsiniz [BI güç destekli öğrenme sayfasını](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Hem grafik hem de ek bilgi içeren tablolar içerik paketinde bulunan raporlar vardır. Aşağıdaki tablo bu raporları açıklar.

| Rapor          | İçindekiler                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurs çözümlemesi | Kayıt konumu, durumu ve kayıt listesi tarafından Kurs katılımcıları tarafından |
| Kurs tipleri    | Yeteneğe göre kurs türleri                                                       |

Grafikleri ve döşeme bu raporlarda filtre uygulayabilir ve grafikleri ve Pano döşemelere Sabitle. Filtre ve güç BI PIN'i hakkında daha fazla bilgi için bkz: [oluşturma ve yapılandırma bir Pano](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 işlemler veri için raporlar kuruluş eğitim içerik paketinde doldurmak için kullanılır. Aşağıdaki tabloda, içerik paketi üzerinde dayandırıldığı varlıkları gösterir.

| Varlık                    | İçindekiler                                                         | Diğer varlıklarla ilişkiler                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eğitim\_CalendarOffset  | Dilim raporları için Takvim kaydırır                                | Eğitim\_CourseAgenda eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_şirket         | Şirketler tarafından raporlara filtre uygulamak için                                   | Eğitim\_CourseAgenda eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_kursu          | Kurs, açıklama, eğitmen adını, konumunu, yer ve durum | Eğitim\_CourseAgenda eğitim\_CourseAttendees eğitim\_CourseSkill                                                                                                                             |
| Eğitim\_CourseAgenda    | Gündem, kurs ve başlangıç ve bitiş saatlerini                          | Eğitim\_şirket eğitim\_CalendarOffset eğitim\_tarih eğitim\_kursu                                                                                                                         |
| Eğitim\_CourseAttendees | Ad, durum, iş ve kayıt tarihi                         | Eğitim\_şirket eğitim\_CalendarOffset eğitim\_tarih eğitim\_demografisi eğitim\_İstihdam eğitim\_kurs eğitim\_WorkerName eğitim\_WorkerTitle eğitim\_iş eğitim\_konumu |
| Eğitim\_CourseSkill     | Beceri, yetenek tipini ve düzeyi                                     | Eğitim\_kursu                                                                                                                                                                                   |
| Eğitim\_tarihi            | Gün, hafta, ay ve yıl                                   | Eğitim\_CourseAgenda eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_demografisi    | Doğum, cinsiyet, etnik köken ve Medeni durum tarihi         | Eğitim\_CourseAgenda eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_çalışma      | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                        | Eğitim\_CourseAgenda eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_işi             | İşlevi, türü ve başlık                                        | Eğitim\_CourseAgenda eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_konumu        | Konum, başlık ve tam zamanlı eşdeğeri (FTE)                  | Eğitim\_CourseAgenda eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_WorkerName      | İlk adı, Soyadı ve tam adı                             | Eğitim\_CourseAttendees                                                                                                                                                                          |
| Eğitim\_WorkerTitle     | Başlık ve kıdem tarihi                                         | Eğitim\_CourseAttendees                                                                                                                                                                          |

Bu varlıklar, hesaplanmış ölçüler veri modelleri oluşturmak için kullanılıyordu. Bunlar hesaplanmış ölçüler sonra anahtar performans göstergeleri (APG) hesaplamak için kullanılır ve içerik paketinde kullanılan raporlar. Raporları ve gösterge tablosu ek hesaplamalara dahil etmek isterseniz, karşıdan yükleyip LCS Training.pbix dosyasından değiştirin. Bu dosyayı içerik paketi oluşturmak için kullanılan varsayılan veri modelidir. Değişiklikleri yaptıktan sonra bir Kuruluş İçerik Paketi ve eklediğiniz bilgiler içeren Pano oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



