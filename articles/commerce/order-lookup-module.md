---
title: Sipariş arama modülü
description: Bu makalede, sipariş arama modülü kapsanmaktadır ve bunun Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağı açıklanmaktadır.
author: bicyclingfool
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 8c60ed0c334bf09916dd633302c6d813ea6f16b6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281467"
---
# <a name="order-lookup-module"></a>Sipariş arama modülü

[!include [banner](includes/banner.md)]

Bu makalede, sipariş arama modülü kapsanmaktadır ve bunun Microsoft Dynamics 365 Commerce'te nasıl yapılandırılacağı açıklanmaktadır.

Sipariş arama modülü, müşterilerin bir e-ticaret sitesine yerleştirilen siparişleri aramaları için kullanabilecekleri bir form sağlar. [Konuk ödemeleri için sipariş aramayı etkinleştirme](order-lookup-guest.md) özelliğinin bir parçası olarak kullanılır. Sipariş arama modülü, bir e-ticaret sitesi, perakende satış noktası (POS) veya bir çağrı merkezi aracılığıyla gönderilen siparişleri aramak için kullanılabilir. Form hem konuk kullanıcılar hem de kayıtlı kullanıcılar tarafından gönderilen siparişleri alabilir.

Aşağıdaki şekilde, sipariş arama modülü tarafından oluşturulan formun bir örneği gösterilmektedir. Müşteriler formu doldurup **Siparişinizi bulun** seçeneğini belirlediklerinde sipariş ayrıntıları sayfasına yönlendirilirler.

![Sayfadaki sipariş arama modülü için form.](./media/OrderLookup_module.PNG)

## <a name="order-lookup-module-properties"></a>Sipariş arama modülü özellikleri

| Özellik adı     | Değer     | Tanım |
|-------------------|-----------|-------------|
| Başlık           | Metin      | Formun üst kısmında görünen başlık (örneğin, "Siparişinizi bulun"). |
| Zengin metin         | Zengin metin | Başlığın altında görüntülenen isteğe bağlı açıklayıcı metin. |
| Sipariş durumu türü | Enum      | <p>Sipariş onay koduna ek olarak formun müşteriden isteyeceği bilgi türünü seçin. Şu anda aşağıdaki değerler desteklenmektedir:</p><ul><li><b>E-posta</b>: Form, müşterilerin siparişi yerleştirdiklerinde kullandıkları e-posta adresini girebildikleri bir alan içermektedir.</li><li><b>Hiçbiri</b>: Form, sipariş onay kodu dışında hiçbir bilgi istemez.</li></ul> |

## <a name="add-an-order-lookup-module-to-a-page"></a>Sayfaya sipariş arama modülü ekleme

Sipariş arama modülü e-ticaret sitenizin herhangi bir sayfasının gövdesine eklenebilir. Konuk ödemeleri için sipariş aramayı etkinleştirmek için sipariş arama modülünü kullanmak istiyorsanız bunu kullanıcının oturum açmasını gerektirmeyen bir sayfaya eklediğinizden emin olun. Commerce site oluşturucu ağaç görünümünde bir sayfanın **Oturum açılması gerekiyor mu?** ayarını bulmak için **Varsayılan sayfa (Gerekli)** yuvasını seçin ve sağ bölmenin altına bakın.

## <a name="additional-resources"></a>Ek kaynaklar

[Konuk ödemeleri için sipariş aramayı etkinleştirme](order-lookup-guest.md)

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
