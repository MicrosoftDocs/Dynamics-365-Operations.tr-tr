---
title: Satınalma siparişi oluşturma
description: Bu yordam, size bir satınalma siparişinin el ile nasıl oluşturulacağını gösterir.
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ad846ba14b05f8e7d34aff2e3a256cc9b3b56c1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838130"
---
# <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, size bir satınalma siparişinin el ile nasıl oluşturulacağını gösterir. Satınalma siparişlerinin master planlama, doğrudan teslimat ve diğer işlemler sonucunda otomatik olarak oluşturulması daha normaldir. Satınalma siparişleri genellikle bir satınalma aracısı tarafından oluşturulur. Buradaki örnek, çeşitli adımlardaki tavsiye edilen notlardaki değerleri kullanarak USMF demo verisi şirketinde kullanılabilir.


## <a name="create-the-purchase-order-header"></a>Satınalma siparişi başlığını oluşturun
1. Tedarik ve kaynak atama > Sipariş emirleri > Tüm sipariş emirleri öğesine gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı US-101'i seçin.
    * Bir satıcı seçtiğiniz zaman, satıcının kaydının adres, fatura hesabı, teslimat koşulları ve teslimat şekli gibi ayrıntıları, sipariş üst bilgisine varsayılan değerler olarak kopyalanır. Bu değerleri istediğiniz zaman değiştirebilirsiniz.  
4. Genel bölümünü genişletin.
    * Site alanı ve Ambar alanı birlikte, satın alınan malların veya hizmetlerin nereye teslim edileceğini belirtir. Site, varsayılan teslimat adresidir. Her iki alan da seçili satıcı için ayarlanan değerlerle doldurulabilir veya el ile belirtilebilir.  
    * Teslimat tarihi alanı, satın alınan mal ve hizmetlerin ne zaman teslim edilmesi gerektiğini belirtmek için kullanılır. Bir sipariş için tek bir teslim tarihi belirleyebilir veya her bir sipariş satırı için benzersiz teslim tarihleri verebilirsiniz. Eğer burada belirtilen teslimat tarihi çeşitli ürünler veya hizmetler için, daha uzun temin etme sürelerine sahip oldukları için sağlanamıyorsa, bu satırlar duruma uyum sağlamak için daha sonraki bir teslimat tarihi ile oluşturulurlar.  
5. Genel bölümünü daraltın.
6. Yönetim bölümünü genişletin.
    * Sipariş eden alanı kimin siparişi verdiğini belirtmek için kullanılabilir. Bu, satıcının bu kişiye ulaşması gerekebileceği durumlarda faydalı olabileceği için satıcıya iletilebilir. Bu alan, mevcut kullanıcı ile Kullanıcılar sayfasında ilişkilendirilmiş ismi kullanarak otomatik olarak doldurulabilir.  
7. Yönetim bölümünü daraltın.
8. Tamam'a tıklayın.
    * Sipariş başlığı şimdi oluşturuldu. Satınalma sipariş satırları ile çalışırken, başlık bilgilerinin yalnızca bir özeti gösterilir. Geri kalan bilgileri görüntülemeniz gerekirse, Başlık'a tıklatın.  

## <a name="add-a-purchase-order-line"></a>Bir satınalma siparişi satırı ekleyin
1. Satınalma siparişi satırına tıklayın.
2. Boyutlar'a tıklayın.
    * Ürünler, renk, ebat veya stil gibi boyutlar ile ayrıştırılabilecek varyantlara sahip olabilirler. Ürünler ayrıca, site ve ambar gibi depolama boyutları kullanacak şekilde ayarlanabilirler. Ayrıca, toplu iş veya seri numaraları gibi isteğe bağlı izleme boyutları da mevcuttur. Sipariş girişinin verimliliğini artırmak için doğrudan sipariş kılavuzuna sık kullandığınız boyut alanları ekleyebilirsiniz.  
3. Renk onay kutusunu işaretleyin.
    * İsteğe bağlı: Eğer Kurulum alanını kaydetmeyi seçerseniz, seçtiğiniz boyutlar da sipariş satırı kılavuzda satınalma sipariş sayfası açtığınız bir sonraki seferde gösterilecektir.  
