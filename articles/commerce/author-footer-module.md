---
title: Alt bilgi modülü
description: Bu makale altbilgi modüllerini ve bunların nasıl Dynamics 365 Commerce içine yazılacağını kapsamaktadır.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e7796d9700eabc923f2bb45187832d5993ae56e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876624"
---
# <a name="footer-module"></a>Alt bilgi modülü  

[!include [banner](includes/banner.md)]

Bu makale altbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.

Altbilgi modülü, sayfa altbilgisinde gösterilen modülleri barındırmak için kullanılan özel bir kapsayıcıdır. Örneğin, **Bize başvurun** ve **Mağaza ilkeleri** sayfaları gibi çeşitli sayfaların bağlantılarını içerebilir.

Aşağıdaki resimde site sayfasında kullanılan bir altbilgi modülü örneği gösterilmektedir.

![Alt bilgi modülü örneği.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Alt bilgi modülü özellikleri 

Çoğu kapsayıcı gibi bir altbilgi modülü de başlık ve genişlik için özellikleri destekler. Çoklu alt bilgi kategorisi modüllerinin eklenmesini de destekler. Eklenen her altbilgi kategorisi modülü altbilgi modülünde bir sütun olarak işlenir.

## <a name="modules-available-in-a-footer-module"></a>Altbilgi modülünde bulunan modüller

**Alt bilgi maddesi** – Bir altbilgi öğeleri modülü bir başlık veya bir bağlantı içerebilir. Başlık genellikle bir altbilgi bölümü başlığı olarak kullanılır.  Alt bilgideki her bağlantı yalnızca metin içerecek şekilde yapılandırılabilir (örneğin, "bize başvurun" ve "Gizlilik" bağlantıları) veya hem metin, hem de resim (örneğin, sosyal medya bağlantıları) vardır. Hem başlık hem de bağlantı sağlanırsa, başlık özelliği bağlantıya göre öncelik kazanır. 

**Başa dön** – en başa dön modülü sayfanın başına hızlı gezinti için bir bağlantı sağlar. Bir hedef gerekli. Varsayılan hedef değeri, kullanıcıyı sayfanın en üstüne götüren \# değeridir.

## <a name="create-a-footer-module"></a>Alt bilgi modülü oluşturma

1. **Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.
1. **Parça seçin** iletişim kutusunda **Konteyner** modülünü seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.
1. **Varsayılan konteyner** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Alt bilgi kategorisi** modülünü seçin ve **Tamam**'ı seçin.
1. **Alt bilgi kategorisi** alanında, üç nokta (**...**) düğmesini seçin ve **Modül ekle**'yi seçin.
1. **Modülleri seç** iletişim kutusunda **Alt bilgi öğesi** modülünü seçin ve **Tamam**'ı seçin.
1. **Altbilgi madde** yuvasını seçin, daha sonra sağdaki özellikler bölmesinde, başlığı, bağlantı ve metin bağlantısını ve resmi gerektiği gibi yapılandırın.
1. Daha fazla alt bilgi öğesi eklemek için 5 ile 7. adımları tekrarlayın.
1. Alt bilginize "başa dön" bağlantısı eklemek için **Alt Bilgi kategorisi** alanında üç nokta (**...**) düğmesini ve sonra **Modül ekle** seçeneğini belirleyin.
1. **Modülleri seç** iletişim kutusunda **Başa dön** modülünü seçin ve **Tamam**'ı seçin.
1. **Başa dön** yuvasını seçin, daha sonra sağdaki özellikler bölmesinde, metni ve diğer modül özelliklerini gerektiği gibi yapılandırın.
1. Parçayı iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

Üstbilginin her sayfada göründüğünü garantilemek için, site için oluşturulan her sayfa şablonunda aşağıdaki adımları izleyin.

1. **Varsayılan sayfanın** **Altbilgi** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.
1. Şablonu iade etmek için **Düzenlemeyi bitir**'i seçin, ardından yayımlamak için **Yayımla**'yı seçin.

Parçayı sayfa şablonlarına ekleyerek, altbilginin her sayfada oluşturulmasını sağlamaya yardımcı olursunuz.

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Kapsayıcı modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Alışveriş sepeti modülü](add-cart-module.md)

[Ödeme yapma modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
