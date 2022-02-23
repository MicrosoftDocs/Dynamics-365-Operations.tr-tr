---
title: Commerce hiyerarşileri
description: Bu konu, Dynamics 365 Commerce içinde hiyerarşilerini açıklar.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: OMHierarchyManager, EcoResCategoryHierarchyFactbox
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8f7e4d01970f459f66934fe434ec7307104b39b2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416519"
---
# <a name="commerce-hierarchies"></a>Commerce hiyerarşileri

[!include [banner](includes/banner.md)]

Bu konu, Dynamics 365 Commerce içinde hiyerarşilerini açıklar.

Kanallarınız üzerinden sattığınız ürünleri organize etmek için bir kategori hiyerarşisi oluşturabilirsiniz. Ürünleri kategorize etmek veya gruplamak için ürün hiyerarşilerini kullanabilirsiniz. Daha sonra, ürün çeşitleri ve müşteri bağlılık programları oluşturmak için bu ürünleri kullanabilirsiniz. Ayrıca, ürün öznitelikleri ve özellikler, fiyatlandırma yapısı atayabilir, ürün promosyonlarına ürün ekleyebilir ve raporlama için ürünleri kullanabilirsiniz. Tüm ürünleri ve kuruluşunuzdaki kategorileri temsil edecek bir kategori hiyerarşisi oluşturun ve sonra bu kategori hiyerarşisini birden çok amaç için kullanabilirsiniz. Alternatif olarak, ürün promosyonları gibi özel amaçlar için birden fazla kategori hiyerarşisi oluşturabilirsiniz. Ürün hiyerarşisi oluşturduğunuzda, kategori hiyerarşisinin amacını belirlemek için bir kategori hiyerarşisi türü atamanız gerekir. Örneğin, ürünlere çevrimiçi veya satış noktası (POS) kategorisine göre göz atarken **Commerce gezinme hiyerarşisine** atanan tek ürün hiyerarşisi türüne başvurulur.

## <a name="hierarchy-types"></a>Hiyerarşi türü

Aşağıdaki tabloda kullanılabilir ve her bir türün genel amacına uygun kategorisi türleri listelenir.

| Kategori hiyerarşisi türü       | Amaç |
|-------------------------------|---------|
| Ürün hiyerarşisi      | Kuruluşunuzun genel ürün hiyerarşisini tanımlamak için bu hiyerarşi türünü kullanın. Bu hiyerarşi türünü alım satım, fiyatlandırma ve promosyonlar, raporlama ve ürün çeşidi planlaması için kullanabilirsiniz. Yalnızca tek bir ürün hiyerarşisi bu hiyerarşi türüne atanabilir. |
| Tamamlayıcı hiyerarşisi | Oluşturmak istediğiniz her bir ek kategori hiyerarşileri için bu hiyerarşi türünü kullanın. Örneğin, ilkbaharda mayolar için bir promosyonunuz var. O halde, mayo ürünlerini ayrı bir kategori hiyerarşisine eklersiniz ve çeşitli ürün kategorilerine promosyonlu fiyatlandırma uygularsınız. |
| Gezinme hiyerarşisi   | Ürünleri çevrimiçi olarak veya satış noktasında göz atılabilmesi amacıyla gruplamak ve kategoriler halinde düzenlemek için bu hiyerarşi türünü kullanın. |

Ürünlerinizi yapılandırmak için bir kategori hiyerarşisi kullanarak ürün özniteliklerini ve özelliklerini kategori düzeyinde ayarlayabilir ve sağlayabilirsiniz. Bu öznitelikler ve özellikler ürün boyutlarına ve POS ayarlarına ilişkin ayarlar içerir. Kategorilere atadığınız herhangi bir ürün, tanımladığınız öznitelikleri ve özellikleri otomatik olarak devralır. Herhangi bir ürünün özellik ayarlarını seçilen kategorideki birden çok ürüne de aynı anda kopyalayabilirsiniz.
