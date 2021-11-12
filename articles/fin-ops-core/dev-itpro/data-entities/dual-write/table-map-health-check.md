---
title: Tablo eşlemesi sistem durumu denetimi için hata kodları
description: Bu konu, tablo eşlemesi durum denetimi için hata kodlarını açıklamaktadır.
author: nhelgren
ms.date: 10/04/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: nhelgren
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: 4f0b92a6bc6c051a6bb24b49d3280ca5ecea3625
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725087"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Tablo eşlemesi sistem durumu denetimi için hata kodları

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Bu konu, tablo eşlemesi durum denetimi için hata kodlarını açıklamaktadır.

## <a name="error-100"></a>Hata 100

Hata iletisi: "Finance and Operations önerilerini çalıştırmak için en düşük Finance and Operations platform sürümü, PU 43'tür."

Özellik, Finance and Operations uygulamalarının sürüm 10.0.19 veya üstü için platform güncelleştirmeleri gerektiriyor.

## <a name="error-400"></a>Hata 400

Hata iletisi: "\{Finance and Operations UniqueEntityName\} varlığı için iş olayı kayıt verileri bulunamadı. Bu, eşlemenin çalışmadığını veya tüm alan eşlemelerinin tek yönlü olduğu anlamına gelir."

## <a name="error-500"></a>Hata 500

Hata iletisi: "\{proje adı\} projesi için proje konfigürasyonu bulunamadı. Bu, proje etkin değil ya da Customer Engagement'tan Finance and Operations'a tüm alan eşlemelerinin tek yönlü olduğu anlamına gelebilir."

Tablo haritası için eşlemeleri denetleyin. Customer Engagement uygulamalarından Finance and Operations uygulamalarına tek yönlülerse, Finance and Operations uygulamalarından Dataverse'e dinamik eşitleme için hiçbir trafik oluşturulmaz.

## <a name="error-900"></a>Hata 900

Hata iletisi: "\{Finance and Operations UniqueEntityName\} varlığı için geçersiz kaynak filtresi \{sourceFilter\} biçimi."

Finance and Operations uygulamaları için tablo eşlemesinde belirtilen kaynak filtresi sözdizimsel olarak doğru değildir. Filtre ölçütlerini doğrulamak için, bkz. [Dinamik eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Hata 1000

Hata iletisi: "Çift yazma canlı eşitleme için kullanılan \{Finance and Operations UniqueEntityName\} varlığı sorgusu: \{Finance and Operations EntityFilterQueryString\}. Sorgu ölçütlerine uyan kayıtlar canlı eşitleme için oluşturulacak."

Döndürülen varlık sorgusu, varlık için yedekleme SQL sorgusudur. Dinamik eşitleme için kullanıma açılan iş verilerini belirleyen sorgudaki iç birleştirmeleri veya filtreleri denetleyin. İç birleştirmeler ve süzgeçler, çift yazılabilir canlı eşitleme için çekilen her kayıt için yerine getirilmesi gereken zorunlu koşullardır.

## <a name="error-1300"></a>Hata 1300

Hata iletisi: "\{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} varlığı için sanal alanlar \{s.EntityFieldName\}, çift yazma için izlenemeyebilir."

Finance and Operations tablolarından gelen sanal alanlar izleme için etkin değil. Canlı eşitleme verileri eşitleyebilir, ancak sütunlarda yapılan değişiklikleri çekemez.

## <a name="error-1500"></a>Hata 1500

Hata iletisi: "\{datasource.DataSourceName\} veri kaynağında izlemeyi etkinleştirmek için Customer Engagement'ta arama olmayan alanla eşlenen en az bir alan olmalıdır."

Varlıktaki veri kaynağında çift yazılabilir olarak eşlenen herhangi bir alan yok. Alttaki tabloda yapılan değişiklikler çift yazılır olarak izlenmez.

## <a name="error-1600"></a>Hata 1600

Hata iletisi: "\{Finance and Operations EntityMetadata.EntityProperties.LogicalEntityName\} varlığı için veri kaynağı \{datasource.DataSourceName\}'in bir aralığı var. Yalnızca aralık koşuluna uyan kayıtlar çıkış için çekilir."

Finance and Operations uygulamalarındaki varlıkların filtre aralıklarının etkinleştirildiği veri kaynakları olabilir. Bu aralıklar, canlı eşitlemenin bir parçası olarak çekilen kayıtları tanımlar. Finance and Operations uygulamalarından Dataverse'e yapılan bazı kayıtlar atlanırsa, kayıtların varlık üzerindeki aralık ölçütüne uyup uymadığını denetleyin. Bu denetimi yapmanın basit bir yolu, aşağıdaki örneğe benzeyen bir SQL sorgusu çalıştırmaktır.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Hata 1700

Hata iletisi: "\{datasourceTable.Key.entityName\} varlığı için Tablo: \{DataSourceTable.Key.subscribedTableName\}, \{origTableToEntityMaps.EntityName\} varlığı için izlenir. Çoklu varlıklar için izlenen aynı tablolar, dinamik eşitleme hareketleri için sistem performansını etkileyebilir."

Aynı tablo birden çok varlık tarafından izleniyorsa, tabloda yapılan tüm değişiklikler bağlantılı varlıklar için çift-yazılır değerlendirmeyi tetikler. Filtre yan tümceleri yalnızca geçerli kayıtları gönderebilse de, uzun süre çalışan sorgular veya iyileştirilmemiş sorgu planları varsa, değerlendirme performans sorununa neden olabilir. Bu sorun iş açısından anlaşılabilir olmayabilir. Ancak, birden fazla varlık arasında birçok kesişen tablo varsa, varlığı basitleştirmeyi veya varlık sorguları için en iyi duruma getirme işlemlerini düşünmelisiniz.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
