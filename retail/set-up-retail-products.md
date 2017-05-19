---
title: "Perakende ürünleri ayarlama"
description: "Bu makalede, Microsoft Dynamics 365 for Operations - Perakende&quot;de perakende ürünlerin nasıl ayarlanacağı açıklanmaktadır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 4f565bd5563cbcf9079f3220dd855f41889f1d5e
ms.contentlocale: tr-tr
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-retail-products"></a>Perakende ürünleri ayarlama

[!include[banner](includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Operations - Perakende'de perakende ürünlerin nasıl ayarlanacağı açıklanmaktadır.

Perakende kanallarınızda ürün satışa sunabilmek için önce ürünleri Dynamics 365 for Operations AX - Perakende içinde oluşturup yapılandırmanız gerekir. Perakende, Dynamics 365 for Operations'taki ürün özelliklerini kullanarak ana üründe kuruluş çapında ürünler oluşturur. Ürünleri oluşturabilir, ürün özelliklerini ve özniteliklerini tanımlayabilir ve ürünü perakende kategorisi hiyerarşilerine atayabilirsiniz. Ürünü perakende kanallarınızda sunmak ve onları aktif bir çeşide eklemek için, ürünleri bulundukları tüzel kişiliklere serbest bırakmanız gerekir. Perakende kanalları kullanarak sattığınız ürünler ayarlamak için, aşağıdaki görevleri tamamlayın.

1.  Bir perakende ürün hiyerarşisi tanımlayın. Dynamics 365 for Operations'taki kategori hiyerarşisi özelliklerini kullanarak, perakende kanallarınıza dağıttığınız ürünleri gruplandırmak ve kategorize etmek için perakende kategorisi hiyerarşileri tanımlayabilirsiniz. Kullanıcı tanımlı ve sistem öznitelikleri kategori düzeyinde tanımlanabilir. Daha sonra kategoriye atanmış tüm ürünler bu öznitelikleri devralır. Birden çok kategori hiyerarşisi tanımlanabilir ve her ürün birden çok hiyerarşiye atanabilir. Ancak, tek bir hiyerarşi içinde her ürün yalnızca bir kategoriye atanabilir.
2.  Ürün ve ürün varyantlarını ana ürüne ekleyin. Ana ürüne eklenen ürünler küresel ürün listesini temsil eder. Ürünleri el ile, tek seferde ekleyebilir veya ürün verilerini satıcınızdan içe aktarabilirsiniz.
3.  Ürünleri tüzel kişiliklere serbest bırakın. Yalnızca tüzel kişiliklere serbest bırakılmış ürünler perakende kanallarınızda sunulabilir. Bir ürünü ilk kez tanımlarken, onu organizasyon çapında bir düzeyde tanımlarsınız. Ardından ürünü serbest bırakacağınız bir veya daha fazla tüzel kişilik seçebilirsiniz. Ürün daha sonra organizasyonunuzdaki birden fazla perakende kanalında kullanılabilir hale gelir. Bu işlevselliği kullanarak bir seferde bir ürün oluşturabilir, bir yerde ürün öznitelikleri ve niteliklerini güncelleyebilir ve ardından ürünü organizasyonunuz boyunca kullanılabilir olduğu perakende kanallarına dağıtabilirsiniz.
4.  Ürünleri çeşitlere ekleyin. Bir çeşit, perakende kanallarınızda sunduğunuz bir ürün koleksiyonunu temsil eder. Bir veya daha fazla çeşit tanımlayabilirsiniz ve her bir ürüne bir veya daha fazla çeşit atanabilir. Ürünleri perakende kanallarına atamak için, çeşitleri bu perakende kanallarına atayın. Bir çeşit oluşturduğunuzda, henüz tüzel kişiliğe serbest bırakılmamış ürünleri ekleyebilirsiniz. Ancak, ürünleri perakende kanallarınızda sunabilmek için önce tüzel kişiliğe serbest bırakmanız gerekir.
5.  Ürünleri gezinme hiyerarşilerine ekleyin. Ürünlerin çevrimiçi veya satış noktasında (POS) ziyaret alabilmesi için, bir Perakende gezinme hiyerarşisinde kategorize edilmeleri gerekir.
6.  Ürünleri kataloglara ekleyin. Bu adım POS için isteğe bağlı olmasına rağmen, çevrimiçi mağazalar ürünlerin en az bir kataloğa dahil edilmesini gerektirir.





