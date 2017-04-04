---
title: "Sipariş girişi sırasında ürünleri ve ürün çeşitlerini arama"
description: "Satış veya satınalma siparişi satırını el ile oluşturduğunuzda ürünleri ve ürün çeşitlerini aramak için <strong>Madde numarası </strong>alanını kullanın.  Bu, yalnızca yapılandırma dizesine sahip olduğunuzda veya ürün boyutlarından biri kullanılabilir olduğunda ürün çeşitlerini hızlı bir şekilde bulmanızı sağlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: MCRFullTextIndexField, MCRFullTextParameters, PurchTable, SalesTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 248534
ms.assetid: 99dd5ce1-0029-4f06-90e7-865e6d46d86e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 5b0f3c1a853f8f5e61dedaf588b6f9d2da3a53b5
ms.lasthandoff: 03/31/2017


---

# <a name="search-for-products-and-product-variants-during-order-entry"></a>Sipariş girişi sırasında ürünleri ve ürün çeşitlerini arama

Satış veya satınalma siparişi satırını el ile oluşturduğunuzda ürünleri ve ürün çeşitlerini aramak için <strong>Madde numarası </strong>alanını kullanın.  Bu, yalnızca yapılandırma dizesine sahip olduğunuzda veya ürün boyutlarından biri kullanılabilir olduğunda ürün çeşitlerini hızlı bir şekilde bulmanızı sağlar.

Bazı durumlarda, çok olan bir satış siparişinde koymak için doğru ürünü bulmak için madde numaraları veya ürün arama adlarını hatırlamak çalıştığınız bir şeylerin çoğunu, olacak şekilde en iyi duruma değil ve bu çok sayıda benzer ürünler satıyorsanız özellikle doğrudur. Kullanabileceğiniz **madde numarası** alan bir satış siparişi satırı veya arama alanı olarak bir satınalma siparişi satırı. Ürün adı, numarası veya boyutunun herhangi bir bölümünü girebilir ve arama kelimesi ile eşleşen tüm maddeleri görüntüleyen bir arama yapabilirsiniz.

## <a name="how-search-works"></a>Arama nasıl yapılır
Ürünleri veya ürün çeşitlerini ararken, arama özelliğinin girdiğiniz metinle eşleşen ürünleri nasıl bulduğunu anlamak önemlidir. Arama sonuçlarının sunulmasında anahtar arama kuralları şunlardır:

-   Arama sonuçları, arama metninin girildiği alanı yok sayarak eşleşen kayıtları getirir.
-   Arama metninin tamamının eşleşme kaydında bulunması gerekir.
-   Arama metni, eşleşme kaydındaki metin dizesinin ortasında olsa bile eşleşme gerçekleşir. Metin dizesinin başında olması gerekmez.
-   Arama metni boşluk karakteri içerse bile tek bir metin dizesi olarak kabul edilir.

### <a name="examples"></a>Örnekler

Aşağıdaki örnekler ürün ve ürün çeşitlerini kullanarak çeşitli senaryolarda arama işleminin nasıl yapıldığını gösterir. **Önkoşul:** altında **satış ve pazarlama &gt;Kurulum &gt;arama &gt;arama parametreleri**&gt;**arama türü**, select **tam eşleşme** seçeneği.

| Ürün türü     | Ürün adı    | Görüntülenen ürün numarası | Madde kodu | Yapılandırma |
|------------------|-----------------|------------------------|-------------|---------------|
| Benzersiz ürün | SpeakerMidRange | D0001                  | D0001       | Yok            |
| Ürün varyantı  | Etkin hoparlör  | D0010:::Siyah:         | D0010       | 000005        |
| Ürün varyantı  | Etkin hoparlör  | D0010:::Beyaz:         | D0010       | Beyaz         |

**Madde numarası** alanına "hopar" yazarsanız arama sonucu olarak yukarıdaki tüm ürünleri alırsınız. **Madde numarası** alanına "siyah" yazarsanız sonuç olarak ikinci ürünü alırsınız, çünkü görüntülenen ürün numarasında 'siyah' metni bulunur. Bu iki örnek aramanın yalnızca alanın başında değil arama metni eşleşme kaydındaki metin dizesinin ortasında bulunsa bile bir eşleşmenin olacağını gösterir.  

"05" yazarsanız sonuç olarak yalnızca ikinci ürün çeşidini alırsınız çünkü yapılandırmada "05" bulunur. Bu, aramanın **Arama ölçütleri** sayfasında etkinleştirilmiş tüm alanlar arasında olduğunu gösterir.  

"hopar 05" yazarsanız sonuç alamazsınız. Bunun nedeni aramanın, girilen metnin tamamı için arama yapmasıdır. Arama "hopar" metnini bulmaya çalışmaz ve ardından sonuçları "05" içerenlere daraltır.  

