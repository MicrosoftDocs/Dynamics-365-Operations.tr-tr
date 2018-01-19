---
title: Kazanca uygunluk ilkeleri
description: "Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 682100881d6ea8c1e02db50629208c765600c49a
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="benefit-eligibility-policies"></a>Kazanca uygunluk ilkeleri

[!include[banner](includes/banner.md)]


Bu konu, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.

Kazançlar oluşturduğunuzda hangi kazançların hangi çalışanlar için geçerli olacağına karar verirsiniz. Aşağıdaki tabloda belirli çalışanlar için geçerli hale getirilebilecek kazançlara örnekler verilmiştir.

| Kazanç          | Kazanç kimin için geçerli olur |
|------------------|---------------------------------|
| Sağlık sigortası | Tüm çalışanlar                   |
| Cep telefonu     | Satış personeli, idareciler         |
| Park geçişleri   | İdareciler                      |

Aşağıdaki bileşenler, uygunluk politikalarının oluşturulması için kullanılır:

-   Politika kuralı türleri
-   Kazanca uygunluk ilkeleri

Politika kuralı türleri, belirli politika kuralları geliştirdiğinizde kullanılan sorgu parametrelerini tanımlar. Politika kuralı türleri oluşturduktan sonra kazanç uygunluk politikaları oluşturabilirsiniz. Politikalar bir veya birden fazla tüzel kişilik için geçerli bir kurallar topluluğu oluşturmanızı sağlar. Her bir politika kapsamında, daha önceden oluşturduğunuz kazanç uygunluk politikası kural türlerinden herhangi birini görüntüleyebilirsiniz. 

Kuralın kapsamını politikada tanımlarsınız. Örneğin, **Yönetici** adında bir kazanç uygunluk politikası kural türü tanımlandığınızda hangi kuralın hangi politika kapsamında olduğunu belirtebilirsiniz. Bu örnekte, "yönetici" sözcüğü içeren tüm iş unvanlarının kurala dahil edilmesini belirtebilirsiniz. Politikaya dahil edilen kuralın veya kuralların parametrelerini tanımladıktan sonra kazanca belirli bir kural atayabilirsiniz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Bir kazanç programı tanımlama ve yönetme](manage-benefit-program.md)




