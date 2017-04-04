---
title: "Maliyet girişleri"
description: "Bu makalede, maliyeti girişleri ve ne zaman oluşturuldukları hakkında bilgiler verilmektedir. Maliyet girişi, belirli bir etkinliğin miktarının ve maliyetinin yazıldığı bir kayıttır."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 55f5ee731c40acc40e8fe20c24d4ed707fe2c81a
ms.lasthandoff: 03/31/2017


---

# <a name="cost-entries"></a>Maliyet girişleri

Bu makalede, maliyeti girişleri ve ne zaman oluşturuldukları hakkında bilgiler verilmektedir. Maliyet girişi, belirli bir etkinliğin miktarının ve maliyetinin yazıldığı bir kayıttır.

Maliyet girişleri, etkin mali stok boyutlarında kaydedilen stok hareketlerinin toplamıdır.

## <a name="examples"></a>Örnekler
### <a name="example-1-no-cost-entries-are-created"></a>Örnek 1: Hiç maliyet girişi oluşturulmaz.

Bir transfer günlüğü olayı kaydedilmiştir. Olay, bir parça A maddesini A konumundan B konumuna transfer ediyor. Konum stok boyutu, maliyet nesnesinin bir parçası olarak değerlendirilmez. Bu nedenle, olay iki stok hareketi oluşturur; maliyet girişi oluşturmaz.

### <a name="example-2-cost-entries-are-created"></a>Örnek 2: Maliyet girişleri oluşturulur.

Bir transfer günlüğü olayı kaydedilmiştir. Olay bir parçasının 1 siteden siteye 2 aktarır. Site stok boyutu maliyet nesnenin bir parçası olarak kabul edilir. Bu nedenle, olay iki stok hareketi ve iki maliyet girişi oluşturur.

### <a name="example-3-one-cost-entry-is-created"></a>Örnek 3: Bir maliyet girişi oluşturulur.

Bir satınalma siparişi için bir ürün giriş olayı kaydedilir. Olay 100 parça A maddesini 10,00 dolarlık (ABD) bir maliyet birimiyle kaydeder. A maddesi, stok yönetimi amacını izlemek üzere, alınan her bir madde için oluşturulan benzersiz bir seri numarası kullanır. Bu nedenle, olay 100 stok hareketi ve 1 maliyet girişi oluşturur.

## <a name="cost-entries-page"></a>Maliyet girişleri sayfası
Yeni **Maliyet girişleri** sayfası, miktar ve maliyet kayıtlarını görüntüleyip kontrol etmenizi sağlar. Bu sayfa, **Stok hareketi** ve **Stok kapatma** sayfalarını tamamlar. Bir olay için kayıtlar kronolojik sırayla kaydedilir. Bu sayede, bir belgeyle ilgili belirli bir olayın veya tüm olayların birikmiş maliyetlerini hızla bulup kontrol edebilirsiniz. Aşağıda bir örnek verilmiştir:

-   A maddesi için bir ürün giriş olayı kaydedilmiştir. 10,00 dolar birim maliyetiyle yüz parça alınmıştır.
-   Fatura olayı kaydedildikten birkaç gün sonra maliyet 11,00 dolara çıkmıştır. Böylece, toplam tutar 1.100 dolar olur. 100 dolarlık farkı hesaba katmak için ikinci bir fiş oluşturulur.
-   Birkaç gün sonra, satınalma siparişine, ulaştırma maliyetini kapsayan 15,00 dolarlık bir sair gider kaydedilir.

| Fiş | Tarih       | Referans      | Sayı | Lot kodu  | Referans Lotu | İade Lot Kodu | Miktar | Tutar  |
|---------|------------|----------------|--------|---------|---------------|---------------|----------|---------|
| 00001   | 01-01-2015 | Satın alma siparişi | 100001 | 0000101 |               |               | 100,00   | 1000,00 |
| 00002   | 20-01-2015 | Satın alma siparişi | 100001 | 0000101 |               |               |          | 100,00  |
| 00003   | 31-01-2015 | Ayarlama     | 100001 | 0000101 |               |               |          | 15,00   |

**Maliyet girişleri** sayfası, belge numarasına ve belge tarihine göre filtrelemeye olanak sağlar. **Not:** maliyeti girişleri yalnızca için kullanılabilir [nesneleri maliyet](cost-object.md) veya ürünleri serbest.

<a name="see-also"></a>Ayrıca bkz.
--------

[Cost objects](cost-object.md)


