---
title: Tazminat ve Kazançlar Power BI içeriği
description: Bu konu Finance and Operations - Ücret ve Kazançlar Power BI içeriğini açıklar.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6834940b16749461066e8f1000cbb7c2d4371109
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548755"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Tazminat ve Kazançlar Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu Finance and Operations - Ücret ve Kazançlar Power BI içeriğini açıklar. 

## <a name="reports-that-are-included-in-the-content-pack"></a>İçerik paketinde bulunan raporlar
İçerik paketini Finance and Operations verinize bağladıktan sonra, raporlar kuruluşunuzun verilerinde görünür. Daha önce hiç Microsoft Power BI kullanmadıysanız daha fazla bilgiyi [Power BI için Destekli Öğrenme sayfasından](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) edinebilirsiniz. İçerik paketinde bulunan raporlar, ek bilgiler içeren hem grafiklere hem de tablolara sahiptir. Aşağıdaki tablo bu raporları açıklar.

| Rapor                     | İçindekiler                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Maaş ve Kazançlar Analizi | Şirket, ortalama saatlik ödem, ortalama maaşlı ödeme, istihdam türüne göre çalışanlar ve plan kaydına göre saatli ve maaşlı çalışanlar |
| Çalışan Kazançları          | Seçilen kazanca göre personel kaydı                                                                                               |

Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Finance and Operations verisi, Ücret ve Kazanç içerik paketindeki raporları doldurmak için kullanılır. Aşağıdaki tablo, içerik paketinin üzerine dayandırıldığı varlıkları gösterir.

| Varlık                            | İçindekiler                                                                                                   | Diğer varlıklarla ilişkiler |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| İşgücü\_CalendarOffset         | Raporları dilimlemek için takvim kaydırmaları                                                                          | İşgücü\_PastPositionAssignment, İşgücü\_PositionTrend, İşgücü\_WorkerTrend, İşgücü\_TerminatedWorker |
| İşgücü\_Şirket                | Raporların filtreleneceği şirketler                                                                             | İşgücü\_CurrentCompensation, İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_Compensation           | Zaman içerisindeki ödeme oranı ve sıklık                                                                           | İşgücü\_CurrentCompensation, İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_CurrentCompensation    | Günün tarihi itibariyle ödeme oranı ve sıklık                                                              | İşgücü\_Şirket, İşgücü\_Maaş, İşgücü\_Demografi, İşgücü\_İş, İşgücü\_Pozisyon |
| İşgücü\_CurrentPosition        | Günün tarihine göre konumlar, tam zaman eşdeği (FTE), açık konumlar ve açıktan doldurulana konumlar | İşgücü\_İş, İşgücü\_Pozisyon |
| İşgücü\_CurrentWorker          | Günün tarihi, ya ve insan sayısına göre çalışanlar                                                         | İşgücü\_Şirket, İşgücü\_Maaş, İşgücü\_GeographicLocation, İşgücü\_Performans, İşgücü\_WorkerName, İşgücü\_ReportsToWorkerName, İşgücü\_WorkerTitle, İşgücü\_Demografikler, İşgücü\_İş, İşgücü\_İstihdam, İşgücü\_Pozisyon, İşgücü\_WorkerBenefit |
| İşgücü\_Tarih                   | Günler, haftalar, aylar ve yıllar                                                                             | İşgücü\_PastPositionAssignment, İşgücü\_PositionTrend, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_Demografikler           | Doğum tarihi, cinsiyet, etnik köken ve medeni hal                                                   | İşgücü\_CurrentWorker İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_İstihdam             | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                                                                  | İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_GeographicLocation     | Şehir, ilçe, posta kodu ve eyalet veya bölge                                                           | İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_İş                    | İşlev, tür ve başlık                                                                                  | İşgücü\_CurrentPosition, İşgücü\_CurrentWorker |
| İşgücü\_PastPositionAssignment | Atama neden, başlangıç tarihi, bitiş tarihi ve iş                                                           | İşgücü\_CalendarOffset, İşgücü\_Tarih, İşgücü\_İş, İşgücü\_Pozisyon |
| İşgücü\_Performans            | Değerlendirme, açıklama ve derecelendirme modeli                                                                      | İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_Konum               | Departman, FTE, konum, konum türü başlığı                                                        | İşgücü\_CurrentPosition, İşgücü\_CurrentWorker |
| İşgücü\_PositionTrend          | Zaman içerisindeki konumlar, FTE ve iş                                                                          | İşgücü\_CalendarOffset, İşgücü\_Tarih, İşgücü\_İş, İşgücü\_Pozisyon |
| İşgücü\_ReportsToWorkerName    | Adı, ikinci ad ve tam adı                                                                       | İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_Yetenek                  | Beceri, beceri türü ve derecelendirme                                                                              | |
| İşgücü\_TerminatedWorker       | Çıkartılan çalışanlar, çıkartılma tarihi, başlık, konum ve iş                                             | İşgücü\_Şirket, İşgücü\_Maaş, İşgücü\_GeographicLocation, İşgücü\_Performans, İşgücü\_WorkerName, İşgücü\_ReportsToWorkerName, İşgücü\_CalendarOffset, İşgücü\_Tarih, İşgücü\_WorkerTitle, İşgücü\_Demografikler, İşgücü\_İstihdam, İşgücü\_İş, İşgücü\_Konum, İşgücü\_WorkerBenefit |
| İşgücü\_WorkerBenefit          | Yürürlük tarihi, kazanç seçeneği, kazanç planı ve kazanç türü                                             | İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_WorkerName             | Adı, ikinci ad ve tam adı                                                                       | İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_WorkerTitle            | Başlık ve kıdem tarihi                                                                                   | İşgücü\_CurrentWorker, İşgücü\_TerminatedWorker, İşgücü\_WorkerTrend |
| İşgücü\_WorkerTrend            | Zaman içerisinde çalışanlar, çalışan sayısı, şirket ve konum                                                        | İşgücü\_Şirket, İşgücü\_Maaş, İşgücü\_GeographicLocation, İşgücü\_Performans, İşgücü\_WorkerName, İşgücü\_ReportsToWorkerName, İşgücü\_CalendarOffset, İşgücü\_Tarih, İşgücü\_WorkerTitle, İşgücü\_Demografikler, İşgücü\_İstihdam, İşgücü\_İş, İşgücü\_WorkerBenefit |
