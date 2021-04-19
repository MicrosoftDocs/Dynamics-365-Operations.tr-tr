---
title: Hareket olayları için e-posta şablonları oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce uygulamasındaki hareket olayları için e-posta şablonlarının nasıl oluşturulacağı, yükleneceği ve yapılandırılacağı açıklanmaktadır.
author: bicyclingfool
ms.date: 03/01/2021
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
ms.openlocfilehash: 55597e83a930fc7d8bcc4c0cf09abc82cb666b25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792643"
---
# <a name="create-email-templates-for-transactional-events"></a>Hareket olayları için e-posta şablonları oluşturma

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce uygulamasındaki hareket olayları için e-posta şablonlarının nasıl oluşturulacağı, yükleneceği ve yapılandırılacağı açıklanmaktadır.

## <a name="overview"></a>Özet

Dynamics 365 Commerce, müşterileri hareket olayları konusunda uyaran e-postalar göndermek için kullanıma hazır bir çözüm sunar (örneğin, bir sipariş verildiğinde, sipariş malzeme çekme için hazır olduğunda veya sipariş sevk edildiğinde). Bu konuda, hareket e-postaları göndermek için kullanılan e-posta şablonlarını oluşturma, yükleme ve yapılandırma adımları açıklanmaktadır.

## <a name="create-an-email-template"></a>Bir e-posta şablonu oluştur

Belirli bir hareket etkinliğini bir e-posta şablonuyla eşleştirmeden önce şablonu oluşturmanız gerekir.

Yeni bir e-posta şablonu oluşturmak için bu adımları izleyin.

1. Commerce merkezinde **Retail ve Commerce \> Merkez kurulumu \> kuruluş e-posta şablonları** veya **kuruluş yönetimi \> kurulum \> kuruluş e-posta şablonları**'na gidin.
1. **Yeni**'yi seçin.
1. **Genel** altında, aşağıdaki alanları ayarlayın:

    - **E-posta Kodu**: E-posta kodu, bir şablon için benzersiz tanımlayıcıdır ve bir olaya eşlemek için bir şablon seçtiğinizde gösterilen değerdir.
    - **E-posta açıklaması**: Bu isteğe bağlı alanı, şablonun açıklamasını sağlamak için kullanabilirsiniz. Girdiğiniz değer yalnızca Commerce Headquarters'da görünür.
    - **Gönderen adı**: Girdiğiniz ad, çoğu e-posta istemcisinin "kimden" alanında görünür.
    - **Gönderen e-postası**: Bu şablon kullanılarak gönderilen e-postalar için kullanılması gereken e-posta adresini girin.
    - **Varsayılan dil kodu**: Bu şablon, bu şablonu çağıran kanal tarafından herhangi bir dil sağlanmadıysa varsayılan olarak gönderilen e-postanın yerelleştirilmiş sürümünü belirtir.

1. **E-posta iletisi içeriği** altında **Yeni**'yi seçin.
1. **Dil** alanına, e-posta şablonu için dil değerini girin. Daha sonra başka diller ve yerelleştirilmiş şablonlar ekleyebilirsiniz.
1. **Konu** alanına, e-postanın konu alanında görünmesi gereken e-posta konusunu girin.
1. E-posta şablonunuzu yüklemek için **Düzenle**'yi seçin.

## <a name="create-an-email-message-body-by-using-html"></a>HTML kullanarak bir e-posta ileti gövdesi oluşturma

E-postanızın ileti gövdesi HTML biçimindedir. HTML ve satır içi Basamaklı Stil Sayfaları'nın (CSS) izin verdiği herhangi bir düzeni, stili ve markalamayı kullanabilirsiniz. Herkese açık bir web uç noktasında barındırıyorsanız görüntüleri de kullanabilirsiniz. Görüntü eklemek için görüntünün URL'sini HTML **&lt;img&gt;** etiketinin **src** özniteliğine girin.

> [!NOTE]
> E-posta istemcileri, ileti gövdesi için kullandığınız HTML ve CSS dilinde ayarlamalar gerektirebilecek düzen ve stil sınırlamaları uygular. En çok beğenilen e-posta istemcileri tarafından desteklenen HTML oluşturma konusunun en iyi uygulamalarını öğrenmenizi öneririz.

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

