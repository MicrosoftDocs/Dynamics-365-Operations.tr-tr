---
title: E-ticaret dijital hediye kartları
description: Bu konuda, dijital hediye kartlarının Microsoft Dynamics 365 Commerce'ün e-ticaret uygulamasında nasıl çalıştığı açıklanmaktadı . Ayrıca, önemli yapılandırma adımlarının genel bir görünümünü sağlar.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982678"
---
# <a name="e-commerce-digital-gift-cards"></a>E-ticaret dijital hediye kartları

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, dijital hediye kartlarının Microsoft Dynamics 365 Commerce'ün e-ticaret uygulamasında nasıl çalıştığı açıklanmaktadı . Ayrıca, önemli yapılandırma adımlarının genel bir görünümünü sağlar.

Dynamics 365 Commerce'te, dijital hediye kartlarının satın alması, sistemdeki diğer ürünlerin satın alma işlemiyle aynı akışı izler. Konfigüre edilecek ek modül yoktur. Sepete birden fazla hediye kartı eklenirse, hediye kartı maddeleri tek bir satış satırında toplanmazlar. Her satış satırı ayrı bir hediye kartı numarası kullanılarak faturalandığından, bu davranış gereklidir.

Dijital hediye kartlarının satın alınması, Dynamics 365 Commerce 10.0.16 ve sonraki sürümlerinde desteklenir.

Aşağıdaki çizimde, Fabrikam e-ticaret sitesindeki dijital hediye kartının ürün ayrıntıları sayfası (PDP) örneği gösterilmektedir.

