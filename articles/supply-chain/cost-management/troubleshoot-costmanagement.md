---
title: Maliyet yönetimi sorunlarını giderme
description: Bu konu, maliyet yönetimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4439743"
---
# <a name="troubleshoot-cost-management"></a>Maliyet yönetimi sorunlarını giderme

Bu konu, maliyet yönetimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Stok değeri/yaşlandırma raporları ile bunların depolama sürümleri arasındaki işlevsel boşluklar

[Stok yaşlandırma raporu depolama alanı](inventory-aging-report-storage.md)ve [Stok değeri depolama raporu özellikleri](inventory-value-report-storage.md), Supply Chain Management'ın büyük miktarda stok hareketi görüntülemesine olanak sağlar. Her durumda, rapor sonuçları, bu raporların depolama dışı sürümlerinden farklı olarak tarama ve dışarı aktarma için kaydedilir. Ancak, bu raporların depolama dışı sürümlerinde bulunan bazı işlevler depolama sürümlerinde yoktur. Aşağıdaki alt bölümler farklılıkları özetler ve geçici çözümler sağlar.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Rapor düzeninde etkinleştirilmiş olsalar bile, depolama raporları alt toplamlar içermez

Sonuç dışarı aktarıldığında, özellikle de kullanıcılar kayıt sırasını değişiyorlarsa alt toplamlar sorunlara neden olabilir.

Alt toplamları denetlemek için sonucu Microsoft Excel'e dışarı aktarabilirsiniz. Alternatif olarak, Supply Chain Management içindeki alt toplamları denetlemek istiyorsanız tüm gruplar için alt toplamı sütuna göre görmek için daha esnek bir yol sağlayan *Yeni kılavuz denetimi* ve *(Önizleme) Kılavuzlarda gruplama* özelliklerini etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanın. Daha fazla bilgi için [Kılavuz özellikleri](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md) bölümüne bakın.

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Stok değeri depolama raporu, kayıt defteri hesap bilgilerini desteklemiyor

Stok hesapları bakiyesini almak ve bunu **Stok değeri depolama** raporuyla karşılaştırmak için mizanı çalıştırabilirsiniz.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Stoğu kapatmadan kayıt defteri dönemi durumu değiştirilirken uyarılar veya hatalar gösteriliyor

Microsoft, maliyetlendirme çevresindeki yanlış dönem sonu işleminin neden olduğu sorunları önlemek için aşağıdaki doğrulamaları kullanıma sunmuştur. Aşağıdaki hata iletilerinden biriyle karşılaşırsanız bu sorunların nasıl çözümleneceği hakkında daha fazla bilgi için [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) başlıklı makaleye bakın.

- %1 tarihi (10-02-2019) ile bir Yeniden Hesaplama yürütmek üzeresiniz. Son kaydedilen Yeniden Hesaplama, %2 tarihli (20-01-2019) önceki bir dönemde yürütüldü. Bir %3 tarihi (31-01-2019) eşleştirme dönemi sonuyla hiçbir envanter kapatma yürütmesi kaydedilmedi. Lütfen %3 (31-01-2019) dönem sonuyla eşleşen bir stok kapanışı yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir.

- %1 olan kayıt defteri dönemi durumunu, %2 olarak değiştirmek üzeresiniz. Bir %3 tarihi eşleştirme dönemi sonuyla hiçbir envanter kapatma yürütmesi kaydedilmedi. Lütfen durumu değiştirmeden önce %3 itibarıyla dönem sonuyla eşleşen bir stok kapanışı yürütün. Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir. %4 tüzel kişiliğinden raporlandı. Şimdilik bilgilendirme amaçlıdır ancak gelecekte bu tür bir eylem gerçekleştirmeniz gerekecektir.

- Hesap yapısı %1 değiştirildi. Bir veya daha fazla ana hesap %2 artık yok. Bu ana hesaplar, %4 tarihli %3 tarafından gerekli kılınır. %3 işini sürdürebilmeniz için lütfen bu Ana hesapları %1 Hesap yapısına ekleyin. Şimdilik bilgilendirme amaçlıdır ancak gelecekte bu tür bir eylem gerçekleştirmeniz gerekecektir.

- Bir %1 tarihli (31-01-2019) bir stok kapanışı yürütmek üzeresiniz. Dönem sonuyla eşleşen %2 (31-01-2019) tarihli hiçbir geriye dönük maliyet hesaplama yürütmesi kaydedilmedi. Dönemi sonuyla eşleşen %3 tarihli (31-01-2019) bir geriye dönük maliyet hesaplaması yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir.

- %1 tarihli (28-02-2019) bir geriye dönük maliyet hesaplaması yürütmek üzeresiniz. Son kaydedilen geriye dönük maliyet hesaplaması, %2 tarihiyle (31-01-2019) önceki bir dönemde yürütüldü. Dönem sonuyla eşleşen %3 tarihli (31-01-2019) hiçbir envanter kapatma yürütmesi kaydedilmedi.
Lütfen %3 (31-01-2019) itibarıyla dönem sonuyla eşleşen bir stok kapanışı yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve varyantlar, stok kapatma işlemi yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir.

## <a name="inventory-aging-report-discrepancies"></a>Stok yaşlandırma raporu uyuşmazlıkları

**Stok yaşlandırma raporu**, farklı depolama boyutlarında (tesis veya ambar gibi) görüntülendiğinde farklı değerler gösterir. Raporlama mantığı hakkında daha fazla bilgi için bkz. [Stok yaşlandırma raporu örnekleri ve mantığı](inventory-aging-report.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]