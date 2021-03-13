---
title: Satınalma siparişi oluşturma
description: Bu konu, size bir satınalma siparişinin el ile nasıl oluşturulacağını gösterir.
author: RichardLuan
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventDimParmFixed, InventItemIdLookupPurchase, InventProductDimensionLookup, PurchTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a3da6b70054fac878ba6266017bffe75f634f61
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016640"
---
# <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

[!include [banner](../../includes/banner.md)]

Bu konu, size bir satınalma siparişinin el ile nasıl oluşturulacağını gösterir. Satınalma siparişlerinin master planlama, doğrudan teslimat ve diğer işlemler sonucunda otomatik olarak oluşturulması daha normaldir. Satınalma siparişleri genellikle bir satınalma aracısı tarafından oluşturulur. Buradaki örnek, çeşitli adımlardaki tavsiye edilen notlardaki değerleri kullanarak USMF demo verisi şirketinde kullanılabilir.


## <a name="create-the-purchase-order-header"></a>Satınalma siparişi başlığını oluşturun
1. **Gezinti bölmesi > Modüller > Tedarik ve kaynak atama > Satınalma siparişleri > Tüm satınalma siparişleri** öğesine gidin.
2. **Yeni**'yi seçin.
3. Satıcı hesabı **US-101**'i seçin. Bir satıcı seçtiğiniz zaman, satıcının kaydının adres, fatura hesabı, teslimat koşulları ve teslimat şekli gibi ayrıntıları, sipariş üst bilgisine varsayılan değerler olarak kopyalanır. Bu değerleri istediğiniz zaman değiştirebilirsiniz.  
4. **Genel** bölümünü genişletin.

    - **Site** alanı ve **Ambar** alanı birlikte, satın alınan malların veya hizmetlerin nereye teslim edileceğini belirtir. Site, varsayılan teslimat adresidir. Her iki alan da seçili satıcı için ayarlanan değerlerle doldurulabilir veya el ile belirtilebilir.  
    - **Teslimat tarihi** alanı, satın alınan mal ve hizmetlerin ne zaman teslim edilmesi gerektiğini belirtmek için kullanılır. Bir sipariş için tek bir teslim tarihi belirleyebilir veya her bir sipariş satırı için benzersiz teslim tarihleri verebilirsiniz. Eğer burada belirtilen teslimat tarihi çeşitli ürünler veya hizmetler için, daha uzun temin etme sürelerine sahip oldukları için sağlanamıyorsa, bu satırlar duruma uyum sağlamak için daha sonraki bir teslimat tarihi ile oluşturulurlar.  

5. **Yönetim** bölümünü genişletin. **Sipariş eden** alanı kimin siparişi verdiğini belirtmek için kullanılabilir. Bu, satıcının bu kişiye ulaşması gerekebileceği durumlarda faydalı olabileceği için satıcıya iletilebilir. Bu alan, mevcut kullanıcı ile **Kullanıcılar** sayfasında ilişkilendirilmiş ismi kullanarak otomatik olarak doldurulabilir.  
6. **Tamam**'ı seçin. Sipariş başlığı şimdi oluşturuldu. Satınalma sipariş satırları ile çalışırken, başlık bilgilerinin yalnızca bir özeti gösterilir. Geri kalan bilgileri görüntülemeniz gerekirse, **Başlık**'ı seçin.  

## <a name="add-a-purchase-order-line"></a>Bir satınalma siparişi satırı ekleyin
1. **Satın alma siparişi satırı**'nı seçin.
2. **Boyutlar**'ı seçin. Ürünler, renk, ebat veya stil gibi boyutlar ile ayrıştırılabilecek varyantlara sahip olabilirler. Ürünler ayrıca, site ve ambar gibi depolama boyutları kullanacak şekilde ayarlanabilirler. Ayrıca, toplu iş veya seri numaraları gibi isteğe bağlı izleme boyutları da mevcuttur. Sipariş girişinin verimliliğini artırmak için doğrudan sipariş kılavuzuna sık kullandığınız boyut alanları ekleyebilirsiniz.  
3. **Renk** onay kutusunu işaretleyin. İsteğe bağlı: Eğer **Kurulumu kaydet** alanını seçerseniz, seçtiğiniz boyutlar da sipariş satırı kılavuzda satınalma sipariş sayfası açtığınız bir sonraki seferde gösterilecektir.  
4. **Tamam**'ı seçin.
5. **Öğe numarası** alanında, **T0004**'yi seçin.

    - Ürünler ve hizmetler için sipariş satırları bir madde numarası belirterek veya satın alma kategorisi belirterek giderler olarak oluşturulur. 
    - **Tedarik** kategori alanı, tedarik edilen maddelerin stoka gitmeden doğrudan giderlendirildiği durumlarda satır eklemek için kullanılır. Bu, eğer bir satınalmayı gider göstermeniz gerekiyorsa bunu bir madde numarasına sahip bir satır oluşturmaktansa tedarik kategorisi belirten bir satınalma siparişi satırı oluşturarak yapabileceğiniz anlamına gelir. Maddeler ayrıca bir tedarik kategorisiyle ilişkilendirilebilirler, bu durumda tedarik kategorisi sadece bilgilendirme amaçlı gösterilir.  

