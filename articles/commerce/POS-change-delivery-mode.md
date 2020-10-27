---
title: POS'ta teslimat şeklini değiştirme
description: Bu konu, POS'ta teslimat işlemi değişiklik modunun nasıl yapılandırıldığını ve kullanıldığını açıklamaktadır.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 1e9f8d202fa81546a9f84af62824e6d8f620cf35
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975109"
---
# <a name="change-mode-of-delivery-in-pos"></a>POS'ta teslimat şeklini değiştirme

[!include [banner](includes/banner.md)]

Bu konu, satış noktası (POS) ortamında "teslimat şeklini değiştir" işlevinin nasıl ayarlanacağını ve kullanılacağını açıklamaktadır. 

Dynamics 365 Commerce 10.0.10 ve sonraki sürümlerinde, **Teslimat şeklini değiştir** işlemi (647) POS ekran düzenlerinize eklenmek üzere sunulur.

Teslimat şeklini değiştir özelliği, POS hareketinde bir veya daha fazla sevkiyat yapılandırılmış satış satırı için teslimat şeklini değiştirme seçeneği sunar. Önceki Commerce sürümlerinde, sevkiyat için yapılandırılmış mevcut bir satırda teslimat şeklini değiştirmek istediğinizde, tam **Tümünü sevk et** veya **Seçileni sevk et** yapılandırma akışlarından geçmeniz gerekirdi. Bu işlem zaman alıyordu ve satır için teslimat kaynağında veya teslimat tarihlerinde yanlışlıkla değişikliklere neden olabiliyordu. Yeni işlev, bu satış satırlarındaki teslimat şeklini etkili şekilde güncelleştirmek için alternatif bir yöntem sağlar.

POS düğme kılavuzundaki bir düğmeye işlem ekleme hakkında daha fazla bilgi için bkz. [Satış noktası için ekran düzenleri](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).

Bu özellik POS'ta yapılandırıldıktan sonra,**Teslimat şeklini değiştir**'i seçtiğinizde, teslimat şeklini değiştirmek istediğiniz hareketin satırlarını seçmenize olanak sağlayan bir liste sayfası görüntülenir. Satırların bazılarını veya tümünü seçebilir veya herhangi bir değişiklik yapmadan çıkabilirsiniz. Daha önce sevkiyat için yapılandırılmış olan satış satırları, listede değiştirebileceğiniz tek satırlardır. Malzeme çekme veya teslim alma için belirlenmiş bir satırı sevk edilmek üzere değiştirmek istiyorsanız, **Tümünü sevk et** veya **Seçileni sevk et** işlemlerini kullanmanız gerekir. Buna karşılık, sevkiyat olarak belirlenmiş bir satırı malzeme çekme veya teslim alma olarak değiştirmek istiyorsanız **Tümünü çek**, **Seçileni çek**, **Tümünü teslim al** veya **Seçileni teslim al** işlemlerini kullanmanız gerekir.

Değiştirmek istediğiniz satırları seçtikten sonra, teslimat şekli seçeneklerini belirlemek için **Teslimat şeklini değiştir**'e tıklayın. Değiştirilecek birden fazla satır seçtiyseniz, POS yalnızca tüm seçili ürünler için izin verilebilir olarak yapılandırılmış teslimat şekillerini görüntüler. Teslimat şekilleri belirli ürünleri ve teslimat adreslerini destekleyecek şekilde yapılandırılabilir. Bir ürün ve adres birleşimi için kabul edilebilir ancak başka bir seçilen ürün ve adres birleşimi için kabul edilebilir olmayan bir teslimat şekli varsa, teslimat şekli kullanılamaz. Bir ürün tarafından desteklenmeyen bir teslimat şeklini başka bir ürünün teslimat şekli olarak seçmek istiyorsanız, satırları tek tek seçmeniz ve teslimat şeklini her bir satır için ayrı olarak değiştirmeniz gerekebilir.  

Yeni teslimat şeklini seçtikten sonra hareket sayfası görüntülenir. Yeni teslimat şekli seçimlerinizi gözden geçirmek için hareket listesinde **Teslimat** sekmesini seçin.   
