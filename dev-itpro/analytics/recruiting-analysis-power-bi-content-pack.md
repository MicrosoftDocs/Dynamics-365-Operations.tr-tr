---
title: "İşe alma Power BI içeriği"
description: "Bu konu Dynamics 365 for Operations - İşe Alma Power BI içeriğini açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b12a2c8983cf7bef770417f76df324293f06fb2
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="recruiting-power-bi-content"></a>İşe alma Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu Dynamics 365 for Operations - İşe Alma Power BI içeriğini açıklar. Bu ayrıca, içerik paketine dahil edilen raporların nasıl kullanılacağını açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik paketine erişmek
--------------------------

İşe Alma içerik paketini, Microsoft Dynamics Lifecycle Services (LCS) içindeki Paylaşılan varlık kütüphanesinde bulabilirsiniz. İçerik paketini indirmek ve Microsoft Dynamics 365 for Operations verinize bağlamak hakkında daha fazla bilgi için bkz. [Microsoft ve ortaklarınızdan LCS içerisindeki Power BI içeriği](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İçerik paketini Dynamics 365 for Operations verinize bağladıktan sonra, raporlar kuruluşunuzun verilerinde görünür. Daha önce hiç Microsoft Power BI kullanmadıysanız, daha fazla bilgiyi şuradan edinin: [Power BI için Destekli Öğrenme sayfası](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). İçerik paketinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                       | İçindekiler                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Başvuranın Analizi           | İşe başvuranlar, başvuran kaynakları, başvuranların konumu ve başvuranların toplam sayısı           |
| Başvuranın Durumu             | Türe ve duruma göre başvuranlar ve başvuranın durumu                                                    |
| Başvuranın Demografisi       | Başvuranların yaşı ve cinsiyeti ve başvuranların eğitim düzeyi ve durumu                             |
| İşe Alma Analizi          | Net işe alma oranı, ortalama işe alma gün sayısı, hatalı işe alımların yüzdesi ve işe alma maliyetleri                    |
| İşe Alma Projesi Analizi | İşe alma projesi sayısı, işe alma projesiyle açılan yerler ve işe alma projesine başvuranların sayısı |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 for Operations verisi, İşe Alma içerik paketindeki raporları doldurmak için kullanılır. Aşağıdaki tablo, içerik paketinin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                          | İçindekiler                                                         | Diğer varlıklarla ilişkiler                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| İşe alma\_Başvuran           | Başvuranlar, işe alınan başvuranlar, net işe alma oranı ve maliyetleri          | İşe alma\_ApplicantName İşe alma\_Şirket İşe alma\_CalendarOffset İşe alma\_Tarih İşe alma\_GeographicLocation İşe alma\_Demografi İşe alma\_İş İşe Alma\_Medya İşe alma\_RecruitmentProject                                |
| İşe alma\_ApplicantName       | Başvuranın ilk adı, soyadı ve tam adı                   | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe Alma\_CalendarOffset      | Raporları dilimlemek için takvim kaydırmaları                                | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_Şirket             | Raporların filtreleneceği şirketler                                   | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_Tarihi                | Günler, haftalar, aylar ve yıllar                                   | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_Demografi        | Doğum tarihi, cinsiyet, etnik köken ve medeni hal         | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_EmployedApplicant   | Başvuran, performans, başlangıç tarihi ve başvuran türü           | İşe alma\_Şirket İşe Alma\_CalendarOffset İşe Alma\_Tarih İşe Alma\_GeographicLocation İşe Alma\_ApplicantName İşe Alma\_Employment İşe Alma\_Performans İşe Alma\_İş İşe Alma\_Media İşe Alma\_RecruitmentProject          |
| İşe alma\_İstihdam          | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                        | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_GeographicLocation  | Şehir, ilçe, posta kodu ve eyalet veya bölge                 | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe Alma\_İş                 | İşlev, tür ve başlık                                        | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_Medya               | Başvuran kaynağı                                             | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_Performans         | Değerlendirme, açıklama ve derecelendirme modeli                            | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_RecruitmentProject  | Proje açıklaması, proje durumu ve açılan yerler                | İşe alma\_Başvuran İşe Alma\_EmployedApplicant İşe Alma\_TerminatedApplicant                                                                                                                                                               |
| İşe alma\_TerminatedApplicant | Sonlandırılan başvuranlar, neden, performans ve sonlandırma tarihi | İşe Alma\_Şirket İşe Alma\_CalendarOffset İşe Alma\_Tarih İşe Alma\_GeographicLocation İşe Alma\_Performans İşe Alma\_Demografi İşe Alma\_İstihdam İşe Alma\_Medya İşe Alma\_RecruitmentProject İşe Alma\_ApplicantName |

Bu varlıklar hesaplanmış ölçümler oluşturmak için kullanılıyordu. Bu hesaplanmış ölçümler daha sonra anahtar performans göstergeleri (KPI'ları) hesaplamak ve içerik paketinde kullanıla raporları hesaplamakta kullanılır. Raporlarınıza ve panonuza ek hesaplamalar dahil etmek istiyorsanız, Recruiting.pbix dosyasını LCS'den indirebilir ve değiştirebilirsiniz. Bu dosya, içerik paketini oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yaptıktan sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





