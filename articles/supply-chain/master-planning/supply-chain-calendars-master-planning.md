---
title: Takvimler ve master planlama
description: Bu makale tedarik zinciri takvimleri ve master planlamayı nasıl etkiledikleri hakkında genel görünüm sağlar.
author: t-benebo
ms.date: 08/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 182c22a77e73573b4e27a81f80debf67242b95c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890987"
---
# <a name="calendars-and-master-planning"></a>Takvimler ve master planlama

[!include [banner](../includes/banner.md)]

Bu makale tedarik zinciri takvimleri ve master planlamayı nasıl etkiledikleri hakkında genel görünüm sağlar.  Ana planlama altyapısında kullanılan farklı takvimler ve bunların planlanan siparişlerin sevkiyat ve teslim alma tarihleri üzerindeki etkisi açıklanır. Son olarak takvimlerin atanması, kullanımı ve güncelleştirilmesine ilişkin öneriler verilir.

## <a name="definition-of-a-calendar"></a>Bir takvimin tanımı

Kuruluşunuzun sayfasında kullanmak üzere bir takvimi, **Kuruluş yönetimi > Ayar > Takvimler > Takvimler** sayfasında tanımlayabilirsiniz. 

Takvimdeki her bir tarih girişi **açık** veya **kapalı** veya **temel takvim** olabilir. Bu, **Çalışma zamanları** sayfasında **Denetim** sütununda belirtilir. Her bir tarih için: 
- **Açık** - İşin seçilen gün gerçekleştirildiğini gösterir. Takvim, çalışma zamanı şablonuna göre güncelleştirilir.
- **Kapalı** - Gün içinde gerçekleştirilmeyen işi gösterir. 
- **Temel takvim** - Belirli bir tarihin çalışma saatlerini ve açık/kapalı durumunu temel takviminden alır. Bu nedenle, temel takvim güncelleştirildiğinde, seçilen takvim buradaki operasyon saatlerini alır. 

Tüm kapatma tarihleri için **Çekme için kapatıldı** onay kutusu otomatik olarak atanacaktır. Açık tarihler için **Malzeme çekme için kapalı** seçeneğini otomatik olarak seçebilirsiniz. Bu, işin tarihinde gerçekleştirildiğini, ancak sevkiyatın gerçekleştirilmediğini gösterir. 

## <a name="calendars-that-affect-master-planning"></a>Master planlamayı etkileyen takvimler

### <a name="calendar-for-a-coverage-group"></a>Karşılama grubu için bir takvim
Bir karşılama grubu, belirli bir karşılama grubuna ait öğelerin stok yenilemesi iiçin kullanılan ortak parametre kümesini belirtir. 

Bir takvimi bir karşılama grubuna eklemek için **Master Planlama > Kurulum > Karşılama > Karşılama grupları**'na gidin. Takvimi atamak istediğiniz karşılama grubunu bulun ve sonra **Takvim** alanında seçin.

Karşılama grubu farklı sayfalarda atanabilir: 
    - Bir öğenin **Serbest bırakılan ürün ayrıntıları** sayfasında. Bir öğe için karşılama grubunu görmek için **Ürün bilgisi yönetimi > Ürünler > Serbest bırakılan ürünler**'e gidin, öğeyi seçin ve **Serbest bırakılan Ürün Ayrıntıları** sayfasına gidin. Öğe karşılama grubunu **Plan** hızlı sekmesinde görebilirsiniz.
    - **Öğe karşılama** sayfasında. Serbest bırakılan ürün ayrıntıları sayfasında, **Öğe karşılaması** üzerine tıklayın ve öğe karşılama sayfasına gidin. Genel bakış sekmesinde, stok yenileme için farklı parametreleri tesis, ambar ve ürün boyutlarına göre görebilirsiniz. Her bir öğe için karşılama grubu **Serbest bırakılan ürün ayrıntıları** sayfasının karşılama grubundan alınacaktır. Bu, **Beliri ayarları kullan** veya **Grup ayarlarını geçersiz kıl** ayarıyla **Genel** sekmesinde geçersiz kılınabilir.
    - **Master planlama parametreleri** sayfasında. Bir öğe önceki sayfalarda bir karşılama grubu ayarlanmamışsa, master planlama genel karşılama grubunu kümesini master planlama parametrelerine götürecektir. Bu, **Genel karşılama grubu** alanında **Master planlama > Kurulum > Master planlama parametreleri** ayarlanır. 

### <a name="calendar-for-a-vendor"></a>Bir satıcı için takvim
Bir satıcının çalışma günlerini belirtmek için bir satınalma takvimini satıcıya **Satınalma sipariş varsayımları** sayfasında bir satıcı için atayabilirsiniz. 

