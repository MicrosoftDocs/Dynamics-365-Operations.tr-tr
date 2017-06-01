---
title: "Perakende hiyerarşileri"
description: "Bu makalede Microsoft Dynamics AX&quot;teki perakende hiyerarşileri açıklanmıştır."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15851
ms.assetid: dfa11d41-2a0c-4cde-99b6-058c49176c94
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2544b299267ec6e21adf5c657c23f545fc66a0b3
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="retail-hierarchies"></a>Perakende hiyerarşileri

[!include[banner](includes/banner.md)]


Bu makalede Microsoft Dynamics AX'teki perakende hiyerarşileri açıklanmıştır.

Perakende kanallarınız üzerinden sattığınız ürünleri organize etmek için bir perakende kategori hiyerarşisi oluşturabilirsiniz. Ürünleri kategorize etmek veya gruplamak için perakende ürün hiyerarşilerini kullanabilirsiniz. Daha sonra, ürün çeşitleri ve müşteri bağlılık programları oluşturmak için bu ürünleri kullanabilirsiniz. Ayrıca, ürün öznitelikleri ve özellikler, fiyatlandırma yapısı atayabilir, ürün promosyonlarına ürün ekleyebilir ve raporlama için ürünleri kullanabilirsiniz. Tüm ürünleri ve kuruluşunuzdaki kategorileri temsil edecek bir perakende kategori hiyerarşisi oluşturun ve sonra bu kategori hiyerarşisini birden çok amaç için kullanabilirsiniz. Alternatif olarak, ürün promosyonları gibi özel amaçlar için birden fazla perakende kategori hiyerarşisi oluşturabilirsiniz. Perakende ürün hiyerarşisi oluşturduğunuzda, kategori hiyerarşisinin amacını belirlemek için bir kategori hiyerarşisi türü atamanız gerekir. Örneğin, ürünlere çevrimiçi veya satış noktası (POS) kategorisine göre göz atarken **Perakende gezinme hiyerarşisine** atanan tek ürün hiyerarşisi türüne başvurulur.

## <a name="retail-hierarchy-types"></a>Perakende hiyerarşisi türleri
Aşağıdaki tabloda kullanılabilir ve her bir türün genel amacına uygun perakende kategorisi türleri listelenir.

| Kategori hiyerarşisi türü       | Amaç                                                                                                                                                                                                                                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Perakende ürün hiyerarşisi      | Kuruluşunuzun genel ürün hiyerarşisini tanımlamak için bu hiyerarşi türünü kullanın. Bu hiyerarşi türünü alım satım, fiyatlandırma ve promosyonlar, raporlama ve ürün çeşidi planlaması için kullanabilirsiniz. Yalnızca tek bir perakende ürün hiyerarşisi bu hiyerarşi türüne atanabilir.                                       |
| Tamamlayıcı perakende hiyerarşisi | Oluşturmak istediğiniz her bir ek perakende kategori hiyerarşileri için bu hiyerarşi türünü kullanın. Örneğin, ilkbaharda mayolar için bir promosyonunuz var. O halde, mayo ürünlerini ayrı bir kategori hiyerarşisine eklersiniz ve çeşitli ürün kategorilerine promosyonlu fiyatlandırma uygularsınız. |
| Perakende gezinme hiyerarşisi   | Ürünleri çevrimiçi olarak veya satış noktasında göz atılabilmesi amacıyla gruplamak ve kategoriler halinde düzenlemek için bu hiyerarşi türünü kullanın.                                                                                                                                                                                       |

Ürünlerinizi yapılandırmak için bir perakende kategori hiyerarşisi kullanarak ürün özniteliklerini ve özelliklerini kategori düzeyinde ayarlayabilir ve sağlayabilirsiniz. Bu öznitelikler ve özellikler ürün boyutlarına ve POS ayarlarına ilişkin ayarlar içerir. Kategorilere atadığınız herhangi bir ürün, tanımladığınız öznitelikleri ve özellikleri otomatik olarak devralır. Herhangi bir ürünün özellik ayarlarını seçilen kategorideki birden çok ürüne de aynı anda kopyalayabilirsiniz.




