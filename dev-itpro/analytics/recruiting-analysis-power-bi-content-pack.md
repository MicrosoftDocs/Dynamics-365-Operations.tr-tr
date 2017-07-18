---
title: "İşe alma Power BI içeriği"
description: "Bu konu, İşe alma Power BI içeriğini açıklar. Bu raporlara nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 49cfd0f1ed645f1980b21b6d4f453cb7a8957a1a
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="recruiting-power-bi-content"></a>İşe alma Power BI içeriği

[!include[banner](../includes/banner.md)]

Bu konu, **İşe alma** Microsoft Power BI içeriğini açıklar. Power BI raporlarına nasıl erişileceğini açıklar ve içeriği oluşturmakta kullanılmış olan veri modeli ve varlıklar hakkında bilgi sağlar.

## <a name="accessing-the-power-bi-content"></a>Power BI içeriğine erişmek
Microsoft Dynamics 365 for Finance and Operations, Enterprise sürümü Temmuz 2017 güncelleştirmesini kullanıyorsanız, **İşe alma** Power BI içeriği **İşe alma yönetimi** çalışma alanında görüntülenir. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>İşe alma yönetimi çalışma alanındaki raporlar ve görseller
**İşe Alma Yönetimi** çalışma alanı bir **Analiz** sekmesi içerir. Bu sekme işe alma için katıştırılmış Power BI içeriği içerir. İçerik bir genel bakış sekmesinden ve ayrıntıları içeren ek sekmelerden oluşur. Aşağıdaki tablo her sekmedeki raporları açıklar.

| Rapor               | İçindekiler |
|----------------------|----------|
| İşe Almaya Genel Bakış | Diğer raporları özetler |
| Başvuranın Analizi   | Başvuranların toplam sayısı, işe başvuranlar, başvuran kaynakları, kadın ve erkek başvuranlar ve konuma göre başvuranlar |
| Başvuranın Durumu     | Türe ve duruma göre başvuranlar ve başvuranın durumu |
| İşe Alma Analizi  | Net işe alma oranı, işe alma ortalama gün sayısı, kötü işe alımların yüzdesi, işe alma maliyetleri, işe alma projesi sayısı, başvuranı işe alma ve işe alma projesi başına açılan konumlara karşı başvurular |

## <a name="understanding-the-data-model-and-entities"></a>Veri modellerini ve varlıklarını anlama
Bu raporlardaki grafikleri ve kutuları filtreleyebilirsiniz ve grafikleri ve kutuları panoya sabitleyebilirsiniz. Power BI'da filtreleme ve sabitleme hakkında daha fazla bilgi için bkz. [Bir Pano Oluşturma ve Yapılandırma](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Aşağıdaki tablo, **İşe Alma** Power BI içeriğinin temel aldığı varlıkları gösterir.

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

Bu varlıklar hesaplanmış ölçümler oluşturmak için kullanılıyordu. Bu hesaplanmış ölçümler daha sonra anahtar performans göstergeleri (KPI'ları) hesaplamak ve içerikte kullanılan raporları hesaplamakta kullanılır. Raporlarınıza ve panonuza ek hesaplamalar dahil etmek istiyorsanız, Recruiting.pbix dosyasını Microsoft Dynamics Lifecycle Services'dan (LCS) indirebilir ve değiştirebilirsiniz. Bu dosya, içeriği oluşturmak için kullanılan varsayılan veri modelidir. Değişikliklerinizi yaptıktan sonra, eklediğiniz içerikleri kapsayan bir kuruluş içerik paketi ve panosu oluşturabilirsiniz.

