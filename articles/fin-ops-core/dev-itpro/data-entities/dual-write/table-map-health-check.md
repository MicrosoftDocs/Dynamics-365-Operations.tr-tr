---
title: Tablo eşlemesi sistem durumu denetimi için hata kodları
description: Bu makalede, tablo eşlemesi durum denetimi için hata kodları açıklanmaktadır.
author: RamaKrishnamoorthy
ms.date: 05/31/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-10-04
ms.openlocfilehash: d3f413f34296fd01da6741bb49658285394cbd17
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288775"
---
# <a name="errors-codes-for-the-table-map-health-check"></a>Tablo eşlemesi sistem durumu denetimi için hata kodları

[!include [banner](../../includes/banner.md)]



Bu makalede, tablo eşlemesi durum denetimi için hata kodları açıklanmaktadır.

## <a name="error-100"></a>Hata 100

Hata iletisi şudur: "finans ve operasyon önerilerini çalıştırmak için gereken minimum finans ve operasyon platformu sürümü PU 43'tür."

Bu özellik, finans ve operasyon uygulamalarının 10.0.19 veya sonraki sürümü için platform güncelleştirmeleri gerektirir.

## <a name="error-400"></a>Hata 400

Hata iletisi şudur: "\{finance and operations UniqueEntityName\} varlığı için hiçbir iş olayı kayıt verisi bulunamadı, bu da eşlemenin çalışmadığı veya tüm alan eşlemesinin tek yönlü olduğu anlamına gelir."

## <a name="error-500"></a>Hata 500

Hata iletisi: "\{proje adı\} projesi için proje konfigürasyonu bulunamadı. Bunun nedeni projenin etkinleştirilmemesi veya tüm alan eşlemelerinin müşteri etkileşiminden finans ve operasyon uygulamalarına tek yönlü olmasıdır."

Tablo haritası için eşlemeleri denetleyin. Müşteri etkileşimi uygulamalarından finans ve operasyon uygulamalarına tek yönlü ise finans ve operasyon uygulamalarından Dataverse'e canlı eşitleme için trafik oluşturulmaz.

## <a name="error-900"></a>Hata 900

Hata iletisi şudur: "\{finance and operations UniqueEntityName\} varlığı için geçersiz kaynak filtresi \{sourceFilter\} biçimi."

