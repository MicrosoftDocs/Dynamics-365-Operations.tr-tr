---
title: "Müşteri siparişleri genel bakış"
description: "Bu konu, müşteri siparişleri, perakende Modern POS (MPOS) hakkında bilgi sağlar. Müşteri Siparişlerini özel siparişler de verilir. Konu bir tartışma ilgili parametreler ve hareket akışları içerir."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Müşteri siparişleri genel bakış

Bu konu, müşteri siparişleri, perakende Modern POS (MPOS) hakkında bilgi sağlar. Müşteri Siparişlerini özel siparişler de verilir. Konu bir tartışma ilgili parametreler ve hareket akışları içerir.

Omni-kanal perakende dünyasında, siparişleri veya çeşitli ürün ve yerine getirme gereksinimlerini karşılamak için özel siparişler Perakendeciler birçok müşterinin seçeneği sağlar. Burada, bazı tipik senaryolar vardır:

-   Müşteri belirli bir tarihte belirli bir adrese teslim edilecek ürünler istiyor.
-   Bir müşteri ürünleri bir mağaza veya depodan farklı konum veya konum nerede müşteri bu ürünleri satın alması istiyor.
-   Bir müşteri, Müşteri satın alınan ürünler çekmek için başkası istemektedir.

Perakendeciler müşteri siparişleri malları teslim ya da farklı bir zaman veya yer toplanma nedeni, hisse senedi kesintileri Aksi takdirde, neden olabilir kayıp satış en aza indirmek için de kullanabilirsiniz.

## <a name="set-up-customer-orders"></a>Müşteri siparişlerini kurun
Ayarlanabilir parametreler bazıları şunlardır **perakende parametreleri** nasıl müşteri siparişleri karşılandıktan tanımlamak için sayfa:

-   **Depozito yüzdesi varsayılan** – sipariş onaylanabilmesi için önce müşterinin ödemesi gereken tutarı bir depozito belirtin. Varsayılan depozito tutarı sipariş değerinin bir yüzdesi olarak hesaplanır. Mağaza çalışanı ayrıcalıklara bağlı olarak, tutar kullanarak geçersiz kılmak mümkün olabilir **havale geçersiz kılma**.
-   **İptal ücreti yüzde** – müşteri siparişi iptal edildiğinde, bir şarj uygulanacaksa bu gideri tutarını belirtin.
-   **İptal ücreti kod** – müşteri siparişi iptal edildiğinde bir gider gider bir gider kodu altında Microsoft Dynamics AX'te satış siparişine yansıtılır uygulanacaktır. İptal ücreti kodu tanımlamak için bu parametreyi kullanın.
-   **Kargo ücreti kod** – Perakendeciler malları müşteriye sevkiyat için ek bir ücret şarj. Bu sevkiyat gideri tutarını altında gider kodu Dynamics AX'de satış siparişine yansıtılır. Giderleri Müşteri siparişin sevkiyat için sevkiyat gider kodunun eşlemek için bu parametreyi kullanın.
-   **Kargo ücretleri iade** – müşteri siparişiyle ilişkili kargo ücretleri hiçbir ödemenin iadesi yapılmaz edilip edilmeyeceğini belirtin.
-   **Maksimum Tutar onayı olmadan** – kargo ücretleri hiçbir ödemenin iadesi yapılmaz, en büyük farkı para iadelerini iade siparişlerinin sevkiyat miktarını belirtin. Bu tutarı aşarsa Yöneticisi geçersiz kılma iadesi ile devam etmek için gereklidir. Aşağıdaki senaryolarda yapabilmek için ilk olarak ödenen tutar Kargo iadesi aşabilir:
    -   Bazı bir ürün satırının miktarı döndürülür, ürünler için izin verilen maksimum iadesi giderleri yollarının ve tüm perakende müşteriler için uygun şekilde miktarı belirlenemiyor giderler satış siparişi başlığının ve düzeyinde uygulanır.
    -   Sevkiyat giderleri sevkiyat her örneği için alınan. Bir müşteriye birden çok kez ürünleri verir ve satıcıya iade kargo ücretleri maliyeti size aittir, Satıcısı'nın İlkesi belirtiyorsa, birden çok asıl kargo ücretleri iade kargo ücretleri olacaktır.

