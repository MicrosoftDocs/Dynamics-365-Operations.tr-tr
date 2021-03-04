---
title: İşe alma Power BI içeriği
description: Bu konu, İşe alma Power BI içeriğini açıklar. Bu raporlara nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 524b1c29d204c1b013546008b1be7868cbf8db06
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680574"
---
# <a name="recruiting-power-bi-content"></a>İşe alma Power BI içeriği

[!include [banner](../includes/banner.md)]

Bu konu, **İşe alma** Microsoft Power BI içeriğini açıklar. Bu Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişim
**İşe alma** Power BI içeriği **İşe alma yönetimi** çalışma alanında gösterilir.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>İşe alma yönetimi çalışma alanındaki raporlar ve görseller
**İşe alma yönetimi** çalışma alanı bir **Analitik** sekmesi içerir. Bu sekme, işe alma için gömülü Power BI içeriğini barındırır. İçerik bir genel bakış sekmesinden ve ayrıntıları içeren ek sekmelerden oluşur. Aşağıdaki tablo her sekmedeki raporları açıklar.

| Rapor               | İçindekiler |
|----------------------|----------|
| İşe Almaya Genel Bakış | Diğer raporları özetler |
| Başvuranın Analizi   | Başvuranların toplam sayısı, işe başvuranlar, başvuran kaynakları, kadın ve erkek başvuranlar ve konuma göre başvuranlar |
| Başvuranın Durumu     | Türe ve duruma göre başvuranlar ve başvuranın durumu |
| İşe Alma Analizi  | Net işe alma oranı, işe alma ortalama gün sayısı, kötü işe alımların yüzdesi, işe alma maliyetleri, işe alma projesi sayısı, başvuranı işe alma ve işe alma projesi başına açılan konumlara karşı başvurular |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano oluşturma ve Yapılandırma](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Aşağıdaki tablo, **İşe alma** Power BI içeriğine dayalı varlıkları gösterir.

| Varlık               | İçindekiler                                                         | Diğer varlıklarla ilişkiler |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Başvuran            | Başvuranlar, işe alınan başvuranlar, net işe alma oranı ve maliyetleri          | Başvuranın Adı, Şirket, Takvim Kaydırma, Tarih, Coğrafi Konum, Demografi, İş, Ortam, İşe Alma Projesi |
| Başvuranın Adı       | Başvuranın ilk adı, soyadı ve tam adı                   | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| Takvim Kaydırma      | Raporları dilimlemek için takvim kaydırmaları                                | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| Şirket              | Raporların filtreleneceği şirketler                                   | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| Tarih                 | Günler, haftalar, aylar ve yıllar                                   | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| Demografi         | Doğum tarihi, cinsiyet, etnik köken ve medeni hal         | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| İstihdam Edilen Başvuran   | Başvuran, performans, başlangıç tarihi ve başvuran türü           | Şirket, Takvim Kaydırma, Tarih, Coğrafi Konum, Başvuranın Adı, İstihdam, Performans, İş, Ortam, İşe Alma Projesi |
| İstihdam           | Başlangıç tarihi, bitiş tarihi ve geçiş tarihi                        | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| Coğrafi Konum  | Şehir, ilçe, posta kodu ve eyalet veya bölge                 | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| İş                  | İşlev, tür ve başlık                                        | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| Ortam                | Başvuran kaynağı                                             | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| Performans          | Değerlendirme, açıklama ve derecelendirme modeli                            | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| İşe Alma Projesi  | Proje açıklaması, proje durumu ve açılan yerler                | Başvuran, İstihdam Edilen Başvuran, Sonlandırılan Başvuran |
| İşten Çıkarılan Başvuran | Sonlandırılan başvuranlar, neden, performans ve sonlandırma tarihi | Şirket, Takvim Kaydırma, Tarih, Coğrafi Konum, Performans, Demografi, İstihdam, Ortam, İşe Alma Projesi, Başvuranın Adı |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]