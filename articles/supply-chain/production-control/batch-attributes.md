---
title: Toplu iş öznitelikleri
description: Bu makalede toplu iş öznitelikleri hakkında bilgiler verilmiştir. Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir. Bu makalede ayrıca toplu iş özniteliklerinin nasıl atanacağı ve toplu işleri rezerve ettiğinizde bunları nasıl arayacağınız açıklanmaktadır.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup, WHSBatchAttribReserve
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e5f5a03df63cf4fa90b5e9e67082a0d60eef9afc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899396"
---
# <a name="batch-attributes"></a>Toplu iş öznitelikleri

[!include [banner](../includes/banner.md)]

Bu makalede toplu iş öznitelikleri hakkında bilgiler verilmiştir. Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir. Bu makalede ayrıca toplu iş özniteliklerinin nasıl atanacağı ve toplu işleri rezerve ettiğinizde bunları nasıl arayacağınız açıklanmaktadır.

Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir. Toplu iş öznitelikleri, ortam koşulları veya toplu işi oluşturmak için kullanılan hammaddelerin kalitesi ya da bitmiş ürünün sonucu gibi çeşitli etkenlere bağlı olarak değişiklik gösterebilir. Kullanılan toplu iş özniteliklerinin sayısı ve tipleri, endüstriler arasında büyük değişiklikler gösterebilir. Toplu iş özniteliklerinin nasıl kullanıldığını gösteren iki örnek aşağıda verilmiştir:

-   Peynir endüstrisinde, peynir üretmekte kullanılan hammaddelerden biri olan süt, yağ içeriği ve yüzde ağırlık gibi özniteliklere sahip olabilir. Sütten üretilen peynirin nem ve yaş gibi başka öznitelikleri olabilir.
-   Çelik endüstrisinde, ürettiğiniz demir magnezyum, gümüş ve çinko içeriği yüzdeleri gibi özniteliklere sahip olabilir.

Öznitelik sayısını ve türünü daha iyi yönetmek için, toplu iş öznitelik grupları kullanabilirsiniz. Bu şekilde, her bir özniteliği tek tek eklemeniz gerekmez.

## <a name="assign-batch-attributes"></a>Toplu iş öznitelikleri atama
Toplu iş özniteliklerini, stok toplu işlerinde tutulan ürünlere tek tek atayabilir veya bunları belirli müşterilerle ilişkili ürünlere atarsınız. Müşteri düzeyinde bir toplu iş özniteliği atamadan önce, ürün düzeyinde atamanız gerekir. Ürünün toplu iş boyutu izleme boyut grubunda **Etkin** olarak ayarlanmış olmalıdır. Ayrı bir ürüne bir toplu iş özniteliği atamak için, ürüne özel sayfayı kullanın. Öznitelik, bir müşteriye yönelik bir ürüne özelse, müşteriye özel sayfayı kullanın. Bir ürüne öznitelik eklediğinizde, diğer parametreleri de tanımlarsınız. Burada bazı örnekler verilmiştir:

-   **Tamsayı** veya **Kesir** türünün özniteliği için minimum veya maksimum aralıklar.
-   **Tamsayı** veya **Kesir** türündeki bir öznitelik için tolerans eylemleri. Özniteliğin değeri minimum ve maksimum aralığı dışında kalıyorsa, eylem bir uyarı mesajı veya hata mesajı olabilir.
-   Öznitelik için hedef değer. Bu değer, özniteliğin optimum değeridir ve tüm öznitelik türleri için geçerlidir.

**Serbest bırakılan ürünler** sayfasında seçtiğiniz ürünlere yönelik sayfalara Ürün bilgileri yönetiminde erişebilirsiniz. Bir ürüne toplu iş öznitelikleri atadıktan sonra, **Stok toplu iş öznitelikleri** sayfasında özniteliklere belirli değerler ekleyebilirsiniz.

## <a name="reserve-batches"></a>Toplu iş rezerve etme
Bir müşterinin siparişini yerine getirmek üzere bir satış emrine yönelik toplu iş rezervasyonları yaparken veya bir üretim emri için toplu işler çekip rezerve ederken toplu iş özniteliklerinde arama yapabilirsiniz. Arama istediğiniz toplu iş özniteliğine sahip ürünü içeren bir stok toplu işini bulmaya yardımcı olur. Toplu işi veya toplu işleri bulduktan sonra, ürünü kaynak stok hareket satırı için rezerve edebilirsiniz.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]