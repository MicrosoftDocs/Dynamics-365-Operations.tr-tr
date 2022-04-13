---
title: Planlama Optimizasyonu tarafından kullanılan tarih ve saat parametreleri
description: Bu konu, Planlama Optimizasyonu tarafından çalışma sırasında kullanılan tarih ve saat parametreleri hakkında bilgi sağlar.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0708404f286253449e0400fc65680e903f6d1e9b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468846"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Planlama Optimizasyonu tarafından kullanılan tarih ve saat parametreleri

[!include [banner](../../includes/banner.md)]

Bu konu, Planlama Optimizasyonu tarafından çalışma sırasında kullanılan tarih ve saat parametreleri hakkında bilgi sağlar.

Yerleşik ana planlama altyapısında hareket tarihleri tüm hesaplamalarda kullanılırken, Planlama Optimizasyonu, tarihlere dönüştürülen tarih ve zaman değerleriyle çalışır. Bu davranış farkı, örneğin Planlama Optimizasyonu işlemi geçerli tarihten önce oluşturulduğunu düşündüğü için, ana planlama çalıştırmasının çalıştırıldığı gün için gece yarısı oluşturulan tahmin hareketlerinin dahil edilmediği durumlara yol açabilir.

## <a name="parameters-for-issue-and-demand-transactions"></a>Çıkış ve talep hareketleri için parametreler

Aşağıdaki tabloda, Planlama Optimizasyonu'nu çıkış ve talep hareketlerini işlerken kullandığı parametreler listelenmiştir.

| Parametre | Planlama Optimizasyonundaki parametre adı | Tanım | Microsoft Dynamics 365 Supply Chain Management'taki eşdeğer alan (ReqTrans tablosunda) |
|---|---|---|---|
| Planlanan çıkış saati | `PlannedIssueTime` | Çıkışın geçerli planlandığı tarih. | **Bitiş tarihi** (`FuturesDate`) ve **Gecikmiş zaman** (`FuturesTime`) |
| İstenen çıkış zamanı | `RequestedIssueTime` | Kullanıcı tarafından istenen ve Supply Chain Management'ta ayarlanan çıkış tarihi. Bu parametre, yalnızca serbest bırakılmış veya onaylanmış planlı siparişler için geçerlidir. Planlı siparişler için varsayılan olarak boştur. | **İstenen tarih** (`ReqDateDlvOrig`) |
| Gerekli çıkış zamanı | `RequiredIssueTime` | Planlama Optimizasyonu tarafından düzeltilmiş gerekli çıkış tarihi. İstenen çıkış zamanı, Planlama Optimizasyonunun çalıştığı tarihte geçmişte kalıyorsa gerekli çıkış saati, bugünün tarihinden erken olmayacak şekilde ilk açık güne düzeltilir. İstenen çıkış zamanı takvimde bloke olarak işaretlenmişse, gerekli çıkış zamanı bu tarihten önceki ilk açık güne ayarlanacaktır. | **Gereksinim tarihi** (`ReqDate`) ve **Gereksinim saati** (`ReqTime`) |
| Çıkış saati gecikmesi | `IssueTimeDelay` | Planlanan çıkış zamanı ile onaylanmış ve serbest bırakılmış siparişler için istenen çıkış zamanı veya gerekli çıkış zamanı arasındaki zaman farkı. | **Gecikme (gün olarak)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Giriş ve tedarik hareketleri için parametreler

Aşağıdaki tabloda, Planlama Optimizasyonu'nu giriş ve tedarik hareketlerini işlerken kullandığı parametreler listelenmiştir.

| Parametre | Planlama Optimizasyonundaki parametre adı | Tanım | Supply Chain Management'ta eşdeğer alan (ReqTrans veya ReqPO tablosunda) |
|---|---|---|---|
| Planlanan kullanılabilirlik süresi | `PlannedAvailabilityTime` | Girişin kullanılabilir olması planlanan tarih. | **Gereksinim tarihi** (`ReqDate`) ve **Gereksinim saati** (`ReqTime`) |
| Planlanan giriş saati | `PlannedReceiptTime` | Girişin, konuma ulaşacağı tarih. | **Bitiş tarihi** (`FuturesDate`), **Gecikmiş bitiş zamanı** (`FuturesTime`) ve **Teslim tarihi** (`ReqDateDlv`) veya sipariş henüz serbest bırakılmamışsa **İstenen tarih** (`ReqDateDlvOrig`). |
| Gerekli kullanılabilirlik süresi | `RequiredAvailabilityTime` | Planlama Optimizasyonu tarafından düzeltilmiş gerekli kullanılabilirlik tarihi. | **Gereksinim tarihi** (`ReqDate`) ve **Gereksinim saati** (`ReqTime`) |
| Beklenen giriş saati | `ExpectedReceiptTime` | Serbest bırakılmış bir giriş için beklenen giriş tarihi. Değer, Supply Chain Management'ta kullanıcı tarafından ayarlanır ve Planlama Optimizasyonu tarafından ayarlanmaz. Bu parametre, yalnızca serbest bırakılan girişler için geçerlidir. | **İstenen tarih** (`ReqDateDlvOrig`) |
| Gerekli giriş saati | `RequiredReceiptTime` | Planlama Optimizasyonu tarafından düzeltilmiş gerekli giriş tarihi. | **Gereksinim tarihi** (`ReqDate`) ve **Gereksinim saati** (`ReqTime`) |
| Planlı sipariş zamanı | `PlannedOrderingTime` | Planlama Optimizasyonu tarafından hesaplanan sipariş tarihi. | **Sipariş tarihi** (`ReqDateOrder`) ve **Sipariş saati** (`ReqTimeOrder`) |
| Planlanan faaliyet başlangıç saati | `PlannedActivityStartTime` | Bu giriş için faaliyetin başlaması gereken tarih. | **Başlangıç tarihi** (`SchedFromDate`) |
| Giriş saati gecikmesi | `ReceiptTimeDelay` | Planlanan giriş zamanı ile gerekli giriş saati arasındaki zaman farkı. | **Gecikme (gün)** (`FuturesDays`) ve **Gecikmeli bitiş süresi** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Planlama Optimizasyonu tarafından kullanılan tarih parametresi örnekleri

