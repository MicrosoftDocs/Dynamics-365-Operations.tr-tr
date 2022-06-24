---
title: Alışveriş sepeti modülü
description: Bu makale sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c4023857f13830449eaa19f8513799ece97729d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866068"
---
# <a name="cart-module"></a>Alışveriş sepeti modülü

[!include [banner](includes/banner.md)]

Bu makale sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır. Ayrıca, modül sipariş özeti gösterir ve müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlar.

Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler. Ayrıca bir **Alışverişe geri git** bağlantısı da destekler. Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.

Sepet modülü, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisi olan sepet kimliğine göre verileri işler. 

Aşağıdaki resimde fabrikam sitesindeki bir sepet sayfası örneği gösterilmektedir.

![Fabrikam sitesindeki bir sepet modülü örneği.](./media/cart2.PNG)

Aşağıdaki resimde fabrikam sitesindeki bir sepet sayfası örneği gösterilmektedir. Bu örnekte, bir satır maddesi için işleme masrafı vardır.

![Satır ögesi için işleme ücreti bulunan bir sepet modülü örneği.](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a>Sepet modülü özelliklerini ve yuvaları

| Özellik | Değerler | Tanım |
|----------------|--------|-------------|
| Başlık | Başlık metmi ve başlık etiketi (**H1**, **H2**, **H3**, **H4**, **H5** veya **H6**) | "Alışveriş çantası" veya "Sepetinizdeki maddeler" gibi bir sepet başlığı. |
| Stokta yok hatalarını göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, alışveriş sepeti sayfası stokla ilgili hataları gösterir. Sitede stok denetimleri uygulanıyorsa bu özelliği **Doğru** olarak ayarlamanız önerilir. |
| Kalemler için sevkiyat masraflarını göster | **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa, bu bilginin var olması durumunda sepet satırı maddeleri sevkiyat giderlerini gösterir. Kullanıcılar ödeme akışında yalnızca sevkiyatı seçtiğindan bu özellik Fabrikam temasında desteklenmez. Ancak, varsa bu özellik diğer iş akışlarında etkinleştirilebilir. |
| Mevcut promosyonları göster| **Doğru** veya **yanlış** | Bu özellik **Doğru** olarak ayarlanırsa alışveriş sepeti, içindeki ürünlere göre mevcut promosyonları gösterir. Bu özellik Dynamics 365 Commerce sürüm 10.0.16'da kullanılabilir. |

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Sepet modülünde kullanılabilen modüller

- **Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler. İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır. "Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.
- **Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir. Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar. Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçme modülü](store-selector.md).

## <a name="module-properties"></a>Modül özellikleri

Aşağıdaki sepet modülü ayarları **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilecek ayarlara sahiptir:

- **Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır. Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.
- **Stok** - Stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).
- **Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır. Rota, Tesis düzeyinde konfigüre edilebilir ve perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri geçirmesine olanak sağlar.

> [!IMPORTANT]
> Dynamics 365 Commerce 10.0.14 sürümü ve sonrasında, sepetteki maddeler, Commerce Headquarters'daki çevrimiçi mağazanın çevrimiçi işlevsellik profilinde tanımlanan ayarlara göre toplanır. Bir çevrimiçi işlevsellik profili oluşturma ve toplama için gerekli özellikleri ayarlama hakkında daha fazla bilgi için, bkz. [Çevrimiçi işlevsellik profili oluşturma](online-functionality-profile.md).

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır. Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.

## <a name="add-a-cart-module-to-a-page"></a>Sayfaya sepet modülü ekleme

Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.
1. **Parça seç** iletişim kutusunda, **Sepet** modülünü seçin.
1. **Parça adı** altında, **Sepet parçası** için bir ad girin ve **Tamam**'ı seçin.
1. **Sepet** yuvasını seçin.
1. Sağdaki Özellikler bölmesinde, Kurşun Kalem sembolünü seçin, alana başlık metnini girin ve onay işareti simgesini seçin.
1. **Sepet** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, şablon için bir ad girin.
1. Anahat ağacında **Gövde** yuvasını seçin, üç nokta (**...**) ve sonra **Parça ekle**'yi seçin.
1. **Parça seç** iletişim kutusunda **Sepet parçası** öğesini ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon Seç** iletişim kutusunda oluşturduğunuz şablonu seçin, sayfa adı girin ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Hediye kartı modülü](add-giftcard.md)

[Perakende kanalları için stok kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md)

[Çevrimiçi işlevsellik profili oluşturma](online-functionality-profile.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