6. **Renk** alanına bir değer girin veya buradan bir değer seçin. **Tesis** ve **Ambar** alanları genellikle sipariş başlığından değerlerle doldurulur, ancak bazı satırların farklı konumlara teslim edilmesi gerekiyorsa, alanları geçersiz kılmak mümkündür.  
7. **Miktar** alanına bir sayı girin.

    - Satın almak istediğiniz miktarı seçin. Bu ayarlanmış olması durumunda **Miktar** alanı, ürün için minimum sipariş miktarı ile veya 1 değeri ile otomatik olarak doldurulur.  
    - **Birim** alanı, sipariş edilen miktarın ölçü birimini gösterir. Genellikle, birim otomatik olarak ürün ana veri temel tablosundan sağlanan satınalma biriminden elde edilir, ancak bunu değiştirebilirsiniz.  
    - **Birim fiyatı** alanı, genellikle bir satın alma sözleşmesi veya bir ticaret anlaşmasından bir değer içerir. Örneğin satıcı ile özel bir fiyat üzerinde anlaşıldıysa, birim fiyatını tek tek sipariş satırlarında değiştirmek mümkündür.  
    - **İskonto** alanı, ürün başına bir iskonto tutarı temsil eder. Bu indirim, bu nedenle birim fiyatı iskontoya göre azaltır. Bu indirim genellikle otomatik olarak satın alma anlaşmaları ya da ticari sözleşmelerinden sağlanır, ancak benzersiz indirimler satıcı ile anlaşılmış ise tek tek satırlarda geçersiz kılmak mümkündür.  
    - Satırın net tutarını uygun şekilde azaltan bir iskonto yüzdesi girmek mümkündür. İndirim yüzdesi çoğu zaman otomatik olarak satın alma anlaşmaları ya da ticari sözleşmelerinden sağlanır, ancak benzersiz bir iskonto yüzdesi satıcı ile anlaşılmış ise tek tek satırlarda geçersiz kılmak mümkündür.  
    - **Net tutar** alanındaki değer satırdaki miktar, birim fiyat, iskonto ve iskonto yüzdesi de dahil olmak üzere diğer alanlardan hesaplanır. Net tutarı değiştirmek mümkündür, ancak böyle olduğunda **Birim Fiyat**, **İskonto** ve **İskonto oranı** alanları boş kalır ve satıra doğru naklettiğinizde, nakledilen tutar net tutara orantılı olacaktır. Genellikle **Net tutar** alanı yalnızca satırın net tutarını görüntülemek için kullanılır.  

8. **Satır ayrıntıları** bölümünü genişletin.
9. **Teslimat** sekmesini seçin.Her sipariş satırı için benzersiz bir teslim tarihi atanabilir. Tarih, satınalma siparişi başlığındaki alanından devralınır, ancak bunu değiştirebilirsiniz.  

## <a name="review-order-totals"></a>Sipariş toplamlarını gözden geçirin
1. **Toplamlar**'ı seçin.

    - **Toplamlar** eylemini göremiyorsanız, Eylem Bölmesi'ndeki **Satınalma Siparişi** sekmesini seçin.  
    - Bu iletişim kutusu, tüm sipariş toplamlarını gösterir.  
    - **Seçim** alanı, toplamların hesaplanmasının temelini değiştirmenize izin verir. Örneğin, **ürün giriş miktarı** alınan, veya sipariş edilen miktar, **sipariş edilen ürün miktarı** göstermek için ürünler miktarı için ilgili toplamları göstermek için tercih edebilirsiniz.  

2. **Tamam**'ı seçin.

