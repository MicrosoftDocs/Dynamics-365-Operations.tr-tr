---
title: Servis düzeyi ve açıklaması
description: Bu konuda Varlık Yönetimi'ndeki düzeyleri ve açıklamaları açıklanmaktadır.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d50955d510dca21c3de160fd280ff53ba54926a5
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356476"
---
# <a name="service-level-and-description"></a>Servis düzeyi ve açıklaması

[!include [banner](../../includes/banner.md)]

 

Bir iş emri oluşturduğunuzda, ilgili servis düzeylerini tanımlamak ve buna genel bir açıklama eklemek isteyebilirsiniz. **İş emri servis düzeyleri** sayfasında iş emri servis düzeylerini ve **İş emri açıklama** sayfasıyla ilgili açıklamaları oluşturabilirsiniz.

## <a name="create-a-service-level"></a>Servis düzeyi oluşturma

1. **Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Servis düzeyi**'ni seçin.
2. **Yeni**'yi seçin.
3. **Servis düzeyi** alanına, servis düzeyini (örneğin bir sayı) girin.
4. **Ad** alanına, bir ad girin.

    **İş emirleri** hızlı sekmesinde, beklenen başlangıç ve bitiş tarihleri ile saatlerini tanımlayabilirsiniz. Bu hızlı sekmedeki alanlar, iş emirlerinin başlaması gereken ve sona erdirildiği dönemi tanımlar. El ile oluşturulan ve bakım taleplerinde oluşturulan iş emirlerinin bulunduğu iş emirleri için kullanılırlar. 

5. **Başlangıç günü** alanına, iş emrinin başlaması gereken dönemi tanımlamak için bir gün sayısı girin. Gün sayısı, iş emrinin yaratılış tarihinden itibaren hesaplanır. Örneğin, iş emri oluşturulurken başlaması gerekiyorsa **0** girin. İş emri oluşturulduktan sonraki bir hafta içinde başlaması gerekirse, **7** girin.
6. Başlangıç tarihine ek olarak, iş emri başlangıç saatini ayarlamak için **Başlangıç saatini ayarla** seçeneğini **Evet** olarak ayarlayın. Sonra **Başlangıç saati** alanına başlangıç saatini girin. Seçeneği **Hayır** olarak ayarlarsanız günün geçerli saati kullanılır.
7. **Bitiş günü** alanına, iş emrinin bitmesi gereken dönemi tanımlamak için bir gün sayısı girin. Gün sayısı, iş emrinin başlangıç tarihinden itibaren hesaplanır. Örneğin, iş emrinin başlangıç tarihinin bir hafta içinde bitmesi gerekiyorsa, **7** girin.
8. Bitiş tarihine ek olarak, iş emri bitiş saatini ayarlamak için **Bitiş saatini ayarla** seçeneğini **Evet** olarak ayarlayın. Sonra **Bitiş saati** alanına bitiş saatini girin. Seçeneği **Hayır** olarak ayarlarsanız günün geçerli saati kullanılır.
9. **Kaydet**'i seçin.

![İş emri hizmet düzeyi sayfası.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Açıklama oluştur

1. **Kıymet yönetimi** \> **Kurulum** \> **İş emirleri** \> **Açıklamalar**'ı seçin.
2. **Yeni**'yi seçin.
3. **Açıklama** alanına bir açıklama girin.
4. **Kaydet**'i seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]