---
title: "Toplu iş öznitelikleri"
description: "Bu makalede toplu iş öznitelikleri hakkında bilgiler verilmiştir. Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir. Bu makalede ayrıca toplu iş özniteliklernin nasıl atanacağı ve toplu işleri rezere ettiğinizde bunları nasıl ayaryacağınız açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f23040177394558e95a13d16885814e83e5ebf99
ms.lasthandoff: 03/31/2017


---

# <a name="batch-attributes"></a>Toplu iş öznitelikleri

Bu makalede toplu iş öznitelikleri hakkında bilgiler verilmiştir. Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir. Bu makalede ayrıca toplu iş özniteliklernin nasıl atanacağı ve toplu işleri rezere ettiğinizde bunları nasıl ayaryacağınız açıklanmaktadır.

Toplu iş öznitelikleri, stok toplu işlerini oluşturan hammaddelerin ve tamamlanan ürünlerin özellikleridir. Toplu iş öznitelikleri, ortam koşulları veya toplu işi oluşturmak için kullanılan hammaddelerin kalitesi ya da bitmiş ürünün sonucu gibi çeşitli etkenlere bağlı olarak değişiklik gösterebilir. Kullanılan toplu iş özniteliklerinin sayısı ve tipleri, endüstriler arasında büyük değişiklikler gösterebilir. Toplu iş özniteliklerinin nasıl kullanıldığını gösteren iki örnek aşağıda verilmiştir:

-   Peynir endüstrisinde, peynir üretmekte kullanılan hammaddelerden biri olan süt, yağ içeriği ve yüzde ağırlık gibi özniteliklere sahip olabilir. Sütten üretilen peynirin nem ve yaş gibi başka öznitelikleri olabilir.
-   Çelik endüstrisinde, ürettiğiniz demir magnezyum, gümüş ve çinko içeriği yüzdeleri gibi özniteliklere sahip olabilir.

Öznitelik sayısını ve türünü daha iyi yönetmek için, toplu iş öznitelik grupları kullanabilirsiniz. Bu şekilde, her bir özniteliği tek tek eklemeniz gerekmez.

## <a name="assign-batch-attributes"></a>Toplu iş öznitelikleri atama
Toplu iş özniteliklerini, stok toplu işlerinde tutulan ürünlere tek tek atayabilir veya bunları belirli müşterilerle ilişkili ürünlere atarsınız. Müşteri düzeyinde bir toplu iş özniteliği atamadan önce, ürün düzeyinde atamanız gerekir. Ürünün toplu iş boyutu izleme boyut grubunda **Etkin** olarak ayarlanmış olmalıdır. Ayrı bir ürüne bir toplu iş özniteliği atamak için, ürüne özel sayfayı kullanın. Öznitelik, bir müşteriye yönelik bir ürüne özelse, müşteriye özel sayfayı kullanın. Bir ürüne öznitelik eklediğinizde, diğer parametreleri de tanımlarsınız. Burada bazı örnekler verilmiştir:

-   **Tamsayı** veya **Kesir** türünün özniteliği için minimum veya maksimum aralıklar.
-   Bir öznitelik için tolerans eylemleri **tamsayı** veya **kesir** türü. Özniteliğinin değeri en düşük ve en yüksek aralığın dışında kalırsa, işlem bir uyarı iletisi veya bir hata iletisi olabilir.
-   Öznitelik için hedef değer. Bu değer, özniteliğin optimum değeridir ve tüm öznitelik türleri için geçerlidir.

**Serbest bırakılan ürünler** sayfasında seçtiğiniz ürünlere yönelik sayfalara Ürün bilgileri yönetiminde erişebilirsiniz. Bir ürüne toplu iş öznitelikleri atadıktan sonra, **Stok toplu iş öznitelikleri** sayfasında özniteliklere belirli değerler ekleyebilirsiniz.

## <a name="reserve-batches"></a>Toplu iş rezerve etme
Bir müşterinin siparişini yerine getirmek üzere bir satış emrine yönelik toplu iş rezervasyonları yaparken veya bir üretim emri için toplu işler çekip rezerve ederken toplu iş özniteliklerinde arama yapabilirsiniz. Arama istediğiniz toplu iş özniteliğine sahip ürünü içeren bir stok toplu işini bulmaya yardımcı olur. Toplu işi veya toplu işleri bulduktan sonra, ürünü kaynak stok hareket satırı için rezerve edebilirsiniz.


