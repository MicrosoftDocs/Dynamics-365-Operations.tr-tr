---
title: NF-e özel sertifika doğrulaması
description: Bu konu, NF-e özel sertifikasını etkinleştirme ve kullanma hakkında bilgi sağlar.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755603"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e özel sertifika doğrulaması

[!include [banner](../includes/banner.md)]

Brezilya Kök Sertifika Yetkilisi tarafından verilen sertifikalardaki **Sunucu kimlik doğrulama amacı** özelliği varsayılan olarak kapalıdır ve el ile etkinleştirilmesi gerekir. Bazı durumlarda, otomatik sertifika güncelleştirme bu özelliği artık etkin olmayacak şekilde değiştirebilir. Bu durumda TLS bağlantısı etkilenir ve artık güvenilir olmayabilir. Minas Gerais (MG) ve Paraná (PR) eyaletlerinin üretim ortamlarında Brezilya elektronik mali belge modeli 55'i (NF-e) verme yeteneği de etkilenebilir.

**NF-e özel sertifika doğrulaması** için düzeltmeyi etkinleştirmek üzere **Özellik yönetimi**'ne gidin. Bu özellik, V5 ve V10 sertifika doğrulamaları için alternatif bir çözüm sağlar ve NF-e'nin güvenli iletimi ve SEFAZ'den yetkilendirme alımı için gereken web hizmetleriyle güvenilir bağlantıya olanak tanır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
