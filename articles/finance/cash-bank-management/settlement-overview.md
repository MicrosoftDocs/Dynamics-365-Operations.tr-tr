---
title: Kapatmaya genel bakış
description: Bu konuda kapatma süreci hakkında genel bilgiler verilmiştir. Hangi hareket türlerinin kapatılabileceğini, bunları kapatmaya yönelik zamanlamayı ve işlemi açıklar. Ayrıca, kapatma işleminin sonuçlarını da açıklar.
author: panolte
ms.date: 07/30/2021
ms.topic: overview
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
ms.openlocfilehash: 57f2b209a852bb9513218fab3df118c7d7a2a1e7
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986395"
---
# <a name="settlement-overview"></a>Kapatmaya genel bakış

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


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

## <a name="resolve-issues-with-transactions-that-cant-be-settled"></a>Kapatılamayan hareketlerle ilgili sorunları çözme

Bazen belgeyi o anda başka bir faaliyet işlemekte olduğu için hareketleri kapatamazsınız. Hareketleri kapatmaya çalıştığınızda bu hareketler kullanımda olduğu için bir hata oluşur. Bu sorunu gidermek için kapatmak üzere **İşaretli hareket ayrıntıları** sayfasını kullanarak işaretlenen hareketleri bulabilir ve bunlara erişim sağlayan diğer işlemleri belirleyebilirsiniz.

Hareketler, satıcı faturaları ödendiğinde veya müşteriler açık faturalarını ödediklerinde kapatma için işaretlenirler. Bazen, bu faturalar kapatma için zaten işaretlenmiş olabilir. Bu nedenle, kullanıcılar ödeme için bunları seçemezler. Faturalar, geçerli tüzel kişilikte veya başka bir tüzel kişilikte başka bir müşteri ödeme günlüğü, satış siparişi, satıcı ödeme günlüğü veya satın alma siparişi tarafından işaretlenebilir.

Müşteri ödemesini girerken bir hareketin kapatılması engellenirse **Müşteri tarafından işaretlenen hareket ayrıntıları** sayfasını (**Alacak hesapları \> Periyodik görevler \> Müşteri tarafından işaretlenen hareket ayrıntıları**) açın. Hareketin nerede engellendiğini hızlı bir şekilde belirlemek için şu seçim parametrelerinden herhangi birini ayarlayabilirsiniz: **Müşteri hesabı**, **Fiş**, **Tarih** veya **Fatura**. Herhangi bir seçim parametresi ayarlamazsanız sistem, geçerli şirket veya seçtiğiniz başka bir şirket tarafından engellenen tüm belgeleri gösterir. Kapatma için bloke edilen hareket tanımlandıktan sonra onu seçebilir ve ardından **Seçili hareketlerin işaretini kaldır**'ı belirleyebilirsiniz. Seçili hareket daha sonra onu içeren herhangi bir günlükten kaldırılır. Ancak belge diğer konumdan kaldırılmaz. Bu günlükten yalnızca işaretleme bilgileri kaldırılır.

Satıcı ödemesini girerken bir hareketin kapatılması engellenirse **Satıcı tarafından işaretlenen hareket ayrıntıları** sayfasını (**Borç hesapları \> Periyodik görevler \> Satıcı tarafından işaretlenen hareket ayrıntıları**) açın. Hareketin nerede engellendiğini hızlı bir şekilde belirlemek için şu seçim parametrelerinden herhangi birini ayarlayabilirsiniz: **Satıcı hesabı**, **Fiş**, **Tarih** veya **Fatura**. Herhangi bir seçim parametresi ayarlamazsanız sistem, geçerli şirket veya seçtiğiniz başka bir şirket tarafından engellenen tüm belgeleri gösterir. Hareket tanımlandıktan sonra onu seçebilir ve ardından engelleme sorununu gidermek için **Seçili hareketlerin işaretini kaldır**'ı seçebilirsiniz. Seçilen hareket daha sonra seçildiği diğer günlüklerden kaldırılır. Ancak belge diğer konumdan kaldırılmaz. Bu günlükten yalnızca işaretleme bilgileri kaldırılır.

Engellenen tüm belgeleri belirlemek için **Tüm işaretli hareket ayrıntıları** sayfasını (**Alacak hesapları \> Periyodik görevler \> Tüm işaretli hareket ayrıntıları** veya **Borç hesapları \> Periyodik görevler \> Tüm işaretli hareket ayrıntıları**) açın. Hareketin nerede engellendiğini hızlı bir şekilde belirlemek için şu seçim parametrelerinden herhangi birini ayarlayabilirsiniz: **Müşteri hesabı**, **Satıcı hesabı**, **Fiş**, **Tarih** veya **Fatura**. Herhangi bir seçim parametresi ayarlamazsanız sistem, geçerli şirket veya seçtiğiniz başka bir şirket tarafından engellenen tüm belgeleri gösterir. Hareket tanımlandıktan sonra onu seçebilir ve ardından engelleme sorununu gidermek için **Seçili hareketlerin işaretini kaldır**'ı seçebilirsiniz. Seçilen hareket daha sonra seçildiği diğer günlüklerden kaldırılır. Ancak belge diğer konumdan kaldırılmaz. Bu günlükten yalnızca işaretleme bilgileri kaldırılır.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için **özellik yönetimi** çalışma alanını kullanabilir. Burada, özellik aşağıdaki şekilde listelenmiştir:

- **Modül:** Nakit ve banka yönetimi
- **Özellik adı:** İşaretli hareket ayrıntısı formu

## <a name="additional-resources"></a>Ek kaynaklar

- [Kalanı kapat](settle-remainder.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
