---
title: NF-e özel sertifika doğrulaması
description: Bu makalede, NF-e özel sertifikasını etkinleştirme ve kullanma hakkında bilgi sağlanmaktadır.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288559"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e özel sertifika doğrulaması

[!include [banner](../includes/banner.md)]

Brezilya Kök Sertifika Yetkilisi tarafından verilen sertifikalardaki **Sunucu kimlik doğrulama amacı** özelliği varsayılan olarak kapalıdır ve el ile etkinleştirilmesi gerekir. Bazı durumlarda, otomatik sertifika güncelleştirme bu özelliği artık etkin olmayacak şekilde değiştirebilir. Bu durumda TLS bağlantısı etkilenir ve artık güvenilir olmayabilir. Minas Gerais (MG) ve Paraná (PR) eyaletlerinin üretim ortamlarında Brezilya elektronik mali belge modeli 55'i (NF-e) verme yeteneği de etkilenebilir.

**NF-e özel sertifika doğrulaması** için düzeltmeyi etkinleştirmek üzere **Özellik yönetimi**'ne gidin. Bu özellik, V5 ve V10 sertifika doğrulamaları için alternatif bir çözüm sağlar ve NF-e'nin güvenli iletimi ve SEFAZ'den yetkilendirme alımı için gereken web hizmetleriyle güvenilir bağlantıya olanak tanır.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
