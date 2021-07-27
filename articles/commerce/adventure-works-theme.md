---
title: Adventure Works temasına genel bakış
description: Bu konu, Adventure Works temasına genel bakış sağlar ve bunun Microsoft Dynamics 365 Commerce'deki site sayfalarına nasıl uygulanacağını açıklar.
author: anupamar-ms
ms.date: 07/08/2021
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
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7557a36a948de5ae877d74bbbdea78821099b82
ms.sourcegitcommit: 7e976059118938b0089e40bef948029a8c088b38
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2021
ms.locfileid: "6479551"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works temasına genel bakış

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, Adventure Works temasına genel bakış sağlar ve bunun Microsoft Dynamics 365 Commerce'deki site sayfalarına nasıl uygulanacağını açıklar.

Dynamics 365 Commerce'te e-ticaret için Adventure Works adlı bir tema bulunur. Adventure Works teması, spor ve eğlence ürünlerini gösterir ve zengin ve geliştirilmiş bir öykü anlatma deneyimi için optimize edilmiştir. E-ticaret müşterilerine yönelik kapsamlı ve etkileyici bir çevrimiçi alışveriş deneyimi oluşturmak için modern bir görünüm, yeni düzenler ve animasyon efektleri sağlar.

Adventure Works teması aşağıdaki yeni iş akışlarını sağlar:

- Video oynatıcı modülü artık ek öykü anlatımı için başlık, paragraf ve bağlantı işlevlerini desteklemektedir.
- Alışveriş sepetine ekle eylemi, bir bildirim sağlamak yerine mini sepeti çağırır.
- Hızlı bakış modülü, hem masaüstü hem de mobil görüntüleme pencerelerindeki kayan bir bölmedir.
- Boş bir sepette artık promosyonlar gösterilebilir.

Adventure Works teması, Commerce modülü kitaplığında aşağıdaki öykü anlatma modüllerini içerir:

- Kutucuk listesi modülü
- Etkileşimli özellik modülü
- Abone ol modülü
- Etkin görüntü modülü
- Görüntü listesi modülü

Adventure Works teması tamamen duyarlıdır ve masaüstü, mobil ve tablet görüntüleme pencereleri için en iyi duruma getirilmiş bir deneyim sunar.

> [!IMPORTANT]
> Adventure Works teması ve yeni modüller Dynamics 365 Commerce Sürüm 10.0.20 itibarıyla kullanılabilir.

Aşağıdaki şekilde, Adventure Works temasını kullanan bir giriş sayfası örneği gösterilmektedir.

![Adventure Works temasını kullanan bir giriş sayfası örneği](./media/aw_b2c.PNG)

Aşağıdaki şekilde, Adventure Works temasını kullanan bir liste sayfası örneği gösterilmektedir.

![Adventure Works temasını kullanan bir liste sayfası örneği](./media/Aw_list.PNG)

Aşağıdaki şekilde, Adventure Works temasını kullanan bir ürün ayrıntıları sayfası (PDP) örneği gösterilmektedir.

![Adventure Works temasını kullanan bir ürün ayrıntıları sayfası (PDP) örneği](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>B2B siteleri için Adventure Works temasını kullanma

Adventure Works teması, işletmeler arası (B2B) siteler için de bir referans temasıdır. Tüm B2B modülleri ve iş akışları Adventure Works temalarında gösterilir. B2B sitesinin nasıl ayarlanacağı hakkında bilgi için bkz. [B2B sitesi kurulumu](./b2b/set-up-b2b-site.md).

Aşağıdaki şekilde, Adventure Works temasını kullanan bir B2B giriş sayfası örneği gösterilmektedir.

![Adventure Works temasını kullanan bir B2B giriş sayfası örneği](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Tema uzantıları

Adventure Works teması, **Görünüm uzantıları** ve **Modül tanımı** uzantıları gibi çeşitli tema uzantıları içerir. Adventure Works teması benzer uzantıları derlemek için referans teması olarak kullanılabilir. Örneğin, Adventure Works temasıyla ilgili liste sayfası, yatay iyileştiricisi olan bir görünüm uzantısı olarak uygulanır. (Bunun aksine, Fabrikam temasında sol bölme iyileştirici kullanılmıştır.)

Benzer şekilde, diğer modüller modül tanımı uzantılarını içerir. Örneğin, [sepet simgesi modülü](cart-icon-module.md) modül tanım uzantıları kullanılarak uygulanan iki **Boş Sepet** ve **Promosyon İçeriği** yuvası içerir. Ek olarak, mobil görüntüleme pencerelerinde logoyu desteklemek için üst bilgi modülüne yeni bir **Mobil Logo** özelliği eklenmiştir. Bu özellik, üst bilgi modülü tanım uzantısı olarak uygulanır.

Tema uzantıları hakkında daha fazla bilgi için bkz. [Tema uzantıları](e-commerce-extensibility/theme-module-extensions.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Modül kitaplığına genel bakış](starter-kit-overview.md)

[Kutucuk listesi modülü](tile-list-module.md)

[Etkileşimli özellik modülü](interactive-feature-module.md)

[Etkin görüntü modülü](active-image-module.md)

[Abone ol modülü](subscribe-module.md)

[Görüntü listesi modülü](image-list-module.md)

[Tema uzantıları](e-commerce-extensibility/theme-module-extensions.md)

[Sepet simgesi modülü](cart-icon-module.md)

[B2B e-ticaret sitesi kurma](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
