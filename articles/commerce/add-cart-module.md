---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411285"
---
# <a name="cart-module"></a>Sepet modülü

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Özet

Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır. Ayrıca, modül sipariş özeti gösterir ve müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlar.

Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler. Ayrıca bir **Alışverişe geri git** bağlantısı da destekler. Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.

Sepet modülü, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisi olan sepet kimliğine göre verileri işler. 

Aşağıdaki resimde fabrikam sitesindeki bir sepet sayfası örneği gösterilmektedir.

![Sepet modülü örneği](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a>Sepet modülü özelliklerini ve yuvaları

Sepet modülü bir **Başlık** özelliğine sahiptir ve bu **Alışveriş sepeti** ve **Sepetinizdeki öğeler** gibi değerlere ayarlanabilir. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Sepet modülünde kullanılabilen modüller

- **Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler. İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır. "Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.
- **Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir. Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar. Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçme modülü](store-selector.md).

## <a name="module-properties"></a>Modül özellikleri

Aşağıdaki sepet modülü ayarları **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilecek ayarlara sahiptir:

- **Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır. Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.
- **Stok** - Stok ayarlarının nasıl uygulanacağı hakkında bilgi için bkz. [Envanter ayarları uygula](inventory-settings.md).
- **Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır. Rota, Tesis düzeyinde konfigüre edilebilir ve perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri geçirmesine olanak sağlar.

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır. Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.

## <a name="add-a-cart-module-to-a-page"></a>Sayfaya sepet modülü ekleme

Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Sayfa Parçaları**'na gidin ve yeni parçası oluşturmak için **Yeni**'yi seçin.
1. **Yeni Sayfa Parçası** iletişim kutusunda, **Sepet kutusu** modülünü seçin.
1. **Sayfa parçası adı** altında, **Sepet parça** için bir ad girin ve **Tamam** 'ı seçin.
1. **Sepet** yuvasını seçin.
1. Sağdaki Özellikler bölmesinde, Kurşun Kalem sembolünü seçin, alana başlık metnini girin ve onay işareti simgesini seçin.
1. **Sepet** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **Mağaza seçici** modülünü seçin ve **Tamam**'ı seçin.
1. **Kaydet**'i seçin, parçayı iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. Bir yeni şablonu oluşturmak için **Şablonlar**'a gidin ve **Yeni**'yi seçin.
1. **Yeni Şablon** iletişim kutusunda **Şablon adı** altında, şablon için bir ad girin.
1. Anahat ağacında **Gövde** yuvasını seçin, üç nokta (**...**) ve sonra **Parça ekle**'yi seçin.
1. **Sayfa Parçası Seç** iletişim kutusunda **Sepet parçası** parçasını ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin, şablonu iade etmek için **Düzenlemeyi bitir**'i ve ardından yayımlamak için **Yayımla**'yı seçin.
1. **Sayfalar**'a gidin ve yeni sayfa oluşturmak için **Yeni**'yi seçin.
1. **Şablon Seç** iletişim kutusunda oluşturduğunuz şablonu seçin, sayfa adı girin ve sonra **Tamam**'ı seçin.
1. **Kaydet**'i seçin ve ardından sayfayı önizlemek için **Önizleme**'yi seçin.
1. Sayfayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Mağaza seçicisi modülü](store-selector.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)

[Perakende kanalları için stok kullanılabilirliğini hesaplama](calculated-inventory-retail-channels.md)
