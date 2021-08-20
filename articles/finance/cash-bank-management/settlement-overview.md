---
title: Kapatmaya genel bakış
description: Bu konuda kapatma süreci hakkında genel bilgiler verilmiştir. Hangi hareket türlerinin kapatılabileceğini, bunları kapatmaya yönelik zamanlamayı ve işlemi açıklar. Ayrıca, kapatma işleminin sonuçlarını da açıklar.
author: kweekley
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14551"
- intro-internal
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 30a96b377d70c74a29e9e90699ccb077c727b20758378b5336660c6c056c6022
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755702"
---
# <a name="settlement-overview"></a>Kapatmaya genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda kapatma süreci hakkında genel bilgiler verilmiştir. Hangi hareket türlerinin kapatılabileceğini, bunları kapatmaya yönelik zamanlamayı ve işlemi açıklar. Ayrıca, kapatma işleminin sonuçlarını da açıklar.

Kapatma sırasında, her bir belgenin bakiyesini artırmak veya azaltmak için bir belgedeki hareketler diğer belgelerdeki hareketlere uygulanır. Örneğin, bir faturaya bir ödeme uygulanabilir. Çeşitli hareket türleri farklı zamanlarda ve farklı yöntemlerle kapatılabilir. Kapatma işlemi yeni hareketler de oluşturabilir.

## <a name="what-transactions-can-be-settled"></a>Hangi hareketler kapatılabilir

Borç hesapları ve Alacak hesaplarında kapatma, satıcı bakiyesini veya müşteri bakiyesini etkileyen tüm hareket türleri arasında gerçekleşebilir. Bu hareket türleri arasında fatura, ödeme, iade faturası ve ücretler bulunabilir. Diğer tüm hareket türlerine karşı her hareket türü kapatılabilir. Örneğin, bir faturaya karşı bir ödeme, bir faturaya karşı bir alacak makbuzu, bir faturaya karşı başka bir fatura ve bir ödemeye karşı başka bir ödemeyi kapatabilirsiniz.

Aynı tüzel kişilikte veya farklı bir tüzel kişilikte bir harekete karşı ödemeleri kapatabilirsiniz. Merkezi ödeme modeli kullanan organizasyonlarda, [merkezi ödemeler](set-up-centralized-payments.md) ödeme sürecini kolaylaştırabilir.

## <a name="when-to-settle-transactions"></a>Hareketleri ne zaman kapatmalı

Hareketler, ödemeler girildikten sonra kapatılabilir. Örneğin, bir satıcıya ödeme yaptığınızda, genellikle ödenecek faturaları seçersiniz. Faturaları seçerek bunları ödemeyle kapatma işareti koyun. Alacak Hesapları ödeme memurları müşteri ödemelerini kayda geçirirken, her müşterinin ödemesine eklenen bilgiler temelinde uygun faturalara kapatma işareti koyabilirler. **Kapatma hareketleri** sayfasını hareketleri kapatma için işaretlemek üzere kullanırsınız. Bu sayfayı, herhangi bir deftere nakledilmemiş fatura veya ödemeden açabilirsiniz. Hareket deftere nakledildiğinde kapatma da nakledilir. 

Hareketler deftere nakledildikten sonra da kapatılabilir. Bir müşteri ödemesini faturalara karşı kapatmadan da girip deftere nakledebilirsiniz. Ancak, kapatmayı deftere nakletmeden önce araştırma yapmak, ödemenin doğru faturaya karşı kapatıldığından emin olmak isteyebilirsiniz. **Kapatma hareketleri** sayfası **Tüm müşteriler** veya **Tüm satıcılar** sayfasından ya da herhangi bir müşteri veya satıcıya yönelik **Hareketler** sayfasından açılabilir.

Bir fatura için deftere nakledilmiş ön ödemeleri, ödemeyi bir satınalma emri veya satış emrine karşı kapatma için işaretleyerek rezerve etmeniz de mümkündür. Bu durumda, ödemede açık bakiye devam eder ancak başka bir faturaya karşılık olarak kapatılamaz. Ödeme, satınalma siparişinden veya satış siparişinden oluşturulan faturaya karşılık otomatik olarak kapatılacaktır.

## <a name="how-to-settle-transactions"></a>Hareketler nasıl kapatılır

Hareketler el ile, otomatik veya bu iki yöntemin bileşimi ile kapatılabilir. Kapatma yöntemi seçimi, iş süreçlerinize bağlıdır. **Borç hesapları parametreleri** ve **Alacak hesapları parametreleri** sayfalarında, kapatma işlemini bu iş süreçleriyle uyumlu olacak şekilde yapılandırabilirsiniz.

