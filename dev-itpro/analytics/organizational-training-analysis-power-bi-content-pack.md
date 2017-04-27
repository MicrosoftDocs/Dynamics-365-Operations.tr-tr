---
title: "Kurumsal Eğitim Power BI içeriği"
description: "Bu konu Dynamics 365 for Operations - Kurumsal Eğitim Power BI içeriğini açıklar. İçerik paketine nasıl erişileceğini açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
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

# <a name="organizational-training-power-bi-content"></a>Kurumsal Eğitim Power BI içeriği

[!include[banner](../includes/banner.md)]


Bu konu Dynamics 365 for Operations - Kurumsal Eğitim Power BI içeriğini açıklar. İçerik paketine nasıl erişileceğini açıklar ve içerik paketini oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

<a name="accessing-the-content-pack"></a>İçerik paketine erişmek
--------------------------

Kurumsal Eğitim içerik paketini, Microsoft Dynamics Lifecycle Services (LCS) içindeki Paylaşılan varlık kütüphanesinde bulabilirsiniz. İçerik paketini indirmek ve Microsoft Dynamics 365 for Operations verinize bağlamak hakkında daha fazla bilgi için bkz. [Microsoft ve ortaklarınızdan LCS içerisindeki Power BI içeriği](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İçerik paketini Dynamics 365 for Operations verinize bağladıktan sonra, raporlar kuruluşunuzun verilerinde görünür. Daha önce hiç Microsoft Power BI kullanmadıysanız, daha fazla bilgiyi şuradan edinin: [Power BI için Destekli Öğrenme sayfası](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). İçerik paketinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor          | İçindekiler                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurs Analizi | Konuma göre kayıt, duruma göre kurs katılımcıları ve kayıt listesi |
| Kurs Türleri    | Yeteneğe göre kurs türleri                                                       |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Dynamics 365 for Operations verisi, Kurumsal Eğitim içerik paketindeki raporları doldurmak için kullanılır. Aşağıdaki tablo, içerik paketinin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                    | İçindekiler                                                         | Diğer varlıklarla ilişkiler                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eğitim\_CalendarOffset  | Raporları dilimlemek için takvim kaydırmaları                                | Eğitim\_CourseAgenda Eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_Şirket         | Raporların filtreleneceği şirketler                                   | Eğitim\_CourseAgenda Eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_Kurs          | Kurs, açıklama, eğitmen adı, konum, yer ve durum | Eğitim\_CourseAgenda Eğitim\_CourseAttendees Eğitim\_CourseSkill                                                                                                                             |
| Eğitim\_CourseAgenda    | Gündem, kurs, başlangıç ve bitiş saatleri                          | Eğitim\_Şirket Eğitim\_CalendarOffset Eğitim\_Tarih Eğitim\_Kurs                                                                                                                         |
| Eğitim\_CourseAttendees | Ad, durum, iş ve kayıt tarihi                         | Eğitim\_Şirket Eğitim\_CalendarOffset Eğitim\_Tarih Eğitim\_Demografi Eğitim\_İstihdam Eğitim\_Kurs Eğitim\_WorkerName Eğitim\_WorkerTitle Eğitim\_İş Eğitim\_Pozisyon |
| Eğitim\_CourseSkill     | Beceri, beceri türü ve düzey                                     | Eğitim\_Kurs                                                                                                                                                                                   |
| Eğitim\_Tarih            | Günler, haftalar, aylar ve yıllar                                   | Eğitim\_CourseAgenda Eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_Demografi    | Doğum tarihi, cinsiyet, etnik köken ve medeni hal         | Eğitim\_CourseAgenda Eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_İstihdam      | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                        | Eğitim\_CourseAgenda Eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_İş             | İşlev, tür ve başlık                                        | Eğitim\_CourseAgenda Eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_Pozisyon        | Pozisyon, unvan ve tam zamanlı eşdeğeri (FTE)                  | Eğitim\_CourseAgenda Eğitim\_CourseAttendees                                                                                                                                                   |
| Eğitim\_WorkerName      | Adı, ikinci ad ve tam adı                             | Eğitim\_CourseAttendees                                                                                                                                                                          |
| Eğitim\_WorkerTitle     | Başlık ve kıdem tarihi                                         | Eğitim\_CourseAttendees                                                                                                                                                                          |

Bu varlıklar, veri modelinde hesaplanmış ölçümler oluşturmak için kullanılıyordu. Bu hesaplanmış ölçümler daha sonra anahtar performans göstergeleri (KPI'ları) hesaplamak ve içerik paketinde kullanıla raporları hesaplamakta kullanılır. Raporlarınıza ve panonuza ek hesaplamalar dahil etmek istiyorsanız, Training.pbix dosyasını LCS'den indirebilir ve değiştirebilirsiniz. Bu dosya, içerik paketini oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yaptıktan sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar
Power BI içeriği oluşturmak ve varlıklarla ilgili bazı yararlı bağlantılar şunlardır:

-   [Veri varlıkları](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Kuruluş içerik paketleri oluşturma](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI kullanarak veri modelleme](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Çalışma alanlarına Power BI kutucukları ekleme](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





