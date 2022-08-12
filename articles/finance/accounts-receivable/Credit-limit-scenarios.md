---
title: Kredi limiti senaryoları
description: Bu makalede, müşteri bir müşteri kredi limiti grubuna ait olduğunda müşteri kredi limitinin nasıl denetlendiği açıklanır.
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130268"
---
# <a name="credit-limit-scenarios"></a>Kredi limiti senaryoları

Kredi yönetiminde, müşteri düzeyinde müşterilere bir kredi limiti atanabilir. Her müşteri bir *müşteri kredi limiti grubuna* atanabilir ve her grubun kredi limiti vardır. Bu nedenle, kredi limitinde, grup düzeyinde müşterilere bir kredi limiti atanabilir. Aynı müşteri kredi grubuna atanan tüm müşteriler aynı kredi limitine sahiptir.

Genel olarak, grup kredi limitleri bireysel kredi limitlerinin önünde kontrol edilir. Bireysel kredi limiti, grup kredi limitini her zaman geçersiz kılmaz.

Bu makalede, müşteri kredi grupları ve bağımsız kredi limitleriyle ilgili beş senaryo açıklanmaktadır.

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>Müşteri grubu kredi limiti, bireysel kredi limitinden daha fazladır

Örneğin müşterinin, 10.000 $ bireysel kredi limiti vardır. Müşteri bir müşteri kredi grubuna atanmıştır ve grubun kredi limiti 15.000 $'dır. Bu durumda, müşterinin "etkili kredi limiti", bu tutar grup sınırından az olduğu için 10.000 $'dır. Durdurma kuralları önce grup limitini denetler. Ardından bireysel limiti denetler. 10.000 $ üzerindeki tüm siparişler bloke edilecektir.

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>Bireysel kredi limiti, müşteri grubu kredi limitinden daha fazladır

Örneğin müşterinin, 20.000 $ bireysel kredi limiti vardır. Müşteri bir müşteri kredi grubuna atanmıştır ve grubun kredi limiti 15.000 $'dır. Bu durumda, müşterinin etkili kredi limiti, durdurma kuralları her zaman önce grup limitini denetlediği için 15.000 $'dır. 15.000 $ üzerindeki tüm satış siparişler bloke edilecektir.

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>Bireysel kredi limiti 0,00 olarak ve Zorunlu kredi limiti ise Evet olarak ayarlanır

Müşterinin bireysel kredi limiti **0,00** olarak ayarlanmışsa ve **Zorunlu kredi limiti** seçeneği **Evet** olarak ayarlanmışsa müşteri bir müşteri kredi grubuna atanmış olsa bile müşterinin etkin kredi limiti  0,00$'dır. Bu şekilde, müşteri bir grubun parçası olabilir, ancak tüm siparişler Kredi yönetimine gider.

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>Bireysel kredi limiti 0,00 olarak ve Sınırsız kredi limiti ise Evet olarak ayarlanır

Müşterinin bireysel kredi limiti **0,00** olarak ayarlanmışsa ancak **Sınırsız kredi limiti** seçeneği **Evet** olarak ayarlanmışsa bir müşteri kredi grubuna atanmış olsa bile müşteri sınırsız krediye sahip olur.

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>Bireysel kredi limiti 0,00 olarak ayarlanmış ve müşteri bir müşteri kredi grubunun parçası ise

Örneğin müşterinin **0,00** olarak ayarlanan bireysel kredi limiti varsa **Sınırsız kredi** seçeneği **Hayır** olarak ayarlanır ve **Zorunlu kredi limiti** seçeneği **Hayır** olarak ayarlanır. Müşteri bir müşteri kredi grubuna atanmıştır ve grubun kredi limiti 15.000 $'dır. Bu durumda, müşterinin etkin kredi limiti, grubun limiti olan 15.000 $'dır. Bu nedenle, bu tutar üzerinden yapılan satış siparişleri bloke edilir. Bu davranış, kredi limitinin müşteri kredi grubu düzeyinde tek bir müşteri düzeyi yerine yönetilmesini sağlar. Aynı gruba atanan tüm müşteriler aynı kredi limitine sahiptir.
