---
title: "Perakende ürünleri ayarlama"
description: "Bu makalede, Microsoft Dynamics 365 for Retail'de perakende ürünlerin nasıl ayarlanacağı açıklanmaktadır."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 85b794bb1a1a7a4e9b0e811d90408ed8872a6f0a
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-retail-products"></a>Perakende ürünleri ayarlama

[!include[banner](includes/banner.md)]


Bu makalede, Microsoft Dynamics 365 for Retail'de perakende ürünlerin nasıl ayarlanacağı açıklanmaktadır.

Perakende kanallarınızda ürünleri yeniden satışa sunmadan önce ürünleri Dynamics 365 for Retail içinde oluşturmanız ve yapılandırmanız gerekir. Perakende, Dynamics 365 for Retail içindeki ürün özelliklerini kullanarak ana üründe kuruluş çapında ürünler oluşturur. Ürünleri oluşturabilir, ürün özelliklerini ve özniteliklerini tanımlayabilir ve ürünü perakende kategorisi hiyerarşilerine atayabilirsiniz. Ürünü perakende kanallarınızda sunmak ve onları aktif bir çeşide eklemek için, ürünleri bulundukları tüzel kişiliklere serbest bırakmanız gerekir. Perakende kanalları kullanarak sattığınız ürünler ayarlamak için, aşağıdaki görevleri tamamlayın.

1.  Bir perakende ürün hiyerarşisi tanımlayın. Dynamics 365 for Retail'deki kategori hiyerarşisi özelliklerini kullanarak, perakende kanallarınıza dağıttığınız ürünleri gruplandırmak ve kategorize etmek için perakende kategorisi hiyerarşileri tanımlayabilirsiniz. Kullanıcı tanımlı ve sistem öznitelikleri kategori düzeyinde tanımlanabilir. Daha sonra kategoriye atanmış tüm ürünler bu öznitelikleri devralır. Birden çok kategori hiyerarşisi tanımlanabilir ve her ürün birden çok hiyerarşiye atanabilir. Ancak, tek bir hiyerarşi içinde her ürün yalnızca bir kategoriye atanabilir.
2.  Ürün ve ürün varyantlarını ana ürüne ekleyin. Ana ürüne eklenen ürünler küresel ürün listesini temsil eder. Ürünleri el ile, tek seferde ekleyebilir veya ürün verilerini satıcınızdan içe aktarabilirsiniz.
3.  Ürünleri tüzel kişiliklere serbest bırakın. Yalnızca tüzel kişiliklere serbest bırakılmış ürünler perakende kanallarınızda sunulabilir. Bir ürünü ilk kez tanımlarken, onu organizasyon çapında bir düzeyde tanımlarsınız. Ardından ürünü serbest bırakacağınız bir veya daha fazla tüzel kişilik seçebilirsiniz. Ürün daha sonra organizasyonunuzdaki birden fazla perakende kanalında kullanılabilir hale gelir. Bu işlevselliği kullanarak bir seferde bir ürün oluşturabilir, bir yerde ürün öznitelikleri ve niteliklerini güncelleyebilir ve ardından ürünü organizasyonunuz boyunca kullanılabilir olduğu perakende kanallarına dağıtabilirsiniz.
4.  Ürünleri çeşitlere ekleyin. Bir çeşit, perakende kanallarınızda sunduğunuz bir ürün koleksiyonunu temsil eder. Bir veya daha fazla çeşit tanımlayabilirsiniz ve her bir ürüne bir veya daha fazla çeşit atanabilir. Ürünleri perakende kanallarına atamak için, çeşitleri bu perakende kanallarına atayın. Bir çeşit oluşturduğunuzda, henüz tüzel kişiliğe serbest bırakılmamış ürünleri ekleyebilirsiniz. Ancak, ürünleri perakende kanallarınızda sunabilmek için önce tüzel kişiliğe serbest bırakmanız gerekir.
5.  Ürünleri gezinme hiyerarşilerine ekleyin. Ürünlerin çevrimiçi veya satış noktasında (POS) ziyaret alabilmesi için, bir Perakende gezinme hiyerarşisinde kategorize edilmeleri gerekir.
6.  Ürünleri kataloglara ekleyin. Bu adım POS için isteğe bağlı olmasına rağmen, çevrimiçi mağazalar ürünlerin en az bir kataloğa dahil edilmesini gerektirir.





