---
title: "Retail Modern POS'ta (MPOS) müşteri siparişleri"
description: "Bu konu, Perakende Modern POS (MPOS) içerisindeki müşteri siparişleri hakkında bilgi sağlar. Müşteri siparişleri, özel siparişler olarak da adlandırılır. Bu konu, ilgili parametreler ve hareket akışları hakkında bir tartışma içerir."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 8025df4f8498efa867f71892b253f71631b731c7
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="customer-orders-in-retail-modern-pos-mpos"></a>Retail Modern POS'ta (MPOS) müşteri siparişleri

[!include [banner](includes/banner.md)]

Bu konu, Perakende Modern POS (MPOS) içerisindeki müşteri siparişleri hakkında bilgi sağlar. Müşteri siparişleri, özel siparişler olarak da adlandırılır. Bu konu, ilgili parametreler ve hareket akışları hakkında bir tartışma içerir.

Çok kanallı perakende dünyasında pek çok perakendeci, çeşitli ürün ve yerine getirme gereksinimlerini karşılamak için müşteri siparişleri seçeneği veya özel siparişler sağlar. Burada bazı tipik senaryolar vardır:

-   Bir müşteri, ürünler belirli bir tarihte belirli bir adrese teslim edilmesini istiyor.
-   Bir müşteri, ürünleri, müşterinin satın aldığı mağazadan başka bir konumda bulunan bir mağazadan teslim almak istiyor.
-   Bir müşteri, müşterinin satın aldığı ürünleri bir başkasının teslim almasını istiyor.

Ayrıca, perakendeciler müşteri siparişlerini, aksi takdirde stok kesintilerinin ortaya çıkabileceği kayıp satışları en aza indirmek için kullanır, çünkü ürünler farklı bir zaman veya yerde teslim edilebilir veya çekilebilir.

## <a name="set-up-customer-orders"></a>Müşteri siparişleri ayarlamak
Müşteri siparişlerinin nasıl karşılandıklarını tanımlamak için **Perakende parametreleri** sayfası üzerinde ayarlanabilecek bazı parametrelerin bunlardır:

-   **Varsayılan depozito yüzdesi** – Siparişin onaylanabilmesi için önce müşterinin ödemesi gereken depozito tutarını belirtin. Varsayılan depozito tutarı, sipariş değerinin bir yüzdesi olarak hesaplanır. Ayrıcalıklara bağlı olarak bir mağaza yetkilisi tutarı **Depozito geçersiz kılma** kullanarak geçersiz kılabilir.
-   **İptal ücreti yüzdesi** – Müşteri siparişi iptal edildiğinde, bir kesinti uygulanacaksa bu giderin tutarını belirtin.
-   **İptal masrafı kodu** – Müşteri siparişi iptal edildiğinde bir masraf uygulanacaksa, bu masraf masraf kodu altında yansıtılacaktır. İptal masrafı kodu tanımlamak için bu parametreyi kullanın.
-   **Kargo masrafı kodu** – Perakendeciler malları müşteriye sevk etmek için ek bir masraf kesebilirler. Bu sevkiyat masrafının tutarı, masraf kodu altında yansıtılır. Bu parametreyi, sevkiyat masraf kodunu müşteri siparişi üzerindeki sevkiyat masrafları ile eşleştirmek için kullanın.
-   **İade kargo ücretleri** – Müşteri siparişi ile ilişkili sevkiyat masraflarının iade edilip edilemeyeceğini belirtin.
-   **Onayı olmadan maksimum tutar** – Sevkiyat masrafları iade edilebilirse, iade siparişleri arasında iade edilebilecek maksimum tutarı belirtin. Bu tutar aşılırsa, iade ile devam etmek için yönetici tarafından geçersiz kılma gereklidir. Aşağıdaki senaryolara karşılık verebilmek için sevkiyat masraflarının iadesi, ilk olarak ödenen tutarı geçebilir:
    -   Masraflar, satış siparişi üstbilgisi seviyesinde uygulanır ve ürün satırının bir miktarı iade edildiğinde, ürünler için izin verilen sevkiyat masrafının maksimum iadesi ve miktar, tüm perakende müşterileri için geçerli olacak bir şekilde belirlenemez.
    -   Sevkiyat giderleri her sevkiyat örneği için alınır. Bir müşteri, ürünleri birden fazla defa iade ederse ve perakendecinin ilkesi, iade sevkiyatı masraflarının karşılanacağını belirtiyorsa, iade sevkiyatı masrafları, gerçek sevkiyat masraflarından fazla olacaktır.

