---
title: İndirim yönetimi grupları
description: Bu makalede, indirim yönetimi grupları için veri ayarlama yöntemi açıklanmaktadır. İndirim Yönetimi grupları, indirim hesaplamaları sırasında kullanılabilir ve bir ana kayda bağlanabilir.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2b948e994783d6ec6f00b77d12bd2594a29f6512
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851550"
---
# <a name="rebate-management-groups"></a>İndirim yönetimi grupları

[!include [banner](../includes/banner.md)]

İndirim yönetimi hesaplamaları gruplar ile yapılabilir. İndirim Yönetimi grupları müşteriler, satıcılar ve maddeler için oluşturulabilir. Bunlar bir ana kayda eklenebilir.

## <a name="rebate-management-customer-groups"></a>İndirim yönetimi müşteri grupları

Bir müşteri grubu için hesaplama genellikle, süpermarket zinciri veya franchise şirket gibi bir şirketler zinciri için oluşturulur. Bu hesaplama türü genellikle bir indirim ile ilgilidir.

Bir kesinti genellikle, uygun siparişin kime satıldığını düşünmeden hesaplanır. Ancak, istisnalar vardır. Örneğin, bir lisans sahibi, müşteri grubu A'nın yüzde 4 ancak müşteri grubu B'nin yalnızca yüzde 3 alacağı bir kesinti düzeni oluşturabilir.

### <a name="set-up-customer-groups"></a>Müşteri gruplarını ayarla

İndirim yönetimi müşteri grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Müşteri grupları**'na gidin. Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın. Her grup için aşağıdaki alanları ayarlayın:

- **İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.
- **Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.

### <a name="manage-customer-group-assignments"></a>Müşteri grubu atamalarını Yönetme

Her müşteri bir dizi indirim Yönetimi grubuna ait olabilir. Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya müşteri listesinden başlayabilirsiniz.

Seçili bir grup için müşterileri görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> müşteri grupları**'na gidin.
1. Yönetilecek grubu seçin.
1. Eylem Bölmesinde **Müşteriler** öğesini seçin. **İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan müşterilerin bir listesini gösterir.
1. Gruba yeni müşteri eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin. Ardından yeni satırda aşağıdaki alanı ayarlayın:

    - **Müşteri hesabı**: Müşteri hesap kimliğini seçin.

1. Bir müşteriyi gruptan kaldırmak için, müşteriyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.

Seçili bir müşteri için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.

1. **Alacak hesapları \> Müşteriler \> Tüm müşteriler**'e gidin.
1. Çalışmak istediğiniz müşteriyi seçin.
1. Eylem Bölmesi'nde, **Müşteri** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin. **İndirim Yönetimi grupları** sayfası görüntülenir ve seçili müşterinin zaten üyesi olduğu bir grup listesini gösterir.
1. Müşteriyi yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin. Ardından yeni satırda aşağıdaki alanı ayarlayın:

    - **İndirim yönetimi grubu**: Müşterinin ekleneceği grubu seçin.

1. Bir müşteriyi gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.

## <a name="rebate-management-vendor-groups"></a>İndirim yönetimi satıcı grupları

Bir grup satıcı için hesaplama genellikle bir grup teslimat noktası için oluşturulur. Bu hesaplama türü genellikle bir indirim ile ilgilidir.

### <a name="set-up-vendor-groups"></a>Satıcı gruplarını ayarlama

İndirim yönetimi satıcı grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Satıcı grupları**'na gidin. Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın. Her grup için aşağıdaki alanları ayarlayın:

- **İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.
- **Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.

### <a name="manage-vendor-group-assignments"></a>Satıcı grubu atamalarını Yönetme

Her satıcı bir dizi indirim Yönetimi grubuna ait olabilir. Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya satıcı listesinden başlayabilirsiniz.

Seçili bir grup için satıcıları görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> satıcı grupları**'na gidin.
1. Yönetilecek grubu seçin.
1. Eylem Bölmesinde, **Satıcılar**'ı seçin. **İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan satıcıların bir listesini gösterir.
1. Yeni bir satıcıyı gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin. Ardından yeni satırda aşağıdaki alanı ayarlayın:

    - **satıcı hesabı**: satıcı hesap kimliğini seçin.

1. Bir satıcıyı gruptan kaldırmak için, satıcıyı seçin ve sonra Eylem bölmesinde **Sil**'i seçin.

Seçili bir satıcı için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.

1. **Borç hesapları \> Satıcılar \> Tüm satıcılar**'a gidin.
1. Çalışmak istediğiniz satıcıyı seçin.
1. Eylem Bölmesi'nde, **satıcı** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin. **İndirim Yönetimi grupları** sayfası görüntülenir ve seçili satıcının zaten üyesi olduğu bir grup listesini gösterir.
1. Satıcıyı yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin. Ardından yeni satırda aşağıdaki alanı ayarlayın:

    - **İndirim yönetimi grubu**: Satıcının ekleneceği grubu seçin.