## <a name="transaction-flow-for-customer-orders"></a>Müşteri siparişleri için işlem akışı
### <a name="create-a-customer-order-in-retail-modern-pos"></a>İçinde Modern POS perakende müşteri siparişi oluşturma

1.  Harekete bir müşteri ekleyin.
2.  Ürünleri Sepete ekleyin.
3.  ' I **müşteri siparişi oluşturmak**ve sonra sipariş tipini seçin. Sipariş tipi olabilir **müşteri siparişi** veya **teklif**.
4.  ' I **seçilen sevk** veya **tüm sevk** adresine ürünleri müşteri hesabında sevk etmek istenen sevkiyat tarihi belirtin ve kargo ücretleri belirtin.
5.  ' I **seçili malzeme çekme** veya **toplama tüm** geçerli mağaza ya da farklı bir mağaza belirli bir tarihte çekilir ürünleri seçmek için.
6.  Depozito tutarı bir depozito gerekiyorsa toplayın.

### <a name="edit-an-existing-customer-order"></a>Varolan bir müşteri siparişi gir

1.  Giriş sayfasında tıklatın **sipariş bulma**.
2.  Bulmak ve düzenlemek için siparişi seçin. Sayfanın alt kısmında,'ı **düzenleme**.

### <a name="pick-up-an-order"></a>Bir sipariş Seç

1.  Giriş sayfasında tıklatın **sipariş bulma**.
2.  Sipariş almak için seçin. Sayfanın alt kısmında,'ı **çekme ve ambalaj**.
3.  ' I **almak**.

### <a name="cancel-an-order"></a>Siparişi iptal etme

1.  Giriş sayfasında tıklatın **sipariş bulma**.
2.  Siparişi iptal etmek için seçin. Sayfanın alt kısmında,'ı **iptal**.

#### <a name="create-a-return-order"></a>Sipariş iadesi oluşturma

1.  Giriş sayfasında tıklatın **sipariş bulma**.
2.  Dönmek, sipariş için faturayı seçin ve sonra verilecek mallar için ürün satırı seçmek için siparişi seçin.
3.  Sayfanın alt kısmında,'ı **iade siparişi**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Müşteri siparişleri için zaman uyumsuz işlem akışı
Müşteri siparişleri satış (POS) istemci noktasından zaman uyumlu veya zaman uyumsuz modu oluşturulabilir.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Zaman uyumsuz modunda oluşturulan müşteri siparişlerini etkinleştirin

1.  Dynamics AX'ı **perakende ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS profil**&gt;**işlevsellik profilleri**.
2.  Üzerinde **genel** hızlı, set **zaman uyumsuz modunda müşteri siparişi oluşturmak** için seçenek **Evet**.

Zaman **zaman uyumsuz modunda müşteri siparişi oluşturmak** seçeneği ayarlanmış **Evet**, müşteri siparişleri her zaman uyumsuz modunda oluşturulan, perakende, hatta hareket hizmeti (RTS) kullanılabilir. Bu seçeneği ayarlamak, **No**, müşteri siparişleri her zaman oluşturulur eşzamanlı modda RTS kullanarak. Zaman uyumsuz modunda müşteri siparişleri oluşturulduğunda, bunlar çekilen ve Dynamics AX çeker (P) işleri tarafından eklendi. İlişkili satış siparişlerini Dynamics AX uygulamasında oluşturulan zaman **eşitleme siparişleri** el ile veya bir toplu işlem aracılığıyla çalıştırın.

<a name="see-also"></a>Ayrıca bkz.
--------

[Karma müşteri siparişleri](hybrid-customer-orders.md)