## <a name="transaction-flow-for-customer-orders"></a>Müşteri siparişleri için hareket akışı
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Perakende Modern POS'ta bir müşteri siparişi oluştur

1.  Harekete bir müşteri ekleyin.
2.  Sepete ürünler ekle.
3.  **Müşteri siparişi oluştur** üzerine tıklayın ve daha sonra sipariş türünü seçin. Sipariş türü **Müşteri siparişi** veya **Teklif** olabilir.
4.  **Seçileni sevk et** veya **Tümünü sevk et** üzerine tıklayarak müşteri hesabındaki bir adrese ürünleri sevk edin, istenen sevkiyat tarihini belirtin ve sevkiyat masraflarını belirtin.
5.  Geçerli mağazadan veya başka bir mağazadan belirli bir tarihte çekilecek ürünleri seçmek için **Seçileni çek** veya **Hepsini çek** üzerine tıklayın.
6.  Depozito gerekiyorsa, depozito tutarını tahsil edin.

### <a name="edit-an-existing-customer-order"></a>Geçerli bir müşteri siparişini düzenle

1.  Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.
2.  Düzenlemek için siparişi bulun ve seçin. Sayfanın altında, **Düzenle**'yi tıklatın.

### <a name="pick-up-an-order"></a>Bir siparişi çekmek

1.  Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.
2.  Çekilecek siparişi seçin. Sayfanın altında, **Çekme ve paketleme**'yi tıklatın.
3.  **Çekme** üzerine tıklayın.

### <a name="cancel-an-order"></a>Bir siparişi iptal edin

1.  Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.
2.  İptal edilecek siparişi seçin. Sayfanın altında, **İptal**'i tıklatın.

#### <a name="create-a-return-order"></a>Sipariş iadesi oluşturma

1.  Giriş sayfasında **Bir siparişi bul** üzerine tıklayın.
2.  İade edilecek siparişi seçin, siparişin faturasını seçin ve daha sonra iade edilecek ürünler için ürün satırını seçin.
3.  Sayfanın altında, **Siparişi iade et**'i tıklatın.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Müşteri siparişleri için zaman uyumsuz işlem akışı
Müşteri siparişleri satış noktası (POS) istemcisinden zaman uyumlu ya da zaman uyumsuz modda oluşturulabilir.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Müşteri siparişlerinin zaman uyumsuz modunda oluşturulmasını etkinleştirin

1.  **Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profili** &gt; **İşlev profilleri**'ne tıklayın.
2.  **Genel** hızlı sekmesi üzerinde, **Müşteri siparişlerini zaman uyumsuz modda oluştur** seçeneğini **Evet** olarak ayarlayın.

**Müşteri siparişlerini zaman uyumsuz moda oluştur** seçeneği **Evet** olarak ayarlanmışsa, müşteri siparişleri her defasında zaman uyumsuz modda oluşturulur, Perakende İşlem Hizmeti (RTS) etkin olsa bile. Bu seçeneği **Hayır** olarak ayarlarsanız, müşteri siparişleri her defasında zaman uyumlu modda RTS kullanarak oluşturulur. Müşteri siparişleri zaman uyumsuz modda oluşturulduklarında, Retail içerisine Çekme (P) işleri ile çekilir ve eklenir. Karşılık gelen satış siparişleri, Retail içerisinde **Senkronizasyon siparişleri** elle veya toplu bir iş aracılığıyla çalıştırıldıklarında oluşturulur.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Karma müşteri siparişleri](hybrid-customer-orders.md)




