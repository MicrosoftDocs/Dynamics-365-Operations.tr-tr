---
title: Ürün reçetesi hesaplamaları grupları
description: Bu makalede, ürün reçeteleri için hesaplama grupları ve bunların nasıl ayarlanacağı hakkında bilgi verilmektedir. Bir ürün reçetesi hesaplaması çalıştırmak için ya hesaplama grupları ayarlamalı ve bunları tek tek maddelere atamalısınız ya da varsayılan bir hesaplama grubu ayarlamalısınız. Ardından, hesaplama grubundaki hesaplama ayarları, ürün reçetesi hesaplaması sayfasında ürün reçetesi hesaplamasında varsayılan değerler olarak kullanılır.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcGroup, BOMCalcTable, BOMCalcTrans, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94063
ms.assetid: 63e1b7dc-c2c5-41b0-81ed-e3e02d1b39e0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2581d35fa02d800b07fcb40efb9d238685233898
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669838"
---
# <a name="bom-calculations-groups"></a>Ürün reçetesi hesaplamaları grupları

[!include [banner](../includes/banner.md)]

Bu makalede, ürün reçeteleri için hesaplama grupları ve bunların nasıl ayarlanacağı hakkında bilgi verilmektedir. Bir ürün reçetesi hesaplaması çalıştırmak için ya hesaplama grupları ayarlamalı ve bunları tek tek maddelere atamalısınız ya da varsayılan bir hesaplama grubu ayarlamalısınız. Ardından, hesaplama grubundaki hesaplama ayarları, ürün reçetesi hesaplaması sayfasında ürün reçetesi hesaplamasında varsayılan değerler olarak kullanılır. 

**Stok ve ambar yönetim parametreleri** sayfasında varsayılan bir hesaplama grubu veya **Serbest bırakılan ürün ayrıntıları** sayfasında ürüne özel hesaplama grubu gereklidir. Sistem, ilk olarak **Serbest bırakılan ürün ayrıntıları** sayfasında hesaplama grubu ayarına bakar. Orada bir hesaplama grubu bulamazsa, **Stok ve ambar yönetim parametreleri** sayfasında bakar. Sistem, bir hesaplama grubu bulamazsa kullanıcı, hesaplama sırasında bir hata iletisi alır. Hesaplama grubu maliyet fiyatı modeli, satış fiyatı modeli ve uyarılar kontrol listesi ilkelerini içerir. Hesaplama grubundaki hesaplama ayarları, **Ürün reçetesi hesaplaması** sayfasında ürün reçetesi hesaplamasında varsayılan değerler olarak kullanılır.

## <a name="purposes-of-bom-calculation-groups"></a>Ürün reçetesi hesaplama gruplarının amaçları
Maddelere ürün reçetesi hesaplama grubunu çeşitli nedenlerle atarsınız:

-   **Maliyet fiyatı modeli** alanını ayarlayarak, üretilmiş bir maddenin planlanan maliyetinin hesaplanması sırasında satın alınan bir bileşenin maliyet katkı verilerinin kaynağını belirtirsiniz. Bazı üreticiler planlanan maliyetleri, satın alınan bileşenler için satınalma fiyatı ticari anlaşmalarını kullanarak veya bir maliyetlendirme sürümündeki satınalma fiyatı kayıtları gibi başka bir temele göre hesaplar.
-   **Satış fiyatı modeli** alanını ayarlayarak, önerilen satış fiyatının hesaplamasında maddenin verilerinin nasıl kullanılacağını belirtirsiniz. Maddenin ya satış fiyatını ya da maliyet grubunu belirleyebilirsiniz. Bazı üreticiler, üretilmiş maddeler için önerilen bir satış fiyatı hesaplamak ister. Hesaplanan satış fiyatı, bileşenin satış fiyatı kaydına dayanan bir toplanan fiyat yaklaşımını yansıtabilir. Alternatif olarak, hesaplanan satış fiyatı, bileşenin maliyetine ve maddenin maliyet grubuyla ilişkili olan geçerli kar yüzdesine dayanan bir maliyet-artı-kar marjı yaklaşımını yansıtabilir.
-   **Açılımı durdur** alanını kullanarak, üretilmiş bir maddenin, ürün reçetesi hesaplamasında satınalınan bir madde gibi ele alınması gerektiğini belirtirsiniz. Ara sıra üretilen bir satınalınan madde veya şu anda satın alınmakta olan üretilen madde tipik senaryolar arasındadır. Ürün, ürün reçetesi ve rota bilgilerini tanımlamak ve ürünün üretim siparişlerinin desteklemek için öncelikle üretilen ürün olarak belirlenir. Ancak, **Açılımı durdur** bayrağı, maddenin ürün reçetesi ve rotasının maliyet hesaplamalarında kullanılmasını engeller. Bunun yerine, ürün reçetesi hesaplaması maddenin belirtilen maliyetlerini kullanır.

