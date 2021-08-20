---
title: Tedarik ve kaynak atama genel özeti
description: Bu makalede, Tedarik ve kaynak atama modülündeki kullanılabilir işlevlere genel bakış sağlar.
author: kamaybac
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogListPage, CatVendorCatalogListPage, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "58021"
- intro-internal
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ed0ffa7b1e0b48008d4192d9d9a471158dc430d2013740074a6563168ed7194
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775639"
---
# <a name="procurement-and-sourcing-overview"></a>Tedarik ve kaynak atama genel özeti

[!include [banner](../includes/banner.md)]

Bu makalede, Tedarik ve kaynak atama modülündeki kullanılabilir işlevlere genel bakış sağlar.

Tedarik ve kaynak atama, ürün ve hizmet ihtiyacını belirlemeden ürünü satın alma, giriş, faturalama ve satıcılarla ödeme işlemlerine kadar tüm adımları kapsar. Tedarik işlemleri; satınalma ilkeleri ve iş akışları tanımlanarak özel iş ihtiyaçlarına yönelik olarak yapılandırılabilir.

## <a name="identifying-a-need-for-product-and-services"></a>Ürün ve hizmet ihtiyacını belirleme

Ürün ve hizmet ihtiyacı *talepler* sonucunda, örneğin bir çalışan bir ürün istediği zaman ortaya çıkabilir. *Ürün katalogları* aralarından seçim yapılabilecek mevcut ürünlerde seçimi yönlendirecek şekilde ayarlanabilir veya henüz katalogda bulunmayan ürünlere yönelik taleplerde bulunulabilir ve satınalma departmanına ürünün nasıl tedarik edilebileceğini düşünme olanağı verilir.  

*Harcama sınırları* harcama talebini sınırlamak için kullanılabilir ve *satınalma iş akışı* sipariş verilmeden önce onay isteme seçeneği ekler. Ayrıca gerektiğinde, bütçe fon tahsisatını belirtmek de mümkündür.  

Tedarik departmanı gerekli ürün ve hizmetler için tedarikçileri belirler ve bunun içinde birden çok potansiyel tedarikçiye gönderilen bir *teklif talebi* de bulunabilir. Talep edilen ürünün teknik özelliklerini paylaşmak mümkündür ve potansiyel satıcılar bu özelliklere uygun bir ürün teslim edip edemeyeceklerini görmek için bu özellikleri görüntüleyebilir. Satıcılar tekliflerini geri gönderir ve sonrasında bu teklifler satınalma departmanı tarafından alışveriş yapmak istedikleri tedarikçiyi seçmeden önce gözden geçirilir.  

Satınalma siparişleri daha kapsamlı bir teklif talebi sürecine alternatif olarak satıcıya bir *satınalma sorgulaması* gönderme seçeneği içerir. Satınalma sorgulaması, fiyatlar, iskontolar ve sipariş teslimat tarihi gibi şartları belirlemeye yardımcı olmak için kullanılabilir. Satıcılar **Satıcı** portalını kullanacak şekilde ayarlanmışsa, satınalma sorgulaması işlevi devre dışı bırakılır. Bunun yerine sipariş **Satıcı** portalında paylaşılır ve bir *onay isteği* gönderildiğinde, satıcı doğrudan sipariş onaylayabilir.  

*Satıcı katalogları* satıcıların tedarik edebileceği ürün çeşidine ilişkin bilgileri toplamak için kullanılabilir. Satıcılar kendi kataloglarını yayınlayabilir, böylece kataloğu güncel tutmak daha kolaylaşır. Bir ürüne *onaylı satıcı listesi* eklemek mümkündür, bu liste yeni satınalma siparişleri açıldığında satıcı seçiminde yol göstermeye ve istenmeyen satıcıların kullanılmasını önlemeye yardımcı olabilir.

## <a name="procurement"></a>Tedarik

*Satınalma siparişleri* aşağıda belirtilenleri içeren farklı şekillerde oluşturulabilir:

- Bir satın alma işlemi gerektiren bir talep belirlemiş olan master planlamanın sonucu olarak. Bu işlem planlı satınalma siparişleri oluşturur ve bunlar serbest bırakıldığında, satınalma siparişi oluşturulur.
- Sonucunda tedariki sağlayan satınalma taleplerinin işlenmesi yoluyla.
- Satınalma siparişlerinin anlaşmalardan serbest bırakılmış siparişler olarak oluşturulduğu satınalma anlaşmalarına ilişkin işlemler yoluyla. Bu yoldan genellikle satınalma anlaşmaları paket siparişleri temsil etmek için kullanıldığında yararlanılır.
- Oluşturulan satınalma siparişi başka bir belgeye dayalı olmadığında, el ile.

*Satınalma onayı iş akışları* ile yapılandırılmış satınalma siparişlerinin, onaylı olarak kaydedilmeden önce onay alması ve bunun da sipariş daha ileri düzeyde işlenmeden önce yapılması gerekir.

Satınalma siparişleri, satıcıyla bir anlaşmaya varıldığını ifade etmek için *teyit edilir*. Satınalma siparişi daha sonra en son faturalandırılana veya iptal edilene kadar kademeli olarak farklı durumlardan geçecektir.  

Bir satınalma siparişi oluşturduğunuzda, alanların çoğu **Satıcılar** sayfasında satıcılar hakkında depolanan bilgilerden varsayılan olarak alınan değerlerle önceden doldurulmuştur. Bu durum, varsayılan değerleri geçersiz kılmak seçeneğiniz bulunmakla birlikte, satınalma siparişinde doldurulması gereken sınırlı sayıda alan olduğu anlamına gelir.

### <a name="prices-and-discounts"></a>Fiyatlar ve iskontolar

