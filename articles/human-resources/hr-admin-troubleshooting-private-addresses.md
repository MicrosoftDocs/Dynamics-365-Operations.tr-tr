---
title: Güvenlik rolüne göre özel adreslere erişim
description: Bu konu, bir müşterinin özel adreslere erişemediği sorunun çözümünü açıklar.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15616a9b3673a4c1842e389b976a80d599e2e77f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346334"
---
# <a name="access-to-private-addresses-by-security-role"></a>Güvenlik rolüne göre özel adreslere erişim

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Stok çıkışı**

Bir müşteri, bir güvenlik rolünü çoğalttıktan sonra ve yeni rol ile oturum açtığında, müşteri özel olarak işaretlenmiş adresleri göremez.

**Çözünürlük**

Bu sorunu gidermek için müşterinin çoğaltılan güvenlik rolü için bu adımları izlemesi gerekmektedir.

1. **Kuruluş yönetimi \> Genel adres defteri \> Genel adres defteri parametreleri seçeneğine gidin.**
2. **Özel konum güvenliği** sekmesinde, yeni güvenlik rolünü **Kullanılabilir roller** listesinden **Seçilen roller** listesine taşıyın.
3. **Kaydet**'i seçin.

![Genel adres defteri parametreleri sayfası.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]