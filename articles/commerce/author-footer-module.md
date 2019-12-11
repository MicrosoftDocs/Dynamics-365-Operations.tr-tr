---
title: Alt bilgi modülü
description: Bu konu altbilgi modüllerini ve bunların nasıl Dynamics 365 Commerce içine yazılacağını kapsamaktadır.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697325"
---
# <a name="footer-module"></a>Alt bilgi modülü  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu altbilgi modüllerini ve bunların nasıl Microsoft Dynamics 365 Commerce'te oluşturacağını açıklamaktadır ve kapsamaktadır.

## <a name="overview"></a>Genel Bakış

Altbilgi modülü, sayfa altbilgisinde gösterilen modülleri barındırmak için kullanılan özel bir kapsayıcıdır. Örneğin, **Bize başvurun** ve **Mağaza ilkeleri** sayfaları gibi çeşitli sayfaların bağlantılarını içerebilir.

## <a name="footer-module-properties"></a>Alt bilgi modülü özellikleri 

Çoğu konteyner gibi bir altbilgi modülü de başlık ve genişlik için özellikleri destekler. Çoklu alt bilgi kategorisi modüllerinin eklenmesini de destekler. Eklenen her altbilgi kategorisi modülü altbilgi modülünde bir sütun olarak işlenir.

## <a name="modules-available-in-a-footer-module"></a>Altbilgi modülünde bulunan modüller

**Alt bilgi maddeleri** – bir altbilgi öğeleri modülü bir başlık, bir resim ve bir bağlantı içerebilir. Başlık tek başına veya bir görüntü ve bir bağlantıyla birlikte kullanılabilir. Alt bilgideki her bağlantı yalnızca metin içerecek şekilde yapılandırılabilir (örneğin, "bize başvurun" ve "Gizlilik" bağlantıları) veya hem metin, hem de resim (örneğin, sosyal medya bağlantıları) vardır.

**Başa dön** – en başa dön modülü sayfanın başına hızlı gezinti için bir bağlantı sağlar. Bir hedef gerekli. Varsayılan hedef değeri, kullanıcıyı sayfanın en üstüne götüren # değeridir.

## <a name="author-a-footer-module"></a>Alt bilgi modülü düzenleme

1. Gezinti bölmesinde, **parçalar**'ı seçin ve sonra **yeni sayfa parçası**'nı seçin.
1. **Yeni sayfa parçası** iletişim kutusunda altbilgi modülünü seçin, sayfa parçası için bir ad girin ve sonra **Tamam**'ı seçin.
1. Soldaki anahat ağacı 'nda üç nokta düğmesini (**...**) ekleyin ve sonra da **Modül Ekle** seçeneğini seçin.
1. **Modül Ekle** iletişim kutusunda alt bilgi kategorisi modülünü seçin ve **Tamam**'ı seçin.
1. Soldaki anahat ağacı alt bilgi kategori modülü için üç nokta düğmesini ve sonra da **Modül Ekle** seçeneğini seçin.
1. **Modül Ekle** iletişim kutusunda alt bilgi öğesi modülünü seçin ve **Tamam**'ı seçin.
1. Anahat ağacında altbilgi madde modülünü seçin. Daha sonra sağdaki özellikler bölmesinde, başlığı, bağlantı ve metin bağlantısını ve resmi gerektiği gibi yapılandırın.
1. Daha fazla alt bilgi öğesi eklemek için 5 ile 7. adımları tekrarlayın.
1. Alt bilginize "başa dön" bağlantısı eklemek için üç nokta düğmesini ve sonra da **Modül Ekle** seçeneğini seçin.
1. **Modül Ekle** iletişim kutusunda başa dön modülünü seçin ve **Tamam**'ı seçin.
1. Anahat ağacında başa dön modülünü seçin. Daha sonra sağdaki Özellikler bölmesinde, en başa dön modülünü gerektiği gibi yapılandırın.
1. Sayfa parçasını kaydedin, giriş yapın ve yayımlayın.

Site için oluşturulan her sayfa şablonunda, aşağıdaki adımları izleyin.

1. Varsayılan sayfanın **ana** yuvasında, altbilgi modülünde, oluşturduğunuz altbilgi parçasını ekleyin.
1. Şablonu kaydedin, giriş yapın ve yayımlayın.

Sayfa parçasını sayfa şablonlarına ekleyerek, altbilginin her sayfada oluşturulmasını sağlamaya yardımcı olursunuz.

## <a name="additional-resources"></a>Ek kaynaklar

[Başlangıç paketine genel bakış](starter-kit-overview.md)

[Konteyner modülü](add-container-module.md)

[Satın alma kutusu modülü](add-buy-box.md)

[Sepet modülü](add-cart-module.md)

[Ödeme modülü](add-checkout-module.md)

[Sipariş onayı modülü](order-confirmation-module.md)

[Üst bilgi modülü](author-header-module.md)

[Alt bilgi modülü](author-footer-module.md)
