---
title: "Perakende ürünleri ayarlama"
description: "Bu makalede, Microsoft Dynamics 365 işlemleri - perakende perakende ürünleri kurmak nasıl açıklanır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 116c49174989ff14982027cc235640c2ad7322f2
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-retail-products"></a>Perakende ürünleri ayarlama

Bu makalede, Microsoft Dynamics 365 işlemleri - perakende perakende ürünleri kurmak nasıl açıklanır.

İkinci el ürünler, perakende kanalları sunma önce oluşturmak ve ürünleri Dynamics 365 işlemleri AX - perakende yapılandırmanız gerekir. Perakende ürün asıl kuruluş çapında ürünler oluşturmak için Dynamics 365 işlemleri için ürün özelliklerini kullanır. Ürünleri oluşturabilir, ürün özelliklerini ve özniteliklerini tanımlayabilir ve ürünü perakende kategorisi hiyerarşilerine atayabilirsiniz. Ürünü perakende kanallarınızda sunmak ve onları aktif bir çeşide eklemek için, ürünleri bulundukları tüzel kişiliklere serbest bırakmanız gerekir. Perakende kanalları kullanarak sattığınız ürünler ayarlamak için, aşağıdaki görevleri tamamlayın.

1.  Bir perakende ürün hiyerarşisi tanımlayın. İşlemler için Dynamics 365 içinde kategori hiyerarşisi özelliklerini kullanarak, gruplamak ve kategorilere ayırmak için perakende kanalları dağıtmak ürünleri perakende kategori sıradüzenleri tanımlayabilirsiniz. Kullanıcı tanımlı ve sistem öznitelikleri kategori düzeyinde tanımlanabilir. Daha sonra kategoriye atanmış tüm ürünler bu öznitelikleri devralır. Birden çok kategori hiyerarşisi tanımlanabilir ve her ürün birden çok hiyerarşiye atanabilir. Ancak, tek bir hiyerarşi içinde her ürün yalnızca bir kategoriye atanabilir.
2.  Ürün ve ürün varyantlarını ana ürüne ekleyin. Ana ürüne eklenen ürünler küresel ürün listesini temsil eder. Ürünleri el ile, tek seferde ekleyebilir veya ürün verilerini satıcınızdan içe aktarabilirsiniz.
3.  Ürünleri tüzel kişiliklere serbest bırakın. Yalnızca tüzel kişiliklere serbest bırakılmış ürünler perakende kanallarınızda sunulabilir. Bir ürünü ilk kez tanımlarken, onu organizasyon çapında bir düzeyde tanımlarsınız. Ardından ürünü serbest bırakacağınız bir veya daha fazla tüzel kişilik seçebilirsiniz. Ürün daha sonra organizasyonunuzdaki birden fazla perakende kanalında kullanılabilir hale gelir. Bu işlevselliği kullanarak bir seferde bir ürün oluşturabilir, bir yerde ürün öznitelikleri ve niteliklerini güncelleyebilir ve ardından ürünü organizasyonunuz boyunca kullanılabilir olduğu perakende kanallarına dağıtabilirsiniz.
4.  Ürünleri çeşitlere ekleyin. Bir çeşit, perakende kanallarınızda sunduğunuz bir ürün koleksiyonunu temsil eder. Bir veya daha fazla çeşit tanımlayabilirsiniz ve her bir ürüne bir veya daha fazla çeşit atanabilir. Ürünleri perakende kanallarına atamak için, çeşitleri bu perakende kanallarına atayın. Bir çeşit oluşturduğunuzda, henüz tüzel kişiliğe serbest bırakılmamış ürünleri ekleyebilirsiniz. Ancak, ürünleri perakende kanallarınızda sunabilmek için önce tüzel kişiliğe serbest bırakmanız gerekir.
5.  Ürünler için gezinme hiyerarşileri ekleyin. Ürünleri çevrimiçi veya satış (POS) giriş göz önce bunlar bir perakende Gezinti hiyerarşisinde kategorize gerekir.
6.  Ürün katalogları için ekleyin. Bu adım için POS isteğe bağlı olsa da, çevrimiçi mağazalar ürünleri en az bir kataloğa dahil edilmiş gerekir.



