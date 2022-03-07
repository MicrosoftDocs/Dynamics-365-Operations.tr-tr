---
title: Hediye kartı modülü
description: Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.
author: anupamar-ms
ms.date: 08/02/2021
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
ms.openlocfilehash: 5a4aaf8e072f6547fe1dcf6fa156d2e144fd03ed806a2dc809a2cedb991461f7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728351"
---
# <a name="gift-card-module"></a>Hediye kartı modülü

[!include [banner](includes/banner.md)]

Bu konu hediye kartı modüllerini kapsamaktadır ve Microsoft Dynamics 365 Commerce'ın site sayfalarına nasıl ekleneceğini açıklamaktadır.

E-ticaret hareketlerinde kullanılan genel bir ödeme biçimi olarak hediye kartı kabul etmek üzere ödeme modülünde bir hediye kartı modülü kullanılabilir. Hediye kartı modülü Dynamics 365, SVS ve Givex hediye kartlarını destekler. SVS ve Givex hediye kartları, Adyen ödeme sağlayıcısı aracılığıyla kullanılır. SVS ve Givex gibi harici hediye kartları desteği hakkında daha fazla bilgi için bkz. [Harici hediye kartları için destek](./dev-itpro/gift-card.md).

> [!NOTE]
> Dynamics 365 Commerce 10.0.11 sürümünde ödeme akışı sırasında SVS ve Givex hediye kartlarının kullanım desteği bulunur. 

İki hediye kartı modülü mevcuttur:

- **Hediye kartı** – Bu modül, geçerli bir ödeme şekli olarak bir hediye kartından yararlanmak için ödeme sayfasında kullanılabilir. 
- **Hediye kartı bakiyesi denetimi** – Bu modül herhangi bir sayfada, bir hediye kartındaki bakiyeyi denetlemek için kullanılabilir. Bu modül Commerce 10.0.14 sürümü ve sonrasında bulunur.

> [!NOTE]
> Hediye kartı bakiyesi denetleme modülü desteği Dynamics 365 Commerce 10.0.14 sürümünde mevcuttur.

Aşağıdaki resimde ödeme sayfasında kullanılan bir hediye kartı modülü örneği gösterilmektedir.

