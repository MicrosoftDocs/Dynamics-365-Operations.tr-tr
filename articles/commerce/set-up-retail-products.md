---
title: Perakende ürünleri ayarlama
description: Bu makale, perakende ürünlerini Dynamics 365 Commerce içinde ayarlamayı anlatır.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailProductAndCategoryWorkspace, EcoResProductDetails
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
ms.openlocfilehash: e8f624f5feb8ee8f641a9b35ae31bdfe38e5e0ce
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024340"
---
# <a name="set-up-retail-products"></a>Perakende ürünlerini ayarlama

[!include [banner](includes/banner.md)]

Bu makale, ürünlerini Dynamics 365 Commerce içinde ayarlamayı anlatır.

Ürünleri ticaret kanallarınızda yeniden satışa sunabilmeniz için oluşturmanız ve yapılandırmanız gerekir. Commerce, ana üründe organizasyon genelinde ürünler oluşturur. Ürünleri oluşturabilir, ürün özelliklerini ve özniteliklerini tanımlayabilir ve ürünleri ticaret kategorisi hiyerarşilerine atayabilirsiniz. Ürünleri kanallarınızda sunmak ve etkin bir ürün çeşidine eklemek için kullanılabilecekleri tüzel kişiliklerde serbest bırakmanız gerekir. Kanalları kullanarak sattığınız ürünler ayarlamak için, aşağıdaki görevleri tamamlayın.

1. **Bir ürün hiyerarşisi tanımlayın.** Commerce'teki kategori hiyerarşisi özelliklerini kullanarak, kanallarınıza dağıttığınız ürünleri gruplandırmak ve kategorize etmek için kategorisi hiyerarşileri tanımlayabilirsiniz. Kullanıcı tanımlı ve sistem öznitelikleri kategori düzeyinde tanımlanabilir. Daha sonra kategoriye atanmış tüm ürünler bu öznitelikleri devralır. Birden çok kategori hiyerarşisi tanımlanabilir ve her ürün birden çok hiyerarşiye atanabilir. Ancak, tek bir hiyerarşi içinde her ürün yalnızca bir kategoriye atanabilir.
2. **Ürün ve ürün varyantlarını ana ürüne ekleyin.** Ana ürüne eklenen ürünler küresel ürün listesini temsil eder. Ürünleri el ile, tek seferde ekleyebilir veya ürün verilerini satıcınızdan içe aktarabilirsiniz.
3. **Ürünleri tüzel kişiliklere serbest bırakın.** Yalnızca bir tüzel kişilik için serbest bırakılan ürünler kanallarınız tarafından kullanılabilir. Bir ürünü ilk kez tanımlarken, onu organizasyon çapında bir düzeyde tanımlarsınız. Ardından ürünü serbest bırakacağınız bir veya daha fazla tüzel kişilik seçebilirsiniz. Ürün daha sonra organizasyonunuzdaki birden fazla kanalında kullanılabilir hale gelir. Bu işlevselliği kullanarak bir seferde bir ürün oluşturabilir, bir yerde ürün öznitelikleri ve niteliklerini güncelleyebilir ve ardından ürünü organizasyonunuz boyunca kullanılabilir olduğu kanallarına dağıtabilirsiniz.
4. **Ürünleri çeşitlere ekleyin.** Bir çeşit, kanallarınızda sunduğunuz bir ürün koleksiyonunu temsil eder. Bir veya daha fazla çeşit tanımlayabilirsiniz ve her bir ürüne bir veya daha fazla çeşit atanabilir. Ürünleri kanallarına atamak için, çeşitleri bu kanallarına atayın. Bir çeşit oluşturduğunuzda, henüz tüzel kişiliğe serbest bırakılmamış ürünleri ekleyebilirsiniz. Ancak, ürünleri kanallarınızda sunabilmek için önce tüzel kişiliğe serbest bırakmanız gerekir.
5. **Ürünleri gezinme hiyerarşilerine ekleyin.** Ürünlerin çevrimiçi veya satış noktasında (POS) ziyaret alabilmesi için, bir Commerce gezinme hiyerarşisinde kategorize edilmeleri gerekir.
6. **Ürünleri kataloglara ekleyin.** Bu adım POS için isteğe bağlı olmasına rağmen, çevrimiçi mağazalar ürünlerin en az bir kataloğa dahil edilmesini gerektirir.