Finans ve operasyon uygulamaları için tablo eşlemesinde belirtilen kaynak filtre sözdizimsel olarak doğru değildir. Filtre ölçütlerini doğrulamak için bkz. [Dinamik eşitleme sorunlarını giderme](dual-write-troubleshooting-live-sync.md#live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps).

## <a name="error-1000"></a>Hata 1000

Hata iletisi şudur: "Çift yazma canlı eşitlemesi için kullanılan Varlık \{finance and operations UniqueEntityName\} sorgusu, \{finance and operations EntityFilterQueryString\}'dir. Sorgu ölçütlerine uyan kayıtlar canlı eşitleme için oluşturulacak."

Döndürülen varlık sorgusu, varlık için yedekleme SQL sorgusudur. Dinamik eşitleme için kullanıma açılan iş verilerini belirleyen sorgudaki iç birleştirmeleri veya filtreleri denetleyin. İç birleştirmeler ve süzgeçler, çift yazılabilir canlı eşitleme için çekilen her kayıt için yerine getirilmesi gereken zorunlu koşullardır.

## <a name="error-1300"></a>Hata 1300

Hata iletisi şudur: "\{finance and operations EntityMetadata.EntityProperties.LogicalEntityName\} için \{s.EntityFieldName\} sanal alanları çift yazma için izlenmeyebilir."

Finans ve operasyon tablolarındaki sanal alanlar izleme için etkinleştirilmemiştir. Canlı eşitleme verileri eşitleyebilir, ancak sütunlarda yapılan değişiklikleri çekemez.

## <a name="error-1500"></a>Hata 1500

Hata iletisi: "\{datasource.DataSourceName\} veri kaynağında izlemeyi etkinleştirmek için Customer Engagement'ta arama olmayan alanla eşlenen en az bir alan olmalıdır."

Varlıktaki veri kaynağında çift yazılabilir olarak eşlenen herhangi bir alan yok. Alttaki tabloda yapılan değişiklikler çift yazılır olarak izlenmez.

## <a name="error-1600"></a>Hata 1600

Hata iletisi şudur: "Veri kaynağı: \{finance and operations EntityMetadata.EntityProperties.LogicalEntityName\} için \{datasource.DataSourceName\} varlığının bir aralığı var. Yalnızca aralık koşuluna uyan kayıtlar çıkış için çekilir."

Finans ve operasyon uygulamalarındaki varlıkların filtre aralıklarının etkinleştirildiği veri kaynakları olabilir. Bu aralıklar, canlı eşitlemenin bir parçası olarak çekilen kayıtları tanımlar. Finans ve operasyon uygulamalarından bazı kayıtlar Dataverse'e atlanırsa, kayıtların varlıktaki aralık ölçütlerini karşılayıp karşılamadığını denetleyin. Bu denetimi yapmanın basit bir yolu, aşağıdaki örneğe benzeyen bir SQL sorgusu çalıştırmaktır.

```sql
select * from <EntityName> where <filter criteria for the records> on SQL.
```

## <a name="error-1700"></a>Hata 1700

Hata iletisi: "\{datasourceTable.Key.entityName\} varlığı için Tablo: \{DataSourceTable.Key.subscribedTableName\}, \{origTableToEntityMaps.EntityName\} varlığı için izlenir. Çoklu varlıklar için izlenen aynı tablolar, dinamik eşitleme hareketleri için sistem performansını etkileyebilir."

Aynı tablo birden çok varlık tarafından izleniyorsa, tabloda yapılan tüm değişiklikler bağlantılı varlıklar için çift-yazılır değerlendirmeyi tetikler. Filtre yan tümceleri yalnızca geçerli kayıtları gönderebilse de, uzun süre çalışan sorgular veya iyileştirilmemiş sorgu planları varsa, değerlendirme performans sorununa neden olabilir. Bu sorun iş açısından anlaşılabilir olmayabilir. Ancak, birden fazla varlık arasında birçok kesişen tablo varsa, varlığı basitleştirmeyi veya varlık sorguları için en iyi duruma getirme işlemlerini düşünmelisiniz.

## <a name="error-1800"></a>Hata 1800
Hata iletisi şudur: "CustCustomerV3Entity varlığı için veri kaynağı ({}) aralık değeri içeriyor. Dataverse'ten finans ve operasyon uygulamalarından gelen kayıt eklemeleri varlıktaki aralık değerlerinden etkilenebilir. Lütfen ayarlarınızı doğrulamak için filtre ölçütüne uymayan kayıtlar ile Dataverse finans ve operasyon uygulamaları yönlü kayıt güncelleştirmelerini sınayın."

Finans ve operasyonlar uygulamalarındaki varlıkta belirtilen bir aralık varsa Dataverse'ten finans ve operasyon uygulamalarına gelen eşleştirme, bu aralık ölçütüyle eşleşmeyen kayıtlarda güncelleştirme davranışı için sınanmalıdır. Aralıkla eşleşmeyen tüm kayıtlar, varlık tarafından bir ekleme işlemi olarak kabul edilir. Temel tabloda mevcut bir kayıt varsa ekleme işlemi başarısız olur. Üretime dağıtmadan önce bu kullanım durumunu tüm senaryolarda sınamanızı öneririz.

## <a name="error-1900"></a>Hata 1900
Hata iletisi şudur: "Varlık, giden çift yazma için izlenmeyen {} veri kaynağına sahiptir. Bu, canlı eşitleme sorgusu performansını etkileyebilir. Lütfen, kullanılmayan veri kaynaklarını ve tabloları kaldırmak için finans ve operasyon uygulamalarında varlığı yeniden modelleyin veya çalışma zamanı sorgularını iyileştirmek için getEntityRecordIdsImpactedByTableChange işlemini uygulayın."

Finans ve Operasyon uygulamalarından gerçek canlı eşitlemede izleme için kullanılmayan birçok veri kaynağı varsa varlık performansı canlı eşitlemeyi etkileyebilir. İzlenen tabloları iyileştirmek için getEntityRecordIdsImpactedByTableChange yöntemini kullanın.

## <a name="error-5000"></a>Hata 5000
Hata iletisi "Zaman uyumlu eklentiler, varlık hesaplarının veri yönetimi olayları için kaydedilir. Bunlar, Dataverse'e ilk eşitleme ve canlı eşitleme ile içe aktarma performansını etkileyebilir. En iyi performans için lütfen eklentileri zaman uyumsuz işleme olarak değiştirin. Kayıtlı eklentilerin listesi: {}."

Dataverse varlığındaki zaman uyumlu eklentiler, hareket yükünü artırdığı için canlı eşitleme ve ilk eşitleme performansını etkileyebilir. Önerilen yaklaşım, eklentileri kapatmak veya belirli bir varlık için ilk eşitlemede veya canlı eşitlemede yükleme zamanı yavaşsa eklentileri zaman uyumsuz hale getirmektir.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