Ödeme teklifi kullanarak satıcı ödemeleri ve müşteri doğrudan borç ödemeleri oluşturabilirsiniz. Ödeme teklifi ödeme yapılacak faturaları seçmek için kullanılır. Ödeme teklifi el ile başlatılır ve ardından sistem ödemeler oluşturulduğunda seçilen faturaları kapatma için otomatik olarak işaretler.

Ödemeler el ile oluşturulduysa, **Kapatma hareketleri** sayfasını kullanarak kapatma için fatura seçebilirsiniz. Faturaları el ile seçebilir veya **Önceliğe göre işaretle** seçeneğini kullanarak faturaları kapatmaya karşı otomatik olarak işaretleyebilirsiniz. **Önceliğe göre işaretle** seçeneği, yalnızca Alacak hesapları için kullanılabilir. Bu seçeneği **Alacak hesapları parametreleri** sayfasındaki **Kapatma önceliği** sekmesinde açabilirsiniz.

Ödeme memuru bir ödeme girer, ancak bu ödeme deftere nakledilmeden önce kapatmazsa, ödeme otomatik olarak kapatılabilir. **Alacak hesapları parametreleri** ve **Borç hesapları parametreleri** sayfalarında otomatik kapatmayı etkinleştirebilirsiniz. Otomatik kapatma, hareketleri yalnızca aynı tüzel varlıkta kapatır. Birden çok tüzel kişilikteki hareketleri kapatmaz.

Otomatik kapatma kullandığınızda, önceden tanımlanmış kapatma önceliği kullanabilir veya **Alacak hesapları parametreleri** sayfasında kendi kapatma öncelik sıranızı tanımlayabilirsiniz. Bu işlev yalnızca Alacak hesapları için kullanılabilir.

## <a name="results-of-settlement"></a>Kapatma sonuçları

Hareketler kapatıldıkça, her bir hareketin devreden bakiyesi uygun şekilde artar veya azalır. Genellikle, bir fatura veya ödeme kapatıldığında, her bir hareketin durumu ve bakiyesi, aşağıdaki kurallara göre güncellenir:

- Ödeme tutarı fatura tutarından fazla ise, fatura bakiyesi 0,00'a düşürülür ve fatura kapatılır. Ödeme açık kalır ve bakiye, ödeme tutarı ile fatura tutarı arasındaki farktır.
- Ödeme tutarı fatura tutarından az ise, ödeme bakiyesi 0,00'a düşürülür ve ödeme kapatılır. Fatura açık kalır ve bakiye, fatura tutarı ile ödeme tutarı arasındaki farktır.
- Ödeme tutarı fatura tutarına eşitse, hem ödeme hem de fatura kapatılır ve her ikisinin de bakiyesi 0,00'a düşürülür.

[Ödeme tutarı fatura tutarından düşükse](../accounts-payable/vendor-payments-partial-amount.md) (nakit iskontosu, ücret silme veya eksik ödeme yüzünden), fatura ve ödeme **Borç hesapları parametreleri** ve **Alacak hesapları parametreleri** sayfasındaki kapatma yapılandırmasına bağlı olarak, yine de kapatılabilir.

Kapatmalar hareketler de üretebilir. Örneğin, bir faturanın ve ödemenin kapatılması, nakit iskontosu, gerçekleşmiş kar veya zarar, satış vergisi düzeltmeleri, ücret silme veya kuruş farkları doğurabilir.

## <a name="identifying-marked-transactions-during-settlement"></a>Kapatma sırasında işaretlenen hareketleri tanımlama

Bir hareketi kapatmaya çalıştığınızda, hareketin başka bir konumda işaretlendiğini gösteren bir sembol görebilirsiniz. Bu durumda, **Kareketleri kapat** sayfasında hareketi seçebilir ve **Sorgula \> Kapatma penceresinden kapatma**'yı seçebilirsiniz. Bu sorgu görünümü, hareketin kapatılmasını engelleyebilecek olan günlükler, satış siparişleri, faturalar, ödeme teklifleri ve müşteri yerleşimlerini gösterir. Sorunu çözmek için, doğrudan sorgudan engellenen konuma gidecek bağlantıyı seçebilirsiniz. Daha sonra belgeyi, bunu kapatmak için gereken ayarlamalarla güncelleştirebilirsiniz. Ayrıca, aynı engelleme konumuna dahil edilen diğer belgeleri tanımlamak için **İşaretlendi** göstergesini de kullanabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalanı kapat](settle-remainder.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]