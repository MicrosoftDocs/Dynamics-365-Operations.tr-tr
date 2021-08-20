---
title: Boyut oluşturma ve boyut üyelerini içe aktarma
description: Maliyet muhasebesi diğer modüllerden alınan ana verilere ihtiyaç duyan bağımsız modüldür.
author: ShylaThompson
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6febb8a48cf6496fb7f4c2ee9f5281d47aa1ccae1a8ecc51c908b3810302e11c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775134"
---
# <a name="create-dimensions-and-import-dimension-members"></a>Boyut oluşturma ve boyut üyelerini içe aktarma

[!include [banner](../includes/banner.md)]

Maliyet muhasebesi diğer modüllerden alınan verilere ihtiyaç duyan bağımsız modüldür. Bu veri aşağıdaki şekilde sınıflandırılır:

-  Maliyet öğeleri
-  Maliyet nesneleri
-  İstatistiksel boyutlar

**Maliyet öğesi** hesap planında maliyetle ilgili bir öğeye karşılık gelir. Bir **Maliyet nesnesi**, ürünler, maliyet merkezleri ve projeler gibi maliyetleri tahmin etmek, tahsis etmek ve doğrudan ölçmek istediğiniz herhangi bir türdeki mali boyuta karşılık gelir. Bir **İstatistiksel boyut** ve üyeleri, parasal olmayan girişleri kaydetmek için kullanılır. İstatistiksel boyut üyelerini tahsisat maliyet dağılımı ve maliyet tahsisatı gibi tahsisat temeli olarak kullanılabilir 

Aşağıdaki diyagram, Maliyet muhasebesinde kullanılan boyutları gösterir.

[![Maliyet muhasebesi boyutları.](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)

Verinin tamamı Maliye muhasebesine aktarıldıktan sonra, kuruluşun tüm seviyesindeki yöneticilere bilgi sağlayacak perspektifler oluşturmak üzere bunu kullanabilirsiniz. Aşağıdaki konular, boyutlar oluşturma ve boyut üyelerini içe aktarma konusunda bilgi sağlar. 

-  [Maliyet öğesi boyutları](cost-elements.md)
-  [Maliyet öğeleri oluşturma](./tasks/create-cost-elements.md)
-  [Maliyet nesnesi boyutları](cost-objects.md)
-  [Maliyet öğesi boyutu üyelerini ortak bir boyut öğeleri kümesiyle eşleme](map-cost-elements-dimension-members.md)
-  [Maliyet öğesi boyutunu eşleştirme](./tasks/map-cost-element-dimension.md)
-  [İstatistiksel boyut üyeleri ve istatistiksel ölçü sağlayıcısı şablonları](statistical-measure-provider-template.md)








[!INCLUDE[footer-include](../../includes/footer-banner.md)]