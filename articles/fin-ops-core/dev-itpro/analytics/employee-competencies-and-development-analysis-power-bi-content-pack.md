---
title: Personel uzmanlıkları ve gelişimi Power BI içeriği
description: Bu konu, Personel yetkinlikleri ve gelişimi Power BI içeriğini açıklar.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 43a6d825de5d8e012d9ccbfccc5d8c708f248981
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751298"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Personel uzmanlıkları ve gelişimi Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, Personel yetkinlikleri ve gelişimi Power BI içeriğini açıklar. 

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İçerik paketini verilerinize bağladıktan sonra, raporlar kuruluşunuzun verilerinde görünür. Daha önce hiç Microsoft Power BI kullanmadıysanız daha fazla bilgiyi [Power BI için Destekli Öğrenme sayfasından](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData) edinebilirsiniz. İçerik paketinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                            | İçindekiler                                               |
|-----------------------------------|--------------------------------------------------------|
| Yeterlik ve Gelişim Analizi | Takım üyesi yetenek türleri ve türe göre takım üyesi yetenekleri |
| Yetenek Profili                     | Seçilen personelin yetenek profili                |
| Yetenek Analizi                    | Tür ve derecelendirmeye göre yetenekler                              |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve Yapılandırma](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Uygulama verileri, Personel yeterlilikleri ve gelişimi içerik paketindeki raporları doldurmak için kullanılır. Aşağıdaki tablo, içerik paketinin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                            | İçindekiler                                                                                                   | Diğer varlıklarla ilişkiler |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| İşgücü\_CalendarOffset         | Raporları dilimlemek için takvim kaydırmaları                                                                          | |
| İşgücü\_Şirket                | Raporların filtreleneceği şirketler                                                                             | |
| İşgücü\_Compensation           | Zaman içerisindeki ödeme oranı ve sıklık                                                                           | |
| İşgücü\_CurrentCompensation    | Günün tarihi itibariyle ödeme oranı ve sıklık                                                              | İşgücü\_Company, İşgücü\_CurrentCompensation, İşgücü\_Demographics, İşgücü\_Job, İşgücü\_Position |
| İşgücü\_CurrentPosition        | Günün tarihine göre konumlar, tam zaman eşdeği (FTE), açık konumlar ve açıktan doldurulana konumlar | İşgücü\_iş İşgücü\_Konum |
| İşgücü\_CurrentWorker          | Günün tarihi, ya ve insan sayısına göre çalışanlar                                                         | Workforce\_Company, İşgücü\_Compensation, İşgücü\_GeographicLocation, İşgücü\_Performance, İşgücü\_PersonSkill, İşgücü\_WorkerName, İşgücü\_ReportsToWorkerName, İşgücü\_WorkerTitle, İşgücü\_Demographics, İşgücü\_Job, İşgücü\_Employment, İşgücü\_Position |
| İşgücü\_Tarih                   | Günler, haftalar, aylar ve yıllar                                                                             | |
| İşgücü\_Demografikler           | Doğum tarihi, cinsiyet, etnik köken ve medeni hal                                                   | |
| İşgücü\_İstihdam             | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                                                  | |
| İşgücü\_GeographicLocation     | Şehir, ilçe, posta kodu ve eyalet veya bölge                                                           | |
| İşgücü\_İş                    | İşlev, tür ve başlık                                                                                  | |
| İşgücü\_JobPreferredSkill      | Önem, derecelendirme, yetenek ve beceri düzeyi                                                                 | İşgücü\_Skill, İşgücü\_Job |
| İşgücü\_PastPositionAssignment | Atama neden, başlangıç tarihi, bitiş tarihi ve iş                                                           | İşgücü\_CalendarOffset, İşgücü\_Tarih, İşgücü\_İş, İşgücü\_Pozisyon |
| İşgücü\_Performans            | Değerlendirme, açıklama ve derecelendirme modeli                                                                      | |
| İşgücü\_PersonSkill            | Düzey, düzey tarihi ve yetenek                                                                               | İşgücü\_Yetenek |
| İşgücü\_PersonSkillAnalysis    | Sertifikalı, seviye, seviye tarihi ve yetenek                                                                    | İşgücü\_WorkerName, İşgücü\_Skill |
| İşgücü\_Konum               | Departman, FTE, konum, konum türü başlığı                                                        | |
| İşgücü\_PositionTrend          | Zaman içerisindeki konumlar, FTE ve iş                                                                          | İşgücü\_CalendarOffset, İşgücü\_Tarih, İşgücü\_İş, İşgücü\_Pozisyon |
| İşgücü\_ReportsToWorkerName    | Adı, ikinci ad ve tam adı                                                                       | |
| İşgücü\_Yetenek                  | Beceri, beceri türü ve derecelendirme                                                                              | |
| İşgücü\_TerminatedWorker       | Çıkartılan çalışanlar, çıkartılma tarihi, başlık, konum ve iş                                             | İşgücü\_Company, İşgücü\_Compensation, İşgücü\_GeographicLocation, İşgücü\_Performance, İşgücü\_WorkerName, İşgücü\_ReportsToWorkerName, İşgücü\_CalendarOffset, İşgücü\_Date, İşgücü\_WorkerTitle, İşgücü\_Demographics, İşgücü\_Employment, İşgücü\_Job, İşgücü\_Position |
| İşgücü\_WorkerName             | Adı, ikinci ad ve tam adı                                                                       | |
| İşgücü\_WorkerTitle            | Başlık ve kıdem tarihi                                                                                   | |
| Workorce\_WorkerTrend             | Zaman içerisinde çalışanlar, çalışan sayısı, şirket ve konum                                                        | İşgücü\_Company, İşgücü\_Compensation, İşgücü\_GeographicLocation, İşgücü\_Performance, İşgücü\_WorkerName, İşgücü\_ReportsToWorkerName, İşgücü\_CalendarOffset, İşgücü\_Date, Workforce\_WorkerTitle, İşgücü\_Demographics, İşgücü\_Employment, İşgücü\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]