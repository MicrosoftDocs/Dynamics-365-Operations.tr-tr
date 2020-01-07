---
title: Site gezintisini özelleştirme
description: Bu konu, Microsoft Dynamics 365 Commerce sitenizde gezinmek üzere ürünlerinizi düzenlemek için özelleştirilmiş bir çevrimiçi gezinti hiyerarşisinin nasıl oluşturulacağını açıklamaktadır.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e1efb4a7484bd4626886c0f9aa40c3e4dfe304a
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697486"
---
# <a name="customize-site-navigation"></a>Site gezintisini özelleştirme

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce sitenizde gezinmek üzere ürünlerinizi düzenlemek için özelleştirilmiş bir çevrimiçi gezinti hiyerarşisinin nasıl oluşturulacağını açıklamaktadır.

## <a name="overview"></a>Genel Bakış

Çevrimiçi mağazalar, genel olarak ürün kategorilerine giderek gezinerek ürünlere keşif ve göz atma sağlar. Bu özellik genellikle sayfanın üst kısmındaki sekmeler veya soldaki bir gezinti çubuğu ile sağlanır. Dynamics 365 Commerce'te, kategori gezinimin hiyerarşik yapısını ve çeşitli kategorilerde bulunan ürünleri oluşturabilir ve yönetebilirsiniz.

## <a name="create-a-retail-channel-navigation-hierarchy"></a>Perakende kanalı gezinme hiyerarşisi oluştur

Perakende kanalı gezinti hiyerarşisi oluşturmak için aşağıdaki adımları izleyin.

1. **Perakende \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.
1. **Kategori hiyerarşileri** ve ardından **Yeni**yi seçin.
1. Hiyerarşiyi adlandırın.

    > [!NOTE]
    > Oluşturduğunuz en üstteki kategori kök kategori düğümüdür. Sitenizde gösterilmez. Sitenizde tek bir üst düzey düğümün gösterildiği bir kategori hiyerarşisi oluşturmak için, kategoriyi kök kategorinin alt öğesi olarak oluşturun ve adlandırın.

1. **Yeni kategori düğümünü** seçin ve kategoriyi adlandırın.
1. Gereksinim duyduğunuz şekilde kardeş ve alt kategori oluşturmaya devam edin.

Artık, en üst düzey kategori altında oluşturduğunuz her bir kategoriye ürün atayabilirsiniz.

## <a name="customize-the-order-of-categories"></a>Kategorilerin sırasını özelleştirme

Varsayılan olarak tanımladığınız Kategoriler sitenizde alfabetik sırada görüntülenir. Ancak, kategorilerin görüntülenme sırasını da özelleştirebilirsiniz.

## <a name="assign-a-category-hierarchy-type"></a>Kategori hiyerarşisi türü atayın

1. **Perakende \> Ürünler ve kategoriler \> Kategori ve ürün yönetimi**'ne gidin.
1. **Kategori hiyerarşileri** seçin.
1. Ardından Eylem Bölmesinde, **kategori hiyerarşisi** sekmesindeki **Ayar** gurubunda **Hiyerarşi türünü ilişkilendir**'i seçin.
1. **Yeni**'yi seçin.
1. **Kategori hiyerarşisi türü** alanında **Perakende kanalı gezinme hiyerarşisi** seçin.
1. **Kategori hiyerarşisi** alanında, daha önce oluşturduğunuz kanal gezinme hiyerarşisini seçin.

## <a name="publish-new-or-updated-navigation-hierarchies"></a>Yeni veya güncelleştirilmiş gezinti hiyerarşileri Yayımla

Gezinti hiyerarşinizi çevrimiçi mağaza için kullanılabilir hale getirmek için, aşağıdaki adımları izleyin.

1. **Perakende \> Kanal Kurulumu \> Kanal kategorileri ve ürün nitelikleri** seçeneğine gidin.
1. Soldaki ağaçta, çevrimiçi mağazayı seçin.
1. **Kanal güncelleştirmelerini yayınla**'yı seçin.
1. **Perakende \> Perakende BT \> Dağıtım planı öğesine** gidin.
1. Listede, **İş 1040** kodlu bulun ve seçin
1. **Şimdi Çalıştır**'ı seçin.
1. 1070 ve 1150 işleri için 5 ve 6 numaralı adımları yineleyin.

## <a name="show-categories-on-your-site"></a>Sitenizde kategorileri gösterin

Kategori hiyerarşinizi çevrimiçi mağazada göstermek için, şablon veya parçadaki uygun konuma gezinti menüsü modülünü eklemeniz gerekir. Daha sonra gezinti menü modülü, sitenizin bağlı olduğu kanala perakende gezinti hiyerarşinizi yayımladığınızda, gezinti hiyerarşinizi gösterecektir.

> [!NOTE]
> Mağaza başlangıç setinde bulunan gezinti menü modülü, kullanıcıların yalnızca alt kategorileri olmayan kategorilere gitmesine izin verir. Müşterilerinizin alt kategorileri olan kategorilere gidebilmesi gerekiyorsa, gezinti menü modülünü özelleştirmeniz gerekir.

## <a name="add-custom-navigation-options"></a>Özel gezinti seçenekleri ekle

Gezinti menünüze, ürün kategori hiyerarşinizin parçası olmayan gezinme seçenekleri ekleyebilirsiniz. Örneğin, ürün kategorileri listesinin sonunda, siteniz için oluşturduğunuz bir kişi sayfasına işaret eden **bize ulaşın** öğesi ekleyebilirsiniz.

Gezinti menünüze özel gezinti seçenekleri eklemek için aşağıdaki adımları izleyin.

1. Özelleştirmek istediğiniz şablonda veya parçada gezinti menü modülünü seçin.
1. Özellik bölmesinde, **veri** sekmesinde, yeni bir içerik yönetim sistemi (CMS) gezinti öğesi oluşturmak için **Öğe ekle**'yi seçin.
1. Bağlantı metnini ve URL'yi girin.
1. Daha fazla özel gezinti seçeneği eklemek için 2 ve 3. adımları tekrarlayın.
1. Bitirdiğinizde, şablonu veya parçayı kaydedin ve iade edin.

## <a name="additional-resources"></a>Ek kaynaklar

[Şablonlar ve düzenlere genel bakış](templates-layouts-overview.md)

[Şablonlarla çalışma](work-with-templates.md)

[Önceden ayarlanmış düzenlerle çalışma](work-with-layouts.md)

[Parçalarla çalışma](work-with-fragments.md)

[Modüllerle çalışma](work-with-modules.md)

[URL sayfası oluşturma](create-page-url.md)