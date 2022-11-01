---
title: Ödeme belirteci kullanımını sınırlama
description: Bu makalede, Microsoft Dynamics 365 Commerce'te ödeme belirteçlerinin nasıl kullanıldığını sınırlayan özellik açıklanmaktadır.
author: BrianShook
ms.date: 10/20/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 8092ab0724f33f21759aa84d25e0bdcb5b2ad5dd
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709673"
---
# <a name="limit-payment-token-usage"></a>Ödeme belirteci kullanımını sınırlama

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te ödeme belirteçlerinin nasıl kullanıldığını sınırlayan özellik açıklanmaktadır. Belirteç kullanımı, satış siparişinin kapsamıyla sınırlıdır veya müşteri onayı verilirse kayıtlı kart olarak depolanır.

## <a name="key-terms"></a>Önemli terimler

| Vade | Açıklama |
|---|---|
| Belirteç | Dynamics 365 sisteminde, hareket amaçlı ödeme referanslarını depolayan başvurulan XML blob'u. |
| Kayıtlı kart | Dynamics 365 sisteminde veya ödeme ağ geçidinde gelecekte kullanmak için üzerinde anlaşılan ve müşterinin hesabına özel olan kaydedilmiş bir kart referans belirteci. |

Ödeme belirteci kullanımıyla ilgili sınırlamalar, yinelenen belirteçlerin olduğu bir ödeme ağ geçidi hizmeti kullanan tüm ortamlar için geçerlidir. Kullanıma hazır [Adyen için Dynamics 365 Payment Connector](adyen-connector.md), yetkilendirme ayarlamaları ve yeniden yetkilendirmeler gibi sonraki sipariş eylemlerini gerçekleştirmek için yinelenen ödeme belirteçlerini kullanır.

Bu yinelenen ödeme belirteçlerinin sistem genelinde nasıl kullanıldığını denetlemeye yardımcı olmak için **Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla** özelliği, sistemdeki satış siparişi kapsamında yinelenen bir belirteç kullanımını kısıtlar. Özellik etkinleştirildiğinde ödeme giriş sayfalarını güncelleştirerek ve yeni hareket örneklerinde kullanım için geçmiş müşteri ödeme referanslarını seçme özelliğini sınırlayarak Commerce headquarters kullanıcı arabirimini (UI) değiştirir.