![Fabrikam e-ticaret sitesindeki dijital hediye kartı PDP örneği](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Commerce Headquarters'da dijital hediye kartı özelliğini açma

Dijital hediye kartlarının Dynamics 365 Commerce'te satın alma akışında çalışması için **Commerce Headquarters'da e-ticaret özelliğinde satın hediye kartı satın alma** özelliği açık olmalıdır. Özelliği, aşağıdaki şekilde gösterildiği gibi Commerce Headquarters'da **Özellik yönetimi** çalışma alanında bulabilirsiniz.

![Commerce Headquarters'da özellik yönetimi çalışma alanı](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Commerce Headquarters'da dijital hediye kartı yapılandırma

Commerce Headquarters'da dijital hediye kartı ürünleri yapılandırılmalıdır. Bu işlem, diğer ürünler için kullanılan sürece benzerdir. Ancak, aşağıdaki önemli adımlar satın alma için hediye kartlarının yapılandırmasına özgüdür. Ürünlerin nasıl oluşturulacağı ve yapılandırılacağı hakkında daha fazla bilgi için bkz. [Commerce'de yeni ürün oluşturma](create-new-product-commerce.md).

- **Yeni ürün** iletişim kutusunda dijital hediye kartı ürünlerini yapılandırdığınızda, **Ürün türü** alanını **Hizmet** olarak ayarlayın. (İletişim kutusunu açmak için **Perakende ve ticaret \>Ürünler ve kategoriler \> Kategorilere göre ürünler**'e gidin ve **Yeni**'yi seçin.) **Hizmet** türündeki ürünler, sipariş alınmadan önce kullanılabilir stok için denetlenmez. Daha fazla bilgi için [Yeni ürün oluşturma](create-new-product-commerce.md#create-a-new-product) konusuna bakın.
- Aşağıdaki çizimde gösterildiği gibi, **Commerce parametreleri** sayfasında, **Deftere nakil** sekmesinde, **Hediye kartı ürünü** alanı **Dijital Hediye Kartı** olarak ayarlanmalıdır. Ürün harici bir hediye kartıysa, daha fazla bilgi için [Harici hediye kartları için destek](./dev-itpro/gift-card.md) bölümüne bakın.

    ![Commerce Headquarters'daki hediye kartı ürün alanı](./media/PostGiftcard.png)

- Bir hediye kartının önceden tanımlanmış birden fazla tutarı (örneğin, $25, $50 ve $100) desteklemesi gerekiyorsa bu önceden tanımlanmış tutarları ayarlamak için **Boyut** boyutu kullanılmalıdır. Her önceden tanımlanmış tutar bir varyant olacaktır. Daha fazla bilgi için bkz. [Ürün boyutları](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json).
- Müşterilerin bir hediye kartı için özel bir tutar belirtmesi gerekiyorsa önce özel bir tutara izin veren bir varyant ayarlayın. Sonra, ürünü, **Kategoride serbest bırakılmış ürünler** sayfasından açın ve sonra **Commerce** hızlı sekmesinde, aşağıdaki çizimde gösterildiği gibi, **Fiyat girin** alanını **Yeni fiyat girilmeli** şekilde ayarlayın. Bu ayar, bir PDP'de ürüne göz attıklarında müşterilerin fiyat girebilmesini sağlar.

    ![Commerce Headquarters'da fiyat girme alanı](./media/KeyInPrice.png)

- Dijital hediye kartının teslimat şekli **Elektronik** olarak ayarlanmalıdır. **Teslimat şekilleri** sayfasında (**Perakende ve ticaret \> Kanal kurulumu \> Teslimat şekilleri**), liste bölmesinden **Elektronik** teslim modunu seçin ve sonra, aşağıdaki çizimde gösterildiği gibi, **Ürünler** hızlı sekmesinde dijital hediye kartı ürününü kılavuza ekleyin. Daha fazla bilgi için bkz. [Teslimat koşullarını ayarlama](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

    ![Commerce Headquarters'da Teslimat modundaki dijital hediye kartı ürünleri](./media/ElectronicMode.PNG)

- Bir çevrimiçi işlevsellik profilinin oluşturulduğundan ve Commerce Headquarters'daki çevrimiçi mağazanızla ilişkili olduğundan emin olun. İşlevsellik profilinde, **Toplu ürünler** seçeneğini **Evet** olarak ayarlayın. Bu ayar, hediye kartları hariç tüm maddelerin toplanmasını sağlar. Daha fazla bilgi için bkz. [Çevrimiçi işlevsellik profili oluşturma](online-functionality-profile.md).
- Bir hediye kartı faturalandıktan sonra müşterilerin e-posta almalarını sağlamak için **E-posta bildirim profilleri** sayfasında yeni bir e-posta bildirim türü oluşturun ve **E-posta bildirim türü** alanını **Hediye kartı oluştur** şekilde ayarlayın. Daha fazla bilgi için, bkz. [E-posta bildirimi profili ayarlama](email-notification-profiles.md).

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Commerce Site Builder ortam kitaplığına ürün görüntüleri ekleme

Commerce Site Builder ortam kitaplığına dijital hediye kartı ürünleri için ürün görüntüleri eklemeniz gerekir. Hediye kartı resim dosyalarının dosya adlarının ürün görüntüleri için sitenizin adlandırma kurallarına uymasını sağlayın. Daha fazla bilgi için bkz. [Görüntüleri yükleme](dam-upload-images.md).

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Commerce Site Builder'da dijital hediye kartı için özel bir tutar yapılandırma

Dijital hediye kartı özel bir tutara izin verecek şekilde yapılandırılacaksa bu davranışın sitenizin PDP'lerinde kullanılan [satın alma kutusu modülünde](add-buy-box.md) de etkinleştirilmesi gerekir. Satın alma kutusu modülü, özel tutarlara izin vermek için modül yapılandırmasını destekler. Ayrıca, özel tutarlar için izin verilen minimum ve maksimum tutarları de tanımlayabilirsiniz.

Commerce Site Builder'da dijital hediye kartının özel tutarını yapılandırmak için aşağıdaki adımları izleyin.

1. Sitenizin PDP'lerinde kullanılan satın alma kutusu modülüne gidin. Bu satın alma kutusu modülü bir parça, şablon veya sayfaya uygulanabilir.
1. **Düzenle** öğesini seçin.
1. Sağdaki Özellikler bölmesinde, **Özel fiyata izin ver** onay kutusunu seçin.
1. İsteğe bağlı: Özel tutarlara ait minimum ve maksimum tutarlar tanımlamak için **Minimum fiyat** ve **Maksimum fiyat** altında tutarlar girin.
1. **Düzenlemeyi bitir** i seçin ve sonra **Yayınla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Satın alma kutusu modülü](add-buy-box.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[Commerce'ta yeni ürün oluşturma](create-new-product-commerce.md)

[Teslimat şekillerini ayarla](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Ürün boyutları](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[E-posta bildirimi profili ayarlama](email-notification-profiles.md)

[Çevrimiçi işlevsellik profili oluşturma](online-functionality-profile.md)

[Harici hediye kartları için destek](./dev-itpro/gift-card.md)