Aşağıdaki çizimlerdeki planlar gün düzeyindedir, ancak Planlama Optimizasyonu daha ayrıntılı bir düzeye göre çalıştırılır. Örneğin, kenar boşlukları saat cinsinden olabileceğinden, planlama sipariş süresi 22 Ocak 2021, 11:35 tarihinde olabilir.

### <a name="example-1-simple-scenario"></a>Örnek 1: Basit senaryo

22 Ocak'ta istenen çıkış zamanı olan bir satış siparişi tek bir satınalma siparişi kapsamındadır. Aşağıdaki ayarlar kullanılır:

- Sağlama süresi yok
- Takvim yok (Tüm günler açık.)
- Marj yok

Aşağıdaki şekilde bu senaryo gösterilmiştir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Basit senaryo.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Örnek 2: Sağlama süresi senaryosu

22 Ocak'ta istenen çıkış zamanı olan bir satış siparişi tek bir satınalma siparişi kapsamındadır. Aşağıdaki ayarlar kullanılır:

- Üç günlük sağlama süresi
- Takvim yok (Tüm günler açık.)
- Marj yok

Aşağıdaki şekilde bu senaryo gösterilmiştir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Sağlama süresi senaryosu.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Örnek 3: Marj senaryosu

22 Ocak'ta istenen çıkış zamanı olan bir satış siparişi tek bir satınalma siparişi kapsamındadır. Aşağıdaki ayarlar kullanılır:

- Üç günlük sağlama süresi
- Dört günlük sipariş marjı
- Beş günlük kullanılabilirlik marjı
- Takvim yok (Tüm günler açık.)

Aşağıdaki şekilde bu senaryo gösterilmiştir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Marj senaryosu.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Örnek 4: Gecikme senaryosu

22 Ocak'ta istenen çıkış zamanı olan bir satış siparişi tek bir satınalma siparişi kapsamındadır. Bu örnekte, örnek 3 ile aynı ayarlar kullanılır, ancak planlama tarihi 15 Ocak'a taşınmıştır. Planlı sipariş saatinin bugünün tarihinden önce olması gerektiğinden, geriye doğru planlama (kırmızı işaretleyiciler) başarısız olur. Bu nedenle, ana planlama ileriye yönelik planlama yapmalıdır ve gecikmeler meydana gelir.

Aşağıdaki şekilde bu senaryo gösterilmiştir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Gecikme senaryosu.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Örnek 5: Aktarım senaryosu

22 Ocak'ta istenen çıkış zamanı olan ambar 1'den alınan bir satış siparişi, planlı bir satınalma siparişinin kapsadığı ambar 2'den alınan bir transfer emri kapsamındadır. Aşağıdaki ayarlar kullanılır:

- Üç günlük aktarma sağlama süresi (ambar 1)
- İki günlük satın alma sağlama süresi (ambar 2)
- Takvim yok (Tüm günler açık.)

Aşağıdaki şekilde bu senaryo gösterilmiştir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Aktarım senaryosu.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Örnek 6: Takvimler ile sağlama süresi senaryosu

22 Ocak'ta istenen çıkış zamanı olan bir satış siparişi tek bir satınalma siparişi kapsamındadır. Aşağıdaki ayarlar kullanılır:

- Üç günlük sağlama süresi
- Çıkış takvimi (Cuma günü kapalı)
- Kullanılabilirlik takvimi (Perşembe ve Cuma günleri kapalı)
- Giriş takvimi (Salı günü, Çarşamba ve Pazar kapalı)
- Sağlama süresi takvimi (Perşembe ve Cuma günleri kapalı)
- Sipariş takvimi (Pazartesi ve Cumartesi açık)

Aşağıdaki şekilde bu senaryo gösterilmiştir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Takvimler ile sağlama süresi senaryosu.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Örnek 7: Takvimler ile gecikme senaryosu

22 Ocak'ta istenen çıkış zamanı olan bir satış siparişi tek bir satınalma siparişi kapsamındadır. Bu örnekte, örnek 6 ile aynı ayarlar kullanılır, ancak planlama tarihi 13 Ocak'a taşınmıştır. Planlı sipariş saatinin bugünün tarihinden önce olması gerektiğinden, geriye doğru planlama (kırmızı işaretleyiciler) başarısız olur. Bu nedenle, ana planlama ileriye yönelik planlama yapmalıdır ve gecikmeler meydana gelir.

Aşağıdaki şekilde bu senaryo gösterilmiştir. (Daha büyük bir sürümü açmak için çizimi seçin.)

[![Takvimler ile gecikme senaryosu.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