Bir satıcı için bir takvim ayarlamak için takvimi **Kuruluş Yönetimi > Takvimler > Takvimler** içinde oluşturmanız gerekir. Takvim oluşturulduğunda, bunu satıcıya atamanız gerekir. **Borç Hesapları > Satıcılar > Tüm satıcılar**'a gidin ve takvimi atamak istediğiniz satıcıyı seçin. Daha sonra, satıcının sayfasında **Satınalma siparişi varsayımları** hızlı sekmesinde, yeni satınalma takvimini açılır menüyü kullanarak atayın. 

Bir satıcı için takvim, satınalma siparişinin yerleştirilmesini kabul ettikleri günleri ve siparişleri şirketinize teslim edebilecekleri tarihleri belirtir. Sonuç olarak, satıcı için satınalma siparişleri için sipariş tarihleri, takvimde açık olarak tanımlanmış olacaktır. Bu siparişler için teslimat tarihleri açık günlerde olacaktır ve bu nedenle satın alınan öğenin sağlama süresine etki edecektir. 

#### <a name="define-the-lead-time-for-a-purchased-item"></a>Satın alınan öğe için sağlama süresini tanımlayın

Bir öğe için satınalma sağlama süresini belirtmek için (ve yalnızca çalışma günleri dikkate alınacaksa), ürün için varsayılan sipariş ayarları sayfasına gitmeniz gerekir, bunu **Ürün bilgisi yönetimi > Ürünler > Serbest bırakılan ürünler** altında bulabilirsiniz ve **Varsayılan sipariş ayarlarını** seçin. 

> [!Note]
> Satınalma sağlama süresi altındaki **Çalışma günleri**, satıcının çalışma günlerini belirtir. Örneğin, yalnızca Salı günleri 10 günlük sağlama süresi ve iş günleri onay kutusu işaretlenmiş şekilde ile teslim edilecek bir takvim, öğenin teslim edilmesinin 10 hafta (10 Salı) süreceğini belirtmektedir.
Bu nedenle, pek çok durumda iş günlerini satınalma siparişi sağlama süreleri için seçmek önerilmez.

#### <a name="define-lead-times-from-the-trade-agreements-page"></a>Ticaret sözleşmeleri sayfasından sağlama sürelerini tanımlayın

Master planlama, satıcılar için tüm ticari sözleşmeleri dahil etmek üzere ayarlanabilir. Ticari sözleşmeler sabit fiyatlar veya indirim sözleşmeleridir ve bunlar bir veya birden fazla müşteri veya satıcı için tekil veya çoklu ürünün satışı veya satın alınması için ayarlanır. **Master planlama > Kurulum > Master planlama parametreleri**'ne ve **Planlanan siparişler** sekmesine gidin ve **Ticari sözleşmeler bul**'u seçerek planlama yaparken ticari sözleşmeleri dahil edin. Master planlama satıcıyı **Minimum sağlama süresi** veya **En düşük birim fiyatı** ile seçebilir.

### <a name="calendar-for-a-warehouse"></a>Bir ambar için takvim
Bir takvimi bir ambara atayabilir ve bu sayede alma ve gönderme için açık tarihleri belirtebilirsiniz. Hiçbir takvim bir ambara atanmadaysa, her gün açık olduğu kabul edilir. 

> [!Note]
> Bir takvimi bir transit ambara atamanın hiçbir etkisi olmaz. Transit ambarlar transfer emirlerini desteklemekte kullanılır. Siparişler için uygulanabilir sevkiyat veya alım tarihleri açık günler ile "Kaynak" ambardan ve "Hedef" ambardan ve teslimat takviminin modundan tanımlanır.

#### <a name="closed-for-pickup-policy"></a>Malzeme çekme için kapalı ilkesi
Bir ambarın alıma açık olduğunu ancak çekmenin mümkün olmadığını belirtmek için **Çekme için kapalı ilkesi**'ni ambar takvimi içinde kullanabilirsiniz. Bu, müşteri çekmeleri için de uygulanır. 

### <a name="transport-calendar"></a>Taşıma takvimi 
Bir **Kaynak ambardan** transfer siparişlerini nakletmek için kullanılabilir günleri belirtmek için bir **Transfer takvimi** atayabilirsiniz. Teslimat moduna göre bir taşıma takvimi ayarlayabilirsiniz veya bir ambardan telsimat moduna göre. Taşıma takvimi **Satış ve pazarlama > Kurulum > Dağıtım > Teslimat modları** içinde ayarlanır. Br teslimat modu seçin ve **Transfer takvimi** düğmesine tıklayın.

