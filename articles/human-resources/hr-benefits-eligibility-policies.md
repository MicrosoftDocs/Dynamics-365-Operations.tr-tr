---
title: Kazanca uygunluk ilkeleri
description: Bu konuda, belirli kazançlar için kimlerin uygun olduğunu tanımlayan kazanç uygunluk ilkeleri hakkında bilgi verilmektedir.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 88b801be5be4f9abcec4632fe1d96dbd83aaec96
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416941"
---
# <a name="benefit-eligibility-policies"></a>Kazanca uygunluk ilkeleri

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, belirli kazançlar için kimlerin uygun olduğunu tanımlayan kazanç uygunluk ilkeleri hakkında bilgi verilmektedir.

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






[!INCLUDE[footer-include](../includes/footer-banner.md)]
