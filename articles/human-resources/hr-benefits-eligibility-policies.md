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
ms.openlocfilehash: e1f64a0beffe12f6b4e0ad53d3bbaa96822dc7e8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066055"
---
# <a name="benefit-eligibility-policies"></a>Kazanca uygunluk ilkeleri


[!INCLUDE [PEAP](../includes/peap-1.md)]

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