1. Bir satıcıyı gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.

## <a name="item-rebate-groups"></a>Madde indirim grupları

Öğeleri gruplandırarak, indirimler ve kesintiler hesaplanırken daha fazla esnekliğe sahip olursunuz. Bu yaklaşım genellikle müşteriler ve satıcılar için indirimleri ve kesintileri ayarlamak için daha etkili bir yoldur.

### <a name="set-up-item-groups"></a>Madde gruplarını ayarla

İndirim yönetimi madde grubu ile çalışmak için, **indirim Yönetimi \> İndirim yönetim grupları kurulumu \> Madde grupları**'na gidin. Gereken şekilde grupları eklemek ve kaldırmak için eylem bölmesindeki düğmeleri kullanın. Her grup için aşağıdaki alanları ayarlayın:

- **İndirim yönetimi grubu**: Grup için benzersiz bir ad girin.
- **Açıklama**: Nasıl kullanılması gerektiği hakkında daha fazla bilgi sağlayan grup açıklamasını girin.

### <a name="manage-item-group-assignments"></a>Madde grubu atamalarını Yönetme

Her madde bir dizi indirim Yönetimi grubuna ait olabilir. Grup üyelerini görüntülemek ve atamak için, Grup listesinden veya madde listesinden başlayabilirsiniz. Ayrıca kategori hiyerarşinize göre de madde ekleyebilirsiniz.

Seçili bir grup için maddeleri görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> Madde grupları**'na gidin.
1. Yönetilecek grubu seçin.
1. Eylem Bölmesinde, **Maddeler**'i seçin. **İndirim Yönetimi grupları** sayfası görüntülenir ve zaten seçili grubun üyesi olan maddelerin bir listesini gösterir.
1. Yeni bir maddeyi gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin. Ardından yeni satırda aşağıdaki alanı ayarlayın:

    - **Madde hesabı**: Madde hesap kimliğini seçin.

1. Bir maddeyi gruptan kaldırmak için, maddeyi seçin ve sonra Eylem bölmesinde **Sil**'i seçin.

Seçili bir madde için grup atamalarını görüntülemek, eklemek veya kaldırmak için aşağıdaki adımları izleyin.

1. **Ürün bilgi yönetimi \> Ürünler \> Serbest bırakılmış ürünler**'e gidin.
1. Çalışmak istediğiniz maddeyi seçin.
1. Eylem Bölmesi'nde, **Ürün** sekmesindeki **İndirim yönetimi** grubunda **İndirim yönetimi grupları**'nı seçin. **İndirim Yönetimi grupları** sayfası görüntülenir ve seçili maddenin zaten üyesi olduğu bir grup listesini gösterir.
1. Maddeyi yeni bir gruba eklemek için Eylem Bölmesinde **Yeni**'yi seçin ve ızgaraya bir satır ekleyin. Ardından yeni satırda aşağıdaki alanı ayarlayın:

    - **İndirim yönetimi grubu**: Maddenin ekleneceği grubu seçin.

1. Bir maddeyi gruptan kaldırmak için, grubu seçin ve sonra Eylem bölmesinde **Sil**'i seçin.

Kategori hiyerarşinize dayalı olarak bir gruba madde eklemek için, aşağıdaki adımları izleyin.

1. **İndirim yönetimi \> indirim Yönetimi grupları kurulumu \> Madde grupları**'na gidin.
1. Yönetilecek grubu seçin.
1. Eylem Bölmesinde, **Madde ekle**'yi seçin.
1. **Madde Ekle** iletişim kutusunda, **Kategori hiyerarşisi** alanında, üst düzey bir kategori seçin.
1. Madde hiyerarşisi sol bölmede açılır. Aradığınız hiyerarşi düzeyini seçin. 
1. Seçili hiyerarşi ve hiyerarşi düzeyindeki maddeler şimdi sağ bölmede listelenir. Bölmeyle çalışmak için aşağıdaki adımları izleyin:

    - Eklemek istediğiniz her madde için onay kutusunu işaretleyin.
    - Listelenen tüm maddeleri seçmek için kılavuz üstbilgisindeki onay kutusunu seçin.
    - Kılavuza yalnızca şimdiye kadar seçtiğiniz öğeleri gösterecek şekilde filtre uygulamak için **Seçileni göster** düğmesini seçin. Tam listeye dönmek için düğmeyi tekrar seçin.

1. Madde seçiminizi seçili gruba uygulamak için **Tamam**'ı seçin.
