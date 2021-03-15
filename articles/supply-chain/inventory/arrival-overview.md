---
title: Varışa genel bakış
description: Bu konu, Varış genel bakış özelliği hakkında bilgi sağlamaktadır. Varış genel bakış sayfası bu özelliğin bir parçasıdır ve gelen maddelere, varması beklenen maddeler olarak genel bir bakış sağlamaktadır.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 89f885cbbe6a5001b507cd9fb1516733f8faee0f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005289"
---
# <a name="arrival-overview"></a>Varışa genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, Varış genel bakış özelliği hakkında bilgi sağlamaktadır. Varış genel bakış sayfası bu özelliğin bir parçasıdır ve gelen maddelere, varması beklenen maddeler olarak genel bir bakış sağlamaktadır.

**Varış genel bakış** sayfası, tüm beklenen gelen maddelerin özetini sağlar. Bir genel görünüme göre başlatılabilecek varışları da gösterir. Bu konu, alma işlemi üzerine odaklanır.

## <a name="business-scenario"></a>İş senaryosu
Gelen işlemlerinde aşağıdaki senaryoyu düşünün.

[![İş senaryosu](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png)

Bir alıcı memur olan Sami, geçerli tarihte nelerin gelmesinin beklendiğini bilmek ister. **Varış genel bakış** sayfası üzerinde, Sami geçerli görevler hakkında genel bir bakış ve miktarlar, hacim, ağırlık, farklı sipariş türleri ve benzeri şeylerin kaba bir tahminine sahip olabilir. Daha sonra, bir giriş noktasına bir teslimat gelir ve Sami, teslimatın bir listesini alır. **Varış genel bakış** sayfası üzerinde, Sami aşağıdaki görevleri gerçekleştirebilir:

-   Eşleşen giriş siparişlerini tespit edebilir ve girişi **Devam eden** olarak kaydedebilir. Kayıt için gerekli satırlar otomatik olarak oluşturulur ve hareketler henüz **Kaydedildi** olarak deftere nakledilmemiş bile olsa, giriş izlenebilir.
-   Uygun varış günlüğü referansına erişin (yani, **Madde varışı** günlüğü veya **Üretim girişi** günlüğü) ve ürün giriş güncelleştirmesi için hazır olan günlükleri tanımlayın.

## <a name="arrival-overview-page"></a>Varış genel bakış sayfası
**Varış genel bakış** sayfasını açmak için **Stok yönetimi** &gt; **Gelen siparişler** &gt; **Varış genel bakış** üzerine tıklayın. Teslim alınması beklenen siparişlerin bir listesini görebilirsiniz. Genel bakış, başlık ve satırlara ayrılmıştır. Başlık bilgisi, sipariş türüne, beklenen giriş tarihine ve teslimat hedefine göre gruplanır. Bir başlık satırı varış için seçildiğinde, giriş referansıyla ilişkili olan tüm ayrıntı satırları, sayfanın satır ayrıntıları kısmında varış için seçilir. Tüm ilgili günlük satırları deftere nakledildiğinde, bu bilgi gösterilmez.

### <a name="arrival-overview-profiles"></a>Varış genel bakış profilleri

**Varış genel bakış** sayfası, varması beklenen maddeler ve ne zaman varması beklendikleri hakkında genel bir bakış sağlar. Varış işleminin bir parçası olarak, birden fazla kişisel ayar kümesi kullanabilir. Bireysel kullanıcılar, kişisel ayarlarını **Varış genel bakış profilleri** sayfasında tanımlayabilirler.

### <a name="set-up-item-arrival"></a>Madde varışını ayarla

Örneğimizde, Sami yeni bir bilgisayarı, Tesis 1'den gelen mamul malları almakta kullanılacak bir konuma kurmak istiyor. **Varış genel bakış profilleri** sayfasında, Sami **Tesis 1 üretimi** adlı yeni bir kurulum oluşturur ve aşağıdaki ayarları belirtir.

1.  **Varış seçenekleri** hızlı sekmesindeki **Aralık** alan grubunda, bir gün aralığı ve genel bakışa dahil edilecek ambarlar hakkında bilgileri girin.
2.  **Varış seçenekleri** hızlı sekmesindeki **Günlük** alan grubunda, bir alıcı ambar, bir konum ve bir günlük adı girin (madde varışı/üretim girişi).
3.  **Varış sorgu ayrıntıları** hızlı sekmesindeki **Tesis** alan grubunda bulunan **Tesise kısıtla** alanında, genel bakış alanındaki görünümü sınırlamak için bir tesis girin.
4.  **Varış sorgu ayrıntıları** hızlı sekmesindeki **Gösterilen hareket türleri** alan grubunda, **Üretim siparişleri** seçeneğini **Evet** olarak ayarlayın.
5.  **Varış sorgu ayrıntıları** hızlı sekmesindeki **Çeşitli** grubunda, **Başlangıçta güncelleştir** seçeneğini **Evet** olarak ayarlayın, görünüm başlangıçta otomatik güncelleştirilecekse. Aralık değerleri değiştirildiğinde görünüm otomatik güncelleştirilecekse, **Aralık değişikliğini güncelleştir** seçeneğini **Evet** olarak ayarlayın.

Bu örnekte, **Varış genel bakış** sayfasının hızlı sekmesindeki **Varış seçenekleri** hızlı sekmesindeki **Varış genel bakış profil adı** alanı, **Tesis 1 üretimi** olarak ayarlanmıştır.

### <a name="prerequisites-for-arrival-journals"></a>Varış günlükleri için önkoşullar

**Varış genel bakış** sayfasından varış günlüklerini otomatik olarak oluşturmak için **Varış seçenekleri** hızlı sekmesindeki **Günlük** alan grubunda, ilgili bilgileri tanımlamalısınız.

-   Bir günlük oluşturmak için günlük adını belirtmeniz gerekir.

[![Bir günlük adı belirtmek](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   **Ambar** ve **Konum** alanlarında değerleri belirtirseniz, bu değerler günlük satırlarına uygulanır. Değerleri belirtmezseniz, sistem stok hareketinde belirtilen boyuttan değerleri kullanır.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Bir beklenen giriş siparişinden alınan maddeler

**Girişler** hızlı sekmesinde, Sami bir satır seçer ve **Varışa başla** üzerine tıklar. Belirtilen aralıktaki tüm ilgili ve kayıt için bir miktara sahip tüm satırlar, otomatik olarak seçilir. Beklenen giriş siparişi ve günlük arasında eşleşmeye sahip bir madde varış günlüğü oluşturulur. Miktar, oluşturulan tüm satırlarda otomatik olarak başlatılır.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Birden fazla beklenen giriş siparişinden alınan maddeler

**Girişler** hızlı sekmesinde, Sami birden fazla satırı seçer ve **Varışa başla** üzerine tıklar. Tüm beklenen giriş siparişleri ve günlük arasında eşleşmeye sahip madde varış günlüğü oluşturulur. Tüm satırlar bir varış günlüğü başlığında oluşturulur ve miktar otomatik olarak başlatılır.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Bir veya birden fazla beklenen giriş siparişlerinden madde almak

#### <a name="view-information"></a>Bilgileri görüntüle

Bir tarih aralığındaki beklenen girişlerin genel bakışını almak için Sami, aşağıdaki bilgiyi **Varış genel bakış** sayfası üzerinde bulunan **Varış seçenekleri** hızlı sekmesine girer ve görünümü güncelleştirmek için **Güncelleştir** üzerine tıklar:

-   Varış genel bakış profil adı: **Sorgu**
-   Gösterilecek satırlar: **Tümü**
-   Kalan günler: (Boş)
-   İleriki günler: **0**
-   Ambarlar: **GW, MW**

Sami ayrıca aşağıdaki bilgileri görüntüleyebilir:

-   Sistem tarihi için tüm ilgili giriş siparişleri ve ondan önceki sınırsız sayıda gün sayısı (**InventTrans.StatusDate** aralığı) ve GW ve MW ambarlarının girişleri, durumdan bağımsız olarak.
-   Birden fazla sipariş için ayrıntılı satır bilgisi. Sami, genel bakışta birden fazla başlığı seçebilir ve daha sonra **Tüm seçilenleri göster** üzerine tıklayarak, tüm seçilen siparişlere karşılık gelen ayrıntılı satır bilgilerini görebilir.
-   Belirli bir satınalma siparişi hakkında bilgi. Genel bakış içerisindeki yalnızca belirli bir referans numarasıyla ilişkili bilgiyi göstermek için Sami, bir hesap numarasını **Hesap numarası** alanına ve bir sipariş numarasını **Referans numarası** alanına girebilir.
-   Bir varış günlüğünün oluşturulmuş olduğu tüm sipariş satırları için vadesi dolmuş tüm kayıt görevlerinin bir genel bakışı oluşturuldu, ancak henüz deftere nakledilmedi. Sami bu bilgiyi görmek için **Satırları göster** alanındaki **Devam eden** seçeneğini seçebilir.

### <a name="update-journals"></a>Günlükleri güncelleştir

İşlenme süresi gelmiş bir ya da birden fazla sipariş satırını kaydetmek için Sami genel bakış kılavuzu veya satır kılavuzundaki satırları seçebilir ve daha sonra **Günlükler** &gt; **Girişlerden varışları göster** üzerine tıklayabilir. Satırlarla eşleşen madde varış başlıkları gösterilir. Kayıtlı maddeleri güncelleştirmek için satınalma siparişi ürün girişlerini güncelleştirmek amacıyla, Sami halihazırda güncelleştirilmeye hazır olan madde varış günlük başlıklarına erişebilir. Bu madde varış günlük başlıklarına erişmek için **Günlükler** &gt; **Ürün giriş hazır günlükleri** üzerine tıklar. Belirtilen ambardaki ürün giriş güncelleştirmesine hazır olan tüm başlık satırları gösterilir. (Gösterilen başlık satırları, gün aralığıyla ilişkili değildir).

### <a name="start-an-arrival-registration"></a>Bir varış kaydı başlat

Sami, birden fazla satırı **Varış genel bakış** sayfasında seçerek birden fazla giriş referansının varışını başlatabilir. Girişler genel bakıştan bir satır seçtiğinde, karşılık gelen satır ayrıntıları seçilir. Kayıt için miktar mevcutsa, **Varışı başlat** düğmesi kullanılabilir olur. Sami, varış kaydını başlatmak için iki yöntem kullanabilir:

-   Yalnızca belirli bir ölçütü karşılayan kayıtları göstermesi için sayfayı filtrelemek amacıyla, **Satıcı referansı** alanında, örneğin bir teslimat notu için barkod gibi, bir satıcıdan bir referans numarası taratın.
-   **Varış genel bakış** sayfası üzerindeki genel bakış kısmı veya ayrıntılar kısmı içerisinde, varış kaydı için kayıt seçimini elle seçin veya iptal edin. Sami **Varışı başlat** üzerine tıkladığında, seçilen kayıtlar bir madde varış günlüğünde otomatik olarak oluşturulur. Kayıtlara satır bilgisi dahildir ve tüm benzersiz alan bilgisi atanmıştır.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Bir ürün girişi için varış bilgisini güncelleştirin ve işleyin
Tüm mallar kaydedildiğinde, ambar yöneticisi veya satınalma yöneticisi, fiziksel maliyeti eklemek için alınan maddeleri ürün girişi ile güncelleştirebilir. Varış bilgisini güncelleştirmek ve bir ürün girişi deftere nakletmek için aşağıdaki adımları izleyin.

1.  **Stok yönetimi** &gt; **Gelen siparişler** &gt; **Varış genel bakış** üzerine tıklayın.
2.  **Varış genel bakış** sayfasında, bir ürün giriş güncelleştirmesi için hazır olan günlüklerin listesinni göstermek için **Günlükler** &gt; **Ürün giriş hazır günlükleri** üzerine tıklayın.
3.  Güncelleştirilmesi gereken günlükleri seçin ve **İşlevler** &gt; **Ürün girişi** üzerine tıklayın.
4.  **Deftere nakil** sayfası üzerinde, halihazırda günlükte kullanılabilir değilse, ürün giriş numarasını girin ve daha sonra ürün girişini işlemek için **Tamam** üzerine tıklayın.

## <a name="summary"></a>Özet
**Varış genel bakış** sayfası, ambar yöneticisi ve ambar çalışanlarının, gelen işlemlerin parçası olarak gerçekleştirilmesi gereken beklenen iş hakkında bir genel bakış edinmelerine yardımcı olabilir. Sayfa, madde varış işlemini başlatmak, maddelerin ambara ilk girişte izlenmesini garanti etmek için de kullanılabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]