4. Tamam'a tıklayın.
5. Madde numarası alanında T0004 seçin.
    * Ürünler ve hizmetler için sipariş satırları bir madde numarası belirterek veya satın alma kategorisi belirterek giderler olarak oluşturulur.  
    * Tedarik kategori alanı, tedarik edilen maddelerin stoka gitmeden doğrudan giderlendirildiği durumlarda satır eklemek için kullanılır. Bu, eğer bir satınalmayı gider göstermeniz gerekiyorsa bunu bir madde numarasına sahip bir satır oluşturmaktansa tedarik kategorisi belirten bir satınalma siparişi satırı oluşturarak yapabileceğiniz anlamına gelir. Maddeler ayrıca bir tedarik kategorisiyle ilişkilendirilebilirler, bu durumda tedarik kategorisi sadece bilgilendirme amaçlı gösterilir.  
6. Renk alanına bir değer girin veya buradan bir değer seçin.
    * Tesis ve Ambar alanları genellikle sipariş başlığından değerlerle doldurulur, ancak bazı satırların farklı konumlara teslim edilmesi gerekiyorsa, alanları geçersiz kılmak mümkündür.  
7. Miktar alanına bir sayı girin.
    * Satın almak istediğiniz miktarı seçin. Bu ayarlanmış olması durumunda Miktar alanı, ürün için minimum sipariş miktarı ile veya 1 değeri ile otomatik olarak doldurulur.  
    * Birim alanı, sipariş edilen miktarın ölçü birimini gösterir. Genellikle, birim otomatik olarak ürün ana veri temel tablosundan sağlanan satınalma biriminden elde edilir, ancak bunu değiştirebilirsiniz.  
    * Birim fiyatı alanı, genellikle bir satın alma sözleşmesi veya bir ticaret anlaşmasından bir değer içerir. Örneğin satıcı ile özel bir fiyat üzerinde anlaşıldıysa, birim fiyatını tek tek sipariş satırlarında değiştirmek mümkündür.  
    * İskonto alanı, ürün başına bir iskonto tutarı temsil eder. Bu indirim, bu nedenle birim fiyatı iskontoya göre azaltır. Bu indirim genellikle otomatik olarak satın alma anlaşmaları ya da ticari sözleşmelerinden sağlanır, ancak benzersiz indirimler satıcı ile anlaşılmış ise tek tek satırlarda geçersiz kılmak mümkündür.  
    * Satırın net tutarını uygun şekilde azaltan bir iskonto yüzdesi girmek mümkündür. İndirim yüzdesi çoğu zaman otomatik olarak satın alma anlaşmaları ya da ticari sözleşmelerinden sağlanır, ancak benzersiz bir iskonto yüzdesi satıcı ile anlaşılmış ise tek tek satırlarda geçersiz kılmak mümkündür.  
    * Net tutar alanındaki değer satırdaki miktar, birim fiyat, iskonto ve iskonto yüzdesi de dahil olmak üzere diğer alanlardan hesaplanır. Net tutarı değiştirmek mümkündür, ancak böyle olduğunda Birim Fiyat, İskonto ve İskonto oranı alanları boş kalır ve satıra doğru naklettiğinizde, nakledilen tutar net tutara orantılı olacaktır. Genellikle Net tutar alanı yalnızca satırın net tutarını görüntülemek için kullanılır.  
8. Satır ayrıntıları bölümünü genişletin.
9. Teslimat sekmesine tıklayın.
    * Her sipariş satırı için benzersiz bir teslim tarihi atanabilir. Tarih, satınalma siparişi başlığındaki alanından devralınır, ancak bunu değiştirebilirsiniz.  
10. Satır ayrıntıları bölümü daraltın.

## <a name="review-order-totals"></a>Sipariş toplamlarını gözden geçirin
1. Toplamlar öğesine tıklayın.
    * Toplamları eylemini göremiyorsanız, eylem çubuğundaki Satınalma Siparişi sekmesini tıklatın.  
    * Bu iletişim kutusu, tüm sipariş toplamlarını gösterir.  
    * Seçim alanı, toplamların hesaplanmasının temelini değiştirmenize izin verir. Örneğin, ürün giriş miktarı alınan, veya sipariş edilen miktar, sipariş edilen ürün miktarı göstermek için ürünler miktarı için ilgili toplamları göstermek için tercih edebilirsiniz.  
2. Tamam'a tıklayın.