Kullanarak arama sonucu sayısını sınırlayabilirsiniz **sonuç sayısı** alanına **satış ve pazarlama &gt;Kurulum &gt;arama &gt;arama parametreleri** sayfa. Bu alanı 0 olarak ayarlarsanız tüm arama sonuçları gösterilir. Örneğin, 10 olarak ayarlarsanız en fazla 10 arama sonucu gösterilir.

## <a name="configure-the-product-search"></a>Ürün aramasını yapılandırma
Ürün ve ürün çeşidi arama özelliğini kullanmadan önce ürün aramayı yapılandırmak için şu adımları izleyin. [![Ürün arama yapılandırmak için 3 adımı\_AXAppFall](./media/3-steps-to-configure-product-search_axappfall.png)](./media/3-steps-to-configure-product-search_axappfall.png)

### <a name="step-1-include-all-the-relevant-product-and-product-variant-identifiers-and-dimensions-in-the-search-criteria"></a>Adım 1: Tüm ilgili ürün ve ürün çeşidi kimlik tanımlayıcılarını ve boyutlarını arama ölçütlerine dahil edin

**Ürün adı, Madde numarası**, **Görüntülenen ürün numarası, Yapılandırma, Renk, Boyut, Stil, Arama adını vb.** arama yapmak için kullanabileceğiniz ürün ve ürün çeşidi kimlik tanımlayıcılarına ve boyutlarına örneklerdir.  

Git **satış ve pazarlama &gt;Kurulum &gt;arama &gt;arama ölçütünü** sayfa. **Arama ölçütleri** sayfası, müşteri, aday müşteri ve ürün araması için ölçütleri tanımlamanıza izin verir. Ürün arama ölçütlerini kullanarak sayfayı filtrelediğinizden emin olun. Bunu, sayfa menüsünde **Ürün**'e değiştirerek yapabilirsiniz.  

Arama ölçütü görüntüleme ürün numarası eklemek için tıklatın **yeni** sayfa menüsünde. Bunu yeni bir kayıt eklemek **arama ölçütünü** kılavuz. **Alan adı** arama sütununu açın ve **DisplayProductNumber**'ı seçin. Ürünün yapılandırması için arama ölçütü eklemek için yeni bir kayıt oluşturun ** arama ölçütünü ** kılavuz ve seçtiğiniz **configId**, **alan adı** sütun. Aynı şekilde renk boyutu için **Alan adı** **InventColorId**, ebat boyutu için **InventSizeId** ve stil boyutu için **InventStyleId** olan bir kayıt oluşturun.

### <a name="step-2-populate-the-database-table-that-is-used-for-product-search"></a>Adım 2: Ürün araması için kullanılan veritabanı tablosunu doldurun

**Arama ölçütleri** sayfasında **Arama verilerini güncelleştir** düğmesine tıklayın. **Arama verilerini güncelleştir** iletişim kutusunda **Kaynak**'ın **Ürün** olarak ayarlandığından emin olun ve ardından **Tamam**'a tıklayın. Sistem bir tabloda 1. adımda belirtilen tüm seçili arama ölçütlerine birleştirir. Bir çok ürün ve ürün çeşitleri varsa, bu işlem oldukça uzun olabilir ve bir uyarı alabilirsiniz. Arama tablosu doldurma işlemini, toplu iş sunucusunda, sunucunun çok yoğun olmadığı bir zamana planlamanızı öneririz.  

Tablo doldurulana kadar ürün arama doğru sonuç vermez. Arama sonucu alamıyorsanız bu tablonun doldurulduğundan emin olun.  

Tablo yalnızca arama ölçütleri değiştirildiğinde doldurulmak zorundadır. Yeni yayımlanan ürünler ve çeşitler tabloya otomatik olarak eklenir. Silinen ürünler ve çeşitler tablodan otomatik olarak çıkarılır.

### <a name="step-3-enable-the-lookup-for-product-search-on-sales-and-purchase-order-lines"></a>Adım 3: Satış ve satınalma siparişi satırlarında ürün arama için aramayı etkinleştirin

Giderek bu işlevi etkinleştirebilirsiniz **satış ve pazarlama &gt;Kurulum &gt;arama &gt;arama parametreleri** ve ayar **etkinleştir arama için arama** için **Evet** üzerinde **genel** sekme.  

Satış siparişi satırı girişi için **Madde numarası** alanına yazmaya başladığınızda ve ardından **Sekme** tuşuna bastığınızda varsayılan davranış, **Ürün arama** sayfasını açmaktır. **Ürün arama** sayfası sipariş satırı oluşturma sırasında bağlamı değiştirir ve gereksiz bir eklenti olarak düşünülebilir. Arama sonuçlarını bir aramada almayı ve sipariş satırı girişi sırasında bağlamı kaybetmemeyi tercih ederseniz bunun yerine aramayı kullanabilirsiniz. Bir ürün veya ürün çeşidi için arama yapıyorsanız ancak aramada herhangi bir şey seçmediyseniz ve **Sekme** tuşuna basarsanız **Ürün arama** sayfası görüntülenir.