| Yer tutucu adı     | Yer tutucu değeri                                            |
| -------------------- | ------------------------------------------------------------ |
| customername         | Siparişi veren müşterinin adı.               |
| salesid              | Siparişin satış kodu.                                   |
| deliveryaddress      | Sevk edilen siparişler için teslimat adresi.                     |
| customeraddress      | Müşterinin adresi.                                 |
| customeremailaddress | Müşterinin ödeme sırasında girdiği e-posta adresi.     |
| deliverydate         | Teslimat tarihi.                                           |
| shipdate             | Sevk tarihi.                                               |
| modeofdelivery       | Siparişin teslim modu.                              |
| masraflar              | Siparişin toplam masrafları.                             |
| vergi                  | Siparişin toplam vergisi.                                 |
| toplam                | Siparişin toplam tutarı.                              |
| ordernetamount       | Siparişin toplam tutarından, toplam verginin çıkarılması.         |
| iskonto             | Siparişin toplam iskontosu.                            |
| storename            | Siparişin verildiği mağazanın adı.            |
| storeaddress         | Siparişi veren mağazanın adresi.              |
| storeopenfrom        | Siparişi veren mağazanın açılış saati.         |
| storeopento          | Siparişi veren mağazanın kapanış saati.         |
| pickupstorename      | Siparişin alınacağı mağazanın adı.     |
| pickupstoreaddress   | Siparişin alınacağı mağazanın adresi.  |
| pickupopenstorefrom  | Siparişin alınacağı mağazanın açılış saati. |
| pickupopenstoreto    | Siparişin alınacağı mağazanın kapanış saati. |

### <a name="order-line-placeholders-sales-line-level"></a>Sipariş satırı yer tutucuları (satış satırı düzeyi)

Aşağıdaki yer tutucular, müşteri siparişindeki her bir ürün (satır) için verileri alır ve gösterir.

| Yer tutucu adı               | Yer tutucu değeri |
|--------------------------------|-------------------|
| productid                      | Satır için ürün kodu. |
| lineproductname                | Ürünün adı. |
| lineproductdescription         | Ürünün açıklaması. |
| linequantity                   | Satır için sipariş edilen birim sayısı ile ölçü biriminin toplamı (örneğin, **ea** veya **çifti**). |
| lineunit                       | Satırın ölçü birimi. |
| linequantity_withoutunit       | Ölçü birimi olmadan satır için sipariş edilen birim sayısı. |
| linequantitypicked             | **PickOrder** olayı kullanıldığında alınan birim sayısı. Aksi takdirde, **0** (sıfır). |
| linequantitypicked_withoutunit | **PickOrder** olayı kullanıldığında ölçü birimi olmadan alınan birim sayısı. Aksi takdirde, **0** (sıfır). |
| linequantitypacked             | **PackOrder** ve **Sipariş malzeme çekme için hazır** olayları kullanıldığında paketlenen birim sayısı. Aksi takdirde, **0** (sıfır). |
| linequantitypacked_withoutuom  | **PackOrder** ve **Sipariş malzeme çekme için hazır** olayları kullanıldığında ölçü birimi olmadan paketlenen birim sayısı. Aksi takdirde, **0** (sıfır). |
| linequantityshipped            | Sonraki satırda açıklandığı gibi belirli olayların kullanılması dışında her zaman **0**'dır. |
| linequantityshipped_withoutuom | **ShipOrder** olayı kullanıldığında ölçü birimi olmadan alınan birim sayısı. Aksi takdirde, **0** (sıfır). |
| lineprice                      | Tek bir birimin fiyatı. |
| linenetamount                  | Birim sayısı ve iskonto uygulandıktan sonra satırın fiyatı. |
| linediscount                   | Her bir birim için iskonto. |
| lineshipdate                   | Satır için sevk tarihi. |
| linedeliverydate               | Satır için teslimat tarihi. |
| linedeliverymode               | Satır için teslimat modu. |
| linedeliveryaddress            | Satır için teslimat adresi. |
| giftcardnumber                 | Hediye kartı türündeki ürünler için hediye kartı numarası. |
| giftcardbalance                | Hediye kartı türündeki ürünler için hediye kartı bakiyesi. |
| giftcardmessage                | Hediye kartı türündeki ürünler için hediye kartı iletisi. |
| giftcardpin                    | Hediye kartı türündeki ürünler için hediye kartının kişisel kimlik numarası (PIN). (Bu yer tutucu, harici hediye kartlarına özeldir.) |
| giftcardexpiration             | Hediye kartı türündeki ürünler için hediye kartının son kullanma tarihi. (Bu yer tutucu, harici hediye kartlarına özeldir.) |
| giftcardrecipientname          | Hediye kartı türündeki ürünler için hediye kartını teslim alacak kişinin adı. |
| giftcardbuyername              | Hediye kartı türündeki ürünler için hediye kartını satın alan kişinin adı. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>E-posta iletisi gövdesinde, sipariş satırı yer tutucularının biçimi

E-posta ileti gövdesinde tek tek sipariş satırları için HTML oluşturduğunuzda HTML açıklama etiketlerinin içine yerleştirilen aşağıdaki yer tutuculara sahip satırlar için HTML'nin tekrarlayan bloğunu ve yer tutucuları çevreleyin.

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

- Makbuz metni **%message%** yer tutucusu kullanılarak e-postaya eklenir. Makbuz gövdesinin doğru bir şekilde oluşturulmasını sağlamak için **%message%** yer tutucusunu HTML **&lt;pre&gt;** ve **&lt;/pre&gt;** etiketleriyle çevreleyin.
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

[E-posta makbuzlarını ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Modern POS'tan (MPOS) e-posta makbuzları gönderme](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