Bir hat her bir ambar ve teslimat modu için oluşturulabilir, takvimin **Teslimat takvimi** sütununa eklenmiş olduğunda. Ürünler ambardan belirli bir teslimat modu kullanılarak taşındıklarında uygulanacak bir taşıma takvimini belirtir. Bir taşıma takvimini belirli bir teslimat modu kullanarak tüm sevkiyatlara uygulamak için bir satır ambar belirtmeden oluşturulabilir.  Belirtilen teslimat modunu kullanan tüm sevkiyatları etkiler, ambardan bağımsız olarak. 

Bir taşıma takvimi atanmamışsa, tüm günlerin taşıma için açık olduğu kabul edilir.

### <a name="calendar-for-a-customer"></a>Bir müşteri için takvim
Bir müşterinin teslimat kabul edebileceği tarihleri belirtmek için bir giriş takvimini müşteriye atayabilirsiniz. Hiçbir takvim bir müşteriye atanmamışsa, müşterinin her gün sipariş kabul edebileceği varsayılır. bu, satış sipariş satırındaki giriş tarihini etkiler. Satış siparişi satırında müşteri takviminde "açık" olmayan bir tarih seçerseniz, sistem giriş tarihinin geçerli olmadığını belirtir. 

Müşteri başına yalnızca bir takvim dahil etmenin mümkün olduğuna dikkat edin. Bir takvimi her bir farklı müşteri adresi için dahil etmeniz gerekirse, adres başına bir müşteri oluşturabilir ve karşılık gelen takvimini atayabilirsiniz. 

Satış siparişi satırındaki talep edilen alındı tarihi müşterinin takviminden ve teslimat tarihi denetim modundan etkilenir. En erken teslimat tarihinin nasıl hesaplandığına dair daha fazla bilgiyi [Sipariş Taahhüt](/dynamics365/unified-operations/supply-chain/sales-marketing/delivery-dates-available-promise-calculations) içinde okuyabilirsiniz.

### <a name="shipping-calendar-for-a-legal-entity"></a>Tüzel bir varlık için sevkiyat takvimi
Bir tüzel varlığın malları sevk edebileceği tarihleri belirtmek için bir teslimat takvimini **Kuruluş yönetimi > Kuruluşlar > Tüzel varlıklar** altında ayarlayabilirsiniz. Tüzel varlığı seçin ve takvimi **Sevkiyat takvimi** alanında bulunan **Dış ticaret ve lojistik** sekmesinde ekleyin. Sevkiyat takvimi tüzel varlık içindeki tüm ambar takvimleri için varsayılanların bir kaynağı olarak iş görür. 

## <a name="how-calendars-affect-dates-in-planning"></a>Takvimlerin planlama tarihlerini nasıl etkilediği

### <a name="order-date-of-a-planned-purchase-order"></a>Planlanan bir satınalma siparişinin sipariş tarihi 
Bir planlanan satınalma siparişi içindeki sipariş tarihi, siparişin verildiği tarihi belirtir. Hem satıcı takviminde hem de kapsama grubu takviminde açık bir tarih olacaktır. Bazen, satıcıların satınalma siparişini almaları ve ürünleri sevk edebilmeleri arasındaki birkaç gün boşluğa ihtiyaçları vardır. Bu tarihleri, satıcının marj günü sayısı içinde belirtilir. Ancak, marj güne sahip bir satın alınan öğe bir kapsama grubuna atanmışsa, bu marj günleri satıcının marj günlerini geçersiz kılacaktır.

### <a name="delivery-date-of-a-planned-purchase-order"></a>Planlanan bir satınalma siparişinin teslimat tarihi
Bir satın almanın giriş tarihi, ürünleri alacağınız tarihi belirtir. Takvimde bir açık tarih olacaktır. Satınalma siparişlerinin alınabileceği günler aşağıdaki takvimde, en yüksek öncelikten başlayarak en düşüğe doğru dikkate alınır: 
1. Satıcının takvimi
1. Teslimat grubu takvimi
1. Giriş yapılan ambar için ambar takvimi

Kapsama grubu takvimi, farklı sayfalarda ayarlanabilir ve aşağıdaki sıralamayı öncelik olarak alacaktır:
1. **Madde karşılama** sayfasındaki madde karşılama grubu
1. **Serbest bırakılan ürün ayrıntıları** sayfasındaki öğe kapsama grubu
1. **Master planlama parametreleri** içindeki varsayılan madde kapsama grubu