![Hediye kartı modülü örneği.](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Modül özellikleri

- **Ek alanları göster** – Bu özellik, her zaman varsayılan olarak görüntülenen hediye kartı numarasına ek olarak, hediye kartları için hangi alanların görüntüleneceğini tanımlar. Örneğin, bazı hediye kartları bir kişisel kimlik numarası (PIN) görüntülemeyi ve başka hediye kartları PIN ve son kullanma tarihini görüntülemeyi destekler. Alternatif olarak, bu özellik yalnızca hediye kartı numarasını görüntüleyebilen ve ek alanlar içermeyen "Hiçbiri" seçeneğine ayarlanabilir.

    Aşağıdaki değerler desteklenir:

    - PIN
    - Bitiş tarihi
    - PIN ve son kullanma tarihi 
    - Hiçbiri

- **Konuk kullanıcılar için etkinleştir**: Bu özellik etkinleştirildiğinde konuk kullanıcılar, hediye kartlarındaki bakiyeleri kullanabilir veya denetleyebilir. Bu özellik, Commerce genel merkezinde hediye kartları için anonim erişimin (konuk erişimi) etkinleştirilmesini gerektirir. Daha fazla bilgi için bkz. [Konuk ödemeleri için hediye kartı ödemelerini etkinleştirme](#enable-gift-card-payments-for-guest-checkout).

> [!IMPORTANT]
> **Konuk kullanıcılar için etkinleştir** özelliği, Commerce 10.0.21 sürümü itibarıyla kullanılabilir. Bunun için Commerce modül kitaplığı paketi sürüm 9.31'in yüklü olması gerekir.

## <a name="site-settings-for-gift-card-modules"></a>Hediye kartı modülleri için site ayarları

Commerce site oluşturucuda **Site Ayarları \> Uzantılar** altında, **Desteklenen hediye kartı türü** adında bir hediye kartı modülü ayarı vardır. Bu ayar üç değeri destekler:
- **Dynamics 365 hediye kartı** – Bu ayar uygulandığında, hediye kartı modülü yalnızca Dynamics 365 hediye kartlarının kullanılmasına izin verir. Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.
- **SVS ve Givex hediye kartları** – Bu ayar uygulandığında, hediye kartı modülü yalnızca Givex ve SVS hediye kartlarının kullanılmasına izin verir. Bu ayar e-Ticaret sitesindeki oturum açmış ve anonim kullanıcılar için desteklenir.
- **Dynamics 365, SVS ve Givex hediye kartları** – Bu ayar uygulandığında, hediye kartı modülü Dynamics 365, Givex ve SVS hediye kartlarının kullanılmasına izin verir. Bu ayar yalnızca e-Ticaret sitesindeki oturum açmış kullanıcılar için desteklenir.

> [!IMPORTANT]
> Bu ayarlar Dynamics 365 Commerce 10.0.11 sürümünde bulunur ve yalnızca SVS veya Givex hediye kartları için desteğe gereksinim duyarsanız gereklidir. Dynamics 365 Commerce'nin eski sürümlerinden birini güncelleştiriyorsanız, appSettings. json dosyasını el ile güncelleştirmeniz gerekir. AppSettings.json dosyasını güncelleştirme yönergeleri için bkz. [SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>E-ticaret mağazasında kullanmak üzere dahili hediye kartlarını uzatın

Varsayılan olarak, dahili hediye kartları e-ticaret mağazalarında kullanım için optimize edilmez. Bu nedenle, dahili hediye kartlarının ödeme için kullanılmasına izin vermeden önce, onları daha güvenli hale getirmek amacıyla kartları uzantılarla yapılandırmalısınız. Dahili hediye kartlarının üretimde kullanılmasına izin vermeden önce, genişletmeniz gereken hediye kartı alanları şunlardır:

- **Hediye kartı numarası** – Numara serileri, dahili hediye kartları için hediye kartı numaraları oluşturmak amacıyla kullanılır. Numara serileri kolayca tahmin edilebileceği için, hediye kartı numaralarının oluşumunu, verilen hediye kartı numaraları için rasgele, kriptografik olarak güvenli dizeler kullanılacak şekilde genişletmelisiniz.
- **GetBalance** – **GetBalance** API, hediye kartı bakiyelerini aramak için kullanılır. Varsayılan olarak, bu API herkesin kullanımına açıktır. Hediye kartı bakiyelerini aramak için PIN gerekli değilse deneme yanılma saldırılarının **GetBalance** API'yi kullanarak bakiyeleri olan hediye kartı numaralarını arama riski olur. Dahili hediye kartları ve API azaltma için PIN gereksinimlerinin her ikisini de uygulayarak, bu riski hafifletebilirsiniz.
- **PIN** – Varsayılan olarak, dahili hediye kartları PIN'leri desteklemez. Bakiyeleri aramak için bir PIN gerekli olacak şekilde dahili hediye kartlarını genişletmelisiniz. Bu işlev ayrıca peş peşe yanlış PIN girme denemelerinden sonra hediye kartlarını kilitlemek için de kullanılabilir.

## <a name="enable-gift-card-payments-for-guest-checkout"></a>Konuk ödemeleri için hediye kartı ödemelerini etkinleştirme

Varsayılan olarak, hediye kartı ödemeleri konuk (anonim) ödeme için etkin değildir. Bunu etkinleştirmek için şu adımları izleyin.

1. Commerce genel merkezinde **Retail ve Commerce \> Kanal ayarı \> POS ayarı \> POS \> POS İşlemleri**'ne gidin.
1. Kılavuz üstbilgisini seçin ve tutun (veya sağ tıklayın) ve sonra **Sütun ekle**'yi seçin.
1. **Sütun ekle** iletişim kutusunda, **AllowAnonymousAccess** onay kutusunu seçin.
1. **Güncelleştir**'i seçin
1. **520** (Hediye kartı bakiyesi) ve **214** işlemleri için **AllowAnonymousAccess** değerini **1** olarak ayarlayın.
1. **Kaydet**'i seçin.
1. Değişiklikleri kanal veritabanıyla eşitlemek için **1090** zamanlayıcı işini yürütün. 

## <a name="add-a-gift-card-module-to-a-page"></a>Sayfaya hediye kartı modülü ekleme

Bir ödeme sayfasına hediye kartı modülü ekleme ve gerekli özellikleri ayarlama yönergeleri için bkz. [Ödeme modülü](add-checkout-module.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Sepet modülü](add-cart-module.md)

[Sepet simgesi modülü](cart-icon-module.md)

[Ödeme modülü](add-checkout-module.md)

[Ödeme modülü](payment-module.md)

[Sevkiyat adresi modülü](ship-address-module.md)

[Teslimat seçenekleri modülü](delivery-options-module.md)

[Malzeme çekme bilgileri modülü](pickup-info-module.md)

[Sipariş ayrıntıları modülü](order-confirmation-module.md)

[Harici hediye kartları için destek](./dev-itpro/gift-card.md)

[SDK ve modül kitaplığı güncelleştirmeleri](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