## <a name="calculation-groups"></a>Hesaplama grupları
Hesaplama gruplarını, maliyet yönetiminde **Önceden tanımlanan maliyet ilkeleri kurulumu** altında tanımlarsınız. Maddelere atanan hesaplama grupları, bileşenlerin maliyet veya satış fiyatının, hesaplama grubunda açıklandığı şekliyle hesaplama için nasıl kaynaklandırıldığını belirtmenizi sağlar. **Hesaplama grupları** sayfasında, maliyet fiyatı modeli, alternatif bir maliyet fiyat modeli, satış fiyatı modeli ve uyarıları tanımlayabilirsiniz.

### <a name="cost-price-model"></a>Maliyet fiyatı modeli

**Maliyet fiyatı modeli** alanı için dört seçenek bulunur:

-   **Madde maliyet fiyatı**: **Serbest bırakılan ürün** tablosundan maliyet fiyatı veya madde boyutlarının birleşimi, maliyet fiyatı olarak kullanılır.
-   **Madde satınalma fiyatı**: **Serbest bırakılan ürünlerin listesi** sayfasının **Satınalma** sekmesindeki **Maliyet fiyatı** alanında bulunan satınalma fiyatı kullanılır.
-   **Ticari anlaşmalar**: Maddelerin ve satıcıların belirli birleşimleri için veya belirli tesisler için ticari anlaşmalar yapılandırabilirsiniz. Ardından, buradan **Ticari anlaşmalar** seçeneğini seçtiğinizde, madde ile birlikte satınalma fiyatı ve tesis için oluşturduğunuz ticari anlaşma kullanılır.
-   **Stok fiyatı**: Ürün reçetesi hesaplamasında birim maliyeti hesaplamak için maddenin güncel stok değeri kullanılır. Birim maliyet fiyatı yalnızca deftere nakledilen miktar ve fiziksel miktar 0 (sıfır)'dan büyükse hesaplanır.

### <a name="alternative-cost-price"></a>Alternatif maliyet fiyatı

**Alternatif maliyet fiyatı** alanı, **Maliyet fiyatı modeli** alanıyla aynı seçeneklere sahiptir. Ancak, bu alan yalnızca birincil maliyet fiyatı modelinde fiyat bulunamadığında kullanılır.

### <a name="sales-price-model"></a>Satış fiyatı modeli

**Satış fiyatları** alanının hesaplaması için iki seçenek bulunur:

-   **Maliyet grubu**: Bu seçenek seçildiğinde satış fiyatı, maliyet grubundaki maliyet fiyatı ve kar ayarlama yüzdesine göre hesaplanır.
-   **Madde satış fiyatı**: Bu seçenek seçildiğinde Serbest bırakılan ürün tablosunda bulunan **Satış** FastTab'ındaki satış fiyatı kullanılır.

### <a name="stop-explosion"></a>Açılımı durdur

