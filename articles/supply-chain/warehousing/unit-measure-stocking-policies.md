---
title: Ölçü birimi ve stoklama politikaları
description: Bu makalede depo süreçlerinde varsayılan ünitelerin, ünite sıralarının ve ünite çevrimlerinin nasıl kullanıldığı açıklanmıştır.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetails, EcoResProductDetailsExtended, EcoResStorageDimensionGroup, InventItemOrderSetup, UnitOfMeasureConversion, WHSRFMenuItem, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 29611
ms.assetid: 4b5ca875-9a06-416d-9ac0-cc3ab8f7338e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bd6a3ea9d7b339df99ffa65f058fc4b98b58b9c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439589"
---
# <a name="unit-of-measure-and-stocking-policies"></a>Ölçü birimi ve stoklama politikaları

[!include [banner](../includes/banner.md)]

Bu makalede depo süreçlerinde varsayılan ünitelerin, ünite sıralarının ve ünite çevrimlerinin nasıl kullanıldığı açıklanmıştır.

Birim sıra grupları, ambar operasyonlarında kullanılabilecek birimlerin sırasını tanımlar. Bunlar **Birim sıra grupları** sayfasında oluşturulur. Sıra çeşitli birimlerin ilişkisini gösterir. Örneğin, maddelerin ayrı ayrı parçalarını içeren kutular içeren paletler depolarsınız. Bu durumda, üç farklı birim ve mantıksal katmanların sırası sağlamanız gerekir. Birim sıra grupları, plakaları gruplamak için politikalar ve çeşitli ambar süreçleri için kullanılması gereken varsayılan birimler tanımlamanıza imkan verir. Bu makale, hem Ambar yönetiminde sunulan gelişmiş ambar çözümleri için hem de Stok yönetiminde sunulan daha temel ambar çözümleri için geçerlidir.

## <a name="unit-sequence-groups-for-released-products"></a>Serbest bırakılan ürünler için birim sıra grupları
Serbest bırakılan ürünleri ambar iş süreçlerinde kullanmaz istiyorsanız, bunlara bir birim sıra grubu atanmalıdır. Depolama boyutu grubu ile ilişkilendirilmiş bir ürünü doğrulamak istiyorsanız ve Depolama boyutu grubu için **Ambar yönetimi süreçlerini kullan** seçeneği **Evet** olarak ayarlıysa, ürüne bir birim sıra grubu kodu tanımlı değilse bir hata iletisi alırsınız. Kullandığınız birim sıra grubu birden fazla satır (ve dolayısıyla birden fazla birim) içeriyorsa birimler arasında bir birim dönüştürmesi ayarlamanız gerekir. Bu kurulumu **Birim dönüştürmeleri** sayfasında tamamlarsınız. Serbest bırakılan ürünle ilişkilendirdiğiniz bir sıra grubundaki en küçük birim, karşılık gelen ürün için tanımlanan stok birimi ile eşleşmelidir. Stok birimi, eldeki stokun hesaplanmasında temel alınan birimdir. Aynı zamanda, **Ölçü birimi dönüştürmelerini etkinleştir** seçeneğini kullanarak ana ürünlerin ürün varyantları için ölçü birimi dönüştürmeleri de ayarlayabilirsiniz.

## <a name="license-plate-grouping"></a>Plaka gruplandırma
Belirli bir birimden azının veya fazlasının tek bir plakada gruplanması gerekip gerekmediğini veya her bir ürün için bir plakaya bölünmesi gerekip gerekmediğini belirtebilirsiniz. Bu davranışı ayarlamak için, **Birim sıra grupları** sayfasının **Satır ayrıntıları** sekmesindeki **Plaka gruplaması** seçeneğini kullanın. İşi bir mobil cihaz kullanarak işlerken plaka gruplandırmasını kullanmak istediğinizde, **Mobil cihaz** menü öğesinde **Plaka gruplandırması** seçeneği seçilmiş olmalıdır. Örneğin, iki satır içeren bir birim sıra grubu ile ilişkilendirilmiş bir maddeyi kaydetmek için bir mobil cihaz kullanıyorsanız. İlk satır Parçalar içindir ve **Plaka gruplandırması** seçeneği **Evet** olarak ayarlıdır. İkinci satır Palet birimi içindir ve **Plaka gruplandırması** seçeneği **Hayır** olarak ayarlıdır. Bu durumda sistem plakaların bölünmesini ve 100 parça başına oluşturulmasını otomatik olarak yönlendirebilir.

## <a name="units-for-cycle-counting"></a>Döngü sayımı birimleri
Döngü sayımı süreçlerinin parçası olarak hangi birimlerin kullanılması gerektiğini tanımlamak için **Birim sıra grupları** sayfasındaki **Döngü sayımı birimini kullan** seçeneğini seçin. Sıra grubunda maksimum dört birim seçebilirsiniz. Dörtten fazla birim seçerseniz, ek birimler mobil cihazda gösterilmez.

## <a name="default-units-for-mobile-device-receiving-processes"></a>Mobil cihaz alma işlemleri için varsayılan birimler
Mobil cihazların alma işlemlerinde kullanılması gereken varsayılan birimleri ayarlamak için, **Birim sıra grupları** sayfasında **Satınalma ve transfer için varsayılan birim** ve **Üretim için varsayılan birim** seçeneklerini etkinleştirin. Örneğin, varsayılan olarak, satınalma emri eldeki stok bir mobil cihaz kullanılarak alındığında sistem Palet miktarlarını kullanacak ama stokta tutma birimi Parçalar olacak şekilde belirleyebilirsiniz. Her bir paletin içerdiği parça sayısına dönük dönüştürme almak için, 100 Parça = 1 PL gibi bir birim dönüştürücü tanımlamanız gerekir.

## <a name="default-order-settings"></a>Varsayılan sipariş ayarları
Serbest bırakılan ürünlerin oluşturulmasının parçası olarak, satınalmalar, satışlar ve stok için çeşitli emirleri işleyecek varsayılan birimler seçebilirsiniz. **Varsayılan sipariş ayarları** ve **Tesise özel sipariş ayarları** sayfalarını kullanarak, çeşitli kaynak belgeler için varsayılan birimler ve miktarlar ayarlayabilirsiniz. Bu sayfalara **Serbest bırakılan ürünler** sayfasından erişebilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]