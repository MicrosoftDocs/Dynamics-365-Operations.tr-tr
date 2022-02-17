---
title: Tablo eşlemesi sistem durumu denetimi için hata kodları
description: Bu konu, tablo eşlemesi durum denetimi için hata kodlarını açıklamaktadır.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 916f3cfca3bae7a073ce4e956a12080ee01c8d31
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061290"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Tablo eşlemesi sistem durumu denetimi için hata kodları

[!include [banner](../../includes/banner.md)]



Bu konu, tablo eşlemesi durum denetimi için hata kodlarını açıklamaktadır.

## <a name="error-100"></a>Hata 100

Hata iletisi şudur: "Finans ve Operasyon önerilerini çalıştırmak için gereken minimum Finans ve Operasyon platformu sürümü PU 43'dür."

Bu özellik, Finans ve Operasyon uygulamalarının 10.0.19 veya sonraki sürümü için platform güncelleştirmeleri gerektirir.

## <a name="error-400"></a>Hata 400

Hata iletisi şudur: "\{Finans ve Operasyon UniqueEntityName\} varlığı için hiçbir iş olayı kayıt verisi bulunamadı, bu da eşlemenin çalışmadığı veya tüm alan eşlemesinin tek yönlü olduğu anlamına gelir."

## <a name="error-500"></a>Hata 500

Hata iletisi: "\{proje adı\} projesi için proje konfigürasyonu bulunamadı. Bu, proje etkinleştirilmedi veya tüm alan eşlemeleri müşteri etkileşiminden Finans ve Operasyon'a tek yönlü olabilir."

Tablo haritası için eşlemeleri denetleyin. Müşteri etkileşimi uygulamalarından Finans ve Operasyon uygulamalarına tek yönlü ise Finans ve Operasyon uygulamalarından Dataverse'e canlı eşitleme için trafik oluşturulmaz.

## <a name="error-900"></a>Hata 900

Hata iletisi şudur: "\{Finans ve Operasyon UniqueEntityName\} varlığı için geçersiz kaynak filtresi \{sourceFilter\} biçimi."

Finans ve Operasyon uygulamaları için tablo eşlemesinde belirtilen kaynak filtre sözdizimsel olarak doğru değildir. Filtre ölçütlerini doğrulamak için, bkz. [Dinamik eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Hata 1000

Hata iletisi şudur: "Çift yazma canlı eşitlemesi için kullanılan \{Finans ve Operasyon UniqueEntityName\} varlığı sorgusu, \{Finans ve Operasyon EntityFilterQueryString\}'dir. Sorgu ölçütlerine uyan kayıtlar canlı eşitleme için oluşturulacak."

Döndürülen varlık sorgusu, varlık için yedekleme SQL sorgusudur. Dinamik eşitleme için kullanıma açılan iş verilerini belirleyen sorgudaki iç birleştirmeleri veya filtreleri denetleyin. İç birleştirmeler ve süzgeçler, çift yazılabilir canlı eşitleme için çekilen her kayıt için yerine getirilmesi gereken zorunlu koşullardır.

## <a name="error-1300"></a>Hata 1300

Hata iletisi şudur: "\{Finans ve Operasyon EntityMetadata.EntityProperties.LogicalEntityName\} için \{s.EntityFieldName\} sanal alanları çift yazma için izlenmeyebilir."

Finans ve Operasyon tablolarındaki sanal alanlar izleme için etkinleştirilmemiştir. Canlı eşitleme verileri eşitleyebilir, ancak sütunlarda yapılan değişiklikleri çekemez.

## <a name="error-1500"></a>Hata 1500

Hata iletisi: "\{datasource.DataSourceName\} veri kaynağında izlemeyi etkinleştirmek için Customer Engagement'ta arama olmayan alanla eşlenen en az bir alan olmalıdır."

Varlıktaki veri kaynağında çift yazılabilir olarak eşlenen herhangi bir alan yok. Alttaki tabloda yapılan değişiklikler çift yazılır olarak izlenmez.

## <a name="error-1600"></a>Hata 1600

Hata iletisi şudur: "Veri kaynağı: \{Finans ve Operasyon EntityMetadata.EntityProperties.LogicalEntityName\} için \{datasource.DataSourceName\} varlığının bir aralığı var. Yalnızca aralık koşuluna uyan kayıtlar çıkış için çekilir."

Finans ve Operasyon uygulamalarındaki varlıkların filtre aralıklarının etkinleştirildiği veri kaynakları olabilir. Bu aralıklar, canlı eşitlemenin bir parçası olarak çekilen kayıtları tanımlar. Finans ve Operasyon uygulamalarından bazı kayıtlar Dataverse'e atlanırsa, kayıtların varlıktaki aralık ölçütlerini karşılayıp karşılamadığını denetleyin. Bu denetimi yapmanın basit bir yolu, aşağıdaki örneğe benzeyen bir SQL sorgusu çalıştırmaktır.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Hata 1700

Hata iletisi: "\{datasourceTable.Key.entityName\} varlığı için Tablo: \{DataSourceTable.Key.subscribedTableName\}, \{origTableToEntityMaps.EntityName\} varlığı için izlenir. Çoklu varlıklar için izlenen aynı tablolar, dinamik eşitleme hareketleri için sistem performansını etkileyebilir."

Aynı tablo birden çok varlık tarafından izleniyorsa, tabloda yapılan tüm değişiklikler bağlantılı varlıklar için çift-yazılır değerlendirmeyi tetikler. Filtre yan tümceleri yalnızca geçerli kayıtları gönderebilse de, uzun süre çalışan sorgular veya iyileştirilmemiş sorgu planları varsa, değerlendirme performans sorununa neden olabilir. Bu sorun iş açısından anlaşılabilir olmayabilir. Ancak, birden fazla varlık arasında birçok kesişen tablo varsa, varlığı basitleştirmeyi veya varlık sorguları için en iyi duruma getirme işlemlerini düşünmelisiniz.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
