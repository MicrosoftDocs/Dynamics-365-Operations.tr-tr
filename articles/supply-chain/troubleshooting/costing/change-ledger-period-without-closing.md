---
title: Stoku kapatmadan genel muhasebe dönemi durumu değiştirilirken uyarılar veya hatalar oluştu
description: Stoku kapatmadan genel muhasebe dönemi durumu değiştirilirken uyarılar veya hatalar oluştu
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477834"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Stoku kapatmadan genel muhasebe dönemi durumu değiştirilirken uyarılar veya hatalar oluştu

Microsoft, maliyetlendirme çevresindeki yanlış dönem sonu işleminin neden olduğu sorunları önlemek için aşağıdaki doğrulamaları kullanıma sunmuştur. Aşağıdaki hata iletilerinden biriyle karşılaşırsanız bu sorunların nasıl çözümleneceği hakkında daha fazla bilgi için [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3) başlıklı makaleye bakın.

- %1 tarihi (10-02-2019) ile bir Yeniden Hesaplama yürütmek üzeresiniz. Son kaydedilen Yeniden Hesaplama, %2 tarihli (20-01-2019) önceki bir dönemde yürütüldü. Bir %3 tarihi (31-01-2019) eşleştirme dönemi sonuyla hiçbir envanter kapatma yürütmesi kaydedilmedi. Lütfen %3 (31-01-2019) dönem sonuyla eşleşen bir stok kapanışı yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir.

- %1 olan kayıt defteri dönemi durumunu, %2 olarak değiştirmek üzeresiniz. Bir %3 tarihi eşleştirme dönemi sonuyla hiçbir envanter kapatma yürütmesi kaydedilmedi. Lütfen durumu değiştirmeden önce %3 itibarıyla dönem sonuyla eşleşen bir stok kapanışı yürütün. Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir. %4 tüzel kişiliğinden raporlandı. Şimdilik bilgilendirme amaçlıdır ancak gelecekte bu tür bir eylem gerçekleştirmeniz gerekecektir.

- Hesap yapısı %1 değiştirildi. Bir veya daha fazla ana hesap %2 artık yok. Bu ana hesaplar, %4 tarihli %3 tarafından gerekli kılınır. %3 işini sürdürebilmeniz için lütfen bu Ana hesapları %1 Hesap yapısına ekleyin. Şimdilik bilgilendirme amaçlıdır ancak gelecekte bu tür bir eylem gerçekleştirmeniz gerekecektir.

- Bir %1 tarihli (31-01-2019) bir stok kapanışı yürütmek üzeresiniz. Dönem sonuyla eşleşen %2 (31-01-2019) tarihli hiçbir geriye dönük maliyet hesaplama yürütmesi kaydedilmedi. Dönemi sonuyla eşleşen %3 tarihli (31-01-2019) bir geriye dönük maliyet hesaplaması yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve varyantlar, bu işlem yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir.

- %1 tarihli (28-02-2019) bir geriye dönük maliyet hesaplaması yürütmek üzeresiniz. Son kaydedilen geriye dönük maliyet hesaplaması, %2 tarihiyle (31-01-2019) önceki bir dönemde yürütüldü. Dönem sonuyla eşleşen %3 tarihli (31-01-2019) hiçbir envanter kapatma yürütmesi kaydedilmedi.

Lütfen %3 (31-01-2019) itibarıyla dönem sonuyla eşleşen bir stok kapanışı yürütmeyi unutmayın. Stok değerlemesi, satılan malların maliyeti ve varyantlar, stok kapatma işlemi yürütülünceye kadar yardımcı kayıt defteri veya genel kayıt defterinde doğru olmayabilir.