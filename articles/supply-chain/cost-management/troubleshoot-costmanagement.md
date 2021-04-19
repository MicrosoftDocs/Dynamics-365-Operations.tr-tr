---
title: Maliyet yönetimi sorunlarını giderme
description: Bu konu, maliyet yönetimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: AndersGirke
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: fc6a48a44a529c82c2a9ee818af95569d9bcb249
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834301"
---
# <a name="troubleshoot-cost-management"></a>Maliyet yönetimi sorunlarını giderme

Bu konu, maliyet yönetimi ile çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Stok değeri/yaşlandırma raporları ile bunların depolama sürümleri arasındaki işlevsel boşluklar

[Stok yaşlandırma raporu depolama alanı](inventory-aging-report-storage.md)ve [Stok değeri depolama raporu özellikleri](inventory-value-report-storage.md), Supply Chain Management'ın büyük miktarda stok hareketi görüntülemesine olanak sağlar. Her durumda, rapor sonuçları, bu raporların depolama dışı sürümlerinden farklı olarak tarama ve dışarı aktarma için kaydedilir. Ancak, bu raporların depolama dışı sürümlerinde bulunan bazı işlevler depolama sürümlerinde yoktur. Aşağıdaki alt bölümler farklılıkları özetler ve geçici çözümler sağlar.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Rapor düzeninde etkinleştirilmiş olsalar bile, depolama raporları alt toplamlar içermez

Sonuç dışarı aktarıldığında, özellikle de kullanıcılar kayıt sırasını değişiyorlarsa alt toplamlar sorunlara neden olabilir.

Alt toplamları denetlemek için sonucu Microsoft Excel'e dışarı aktarabilirsiniz. Alternatif olarak, Supply Chain Management içindeki alt toplamları denetlemek istiyorsanız tüm gruplar için alt toplamı sütuna göre görmek için daha esnek bir yol sağlayan *Yeni kılavuz denetimi* ve *Kılavuzlarda gruplama* özelliklerini etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'ni kullanın. Daha fazla bilgi için [Kılavuz özellikleri](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md) bölümüne bakın.

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

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Stok değerleme yöntemi Standart maliyet veya Hareketli ortalama olduğunda güncelleştirme çakışması oluşur

Ölçeklenebilirlik ve performans için paralel olarak stok günlükleri, satınalma siparişi faturaları veya satış siparişi faturaları gibi belgeleri deftere naklettiğinizde, güncelleştirme çakışmasıyla ilgili hata iletisi alabilirsiniz ve belgelerden bazıları deftere nakledilmeyebilir. Bu sorun, stok değerleme yöntemi *Standart maliyet* veya *Hareketli ortalama* olduğunda gerçekleşebilir. Her iki yöntem de kalıcı maliyetlendirme yöntemidir. Başka bir deyişle, son maliyet deftere nakil sırasında belirlenir.

*Hareketli ortalama* yöntemini kullanıyorsanız, hata iletisi aşağıdaki örneğe benzer:

> Orantılı gider hesaplamasından sonra xx.xx stok değeri beklenmez

*Standart maliyet* yöntemini kullanıyorsanız, hata iletisi aşağıdaki örneğe benzer:

> Standart maliyet, güncelleştirmeden sonraki mali stok değeriyle eşleşmez. Değer = xx.xx, Miktar = yy.yy, Standart maliyet = zz.zz

Microsoft sorunu düzeltmek üzere bir çözüm yayınlayana kadar, bu hataları önlemek veya azaltmak için aşağıdaki geçici çözümleri kullanabilirsiniz:

- Başarısız belgeleri yeniden deftere nakledin.
- Daha az satır içeren belgeler oluşturun.
- Standart maliyette ondalık değerler kullanmaktan kaçının. Standart maliyeti, **Fiyat miktarı** alanı *1* olarak ayarlanacak şekilde tanımlamaya çalışın. *1*'den yüksek bir **Fiyat miktarı** değeri belirtmeniz gerekiyorsa birim standart maliyetindeki ondalık basamak sayısını en aza indirmeye çalışın. (İdeal olarak, ikiden az ondalık basamak olmalıdır.) Örneğin, standart maliyet ayarlarını şu şekilde ayarlamaktan kaçının: **Fiyat** = *10* ve **Fiyat miktarı** = *3*, çünkü bunlar 3,333333 (ondalık değer devam eder) değerinde bir birim standart maliyeti oluşturur.
- Birçok belgede, aynı ürün ve mali stok boyutları birleşimini içeren birden çok satırı kullanmaktan kaçının.
- Paralelleşme derecesini azaltın. (Bu durumda sisteminiz daha hızlı olabilir, çünkü daha az güncelleştirme çakışması ve yeniden deneme gerçekleştirilir.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]