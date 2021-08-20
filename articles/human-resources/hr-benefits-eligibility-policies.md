---
title: Kazanca uygunluk ilkeleri
description: Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8f0f51bc701af3f5dec2d393a87f589729af147bf44a56c4995991631f0d6379
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727173"
---
# <a name="benefit-eligibility-policies"></a>Kazanca uygunluk ilkeleri

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, kazanç uygunluk ilkeleri hakkında, belirli kazançlara uygun olan kişileri tanımlamanıza yardımcı olacak bilgiler verilmektedir.

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