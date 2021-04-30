---
title: Kıymet kiralama kuralları
description: Bu konuda kiralanan kıymetlere yönelik kurallar anlatılmıştır.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881820"
---
# <a name="asset-leasing-conventions"></a>Kıymet kiralama kuralları

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Bu konuda kiralanan kıymetlere yönelik kurallar anlatılmıştır. Kiralama sözleşmeleri, bir kiralama defterinin başlangıç tarihini belirlemek için kullanılır. Kiralama kuralı **Yok** olarak ayarlanırsa, başlangıç tarihi kiralamanın başlangıç tarihiyle (diğer bir deyişle, **Kiralama başlangıç tarihi** alanının değeri) aynıdır. Kiralama sözleşmesi **Tam ay** olarak ayarlanırsa, başlangıç tarihi, kiralamanın başlangıç tarihinin bulunduğu ayın ilk günüdür.

Başlangıç tarihi, borç amortismanı ve kıymet amortisman çizelgeleri için dönemin başlangıç tarihini belirler. Faiz giderleri ve amortisman giderleri, ilgili çizelgelerin dönem bitiş tarihinde deftere nakledilir. İlk denklik ve ayarlama günlüğü girişi, başlangıç tarihinde deftere nakledilir.

> [!NOTE]
> Kiralama kuralları özelliği, Özellik Yönetimi aracılığıyla açılmalıdır. **Özellik yönetimi** çalışma alanında, **Varlık kiralama için kiralama kuralı** özelliği olarak adlandırılan özelliği bulup seçin ve **Şimdi etkinleştir**'i seçin.

Kiralama kuralları, kiralama varlığı defterinin kurulumuna atanır.

Kiralama sözleşmesini görüntülemek veya atamak için şu adımları izleyin.

1. **Varlık kiralama \> Kurulum \> Kiralama defterleri**'ne gidin.
2. **Kiralama kuraı** alanında, aşağıdaki değerlerden birini seçin.

    | Kiralama kuralı | Tanım |
    |--------------------|-------------|
    | Hiçbiri               | Borç amortismanı ve varlık amortisman çizelgeleri kiralamanın başlangıç tarihinde başlar çünkü başlangıç tarihi kiralamanın başlangıç tarihine eşittir. Bitiş tarihi bir ay sonrasıdır. Bu kiralama kuralı, faizin her ayın son günü deftere nakledileceğini garanti etmez. |
    | Tam ay         | Ay içinde herhangi bir zamanda gerçekleşen bir başlangıç tarihi olan kiralamalar için, borç amortismanı ve varlık amortismanı çizelgeleri o ayın ilk gününde gider tahakkuk etmeye başlar. Bu kiralama kuralı, faizin tüm ay boyunca her ayın son gününde tahakkuk ettirilmesini sağlar. |

3. **Kaydet**'i seçin.

Bir kiralama oluşturulduğunda, her defterin başlangıç tarihi, kiralama için girilen başlangıç tarihine ve defter için belirtilen kiralama kuralına göre otomatik olarak girilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
