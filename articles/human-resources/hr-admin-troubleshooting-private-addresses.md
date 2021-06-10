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
ms.openlocfilehash: 2edcef338f0ff8fcf231d4314fc972284397d000
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053335"
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

![Genel adres defteri parametreleri sayfası](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]