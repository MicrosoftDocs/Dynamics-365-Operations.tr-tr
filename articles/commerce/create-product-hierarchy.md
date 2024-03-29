---
title: Yeni bir ürün hiyerarşisi oluşturma
description: Bu makalede, Microsoft Dynamics 365 Commerce'te yeni ürün hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 54a29381bb9231766d76b653904339d4bd60c257
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270140"
---
# <a name="create-a-new-product-hierarchy"></a>Yeni bir ürün hiyerarşisi oluşturma


[!include [banner](includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce'te yeni ürün hiyerarşisinin nasıl oluşturulacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Dynamics 365 Commerce birden fazla perakende kanalı destekler. Bu perakende kanalları çevrimiçi mağazaları, çağrı merkezlerini ve perakende mağazalarını (tuğla dibek mağazalar olarak da bilinir) içerir. Her perakende mağaza kanalının kendi ödeme türleri, fiyat grupları, satış noktası (POS) kasaları, gelir hesapları ve gider hesapları ve personeli olabilir. Bir perakende mağaza kanalı oluşturabilmeniz için tüm bu öğeleri ayarlamanız gerekir. 

Kuruluşunuzun genel ürün hiyerarşisini tanımlamak için bir Commerce ürün hiyerarşisi kullanılır. Alım satım, fiyatlandırma ve promosyonlar, raporlama ve ürün çeşidi planlaması için bir Commerce ürün hiyerarşisi kullanabilirsiniz. Kuruluş başına yalnızca bir Commerce ürün hiyerarşisi atanabilir.

## <a name="create-and-configure-a-product-hierarchy"></a>Ürün hiyerarşisini oluşturma ve yapılandırma

Bir Commerce ürün hiyerarşisi oluşturmak ve yapılandırmak için bu adımları izleyin.

1. Gezinti bölmesinde, **Modüller \> Retail and commerce \> Ürünler ve kategoriler \> Commerce ürün hiyerarşisi**'ne gidin.
1. Henüz bir hiyerarşi yoksa, hiyerarşinin kökünü oluşturmak için **Eylem bölmesinde** **Yeni**'yi seçin.
1. **Genel** altında:
    1. **Ad** kutusuna bir ad girin.
    1. **Açıklama** kutusuna bir açıklama girin.
    1. **Kolay ad** kutusuna bir kolay ad girin.
    1. **Etkin** ayarını **Evet** yapın.

## <a name="add-hierarchy-nodes"></a>Hiyerarşi düğümleri ekleme

Hiyerarşi düğümleri eklemek için bu adımları izleyin.

1. Eylem bölmesinde **Kategori hiyerarşisini düzenle**'yi seçin.
1. Yeni düğüm eklemek istediğiniz üst düğümü ve ardından **Yeni kategori düğümü**' nü seçin.
1. **Genel** bölümünde bir **Ad**, **Açıklama**, **Kolay ad** ve **Anahtar sözcükler** girin.
1. **Genel** altında:
    1. **Ad** kutusuna bir ad girin.
    1. **Açıklama** kutusuna bir açıklama girin.
    1. **Kolay ad** kutusuna bir kolay ad girin.
    1. **Anahtar sözcükler** kutusuna ilgili anahtar sözcükleri girin.
    1. **Görüntüleme sırası** kutusuna, görüntüleme sırası için bir numara girin (isteğe bağlı).
1. Eylem bölmesinde, **Kaydet**'i seçin.
1. Başka düğümler eklemek için yukarıdaki adımları yineleyin.

Aşağıdaki resimde yeni bir ürün hiyerarşisi düğümünün oluşturulması gösteriliyor.

![Ürün hiyerarşisi oluşturma.](media/create-product-hierarchy.png)

## <a name="other-settings"></a>Diğer ayarlar

Gerektiğinde her bir kategori grubuna kategori öznitelik grupları da atanabilir.  

## <a name="additional-resources"></a>Ek kaynaklar

[Commerce hiyerarşileri](retail-hierarchies.md)

[Ürün kategorilerini ve ürünleri yönetme ](category-management-product-creation.md)

[Ticari varlıkların sıralama düzenini değiştirme](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
