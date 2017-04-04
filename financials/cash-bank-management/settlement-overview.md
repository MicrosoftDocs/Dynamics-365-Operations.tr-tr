---
title: "Kapatmaya genel bakış"
description: "Bu makalede kapatma süreci hakkında genel bilgiler verilmiştir. Kapatılabilecek hareketlerin türleri, hareketlerin ne zaman ve nasıl kapatılabileceği ve kapatma sürecinin sonuçları açıklanmıştır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: adbfa6f99c481129e8cbf4a2dc4b23b4be1e8b34
ms.lasthandoff: 03/31/2017


---

# <a name="settlement-overview"></a>Kapatmaya genel bakış

Bu makalede kapatma süreci hakkında genel bilgiler verilmiştir. Kapatılabilecek hareketlerin türleri, hareketlerin ne zaman ve nasıl kapatılabileceği ve kapatma sürecinin sonuçları açıklanmıştır.

Kapatma sırasında, her bir belgenin bakiyesini artırmak veya azaltmak için bir belgedeki hareketler diğer belgelerdeki hareketlere uygulanır. Örneğin, bir fatura için bir ödeme uygulanabilir. Çeşitli hareket tipleri farklı zamanlarda ve çeşitli yöntemler aracılığıyla kapatılabilir. Kapatma yeni hareketlerin üretilmesine de neden olabilir.

## <a name="what-transactions-can-be-settled"></a>Hangi hareketler kapatılabilir
Borç hesapları ve Alacak hesapları dahilindeki kapatmalar, faturalar, ödemeler, alacak makbuzları ve ücretler gibi satıcı bakiyesini veya müşteri bakiyesini etkileyen tüm hareket türleri arasında gerçekleşebilir. Diğer tüm hareket türlerine karşı her hareket türü kapatılabilir. Örneğin, bir faturaya karşı bir ödeme, bir faturaya karşı bir alacak makbuzu, bir faturaya karşı bir fatura ve bir ödemeye karşı bir ödemeyi kapatabilirsiniz. Aynı tüzel kişilikte veya farklı bir tüzel kişilikte bir harekete karşı ödemeleri kapatabilirsiniz. Bir merkezi ödeme modeli kullanan kuruluşlarda [merkezi ödemeler](set-up-centralized-payments.md) ödeme süreci daha verimli yardımcı olabilir.

## <a name="when-to-settle-transactions"></a>Hareketleri ne zaman kapatmalı
Hareketler ödeme girişinin zamanında kapatılabilir. Örneğin, bir satıcıya ödeme yaptığınızda, genellikle ödenecek faturaları seçersiniz. Faturaları seçerek bunları ödeme karşı kapatma için işaretleyin. Alacak hesapları ödeme elemanı bir müşteri ödemesi kaydettiğinizde, bunlar uygun faturalar müşterinin Ödeme ile birlikte gelen bilgilere dayanarak, kapatma için işaretleyebilirsiniz. **Kapatma hareketleri** sayfası hareketleri kapatma için işaretlemede kullanılır. Bu sayfa, herhangi bir deftere nakledilmeyen fatura veya ödemeden açılabilir. Hareket deftere nakledildiğinde kapatma da nakledilir. Hareketler deftere nakledildikten sonra da kapatılabilir. Bir müşteri ödemesini faturalara karşı kapatmadan da girip deftere nakledebilirsiniz. Ancak, öncelikle araştırma yapmanız, ödemenin doğru faturaya karşı kapatıldığından emin olmanız gerekir. **Kapatma hareketleri** sayfası **Tüm müşteriler** veya **Tüm satıcılar** sayfasından ya da herhangi bir müşteri veya satıcıya yönelik **Hareketler** sayfasından açılabilir. Bir fatura için deftere nakledilmiş ön ödemeleri, ödemeyi bir satınalma emri veya satış emrine karşı kapatma için işaretleyerek rezerve etmeniz de mümkündür. Bu durumda, ödeme bir açık Bakiye devam ediyor, ancak başka bir fatura karşı kapatılamaz. Ödeme, satınalma siparişi veya satış siparişi oluşturulan fatura karşı otomatik olarak kapatılacaktır.

## <a name="how-to-settle-transactions"></a>Hareketler nasıl kapatılır
Hareketler el ile, otomatik veya bu iki yöntemin bileşimi ile kapatılabilir. Kapatma yöntemi tercihi, Borç hesapları parametreleri ve Alacak hesapları parametreleri içinde kapatmanın kurulumu üzerinden uygulanabilecek işletme süreçlerine bağlıdır. Ödenecek faturaları seçmede kullanılan bir ödeme teklifi kullanarak satıcı ödemeleri ve müşteri doğrudan borç ödemeleri oluşturabilirsiniz. Ödeme teklifi el ile başlatılan, ancak ödeme oluşturulduğunda sonra Microsoft Dynamics 365 işlemleri için otomatik olarak seçili faturaları kapatma için işaretler. Ödemeler el ile oluşturulduysa, **Kapatma hareketleri** sayfasını kullanarak kapatma için fatura seçebilirsiniz. Faturaları el ile seçebilir veya **Önceliğe göre işaretle** seçeneğini kullanarak faturaları kapatmaya karşı otomatik olarak işaretleyebilirsiniz. **Önceliğe göre işaretle** seçeneği, yalnızca Alacak hesapları için kullanılabilir. Bu seçeneği etkinleştirmek için,Alacak hesapları parametrelerindeki **Kapatma önceliği** sayfasını kullanın. Ödeme memuru bir ödeme girer, ancak bu ödemeyi deftere nakletmeden önce kapatmazsa, ödeme otomatik olarak kapatılabilir. Alacak hesapları parametrelerini ve Borç hesapları parametreleri otomatik kapatma etkinleştirebilirsiniz. Otomatik kapatma kullandığınızda, önceden tanımlanmış kapatma sırası kullanabilir veya kendi kapatma öncelik sırası Alacak hesapları parametrelerinde tanımlayabilirsiniz. Bu işlev yalnızca Alacak hesapları için kullanılabilir.

## <a name="results-of-settlement"></a>Kapatma sonuçları
Hareketler kapatıldıkça, her bir hareketin devreden bakiyesi uygun şekilde artar veya azalır. Bir faturanın veya ödemenin kapatıldığı tipik bir senaryoda, her bir hareketin durumu ve bakiyesi, aşağıdaki kurallara göre güncellenir:

-   Ödeme tutarı fatura tutarından fazla ise, fatura bakiyesi 0,00'a düşürülür ve fatura kapatılır. Ödeme açık kalır; bakiye, ödemenin fatura tutarını aştığı tutardır.
-   Ödeme tutarı fatura tutarından az ise, ödeme bakiyesi 0,00'a düşürülür ve ödeme kapatılır. Fatura açık kalır; bakiye, ödemenin faturadan düşük kaldığı tutardır.
-   Ödeme tutarı fatura tutarına eşitse, hem ödeme hem de fatura kapatılır ve her ikisinin de bakiyesi 0,00 olur.

Bir [ödeme fatura tutarından düşükse](../accounts-payable/vendor-payments-partial-amount.md) (nakit iskontosu, ücret silme veya eksik ödeme yüzünden), fatura ve ödeme, Borç hesapları parametreleri ve Alacak hesapları parametreleri içinde kapatmanın kurulumuna bağlı olarak halen kapatılabilir. Kapatma, hareketler de üretebilir. Örneğin, bir faturanın ve ödemenin kapatılması, nakit iskontosu, gerçekleşmiş kar veya zarar, satış vergisi düzeltmeleri, ücret silme veya kuruş farkları doğurabilir.