### <a name="shipping-date-of-a-planned-transfer-order"></a>Planlanan transfer siparişlerinin sevk tarihi
İki ambar arasında bir transfer siparişi oluştururken, sevkiyat tarihi ve giriş tarihi transfer siparişi başlığında, "Kaynak" ambar ve "Hedef" ambar ile birlikte dahil edilir. Bu iki tarih arasındaki fark, ambarlar arasındaki beklenen taşıma süresidir (gün cinsinden).

Planlanan bir transfer siparişinin sevk tarihi, ürünlerin "Kaynak" ambardan sevk edildikleri tarihi gösterir. Takvimlerik, kullanılabilir sevkiyat tarihlerini belirtmek için önceliğe göre listelenir: 
1. "Kaynak" ambardan ambar takvimi
1. Kapsama grubu takvimi (bu takvim için yukarıdaki geri dönüş sırasına bkz.) Bir ambar takvim kümesi varsa, sevkiyat tarihi takvimdeki açık bir gün olacaktır. Takvim kümesinde bir ambar yoksa, kapsama grubu takvimini alacaktır. 

### <a name="receipt-date-of-a-planned-transfer-order"></a>Planlanan transfer siparişlerinin giriş tarihi
Bir transfer siparişi için giriş tarihi, ürünlerin "Hedef" ambarda alındığı tarihi belirtir.

Giriş tarihlerini belirtmek için kullanılan takvimler, önceliğe göre listelenir: 
1. Teslimat grubu takvimi 
1. Bir kapsama takvimi kümesi varsa, "Hedef" ambarın ambar takvimi, giriş tarihi takvimdeki açık bir gün olacaktır. Bir kapsama grubu takvim kümesi yoksa, ambar takvimini alacaktır. 

Planlanan transfer için sevkiyat ve alım tarihlerini bulurken, kullanıcı tarafından sevkiyat ve alım için belirlenen marjlar da dikkate alınır. 

## <a name="using-calendars-in-master-planning"></a>Master planlamada takvimleri kullanmak

### <a name="assignment-of-scm-calendars"></a>SCM takvimlerin ataması
Takvimlerin şirketin çalışma günlerini tanımlamaya ayarlanması önemlidir. En iyi uygulama, her bir öğe için farklı çalışma günlerine sahip bir takvim ayarlamaktır. Başka bir deyişle, tüm harici takvimler (müşteri, satıcı) ve şirket ile ilişkili tüm dahili (ambar, kapsama grubu ve teslimat modu).

### <a name="recommendation-on-warehouse-calendars"></a>Ambar takvimleri için öneri
Yalnızca ambarı etkileyen belirli değişiklikleri dahil etmek için ambar başına bir takvim kullanmak önerilir. Örneğin, iki veya daha fazla ambar aynı iş günlerine ancak farklı bir çekme ilkesine sahip olabilir. Bu durumda, her bir ambar için bir takvim karşılık gelen çekme ilkesi ile, satınalma, transfer ve üretim siparişlerini dahil etmek için sistem için en iyi uygulamadır. Ambar takvimi ayarlanmamışsa, tüzel varlık takvimi, ambar takvimi için bir varsayılan kaynağı olabilir. 

### <a name="recommendation-of-coverage-group-calendars"></a>Grup takvimlerinin kapsaması için öneri
Kapsama grubu takvimine ilişkin olarak, master planlamada bir geçersiz kılma davranışına sahip olduklarını dikkate almak önemlidir. Bu nedenle, dikkatle kullanılması önerilir. Özellikle de, stok yenilemenin haftanın belirli günleri gerçekleştirilmesi gereken durumlarda faydalıdır. 

### <a name="updating-scm-related-calendars"></a>SCM ilgili takvimleri güncelleştirmek
Tüm ilgili takvimlerin karşılık gelen yerlerde atanmış olması önemliyken (satıcı, müşteri, ambar, teslimat modu veya kapsama grubu), değişiklikleri yansıtmaları için bunları güncelleştirmek de aynı şekilde önemlidir. Sistem üretim, transfer, satın alma ve satış siparişi tarihlerini atanmış takvimlerin kombinasyonuna bağlı olarak tanımlar. Takvimleri karşılık gelen bölgelerinde atamak ve güncelleştirmek için kimin sorumluluğa sahip olduğunu belirtmek en iyi uygulamadır. İş günlerinde bir bozulma veya diğer bir olağandışı değişiklik olması durumunda, takvimleri buna göre güncelleştirmek önemlidir. Takvimlere dayanan tüm görevlerin, örneğin master planlama ve üretim zamanlama gibi, takvimler güncelleştirildikten sonra yeniden çalıştırılması gerekir. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]