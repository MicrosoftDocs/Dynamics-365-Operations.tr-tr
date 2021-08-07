---
title: Adventure Works temasına genel bakış
description: Bu konu, Adventure Works temasına genel bakış sağlar ve bunun Microsoft Dynamics 365 Commerce'deki site sayfalarına nasıl uygulanacağını açıklar.
author: anupamar-ms
ms.date: 07/21/2021
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
ms.openlocfilehash: c8183d09e15f83606d84fddd02cb2dfb9b2fb528
ms.sourcegitcommit: 0c77dbb8547cd36fce3977ca9515fa1474efa77a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/22/2021
ms.locfileid: "6655644"
---
# <a name="adventure-works-theme-overview"></a>Adventure Works temasına genel bakış

[!include [banner](includes/banner.md)]

Bu konu, Adventure Works temasına genel bakış sağlar ve bunun Microsoft Dynamics 365 Commerce'deki site sayfalarına nasıl uygulanacağını açıklar.

Dynamics 365 Commerce'te e-ticaret için Adventure Works adlı bir tema bulunur. Adventure Works teması, spor ve eğlence ürünlerini gösterir ve zengin ve geliştirilmiş bir öykü anlatma deneyimi için optimize edilmiştir. E-ticaret müşterilerine yönelik kapsamlı ve etkileyici bir çevrimiçi alışveriş deneyimi oluşturmak için modern bir görünüm, yeni düzenler ve animasyon efektleri sağlar.

## <a name="trial-environments-in-commerce"></a>Commerce'teki deneme ortamları

Adventure Works temasının işletmeden tüketiciye (B2C) ve işletmeden işletmeye (B2B) siteler için dağıtıldığında nasıl göründüğünü görmek için aşağıdaki deneme sitelerini ziyaret edin:

- [Adventure Works B2C sitesi](https://www.adventure-works.com/)
- [Adventure Works B2B sitesi](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Tema özellikleri

Adventure Works teması aşağıdaki yeni özellikleri sunar:

- Video oynatıcı modülü artık ek hikaye anlatımı için başlık, paragraf ve bağlantı işlevselliğini destekler.
- Animasyon aracılığıyla daha iyi içerik geçişleri var.
- "Sepete ekle" eylemi, bildirim sağlamak yerine mini sepeti çağırır.
- Hızlı bakış modülü, hem masaüstü hem de mobil görüntüleme pencerelerindeki kayan bir bölmedir.
- Site sayfaları için yeni düzenler var. 
- Pazarlama içeriği, boş olduklarında sepet ve mini sepet için yapılandırılabilir.
- Mini sepette "50 TL'nin üzerindeki siparişlerde ücretsiz kargo" gibi promosyon mesajları gösterilebilir.
- Açıklama kartları arama ve kategori sayfalarında işlenir.

Adventure Works teması artık Commerce modül kitaplığında aşağıdaki hikaye anlatımı modüllerini içerir:

- [Kutucuk listesi modülü](tile-list-module.md)
- [Etkileşimli özellik modülü](interactive-feature-module.md)
- [Etkin görüntü modülü](active-image-module.md)
- [Abonelik modülü](subscribe-module.md)
- [Görüntü listesi modülü](image-list-module.md)

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

## <a name="install-the-adventure-works-theme"></a>Adventure Works temasını yükleme

Adventure Works temasını yükleme hakkında bilgi için bkz. [Adventure Works temasını yükleme](install-adventure-works.md).

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