**Açılımı durdur** onay kutusu, üretilen maddenin ne zaman satınalma maddesi olarak ele alınması gerektiğini belirtmek için kullanılır. Normalde, **Açılımı durdur** onay kutusunu boş bırakın. Bu onay kutusunu seçerek, üretilen bir bileşenin ürün reçetesi hesaplama amacıyla üretilen bileşen yerine satınalma bileşeni olarak ele alınması gerektiğini belirtirsiniz. Tesise bağlı olarak, maddenin maliyeti, ürün reçetesi hesaplamaları kullanılarak hesaplanabilir. **Açılımı durdur** onay kutusunun seçili olduğu hesap grubuyla ilişkili bileşenleri olan planlı satınalma ve üretim siparişlerinin açılımı ürün reçetesinde durdurulur. Master planlama çizelgeleme, planlı siparişleri ürün reçetesinde bulunan maddelerde değil, ürün reçetesinin üzerinde oluşturur. Temelde, bu onay kutusunu seçerek, maliyetin, bu hesaplama grubuna sahip maddeler için ürün reçetesi hesaplamasına eklenmeyeceğini belirtirsiniz.

### <a name="warnings"></a>Uyarılar

**Uyarılar** FastTab'ında kullanıcıların, ürün reçetesi hesaplamaları yaparken almaları gereken her türlü uyarı iletileri için seçenekleri seçin. 

Örneğin, **Ürün reçetesi yok** onay kutusunu seçtiğinizde, bileşenlerden biri veya ürün reçetesi hesaplamasının çalıştırıldığı ana madde için etkin ürün reçetesi bulunamazsa kullanıcı uyarı alır. **Rota yok** onay kutusunu seçerseniz, kullanıcı etkin rota sürümü bulunamazsa uyarı alır. Rotalarınızda ve işlemlerinizde kaynaklar kullanıyorsanız sisteme, bu kaynaklar için denetim yapmasını söyleyebilirsiniz. Ardından etkin rota içindeki her bir satırda birer kaynak bulunamazsa kullanıcı bir uyarı alır. 

Ayrıca tüketimi doğrulayabilir ve denetleyebilirsiniz. Tüketim, belirli bir rotadaki miktardır. Normalde, bir üretim sürecinde belirli bir işlemi gerçekleştirmek için gerekli zaman miktarını temsil eder. Bir maddenin maliyet fiyatı olup olmadığını denetleyebilirsiniz. Madde için etkin maliyet fiyatı yoksa ürün reçetesi hesaplamasına hiçbir maliyet eklenmez. 

Ayrıca maliyet fiyatının yaşını denetleyebilir ve doğrulayabilirsiniz. Örneğin, birim maliyet fiyatının 60 günden sonra yeniden değerlendirilmesi gerektiğini belirtmek için **60** girin. Sınıra ulaşılırsa, sistem bir uyarı oluşturur. Örneğin, bu yılın Ocak ayında bir madde için maliyet fiyatı girildi. Maliyet fiyatının girilmesinden 60 günden daha geç olan Ağustos ayına gelindiğinde, kullanıcı ürün reçetesi hesaplaması çalıştırıldığında bir uyarı alır. **Minimum katkı payı** alanına bir yüzde girebilirsiniz. Bu değer, minimum katkı payının karşılanmadığı noktayı belirtir. Belirli bir bileşen için katkı payı karşılanmamışsa kullanıcı bir uyarı alır. Bu nedenle, bu alan maliyetlerinizin ve maddeleriniz için gerekli olabilecek ek taşıma maliyetlerinin altına inmemenizi garantilemeye yardımcı olur.

### <a name="default-setup-in-inventory-and-warehouse-management-parameters"></a>Stok ve ambar yönetimi parametrelerinde varsayılan ayar

Hesaplamaları çalıştırmak için hesaplama grupları gerekli olduğundan, Stok yönetimi parametrelerinde varsayılan hesaplama grubunu ayarlamanız gerekir. Bu ayar, şirketlerin tüm maddeler için standart maliyet grupları ve kar ayarları olmasını sağlar. Ardından, belirli bir maddenin özel hesaplama gereksinimleri varsa, kullanıcı bu madde için farklı bir hesaplama grubu atayabilir. Normalde, ürün reçetesi maddeleri yerine ürün reçetesinin bileşen maddelerinde hesaplama grupları ayarlayabilirsiniz. Ancak, uyarı iletileri gösterildiğinde hesaplama grupları uygulanabilir. Maddelere atanmış bir hesaplama grubu, Stok yönetimi parametrelerinde ayarlanan varsayılan değeri geçersiz kılar. 