Fiyatlar ve iskontolar; fiyatlar, iskontolar ve sundukları indirim koşulları hakkında bilgiler içerir. Fiyatlar ve iskontolar, *ticaret anlaşmaları* olarak ifade edilebilir. Ticaret anlaşmaları fiyatları veya iskontoları içeren satıcı fiyat listelerini ifade eder ve bu anlaşmalarda anlaşmanın geçerli olduğu belli bir tarih kümesi bulunur. Fiyatlar ve iskontolar, pazarlık edilen şartların ön koşulu olarak belli hacimler veya parasal tutarlar alma taahhütleri gibi koşulları içeren *satınalma anlaşmaları* yoluyla görüşülebilir ve temsil edilebilir. Satıcılarla *İndirim anlaşmaları* oluşturulabilir ve bu anlaşmalara göre, belli ürünlerin veya ürün gruplarının tedariki satınalma tutarı veya hacmine bağlı olarak satıcının indirim yapmasını sağlayabilir.

### <a name="delivery-options"></a>Teslimat seçenekleri

Bir satınalma siparişiyle ilişkili teslimat işlemi için farklı seçenekler vardır. Sipariş edilen ürünler *teslimat* planlarına bölünebilir, burada sipariş edilen miktarın parçaları farklı tarihlerde teslim edilecek şekilde planlanabilir. Teslimat, ürün girişinin satınalma siparişine kaydedildiği anda satış siparişinde otomatik olarak sevk irsaliyesi oluşturan bir satış siparişinden başlatılan *doğrudan teslimat* ı da içerebilir. Satınalma siparişleri, şirketlerarası satınalma siparişleri olarak da belirtilen, ürünlerin eşleşen bir şirketlerarası satış siparişinden sipariş edildiği *şirketlerarası sipariş* zincirinin de bir parçası olabilir.. Bu durumda, bazı adımlar iki ilgili şirketlerarası sipariş arasında otomatik olarak gerçekleşir.

### <a name="supplementary-items"></a>Tamamlayıcı maddeler

Ürünleri *tamamlayıcı öğeleri* içerek şekilde ayarlayabilirsiniz. Bunun amacı sipariş edilen ürünle ilgili ürünler önermektir. Ek ürünler, gerekli olabilir veya isteğe bağlı olabilir. Bazı durumlarda, tamamlayıcı maddeler, diğer ürünlerin satın alınmasına eşlik eden ücretsiz ürünler olarak eklenebilir.

### <a name="purchase-order-charges"></a>Satınalma siparişi masrafları

Bir satınalma siparişine masraflar atanabilir. Bu işlem, otomatik masraflar ayarlanmak suretiyle otomatik olarak veya masraflar elle eklenerek yapılabilir. Masraflar başlık düzeyinde veya sipariş satırı düzeyinde siparişe atanabilir. Masrafların muhasebesi farklı şekillerde ayarlanabilir. Örneğin, bir masrafı bir ürün maliyeti olarak hesaba katılacak şekilde ayarlayabilirsiniz. Bunu yaparsanız, siparişiniz onaylanmadan önce masrafların sipariş satırı düzeyinde atanması gerekir. Masrafları sipariş başlığından satırlara tahsis etmeye yardımcı olabilen bir seçenek vardır.

## <a name="product-receipt-and-invoicing"></a>Ürün girişi ve faturalandırma

Fiziksel ürünler içeren satınalma siparişleri, yaygın şekilde, bir ambarda yapılacak *varış kaydı* gerektirir ve bundan sonra sipariş için bir *ürün girişi* kaydedilir. İstekleri yerine getiren ürünleri içeren satınalma siparişleri, ürünleri talep eden çalışanın bir *giriş onayı* da sağlaması gerekecek şekilde yapılandırılabilir.  

Bazı satınalma siparişleri, bir ambara alınmasına gerek olmayan hizmet şeklindeki ürünleri veya diğer fiziksel olmayan ürünleri içerir. Ürünler, hizmetler olarak oluşturulabilir veya *tedarik kategorileri* bu tür siparişler için satınalma siparişinde doğrudan kullanılabilir. Bu siparişler ile, ürün giriş muhasebesi bazen atlanır ve sipariş doğrudan faturalandırılır veya alternatif olarak ürün giriş kaydı önceden varış kaydı olmadan satınalma siparişinde yapılır.  

Ürünlerin girişi belirli bir amaç doğrultusunda otomatik tüketime yol açabilir. Bunun içinde doğrudan teslimatla örtülü tüketim, bir projeye yönelik tüketim veya ürünü bir sabit kıymet olarak hesaba katma bulunur.  

Satıcıdan *satıcı faturaları* geldiğinde, bunlar satınalma siparişinden bağımsız olarak öncelikle *fatura kaydı* nda kaydedilir ve sonra satınalma siparişine karşı bir kayıt olarak onaylanır. Satınalma siparişi ile satıcı faturasını kaydetme, fatura doğrultusunda ürün girişini eşleştirmeyi içerir.  

*Muhasebe dağıtımları* muhasebenin genel muhasebe içinde nasıl yapılması gerektiğini tarif edecek şekilde satınalma siparişinde belirtilebilir ve ayrıca yapılandırmanıza dahil edildiğinde bütçe fon tahsisatının nasıl elde edildiğini de tanımlayabilir.  

Faturalanan satınalma siparişleri, borcu borç hesapları içindeki satıcı hesabına kaydeder ve buradan *satıcı ödemesi* işlenebilir.

## <a name="vendor-performance"></a>Satıcı performansı

Satınalma performansı ve incelemesi, içinde harcama analizinin ve satıcı performans analizinin bulunduğu *tedarik ve borç hesabı raporları* yoluyla desteklenir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]