---
title: Müşteri portalını yükleme, kurma ve güncelleme
description: Bu makale, Müşteri portalı için lisans ayrıntılarını ve kurulum yönergelerini sağlar.
author: Henrikan
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8344212e66cb57ea8c9d4e8c2cdfbf022bc199c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850597"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Müşteri portalını yükleme, kurma ve güncelleştirme

[!include [banner](../includes/banner.md)]


## <a name="licensing-requirements"></a>Lisanslama gereksinimleri

Müşteri portalını uygulamak için aşağıdaki lisanslara sahip olmanız gerekir:

- **Power Apps portallar** – Bu lisansın müşteri portalını barındırması gereklidir. Portallar kullanıma göre lisanslıdır. Daha fazla bilgi için, [Power Apps Portal lisans gereksinimlerine](/power-platform/admin/powerapps-flow-licensing-faq#portals) bakın.
- **Çift yazma**: Supply Chain Management tablolarında çift yazma özelliğini etkinleştirmek için gerekli lisanslara sahip olmanız gerekir. Daha fazla bilgi için bkz: [çift yazma için sistem gereksinimleri.](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md)

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Çift yazma ve Power Apps portallarda bağımlılıklar

Müşteri Portalı, Aşağıdaki çizimde gösterildiği gibi Power Apps portallara ve çift yazmaya bağlıdır.

![Müşteri portalı bağımlılıkları.](media/customer-portal-elements.png "Müşteri portalına bağımlılıklar")

Supply Chain Management'tan alınan diğer özelliklerden farklı olarak, Müşteri Portalı şablonu Power Apps portalları içinde bulunur. Bu nedenle, Müşteri portalı çift yazmadaki Power Apps portalları ve tabloları tarafından sağlanan işlevler ve özelliklerle sınırlıdır.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Müşteri portalını etkinleştirmek için gerekli kurulum

Gerekli lisanslara sahip olduğunuzdan emin olduktan sonra, [Çift-yazılabilir başlangıç eşitleme yönergelerinde](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-entity-map.md) açıklandığı gibi çift-yazılabilir ayarlayabilirsiniz.

Çift yazmada aşağıdaki tablo eşlemelerini etkinleştirdiğinizden emin olun:

- Satış siparişi başlığı
- Satış siparişi ayrıntıları
- Hesaplar
- İlgili kişiler
- Ürünler

Bu kurulum tamamlandıktan sonra, müşteri portalı şablonunu temin edebilirsiniz.

## <a name="provision-the-customer-portal"></a>Müşteri Portalı Hazırlama

Başlamadan önce [gerekli kurulumu](#required-setup) tamamlamış olduğunuzdan emin olun. Müşteri portalını sağlamak için aşağıdaki adımları izleyin.

1. [make.powerapps.com](https://make.powerapps.com/) gidin.
2. Çift-yazmayı etkinleştirdiğiniz ortamı kullandığınızdan emin olun.
3. **Oluştur** sekmesinde, **şablondan başlangıç şablonu** bölümüne gidin ve **Müşteri Portalı** olarak adlandırılan şablonu seçin.
4. Ekrandaki yönergeleri izleyin.

Sağlama tamamlandıktan sonra, **giriş** sayfasının **uygulamalarınız** bölümünde müşteri portalına erişebilirsiniz.

> [!NOTE]
> Çift-yazılır çözüm, üzerinde çalışmakta olduğunuz ortamda kurulu değilse bir hata iletisi alırsınız ve müşteri portalı sağlanmayacaktır.

## <a name="update-the-customer-portal"></a>Müşteri Portalı güncelleme

Daha sonra müşteri portalına daha fazla işlevsellik eklenebilir. Microsoft'un alttaki çözüm bileşenlerine yaptığı değişiklikler sizin ortamınızda otomatik olarak görüntülenir. Ancak, ortamınızda sağlanan Web sitesi, yapılandırma verilerinde yapılan değişiklikleri otomatik olarak yansıtmayacaktır. Yeni şablondan kodu alarak ve bunu sağlanan Web sitesiyle birleştirerek bu değişiklikleri el ile uygulamanız gerekir.

## <a name="additional-resources"></a>Ek kaynaklar

Müşteri portalını nasıl ayarlayabileceğinizi ve özelleştirebileceğinizi öğrenmek için, temeldeki teknolojiler için aşağıdaki belgeleri gözden geçirerek başlamanız gerekir:

- [Power Apps portal belgeleri](/powerapps/maker/portals/overview)
- [Çift yazma belgeleri](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Portallarınızı etkili şekilde yönetmek için Power Apps portalları ve Microsoft Dataverse yaşam döngüsünü anlamanız gerekir. Daha fazla bilgi edinmek için aşağıdaki kaynaklara bakın:

- [Portal yaşam döngüsü hakkında](/powerapps/maker/portals/admin/portal-lifecycle)
- [Bir portalı yükselt](/powerapps/maker/portals/admin/upgrade-portal)
- [Portal konfigürasyonu geçir](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Çözüm yaşam döngüsü yönetimi: Customer Engagement için Dynamics 365 uygulamaları](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]