---
title: Ürün sahipleri
description: Bu konuda ürün sahipleri hakkında bilgiler sağlanmaktadır. Ürün sahibi, belirli ürünlerden sorumlu kullanıcılardan oluşan bir gruptur. Yalnızca grubun üyeleri bu ürünleri serbest bırakabilir. Ürün sahibi ayrıca onay iş akışında da kullanılabilir.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 90f5596f9b5fc45e78cc49a3309c45864e07e70b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967345"
---
# <a name="product-owners"></a>Ürün sahipleri

[!include [banner](../includes/banner.md)]

Ürün sahibi, belirli ürünlerden sorumlu kullanıcılardan oluşan bir gruptur. Bir ürün sahibi grubu bir ürüne atandığında, yalnızca bu grubun üyeleri ürünü serbest bırakabilir. Ürün sahibi mühendislik değişikliği yönetiminde onay iş akışında da kullanılabilir.

Ürün sahipleri genel ayarlardır. Bu nedenle, tüm tüzel kişilikler için kullanılabilirdir.

## <a name="create-a-product-owner-group"></a>Ürün sahibi grubu oluşturma

Bir ürün sahibi grubu oluşturmak ve bu gruba üye eklemek için aşağıdaki adımları izleyin.

1. **Mühendislik değişikliği yönetimi \> Kurulum \> Ürün sahipleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Ürün sahibi** alanına, ürün grubu için açıklayıcı bir ad girin.
4. **Ad** alanına grubun kısa bir açıklamasını yazın.
5. **Üyeler** hızlı sekmesinde, grubun üyesi olması gereken çalışanları ekleyin.

## <a name="assign-a-product-owner-to-a-product"></a>Bir ürüne ürün sahibi atama

Bir ürüne ürün sahibi atamak için aşağıdaki adımları izleyin.

1. İlgili ürün veya ana ürünün **Ürün ayrıntıları** sayfasını açın.
1. **Genel** hızlı sekmesinde, **Ürün sahibi** alanını ilgili ürün sahibi grubunun adına ayarlayın.

Ürün sahibi bir ürüne atandığında, yalnızca ürün sahibi grubunun üyeleri **ürün sahibi** ayarını düzenleyebilir.

Ürün sahibi **Serbest bırakılan ürünler** sayfasında da görünür.

## <a name="product-owners-and-product-releases"></a>Ürün sahipleri ve ürün serbest bırakmaları

Yalnızca bir ürünün ürün sahibi grubundaki kullanıcılar söz konusu ürünü serbest bırakabilir. Ancak, ürün bir alt öğe olduğunda ve üst öğesi üst öğenin sahibi tarafından serbest bırakıldığında bir özel durum vardır. Başka bir deyişle, ürün başka bir ürünün ürün reçetesinin parçasıysa, sistem ürün reçetesindeki her maddenin ürün sahibini denetlemez. Yalnızca ana maddenin ürün sahibini denetler.

Örneğin, X ürünü *Tasarım dolapları* ürün sahibi grubuna atanır. X ürünü, *Tasarım Hoparlörleri* ürün sahibi grubuna atanmış, Y ürününün ürün reçetesinin de bir parçasıdır. *Tasarım Hoparlörleri* ürün sahibi grubundaki bir kullanıcı, Y ürününü ve ürün reçetesini serbest bıraktığında, X ürünü, Y ürünü ile birlikte serbest bırakılacaktır.

## <a name="product-owners-and-approvals"></a>Ürün sahipleri ve onaylar

Ürün sahipleri belirli mühendislik değişikliklerinin ürünleri için faydalı olup olmadığını bildiğinden, bunları mühendislik değişikliği yönetimi içindeki onay sürecinin bir parçası olarak eklemek mantıklı olur. Bu yaklaşımı, mühendislik değişikliği yönetimi için kullanılan iş akışlarında katılımcı sağlayıcılar olarak ürün sahiplerini ayarlayarak uygulayabilirsiniz. Sistem daha sonra, mühendislik değişikliği istekleri ve mühendislik değişikliği emirlerindeki ürünlere göre iş akışlarında onay görevleri atayacaktır. Daha fazla bilgi için bkz. [Mühendislik ürünlerindeki değişiklikleri yönetme](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]