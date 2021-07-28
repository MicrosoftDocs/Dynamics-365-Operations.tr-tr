---
title: Alt bilgi modülü
description: Bu konu altbilgi modüllerini ve bunların nasıl Dynamics 365 Commerce içine yazılacağını kapsamaktadır.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: 2768317092f43862f26847c4b4c57f5929d43912
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346790"
---
# <a name="footer-module"></a>Alt bilgi modülü  

[!include [banner](includes/banner.md)]

Bu konu altbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.

Altbilgi modülü, sayfa altbilgisinde gösterilen modülleri barındırmak için kullanılan özel bir kapsayıcıdır. Örneğin, **Bize başvurun** ve **Mağaza ilkeleri** sayfaları gibi çeşitli sayfaların bağlantılarını içerebilir.

Aşağıdaki resimde site sayfasında kullanılan bir altbilgi modülü örneği gösterilmektedir.

![Alt bilgi modülü örneği.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Alt bilgi modülü özellikleri 

Çoğu kapsayıcı gibi bir altbilgi modülü de başlık ve genişlik için özellikleri destekler. Çoklu alt bilgi kategorisi modüllerinin eklenmesini de destekler. Eklenen her altbilgi kategorisi modülü altbilgi modülünde bir sütun olarak işlenir.

## <a name="modules-available-in-a-footer-module"></a>Altbilgi modülünde bulunan modüller

**Alt bilgi maddeleri** – bir altbilgi öğeleri modülü bir başlık, bir resim ve bir bağlantı içerebilir. Başlık tek başına veya bir görüntü ve bir bağlantıyla birlikte kullanılabilir. Alt bilgideki her bağlantı yalnızca metin içerecek şekilde yapılandırılabilir (örneğin, "bize başvurun" ve "Gizlilik" bağlantıları) veya hem metin, hem de resim (örneğin, sosyal medya bağlantıları) vardır.

**Başa dön** – en başa dön modülü sayfanın başına hızlı gezinti için bir bağlantı sağlar. Bir hedef gerekli. Varsayılan hedef değeri, kullanıcıyı sayfanın en üstüne götüren \# değeridir.

## <a name="create-a-footer-module"></a>Alt bilgi modülü oluşturma

1. **Parçalar**'a gidin ve yeni parça oluşturmak için **Yeni**'yi seçin.
1. **Yeni parça** iletişim kutusunda **Kapsayıcı** modülünü seçin, parça için bir ad girin ve sonra **Tamam**'ı seçin.
1. **Varsayılan Konteyner** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **alt bilgi kategorisi** modülünü seçin ve **Tamam**'ı seçin.
1. **Altbilgi kategorisi** yuvası için üç nokta (**...**) düğmesini seçin ve **Modül Ekle**'yi seçin.
1. **Modül Ekle** iletişim kutusunda **alt bilgi öğesi** modülünü seçin ve **Tamam**'ı seçin.
1. **Altbilgi madde** yuvasını seçin, daha sonra sağdaki özellikler bölmesinde, başlığı, bağlantı ve metin bağlantısını ve resmi gerektiği gibi yapılandırın.
1. Daha fazla alt bilgi öğesi eklemek için 5 ile 7. adımları tekrarlayın.
1. Alt bilginize "başa dön" bağlantısı eklemek için **Altbilgi kategorisi** yuvasında üç nokta (**...**) düğmesini ve sonra da **Modül Ekle** seçeneğini seçin.
1. **Modül Ekle** iletişim kutusunda **başa dön** modülünü seçin ve **Tamam**'ı seçin.
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