Bu özellik, Visa gibi bazı ödeme kuruluşlarının kullanım kurallarına uymaya yardımcı olur. [Visa Temel Kuralları ve Visa Ürün ve Hizmet Kuralları](https://usa.visa.com/content/dam/VCOM/download/about-visa/visa-rules-public.pdf) kapsamında Visa, kart sahibi aksini kabul etmedikçe ödeme belirteçlerinin kullanımının hareketin kapsamı ile kısıtlanması gerektiğini belirtir.

**Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla** özelliği yalnızca yinelenen ödeme belirteci referansları kullanan bir ödeme ağ geçidi hizmeti kullanıyorsanız ilgilidir.

## <a name="enable-the-feature"></a>Özelliği etkinleştirme

**Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla** özelliğini etkinleştirmek üzere ortamınız için Commerce Headquarters'ta **Çalışma alanları \> Özellik yönetimi**'ne gidin, listede **Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla** özelliğini bulup seçin ve ardından **Şimdi Etkinleştir** seçeneğini belirleyin.

## <a name="limit-payment-token-usage"></a>Ödeme belirteci kullanımını sınırlama

Özellik etkinleştirildiğinde ödeme yakalama yöntemi için kullanılan Commerce Headquarters sayfalarında, müşteri için kayıtlı müşteri ödeme yöntemlerine başvurma biçimi güncelleştirilir. Bu güncelleştirme öncelikle iki işlem alanını etkiler:

- Müşteri adına kayıtlı müşteri kartının girilme biçimi
- Müşteriyle ilgili ödeme bilgilerinin gelecekteki satış siparişi ödeme girişleri için depolanma biçimi

Müşteri Commerce kanallarında işlem yaptığında ödeme ayrıntıları, satış siparişi bağlamıyla birlikte depolanır. Satış siparişi bağlamı, ödeme belirtecini Commerce Headquarters'taki yeni veya düzenlenmiş satış siparişi ödemeleri için ödeme sayfalarında müşteri kaydı karşılığında ödeme referansı olarak kullanılmaması için sınırlar.

### <a name="payment-form-changes"></a>Ödeme formu değişiklikleri

Çağrı merkezi veya Commerce Headquarters kullanıcısı bir müşteri için satış siparişi karşılığında ödeme aldığında ödeme sayfasında ödeme yöntemi seçim ayrıntıları sunulur. **Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla** özelliği etkinleştirildiğinde kullanıcı ödeme sayfasında artı simgesini (**+**) seçerse yalnızca "kayıtlı kart" kayıtları gösterilir. Değişiklikler, çağrı merkezi veya Commerce Headquarters kullanıcısının, müşterinin sağladığı ve yeni satış siparişi hareketi için **Müşteri ödeme bilgileri girme** sayfasında doldurulan tam ödeme ayrıntılarını girmesini gerektirir.

**Sayı** alanı için değer listesi yalnızca kayıtlı karta sahip müşteriyle ilişkili kart başvurularını içerir. Satış siparişi kapsamında olmayan geçmiş ödeme referansları filtrelenir.

**Sayı** alanındaki artı simgesi (**+**) mevcut kalır ve müşterinin işlenmekte olan satış siparişiyle ilişkili hareket için sağladığı ödeme bilgilerini girmek için kullanılabilir.

### <a name="how-cards-on-file-work"></a>Kayıtlı kartların çalışma biçimi

**Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla** özelliği etkinleştirildiğinde kayıtlı kart, müşteri kaydı karşılığında kaydedilen bir yinelenen ödeme belirtecidir ve satış siparişinin kapsamıyla sınırlı değildir. Kayıtlı kart, Commerce Headquarters kullanıcılarına yeni bir satış siparişi ödemesi için ödeme sayfasını doldururken hızlı başvuru sağlar. Bu belirteç referansı yalnızca Dynamics 365 ortamı için geçerlidir. Kullanıcıların ödeme iFrame modülünde gelecekteki kullanım için ödeme yöntemi kaydetmesine olanak tanıyan bir ödeme ağ geçidi hizmeti kullanan çevrimiçi kanallarda ödeme ağ geçidi bu referansları Dynamics 365 kayıtlı kartına ayrı bir referans olarak güvenli şekilde depolar.

Örneğin, çevrimiçi bir kanalda Adyen için Dynamics 365 Commerce Payment Connector kullanılırsa ödeme iFrame modülünde kredi kartı bilgilerini giren müşteriler, kimlikleri doğrulandıklarında sonraki çevrimiçi alışverişleri için yalnızca ağ geçidi hizmeti kayıtlı kart referanslarını görür. Ödeme iFrame modülünde seçenek olarak Dynamics 365 ortamında depolanan kayıtlı kartı görmezler. Benzer şekilde alışverişçiler çağrı merkezi aracılığıyla sipariş verdiğinde çevrimiçi kayıtlı kart referansları, çağrı merkezi kullanıcısına seçenek olarak sunulmaz. Çağrı merkezi kullanıcısı, gelecekteki siparişler için kaydetmek üzere Dynamics 365 sisteminden (müşteri tarafından kabul edildiği şekilde) dosya referanslarında yalnızca önceki kartı görür.

Commerce Headquarters kullanıcıları, **Perakende ve Ticaret \> Müşteriler** bölümüne gidip müşteri hesabı kaydını seçerek müşteri için kayıtlı kart kaydedebilir. **Müşteri \> Kurulum** bölümünde, ödeme sayfalarını işleme izni olan kullanıcılar **Kredi kartları** giriş sayfasını kullanarak gelecekteki hareketler için dosyada depolanacak bir ödeme kartı girebilir. Bu işlem, müşteri için gelecekte satış siparişi ödemeleri işlenirken zamandan tasarruf etmenize yardımcı olur. Çağrı Merkezi ve Commerce Headquarters kullanıcılarının kayıtlı kart ayrıntılarını yalnızca müşteri gelecekteki hareketler için kart referansı kullanmayı kabul ederse girmesi gerekir.

Commerce Headquarters ödeme sayfalarının alt kısmındaki **Gelecekteki kullanım için kaydet** onay kutusu, kullanıcıların gelecekteki kullanım için kayıtlı kart girmesine olanak tanır. Bu onay kutusu yalnızca müşteri gelecekteki hareketler için kayıtlı kartı kullanmayı kabul ederse kullanılmalıdır. Commerce Headquarters'ta **Çağrı merkezi parametreleri** sayfasının **Ödeme** sekmesindeki **Kayıtlı müşteri kartına izin ver** seçeneğini kullanarak **Gelecekteki kullanım için kaydet** onay kutusunu gösterebilir veya kısıtlayabilirsiniz. Bu seçenek **Evet** olarak ayarlandığında ödeme sayfalarını işleme izni olan Commerce Headquarters kullanıcıları, **Gelecekteki kullanım için kaydet** onay kutusunu kullanarak kayıtlı kart girebilir. Seçenek **Hayır** olarak ayarlandığında onay kutusu, ödeme sayfalarını işleme izni olan Commerce Headquarters kullanıcılarının kullanımına sunulmaz. **Kayıtlı müşteri kartına izin ver** seçeneği, şirketiniz Commerce Headquarters'ta yinelenen belirteçlerin kullanımını kısıtlamak istiyorsa ancak müşteri onayının verildiğinden emin olmak için prosedür olmadan kayıtlı kart girilmesine henüz izin vermek istemiyorsa kullanılabilir.

### <a name="commerce-headquarters-pages-where-the-recurring-token-restrictions-are-enforced"></a>Yinelenen belirteç kısıtlamalarının zorlandığı Commerce Headquarters sayfaları

Belirteç sınırlama kapsamı, özellik etkinleştirildiğinde Commerce Headquarters'ta bulunan aşağıdaki alanları etkiler:

- **Satış Siparişi \> Ödemeler \> Müşteri ödemesi girme** bölümündeki müşteri ödeme bilgileri
- Süreklilik siparişleri
- Taksit ödemeleri
- Alacak hesapları kredi kartı ödemeleri

### <a name="manage-payment-tokens-archiving-or-removal"></a>Ödeme belirteçlerini yönetme (arşivleme veya kaldırma)

**Ödeme Belirteci kullanımını Sipariş bağlamıyla sınırla** özellik bayrağı etkinleştirilmeden önce (veya özellik devre dışıyken) oluşturulan ödeme belirteçleri, sistemde "kapsamsız" kalır ve bunlara Commerce Headquarters ödeme sayfasında seçim listelerinde başvurulabilir. Bu belirteçler, Commerce Headquarters'ta iki şekilde düzenli olarak kaldırılabilir:

- **Kredi kartı hareketi verilerini arşivle** sayfasını kullanarak ödeme belirteçlerini düzenli olarak temizleyen veya arşivleyen bir iş ayarlayın. **Verileri arşivlemeden sil** seçeneğini **Evet** olarak ayarlarsanız **Minimum hareket yaşı (gün cinsinden)** ayarını karşılayan belirteçler silinir. Daha fazla bilgi için bkz. [Kredi kartı hareketi verilerini arşivleme](archive-cc-data.md).
- Ödeme belirteçlerini silen bir toplu iş çalıştırmanıza veya ayarlamanıza olanak tanıyan yeni **Kredi kartı belirteçlerini temizle** sayfasını (**Alacak hesapları \> Sorgular ve raporlar \> Temizle \> Kredi kartı belirteçlerini temizle**) kullanın. Aşağıdaki parametreleri ayarlayın:

    - **Gün cinsinden minimum belirteç yaşı** değeri 90 gün veya daha fazlası olmalıdır.
    - **Arka planda çalıştır** ayarları, **Yineleme** veya **Uyarılar** ayarlarını tanımlamak için kullanılabilir.
    - Belirli bir grup için görevi çalıştırmak üzere toplu iş grubu atanabilir.
    - **Özel** seçeneği **Evet** olarak ayarlanırsa işi yalnızca oluşturan kullanıcı çalıştırabilir.
    - **Kritik İş** seçeneği için **Evet** ayarı, sistemin işin durumunu etkin şekilde izlemesini sağlar.

Silinen belirteçler alınamaz. **Gün cinsinden minimum belirteç yaşı** alanını, ortamınız için en uzun süren hareket ömrüne (yetkilendirmeden yakalama veya geri ödemeye kadar) uygun bir aralık olarak ayarlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Ödemeler ile ilgili SSS](payments-retail.md)

[Ödeme yapma modülü](../add-checkout-module.md)

[Ödeme modülü](../payment-module.md)
