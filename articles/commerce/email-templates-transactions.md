---
title: Hareket olayları için e-posta şablonları oluşturma
description: Bu makalede, Microsoft Dynamics 365 Commerce uygulamasındaki hareket olayları için e-posta şablonlarının nasıl oluşturulacağı, yükleneceği ve yapılandırılacağı açıklanmaktadır.
author: bicyclingfool
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9a4d67d901608e210b4060a655ce39f0ea707a52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910562"
---
# <a name="create-email-templates-for-transactional-events"></a>Hareket olayları için e-posta şablonları oluşturma

[!include [banner](includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 Commerce uygulamasındaki hareket olayları için e-posta şablonlarının nasıl oluşturulacağı, yükleneceği ve yapılandırılacağı açıklanmaktadır.

Dynamics 365 Commerce, müşterilere hareketsel olaylar hakkında uyarı veren bir e-posta göndermek için kullanıma hazır bir çözüm sağlar. Örneğin, bir sipariş yerleştirildiğinde e-postalar, malzeme çekme için hazır veya sevk edilmiş olduğunda gönderilebilir. Bu makalede, hareket e-postaları göndermek için kullanılan e-posta şablonlarını oluşturma, yükleme ve yapılandırma adımları açıklanmaktadır.

## <a name="notification-types"></a>Bildirim türleri

Bildirimler, sipariş ve müşteri ömrünün bir parçası olarak belirli olaylar gerçekleştiğinde, müşterileri e-posta yoluyla bildirmek için konfigüre edilebilir. Bildirimleri konfigüre etmek için, Commerce e-posta bildirim profili oluşturarak bir bildirim türüne e-posta şablonu eşlemeniz gerekir. E-posta bildirim profillerinin nasıl ayarlanacağı konusunda bilgi için, bkz. [E-posta bildirim profili kurulumu](email-notification-profiles.md).

Dynamics 365 Commerce, aşağıdaki bildirim türlerini destekler.

### <a name="order-created"></a>Sipariş oluşturuldu

*Sipariş oluşturuldu* bildirim türü, Commerce Headquarters'ta yeni bir satış siparişi oluşturulduğunda tetiklenir.

> [!NOTE]
> Sipariş oluşturuldu bildirim türü, satış noktası (POS) terminalinde gerçekleşen peşin hareketler için tetiklenmez. Bu durumda, e-postayla gönderilmiş ve/veya yazdırılmış bir giriş oluşturulur. Daha fazla bilgi için, bkz. [Modern POS'tan (MPOS) e-posta girişleri gönderme](email-receipts.md).

### <a name="order-confirmed"></a>Sipariş onaylandı

*Sipariş onaylandı* bildirim türü, Commerce Headquarters'tan bir satış siparişi için bir sipariş onayı belgesi oluşturulduğunda tetiklenir.

### <a name="picking-completed"></a>Malzeme çekme işlemi tamamlandı

*Malzeme çekme tamamlandı* bildirim türü, bir sipariş için Commerce Headquarters'ta bir malzeme çekme listesi tamamlandı olarak işaretlendiğinde tetiklenir.

> [!NOTE]
> Bir madde, POS terminalinde çekilmiş olarak işaretlendiğinde malzeme çekme tamamlandı bildirimi türü tetiklenmez.

### <a name="packing-completed"></a>Paketleme tamamlandı

*Paketleme tamamlandı* bildirim türü, bir sipariş için POS terminalinde Commerce Headquarters'ta bir sevk irsaliyesi belgesi oluşturulduğunda tetiklenir.

Paketleme tamamlandı bildirimi türü, hareket e-postalarından gelen "Sipariş malzeme çekme için hazır" ve sipariş arama işlevlerini kolaylaştırmak için aşağıdaki ek e-posta yer tutucuları destekler.

| Yer tutucu adı    | Amaç |
| ------------------- | ------- |
| `pickupstorename`     | Siparişin malzeme çekme için uygun olduğu mağazanın adı. |
| `pickupstoreaddress`  | Siparişin malzeme çekme için uygun olduğu mağazanın adresi. |
| `pickupstoreopenfrom` | Malzeme çekme deposunun açılış saati. |
| `pickupstoreopento` | Malzeme çekme deposunun kapanış saati. |
| `pickupchannelid`     | Malzeme çekme deposunun mağaza kanal kodu. |
| `packingslipid`      | Çekilecek sipariş için sevk irsaliyesinin kodu. |
| `confirmationid`      | Çekilecek sipariş için sipariş onayı kodu. (Bu koda bazen kanal referans kodu da denir.) |

Müşteri iade ve sipariş arama özellikleri hakkında daha fazla bilgi için bkz. [Coğrafi bölge algılama ve yönlendirme kurulumu](geo-detection-redirection.md) ve [Konuk ödemeleri için aramayı etkinleştirme](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Sipariş çekme için hazır

Bir sipariş paketlendi olarak işaretlendiğinde ve teslimat modu bir veya daha fazla sipariş satırında **Müşteri teslimi** olarak ayarlandığında, *sipariş, teslimat için hazır* bildirim türü tetiklenir.

> [!NOTE]
> Sipariş teslimat için hazır bildirim türü, paketleme tamamlandı bildirim türü nedeniyle kullanımdan kaldırılmıştır. Bu bildirim türü, teslimat modu ile özelleştirilir.

### <a name="order-shipped"></a>Sipariş sevk edildi

*Sipariş sevk edildi* bildirim türü, mağazadan teslim olmayan bir teslimat türü faturalandırıldığında tetiklenir.

> [!NOTE]
> Sipariş sevk edildi bildirim türü, sipariş faturalandırıldı bildirim türü nedeniyle kullanımdan kaldırılmıştır. Bu bildirim türü, teslimat modu ile özelleştirilir.

### <a name="order-invoiced"></a>Sipariş faturalandırıldı

*Sipariş faturalandırıldı* bildirim türü, POS'ta veya Commerce Headquarters'ta yeni bir sipariş faturalandırıldığında tetiklenir.

### <a name="issue-gift-card"></a>Hediye kartı ver

*Çıkış hediye kartı* bildirim türü, hediye kartı türünde bir ürün içeren bir satış siparişi faturalanmışsa tetiklenir.

> [!NOTE]
> Çıkış hediye kartı bildirim e-postası hediye kartı alıcısına gönderilir. Hediye kartı alıcısı Commerce Headquarters'ta, **Satır ayrıntıları**'nın altındaki **Paketleme** sekmesinde bulunan tek bir satış siparişi satırında belirtilir. El ile veya program aracılığıyla belirtilebilir.

Çıkış hediye kartı bildirim türü aşağıdaki ek yer tutucuları destekler.

| Yer tutucu adı      | Amaç |
| --------------------- | ------- |
| `giftcardnumber`        | Hediye kartı türündeki ürünler için hediye kartı numarası. |
| `availablebalance` | Hediye kartında kalan bakiye. |
| `giftcardmessage`       | Hediye kartı türündeki ürünler için hediye kartı iletisi. |
| `giftcardpin`         | Hediye kartı türündeki ürünler için hediye kartının kişisel kimlik numarası (PIN). (Bu yer tutucu, harici hediye kartlarına özeldir.) |
| `giftcardexpiration`    | Hediye kartı türündeki ürünler için hediye kartının son kullanma tarihi. (Bu yer tutucu, harici hediye kartlarına özeldir.) |
| `giftcardrecipientname` | Hediye kartı türündeki ürünler için hediye kartını teslim alacak kişinin adı. |
| `giftcardbuyername`     | Hediye kartı türündeki ürünler için hediye kartını satın alan kişinin adı. |

Hediye kartları hakkında daha fazla bilgi için bkz. [E-ticaret dijital hediye kartları](digital-gift-cards.md) ve [Harici hediye kartları için destek](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Sipariş iptali

*Sipariş iptali* bildirim türü, Commerce Headquarters'ta bir sipariş iptal edildiğinde tetiklenir.

### <a name="customer-created"></a>Müşteri oluşturuldu

*Müşteri oluşturuldu* bildirim türü, Commerce Headquarters'ta yeni bir müşteri varlığı oluşturulduğunda tetiklenir.

### <a name="b2b-prospect-approved"></a>B2B aday müşterisi onaylandı

*B2B aday müşteri onaylandı* bildirimi türü, müşteri adayının ekleme talebi Commerce Headquarters'ta onaylandığında tetiklenir. B2B aday bilgilerini onaylama veya reddetme hakkında daha fazla bilgi için, bkz. [Yeni bir iş ortağı için yönetici kullanıcıyı ayarlama](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B adayı onaylandı bildirim türü aşağıdaki ek yer tutucuları destekler.

| Yer tutucu adı | Amaç                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | B2B adayının adı, uygulamada girildiği şekildedir. |
| `lastname`         | B2B adayının soyadı, uygulamada girildiği şekildedir. |
| `company`          | Başvuranın şirket adı, uygulamada girildiği şekildedir. |
| `email`            | Adayın e-posta adresi, uygulamada girildiği şekildedir.   |
| `zipcode`          | Adayın birincil adresinin ZIP/posta kodu. |
| `comments`         | Aday müşterinin uygulamaya girdiği açıklama. |
| `storename`        | Adayın oluşturulduğu kanalın adı. |
| `storeurl`         | Varsayılan olarak boştur. Bu yer tutucuyu kullanmak için özel bir uzantı oluşturulmalıdır. |

### <a name="b2b-prospect-rejected"></a>B2B aday müşterisi reddedildi

*B2B aday müşteri reddedildi* bildirimi türü, müşteri adayının ekleme talebi Commerce Headquarters'ta reddedildiğinde tetiklenir. B2B aday bilgilerini onaylama veya reddetme hakkında daha fazla bilgi için, bkz. [Yeni bir iş ortağı için yönetici kullanıcıyı ayarlama](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B adayı reddedildi bildirim türü aşağıdaki ek yer tutucuları destekler.

| Yer tutucu adı | Amaç                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | B2B adayının adı, uygulamada girildiği şekildedir. |
| `lastname`         | B2B adayının soyadı, uygulamada girildiği şekildedir. |
| `company`          | Başvuranın şirket adı, uygulamada girildiği şekildedir. |

## <a name="create-an-email-template"></a>Bir e-posta şablonu oluştur

Belirli bir hareket etkinliğini bir e-posta şablonuyla eşleştirmeden önce şablonu oluşturmanız gerekir.

Yeni bir e-posta şablonu oluşturmak için bu adımları izleyin.

1. Commerce merkezinde **Retail ve Commerce \> Merkez kurulumu \> kuruluş e-posta şablonları** veya **kuruluş yönetimi \> kurulum \> kuruluş e-posta şablonları**'na gidin.
1. **Yeni**'yi seçin.
1. **Genel** altında, aşağıdaki alanları ayarlayın:

    - **E-posta kimliği** – E-posta kimliği bir şablonun benzersiz tanımlayıcısıdır. Bir olayla eşlenecek şablonu seçtiğinizde gösterilen değerdir.
    - **E-posta açıklaması**: Bu isteğe bağlı alanı, şablonun açıklamasını sağlamak için kullanabilirsiniz. Girdiğiniz değer yalnızca Commerce Headquarters'da görünür.
    - **Gönderen adı**: Girdiğiniz ad, çoğu e-posta istemcisinin "kimden" alanında görünür.
    - **Gönderen e-postası**: Bu şablon kullanılarak gönderilen e-postalar için kullanılması gereken e-posta adresini girin.
    - **Varsayılan dil kodu**: Bu şablon, bu şablonu çağıran kanal tarafından herhangi bir dil belirlenmediyse varsayılan olarak gönderilen e-postanın yerelleştirilmiş sürümünü belirtir.

1. **E-posta iletisi içeriği** altında **Yeni**'yi seçin.
1. **Dil** alanına, e-posta şablonu için dil değerini girin. Daha sonra başka diller ve yerelleştirilmiş şablonlar ekleyebilirsiniz.
1. **Konu** alanına, e-postanın konu alanında görünmesi gereken e-posta konusunu girin.
1. E-posta şablonunuzu yüklemek için **Düzenle**'yi seçin.

## <a name="create-an-email-message-body-by-using-html"></a>HTML kullanarak bir e-posta ileti gövdesi oluşturma

E-postanızın ileti gövdesi HTML biçimindedir. HTML ve satır içi Basamaklı Stil Sayfaları'nın (CSS) izin verdiği herhangi bir düzeni, stili ve markalamayı kullanabilirsiniz. Herkese açık bir web uç noktasında barındırıyorsanız görüntüleri de kullanabilirsiniz. Görüntü eklemek için görüntünün URL'sini HTML **&lt;img&gt;** etiketinin **src** özniteliğine girin.

> [!NOTE]
> E-posta istemcileri, ileti gövdesi için kullandığınız HTML ve CSS dilinde ayarlamalar gerektirebilecek düzen ve stil sınırlamaları uygular. En çok beğenilen e-posta istemcilerinin desteklediği HTML oluşturma konusunun en iyi uygulamalarını öğrenmenizi öneririz.

## <a name="add-placeholders-to-the-email-message-body"></a>E-posta iletisi gövdesine yer tutucu ekleme

E-postanız, e-posta oluşturulduğunda müşteriye özel ve harekete özgü değerlerle değiştirilen yer tutucular içerebilir. Yer tutucular, her zaman yüzde işaretleriyle (%) çevrelenmiştir ve doğrudan HTML belgesine eklenir.

Aşağıda bir örnek verilmiştir.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Sipariş yer tutucuları (satış siparişi düzeyi)

Aşağıdaki yer tutucular, satış siparişi düzeyinde (satış satırları seviyesinin aksine) tanımlanan verileri alır ve gösterir.

| Yer tutucu adı     | Amaç                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Siparişi veren müşterinin adı.               |
| `customeraddress`      | Müşterinin adresi.                                 |
| `customeremailaddress` | Müşterinin ödeme sırasında girdiği e-posta adresi.     |
| `salesid`              | Siparişin satış kodu.                                   |
| `orderconfirmationid`  | Sipariş oluşturulurken elde edilen çapraz kanal kimliği.   |
| `channelid`            | Siparişin verildiği perakende kanalının veya çevrimiçi kanalın kimliği. |
| `deliveryname`         | Teslimat adresi için belirtilen ad.         |
| `deliveryaddress`      | Sevk edilen siparişler için teslimat adresi.                     |
| `deliverydate`         | Teslimat tarihi.                                           |
| `shipdate`             | Sevk tarihi.                                               |
| `modeofdelivery`       | Siparişin teslim modu.                              |
| `ordernetamount`       | Siparişin toplam tutarından, toplam verginin çıkarılması.         |
| `discount`            | Siparişin toplam iskontosu.                            |
| `charges`              | Siparişin toplam masrafları.                             |
| `tax`                  | Siparişin toplam vergisi.                                 |
| `total`                | Siparişin toplam tutarı.                              |
| `storename`            | Siparişin verildiği mağazanın adı.            |
| `storeaddress`         | Siparişi veren mağazanın adresi.              |
| `storeopenfrom`        | Siparişi veren mağazanın açılış saati.         |
| `storeopento`          | Siparişi veren mağazanın kapanış saati.         |
| `pickupstorename`      | Siparişin alınacağı mağazanın adı.\*   |
| `pickupstoreaddress`   | Siparişin alınacağı mağazanın adresi.\* |
| `pickupopenstorefrom`  | Siparişin alınacağı mağazanın açılış saati.\* |
| `pickupopenstoreto`    | Siparişin alınacağı mağazanın kapanış saati.\* |
| `pickupchannelid`     | Teslimatın alma şekli için belirtilen mağazanın kanal kimliği.\* |
| `packingslipid`        | Siparişteki satırlar paketlendiğinde oluşturulan sevk irsaliyesinin kimliği.\* |

\* Bu yer tutucular yalnızca **Sipariş alma için hazır** bildirim türü için kullanıldığında veri döndürür. 

### <a name="order-line-placeholders-sales-line-level"></a>Sipariş satırı yer tutucuları (satış satırı düzeyi)

Aşağıdaki yer tutucular, müşteri siparişindeki her bir ürün (satır) için verileri alır ve gösterir.

| Yer tutucu adı               | Amaç |
|--------------------------------|-------------------|
| `productid`                      | <p>Ürünün kimliği. Bu kimlik, çeşitleri hesaba katar.</p><p><strong>Not:</strong> Bu yer tutucu, yerini `lineproductrecid` aldığından kullanım dışı bırakıldı.</p> |
| `lineproductrecid`               | Ürünün kimliği. Bu kimlik, çeşitleri hesaba katar. Bu, bir öğeyi çeşit düzeyinde benzersiz şekilde tanımlar. |
| `lineitemid`                     | Ürünün ürün düzeyinde kimliği. (Bu kimlik, çeşitleri hesaba katmaz.) |
| `lineproductvariantid`           | Ürün çeşidinin kimliği. |
| `lineproductname`                | Ürünün adı. |
| `lineproductdescription`         | Ürünün açıklaması. |
| `linequantity`                   | Satır için sipariş edilen birim sayısı ile ölçü biriminin toplamı (örneğin, **ea** veya **çifti**). |
| `lineunit`                       | Satırın ölçü birimi. |
| `linequantity_withoutunit`       | Ölçü birimi olmadan satır için sipariş edilen birim sayısı. |
| `linequantitypicked`             | **PickOrder** olayı kullanıldığında alınan birim sayısı. Aksi takdirde, **0** (sıfır). |
| `linequantitypicked_withoutunit` | **PickOrder** olayı kullanıldığında ölçü birimi olmadan alınan birim sayısı. Aksi takdirde, **0** (sıfır). |
| `linequantitypacked`             | **PackOrder** ve **Sipariş malzeme çekme için hazır** olayları kullanıldığında paketlenen birim sayısı. Aksi takdirde, **0** (sıfır). |
| `linequantitypacked_withoutuom`  | **PackOrder** ve **Sipariş malzeme çekme için hazır** olayları kullanıldığında ölçü birimi olmadan paketlenen birim sayısı. Aksi takdirde, **0** (sıfır). |
| `linequantityshipped`            | Sonraki satırda açıklandığı gibi belirli olayların kullanılması dışında her zaman **0**'dır. |
| `linequantityshipped_withoutuom` | **ShipOrder** olayı kullanıldığında ölçü birimi olmadan alınan birim sayısı. Aksi takdirde, **0** (sıfır). |
| `lineprice`                      | Tek bir birimin fiyatı. |
| `linenetamount`                  | Birim sayısı ve iskonto uygulandıktan sonra satırın fiyatı. |
| `linediscount`                   | Her bir birim için iskonto. |
| `lineshipdate`                   | Satır için sevk tarihi. |
| `linedeliverydate`               | Satır için teslimat tarihi. |
| `linedeliverymode`               | Satır için teslimat modu. |
| `linedeliveryaddress`            | Satır için teslimat adresi. |
| `linepickupdate`                 | Teslimatın alma modunun kullanıldığı siparişler için müşterinin belirttiği alma tarihi. |
| `linepickuptimeslot`             | Teslimatın alma modunun kullanıldığı siparişler için müşterinin belirttiği alma zaman aralığı. |
| `giftcardnumber`                 | Hediye kartı türündeki ürünler için hediye kartı numarası. |
| `giftcardbalance`                | Hediye kartı türündeki ürünler için hediye kartı bakiyesi. |
| `giftcardmessage`                | Hediye kartı türündeki ürünler için hediye kartı iletisi. |
| `giftcardpin`                    | Hediye kartı türündeki ürünler için hediye kartı PIN'i. (Bu yer tutucu, harici hediye kartlarına özeldir.) |
| `giftcardexpiration`             | Hediye kartı türündeki ürünler için hediye kartının son kullanma tarihi. (Bu yer tutucu, harici hediye kartlarına özeldir.) |
| `giftcardrecipientname`          | Hediye kartı türündeki ürünler için hediye kartını teslim alacak kişinin adı. |
| `giftcardbuyername`              | Hediye kartı türündeki ürünler için hediye kartını satın alan kişinin adı. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>E-posta iletisi gövdesinde, sipariş satırı yer tutucularının biçimi

E-posta ileti gövdesinde tek tek sipariş satırları için HTML oluşturduğunuzda aşağıdaki yer tutuculara sahip satırlar için HTML'nin tekrarlayan bloğunu ve yer tutucuları çevreleyin. Yer tutucuların, HTML açıklama etiketlerinin içinde bulunduğuna dikkat edin.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Aşağıda bir örnek verilmiştir.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>E-postayla gönderilen makbuzlar için şablon oluşturma

Satış noktasında (POS) alışveriş yapan müşterilere makbuzlar e-postayla gönderilebilir. Genel olarak, e-postayla gönderilen makbuz şablonunu oluşturma adımları, diğer hareket olayları için şablon oluşturma adımlarıyla aynıdır. Ancak, aşağıdaki değişiklikler gereklidir:

- **%message%** yer tutucu, alıcı metnini e-postaya yerleştirmek için kullanılır. Makbuz gövdesinin doğru bir şekilde oluşturulmasını sağlamak için **%message%** yer tutucusunu HTML **&lt;pre&gt;** ve **&lt;/pre&gt;** etiketleriyle çevreleyin.
- **%receiptid%** yer tutucu, makbuz kodunu temsil eden bir QR kodu veya barkod göstermek için kullanılabilir. (QR kodları ve barkodlar dinamik olarak oluşturulur ve üçüncü taraf bir hizmet tarafından sunulur.) Bir QR kodunun veya bar kodun e-postayla gönderilen makbuzda nasıl gösterileceği hakkında daha fazla bilgi için, bkz. [işlem ve makbuz e-postalarına QR kodu ya da barkod ekleme](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>E-posta HTML'sini yükleme

İleti gövdeniz için HTML'yi oluşturup test ettikten sonra HTML, Commerce Headquarters'a yüklenmelidir. Şu anda, e-posta HTML'si dışa aktarılamıyor. Bu nedenle, HTML'nizin ana kopyasını Commerce Headquarters'ın dışında tutmalısınız.

Yeni veya düzenlenmiş bir e-posta şablonu HTML'si yüklemek için aşağıdaki adımları izleyin.

1. Commerce Headquarters'da **Retail and Commerce \> Genel Merkezi kurulumu \> Kuruluş e-posta şablonları**'na gidin.
1. HTML eklemek veya değiştirmek istediğiniz dilin satırını seçin. Alternatif olarak, yeni bir dil için bir satır oluşturmak üzere **Yeni**'yi seçin.
1. **Düzenle** öğesini seçin.
1. Görünen iletişim kutusunda **Gözat**'ı seçin. Yüklemek istediğiniz HTML belgesine gidin, belgeyi seçin ve sonra **Aç**'ı seçin.
1. **Yükle**'yi seçin.
1. E-posta HTML'niz, önizleme penceresinde göründükten sonra **Tamam**'ı seçin.
1. Satır için, **Gövde var** onay kutusunun seçili olduğundan emin olun.

Commerce Headquarters'ı zaten e-posta gönderecek şekilde yapılandırdıysanız yeni veya güncelleştirilmiş e-postanız, şablonla eşlenen etkinliği çağıran bir işlem gerçekleştiren tüm müşterilere gönderilir.

Dynamics 365 Commerce uygulamasındaki e-postayı yapılandırma hakkında daha fazla bilgi için bkz. [E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Ek kaynaklar 

[E-posta bildirimi profili ayarlama](email-notification-profiles.md)

[E-posta yapılandırma ve gönderme](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[E-posta makbuzlarını ayarlama](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Modern POS'tan (MPOS) e-posta makbuzları gönderme](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
