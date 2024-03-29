---
title: Satış noktasında teslimat şeklini değiştirme
description: Bu makale, POS'ta teslimat işlemi değişiklik modunun nasıl yapılandırıldığını ve kullanıldığını açıklamaktadır.
author: hhainesms
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 583f568164d0de70e22998bf5ded5f4616b00bd2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855833"
---
# <a name="change-mode-of-delivery-in-pos"></a>Satış noktasında teslimat şeklini değiştirme

[!include [banner](includes/banner.md)]

Bu makale, satış noktası (POS) ortamında "teslimat şeklini değiştir" işlevinin nasıl ayarlanacağını ve kullanılacağını açıklamaktadır. 

Dynamics 365 Commerce 10.0.10 ve sonraki sürümlerinde, **Teslimat şeklini değiştir** işlemi (647) POS ekran düzenlerinize eklenmek üzere sunulur.

Teslimat şeklini değiştir özelliği, POS hareketinde bir veya daha fazla sevkiyat yapılandırılmış satış satırı için teslimat şeklini değiştirme seçeneği sunar. Önceki Commerce sürümlerinde, sevkiyat için yapılandırılmış mevcut bir satırda teslimat şeklini değiştirmek istediğinizde, tam **Tümünü sevk et** veya **Seçileni sevk et** yapılandırma akışlarından geçmeniz gerekirdi. Bu işlem zaman alıyordu ve satır için teslimat kaynağında veya teslimat tarihlerinde yanlışlıkla değişikliklere neden olabiliyordu. Yeni işlev, bu satış satırlarındaki teslimat şeklini etkili şekilde güncelleştirmek için alternatif bir yöntem sağlar.

POS düğme kılavuzundaki bir düğmeye işlem ekleme hakkında daha fazla bilgi için bkz. [Satış noktası için ekran düzenleri](pos-screen-layouts.md).

Bu özellik POS'ta yapılandırıldıktan sonra,**Teslimat şeklini değiştir**'i seçtiğinizde, teslimat şeklini değiştirmek istediğiniz hareketin satırlarını seçmenize olanak sağlayan bir liste sayfası görüntülenir. Satırların bazılarını veya tümünü seçebilir veya herhangi bir değişiklik yapmadan çıkabilirsiniz. Daha önce sevkiyat için yapılandırılmış olan satış satırları, listede değiştirebileceğiniz tek satırlardır. Malzeme çekme veya teslim alma için belirlenmiş bir satırı sevk edilmek üzere değiştirmek istiyorsanız, **Tümünü sevk et** veya **Seçileni sevk et** işlemlerini kullanmanız gerekir. Buna karşılık, sevkiyat olarak belirlenmiş bir satırı malzeme çekme veya teslim alma olarak değiştirmek istiyorsanız **Tümünü çek**, **Seçileni çek**, **Tümünü teslim al** veya **Seçileni teslim al** işlemlerini kullanmanız gerekir.

Değiştirmek istediğiniz satırları seçtikten sonra, teslimat şekli seçeneklerini belirlemek için **Teslimat şeklini değiştir**'e tıklayın. Değiştirilecek birden fazla satır seçtiyseniz, POS yalnızca tüm seçili ürünler için izin verilebilir olarak yapılandırılmış teslimat şekillerini görüntüler. Teslimat şekilleri belirli ürünleri ve teslimat adreslerini destekleyecek şekilde yapılandırılabilir. Bir ürün ve adres birleşimi için kabul edilebilir ancak başka bir seçilen ürün ve adres birleşimi için kabul edilebilir olmayan bir teslimat şekli varsa, teslimat şekli kullanılamaz. Bir ürün tarafından desteklenmeyen bir teslimat şeklini başka bir ürünün teslimat şekli olarak seçmek istiyorsanız, satırları tek tek seçmeniz ve teslimat şeklini her bir satır için ayrı olarak değiştirmeniz gerekebilir.  

Yeni teslimat şeklini seçtikten sonra hareket sayfası görüntülenir. Yeni teslimat şekli seçimlerinizi gözden geçirmek için hareket listesinde **Teslimat** sekmesini seçin.

## <a name="additional-resources"></a>Ek kaynaklar

[Çağrı merkezi siparişleri oluşturma](tasks/create-call-center-orders.md)

[Teslimat şekline göre işlem tabanlı e-postaları özelleştirme](customize-email-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]