Varsayılan parametreyi, **Maliyet yönetimi** &gt; **Stok muhasebesi politikaları kurulumu** &gt; **Parametreler** &gt; **Stok muhasebesi** &gt; **Hesaplama grubu** üzerinde ayarlayabilirsiniz. Varsayılan yapılandırma grubu ayarlayarak, ürün reçetesi hesaplama sürecinde kullanıcılara, seçili bileşenlerin hesaplama hatalarına neden olabileceğini belirtecek uyarı koşullarını da yapılandırabilirsiniz.

### <a name="view-warning-messages-on-the-complete-page"></a>Tamamla sayfasında uyarı iletileri görüntüleme

Ürün reçetesi hesaplaması uyarı iletileri oluşturur. Bir seçili madde hakkındaki uyarıları görüntüleyebilirsiniz. Örneğin, Satış ve pazarlamada, D0001 maddesi için yeni bir satış siparişi oluşturun. Ardından, hesaplama ayrıntılarını ve uyarıları görüntülemek için, satış sipariş satırında **Satırı güncelleştir** menüsünde **Ürün Reçetesine/Formüle göre Hesapla** öğesini tıklayın. Ayrıca **Tamamla** sayfasında ürün reçetesi hesaplama sonuçlarını da görüntüleyebilirsiniz. Uyarı iletileri için, herhangi bir maddeye dört uyarı koşulu uygulanırken üretilen maddelere yalnızca iki uyarı koşulu uygulanır:
-   Üretilen maddenin etkin ürün reçetesi olmadığında tespit edin.
-   Üretilen maddenin etkin rotası olmadığında tespit edin.
-   Ürün reçetesi satırındaki maddenin 0 (sıfır) miktarına sahip olduğunda tespit edin.
-   Ürün reçetesi satırındaki maddenin 0 (sıfır) miktarına sahip olduğunda veya maliyet kaydı olmadığında tespit edin.
-   Ürün reçetesi satırındaki maddenin tarihi geçmiş bir maliyeti olduğunda tespit edin. Uyarı, hesaplama tarihiyle maksimum maliyet yaşı için belirtilen günlere yönelik bir karşılaştırmayı yansıtmaktadır.
-   Ürün reçetesi satırındaki maddenin istediğinizden daha düşük bir karlılık yüzdesi olduğunda tespit edin.

Uyarı iletilerindeki değişim gereksinimlerinize bağlı olarak birden fazla ürün reçetesi hesaplama grubu tanımlayabilirsiniz. Örneğin, etkin bir ürün reçetesi, bileşen miktarı 0 (sıfır) ve bileşen maliyeti 0 (sıfır) hakkında uyarı koşulları olan bir ürün reçetesi hesaplama grubu yeterli olabilir. Ürün reçetesi hesaplamasına başladığınızda, ürün reçetesi hesaplama grubuyla ilişkili olan uyarı koşullarını geçersiz hale getirilebilirsiniz. Ayrıca uyarı koşulları ekleyebilir veya kaldırabilirsiniz. Örneğin, mevcut durum rota verilerini içermiyorsa etkin rota hakkındaki uyarı koşulunu kaldırabilirsiniz. **Not:** Saat ve işe devam, bir **Hesaplama grupları** sayfası içerir ancak bu sayfanın ürün reçetesi hesaplama gruplarıyla ilişkisi bulunmaz. Saat ve işe devamda, çalışanlar aynı gözetmen veya yönetici ile ilişkili çalışanların gruplanmasını yansıtan hesaplama gruplarına atanabilir. Çalışan kayıtlarının hesaplaması, bir gözetmen veya yönetici tarafından otomatik veya el ile yapılabilir.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]