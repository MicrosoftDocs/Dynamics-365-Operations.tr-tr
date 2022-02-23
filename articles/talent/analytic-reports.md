---
title: Attract'te analitik raporları kullanma
description: Bu konuda, Microsoft Dynamics 365 Talent- Attract'ta işe alım süreci öngörülerine yönelik analitik raporları açıklanmaktadır
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462858"
---
# <a name="use-analytic-reports-in-attract"></a>Attract'te analitik raporları kullanma

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract'teki analitik raporlar, işe alım işlemi öngörüleriniz için kullanıma hazır (OOTB) bir çözüm sağlar. Kullanılabilir özellikler şunları içerir:

- **İş analizleri** İşe başvuranların ölçümleri için işin içinde **Analiz** sekmesine tıklayın.
- **Analitik Hub:** İşlerdeki toplu ölçümler için sol gezinme panosunda **Analiz**'e tıklayın.
- **Kullanıcıya özel güvenlik:** –  Raporlara erişim Attract [rolü](security-attract.md) ve iş katılımcısı rolü tarafından denetlenir.
- **Çapraz filtreleme:** Seçilen veriye göre filtrelenen diğer ölçümleri görmek için rapor içindeki görsellere tıklayın.

>[!NOTE] 
>- Bu özellik şu anda [önizlemededir](access-preview-feature.md). Denemek için, [**Kapsamlı Aşe Alım Eklentisine**](attract-comprehensive-hiring.md) sahip olmanız gerekir.
>- Genel kullanıma sunulan tüm önizleme raporları İngilizce olarak görüntülenir.
>- Raporlar 3 saatte bir yenilenir. Son yenileme zamanı (yerel saat diliminde) raporun en üstünde bulunur. Yenileme saatleri yaklaşık değerlerdir ve bölgenizdeki veri hacmine ve kaynak yüküne göre değişir.

## <a name="job-analytics"></a>İş Analizi

İş Analitiği raporları, iş için işe alım sürecinin anlık görüntüleridir.  Temel ölçümler şunları içerir:

- Aşamaya göre etkin başvuranlar
- Başvuran kaynağı
- Başvuran türü (dahili veya harici)

## <a name="analytics-hub"></a>Analiz Merkezi

Analiz Merkezi raporları, işe alma sürecindeki eğilimleri ortaya çıkarmak için işlerden veri toplar. Attract'te iki OOTB rapor bulunur: İşlem Hattı Özeti ve Huni Analizi.

### <a name="pipeline-summary"></a>Potansiyel Satış Özeti

İşlem Hattı Özeti raporu açık işlerle ilgili verileri toplar. Temel ölçümler şunları içerir:

- Aşamaya göre tüm işlerdeki başvuranlar
- Başvuran kaynağı
- Kıdem düzeyine göre açık işler

### <a name="funnel-analysis"></a>Huni Analizi

Huni Analizi raporu, dolduruldu olarak kapatılan işler için veri toplar. Temel ölçümler şunları içerir:

- İşe alım zamanı
- Dönüştürme ölçümleri (üzerine gidildiğinde)
- Teklif kabul oranı

Not: İşe alım raporlamasında en doğru zaman için Kapsamlı İşe Alım Eklentisinin bir parçası olarak sunulan [Teklif yönetimini](offer-setup.md) kullanmanız önerilir.

>[!TIP] 
>Ek bilgi için görsellerin üzerine gelmeyi deneyin. Örneğin, **Etkin başvuranlar**'ın üzerine geldiğinizde görseller aşamadaki ortalama gün sayısını gösterir. Bu bilgileri analiz etmek, işe alım için sürenin kısaltılması açısından önemli öngörüler sağlayabilir ve işe alım görevlilerinin her aşamada harcanan süreyi kısaltma yöntemlerine odaklanmasını sağlar.

## <a name="user-specific-security"></a>Kullanıcıya özel güvenlik

Attract raporlarına Yönetici, Tümünü Oku, İşe Alma Görevlisi ve İşe Alım Müdürü [rolleri](security-attract.md) tarafından erişilebilir. Atanmamış kullanıcılar analitik rapor sayfalarına (İş analizi veya Analiz merkezi) erişime sahip değildir.

İş Analizi raporları, seçili iş için verileri gösterir. Analiz Merkezi bir kullanıcının görüntüleyebileceği tüm işlerden toplanan verileri bildirir. İşler sayfasında hem İşlerim hem de Tüm işleri görebilen kullanıcılar aynı öğeleri Analiz Merkezinde de görebilir.

## <a name="cross-filter"></a>Çapraz filtreleme

Power BI'nin harika özelliklerinden biri, bir rapor sayfasındaki tüm görsellerin birbirlerine bağlı olma şeklidir. Görsellerin birinde bir veri noktası seçerseniz, seçimi temel alarak bu veriyi içeren sayfadaki tüm görseller değişir. Daha fazla bilgi edinmek ve bir örnek görüntülemek için bkz. [Power BI raporunda görseller birbirlerine nasıl çapraz filtre uygular](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Excel'e aktar

Rapor verilerini Excel'de görüntülemek için görseldeki seçenekler menüsüne (üç nokta) tıklayıp **Temel alınan verileri dışa aktar**'ı seçebilirsiniz. Dışa aktarılan veriler Attract'teki kullanıcı izinleri dikkate alınarak filtrelenmiş aktarılır. Daha fazla bilgi için bkz. [Görselleştirmelerden dışa veri aktarma](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
