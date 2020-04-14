---
title: Sepet modülü
description: Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154029"
---
# <a name="cart-module"></a>Sepet modülü

[!include [banner](includes/banner.md)]

Bu konu sepet modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'un site sayfalarına nasıl ekleneceğini açıklamaktadır.

## <a name="overview"></a>Özet

Bir sepet modülü, müşteri kullanıma devam etmeden önce alışveriş sepetine eklenen maddeleri göstermek için kullanılır. Ayrıca, modül sipariş özeti gösterir ve müşterinin promosyon kodları uygulamasını veya kaldırmasını sağlar.

Sepet modülü, oturum açan kullanıma alma ve konuk kullanıma almayı destekler. Ayrıca bir **Alışverişe geri git** bağlantısı da destekler. Bu bağlantı için yolu **Site Ayarları \> Uzantılar \> Rotalar** adresinden yapılandırabilirsiniz.

Sepet modülü, tüm sitede kullanılabilen bir tarayıcı tanımlama bilgisi olan sepet kimliğine göre verileri işler.

## <a name="cart-module-properties-and-slots"></a>Sepet modülü özelliklerini ve yuvaları

Sepet modülü bir **Başlık** özelliğine sahiptir ve bu **Alışveriş sepeti** ve **Sepetinizdeki öğeler** gibi değerlere ayarlanabilir. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Sepet modülünde kullanılabilen modüller

- **Metin bloğu** – bu modül sepet modülündeki özel iletileri destekler. İletiler, içerik yönetim sistemi (CMS) tarafından çalıştırılır. "Siparişinizdeki sorunları için 1-800-Fabrikam ile iletişim" gibi herhangi bir ileti eklenebilir.
- **Mağaza seçici** - Bu modül bir maddenin almak için kullanılabilir olduğu yakındaki mağazaların listesini gösterir. Kullanıcıların yakındaki mağazaları bulabilmesi için bir konum girmesini sağlar. Bu modülle ilgili daha fazla bilgi için bkz. [Mağaza seçme modülü](store-selector.md).

## <a name="cart-module-settings"></a>Sepet modülü ayarları

Sepet modülleri, **Site Ayarları \> Uzantılar** üzerinden yapılandırılabilir:

- **Maksimum miktar** - Bu özellik, alışveriş sepetine eklenebilecek maksimum madde sayısını belirtmekte kullanılır. Örneğin, bir perakende satılan her ürünün yalnızca 10 tanesi tek bir harekette satılabilir olduğuna karar verebilir.
- **Stok denetimi** – değer **doğru** olarak ayarlandığında, yalnızca satın alma kutusu modülü stokta olduğundan emin olduktan sonra alışveriş sepetine bir madde eklenir. Bu stok denetimi hem maddenin sevk edileceği senaryolar için, hem de mağazada yer alacak senaryolar için gerçekleştirilir. Değer **yanlış** olarak ayarlandığında, bir madde alışveriş sepetine eklenmeden önce hiçbir stok denetimi yapılmaz ve sipariş yerleştirilir.
- **Stok tamponu** – Bu özellik, stok için bir tampon numarası belirtmek için kullanılır. Gerçek zamanlı olarak sürdürülür ve birçok müşteri sipariş yerleştirirken, doğru stok sayımının korunması zor olabilir. Bir stok denetimi yapıldığında, stok tampon tutardan azsa, ürün Stokta tükenmiş olarak kabul edilir. Bu nedenle, stok sayımı tam olarak eşitlenmemesi için çeşitli kanallarda hızlı şekilde satış gerçekleştiğinde, stokta olmayan bir maddenin satılması için daha az risk vardır.
- **Alışverişe dön** – Bu özellik, **alışverişe geri dön** bağlantısına ait rotayı belirtmek için kullanılır. Rota, Tesis düzeyinde konfigüre edilebilir ve perakendeciler müşteriyi giriş sayfasına veya sitedeki herhangi bir sayfaya geri geçirmesine olanak sağlar.

## <a name="commerce-scale-unit-interaction"></a>Ticari ölçek birim etkileşimi

Sepet modülü, ürün bilgilerini Commerce Scale Unit API'leri kullanarak alır. Commerce Scale Unit'deki tüm ürün bilgilerini almak için, tarayıcı tanımlama bilgisinden alışveriş sepetinin kodu kullanılır.

## <a name="add-a-cart-module-to-a-page"></a>Sayfaya sepet modülü ekleme

Bir yeni sayfaya sepet modülü eklemek ve gerekli özellikleri ayarlamak için aşağıdaki adımları izleyin.

1. **Sepet parçası** olarak adlandırılan bir parça oluşturun ve yeni parçaya sepet birimi ekleyin.
1. Sepet modülüne başlık ekleyin.
1. Sepet modülüne bir depo seçici modülü ekleyin.
1. Başlık parçasını kaydedin, düzenlemeyi bitirin ve yayımlayın.
1. **Sepet şablonu** adlı bir şablon oluşturun ve yeni oluşturduğunuz sepet parçasını ekleyin.
1. Şablonu kaydedin, düzenlemeyi bitirin ve yayımlayın.
1. Yeni şablonu kullanan bir sayfa oluşturun.
1. Sayfayı kaydet ve önizleyin.
1. Sayfayı düzenlemeyi bitirin ve yayımlayın.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Mağaza seçicisi modülü](store-selector.md)

[Satınalma kutusu modülü](add-buy-box.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
