---
title: "Güç BI içeriği işe alma"
description: "Bu konuda Dynamics 365 işlemleri - güç BI işe alma içeriği açıklar. İçerik paketinde bulunan raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Güç BI içeriği işe alma

Bu konuda Dynamics 365 işlemleri - güç BI işe alma içeriği açıklar. İçerik paketinde bulunan raporlara erişimi açıklar ve içerik paketi oluşturmak için kullanılan varlıkları ve veri modeli hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik Paketi erişme
--------------------------

İşe alma içerik paketi paylaşılan varlıkları kitaplığı Microsoft Dynamics ömrü Hizmetleri (LCS) bulabilirsiniz. İçerik paketini karşıdan yüklemek ve veri işlemleri için Microsoft Dynamics 365 bağlanma hakkında daha fazla bilgi için bkz: [Microsoft ve ortaklarınız LCS içeriğinde güç BI](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İşlem verileri, Dynamics 365 içerik paketi bağlandıktan sonra kuruluşunuzun veri raporlarını göster. Microsoft Power BI önce hiç kullanmadıysanız, daha fazla bilgi üzerinde öğrenebilirsiniz [BI güç destekli öğrenme sayfasını](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Hem grafik hem de ek bilgi içeren tablolar içerik paketinde bulunan raporlar vardır. Aşağıdaki tablo bu raporları açıklar.

| Rapor                       | İçindekiler                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Başvuranın analizi           | Başvuranlar iş, başvuran kaynakları, başvuranların konumu ve başvuranların toplam sayısı           |
| Başvuranın durumu             | Başvuranlar tarafından türünü, durumunu ve Başvuranın durumu                                                    |
| Başvuranın demografisi       | Başvuranların yaş ve cinsiyet ve eğitim düzeyi ve durum Başvuranlar                             |
| Analiz işe alma          | İşe alma oranı net, işe almak, hatalı hires ve personel arama maliyetleri yüzde gün ortalama                    |
| İşe alma projesi analizi | İşe alma projeleri, işe alma projesi tarafından delikler ve işe alma projesi tarafından başvuranların sayısı |

Grafikleri ve döşeme bu raporlarda filtre uygulayabilir ve grafikleri ve Pano döşemelere Sabitle. Filtre ve güç BI PIN'i hakkında daha fazla bilgi için bkz: [oluşturma ve yapılandırma bir Pano](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 veri işlemleri için işe alma içerik paketinde raporları doldurmak için kullanılır. Aşağıdaki tabloda, içerik paketi üzerinde dayandırıldığı varlıkları gösterir.

| Varlık                          | İçindekiler                                                         | Diğer varlıklarla ilişkiler                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| İşe alma\_başvuran           | Başvuranlar, işe alınan Başvuranlar, net işe alma oranı ve maliyetleri          | İşe alma\_ApplicantName işe alma\_şirketin işe alma\_CalendarOffset Recuriting\_işe alma tarihi\_GeographicLocation işe\_işe alma demografisi\_işe alma işi\_medya işe alma\_RecruitmentProject                                |
| İşe alma\_ApplicantName       | Başvuranın adı, Soyadı ve tam adı                   | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_CalendarOffset      | Dilim raporları için Takvim kaydırır                                | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_şirket             | Şirketler tarafından raporlara filtre uygulamak için                                   | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_tarihi                | Gün, hafta, ay ve yıl                                   | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_demografisi        | Doğum, cinsiyet, etnik köken ve Medeni durum tarihi         | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_EmployedApplicant   | Başvuran, performans, başlangıç tarihi ve başvuran yazın           | İşe alma\_şirketin işe alma\_CalendarOffset işe alma\_işe alma tarihi\_GeographicLocation işe\_ApplicantName işe\_İstihdam işe alma\_performans işe alma\_işe alma işi\_medya işe alma\_RecruitmentProject          |
| İşe alma\_çalışma          | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                        | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_GeographicLocation  | Şehir, ilçe, posta kodu ve eyalet veya bölge                 | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_işi                 | İşlevi, türü ve başlık                                        | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_ortam               | Başvuranlar kaynağı                                             | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_performans         | Derecelendirme, açıklama ve değerlendirme modeli                            | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_RecruitmentProject  | Proje açıklaması, proje durumu ve delikler                | İşe alma\_işe başvuran\_işe EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_TerminatedApplicant | Başvuranlar, neden, performans ve sonlandırma tarihi sona erdi | İşe alma\_şirketin işe alma\_CalendarOffset işe alma\_işe alma tarihi\_GeographicLocation işe alma\_performans işe alma\_işe alma demografisi\_İstihdam işe alma\_ortam işe alma\_RecruitmentProject işe\_ApplicantName |

Bu varlıklar, hesaplanmış ölçüler oluşturmakta kullanılmış. Bunlar hesaplanmış ölçüler sonra anahtar performans göstergeleri (APG) hesaplamak için kullanılır ve içerik paketinde kullanılan raporlar. Raporları ve gösterge tablosu ek hesaplamalara dahil etmek isterseniz, karşıdan yükleyip LCS Recruiting.pbix dosyasından değiştirin. Bu dosyayı içerik paketi oluşturmak için kullanılan varsayılan veri modelidir. Değişiklikleri yaptıktan sonra bir Kuruluş İçerik Paketi ve eklediğiniz bilgiler içeren Pano oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



